---
title: Asociar un pedido de venta a un pedido de compra para un envío directo | Documentos de Microsoft
description: Describe cómo crear un pedido de venta vinculado a un pedido de compra para habilitar el envío directo del proveedor al cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 938b0cc9f35e980ca9121cb037665b8699ca336f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393378"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="26361-103">Realizar envíos directos</span><span class="sxs-lookup"><span data-stu-id="26361-103">Make Drop Shipments</span></span>

<span data-ttu-id="26361-104">Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="26361-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="26361-105">Cuando se marca un pedido de venta para envío directo y se crea un pedido de compra especificando el cliente en el campo **Dirección de envío**, **Dirección del cliente**, se pueden enlazar los dos documentos para indicar al proveedor que realice el envío directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="26361-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="26361-106">Para crear un pedido de venta de envío directo</span><span class="sxs-lookup"><span data-stu-id="26361-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="26361-107">Para preparar un envío directo cree un pedido de venta para un producto e indique en la línea de ventas que dicha venta requiere un envío directo.</span><span class="sxs-lookup"><span data-stu-id="26361-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="26361-108">Cree un pedido de ventas para un artículo.</span><span class="sxs-lookup"><span data-stu-id="26361-108">Create a sales order for an item.</span></span> <span data-ttu-id="26361-109">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="26361-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="26361-110">En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**.</span><span class="sxs-lookup"><span data-stu-id="26361-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="26361-111">Use la función **Elegir columnas** si el campo no está visible.</span><span class="sxs-lookup"><span data-stu-id="26361-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="26361-112">Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="26361-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="26361-113">Para crear pedidos de compra para envíos directos</span><span class="sxs-lookup"><span data-stu-id="26361-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="26361-114">Para preparar un envío directo, debe indicar en el pedido de compra que debe enviarse a su cliente, no a usted mismo.</span><span class="sxs-lookup"><span data-stu-id="26361-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="26361-115">Cree un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="26361-115">Create a purchase order.</span></span> <span data-ttu-id="26361-116">No rellene ningún campo en las líneas.</span><span class="sxs-lookup"><span data-stu-id="26361-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="26361-117">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="26361-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="26361-118">En el campo **Dirección de envío**, seleccione **Dirección del cliente**.</span><span class="sxs-lookup"><span data-stu-id="26361-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="26361-119">En el campo **Cliente**, seleccione el cliente al que está realizando la venta.</span><span class="sxs-lookup"><span data-stu-id="26361-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="26361-120">Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="26361-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="26361-121">En la página **Lista ventas**, seleccione el pedido de ventas que ha preparado en [Para crear un pedido de venta de envío directo](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="26361-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="26361-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="26361-122">Choose the **OK** button.</span></span>

<span data-ttu-id="26361-123">La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="26361-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="26361-124">Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando el pedido de compra por correo electrónico en formato PDF.</span><span class="sxs-lookup"><span data-stu-id="26361-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="26361-125">Para crear varios pedidos de compra para envíos directos</span><span class="sxs-lookup"><span data-stu-id="26361-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="26361-126">También puede utilizar la hoja de demanda para crear el pedido de compra para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="26361-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="26361-127">La ventaja de utilizar la hoja de demanda es que puede crear órdenes de compra para todos los envíos directos pendientes, por lo que no tiene que crear cada uno individualmente.</span><span class="sxs-lookup"><span data-stu-id="26361-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="26361-128">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hojas de demanda** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="26361-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="26361-129">Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="26361-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="26361-130">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="26361-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="26361-131">Revise las líneas del pedido de compra y, en el campo **Nº proveedor**, seleccione el proveedor que suministra los bienes necesarios.</span><span class="sxs-lookup"><span data-stu-id="26361-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="26361-132">Elija la acción **Ejecutar mensajes de acción** para convertir líneas revisadas en un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="26361-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="26361-133">Para ver el pedido de compra vinculado al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="26361-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="26361-134">Seleccione la línea del envío directo del pedido de compra, elija las acciones **Pedido**, **Envío directo** y, a continuación, **Pedido de compra**.</span><span class="sxs-lookup"><span data-stu-id="26361-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="26361-135">Para registrar un envío directo</span><span class="sxs-lookup"><span data-stu-id="26361-135">To post a drop shipment</span></span>

<span data-ttu-id="26361-136">Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados.</span><span class="sxs-lookup"><span data-stu-id="26361-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="26361-137">También puede registrar el pedido de compra, pero solo con la opción **Recibir** hasta que se haya facturado el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="26361-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="26361-138">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="26361-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="26361-139">Abra el pedido de venta que ha creado en [Para crear un pedido de venta de envío directo](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="26361-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="26361-140">En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.</span><span class="sxs-lookup"><span data-stu-id="26361-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="26361-141">Seleccione la acción **Registrar** o **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="26361-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="26361-142">Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.</span><span class="sxs-lookup"><span data-stu-id="26361-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="26361-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26361-143">See Also</span></span>

[<span data-ttu-id="26361-144">Crear pedidos especiales</span><span class="sxs-lookup"><span data-stu-id="26361-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="26361-145">Comprar productos para una venta</span><span class="sxs-lookup"><span data-stu-id="26361-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="26361-146">Vender productos</span><span class="sxs-lookup"><span data-stu-id="26361-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="26361-147">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="26361-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="26361-148">Ccial</span><span class="sxs-lookup"><span data-stu-id="26361-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="26361-149">Inventario</span><span class="sxs-lookup"><span data-stu-id="26361-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="26361-150">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26361-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]