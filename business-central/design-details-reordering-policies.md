---
title: "Detalles de diseño: Directivas de reaprovisionamiento | Documentos de Microsoft"
description: "Este tema proporciona un resumen de las políticas para la reposición de producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4aaef129da953596632b56716eaff2f0c47736f7
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-reordering-policies"></a>Detalles de diseño: Directivas de reaprovisionamiento
Las directivas de reaprovisionamiento definen cuánto se debe pedir cuando se debe reponer el producto. Hay cuatro directivas de reaprovisionamiento.  

## <a name="fixed-reorder-qty"></a>Cdad. fija reaprov.
La directiva Cdad. fija reaprov. está relacionada con la planificación de inventario de los productos C típicos (coste de inventario bajo, poco riesgo de obsolescencia o muchos productos). Normalmente, esta directiva se usa con relación a un punto de pedido que refleja la demanda anticipada durante el plazo del producto.  

### <a name="calculated-per-time-bucket"></a>Calculado por ciclo  
 Si el sistema de planificación detecta que se ha alcanzado o superado el punto de pedido en un ciclo determinado (ciclo de reaprovisionamiento), por encima del punto de pedido al inicio del periodo o en ese mismo punto, o por debajo al final del periodo o en ese mismo punto, sugerirá crear un nuevo pedido de aprovisionamiento con la cantidad de reaprovisionamiento especificada y anticipará su programación a partir de la primera fecha después de final del ciclo.  

 El concepto de punto de pedido por ciclos reduce el número de sugerencias de suministro. Esto refleja el proceso manual de recorrer con frecuencia el almacén para comprobar el contenido real de varias ubicaciones.  

### <a name="creates-only-necessary-supply"></a>Crea solo el aprovisionamiento necesario  
 Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el aprovisionamiento se ha pedido ya para ser recibido en el plazo de entrega del producto. Si un pedido de aprovisionamiento existente puede solucionar el problema llevando el inventario proyectado hasta el punto de pedido o por encima dentro del plazo de entrega, el sistema no sugerirá un nuevo pedido de aprovisionamiento.  

 Los pedidos de suministro que se crean específicamente para satisfacer un punto de pedido se excluyen del equilibrado de suministro normal y no cambiarán posteriormente. Por tanto, si un producto con punto de pedido debe retirarse (no reponerse), es recomendable revisar los pedidos de aprovisionamiento pendientes manualmente o cambiar la directiva de reaprovisionamiento a lote por lote, de modo que el sistema reduzca o cancele los aprovisionamientos superfluos.  

### <a name="combines-with-order-modifiers"></a>Combina con modificadores de pedido  
 Los modificadores de pedido, Cantidad mínima pedido, Cantidad máxima pedido y Múltiplos de pedido, no deben desempeñar un rol amplio cuando se usa la directiva cantidad de pedido fija. No obstante, el sistema de planificación aún tiene en cuenta estos modificadores y disminuye la cantidad a la cantidad de pedido máxima especificada (y crea dos o más aprovisionamientos para alcanzar la cantidad total de pedido), aumenta el pedido a la cantidad de pedido mínima especificada, o la redondea para que llegue al múltiplo del pedido especificado.  

### <a name="combines-with-calendars"></a>Combina con Calendarios  
 Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el pedido está programado para un día no laborable, según los calendarios definidos en el campo **Código calendario base** en las páginas **Información empresa** y **Ficha almacén**.  

 Si la fecha programada es un día no laborable, el sistema de planificación mueve el pedido al próximo día laborable. Esto puede dar lugar a un pedido que cumpla con el punto de pedido pero que no cumpla una demanda específica. Para este tipo de demandas sin saldar, el sistema de planificación crea un suministro extra.  

### <a name="should-not-be-used-with-forecast"></a>No debe usarse con la previsión  
 Dado que la demanda prevista aparece expresada ya en el nivel del punto de pedido, no es necesario incluir una previsión en la planificación de un producto mediante un punto de pedido. Si es necesario basar el plan en una previsión, utilice la directiva de lote por lote.  

### <a name="must-not-be-used-with-reservations"></a>No se debe usar con reservas  
 Si el usuario ha reservado una cantidad, por ejemplo una cantidad en inventario, en algunas demandas lejanas se perturbará la base de la planificación. Aunque el nivel de inventario estimado es aceptable en relación con el punto de nuevo pedido, las cantidades pueden no estar disponibles. El programa puede intentar compensarlo mediante la creación de pedidos de excepción; no obstante, se recomienda que el campo Reservar está configurado como Nunca en los productos que están planificados con un punto de pedido.

## <a name="maximum-qty"></a>Cdad. máxima
La directiva de cantidad máxima es una forma de mantener el inventario mediante un punto de pedido.  

También se aplica a esta directiva todo lo relacionado con la directiva de cantidad de reaprovisionamiento fija. La única diferencia es la cantidad del suministro sugerido. Al usar la directiva de cantidad máxima, la cantidad del nuevo pedido se definirá dinámicamente según el nivel de inventario proyectado y, por lo tanto, normalmente será distinta de un pedido a otro.  

