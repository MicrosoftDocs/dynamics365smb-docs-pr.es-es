---
title: 'Detalles de diseño: Transferencias en planificación'
description: Aprenda cómo usar pedidos de transferencia como origen de provisión al planificar los niveles de inventario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a><a name="design-details-transfers-in-planning"></a><a name="design-details-transfers-in-planning"></a>Detalles de diseño: Transferencias en planificación

Los pedidos de transferencia también son un origen de suministro al trabajar en el nivel de UA. Al usar varias ubicaciones (almacenes), el sistema de reposición de UA se puede configurar en Transferencia, lo que implica que se realiza la reposición de la ubicación mediante la transferencia de mercancías desde otra ubicación. En una situación con más almacenes, es posible que tenga una cadena de transferencias. El suministro a la ubicación VERDE se transfiere desde AMARILLO, el suministro a AMARILLO se transfiere desde ROJO, y así sucesivamente. En el principio de la cadena hay un sistema de reposición de **Or. prod.** o **Compra**.  

![Ejemplo de flujo de transferencia.](media/nav_app_supply_planning_7_transfers1.png "Ejemplo de flujo de transferencia")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Si compara las siguientes situaciones, es evidente que la tarea de planificación en esta última puede volverse compleja:

* Un pedido de suministro da la cara directamente a un pedido de demanda
* Un pedido de venta se suministra a través de una cadena de transferencias de SKU

Si la demanda cambia, podría causar un efecto dominó a lo largo de la cadena. Todos los pedidos de transferencia, más el pedido de compra y producción en el extremo opuesto de la cadena, deberán actualizarse para reequilibrar la oferta y la demanda.  

![Ejemplo de equilibrio entre la oferta y la demanda en transferencias.](media/nav_app_supply_planning_7_transfers2.png "Ejemplo de equilibrio entre la oferta y la demanda en transferencias")  

## <a name="why-is-a-transfer-a-special-case"></a><a name="why-is-a-transfer-a-special-case"></a><a name="why-is-a-transfer-a-special-case"></a>¿Por qué la transferencia es un caso especial?

Los pedidos de transferencia son similares a los demás pedidos, como los pedidos de compra o producción. No obstante, lo que ocurre en un segundo plano es diferente.  

Una diferencia consiste en que una línea de transferencia representa tanto la demanda como la oferta. La parte saliente que se envía es la demanda. La parte de entrada que se recibe en el nuevo almacén es el suministro de ese almacén.  

![Contenido de la página Orden de transferencia.](media/nav_app_supply_planning_7_transfers3.png "Contenido de la página Orden de transferencia")  

Cuando [!INCLUDE [prod_short](includes/prod_short.md)] cambia la parte de suministro de la transferencia, debe realizar un cambio similar en la parte de demanda.  

## <a name="transfers-are-dependent-demand"></a><a name="transfers-are-dependent-demand"></a><a name="transfers-are-dependent-demand"></a>Las transferencias dependen de la demanda

La relación de la oferta y la demanda es similar a la de los componentes en las líneas de pedidos de producción. La diferencia radica en que los componentes de las líneas de pedido de producción están en el siguiente nivel de planificación y tienen un producto diferente. Las dos partes de la transferencia están en el mismo nivel para el mismo producto.  

Una similitud importante es que los componentes y las transferencias dependen de la demanda. La demanda de una línea de transferencia está dictada por el lado de la oferta de la transferencia. Si la oferta cambia, la demanda se ve directamente afectada.

A menos que la flexibilidad de planificación sea Ninguna, una línea de transferencia no se debe tratar como demanda independiente en la planificación.  

En el procedimiento de planificación, la demanda de transferencia debe tenerse en consideración solo después de que el sistema de planificación haya procesado el lado de la oferta. Antes de que se produzca ese procesamiento, no se conoce la demanda real. La secuencia de modificaciones es importante para los pedidos de transferencia.  

## <a name="planning-sequence"></a><a name="planning-sequence"></a><a name="planning-sequence"></a>Secuencia de planificación

La siguiente imagen muestra un ejemplo de una cadena de transferencias.  

![Ejemplo de flujo de transferencia simple.](media/nav_app_supply_planning_7_transfers4.png "Ejemplo de flujo de transferencia simple")  

En este ejemplo, un cliente solicita el producto en el almacén VERDE. El suministro al almacén VERDE se realiza mediante una transferencia desde el almacén ROJO. El suministro al almacén ROJO se realiza mediante transferencia desde producción en la ubicación AZUL.  

En este ejemplo, el sistema de planificación empieza con la demanda del cliente y va retrocediendo a través de la cadena. Las demandas y las ofertas se procesan para un almacén al mismo tiempo.  

![Planificación de suministros con transferencias.](media/nav_app_supply_planning_7_transfers5.png "Planificación de suministros con transferencias")  

## <a name="transfer-level-code"></a><a name="transfer-level-code"></a><a name="transfer-level-code"></a>Código de nivel de transferencia

El código de nivel de transferencia del SKU determina la secuencia en que el sistema de planificación procesa los almacenes.  

