---
title: Registrar gastos o ingresos directamente en contabilidad | Documentos de Microsoft
description: "Para las actividades empresariales que no está representadas por un documento, como los gastos o recibos de efectivo más pequeños, puede crear las transacciones relacionadas registrando líneas de diario en la ventana Diario general."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="e52c4-103">Registrar transacciones directamente en la contabilidad</span><span class="sxs-lookup"><span data-stu-id="e52c4-103">How to: Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="e52c4-104">La mayoría de las transacciones financieras se registran en la contabilidad a través de documentos empresariales dedicados, como facturas de compra y pedidos de ventas.</span><span class="sxs-lookup"><span data-stu-id="e52c4-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="e52c4-105">Para las actividades empresariales que no está representadas por un documento en [!INCLUDE[d365fin](includes/d365fin_md.md)], como los gastos o recibos de efectivo más pequeños, puede crear las transacciones relacionadas registrando líneas de diario en la ventana **Diario general**.</span><span class="sxs-lookup"><span data-stu-id="e52c4-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="e52c4-106">Los diarios generales registran las transacciones financieras directamente en cuentas contables y otras cuentas, como bancarias, de clientes y de proveedores.</span><span class="sxs-lookup"><span data-stu-id="e52c4-106">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, and vendor accounts.</span></span> <span data-ttu-id="e52c4-107">Registrar con un diario general siempre crea movimientos en cuentas contables.</span><span class="sxs-lookup"><span data-stu-id="e52c4-107">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="e52c4-108">Esto es así incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="e52c4-108">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="e52c4-109">Puede personalizar la versión de un diario general configurando una sección o una plantilla de diario.</span><span class="sxs-lookup"><span data-stu-id="e52c4-109">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="e52c4-110">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="e52c4-110">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="e52c4-111">A diferencia de los movimientos que se registran en documentos, que requieren un proceso de abono, puede revertir correctamente los movimientos que se registran con el diario general.</span><span class="sxs-lookup"><span data-stu-id="e52c4-111">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="e52c4-112">Para obtener más información, consulte [Revertir un registro de diario](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="e52c4-112">For more information, see [How to: Reverse Journal Posting](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="e52c4-113">Para registrar una transacción directamente en una cuenta contable</span><span class="sxs-lookup"><span data-stu-id="e52c4-113">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="e52c4-114">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios generales** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="e52c4-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e52c4-115">Abra la sección del diario general correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e52c4-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="e52c4-116">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="e52c4-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="e52c4-117">En una línea nueva de diario, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e52c4-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="e52c4-118">Repita el paso 3 para todas las transacciones independientes que desee registrar.</span><span class="sxs-lookup"><span data-stu-id="e52c4-118">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="e52c4-119">Si desea introducir varias líneas de transacción sobre una línea de cuenta de contrapartida, por ejemplo, de una cuenta bancaria, seleccione la casilla de verificación **Sugerir importe de compensación** en la línea de la sección en la ventana **Secciones diario general**.</span><span class="sxs-lookup"><span data-stu-id="e52c4-119">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="e52c4-120">El campo **Importe** de la línea de la cuenta de contrapartida se rellena previamente de forma automática con el valor que se requiere para compensar las transacciones.</span><span class="sxs-lookup"><span data-stu-id="e52c4-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="e52c4-121">Seleccione la acción **Registrar** para registrar las transacciones en las cuentas contables especificadas.</span><span class="sxs-lookup"><span data-stu-id="e52c4-121">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="e52c4-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e52c4-122">See Also</span></span>
[<span data-ttu-id="e52c4-123">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="e52c4-123">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="e52c4-124">Revertir un registro de diario</span><span class="sxs-lookup"><span data-stu-id="e52c4-124">How to: Reverse Journal Posting</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="e52c4-125">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e52c4-125">Finance</span></span>](finance.md)  
<span data-ttu-id="e52c4-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e52c4-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

