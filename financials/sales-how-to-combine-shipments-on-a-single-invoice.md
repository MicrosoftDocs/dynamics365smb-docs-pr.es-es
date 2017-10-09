---
title: "Procedimiento: agrupamiento de envíos en una factura única | Documentos de Microsoft"
description: "Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6d94-103">Procedimiento: Agrupamiento de envíos en una factura única</span><span class="sxs-lookup"><span data-stu-id="d6d94-103">How to: Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="d6d94-104">Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.</span><span class="sxs-lookup"><span data-stu-id="d6d94-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="d6d94-105">Para crear una agrupación de envíos, primero debe registrar más de un envío de venta para el mismo cliente en la misma divisa.</span><span class="sxs-lookup"><span data-stu-id="d6d94-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="d6d94-106">Dicho de otro modo, debe haber rellenado dos o más pedidos de venta y haberlos registrado como enviados pero no facturados.</span><span class="sxs-lookup"><span data-stu-id="d6d94-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="d6d94-107">Para agrupar envíos deberá activar la casilla de verificación **Fact. automática** de la ficha desplegable **Envíos** de la ficha del **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6d94-108">Para agrupar envíos de forma manual en una factura única</span><span class="sxs-lookup"><span data-stu-id="d6d94-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="d6d94-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas venta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d6d94-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d6d94-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-110">Choose the **New** action.</span></span> <span data-ttu-id="d6d94-111">Para obtener más información, vea [Procedimiento: Facturar ventas](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="d6d94-111">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="d6d94-112">En el campo **Venta a-N.º cliente**,</span><span class="sxs-lookup"><span data-stu-id="d6d94-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="d6d94-113">introduzca el cliente que recibirá la factura de los productos enviados.</span><span class="sxs-lookup"><span data-stu-id="d6d94-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="d6d94-114">En la ficha desplegable **Líneas**, elija la acción **Traer líns. recep**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="d6d94-115">Seleccione la línea del envío que desee incluir en la factura:</span><span class="sxs-lookup"><span data-stu-id="d6d94-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="d6d94-116">Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="d6d94-117">Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="d6d94-118">Puede utilizar la tecla Ctrl para seleccionar varias líneas no secuenciales.</span><span class="sxs-lookup"><span data-stu-id="d6d94-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="d6d94-119">Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas de la factura y volver a ejecutar la función **Traer líneas alb. venta**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="d6d94-120">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="d6d94-121">Para agrupar envíos de forma automática en una factura única</span><span class="sxs-lookup"><span data-stu-id="d6d94-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="d6d94-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Fact. automática...** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d6d94-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="d6d94-123">Se abre la ventana de solicitud de trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="d6d94-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="d6d94-124">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d6d94-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d6d94-125">Seleccione la casilla de verificación **Registrar facturas**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="d6d94-126">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d6d94-127">Deberá registrar las facturas manualmente si no se ha activado la casilla de verificación **Registrar facturas** en el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="d6d94-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="d6d94-128">Eliminar pedidos de venta abiertos después del registro de envío combinado</span><span class="sxs-lookup"><span data-stu-id="d6d94-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="d6d94-129">Cuando se agrupan envíos en una factura y se registran, se crea una factura de venta registrada para las líneas facturadas.</span><span class="sxs-lookup"><span data-stu-id="d6d94-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="d6d94-130">El campo **Cantidad facturada** del pedido de venta o pedido abierto de venta de origen se actualiza en función de la cantidad facturada.</span><span class="sxs-lookup"><span data-stu-id="d6d94-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="d6d94-131">Al facturar envíos de esta forma, los pedidos a partir de los cuales se registraron los envíos siguen existiendo, aunque se hayan enviado y facturado por completo.</span><span class="sxs-lookup"><span data-stu-id="d6d94-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="d6d94-132">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar ped. venta fact...** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d6d94-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="d6d94-133">Especifique en el campo de filtro **Nº.**</span><span class="sxs-lookup"><span data-stu-id="d6d94-133">Specify in the **No.**</span></span> <span data-ttu-id="d6d94-134">que pedidos de venta desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="d6d94-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="d6d94-135">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d94-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="d6d94-136">También puede eliminar los pedidos de venta individuales manualmente.</span><span class="sxs-lookup"><span data-stu-id="d6d94-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="d6d94-137">Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de ventas.</span><span class="sxs-lookup"><span data-stu-id="d6d94-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6d94-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6d94-138">See Also</span></span>  
[<span data-ttu-id="d6d94-139">Ccial</span><span class="sxs-lookup"><span data-stu-id="d6d94-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d6d94-140">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6d94-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

