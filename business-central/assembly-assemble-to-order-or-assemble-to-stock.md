---
title: Descripción de ensamblar para pedido y ensamblar para stock
description: Aprenda a ensamblar artículos para órdenes de venta o para mantenerlos en stock para futuras ventas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock" />Descripción de ensamblar para pedido y ensamblar para stock

[!INCLUDE [prod_short](includes/prod_short.md)] permite suministrar productos de ensamblaje de estas formas:

* Ensamblar para pedido  
* Ensamblar para stock  

## <a name="assemble-to-order" />Ensamblar para pedido

Use el proceso de ensamblado a pedido para los artículos que no desea almacenar. Por ejemplo, por las siguientes razones:

* Personalizará los artículos según los requisitos del cliente.
* Desea minimizar el costo del inventario disponible.

La siguiente lista describe algunos de los beneficios del proceso de ensamblaje bajo pedido:  

* Personalice los artículos de montaje al realizar un pedido de venta.  
* Resumen de la disponibilidad del artículo de montaje y sus componentes.  
* Reserve los componentes de ensamblado de inmediato para garantizar el cumplimiento de los pedidos.  
* Determine la rentabilidad del pedido personalizada redondeando el precio y el coste.  
* Se integra con el almacén para facilitar el ensamblado y el envío.  
* Ensamblar para pedido cuando crea una cotización de venta o una orden de venta abierta.  
* Combine cantidades del inventario con las de ensamblar para pedido.  

En el proceso de ensamblar para pedido, ensamble artículos para una orden de venta. Existe un vínculo uno a uno entre el pedido de ensamblado y el pedido de venta.  

