---
title: "Deshacer un registro de diario registrando el movimiento de reversión | Documentos de Microsoft"
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
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="8e3ef-103">Revertir un registro de diario</span><span class="sxs-lookup"><span data-stu-id="8e3ef-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="8e3ef-104">Para deshacer un registro erróneo del diario, seleccione un movimiento y cree un movimiento de reversión (movimientos idénticos al original, pero con el signo contrario en el campo de importe) con el mismo número de documento y la misma fecha de registro que el movimiento original.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="8e3ef-105">Después de revertir un movimiento, debe registrar el movimiento correcto.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="8e3ef-106">Solo se pueden revertir los movimientos que están registrados desde una línea del diario general.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="8e3ef-107">Un movimiento solo se puede revertir una vez.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="8e3ef-108">Para obtener más información sobre el registro desde un diario general, vea [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ef-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="8e3ef-109">Se pueden revertir movimientos desde todas las ventanas **Movimientos**.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="8e3ef-110">El siguiente procedimiento se basa en la ventana **Movs. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="8e3ef-111">Para revertir el registro de diario de un movimiento de contabilidad</span><span class="sxs-lookup"><span data-stu-id="8e3ef-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="8e3ef-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movs. contabilidad** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="8e3ef-113">Seleccione el movimiento que desea revertir y, después, seleccione **Revertir transacción**.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="8e3ef-114">Tenga en cuenta que debe proceder de un registro de diario.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="8e3ef-115">En la ventana **Revertir movs. trans.**, seleccione el movimiento relevante y, después, seleccione la acción **Revertir**.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="8e3ef-116">Elija el botón **Sí** para en el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="8e3ef-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e3ef-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8e3ef-117">See Also</span></span>
[<span data-ttu-id="8e3ef-118">Registrar transacciones directamente en la contabilidad</span><span class="sxs-lookup"><span data-stu-id="8e3ef-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="8e3ef-119">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="8e3ef-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="8e3ef-120">Finanzas</span><span class="sxs-lookup"><span data-stu-id="8e3ef-120">Finance</span></span>](finance.md)  
<span data-ttu-id="8e3ef-121">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e3ef-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