El código de nivel de transferencia es un campo interno. El campo se calcula y almacena en el SKU cuando se crea o modifica el SKU. El cálculo se ejecuta en todos los SKU de una combinación dada de producto y variante de producto. El cálculo usa el código de almacén y el código de origen de la transferencia para determinar la ruta a usar para los SKU. El cálculo garantiza que se procesen todas las demandas.  

El código de nivel de transferencia será 0 para las SKU con pedido de compra o de producción del sistema de reposición y será -1 para el primer nivel de transferencia, -2 para el segundo, y así sucesivamente. En el ejemplo descrito en la sección anterior, los niveles deben ser -1 para ROJO y -2 para VERDE, como se muestra en la ilustración siguiente.  

![Contenido de la página Ficha UA.](media/nav_app_supply_planning_7_transfers6.gif "Contenido de la página Ficha UA")  

Al actualizar un SKU, el sistema de planificación detecta los sistemas de reposición de los SKU tienen referencias circulares.  

## <a name="planning-transfers-without-sku"></a><a name="planning-transfers-without-sku"></a><a name="planning-transfers-without-sku"></a>Transferencias de planificación sin SKU

Para configuraciones de almacén menos avanzadas, puede usar almacenes y realizar transferencias manuales entre almacenes, incluso si no usa SKU. Por ejemplo, la transferencia puede cubrir un pedido de ventas en ese almacén. El sistema de planificación reacciona a los cambios de la demanda.  

Para las transferencias manuales, el sistema de planificación analiza los pedidos de transferencia ya existentes y, a continuación, planea el orden en que se deben procesar los almacenes. Internamente, el sistema de planificación usa SKU temporales con códigos de nivel de transferencia.  

![Código de nivel de transferencia.](media/nav_app_supply_planning_7_transfers7.png "Código de nivel de transferencia")  

Si hay varias transferencias a un almacén, el primer pedido de transferencia define la dirección de la planificación. Las transferencias en dirección opuesta se cancelarán.  

## <a name="changing-quantity-with-reservations"></a><a name="changing-quantity-with-reservations"></a><a name="changing-quantity-with-reservations"></a>Cambio de cantidad con reservas

Al cambiar las cantidades de una oferta, el sistema de planificación tiene en cuenta las reservas. La cantidad reservada representa el límite inferior de cuánto reducir la oferta.  

Cuando cambie la cantidad de una línea de pedido de transferencia, tenga en cuenta el límite inferior. El límite inferior es la cantidad reservada más alta de las líneas de transferencia salientes y entrantes.

Por ejemplo, una línea de pedido de transferencia de 117 piezas se reserva para las siguientes líneas:

* Una línea de venta de 46
* Una línea de compra de 24

Aunque en el lado entrante pueda haber un exceso de oferta, no puede reducir la línea de transferencia por debajo de 46.  

![Reservas en planificación de transferencia.](media/nav_app_supply_planning_7_transfers8.png "Reservas en planificación de transferencia")  

## <a name="changing-quantity-in-a-transfer-chain"></a><a name="changing-quantity-in-a-transfer-chain"></a><a name="changing-quantity-in-a-transfer-chain"></a>Cambio de cantidad en un cadena de transferencia

Este es un ejemplo de lo que sucede cuando cambia una cantidad en un cambio de transferencia.

El punto de partida es una situación equilibrada con una cadena de transferencia que suministra un pedido de venta de 27 en el almacén ROJO. Hay un pedido de compra correspondiente en el almacén AZUL. Ambas transferencias pasan por el almacén ROSA. Hay dos pedidos de transferencia, AZUL-ROSA y ROSA-ROJO.  

![Cambiar la cantidad en la planificación de transferencia 1.](media/nav_app_supply_planning_7_transfers9.png "Cambiar la cantidad en la planificación de transferencia 1")  

Ahora, el planificador del almacén ROSA decide hacer la reserva de la compra.  

![Cambiar la cantidad en la planificación de transferencia 2.](media/nav_app_supply_planning_7_transfers10.png "Cambiar la cantidad en la planificación de transferencia 2")  

Normalmente la reserva significa que el sistema de planificación omite el pedido de compra y la demanda de transferencia. No hay ningún problema siempre que haya un equilibrio. Pero, ¿qué sucede cuando el almacén ROJO cambia el pedido de 27 a 22?  

![Cambiar la cantidad en la planificación de transferencia 3.](media/nav_app_supply_planning_7_transfers11.png "Cambiar la cantidad en la planificación de transferencia 3")  

Cuando el sistema de planificación se ejecuta de nuevo, debe eliminar el exceso de suministro. No obstante, la reserva bloquea la compra y la transferencia a una cantidad de 27.  

![Cambiar la cantidad en la planificación de transferencia 4.](media/nav_app_supply_planning_7_transfers12.png "Cambiar la cantidad en la planificación de transferencia 4")  

La transferencia ROSA-ROJA se ha reducido a 22. La parte de entrada de la transferencia AZUL-ROSA no está reservada, pero la parte de salida sí. La reserva significa que no se puede reducir la cantidad por debajo de 27.  

