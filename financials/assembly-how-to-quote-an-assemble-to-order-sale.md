---
title: Oferta de una venta de ensamblar para pedido | Documentos de Microsoft
description: "Puede utilizar la administración de ensamblados para personalizar un artículo del ensamblado a la solicitud de un cliente durante el proceso de venta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4b91b8a0ee359c1dc8dc4507cade6b635dace644
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Oferta de una venta de ensamblar para pedido
Puede utilizar la administración de ensamblados para personalizar un artículo del ensamblado a la solicitud de un cliente durante el proceso de venta. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

Como cuando se vende cualquier otro tipo de producto, también puede crear una oferta de venta para un elemento del ensamblado personalizado antes de convertirlo en un pedido de venta. Este proceso implica varios pasos adicionales cuando se compara con crear una oferta de venta regular y usa una variación de un pedido de ensamblado vinculado, que es una oferta de ensamblado.

> [!NOTE]  
>  Como todos los tipos de oferta, las cantidades en ofertas de ensamblado no se utilizan en la disponibilidad, la planificación o las reservas.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Para crear una oferta de venta de productos ensamblar para pedido  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Oferta de venta** y, a continuación, seleccione el vínculo relacionado.  
2.  Cree una línea de oferta de venta con una línea para un elemento del ensamblado. Para obtener más información, consulte [Realización de ofertas](sales-how-make-offers.md).  
3.  En el campo **Cdad. al ensamblar para pedido**, introduzca la cantidad total.

    > [!NOTE]  
    >  No debe crear una oferta para una cantidad parcial. Por tanto, deberá introducir la misma cantidad que ha introducido en el campo **Cantidad** de la línea de oferta de venta.  

4.  En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Ensamblar para líneas de pedido**. También puede elegir el campo **Cdad. al ensamblar para pedido** en la línea.  
5.  En la ventana **Ensamblar para líneas de pedido**, revise o modifique las líneas de pedido de ensamblado de acuerdo con la oferta que el cliente solicita. Si desea ver más información, seleccione la acción **Mostrar documento** para abrir el pedido de oferta abierto completo. No puede modificar el contenido de la mayoría de los campos, y no puede realizar ningún registro.  
6.  Cuando se hayan ajustado las líneas del pedido de ensamblado a la oferta, cierre la ventana **Ensamblar para líneas de pedido** para volver a la ventana **Oferta venta**.  
7.  Si el cliente acepta la oferta, cree un pedido de venta para el elemento del ensamblado ofertado. Para obtener más información, consulte [Realización de ofertas](sales-how-make-offers.md). La oferta de ensamblado vinculada y cualquier personalización se asocian a ese nuevo pedido de venta para preparar el ensamblado del producto o los productos que se van a vender.  

## <a name="see-also"></a>Consulte también  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

