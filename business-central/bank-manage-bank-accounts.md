---
title: Administrar cuentas bancarias | Documentos de Microsoft
description: Debe reconciliar regularmente los movimientos de banco en Financials con las transacciones bancarias relacionadas en sus cuentas bancarias.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: dd3068cc1af6a16a43f982d3b48cdec42a7d7eca
ms.contentlocale: es-es
ms.lasthandoff: 05/17/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="690d9-103">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="690d9-103">Managing Bank Accounts</span></span>
<span data-ttu-id="690d9-104">A intervalos regulares, debe conciliar sus movimientos bancarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] con las transacciones bancarias relacionadas a cuentas bancarias en su banco y, a continuación, registrar el saldo en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="690d9-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="690d9-105">Puede realizar esta tarea, ya sea como parte del procesamiento de los pagos representados en un extracto bancario en el **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="690d9-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="690d9-106">Alternativamente, puede realizar la tarea por separado del proceso de pagos, en la ventana **Conciliación banco** donde coincide (reconcilia) líneas de extracto bancario en el panel izquierdo con los movimientos de cuenta bancaria internos en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="690d9-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="690d9-107">En ambas ventanas, puede completar la información del extracto de cuenta mediante la importación de un archivo o de una fuente y puede usar sugerencias de coincidencia automática.</span><span class="sxs-lookup"><span data-stu-id="690d9-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="690d9-108">En las versiones de EE. UU., también puede realizar las conciliaciones bancarias en **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario.</span><span class="sxs-lookup"><span data-stu-id="690d9-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="690d9-109">Para usar esta ventana en lugar de la **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la ventana **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="690d9-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="690d9-110">Para obtener más información, consulte la sección "Conciliar cuentas bancarias" en Funcionalidad local para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="690d9-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="690d9-111">A veces, debe transferir importes entre la cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] para reflejar las transferencias en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="690d9-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="690d9-112">Puede realizar esta tarea en la ventana **Diario general**, de diferentes maneras en función de la divisa de los fondos.</span><span class="sxs-lookup"><span data-stu-id="690d9-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="690d9-113">Para poder gestionar las cuentas bancarias, debe configurar cada cuenta bancaria como una ficha de banco.</span><span class="sxs-lookup"><span data-stu-id="690d9-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="690d9-114">Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos.</span><span class="sxs-lookup"><span data-stu-id="690d9-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="690d9-115">Para obtener más información, consulte [Configurar cuentas bancarias](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="690d9-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="690d9-116">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="690d9-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="690d9-117">Para</span><span class="sxs-lookup"><span data-stu-id="690d9-117">To</span></span> | <span data-ttu-id="690d9-118">Vea</span><span class="sxs-lookup"><span data-stu-id="690d9-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="690d9-119">Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la ventana **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="690d9-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="690d9-120">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="690d9-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="690d9-121">Concilie cuentas bancarias, incluidos los movimientos de cheque, como una tarea independiente en la ventana **Conciliación de cuentas bancarias**.</span><span class="sxs-lookup"><span data-stu-id="690d9-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="690d9-122">Conciliar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="690d9-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="690d9-123">Registre transferencias entre bancos en la misma divisa o en divisas diferentes.</span><span class="sxs-lookup"><span data-stu-id="690d9-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="690d9-124">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="690d9-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="690d9-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="690d9-125">See Also</span></span>
[<span data-ttu-id="690d9-126">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="690d9-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="690d9-127">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="690d9-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="690d9-128">[Administrar pagos](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="690d9-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="690d9-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="690d9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="690d9-130">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="690d9-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

