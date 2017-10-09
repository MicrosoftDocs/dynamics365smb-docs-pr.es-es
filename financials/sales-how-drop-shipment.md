---
title: "Crear un pedido de venta asociado a un pedido de compra para un envío directo | Documentos de Microsoft"
description: "Describe cómo crear un pedido de venta vinculado a un pedido de compra para habilitar el envío directo del proveedor al cliente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="f227b-103">Procedimiento: Realizar envíos directos</span><span class="sxs-lookup"><span data-stu-id="f227b-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="f227b-104">Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="f227b-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="f227b-105">Cuando marca un pedido de venta con el envío directo y crea un pedido especificando el cliente en el campo **Venta a-N.º cliente**</span><span class="sxs-lookup"><span data-stu-id="f227b-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="f227b-106">puede vincular los dos documentos y así asignar instrucciones al proveedor para que envíe el producto directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="f227b-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="f227b-107">Para crear un pedido de venta de envío directo</span><span class="sxs-lookup"><span data-stu-id="f227b-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="f227b-108">Para preparar un envío directo cree un pedido de venta como si fuese normal, pero indique en la línea de ventas que dicha venta requiere un envío directo.</span><span class="sxs-lookup"><span data-stu-id="f227b-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="f227b-109">Cree un pedido de ventas para un artículo.</span><span class="sxs-lookup"><span data-stu-id="f227b-109">Create a sales order for an item.</span></span> <span data-ttu-id="f227b-110">Para obtener más información, vea [Procedimiento: Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="f227b-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="f227b-111">En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**.</span><span class="sxs-lookup"><span data-stu-id="f227b-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="f227b-112">Use la función **Elegir columnas** si el campo no está visible.</span><span class="sxs-lookup"><span data-stu-id="f227b-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="f227b-113">Para obtener más información, vea [Personalización del usuario](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="f227b-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="f227b-114">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="f227b-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="f227b-115">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="f227b-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="f227b-116">Para crear pedidos de compra para envíos directos</span><span class="sxs-lookup"><span data-stu-id="f227b-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="f227b-117">Para preparar un envío directo de un producto que se va a vender, cree un pedido de compra como si fuese normal, pero indique en el pedido que el producto debe enviarse directamente al cliente no a usted.</span><span class="sxs-lookup"><span data-stu-id="f227b-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="f227b-118">Cree un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="f227b-118">Create a purchase order.</span></span> <span data-ttu-id="f227b-119">No rellene ningún campo en las líneas.</span><span class="sxs-lookup"><span data-stu-id="f227b-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="f227b-120">Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="f227b-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="f227b-121">En el campo **Venta a-N.º cliente**,</span><span class="sxs-lookup"><span data-stu-id="f227b-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="f227b-122">seleccione el cliente al que le está vendiendo.</span><span class="sxs-lookup"><span data-stu-id="f227b-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="f227b-123">Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="f227b-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="f227b-124">En la ventana **Lista ventas**, seleccione el pedido de ventas que ha preparado en la sección "Para crear un pedido de venta de envío directo".</span><span class="sxs-lookup"><span data-stu-id="f227b-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="f227b-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f227b-125">Choose the **OK** button.</span></span>

<span data-ttu-id="f227b-126">La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="f227b-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="f227b-127">Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando el pedido de compra por correo electrónico en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="f227b-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="f227b-128">Para ver el pedido de compra vinculado al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="f227b-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="f227b-129">Seleccione la línea del envío directo del pedido de compra, elija las acciones **Pedido**, **Envío directo** y, a continuación, **Pedido de compra**.</span><span class="sxs-lookup"><span data-stu-id="f227b-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="f227b-130">Para registrar un envío directo</span><span class="sxs-lookup"><span data-stu-id="f227b-130">To post a drop shipment</span></span>
<span data-ttu-id="f227b-131">Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados.</span><span class="sxs-lookup"><span data-stu-id="f227b-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="f227b-132">También puede registrar el pedido de compra, pero solo con la opción **Recibir** hasta que se haya facturado el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="f227b-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="f227b-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f227b-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f227b-134">Abra el pedido de venta que ha creado en la sección "Para crear un pedido de venta de envío directo".</span><span class="sxs-lookup"><span data-stu-id="f227b-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="f227b-135">En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.</span><span class="sxs-lookup"><span data-stu-id="f227b-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="f227b-136">Seleccione la acción **Registrar** o **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="f227b-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="f227b-137">Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="f227b-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="f227b-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f227b-138">See Also</span></span>
<span data-ttu-id="f227b-139">[Procedimiento: crear pedidos especiales](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="f227b-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="f227b-140">Vender productos</span><span class="sxs-lookup"><span data-stu-id="f227b-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="f227b-141">Procedimiento: Registro de compras</span><span class="sxs-lookup"><span data-stu-id="f227b-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="f227b-142">Ccial</span><span class="sxs-lookup"><span data-stu-id="f227b-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f227b-143">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="f227b-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f227b-144">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f227b-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

