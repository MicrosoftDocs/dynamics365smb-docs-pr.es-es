---
title: "Acerca de la funcionalidad de planificación | Documentos de Microsoft"
description: "El programa de planificación tiene en cuenta todos los datos del aprovisionamiento y la demanda, cuadra el resultado y genera sugerencias para hacer que el aprovisionamiento satisfaga la demanda."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0910760881decc98ba1bfa6e8753566316386b2c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="about-planning-functionality"></a>Sobre la funcionalidad de la planificación
El programa de planificación tiene en cuenta todos los datos del aprovisionamiento y la demanda, cuadra el resultado y genera sugerencias para hacer que el aprovisionamiento satisfaga la demanda.  

Para obtener información detallada, consulte [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md).  

> [!NOTE]  
> En todos los campos que se mencionan en este tema, lea la información de herramienta para entender su función. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Aprovisionamiento y demanda  
La planificación tiene dos elementos: demanda y aprovisionamiento. Dichos elementos se deben equilibrar para garantizar que la demanda se satisface de manera puntual y rentable.  

- Demanda es el término habitual usado para todo tipo de necesidades brutas: pedido de venta, pedido de servicio, necesidad de componentes de órdenes de producción, pedidos de ensamblado, transferencia de salida, pedido abierto o previsión. Además de todos ellos, el programa admite algunos otros tipos técnicos de demanda, por ejemplo una orden de producción o un pedido de compra negativos, existencias negativas y devoluciones de compras.  
- Aprovisionamiento es el término habitual utilizado para todo tipo de reposición: existencias, pedido de compra, pedido de ensamblado, orden de producción o transferencia de entrada. En correspondencia, puede haber un pedido de venta o de servicio negativo, una necesidad de componente negativa o una devolución de ventas; todos ellos, de alguna forma, representan también un aprovisionamiento.  

Otro objetivo del sistema de planificación es el de garantizar que las existencias no aumentan innecesariamente. En el caso de un descenso de la demanda, el programa de planificación sugerirá que se pospongan o cancelen algunos de los pedidos de reposición existentes, o que se reduzca sus cantidades.  

## <a name="planning-calculation"></a>Cálculo de la planificación  
El programa de planificación está controlado por la demanda, estimada y real, de los clientes, además de los parámetros de reaprovisionamiento de existencias. Si se ejecuta el cálculo de la planificación, el programa sugerirá acciones concretas (mensajes de acción) que se deben emprender en relación con una posible reposición de los proveedores, transferencias entre almacenes, o producción. Si ya hay pedidos de reposición, las acciones sugeridas pueden ser aumentar o acelerar los pedidos para satisfacer los cambios de la demanda.  

La base de la rutina de planificación es el cálculo bruto-neto. Las necesidades netas controlan la emisión de pedidos planificados, que se programan en función de la información sobre rutas (productos fabricados) o el plazo de seguridad de la ficha de producto (productos comprados). Las cantidades de los pedidos planificados se basan en el cálculo de la planificación y se ven afectadas por los parámetros definidos en cada una de las fichas de producto.  

## <a name="planning-with-manual-transfer-orders"></a>Planificación con pedidos de transferencia manuales
Como se puede ver en el campo **Sistema reposición** de una ficha de unidad de almacenamiento, el programa de planificación se puede configurar para que cree pedidos de transferencia que equilibren el suministro y la demanda entre los distintos almacenes.  

Además de dichos pedidos de transferencia automáticos, puede que a veces sea necesario realizar un traslado general de cantidades en existencia a otro almacén, independientemente de la demanda existente. Para ello debería crear manualmente un pedido de transferencia con la cantidad que trasladar. Para garantizar que el sistema de planificación no intenta manipular este pedido de transferencia manual, debe establecer el campo **Flexibilidad de planificación** de las líneas de transferencia en Ninguna.  

Por el contrario, si desea que el sistema de planificación ajuste las cantidades del pedido de transferencia y las fechas para la demanda existente, debe establecer el campo **Flexibilidad de planificación** en el valor predeterminado, Ilimitada.

## <a name="planning-parameters"></a>Parámetros de la planificación  
Los parámetros de la planificación controlan cuándo, en qué cantidad y cómo realizar el reaprovisionamiento, en función de diversas opciones de la ficha de producto (o unidad de almacenamiento, SKU) y de la configuración de la fabricación.  

Existen los siguientes parámetros de planificación en la ficha del producto o de la UA:  

