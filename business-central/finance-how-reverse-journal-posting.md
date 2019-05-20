---
title: Deshacer un registro registrando el movimiento de reversión | Documentos de Microsoft
description: Si ha realizado un registro erróneo en el diario general, puede utilizar la función Revertir transacción para deshacer el registro con un seguimiento de auditoria correcto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2767fca96e1f3689fc4806d878381d02622f261
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243738"
---
# <a name="reverse-postings"></a><span data-ttu-id="04409-103">Revertir registros</span><span class="sxs-lookup"><span data-stu-id="04409-103">Reverse Postings</span></span>
<span data-ttu-id="04409-104">Para deshacer un registro erróneo del diario, seleccione un movimiento y cree un movimiento de reversión (movimientos idénticos al original, pero con el signo contrario en el campo de importe) con el mismo número de documento y la misma fecha de registro que el movimiento original.</span><span class="sxs-lookup"><span data-stu-id="04409-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="04409-105">Después de revertir un movimiento, debe registrar el movimiento correcto.</span><span class="sxs-lookup"><span data-stu-id="04409-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="04409-106">Solo se pueden revertir los movimientos que están registrados desde una línea del diario general.</span><span class="sxs-lookup"><span data-stu-id="04409-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="04409-107">Un movimiento solo se puede revertir una vez.</span><span class="sxs-lookup"><span data-stu-id="04409-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="04409-108">Para obtener más información sobre el registro desde un diario general, vea [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="04409-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="04409-109">Si ha realizado un registro de una cantidad negativa errónea, como un pedido de compra con un número de productos erróneo y lo ha registrado como recibido, pero no facturado, puede deshacer el registro.</span><span class="sxs-lookup"><span data-stu-id="04409-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="04409-110">Si ha realizado un registro de una cantidad positiva errónea, como un pedido de devolución de compra con un número de productos erróneo y lo ha registrado como enviado, pero no facturado, puede deshacer el registro.</span><span class="sxs-lookup"><span data-stu-id="04409-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="04409-111">Para revertir el registro de diario de un movimiento de contabilidad</span><span class="sxs-lookup"><span data-stu-id="04409-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="04409-112">Se pueden revertir movimientos desde todas las páginas **Movimientos**.</span><span class="sxs-lookup"><span data-stu-id="04409-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="04409-113">El siguiente procedimiento se basa en la página **Movs. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="04409-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="04409-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Movs. contabilidad** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="04409-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="04409-115">Seleccione el movimiento que desea revertir y, después, seleccione **Revertir transacción**.</span><span class="sxs-lookup"><span data-stu-id="04409-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="04409-116">Tenga en cuenta que debe proceder de un registro de diario.</span><span class="sxs-lookup"><span data-stu-id="04409-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="04409-117">En la página **Revertir movs. trans.**, seleccione el movimiento relevante y, después, seleccione la acción **Revertir**.</span><span class="sxs-lookup"><span data-stu-id="04409-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="04409-118">Elija el botón **Sí** para en el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="04409-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="04409-119">Para deshacer la cantidad registrada en un albarán de compra registrado</span><span class="sxs-lookup"><span data-stu-id="04409-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="04409-120">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico albaranes compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="04409-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04409-121">Abra la recepción registrada que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="04409-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="04409-122">Selecciones las líneas del diario que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="04409-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="04409-123">Seleccione la acción **Deshacer albarán**.</span><span class="sxs-lookup"><span data-stu-id="04409-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="04409-124">Una línea correctiva se inserta bajo la línea de recepción seleccionada.</span><span class="sxs-lookup"><span data-stu-id="04409-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="04409-125">Si la cantidad se ha recibido en una recepción de almacén, entonces se inserta una línea de corrección en la recepción de almacén registrado.</span><span class="sxs-lookup"><span data-stu-id="04409-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="04409-126">Los campos de **Cantidad recibida** y de **Cdad. Rec. no facturada** en el pedido de compra relacionado se establecerán a cero.</span><span class="sxs-lookup"><span data-stu-id="04409-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="04409-127">Deshacer y rehacer una cantidad registrada en un envío devuelto registrado</span><span class="sxs-lookup"><span data-stu-id="04409-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="04409-128">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Histórico envíos devolución** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="04409-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="04409-129">Abra el envío devolución registrado que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="04409-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="04409-130">Selecciones las líneas del diario que desea deshacer.</span><span class="sxs-lookup"><span data-stu-id="04409-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="04409-131">Elija la acción **Deshacer envío dev.**.</span><span class="sxs-lookup"><span data-stu-id="04409-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="04409-132">Se insertará una línea de corrección en el documento registrado y los campos **Cantidad dev. enviada** y **Dev. enviadas no facturadas** del pedido de devolución se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="04409-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="04409-133">Ahora vuelva al pedido de devolución de compra para volver a realizar el registro.</span><span class="sxs-lookup"><span data-stu-id="04409-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="04409-134">En la página **Histórico envío devolución**, tome una nota del número en el campo **Nº devolución**</span><span class="sxs-lookup"><span data-stu-id="04409-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="04409-135">.</span><span class="sxs-lookup"><span data-stu-id="04409-135">field.</span></span>  
6.  <span data-ttu-id="04409-136">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos devolución compra** y luego seleccione el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="04409-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="04409-137">Abra el pedido de devolución en cuestión y, a continuación, elija la acción **Volver a abrir**.</span><span class="sxs-lookup"><span data-stu-id="04409-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="04409-138">Corrija el movimiento en el campo **Cantidad** y vuelva a publicar la orden de devolución de la compra.</span><span class="sxs-lookup"><span data-stu-id="04409-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="04409-139">Para registrar un movimiento negativo</span><span class="sxs-lookup"><span data-stu-id="04409-139">To post a negative entry</span></span>  
<span data-ttu-id="04409-140">Puede utilizar el campo **Corrección** para enviar un adeudo negativo en lugar de un abono, o registrar un crédito negativo en vez de un débito en una cuenta.</span><span class="sxs-lookup"><span data-stu-id="04409-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="04409-141">Para cumplir los requisitos legales, este campo estará visible de forma predeterminada en todos los diarios.</span><span class="sxs-lookup"><span data-stu-id="04409-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="04409-142">Los campos **Importe debe** e **Importe haber** incluyen tanto el movimiento original como el corregido.</span><span class="sxs-lookup"><span data-stu-id="04409-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="04409-143">Estos campos no influyen en el saldo de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="04409-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="04409-144">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios generales** y luego elija el enlace relacionado</span><span class="sxs-lookup"><span data-stu-id="04409-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="04409-145">En el campo **Nombre sección**, seleccione el nombre de sección requerido.</span><span class="sxs-lookup"><span data-stu-id="04409-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="04409-146">Escriba información en los campos relevantes.</span><span class="sxs-lookup"><span data-stu-id="04409-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="04409-147">En la línea del diario que desea activar para los movimientos negativos, seleccione la casilla de activación **Corrección**.</span><span class="sxs-lookup"><span data-stu-id="04409-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="04409-148">Para registrar el diario, elija la acción **Registrar** y el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="04409-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="04409-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04409-149">See Also</span></span>
[<span data-ttu-id="04409-150">Registrar transacciones directamente en la contabilidad</span><span class="sxs-lookup"><span data-stu-id="04409-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="04409-151">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="04409-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="04409-152">Finanzas</span><span class="sxs-lookup"><span data-stu-id="04409-152">Finance</span></span>](finance.md)  
<span data-ttu-id="04409-153">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04409-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
