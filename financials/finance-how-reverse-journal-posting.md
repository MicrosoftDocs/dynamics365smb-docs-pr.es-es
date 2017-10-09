---
title: "Deshacer un registro registrando el movimiento de reversión | Documentos de Microsoft"
description: "Si ha realizado un registro erróneo en el diario general, puede utilizar la función Revertir transacción para deshacer el registro con un seguimiento de auditoria correcto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 802171d4f421270cb7e9b4f9dfedec9b9fe5ddc6
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-postings"></a><span data-ttu-id="d648a-103">Revertir registros</span><span class="sxs-lookup"><span data-stu-id="d648a-103">How to: Reverse Postings</span></span>
<span data-ttu-id="d648a-104">Para deshacer un registro erróneo del diario, seleccione un movimiento y cree un movimiento de reversión (movimientos idénticos al original, pero con el signo contrario en el campo de importe) con el mismo número de documento y la misma fecha de registro que el movimiento original.</span><span class="sxs-lookup"><span data-stu-id="d648a-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="d648a-105">Después de revertir un movimiento, debe registrar el movimiento correcto.</span><span class="sxs-lookup"><span data-stu-id="d648a-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="d648a-106">Solo se pueden revertir los movimientos que están registrados desde una línea del diario general.</span><span class="sxs-lookup"><span data-stu-id="d648a-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="d648a-107">Un movimiento solo se puede revertir una vez.</span><span class="sxs-lookup"><span data-stu-id="d648a-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="d648a-108">Para obtener más información sobre el registro desde un diario general, vea [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="d648a-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="d648a-109">Si ha realizado un registro de una cantidad negativa errónea, como un pedido de compra con un número de productos erróneo y lo ha registrado como recibido, pero no facturado, puede deshacer el registro.</span><span class="sxs-lookup"><span data-stu-id="d648a-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="d648a-110">Si ha realizado un registro de una cantidad positiva errónea, como un pedido de devolución de compra con un número de productos erróneo y lo ha registrado como enviado, pero no facturado, puede deshacer el registro.</span><span class="sxs-lookup"><span data-stu-id="d648a-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="d648a-111">Para revertir el registro de diario de un movimiento de contabilidad</span><span class="sxs-lookup"><span data-stu-id="d648a-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="d648a-112">Se pueden revertir movimientos desde todas las ventanas **Movimientos**.</span><span class="sxs-lookup"><span data-stu-id="d648a-112">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="d648a-113">El siguiente procedimiento se basa en la ventana **Movs. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="d648a-113">The following procedure is based on the **General Ledger Entries** window.</span></span>
1. <span data-ttu-id="d648a-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movs. contabilidad** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d648a-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="d648a-115">Seleccione el movimiento que desea revertir y, después, seleccione **Revertir transacción**.</span><span class="sxs-lookup"><span data-stu-id="d648a-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="d648a-116">Tenga en cuenta que debe proceder de un registro de diario.</span><span class="sxs-lookup"><span data-stu-id="d648a-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="d648a-117">En la ventana **Revertir movs. trans.**, seleccione el movimiento relevante y, después, seleccione la acción **Revertir**.</span><span class="sxs-lookup"><span data-stu-id="d648a-117">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="d648a-118">Elija el botón **Sí** para en el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="d648a-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="d648a-119">Para deshacer la cantidad registrada en un albarán de compra registrado</span><span class="sxs-lookup"><span data-stu-id="d648a-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="d648a-120">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico albaranes compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d648a-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d648a-121">Abra la recepción registrada que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="d648a-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="d648a-122">Selecciones las líneas del diario que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="d648a-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="d648a-123">Seleccione la acción **Deshacer albarán**.</span><span class="sxs-lookup"><span data-stu-id="d648a-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="d648a-124">Una línea correctiva se inserta bajo la línea de recepción seleccionada.</span><span class="sxs-lookup"><span data-stu-id="d648a-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="d648a-125">Si la cantidad se ha recibido en una recepción de almacén, entonces se inserta una línea de corrección en la recepción de almacén registrado.</span><span class="sxs-lookup"><span data-stu-id="d648a-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="d648a-126">Los campos de **Cantidad recibida** y de **Cdad. Rec. no facturada** en el pedido de compra relacionado se establecerán a cero.</span><span class="sxs-lookup"><span data-stu-id="d648a-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="d648a-127">Deshacer y rehacer una cantidad registrada en un envío devuelto registrado</span><span class="sxs-lookup"><span data-stu-id="d648a-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="d648a-128">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico envíos devolución** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d648a-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d648a-129">Abra el envío devolución registrado que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="d648a-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="d648a-130">Selecciones las líneas del diario que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="d648a-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="d648a-131">Elija la acción **Deshacer envío dev.**.</span><span class="sxs-lookup"><span data-stu-id="d648a-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="d648a-132">Se insertará una línea de corrección en el documento registrado y los campos **Cantidad dev. enviada** y **Dev. enviadas no facturadas** del pedido de devolución se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="d648a-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="d648a-133">Ahora vuelva al pedido de devolución de compra para volver a realizar el registro.</span><span class="sxs-lookup"><span data-stu-id="d648a-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="d648a-134">En la ventana **Histórico envío devolución**, tome una nota del número en el campo **Nº devolución**</span><span class="sxs-lookup"><span data-stu-id="d648a-134">In the **Posted Return Shipment** window, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="d648a-135">.</span><span class="sxs-lookup"><span data-stu-id="d648a-135">field.</span></span>  
6.  <span data-ttu-id="d648a-136">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos dev. compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d648a-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="d648a-137">Abra el pedido de devolución en cuestión y, a continuación, elija la acción **Volver a abrir**.</span><span class="sxs-lookup"><span data-stu-id="d648a-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="d648a-138">Corrija el movimiento en el campo **Cantidad** y vuelva a publicar la orden de devolución de la compra.</span><span class="sxs-lookup"><span data-stu-id="d648a-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d648a-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d648a-139">See Also</span></span>
[<span data-ttu-id="d648a-140">Registrar transacciones directamente en la contabilidad</span><span class="sxs-lookup"><span data-stu-id="d648a-140">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="d648a-141">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="d648a-141">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="d648a-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="d648a-142">Finance</span></span>](finance.md)  
<span data-ttu-id="d648a-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d648a-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

