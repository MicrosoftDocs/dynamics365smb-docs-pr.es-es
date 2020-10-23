---
title: Descripción de ensamblar para pedido y ensamblar para stock | Documentos de Microsoft
description: Los elementos de ensamblado se pueden suministrar ensamblándolos cuando se ordenan o ensamblándolos para que se mantengan en el inventario hasta que sean necesarios en una orden de venta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 746aa6c0146205cbc3f3ed1796b084825bbfdbdf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915715"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Descripción de ensamblar para pedido y ensamblar para stock
Los artículos de montaje se pueden suministrar en los dos procesos siguientes:  

-   Ensamblar para pedido  
-   Ensamblar para stock.  

## <a name="assemble-to-order"></a>Ensamblar para pedido  
Utilice normalmente *ensamblar para pedido* para los artículos que no desea llevar porque espera personalizarlos según lo solicitado por el cliente o porque desee minimizar el coste que incluye del inventario. La funcionalidad incluye:  

-   Capacidad de personalizar los artículos de montaje al realizar un pedido de venta.  
-   Resumen de la disponibilidad del artículo de montaje y sus componentes.  
-   Capacidad de reservar inmediatamente los componentes de ensamblado para garantizar el cumplimiento de los pedidos.  
-   Función para determinar la rentabilidad del pedido personalizada redondeando el precio y el coste.  
-   Integración con almacén para facilitar el ensamblado y el envío.  
-   Capacidad de ensamblar para pedido en el momento de realizar una oferta de venta o de un pedido abierto de venta.  
-   Capacidad de agrupar las cantidades del inventario con las de ensamblar para pedido.  

En el proceso del ensamblar para pedido, el artículo se ensambla en respuesta a un pedido de venta y con un vínculo uno a uno entre el pedido de ensamblado y el pedido de venta.  

