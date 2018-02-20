---
title: "Detalles de diseño: Carga de los perfiles de inventario | Documentos de Microsoft"
description: "Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d2a2ee196be4562f62604afd4faed608ff07411f
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-loading-the-inventory-profiles"></a>Detalles de diseño: Carga de los perfiles de inventario
Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario.  

 Los tipos normales de demanda y suministro con fechas de fecha de vencimiento en la fecha inicial de planificación se cargan en cada perfil de inventario. Cuando se cargan, los distintos tipos de demanda y de suministro se ordenan según las prioridades generales, como la fecha de vencimiento, los códigos de bajo nivel, la ubicación y la variante. Además, se aplican prioridades de pedido a los diversos tipos para garantizar que primero se satisfaga la demanda más importante. Para obtener más información, consulte [Detalles de diseño: Prioridad de pedidos](design-details-prioritizing-orders.md).  

 Como se indicaba anteriormente, la demanda también podría ser negativa. Esto significa que se debe tratar como suministro; no obstante, a diferencia de los tipos de suministro normales, la demanda negativa se considera suministro fijo. El sistema de planificación puede tenerla en cuenta, pero no sugerirá cambios.  

 En general, el sistema de planificación considera todos los pedidos de aprovisionamiento posteriores a la fecha de inicio de la planificación como sujetos a cambios para cubrir la demanda. No obstante, en cuanto una cantidad se registra a partir de un pedido de aprovisionamiento, ya no la puede modificar el sistema de planificación. Por consiguiente, los diferentes pedidos siguientes no se pueden replanificar:  

-   Órdenes de producción lanzadas donde se ha registrado la salida o el consumo.  

-   Pedidos de ensamblado donde se ha registrado la salida o el consumo.  

-   Pedidos de transferencia donde se ha registrado el envío.  

-   Pedidos de compra en los que se ha registrado la recepción.  

 Aparte de cargar los tipos de demanda y aprovisionamiento, se cargan determinados tipos respetando reglas especiales y dependencias, las cuales que se describen a continuación.  

## <a name="item-dimensions-are-separated"></a>Las dimensiones de producto están separadas  
 El plan de suministro se debe calcular mediante la combinación de dimensiones de producto, como variante y ubicación. No obstante, no hay razón para calcular ninguna combinación teórica. Solo es necesario calcular las combinaciones con una necesidad de demanda o de suministro.  

 El sistema de planificación lo controla mediante la ejecución a través del perfil de inventario. Cuando se encuentra una nueva combinación, el programa crea un registro de control interno que contiene la información de combinación real. El programa inserta la UA como el registro de control, o bucle externo. Como resultado, se establecerán los parámetros de planificación adecuados según una combinación de variante y almacén, y el programa podrá proceder al bucle interno.  

> [!NOTE]  
>  El programa no requiere que el usuario introduzca un registro de UA al introducir la demanda o el suministro de una determinada combinación de variante y ubicación. Por lo tanto, si no exista una UA para una combinación determinada, el programa crea su propio registro de UA temporal según los datos de la ficha de producto. Si Almacén obligatorio se establece en Sí en la ventana de configuración del inventario, se debe crear una UA o bien los componentes en el almacén deben definirse en Sí. Para obtener más información, consulte [Detalles de diseño: Demanda en almacén vacío](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Los números de serie y de lote se cargan por nivel de especificación  
 Los atributos en forma de números de serie o lote se cargan en los perfiles de inventario, junto con la demanda y el aprovisionamiento a los que están asignados.  

 Los atributos de demanda y aprovisionamiento se organizan por prioridad de pedido, así como por el nivel de especificación. Dado que las coincidencias de número de serie o de lote reflejan el nivel de especificación, la demanda más específica, como un número de lote seleccionado específicamente para una línea de venta, buscará una coincidencia antes que una demanda menos específica, por ejemplo una venta de cualquier número de lote seleccionado.  

> [!NOTE]  
>  No existen reglas de prioridades exclusivas para demanda y suministro con números de serie y de lote, aparte del nivel de especificación definido por sus combinaciones de números de serie y de lote, y la configuración de seguimiento de producto de los productos que intervienen.  

 Durante el proceso de equilibrado, el sistema de planificación toma los números de serie y de lote inflexibles y no intenta ni aumentar ni reprogramar estos pedidos de aprovisionamiento (a menos que se utilicen en una relación de pedido a pedido). Vea Las conexiones de pedido contra pedido nunca se rompen). De este modo se protege el suministro frente a la recepción varios mensajes de acción, posiblemente en conflicto, cuando un suministro tiene atributos variables, como, por ejemplo, una colección de números de serie distintos.  

 Otra razón por la que el aprovisionamiento de números de serie y de lote no es flexible es que los números de serie y de lote generalmente se asignan tan tarde en el proceso que resultaría confuso si se sugirieran cambios.  

 La contrapartida de números de serie o de lote no respeta [Zona congelada](design-details-dealing-with-orders-before-the-planning-starting-date.md). Si la demanda y el aprovisionamiento no se sincroniza, el sistema de planificación sugerirá cambios o sugerirá nuevos pedidos, independientemente de la fecha de inicio de la planificación.  

