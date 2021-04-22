---
title: 'Detalles de diseño: Transferencias en planificación | Documentos de Microsoft'
description: En este tema se describe cómo usar pedidos de transferencia como origen de provisión al planificar los niveles de inventario.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 64e3a85a4a57a229d23070d7453729b46979d97e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785165"
---
# <a name="design-details-transfers-in-planning"></a>Detalles de diseño: Transferencias en planificación
Los pedidos de transferencia también son un origen de suministro al trabajar en el nivel de UA. Al usar varias ubicaciones (almacenes), el sistema de reposición de UA se puede configurar en Transferencia, lo que implica que se realiza la reposición de la ubicación mediante la transferencia de mercancías desde otra ubicación. En una situación con varios almacenes, las empresas pueden tener una cadena de transferencias donde el aprovisionamiento al almacén VERDE se transfiere de AMARILLO, y el aprovisionamiento a AMARILLO se transfiere desde ROJO, etc. En el principio de la cadena hay un sistema de reposición de Ord. prod. o Compra.  

![Ejemplo de flujo de transferencia](media/nav_app_supply_planning_7_transfers1.png "Ejemplo de flujo de transferencia")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Al comparar la situación en que un pedido de suministro atiende directamente un pedido de demanda para una situación en que el pedido de venta se suministra a través de una cadena de transferencias de UA, es evidente que la tarea de planificación en esta última situación puede llegar a ser muy compleja. Si la demanda cambia, puede causar un efecto de ondulación a través de la cadena, ya que tendrán que manipularse todos los pedidos de transferencia más el pedido de compra o la orden de producción en el extremo opuesto de la cadena para volver a establecer el saldo entre la demanda y el aprovisionamiento.  

![Ejemplo de equilibrio entre la oferta y la demanda en transferencias](media/nav_app_supply_planning_7_transfers2.png "Ejemplo de equilibrio entre la oferta y la demanda en transferencias")  

## <a name="why-is-transfer-a-special-case"></a>¿Por qué la transferencia es un caso especial?  
Un pedido de transferencia se parece mucho a cualquier otro pedido en la aplicación. No obstante, lo que ocurre en un segundo plano es muy diferente.  

Un aspecto fundamental que diferencia las transferencias en la planificación de los pedidos de compra y de las órdenes de producción es que una línea de transferencia representa la demanda y el suministro al mismo tiempo. La parte de salida, que se envía desde la ubicación anterior, es demanda. La parte de entrada, que se recibirá en la nueva ubicación, es el suministro de esa ubicación.  

![Contenido de la página Orden de transferencia](media/nav_app_supply_planning_7_transfers3.png "Contenido de la página Orden de transferencia")  

Esto significa que, cuando el sistema manipula la parte de suministro de la transferencia, se debe realizar un cambio similar en la parte de demanda.  

## <a name="transfers-are-dependent-demand"></a>Las transferencias dependen de la demanda  
La demanda y el suministro relacionados tienen cierta similitud con los componentes de una línea de orden de producción, pero la diferencia está en que los componentes estarán en el siguiente nivel de planificación y con un producto distinto, mientras que las dos partes de la transferencia se encuentran en el mismo nivel, para el mismo producto.  

Una similitud importante es que, tal y como los componentes dependen de la demanda, igualmente lo hace la demanda de transferencia. La demanda de una línea de transferencia se indica mediante la parte de suministro de la transferencia en el sentido de que, si cambia el suministro, la demanda se ve afectada directamente.  

A menos que la flexibilidad de planificación sea Ninguna, una línea de transferencia nunca se debe tratar como demanda independiente en la planificación.  

En el procedimiento de planificación, la demanda de transferencia debe tenerse en consideración solo después de que el lado de aprovisionamiento haya sido procesado por el sistema de planificación. Antes de esto no se conoce la demanda real. Por lo tanto, la secuencia de los cambios realizados es muy importante cuando se trata de pedidos de transferencia.  

## <a name="planning-sequence"></a>Secuencia de planificación  
En la ilustración siguiente se muestra el aspecto que podría tener una cadena de transferencias.  

![Ejemplo de flujo de transferencia simple](media/nav_app_supply_planning_7_transfers4.png "Ejemplo de flujo de transferencia simple")  

En este ejemplo, un cliente solicita el producto en el almacén VERDE. El suministro al almacén VERDE se realiza mediante una transferencia desde el almacén ROJO. El suministro al almacén ROJO se realiza mediante transferencia desde producción en la ubicación AZUL.  

En este ejemplo, el sistema de planificación empezará con la demanda del cliente e irá retrocediendo a través de la cadena. Las demandas y los suministros se procesarán en una ubicación al mismo tiempo.  

![Planificación de suministros con transferencias](media/nav_app_supply_planning_7_transfers5.png "Planificación de suministros con transferencias")  

