---
title: 'Procedimiento: agrupamiento de envíos en una factura única | Documentos de Microsoft'
description: Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2936e819ba50adde6df021cc0dc2694367c29fc9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778502"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="263f3-103">Agrupar envíos en una factura única</span><span class="sxs-lookup"><span data-stu-id="263f3-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="263f3-104">Si desea facturar varios envíos a la vez, utilice la función de agrupación de envíos.</span><span class="sxs-lookup"><span data-stu-id="263f3-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="263f3-105">Para crear una agrupación de envíos, primero debe registrar más de un envío de venta para el mismo cliente en la misma divisa.</span><span class="sxs-lookup"><span data-stu-id="263f3-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="263f3-106">Dicho de otro modo, debe haber creado dos o más pedidos de venta y haberlos registrado como enviados pero no facturados.</span><span class="sxs-lookup"><span data-stu-id="263f3-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="263f3-107">Para agrupar envíos de forma manual en una factura única</span><span class="sxs-lookup"><span data-stu-id="263f3-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="263f3-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="263f3-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="263f3-109">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="263f3-109">Choose the **New** action.</span></span> <span data-ttu-id="263f3-110">Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="263f3-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="263f3-111">En el campo **Venta a-N.º cliente**,</span><span class="sxs-lookup"><span data-stu-id="263f3-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="263f3-112">introduzca el cliente que recibirá la factura de los productos enviados.</span><span class="sxs-lookup"><span data-stu-id="263f3-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="263f3-113">En la ficha desplegable **Líneas**, elija la acción **Traer líns. recep**.</span><span class="sxs-lookup"><span data-stu-id="263f3-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="263f3-114">Seleccione la línea del envío que desee incluir en la factura:</span><span class="sxs-lookup"><span data-stu-id="263f3-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="263f3-115">Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="263f3-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="263f3-116">Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="263f3-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="263f3-117">Puede utilizar la tecla Ctrl para seleccionar varias líneas no secuenciales.</span><span class="sxs-lookup"><span data-stu-id="263f3-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="263f3-118">Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas de la factura y volver a ejecutar la función **Traer líneas alb. venta**.</span><span class="sxs-lookup"><span data-stu-id="263f3-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="263f3-119">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="263f3-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="263f3-120">Para agrupar envíos de forma automática en una factura única</span><span class="sxs-lookup"><span data-stu-id="263f3-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="263f3-121">seleccionará solo pedidos de venta donde se elija **Combinar envíos**.</span><span class="sxs-lookup"><span data-stu-id="263f3-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="263f3-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Fact. automática** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="263f3-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="263f3-123">Se abre la página de solicitud de trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="263f3-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="263f3-124">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="263f3-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="263f3-125">Elija la casilla de verificación **Registrar facturas**.</span><span class="sxs-lookup"><span data-stu-id="263f3-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="263f3-126">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="263f3-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="263f3-127">Deberá registrar las facturas manualmente si no se ha activado la casilla de verificación **Registrar facturas** en el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="263f3-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="263f3-128">Eliminar pedidos de venta abiertos después del registro de envío combinado</span><span class="sxs-lookup"><span data-stu-id="263f3-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="263f3-129">Cuando se agrupan envíos en una factura y se registran, se crea una factura de venta registrada para las líneas facturadas.</span><span class="sxs-lookup"><span data-stu-id="263f3-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="263f3-130">El campo **Cantidad facturada** del pedido de venta o pedido abierto de venta de origen se actualiza en función de la cantidad facturada.</span><span class="sxs-lookup"><span data-stu-id="263f3-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="263f3-131">Al facturar envíos de esta forma, los pedidos a partir de los cuales se registraron los envíos siguen existiendo, aunque se hayan enviado y facturado por completo.</span><span class="sxs-lookup"><span data-stu-id="263f3-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="263f3-132">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Eliminar ped. venta fact.** y luego seleccione el enlace.</span><span class="sxs-lookup"><span data-stu-id="263f3-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="263f3-133">Especifique en el campo de filtro **Nº.**</span><span class="sxs-lookup"><span data-stu-id="263f3-133">Specify in the **No.**</span></span> <span data-ttu-id="263f3-134">que pedidos de venta desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="263f3-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="263f3-135">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="263f3-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="263f3-136">También puede eliminar los pedidos de venta individuales manualmente.</span><span class="sxs-lookup"><span data-stu-id="263f3-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="263f3-137">Repita las tareas 1 a 3 para cualquier otro documento asignado, como pedidos abiertos de ventas.</span><span class="sxs-lookup"><span data-stu-id="263f3-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="263f3-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="263f3-138">See Also</span></span>  
[<span data-ttu-id="263f3-139">Ccial</span><span class="sxs-lookup"><span data-stu-id="263f3-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="263f3-140">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="263f3-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]