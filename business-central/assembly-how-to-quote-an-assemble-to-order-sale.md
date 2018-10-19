---
title: Oferta de una venta de ensamblar para pedido | Documentos de Microsoft
description: "Puede utilizar la administración de ensamblados para personalizar un artículo del ensamblado a la solicitud de un cliente durante el proceso de venta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: be0a80ea66dea634a37cb187408c7142d70af011
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="d8199-103">Oferta de una venta de ensamblar para pedido</span><span class="sxs-lookup"><span data-stu-id="d8199-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="d8199-104">Puede utilizar la administración de ensamblados para personalizar un artículo del ensamblado a la solicitud de un cliente durante el proceso de venta.</span><span class="sxs-lookup"><span data-stu-id="d8199-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="d8199-105">Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="d8199-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="d8199-106">Como cuando se vende cualquier otro tipo de producto, también puede crear una oferta de venta para un elemento del ensamblado personalizado antes de convertirlo en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d8199-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="d8199-107">Este proceso implica varios pasos adicionales cuando se compara con crear una oferta de venta regular y usa una variación de un pedido de ensamblado vinculado, que es una oferta de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="d8199-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="d8199-108">Como todos los tipos de oferta, las cantidades en ofertas de ensamblado no se utilizan en la disponibilidad, la planificación o las reservas.</span><span class="sxs-lookup"><span data-stu-id="d8199-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="d8199-109">Para crear una oferta de venta de productos ensamblar para pedido</span><span class="sxs-lookup"><span data-stu-id="d8199-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="d8199-110">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Oferta de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d8199-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d8199-111">Cree una línea de oferta de venta con una línea para un elemento del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="d8199-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="d8199-112">Para obtener más información, consulte [Crear ofertas de ventas](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="d8199-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="d8199-113">En el campo **Cdad. al ensamblar para pedido**, introduzca la cantidad total.</span><span class="sxs-lookup"><span data-stu-id="d8199-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="d8199-114">No debe crear una oferta para una cantidad parcial.</span><span class="sxs-lookup"><span data-stu-id="d8199-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="d8199-115">Por tanto, deberá introducir la misma cantidad que ha introducido en el campo **Cantidad** de la línea de oferta de venta.</span><span class="sxs-lookup"><span data-stu-id="d8199-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="d8199-116">En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Ensamblar para líneas de pedido**.</span><span class="sxs-lookup"><span data-stu-id="d8199-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="d8199-117">También puede elegir el campo **Cdad. al ensamblar para pedido** en la línea.</span><span class="sxs-lookup"><span data-stu-id="d8199-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="d8199-118">En la ventana **Ensamblar para líneas de pedido**, revise o modifique las líneas de pedido de ensamblado de acuerdo con la oferta que el cliente solicita.</span><span class="sxs-lookup"><span data-stu-id="d8199-118">In the **Assemble-to-Order Lines** window, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="d8199-119">Si desea ver más información, seleccione la acción **Mostrar documento** para abrir el pedido de oferta abierto completo.</span><span class="sxs-lookup"><span data-stu-id="d8199-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="d8199-120">No puede modificar el contenido de la mayoría de los campos, y no puede realizar ningún registro.</span><span class="sxs-lookup"><span data-stu-id="d8199-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="d8199-121">Cuando se hayan ajustado las líneas del pedido de ensamblado a la oferta, cierre la ventana **Ensamblar para líneas de pedido** para volver a la ventana **Oferta venta**.</span><span class="sxs-lookup"><span data-stu-id="d8199-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** window to return to the **Sales Quote** window.</span></span>  
7.  <span data-ttu-id="d8199-122">Si el cliente acepta la oferta, cree un pedido de venta para el elemento del ensamblado ofertado.</span><span class="sxs-lookup"><span data-stu-id="d8199-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="d8199-123">Para obtener más información, consulte [Crear ofertas de ventas](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="d8199-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="d8199-124">La oferta de ensamblado vinculada y cualquier personalización se asocian a ese nuevo pedido de venta para preparar el ensamblado del producto o los productos que se van a vender.</span><span class="sxs-lookup"><span data-stu-id="d8199-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8199-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8199-125">See Also</span></span>  
[<span data-ttu-id="d8199-126">Gestión de ensamblaje</span><span class="sxs-lookup"><span data-stu-id="d8199-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="d8199-127">Trabajar con listas de materiales</span><span class="sxs-lookup"><span data-stu-id="d8199-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="d8199-128">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="d8199-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d8199-129">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="d8199-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="d8199-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8199-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

