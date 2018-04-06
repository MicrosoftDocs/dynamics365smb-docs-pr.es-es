---
title: Administrar cuentas bancarias | Documentos de Microsoft
description: Debe reconciliar regularmente los movimientos de banco en Financials con las transacciones bancarias relacionadas en sus cuentas bancarias.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 20ff1bad076bff8ce07716cfffc2fa5e05605bb2
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="800b9-103">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="800b9-103">Managing Bank Accounts</span></span>
<span data-ttu-id="800b9-104">A intervalos regulares, debe conciliar sus movimientos bancarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] con las transacciones bancarias relacionadas a cuentas bancarias en su banco y, a continuación, registrar el saldo en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="800b9-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="800b9-105">Puede realizar esta tarea, ya sea como parte del procesamiento de los pagos representados en un extracto bancario en el **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="800b9-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="800b9-106">O, de forma alternativa, puede realizar la tarea por separado del procesamiento de los pagos, en la ventana **Conciliación de cuentas bancarias** que admite movimientos de cheque.</span><span class="sxs-lookup"><span data-stu-id="800b9-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="800b9-107">En ambos casos, puede rellenar las ventanas importando el extracto bancario a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="800b9-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="800b9-108">A veces, debe transferir importes entre la cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] para reflejar las transferencias en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="800b9-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="800b9-109">Puede realizar esta tarea en la ventana **Diario general**, de diferentes maneras en función de la divisa de los fondos.</span><span class="sxs-lookup"><span data-stu-id="800b9-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="800b9-110">Para poder gestionar las cuentas bancarias, debe configurar cada cuenta bancaria como una ficha de banco.</span><span class="sxs-lookup"><span data-stu-id="800b9-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="800b9-111">Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos.</span><span class="sxs-lookup"><span data-stu-id="800b9-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="800b9-112">Para obtener más información, consulte [Configurar cuentas bancarias](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="800b9-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="800b9-113">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="800b9-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="800b9-114">Para</span><span class="sxs-lookup"><span data-stu-id="800b9-114">To</span></span> | <span data-ttu-id="800b9-115">Vea</span><span class="sxs-lookup"><span data-stu-id="800b9-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="800b9-116">Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la ventana **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="800b9-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="800b9-117">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="800b9-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="800b9-118">Concilie cuentas bancarias, incluidos los movimientos de cheque, como una tarea independiente en la ventana **Conciliación de cuentas bancarias**.</span><span class="sxs-lookup"><span data-stu-id="800b9-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="800b9-119">Conciliar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="800b9-119">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="800b9-120">Registre transferencias entre bancos en la misma divisa o en divisas diferentes.</span><span class="sxs-lookup"><span data-stu-id="800b9-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="800b9-121">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="800b9-121">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="800b9-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="800b9-122">See Also</span></span>
[<span data-ttu-id="800b9-123">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="800b9-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="800b9-124">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="800b9-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="800b9-125">[Administrar pagos](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="800b9-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="800b9-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="800b9-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="800b9-127">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="800b9-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

