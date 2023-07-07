---
title: Vender productos de inventario en los flujos de ensamblar para pedido
description: Los artículos ensamblados a pedido se ensamblan para órdenes de venta a través de una orden de ensamblado.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a>Vender productos de inventario en flujos de ensamblar para pedido

Si el campo **Directiva de ensamblado** de la ficha de producto de un elemento del ensamblado contiene **Ensamblar para pedido**, el proceso de pedido de venta supone que el producto no está en el inventario y se debe ensamblar para los pedidos de venta. Cuando agrega el producto a una línea de un pedido de venta, [!INCLUDE [prod_short](includes/prod_short.md)] creará un pedido de ensamblado vinculado al pedido de venta. Para obtener más información sobre cómo vender productos ensamblados para pedido, vaya a [Vender artículos ensamblados por pedido](assembly-how-to-sell-items-assembled-to-order.md). Sin embargo, si parte de la cantidad del pedido de venta ya está disponible en el inventario, puede reducir la cantidad del pedido de ensamblado cambiando el campo **Cdad. al ensamblar para pedido** de la línea de pedido de venta.  

Es relativamente raro que las empresas vendan artículos de inventario como artículos ensamblados a pedido. Los artículos ensamblados a pedido generalmente no son estándar. Están personalizados para cumplir con los requisitos específicos del cliente. Sin embargo, es posible que tenga cantidades de artículos ensamblados sobre pedido en el inventario debido a devoluciones o cancelaciones de pedidos. Esas cantidades deben seleccionarse y venderse antes de ensamblar las nuevas.  

> [!NOTE]  
> Para comprobar si los artículos ensamblados sobre pedido ya están disponibles para pedidos de ensamblado, use el cuadro informativo **Detalles de línea de ventas** en el pedido de ventas.  

Puede hacer cosas similares cuando vende artículos de ensamblaje del inventario y parte o la totalidad de la cantidad no está disponible. Puede suministrar la cantidad que falta a través de una orden de ensamblado. Para obtener más información sobre la venta de inventario y productos de ensamblado, vaya a [Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Hay reglas que se aplican al campo **Cdad. a enviar** de las líneas de pedido de venta que contienen una combinación de cantidades de ensamblar para pedido y de cantidades de inventario. Para obtener más información sobre las reglas, vaya a [Escenarios combinados](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

En este procedimiento, se reemplazan las cantidades de ensamblar para pedido con cantidades de inventario en una línea de pedido de venta. Los siguientes pasos proporcionan una descripción general:

1. Determinar la disponibilidad.
2. Reducir esa cantidad del pedido de ensamblado vinculado.
3. Reservar la cantidad de inventario para asegurarse de que se seleccione y envíe para el pedido.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Para vender productos de inventario en los flujos de ensamblar para pedido

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Cree un pedido de ventas. Para obtener más información sobre cómo crear pedidos de ventas, vaya a [Vender productos](sales-how-sell-products.md).  
3. En una línea de pedido de venta que contiene un artículo de ensamblar para pedido, en el campo **Cantidad**, introduzca la cantidad.  
4. En el cuadro informativo **Detalles líneas venta**, determine si una parte o la totalidad de la cantidad está disponible.  
5. En el campo **Cdad. al ensamblar para pedido**, deduzca la cantidad disponible de forma que solo la cantidad no disponible se ensamble para pedido. El campo **Cantidad reservada** se reduce en consecuencia para reflejar que el vínculo de pedido-a-pedido o la reserva solo se aplican a la cantidad que se va a ensamblar.  
6. En la ficha desplegable **Líneas**, elija **Funciones** y, a continuación, la acción **Reservar**.  
7. En la página **Reservas**, seleccione la línea o las líneas del movimiento de producto que contienen las cantidades disponibles, elija la acción **Reservar desde la línea actual** y, a continuación, elija el botón **Aceptar**.  

    En la página **Pedido venta**, el campo **Cantidad reservada** muestra ahora que la cantidad completa de la línea de pedido está reservada. El campo **Cdad. al ensamblar para pedido** aún refleja la cantidad para ensamblar.  

8. Lance el pedido de venta para hacer que los artículos estén disponibles para el picking y para el ensamblado de los productos no disponibles. Para obtener más información sobre productos de ensamblaje, vaya a [Ensamblaje de productos](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> El campo **Cód. ubicación** en el pedido de venta podría contener el valor de lo scampos **Cód. ubic. ensamblar para pedido** o **Cód. ubic. desde ensamblado** en la ficha de almacén. Si es así, el campo **Cód. ubicación** de la línea de pedido de venta podría ser incorrecto para esta combinación de cantidades de ensamblar para pedido y ensamblar para stock. Es una buena idea hacer una doble comprobación de que la ubicación en el campo **Cód. ubicación** es válida para todas las cantidades. También puede introducir las dos cantidades en líneas de pedido de venta distintas.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/assemble-to-order-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