## <a name="transfer-level-code"></a>Cód. nivel transfer.  
La secuencia en que se procesan las ubicaciones en el sistema de planificación se determina mediante el código de nivel de transferencia de UA.  

El código de nivel de transferencia es un campo interno que se calcula automáticamente y se almacena en la UA cuando se crea o se modifica la UA. El cálculo se ejecuta en todos los UA para una determinada combinación de producto o variante y usa el código de almacén y de procedencia de la transferencia para determinar la ruta que tendrá que usar la planificación cuando recorra las UA para garantizar que se procesan todas las demandas.  

El código de nivel de transferencia será 0 para las UA con pedido de compra o de producción del sistema de reposición y será -1 para el primer nivel de transferencia, -2 para el segundo, y así sucesivamente. En la cadena de transferencia descrita anteriormente, los niveles serían -1 para ROJO y -2 para VERDE, como se muestra en la ilustración siguiente.  

![Contenido de la página Ficha UA](media/nav_app_supply_planning_7_transfers6.gif "Contenido de la página Ficha UA")  

Al actualizar una UA, el sistema de planificación detectará si las UA con la transferencia del sistema de reposición están configuradas con referencias circulares.  

## <a name="planning-transfers-without-sku"></a>Transferencias de planificación sin UA  

Aunque no se utilice la característica de la unidad de almacenamiento, es posible utilizar almacenes y hacer transferencias manuales entre almacenes. Para las empresas con configuración de almacén menos avanzada, el sistema de planificación admite casos donde el inventario existente se transfiere manualmente a otra ubicación, por ejemplo para cubrir un pedido de venta en ese almacén. Al mismo tiempo, el sistema de planificación debe reaccionar a los cambios de la demanda.  

Para usar las transferencias manuales, la planificación analizará los pedidos de transferencia existentes y, a continuación, planificará el orden en que se deben procesar las ubicaciones. Internamente, el sistema de planificación operará con UA temporales con códigos de nivel de transferencia.  

![Código de nivel de transferencia](media/nav_app_supply_planning_7_transfers7.png "Código de nivel de transferencia")  

Si hay más transferencias para un almacén determinado, el primer pedido de transferencia definirá la dirección de la planificación. Se cancelarán las transferencias que vayan en dirección opuesta.  

## <a name="changing-quantity-with-reservations"></a>Cambio de cantidad con reservas  
Al cambiar las cantidades en el suministro existente, el sistema de planificación tiene en cuenta las reservas en el sentido en que la cantidad reservada representa el límite inferior de hasta cuánto se puede reducir el suministro.  

Al cambiar la cantidad de una línea de pedido de transferencia existente, tenga en cuenta que el límite inferior se definirá como la cantidad reservada máxima de una línea de transferencia de salida y de entrada.  

Por ejemplo, si una línea de pedido de transferencia de 117 piezas está reservada con respecto a una línea de venta de 46 y una línea de compra de 24, no es posible reducir la línea de transferencia por debajo de las 46 piezas, aunque esto pueda representar un exceso de aprovisionamiento en el lado de entrada.  

![Reservas en planificación de transferencia](media/nav_app_supply_planning_7_transfers8.png "Reservas en planificación de transferencia")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Cambio de cantidad en un cadena de transferencia  
En el ejemplo siguiente, el punto de partida es una situación equilibrada con una cadena de transferencia que suministra un pedido de venta de 27 en el almacén ROJO con un pedido de compra correspondiente en el almacén AZUL, transferido a través del almacén ROSA. Por lo tanto, aparte de ventas y compras, hay dos pedidos de transferencia: AZUL-ROSA y ROJO-ROSA.  

![Cambiar la cantidad en la planificación de transferencia 1](media/nav_app_supply_planning_7_transfers9.png "Cambiar la cantidad en la planificación de transferencia 1")  

Ahora, el planificador en el almacén ROSA decide hacer la reserva según la compra.  

![Cambiar la cantidad en la planificación de transferencia 2](media/nav_app_supply_planning_7_transfers10.png "Cambiar la cantidad en la planificación de transferencia 2")  

Normalmente significa que el sistema de planificación omitirá el pedido de compra y la demanda de transferencia. Siempre que haya saldo no habrá problema. Pero, ¿qué sucede cuando el cliente en el almacén ROJO se arrepiente del pedido y lo cambia a 22?  

![Cambiar la cantidad en la planificación de transferencia 3](media/nav_app_supply_planning_7_transfers11.png "Cambiar la cantidad en la planificación de transferencia 3")  

Cuando el sistema de planificación se ejecuta de nuevo, debe eliminar el exceso de suministro. No obstante, la reserva bloqueará la compra y la transferencia a una cantidad de 27.  

![Cambiar la cantidad en la planificación de transferencia 4](media/nav_app_supply_planning_7_transfers12.png "Cambiar la cantidad en la planificación de transferencia 4")  

La transferencia ROSA-ROJA se ha reducido a 22. La parte de entrada de la transferencia AZUL-ROSA no está reservada, pero como la parte de salida está reservada, no es posible reducir la cantidad por debajo de 27.  