-   Periodo amortiguador  
-   Cantidad amortiguador  
-   Directiva reaprov.  
-   Punto pedido
-   Stock máximo  
-   Nivel desbordamiento  
-   Ciclo  
-   Periodo de acumulación de lotes  
-   Periodo de reprogramación  
-   Cantidad a pedir  
-   Plazo de seguridad  
-   Stock de seguridad  
-   Directiva de ensamblado  
-   Política fabricación  

Existen los modificadores de pedido en la ficha del producto o de la UA:  

-   Cantidad mínima pedido  
-   Cantidad máxima pedido  
-   Múltiplos de pedido  

Los campos de configuración de planificación global de la ventana **Configuración de fabricación** son:  

-   Código nivel más bajo dinámico  
-   Previsión prod. actual  
-   Previsiones en almacénes  
-   Plazo seguridad genérico  
-   Nivel desbordamiento en blanco  
-   Combinar cálc. MPS/MRP   
-   Componentes en alm.  
-   Periodo predet. amortiguador  
-   Cantidad predet. amortiguador  

Para obtener más información, consulte [Detalles de diseño: parámetros de planificación](design-details-planning-parameters.md).  

## <a name="other-important-planning-fields"></a>Otros campos importantes de planificación
### <a name="planning-flexibility"></a>Flexib. planificación
En la mayoría de pedidos de suministros, como pedidos de producción, puede seleccionar **Ilimitada** o **Ninguna** en el campo **Flexibilidad de planificación** en las líneas.

Esto especifica si el sistema de planificación tiene en cuenta el suministro representado en la línea del pedido de producción al calcular mensajes de acción.
Si el campo contiene la opción **Ilimitada**, el sistema de planificación incluye la línea cuando calcula mensajes de acción. Si en el campo está especificada la opción **Ninguna**, la línea es firme e invariable, y el sistema de planificación no la incluye al calcular los mensajes de acción.

### <a name="warning"></a>Advertencia
El campo de información **Advertencia**, la ventana **Hoja de planificación** le indica las líneas de planificación creadas para una situación inusual, con un texto que el usuario puede elegir para leer información adicional. Existen los siguientes tipos de advertencia:

- Emergencia
- Excepción
- Atención
- Emergencia

La advertencia de emergencia se muestra en dos situaciones:

- El inventario es negativo en la fecha de inicio de la planificación.
- Existen eventos de demanda u oferta atrasados.

Si el inventario de un producto es negativo en la fecha de inicio de la planificación, el sistema de planificación le sugiere un pedido de suministro de emergencia para la cantidad negativa que llegue en la fecha de inicio de la planificación. El texto de advertencia informa de tal fecha y de la cantidad del pedido de emergencia.

Todas las líneas de documento con fecha de vencimiento antes de la fecha de inicio de la planificación se consolidan en un pedido de demanda de emergencia para que el elemento llegue en la fecha de inicio de la planificación.

### <a name="exception"></a>Excepción
Se mostrará la advertencia de excepción si el inventario disponible previsto cae por debajo de la cantidad de existencias de seguridad.

El programa de planificación sugerirá un pedido de suministros para cubrir la demanda en la fecha de vencimiento. El texto de advertencia informa de la cantidad de existencias de seguridad del producto y de la fecha en la que se infringe.

Infringir el nivel de existencias de seguridad está considerado una excepción debido a que no debería ocurrir si se configura correctamente el punto de nuevo pedido.

> [!NOTE]
> El suministro de las líneas de planificación con advertencias de excepción no se modifica normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere solo un suministro para satisfacer la cantidad exacta de demanda. Sin embargo, puede configurar la ejecución de la planificación para que respete ciertos parámetros de planificación para las líneas de planificación con determinadas advertencias. Para obtener más información, vea la sección sobre cómo "respetar los parámetros de planificación para las advertencias de excepción" en Calcular plan - Plan. Hoja.

### <a name="attention"></a>Atención
La advertencia de atención se muestra en dos situaciones:

- La fecha de inicio de la planificación es anterior a la fecha de trabajo.
- La línea de planificación sugiere cambiar una compra realizada o una orden de producción.

> [!NOTE]
> En las líneas de planificación con advertencias, el campo **Aceptar mensaje acción** está desactivado, ya que se espera que el planificador investigue estás líneas más detalladamente antes de llevar a cabo el plan.

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  
[Planificación](production-planning.md)   
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

