---
title: Vender productos de ensamblado para pedido y productos de inventario juntos
description: 'Si no está disponible parte de la configuración de un elemento del ensamblado para ensamblar para stock, puede crear un pedido de ensamblado para la cantidad restante.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Vender productos de ensamblado para pedido y productos de inventario juntos

Si el campo **Directiva de ensamblado** de la ficha de producto de un elemento del ensamblado contiene **Ensamblar para stock**, el proceso de pedido de venta supone que el producto está ensamblado y se puede ya seleccionar del inventario, si está disponible. Por tanto, no se crea ni vincula ningún pedido de ensamblado automáticamente a la línea de pedido de venta. Sin embargo, si no está disponible parte o la totalidad de la configuración de un elemento del ensamblado para ensamblar para stock, puede crear un pedido de ensamblado para la cantidad restante. Para ello, rellene el campo **Cantidad a ensamblar para pedido** en la línea del pedido de ensamblado. Esta configuración le permite ensamblar el producto para pedido aunque esté configurado para ensamblarse para stock.  

Tiene una flexibilidad similar cuando vende artículos ensamblados a pedido y parte de la cantidad ya está en el inventario. Querrá deducir esa cantidad de la orden de montaje. Para obtener más información sobre la venta de productos de inventario, vaya a [Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Hay reglas que se aplican al campo **Cdad. a enviar** de las líneas de pedido de venta que contienen una combinación de cantidades de ensamblar para pedido y de cantidades de inventario. Para obtener más información sobre las reglas, vaya a [Escenarios combinados](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> El procedimiento siguiente no incluye los pasos de pedido de venta que necesita seguir antes de crear un pedido de ensamblado para las cantidades no disponibles.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Para vender productos de ensamblado para pedido y productos de inventario juntos

1. En una línea de pedido de venta de un producto para ensamblarse para stock, escriba una cantidad en el campo **Cantidad** que sea mayor que el inventario. La página **Comprobación disponibilidad** aparecerá. Para obtener más información sobre la disponibilidad de artículos, vaya a [Ver la disponibilidad de artículos](inventory-how-availability-overview.md).
2. En el campo **Cdad. al ensamblar para pedido**, introduzca el valor del campo **Cantidad total**.  
3. Realice los cambios necesarios en los componentes de ensamblado. Obtenga más información en [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  
4. Lance el pedido de venta para hacer que los artículos estén disponibles para el picking y para el ensamblado de los productos no disponibles. Para obtener más información acerca de los pasos estándar del ensamblado, vaya a [Ensamblar productos](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> El campo **Cód. ubicación** en el pedido de venta podría contener el valor de lo scampos **Cód. ubic. ensamblar para pedido** o **Cód. ubic. desde ensamblado** en la ficha de almacén. Si es así, el campo **Cód. ubicación** de la línea de pedido de venta podría ser incorrecto para esta combinación de cantidades de ensamblar para pedido y ensamblar para stock. Es una buena idea hacer una doble comprobación de que la ubicación en el campo **Cód. ubicación** es válida para todas las cantidades. También puede introducir las dos cantidades en líneas de pedido de venta distintas.  

## <a name="see-also"></a>Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
