---
title: Modificar o cancelar facturas de compra sin abonar | Documentos de Microsoft
description: "Explica cómo corregir, cancelar o deshacer una factura de compra registrada y crear automáticamente un abono de compra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75a56e6089567c456280b2cc287dda62fb4f3f8b
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="c3bd3-103">Corrección o cancelación de facturas de compra sin abonar</span><span class="sxs-lookup"><span data-stu-id="c3bd3-103">How to: Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="c3bd3-104">Puede corregir o cancelar una factura de compra registrada.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="c3bd3-105">Esto es útil si se desea corregir un error de escritura o si desea cambiar la compra de forma anticipada en el proceso de pedido.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="c3bd3-106">Si ya ha pagado productos en la factura de compra registrada, no puede corregirla o cancelarla desde la factura de compra registrada en sí.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="c3bd3-107">En su lugar, debe crear manualmente un abono de compra para revertir la compra.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-107">Instead, you must manually create a purchase credit memo to reverse the purchase.</span></span> <span data-ttu-id="c3bd3-108">Para obtener más información, vea [Procedimiento: Procesar devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="c3bd3-108">For more information, see [How to: Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="c3bd3-109">En la ventana **Factura de compra registrada**, puede elegir el botón **Corregir** o **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-109">In the **Posted Purchase Invoice** window, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="c3bd3-110">Al corregir o cancelar una factura de compra registrada, el abono de compra de corrección se aplica a todos los movimientos contables y del inventario que se crearon cuando se registró la factura de compra inicial.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="c3bd3-111">De esta forma se invierte la factura de compra registrada en los registros financieros deja el abono de compra registrado de corrección para el seguimiento de auditoria.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="c3bd3-112">A continuación se describe el uso de **Corregir** y **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="c3bd3-113">Para corregir una factura de compra registrada</span><span class="sxs-lookup"><span data-stu-id="c3bd3-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="c3bd3-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico facturas compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c3bd3-115">Seleccione la factura de compra registrada que desea corregir.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="c3bd3-116">Si se selecciona la casilla **Cancelado**, no puede corregir la factura de compra registrada porque ya se ha corregido o cancelado.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="c3bd3-117">En la ventana **Factura de compra registrada**, elija **Corregir**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-117">In the **Posted Purchase Invoice** window, choose **Correct**.</span></span>

    <span data-ttu-id="c3bd3-118">Una nueva factura de compra con la misma información se crea donde puede realizar la corrección.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="c3bd3-119">Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="c3bd3-119">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="c3bd3-120">El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="c3bd3-121">Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="c3bd3-122">Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="c3bd3-123">Para cancelar una factura de compra registrada</span><span class="sxs-lookup"><span data-stu-id="c3bd3-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="c3bd3-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico facturas compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c3bd3-125">Seleccione la factura de compra registrada que desea cancelar.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="c3bd3-126">Si se selecciona la casilla **Cancelado**, no puede cancelar la factura de compra registrada porque ya se ha cancelado o corregido.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="c3bd3-127">En la ventana **Factura de compra registrada**, elija **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-127">In the **Posted Purchase Invoice** window, choose **Cancel**.</span></span>

    <span data-ttu-id="c3bd3-128">Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="c3bd3-129">El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="c3bd3-130">Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.</span><span class="sxs-lookup"><span data-stu-id="c3bd3-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3bd3-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c3bd3-131">See Also</span></span>
[<span data-ttu-id="c3bd3-132">Compras</span><span class="sxs-lookup"><span data-stu-id="c3bd3-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c3bd3-133">Registro de compras</span><span class="sxs-lookup"><span data-stu-id="c3bd3-133">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="c3bd3-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c3bd3-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