## <a name="order-to-order-links-are-never-broken"></a>Las conexiones de pedido contra pedido nunca se rompen  
 Al planificar un producto de pedido contra pedido, el suministro vinculado no se debe usar para ninguna otra demanda que para la que se ha pensado originalmente. La demanda vinculada no se debe cubrir con otro suministro aleatorio, incluso si, en la situación actual, está disponible en cuanto a tiempo y a cantidad. Por ejemplo, no se podrá utilizar para cubrir otra demanda un pedido de ensamblado vinculado a un pedido de venta en un caso de ensamblado para pedido.  

 La demanda y el suministro de pedido contra pedido se deben equilibrar de forma precisa. El sistema de planificación garantizará el suministro en todas las situaciones sin tener en cuenta los parámetros de tamaño de pedido, los modificadores y las cantidades en el inventario (aparte de las cantidades relacionadas con los pedidos vinculados). Por el mismo motivo, el sistema sugiere disminuir aprovisionamientos en exceso si se disminuye la demanda vinculada.  

 Esta contrapartida también afecta a la temporización. No se considera el horizonte limitado que ofrece el ciclo; el suministro se reprogramará si ha cambiado el plazo de la demanda. No obstante, el tiempo de amortiguación se respetará e impedirá que los aprovisionamientos de pedido a pedido no entren en el programa, excepto en el caso de aprovisionamientos internos de una orden de producción de varios niveles (orden de proyecto).  

> [!NOTE]  
>  Los números de serie y de lote también se pueden especificar en la demanda de pedido contra pedido. En ese caso, el aprovisionamiento no es inflexible de forma predeterminada, como generalmente sucede con números de serie y de lote. En este caso, el programa aumentará o disminuirá según los cambios en la demanda. Además, si una demanda lleva distintos números de serie o de lote, por ejemplo más de un número de lote, se sugerirá un pedido de aprovisionamiento por lote.  

> [!NOTE]  
>  Las previsiones no deben llevar a crear pedidos de aprovisionamiento limitados por un vínculo de pedido a pedido. Si se usa la previsión, solo debe hacerse como generador de una demanda dependiente en un entorno de fabricación.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>La necesidad de componente se carga según los cambios de la orden de producción  
 Al manipular las órdenes de producción, el sistema de planificación debe supervisar los componentes necesarios antes de cargarlos en el perfil de demanda. Las líneas de componente resultantes de una orden de producción modificada reemplazarán las del pedido original. De este modo se garantiza que el sistema de planificación establece que nunca se dupliquen las líneas de planificación de la necesidad de componentes.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> El stock de seguridad se puede consumir  
 El stock de seguridad es, principalmente, un tipo de demanda y, por lo tanto, se carga en el perfil de inventario en la fecha inicial de la planificación.  

 El stock de seguridad es una cantidad que se aparta para compensar las incertidumbres en la demanda durante el plazo de reposición. No obstante, se pueden consumir si es necesario para cubrir una demanda. En dicho caso, el programa de planificación garantizaría que el stock de seguridad se sustituye rápidamente sugiriendo un pedido de aprovisionamiento para abastecer la cantidad de stock de seguridad en la fecha en la que se consume. Esta línea de planificación mostrará un icono de advertencia de excepción explicando al planificador que el stock de seguridad se ha consumido parcialmente o en su totalidad a través de un pedido de excepción para la cantidad que falta.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Los pedidos de ventas reducen la demanda de previsión  
 La previsión de producción expresa la demanda futura prevista. Mientras se introduce la demanda real, normalmente como pedidos de venta para productos fabricados, se consume la previsión.  

 La previsión no se reduce realmente por los pedidos de venta; permanece igual. No obstante, las cantidades de previsión utilizadas en el cálculo de la planificación se reducen (por las cantidades del pedido de venta) antes de que la cantidad pendiente, si la hubiera, entre en el perfil del inventario de demanda. Cuando el sistema de planificación examina las ventas reales durante un periodo, se incluyen los pedidos de venta abiertos y los movimientos de producto de las ventas enviadas, a menos que se deriven de un pedido abierto.  

 Un usuario debe definir un periodo válido de previsión. La fecha de la cantidad prevista define el comienzo del periodo y la fecha de la previsión siguiente define el final del periodo.  

 No se usa la previsión para periodos anteriores al periodo de planificación, independientemente de si se ha consumido o no. La primera cifra de previsión que interesa es la fecha de inicio de la planificación o la fecha anterior más próxima.  

 La previsión puede ser de demanda independiente, como pedidos de venta, o de demanda dependiente, como los componentes de orden de producción (módulo - previsión). Un producto puede tener los dos tipos de previsión. Durante la planificación, el consumo se realiza por separado, primero para la demanda independiente y después para la demanda dependiente.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Los pedidos de venta reducen la demanda del pedido abierto  
 La previsión se complementa con el pedido de venta abierto para especificar la demanda futura de un cliente específico. Como con la previsión (sin especificar), las ventas reales deberán consumir la demanda prevista, y la cantidad pendiente deberá corresponder al perfil de inventario de demanda. Una vez, más el consumo no reduce realmente el pedido abierto.  

 El cálculo de planificación tiene en cuenta los pedidos de venta abiertos vinculados a la línea de pedido abierto específica, pero no tiene en cuenta ningún periodo de tiempo válido. Ni tiene en cuenta los pedidos registrados, debido a que el procedimiento de registro ya ha reducido la cantidad pendiente del pedido abierto.  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
 [Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
 [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)   
 [Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)

