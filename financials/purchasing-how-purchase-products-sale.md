---
title: Crear una factura de compra a partir de una factura de venta para comprar productos para una venta | Documentos de Microsoft
description: A partir de una factura de venta, para comprar productos, puede crear una factura de compra de un proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="5eb4c-103">Comprar productos para una venta</span><span class="sxs-lookup"><span data-stu-id="5eb4c-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="5eb4c-104">A partir de pedidos y facturas de venta, puede utilizar funciones para crear rápidamente los documentos de compra de las cantidades de productos que faltan que sean necesarias para la venta.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="5eb4c-105">Puede utilizar dos funciones distintas dependiendo del tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="5eb4c-106">Función</span><span class="sxs-lookup"><span data-stu-id="5eb4c-106">Function</span></span>|<span data-ttu-id="5eb4c-107">Description</span><span class="sxs-lookup"><span data-stu-id="5eb4c-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="5eb4c-108">**Crear pedidos de compra**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="5eb4c-109">A partir de un pedido de compra, esta función crea un pedido de compra para cada proveedor de los productos que hay en el pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="5eb4c-110">Puede modificar la cantidad de compra antes de crear los pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="5eb4c-111">Solo se sugieren las cantidades de venta no disponibles.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="5eb4c-112">**Crear factura de compra**</span><span class="sxs-lookup"><span data-stu-id="5eb4c-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="5eb4c-113">A partir de un pedido de venta y desde una factura de venta, esta función crea una factura de compra de un proveedor seleccionado para todas las líneas o las líneas seleccionadas del documento de venta.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="5eb4c-114">Se sugiere la cantidad de venta completa.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="5eb4c-115">Para crear uno o más pedidos de compra a partir de un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="5eb4c-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="5eb4c-116">Para crear un pedido de compra para cada cantidad de producto no disponible en el pedido de venta, utilice la función **Crear pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="5eb4c-117">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="5eb4c-118">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="5eb4c-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="5eb4c-119">En la página Inicio, elija el mosaico **Pedidos de venta en curso**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="5eb4c-120">Abra un pedido de venta para el que desea comprar productos.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="5eb4c-121">Elija la acción **Crear pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="5eb4c-122">Se abre la ventana **Crear pedidos de compra** mostrando una línea para cada producto en el pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="5eb4c-123">Se muestran de forma predeterminada las líneas para las cantidades de venta totalmente disponibles y las cantidades de venta no disponibles (atenuadas).</span><span class="sxs-lookup"><span data-stu-id="5eb4c-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="5eb4c-124">Puede elegir la acción **Mostrar no disponibles** para ver solo las líneas de las cantidades de venta no disponibles.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="5eb4c-125">El campo **Cantidad de compra** contiene la cantidad de venta no disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="5eb4c-126">Para comprar una cantidad distinta de la cantidad de venta no disponible, edite el valor del campo **Cantidad de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="5eb4c-127">También puede cambiar el campo **Cantidad de compra** en las líneas atenuadas aunque representen las cantidades de venta totalmente disponibles.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="5eb4c-128">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="5eb4c-129">Se crea un pedido de compra para cada proveedor de productos del pedido de venta, incluido cualquier cambio de la cantidad que ha realizado en la ventana **Crear pedidos de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="5eb4c-130">Procese el pedido o los pedidos de compra, por ejemplo, mediante la modificación o la adición de las líneas del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="5eb4c-131">Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5eb4c-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="5eb4c-132">Para crear una factura de compra a partir de un pedido o pedidos de venta</span><span class="sxs-lookup"><span data-stu-id="5eb4c-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="5eb4c-133">Para crear una sola factura de compra para una o varias líneas de un documento de ventas seleccionando primero el proveedor al que se compra, utilice la función **Crear factura de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="5eb4c-134">Esta función crea una factura de compra para la cantidad exacta de productos en el documento de venta seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="5eb4c-135">Para cambiar la cantidad de compra, debe modificar la factura de compra después de que se cree.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="5eb4c-136">En la página Inicio, elija el mosaico **Facturas de ventas en curso**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="5eb4c-137">Abra una factura de venta para la que desea comprar productos.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="5eb4c-138">Seleccione una o varias líneas de factura de venta que desee usar en la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="5eb4c-139">Para usar todas las líneas de factura de venta, selecciónelas todas o no seleccione ninguna.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="5eb4c-140">Elija la acción **Crear factura de compra**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="5eb4c-141">Seleccione o **Todas las líneas** o **Líneas seleccionadas** y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="5eb4c-142">En la lista de proveedores que aparece, seleccione el proveedor al que desea comprar todos los productos y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="5eb4c-143">Se crea una factura de compra que contiene una, varias o todas las líneas en la factura de venta.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="5eb4c-144">Procese la factura de compra, por ejemplo, mediante la modificación o la adición de las líneas de la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="5eb4c-145">Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="5eb4c-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb4c-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5eb4c-146">See Also</span></span>
[<span data-ttu-id="5eb4c-147">Compras</span><span class="sxs-lookup"><span data-stu-id="5eb4c-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="5eb4c-148">Registro de compras</span><span class="sxs-lookup"><span data-stu-id="5eb4c-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="5eb4c-149">Facturación de ventas</span><span class="sxs-lookup"><span data-stu-id="5eb4c-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="5eb4c-150">Registro de proveedores nuevos</span><span class="sxs-lookup"><span data-stu-id="5eb4c-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="5eb4c-151">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5eb4c-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