## <a name="lead-time-calculation"></a>Plazo entrega (días)  
Al calcular la fecha de vencimiento de un pedido de transferencia, se tendrán en cuenta varios tipos de plazos.  

Los plazos que están activos al planificar un pedido de transferencia son:  

* Tiempo manip. alm. salida  
* Tiempo envío  
* Tiempo manip. alm. entrada  
* En la línea de planificación, se usan los siguientes campos para proporcionar información sobre el cálculo.  
* Fecha envío transfer.  
* Fecha inicial  
* Fecha final  
* Fecha vencimiento  

La fecha de envío de la línea de transferencia se mostrará en el campo Fecha envío transfer., y la fecha de recepción de la línea de transferencia se mostrará en el campo Fecha vencimiento.  

Las fechas iniciales y finales se usarán para describir el periodo de transporte real.  

En la ilustración siguiente se muestra la interpretación de la fecha-hora inicial y la hora-fecha final de las líneas de planificación relacionadas con los pedidos de transferencia.  

![Fechas-horas centrales en la planificación de transferencia](media/nav_app_supply_planning_7_transfers13.png "Fechas-horas centrales en la planificación de transferencia")  

En este ejemplo, esto significa que:  

* Fecha de envío + Manipulación en salida = Fecha de inicio  
* Fecha inicial + Tiempo de envío = Fecha final  
* Fecha final + Tiempo manip. alm. entrada = Fecha recepción  

## <a name="safety-lead-time"></a>Plazo de seguridad  
El campo Plazo seguridad genérico de la página Configuración fabricación y el campo Plazo de seguridad relacionado de la ficha de producto no se tendrán en cuenta en el cálculo de un pedido de transferencia. No obstante, el plazo de seguridad seguirá influenciando en el plan total, ya que afectará al pedido de reabastecimiento (compra o producción) al comienzo de la cadena de transferencia cuando los productos se coloquen en la ubicación desde la que se transferirán.  

![Elementos de la fecha de vencimiento de la transferencia](media/nav_app_supply_planning_7_transfers14.png "Elementos de la fecha de vencimiento de la transferencia")  

En la línea de la orden de producción, la Fecha final + Plazo de seguridad + Tiempo manip. alm. entrada = Fecha vencimiento.  

En la línea del pedido de compra, la Fecha recep. planificada + Plazo de seguridad + Tiempo manip. alm. entrada = Fecha recepción esperada.  

## <a name="reschedule"></a>Reprogramar  
Al reprogramar una línea de transferencia existente, el sistema de planificación debe buscar la parte de salida y modificar la fecha y hora en ella. Es importante recordar que si se ha definido un plazo, habrá discontinuidad entre envío y recepción. Tal como se ha dicho, el plazo de entrega puede tener más elementos, como tiempo de transporte y tiempo de manipulación en el almacén. En una escala de tiempo, el sistema de planificación retrocederá en el tiempo mientras cuadra los elementos.  

![Cambiar la fecha de vencimiento en la planificación de transferencia](media/nav_app_supply_planning_7_transfers15.png "Cambiar la fecha de vencimiento en la planificación de transferencia")  

Por lo tanto, al modificar la fecha de vencimiento de una línea de transferencia, el plazo se debe calcular para actualizar la parte de salida de la transferencia.  

## <a name="seriallot-numbers-in-transfer-chains"></a>Números de serie y de lote en cadenas de transferencias  
Si la demanda incluye números de serie o lote y se ejecuta el motor de planificación, generará algunos pedidos de transferencia creados directamente. Para obtener más información acerca de este concepto, consulte Atributos de producto. Si, no obstante, se eliminan números de serie y lote de la demanda, los pedidos de transferencia creados en la cadena aún llevarán números de serie y de lote, por lo que se ignorarán en la planificación (no eliminados).  

## <a name="order-to-order-links"></a>Vínculos de pedido a pedido  
En este ejemplo, la UA AZUL se ha configurado con la directiva de reaprovisionamiento de pedido, mientras que los almacenes ROSA y ROJO usan la de lote por lote. Cuando se crea un pedido de venta de 27 en la ubicación ROJA, generará una cadena de transferencias y la última unión en la ubicación AZUL se reservará con enlace. En este ejemplo, las reservas no son reservas firmes creadas por el planificador en el almacén ROSA, sino uniones creadas por el sistema de planificación. La diferencia importante es que el sistema de planificación puede cambiar esto último.  

![Vínculos de pedido a pedido en la planificación de transferencia](media/nav_app_supply_planning_7_transfers16.png "Vínculos de pedido a pedido en la planificación de transferencia")  

Si la demanda cambia de 27 a 22, el sistema bajará la cantidad a lo largo de la cadena, reduciendo también la reserva vinculante.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Demanda en almacén vacío](design-details-demand-at-blank-location.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]