---
title: "Asociar un pedido de venta a un pedido de compra para un envío directo | Documentos de Microsoft"
description: "Describe cómo crear un pedido de venta vinculado a un pedido de compra para habilitar el envío directo del proveedor al cliente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4840cde44374f17dcbd2befb167bfdf6110fe6fe
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="make-drop-shipments"></a><span data-ttu-id="50035-103">Realizar envíos directos</span><span class="sxs-lookup"><span data-stu-id="50035-103">Make Drop Shipments</span></span>
<span data-ttu-id="50035-104">Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="50035-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="50035-105">Cuando marca un pedido de venta con el envío directo y crea un pedido especificando el cliente en el campo **Venta a-N.º cliente**</span><span class="sxs-lookup"><span data-stu-id="50035-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="50035-106">puede vincular los dos documentos y así asignar instrucciones al proveedor para que envíe el producto directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="50035-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="50035-107">Para crear un pedido de venta de envío directo</span><span class="sxs-lookup"><span data-stu-id="50035-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="50035-108">Para preparar un envío directo cree un pedido de venta como si fuese normal, pero indique en la línea de ventas que dicha venta requiere un envío directo.</span><span class="sxs-lookup"><span data-stu-id="50035-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="50035-109">Cree un pedido de ventas para un artículo.</span><span class="sxs-lookup"><span data-stu-id="50035-109">Create a sales order for an item.</span></span> <span data-ttu-id="50035-110">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="50035-110">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="50035-111">En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**.</span><span class="sxs-lookup"><span data-stu-id="50035-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="50035-112">Use la función **Elegir columnas** si el campo no está visible.</span><span class="sxs-lookup"><span data-stu-id="50035-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="50035-113">Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="50035-113">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="50035-114">Para crear pedidos de compra para envíos directos</span><span class="sxs-lookup"><span data-stu-id="50035-114">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="50035-115">Para preparar un envío directo de un producto que se va a vender, cree un pedido de compra como si fuese normal, pero indique en el pedido que el producto debe enviarse directamente al cliente no a usted.</span><span class="sxs-lookup"><span data-stu-id="50035-115">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="50035-116">Cree un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="50035-116">Create a purchase order.</span></span> <span data-ttu-id="50035-117">No rellene ningún campo en las líneas.</span><span class="sxs-lookup"><span data-stu-id="50035-117">Do not fill any fields on the lines.</span></span> <span data-ttu-id="50035-118">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="50035-118">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="50035-119">En el campo **Venta a-N.º cliente**,</span><span class="sxs-lookup"><span data-stu-id="50035-119">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="50035-120">seleccione el cliente al que le está vendiendo.</span><span class="sxs-lookup"><span data-stu-id="50035-120">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="50035-121">Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="50035-121">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="50035-122">En la ventana **Lista ventas**, seleccione el pedido de ventas que ha preparado en la sección "Para crear un pedido de venta de envío directo".</span><span class="sxs-lookup"><span data-stu-id="50035-122">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="50035-123">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="50035-123">Choose the **OK** button.</span></span>

<span data-ttu-id="50035-124">La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="50035-124">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="50035-125">Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando el pedido de compra por correo electrónico en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="50035-125">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="50035-126">Para ver el pedido de compra vinculado al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="50035-126">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="50035-127">Seleccione la línea del envío directo del pedido de compra, elija las acciones **Pedido**, **Envío directo** y, a continuación, **Pedido de compra**.</span><span class="sxs-lookup"><span data-stu-id="50035-127">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="50035-128">Para registrar un envío directo</span><span class="sxs-lookup"><span data-stu-id="50035-128">To post a drop shipment</span></span>
<span data-ttu-id="50035-129">Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados.</span><span class="sxs-lookup"><span data-stu-id="50035-129">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="50035-130">También puede registrar el pedido de compra, pero solo con la opción **Recibir** hasta que se haya facturado el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="50035-130">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="50035-131">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="50035-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="50035-132">Abra el pedido de venta que ha creado en la sección "Para crear un pedido de venta de envío directo".</span><span class="sxs-lookup"><span data-stu-id="50035-132">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="50035-133">En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.</span><span class="sxs-lookup"><span data-stu-id="50035-133">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="50035-134">Seleccione la acción **Registrar** o **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="50035-134">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="50035-135">Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="50035-135">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="50035-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50035-136">See Also</span></span>
<span data-ttu-id="50035-137">[Crear pedidos especiales](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="50035-137">[Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="50035-138">Vender productos</span><span class="sxs-lookup"><span data-stu-id="50035-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="50035-139">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="50035-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="50035-140">Ventas</span><span class="sxs-lookup"><span data-stu-id="50035-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="50035-141">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="50035-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="50035-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50035-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