Cuando especifique un producto de ensamblar para pedido en una línea de pedido de venta, automáticamente se crea un pedido de ensamblado. El pedido de ensamblado se basa en la línea de ventas y sus líneas se basan en la L. MAT. de ensamblado del artículo. La cantidad de componentes en la lista de materiales de ensamblaje se multiplica por la cantidad del pedido. La página **Líneas de ensamblaje para pedido** muestra detalles sobre las líneas de pedido de ensamblaje vinculadas. Los detalles pueden ayudarlo a personalizar el elemento de ensamblaje. El fecha de entrega se basa en la disponibilidad de los componentes. Para obtener más información sobre el ensamblaje de productos para pedidos de venta, vaya a [Vender artículos ensamblados por pedido](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Aunque no es parte del proceso predeterminado, puede vender las cantidades del inventario y las de ensamblar para pedido en el mismo pedido de venta. Para obtener más información sobre la combinación de artículos en stock y ensamblados a pedido, vaya a [Vender artículos de inventario en flujos de ensamblado a pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Para especificar que un artículo se ensambla a pedido, en el campo **Política de ensamblaje** en la página **Tarjeta de artículo** para el artículo, elija **Ensamblar para pedido**.  

## <a name="assemble-to-stock" />Ensamblar para stock

Use el proceso ensamblar para almacenar para artículos que ensamble y almacene para futuras ventas. Los artículos ensamblados para almacenar son artículos estándar, como kits empaquetados, que no se pueden personalizar. También puede consumir estos elementos como componentes de subensamblaje. Los productos se seleccionan y procesan como artículos únicos y se consideran productos terminados. Para obtener más información sobre productos de montaje, vaya a [Ensamblaje de productos](assembly-how-to-assemble-items.md).  

Cuando se especifica un artículo de ensamblar para stock en una línea de venta, el artículo se trata como cualquier otro artículo vendido del inventario. Por ejemplo, [!INCLUDE [prod_short](includes/prod_short.md)] comprueba la disponibilidad solo del artículo ensamblado y no de sus componentes.  

> [!NOTE]  
> Aunque no forma parte del proceso, se puede ensamblar un artículo para pedido aunque el artículo esté configurado para ensamblarse para stock. Obtenga más información en [Vender productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Para especificar que un artículo se ensambla para stock, en el campo **Política de ensamblaje** en la página **Tarjeta de artículo** para el artículo, elija **Ensamblar para stock**.  

## <a name="combination-scenarios" />Escenarios de combinación

Cuando se combinan las cantidades de inventario y ensamblar a pedido en una orden de venta, las cantidades de ensamblar a pedido deben enviarse primero.  

Si un pedido de ensamblado está vinculado a una línea del pedido de venta, el valor del campo **Cdad. en ensamblar para pedido** en la línea del pedido de venta se copia al campo **Cantidad a ensamblar** mediante el campo **Cantidad** del pedido de ensamblado. Obtenga más información en [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

El valor del campo **Cantidad a ensamblar** está relacionado con el campo **Cdad. a enviar** en la línea del pedido de venta. Esta relación administra cómo envía cantidades parciales y completas ensambladas bajo pedido:

* Cuando toda la cantidad de la línea del pedido de venta se ensambla para pedido
* En escenarios de combinación en donde parte de la cantidad de la línea de venta se ensambla para pedido y parte se envía del inventario.

El escenario combinado permite flexibilidad para envíos parciales. Puede usar el campo **Cantidad para ensamblar** para especificar la cantidad que se enviará parcialmente desde el inventario y ensamblando según pedido.  

Si toda la cantidad de la línea de venta se debe ensamblar para pedido y enviar, el valor en el campo **Cdad. a enviar** se copia al campo **Cantidad a ensamblar** en el pedido de ensamblado cuando cambie la cantidad para enviar. Esta actualización garantiza que la cantidad que se enviará sea suministrada totalmente por la cantidad ensamblar para pedido.  

Sin embargo, en los escenarios de combinación, el valor completo de **Cdad. a enviar** no se copia al campo **Cantidad a ensamblar** del pedido de ensamblado. En su lugar, se inserta un valor predeterminado en el campo **Cantidad para ensamblar** . El valor se calcula a partir de la **Cantidad. para enviar** para asegurarse de que las cantidades ensambladas a pedido se envíen primero.

Para desviarse del valor predeterminado, por ejemplo porque solo quiera ensamblar cantidades mayores o menores en el campo **Cdad. a enviar**, puede modificar el campo **Cantidad a ensamblar**, dentro de las reglas predefinidas, tal como se muestra abajo.  

Un ejemplo del motivo por el que modificaría la cantidad para ensamblar es que desee registrar parcialmente el envío de las cantidades del inventario antes de enviar la salida de ensamblado.  

En las siguiente tablas, se explican las reglas que definen los valores mínimo y máximo que se pueden introducir manualmente en el campo **Cantidad a ensamblar** para desviarse del valor predeterminado en un escenario de combinación. La tabla muestra un escenario de combinación cuyo campo **Cdad. a enviar** en la línea vinculada del pedido de venta se cambia del 7 al 4, y **Cdad. a ensamblar** se establece de forma predeterminada en 4.  

**Línea de pedido de venta**

|                | **Cantidad** | **Cdad. a enviar** | **Cdad. en ensamblar para pedido** | **Cantidad enviada** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valor inicial**| 10          | 7                | 7                             | 0                    |
|**Cambio**      |              | 4                |                               |                      |

**Cabecera de pedido de ensamblado**

|                | **Cantidad** | **Cdad. a enviar** | **Cdad. en ensamblar para pedido** | **Cantidad enviada** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Valor inicial**| 7           | 7                | 0                             | 7                    |
|**Cambio**      |              | 4 (insertado de forma predeterminada)|                         |                      |

En función de este ejemplo, puede modificar el campo **Cantidad a ensamblar** de la siguiente forma:  

* La cantidad mínima que puede introducir es 1. Debe ensamblar al menos una unidad para poder vender las cuatro unidades, si se asume que las tres restantes están disponibles en el inventario.  
* La cantidad máxima que puede introducir es 4. Este límite asegura que usted no ensamble más artículos de los que necesita para la venta.  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics--business-central" />Consultar la [formación de Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
