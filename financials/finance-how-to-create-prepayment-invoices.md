---
title: "Cómo crear facturas de prepago | Documentos de Microsoft"
description: Conocer el modo de gestionar las situaciones en las que requiere prepago, o lo requiere el proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a><span data-ttu-id="b4d4d-103">Cómo crear facturas de prepago</span><span class="sxs-lookup"><span data-stu-id="b4d4d-103">How to: Create Prepayment Invoices</span></span>
<span data-ttu-id="b4d4d-104">Si desea que sus clientes realicen el pago antes de enviarles un pedido o su proveedor le requiere que efectúe el pago antes de enviarle un pedido, puede utilizar la funcionalidad de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="b4d4d-105">Después de crear un pedido de venta o de compra, puede crear una factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="b4d4d-106">Para ello, puede utilizar los porcentajes predeterminados de cada línea de venta o de compra o bien ajustar el importe según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="b4d4d-107">Por ejemplo, puede especificar un importe total para todo el pedido.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="b4d4d-108">El procedimiento siguiente describe cómo facturar un prepago del pedido.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="b4d4d-109">Los pasos son parecidos para pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="b4d4d-110">Para crear una factura de prepago</span><span class="sxs-lookup"><span data-stu-id="b4d4d-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="b4d4d-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b4d4d-112">Crear un nuevo pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-112">Create a new sales order.</span></span> <span data-ttu-id="b4d4d-113">Para obtener más información, vea [Procedimiento: Vender productos](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="b4d4d-113">For more information, see [How to: sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="b4d4d-114">En la ficha desplegable **Prepago**, el campo **% prepago** de la cabecera se rellenará automáticamente si existe un porcentaje de prepago predeterminado en la ficha del cliente.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="b4d4d-115">Puede cambiar el contenido del campo.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-115">You can change the contents of the field.</span></span> <span data-ttu-id="b4d4d-116">El porcentaje de prepago sólo se copia desde la cabecera en las líneas que no copian dicho porcentaje predeterminado del producto.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="b4d4d-117">Si el campo **Compresión prepago** está seleccionado, las líneas se agruparán en la factura si:</span><span class="sxs-lookup"><span data-stu-id="b4d4d-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="b4d4d-118">Tienen la misma cuenta para los prepagos, tal y como lo haya determinado en la configuración de grupos contables.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="b4d4d-119">Tienen las mismas dimensiones.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="b4d4d-120">Deje el campo en blanco si desea especificar una factura de prepago con una línea para cada línea de pedido de venta que tenga un porcentaje de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="b4d4d-121">Rellene las líneas de venta.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="b4d4d-122">Si se han definido porcentajes de prepago para los productos, se copian automáticamente en el campo **% de prepago** de la línea.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="b4d4d-123">De lo contrario, el porcentaje de prepago se copia de la cabecera.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="b4d4d-124">Puede cambiar el contenido del campo **% de prepago** en la línea.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="b4d4d-125">Si desea aplicar un porcentaje de prepago a todo el pedido, modifique el campo **% de prepago** en la cabecera después de rellenar las líneas.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="b4d4d-126">Para ver el importe de prepago total, elija la acción **Estadísticas**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="b4d4d-127">Si desea ajustar el importe de prepago total para el pedido, puede cambiar los contenidos del campo **Importe prepago** en la ventana **Estad. pedido ventas**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="b4d4d-128">Si se selecciona el campo **Precios IVA incluido**, el campo **Cantidad prepago incl. IVA** se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="b4d4d-129">Si cambia el contenido del campo **Cantidad prepago**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas cuyo valor es **0** en el campo **% de prepago**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="b4d4d-130">Para imprimir un test antes de registrar la factura de prepago, elija las acciones **Prepago** e **Informe test prepago**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="b4d4d-131">Para registrar una factura de prepago, elija las acciones **Prepago** y **Registrar factura prepago**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="b4d4d-132">Para registrar e imprimir la factura de prepago, seleccione la acción **Registrar e imprimir factura prepago**.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="b4d4d-133">Puede emitir facturas de prepago adicionales para el pedido.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="b4d4d-134">Para ello, aumente la cantidad de prepago de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="b4d4d-135">Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas hasta el momento y la nueva cantidad de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b4d4d-136">Si se encuentra en América del Norte, no puede cambiar el porcentaje de prepago después de que se haya contabilizado la factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="b4d4d-137">Esto se evita en la versión americana de [!INCLUDE[d365fin](includes/d365fin_md.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="b4d4d-138">Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de prepago se descontará automáticamente del importe vencido.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b4d4d-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b4d4d-139">See Also</span></span>  
[<span data-ttu-id="b4d4d-140">Facturación de prepagos</span><span class="sxs-lookup"><span data-stu-id="b4d4d-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="b4d4d-141">Tutorial: Configuración y facturación de prepagos de ventas</span><span class="sxs-lookup"><span data-stu-id="b4d4d-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="b4d4d-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="b4d4d-142">Finance</span></span>](finance.md)  
<span data-ttu-id="b4d4d-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4d4d-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

