---
title: Cómo crear facturas de prepago | Documentos de Microsoft
description: Conocer el modo de gestionar las situaciones en las que requiere prepago, o lo requiere el proveedor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 57284dc738ba35c9865bd25f9c180827d4c59c94
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913376"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="1ca07-103">Crear facturas de prepagos</span><span class="sxs-lookup"><span data-stu-id="1ca07-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="1ca07-104">Si requiere que sus clientes envíen el pago antes de enviarles un pedido, puede usar la funcionalidad de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="1ca07-105">Lo mismo se aplica si su proveedor requiere que envíe el pago antes de enviarle un pedido.</span><span class="sxs-lookup"><span data-stu-id="1ca07-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="1ca07-106">Puede iniciar el proceso de prepago cuando cree un pedido de venta o de compra.</span><span class="sxs-lookup"><span data-stu-id="1ca07-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="1ca07-107">Si tiene un porcentaje de prepago predeterminado para este cliente o proveedor, se incluirá automáticamente en la factura de prepago resultante.</span><span class="sxs-lookup"><span data-stu-id="1ca07-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="1ca07-108">También puede especificar un porcentaje de prepago para todo el documento.</span><span class="sxs-lookup"><span data-stu-id="1ca07-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="1ca07-109">Después de crear un pedido de venta o de compra, puede crear una factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="1ca07-110">Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1ca07-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="1ca07-111">Por ejemplo, puede especificar un importe total para todo el pedido.</span><span class="sxs-lookup"><span data-stu-id="1ca07-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="1ca07-112">El procedimiento siguiente describe cómo facturar un prepago del pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="1ca07-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="1ca07-113">Los pasos son parecidos para pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="1ca07-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="1ca07-114">Para crear una factura de prepago</span><span class="sxs-lookup"><span data-stu-id="1ca07-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="1ca07-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1ca07-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ca07-116">Cree un pedido de venta nuevo para un cliente relevante.</span><span class="sxs-lookup"><span data-stu-id="1ca07-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="1ca07-117">Para obtener más información, vea [Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="1ca07-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="1ca07-118">En la ficha desplegable **Prepago**, el campo **% de prepago** especifica el porcentaje que se utilizará para calcular el importe de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="1ca07-119">Si existe un porcentaje de prepago predeterminado en la ficha del cliente, el campo se rellenará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1ca07-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="1ca07-120">Puede cambiar el porcentaje.</span><span class="sxs-lookup"><span data-stu-id="1ca07-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="1ca07-121">Elija el campo **Compreión prepago** si desea crear líneas en la factura de prepago que combinen líneas del pedido de cliente si:</span><span class="sxs-lookup"><span data-stu-id="1ca07-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="1ca07-122">Tienen la misma cuenta para los prepagos, tal y como lo haya determinado en la configuración de grupos contables.</span><span class="sxs-lookup"><span data-stu-id="1ca07-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="1ca07-123">Tienen las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="1ca07-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="1ca07-124">Si desea especificar una factura de prepago con una línea para cada línea de pedido de venta que tenga un porcentaje de prepago, después, no elija el campo **Compresión prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="1ca07-125">La fecha de vencimiento del prepago se calcula automáticamente en función del valor de **Código términos prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="1ca07-126">Rellene las líneas de venta.</span><span class="sxs-lookup"><span data-stu-id="1ca07-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="1ca07-127">Si ha especificado un porcentaje de prepago predeterminado para el cliente o en la ficha desplegalbe **Prepago** en este documento, este valor se copia en cada línea.</span><span class="sxs-lookup"><span data-stu-id="1ca07-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="1ca07-128">Puede cambiar el contenido del campo **% de prepago** en la línea.</span><span class="sxs-lookup"><span data-stu-id="1ca07-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="1ca07-129">Para ver el importe de prepago total, elija la acción **Estadísticas**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="1ca07-130">Si desea ajustar el importe de prepago total para el pedido, puede cambiar los contenidos del campo **Importe prepago** en la página **Estad. pedido ventas**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="1ca07-131">Si se selecciona el campo **Precios IVA incluido**, el campo **Cantidad prepago incl. IVA** se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="1ca07-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="1ca07-132">Si cambia el contenido del campo **Cantidad prepago**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="1ca07-133">Para imprimir un test antes de registrar la factura de prepago, elija las acciones **Prepago** e **Informe test prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="1ca07-134">Para registrar una factura de prepago, elija las acciones **Prepago** y **Registrar factura prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="1ca07-135">Para registrar e imprimir la factura de prepago, seleccione la acción **Registrar e imprimir factura prepago**.</span><span class="sxs-lookup"><span data-stu-id="1ca07-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="1ca07-136">Puede emitir facturas de prepago adicionales para el pedido.</span><span class="sxs-lookup"><span data-stu-id="1ca07-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="1ca07-137">Para ello, aumente la cantidad de prepago de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="1ca07-138">Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas hasta el momento y la nueva cantidad de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="1ca07-139">Si se encuentra en América del Norte, no puede cambiar el porcentaje de prepago después de que se haya contabilizado la factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="1ca07-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="1ca07-140">Esto se evita en la versión americana de [!INCLUDE[d365fin](includes/d365fin_md.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1ca07-140">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="1ca07-141">Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de prepago se descontará automáticamente del importe vencido.</span><span class="sxs-lookup"><span data-stu-id="1ca07-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ca07-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ca07-142">See Also</span></span>

[<span data-ttu-id="1ca07-143">Facturación de prepagos</span><span class="sxs-lookup"><span data-stu-id="1ca07-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="1ca07-144">Tutorial: Configuración y facturación de prepagos de ventas</span><span class="sxs-lookup"><span data-stu-id="1ca07-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="1ca07-145">Finanzas</span><span class="sxs-lookup"><span data-stu-id="1ca07-145">Finance</span></span>](finance.md)  
<span data-ttu-id="1ca07-146">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ca07-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