### <a name="calculated-per-time-bucket"></a>Calculado por ciclo  
La cantidad a pedir se actualmente en el momento (el final de un ciclo) en el que el sistema de planificación detecta que se ha superado el punto de pedido. En este punto, el programa mide la diferencia entre el nivel de inventario proyectado actual y el inventario máximo especificado. Esto constituye la cantidad que se debe volver a pedir. A continuación, el sistema comprueba si el suministro ya se ha pedido en otra parte para recibirse en el plazo y, en caso afirmativo, reduce la cantidad del nuevo pedido de suministro en las cantidades ya pedidas.  

El programa garantizará que el inventario proyectado llegue como mínimo al nivel de punto de pedido como mínimo, en el caso de que el usuario haya olvidado especificar una cantidad de inventario máxima.  

### <a name="combines-with-order-modifiers"></a>Combina con modificadores de pedido  
Dependiendo de la configuración, puede ser mejor agrupar la directiva de cantidad máxima con modificadores de pedido para garantizar una cantidad de pedido mínima o redondearla a un número entero de unidades de medida de compra, o dividirla en más lotes según lo definido en la cantidad de pedido máxima.  

### <a name="combines-with-calendars"></a>Combina con Calendarios  
Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el pedido está programado para un día no laborable, según los calendarios definidos en el campo **Código calendario base** en las páginas **Información empresa** y **Ficha almacén**.  

Si la fecha programada es un día no laborable, el sistema de planificación mueve el pedido al próximo día laborable. Esto puede dar lugar a un pedido que cumpla con el punto de pedido pero que no cumpla una demanda específica. Para este tipo de demandas sin saldar, el sistema de planificación crea un suministro extra.

## <a name="order"></a>Sentido
En un entorno de fabricación contra pedido, el producto se compra o se produce para cubrir exclusivamente una demanda concreta. Normalmente, se relaciona con productos A y el motivo para elegir la política de reaprovisionamiento de pedido puede ser que la demanda se produce con poca frecuencia, el plazo es insignificante o varían los atributos requeridos.  

El programa crea un vínculo de pedido contra pedido, que actúa de conexión preliminar entre el suministro, un pedido de suministro o inventario, y la demanda que se va a cumplir.  

Aparte de utilizar la directiva de pedido, el vínculo de pedido a pedido se puede aplicar de las siguientes formas durante la planificación:  

* Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes necesarios en la misma orden de producción).  
* Al usar la característica de planificación de pedido de venta para crear una orden de producción a partir de un pedido de venta.  

Aunque una empresa de fabricación se considere a sí misma como entorno de fabricación contra pedido, puede ser preferible utilizar una directiva de lote por lote si los productos son puramente estándar sin variación en los atributos. Como resultado, el programa utilizará un inventario no planificado y solo acumulará los pedidos de venta con la misma fecha de envío o dentro de un ciclo definido.  

### <a name="order-to-order-links-and-past-due-dates"></a>Conexiones de pedido contra pedido y fechas vencidas  
A diferencia de la mayoría de conjuntos de suministro-demanda, el sistema ha planificado completamente los pedidos vinculados con fechas de vencimiento anteriores a la fecha inicial de planificación. El motivo empresarial de esta excepción es que los conjuntos de demanda-suministro específicos se deben sincronizar mediante la ejecución. Para obtener más información acerca de la zona congelada aplicable a la mayoría de los tipos de aprovisionamiento-demanda, consulte [Detalles de diseño: Gestión de pedidos antes de la fecha de inicio de planificación](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lote a lote
La directiva de lote por lote es la más flexible porque el sistema solo reacciones ante la demanda real, además de actuar ante la demanda anticipada de los pedidos de previsión y abiertos; a continuación, liquida la cantidad del pedido según la demanda. La directiva de lote por lote está dirigida a los productos A y B, donde el inventario se puede aceptar pero se debe evitar.  

De algún modo, la directiva del lote por lote se parece a la directiva de pedido, pero su acercamiento a los productos es genérico; puede aceptar cantidades en el inventario y une demandas con aprovisionamientos correspondientes en ciclos definidos por el usuario.  

El ciclo se define en el campo **Ciclo**. El programa trabaja con un ciclo mínimo de un día, ya que es la unidad de medida de tiempo menor en los eventos de demanda y de suministro del sistema (aunque, en la práctica, la unidad de medida de tiempo en las órdenes de producción y las necesidades de componentes puede ser segundos).  

El ciclo también establece límites con respecto a cuándo se debe reprogramar un pedido de suministro existente para cubrir una demanda determinada. Si el aprovisionamiento entra dentro del ciclo, se volverá a programar dentro o fuera para cubrir la demanda. De lo contrario, si es anterior, se producirá una acumulación innecesaria del inventario y se debe cancelar. Si es posterior, se creará un nuevo pedido de aprovisionamiento en su lugar.  

Con esta directiva, también se puede definir un stock de seguridad para compensar las fluctuaciones posibles en el suministro, o para satisfacer la demanda repentina.  

Dado que la cantidad del pedido de aprovisionamiento se basa en la demanda real, puede tener sentido usar los modificadores de pedido: redondear la cantidad del pedido para satisfacer un múltiplo de pedido especificado (o unidad de medida de compra), incrementar el pedido a una cantidad mínima especificada o disminuir la cantidad máxima especificada (y crear así dos aprovisionamientos o más para alcanzar la cantidad total necesaria).

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)