## <a name="lead-time-calculation"></a><a name="lead-time-calculation"></a><a name="lead-time-calculation"></a>Cálculo del plazo

Al calcular la fecha de vencimiento de un pedido de transferencia, se tienen en cuenta varios tipos de plazos.  

Los plazos siguientes están activos al planificar un pedido de transferencia:  

* Tiempo de manipulación del almacén de salida  
* Tiempo de envío  
* Tiempo de manipulación de almacén de entrada  

En la línea de planificación, se usan los siguientes campos para proporcionar información sobre el cálculo:  

* Fecha envío transfer.  
* Fecha inicial  
* Fecha final  
* Fecha de vencimiento  

La fecha de envío de la línea de transferencia se muestra en el campo **Fecha envío transfer.** La fecha de recepción de la línea de transferencia se muestra en el campo **Fecha vencimiento**.  

Las fechas iniciales y finales describen el periodo de transporte real.  

En la imagen siguiente se muestra la interpretación de la fecha-hora inicial y la hora-fecha final de las líneas de planificación de los pedidos de transferencia.  

![Fechas-horas centrales en la planificación de transferencia.](media/nav_app_supply_planning_7_transfers13.png "Fechas-horas centrales en la planificación de transferencia")  

El ejemplo muestra los siguientes cálculos:  

* Fecha de envío + Manipulación en salida = Fecha de inicio  
* Fecha inicial + Tiempo de envío = Fecha final  
* Fecha final + Tiempo manip. alm. entrada = Fecha recepción  

## <a name="safety-lead-time"></a><a name="safety-lead-time"></a><a name="safety-lead-time"></a>Plazo de seguridad

El campo **Plazo seguridad genérico** de la página **Configuración fabricación** y el campo **Plazo de seguridad** de la página **Ficha producto** no están incluidos en el cálculo del pedido de transferencia. Sin embargo, el plazo de seguridad influye en el plan total. El plazo de seguridad afecta al pedido de reabastecimiento (compra o producción) al comienzo de la cadena de transferencia. Ese es el punto donde se colocaron los productos en el almacén desde el que se transferirán.  

![Elementos de la fecha de vencimiento de la transferencia.](media/nav_app_supply_planning_7_transfers14.png "Elementos de la fecha de vencimiento de la transferencia")  

En la línea de la orden de producción, la Fecha final + Plazo de seguridad + Tiempo manip. alm. entrada = Fecha vencimiento.  

En la línea del pedido de compra, la Fecha recep. planificada + Plazo de seguridad + Tiempo manip. alm. entrada = Fecha recepción esperada.  

## <a name="reschedule"></a><a name="reschedule"></a><a name="reschedule"></a>Reprogramar

Al reprogramar una línea de transferencia, el sistema de planificación buscar la parte de salida y modifica la fecha y hora.

> [!NOTE]
> Si se ha definido un plazo, habrá discontinuidad entre el envío y la recepción. El plazo puede tener más elementos, como tiempo de transporte y tiempo de manipulación en el almacén. En una escala de tiempo, el sistema de planificación retrocede en el tiempo mientras cuadra los elementos.  

![Cambiar la fecha de vencimiento en la planificación de transferencia.](media/nav_app_supply_planning_7_transfers15.png "Cambiar la fecha de vencimiento en la planificación de transferencia")  

Al modificar la fecha de vencimiento de una línea de transferencia, el plazo se debe calcular para actualizar la parte de salida de la transferencia.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a><a name="serial-and-lot-numbers-in-transfer-chains"></a><a name="serial-and-lot-numbers-in-transfer-chains"></a>Números de serie y de lote en cadenas de transferencias

Si la demanda usa números de serie o lote y se ejecuta el motor de planificación, se crearán pedidos de transferencia. Para obtener más información acerca de este concepto, consulte Atributos de producto. Sin embargo, si se eliminan números de serie o lote de la demanda, los pedidos de transferencia seguirán usando los números de serie y de lote, y la planificación no los tendrá en cuenta (no eliminados).  

## <a name="order-to-order-links"></a><a name="order-to-order-links"></a><a name="order-to-order-links"></a>Vínculos de pedido a pedido

En este ejemplo, el SKU AZUL está configurado con una directiva de reaprovisionamiento **Pedido**. Los SKU ROSA y ROJO tienen la directiva de reaprovisionamiento **Lote a lote**. La creación de un pedido de venta de 27 en el almacén ROJO conduce a una cadena de transferencias. La última transferencia está en el almacén AZUL y está reservada con un enlace. En este ejemplo, las reservas no son reservas firmes creadas por el planificador en el almacén ROSA. El sistema de planificación crea los enlaces. La diferencia importante es que el sistema de planificación puede cambiar esto último.  

![Vínculos de pedido a pedido en la planificación de transferencia.](media/nav_app_supply_planning_7_transfers16.png "Vínculos de pedido a pedido en la planificación de transferencia")  

Si la demanda cambia de 27 a 22, el sistema de planificación bajará la cantidad a lo largo de la cadena. La reserva vinculante también se reducirá.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles del diseño: Planificación con o sin almacenes](production-planning-with-without-locations.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