Cuando se introduce un artículo de ensamblar para pedido en una línea de venta, se crea automáticamente un pedido de ensamblado con una cabecera que se basa en la línea de venta y con las líneas que se basan en el L.M. de ensamblado del artículo multiplicado por la cantidad del pedido. Puede usar la página **Líneas ensamblar para pedido** para ver las líneas del pedido de ensamblado con el fin de ayudarle a personalizar el elemento del ensamblado y para comprometerse con una fecha de entrega basada en la información de disponibilidad del componente. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Aunque no es parte del proceso predeterminado, puede vender las cantidades del inventario con las de ensamblar para pedido. Para obtener más información, consulte [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Para activar este proceso, el campo de **Directiva de ensamblado** en la ficha del artículo debe ser **Ensamblar para pedido**.  

## <a name="assemble-to-stock"></a>Ensamblar para stock.  
 Se utiliza normalmente *Ensamblar para stock* para los artículos que se desea ensamblar antes de la venta, como para prepararse para una campaña de equipo, y mantenerlo en stock hasta que se soliciten. Estos artículos suelen ser estándar, como equipos embalados que no ofrecen personalización según las solicitudes de cliente.  

 En el proceso del ensamblar para stock, el artículo se ensamble sin demanda de venta inmediata y se mantiene en existencias en el almacén como producto de inventario para la venta o el consumo posterior como subelemento. Para obtener más información, consulte [Ensamblar productos](assembly-how-to-assemble-items.md). De ese momento, el artículo se prepara y se procesa como único artículo y se considera un producto terminado.  

 Cuando se introduce un artículo de ensamblar para stock en una línea de venta, la línea es como cualquier otro artículo vendido del inventario. Por ejemplo, se comprueba la disponibilidad sólo para el artículo de ensamblado.  

> [!NOTE]  
>  Aunque no forma parte del proceso, se puede ensamblar un artículo para pedido aunque esté configurado para ensamblarse para stock. Para obtener más información, consulte [Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Para activar este proceso, el campo **Directiva de ensamblado** en la ficha del artículo debe ser **Ensamblar para stock**.  

## <a name="combination-scenarios"></a>Escenarios de combinación  
 Un principio general de la administración de ensamblados es que cuando están agrupadas en una línea del pedido de venta, las cantidades de ensamblar para pedido se deben enviar antes de las del inventario.  

 Si un pedido de ensamblado está vinculado a una línea del pedido de venta, el valor del campo **Cdad. en ensamblar para pedido** en la línea del pedido de venta se copia al campo **Cantidad a ensamblar** mediante el campo **Cantidad** de la cabecera del pedido de ensamblado. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

 Además, el valor del campo **Cantidad a ensamblar** está relacionado con el campo **Cdad. a enviar** en la línea del pedido de venta, y esta relación se encarga del envío de las cantidades de ensamblar para pedido, parcial y completamente. Esto es válido tanto cuando se ensamble la cantidad completa de la línea de venta para el pedido y en los escenarios de combinación donde una parte de la cantidad de la línea de venta se ensambla para el pedido y otra parte se envía desde el inventario. Sin embargo, en el escenario de combinación, tendrá una flexibilidad adicional al enviar parcialmente en el sentido que podrá modificar el campo **Cantidad a ensamblar**, dentro de las reglas predefinidas, para especificar cuántas unidades deben enviarse parcialmente del inventario y cuántas parcialmente mediante ensamblado para pedido.  

 Si toda la cantidad de la línea de venta se debe ensamblar para pedido y enviar, el valor en el campo **Cdad. a enviar** se copia al campo **Cantidad a ensamblar** en el pedido de ensamblado cuando cambie la cantidad para enviar. Esto garantiza que la cantidad que se enviará sea suministrada totalmente por la cantidad ensamblar para pedido.  

 Sin embargo, en los escenarios de combinación, el valor completo de **Cdad. a enviar** no se copia al campo **Cantidad a ensamblar** de la cabecera del pedido de ensamblado. Un su lugar, este valor predeterminado se inserta en el campo **Cantidad a ensamblar** calculado a partir de **Cdad. a enviar** según una regla predefinida que garantiza antes el envío de las cantidades ensamblar para pedido.  

 Si desea desviarse de este valor predeterminado, por ejemplo porque solo quiera ensamblar cantidades mayores o menores en el campo **Cdad. a enviar**, puede modificar el campo **Cantidad a ensamblar**, pero sólo dentro de las reglas predefinidas, tal como se muestra abajo.  

 Un ejemplo del motivo por el que querría modificar la cantidad para ensamblar es que desee registrar parcialmente el envío de las cantidades del inventario antes de que la salida de ensamblado se pueda enviar.  

 En la siguiente tabla, se explican las reglas que definen los valores mínimo y máximo que se pueden introducir manualmente en el campo **Cantidad a ensamblar** para desviarse del valor predeterminado en un escenario de combinación. La tabla muestra un escenario de combinación cuyo campo **Cdad. a enviar** en la línea vinculada del pedido de venta se cambia del 7 al 4, y **Cdad. a ensamblar** se establece de forma predeterminada en 4.  

|-|Línea de pedido de venta|Cabecera de pedido de ensamblado|  
|-|----------------------|---------------------------|  
||**Cantidad**|**Cdad. a enviar**|**Cdad. en ensamblar para pedido**|**Cantidad enviada**|**Cantidad**|**Cantidad a ensamblar**|**Cantidad ensamblada**|**Cantidad pendiente**|  
|Inicial|10|7|7|0|7|7|0|7|  
|Cambiar||4||||4 (insertado de forma predeterminada)|||  

 En función de la situación anterior, sólo se puede modificar el campo **Cantidad a ensamblar** de la siguiente forma:  

-   La cantidad mínima que puede introducir es 1. Esto se debe a que debe ensamblar al menos una unidad para poder vender las cuatro unidades, si se asume que las tres restantes están disponibles en el inventario.  
-   La cantidad máxima que puede introducir es 4. Así se garantiza que no ensamble más de este artículo de ensamblar para pedido de lo que se necesita en la venta.  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
