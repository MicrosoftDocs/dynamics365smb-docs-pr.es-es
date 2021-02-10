---
title: Venta de productos de inventario en los flujos de ensamblar para pedido | Documentos de Microsoft
description: Si un elemento está configurado para la ficha de Ensamblar para pedido, el proceso de pedido de venta predeterminado supone que el producto no está en el inventario y se debe ensamblar para ese pedido de venta concreto. Por tanto, se crea automáticamente un pedido de ensamblado al agregar el elemento a una línea de pedido de venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fb2487f2c8300fa73c2251b978e8deebc50ed404
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747346"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Vender productos de inventario en los flujos de ensamblar para pedido
Si el campo **Directiva de ensamblado** de la ficha de producto de un elemento del ensamblado contiene **Ensamblar para pedido**, el proceso de pedido de venta predeterminado supone que el producto no está en el inventario y se debe ensamblar para ese pedido de venta concreto. Por tanto, se crea automáticamente un pedido de ensamblado al agregar el elemento a una línea de pedido de venta. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md). Sin embargo, si parte de la cantidad del pedido de venta ya está disponible en el inventario, puede reducir la cantidad del pedido de ensamblado cambiando el campo **Cdad. al ensamblar para pedido** de la línea de pedido de venta.  

Este ejemplo es raro ya que se espera que los productos de ensamblar para pedido estén siempre personalizados y la posibilidad de que estén en el inventario con la configuración solicitada por otro cliente es baja. Sin embargo, si una empresa tiene cantidades de ensamblar para pedido en el inventario debido a devoluciones o cancelaciones de pedidos, se debe realizar el picking de estas cantidades y venderlas antes de que se ensamblen nuevas.  

> [!NOTE]  
>  Ninguna funcionalidad existe en los pedidos de venta que automáticamente alerte o ayude a deducir cantidades de pedido de ensamblado que ya estén disponibles. En su lugar, debe supervisar la información de la disponibilidad, como en el cuadro informativo **Detalles líneas venta**.  

Hay una funcionalidad similar disponible al vender productos de ensamblado del inventario y una parte o toda la cantidad no está disponible y se puede suministrar mediante un pedido de ensamblado. Para obtener más información, consulte [Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Ciertas reglas se aplican al campo **Cdad. a enviar** de las líneas de pedido de venta que contienen una combinación de cantidades de ensamblar para pedido y de cantidades de inventario. Para obtener más información, consulte la sección Escenarios de combinación en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

En este procedimiento, se reemplazan las cantidades de ensamblar para pedido con cantidades de inventario en una línea de pedido de venta. Los pasos incluyen la detección de que existe la disponibilidad, la deducción de dicha cantidad del pedido de ensamblado vinculado y, a continuación, la reserva de la cantidad de inventario para asegurarse de que se ha realizado el picking de la misma y se ha enviado para el pedido.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Para vender productos de inventario en los flujos de ensamblar para pedido  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  Cree un pedido de ventas. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  
3.  En una línea de pedido de venta para un artículo de ensamblar para pedido, en el campo **Cantidad**, introduzca la cantidad solicitada.  
4.  En el cuadro informativo **Detalles líneas venta**, determine si toda la cantidad solicitada o parte de ella está disponible.  
5.  En el campo **Cdad. al ensamblar para pedido**, deduzca la cantidad disponible de forma que solo la cantidad no disponible se ensamble para pedido. El campo **Cantidad reservada** se reduce en consecuencia para reflejar que el vínculo de pedido-a-pedido o la reserva solo se aplican a la cantidad que se va a ensamblar.  
6.  En la ficha desplegable **Líneas**, elija **Funciones** y, a continuación, la acción **Reservar**.  
7.  En la página **Reservas**, seleccione la línea o las líneas del movimiento de producto que contienen las cantidades disponibles, elija la acción **Reservar desde la línea actual** y, a continuación, elija el botón **Aceptar**.  

    En la página **Pedido venta**, el campo **Cantidad reservada** muestra ahora que la cantidad completa de la línea de pedido está reservada. El campo **Cdad. al ensamblar para pedido** aún refleja la cantidad secundaria que debe ensamblarse.  

8.  Lance el pedido de venta para el picking de los productos de inventario y para el ensamblado de los productos no disponibles. Para obtener más información, consulte [Ensamblar productos](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  El campo **Cód. ubicación** en el pedido de venta se puede llenar por anticipado de acuerdo con el campo **Cód. ubic. ensamblar para pedido** o **Cód. ubic. desde ensamblado** en la ficha de almacén. En ese caso, el campo **Cód. ubicación** de la línea de pedido de venta puede ser incorrecto en esta combinación de cantidades de ensamblar para pedido y ensamblar para stock. Es una buena idea observar el campo **Cód. ubicación** y garantizar que la ubicación es válida para todas las cantidades. También puede introducir las dos cantidades en líneas de pedido de venta distintas.  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
