---
title: Administrar cuentas bancarias | Documentos de Microsoft
description: Debe reconciliar regularmente los movimientos de banco con las transacciones bancarias relacionadas en sus cuentas bancarias.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 25e1242541e98cc47e2fcc4f016a860ad08c635d
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/16/2019
ms.locfileid: "939134"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="72ed5-103">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="72ed5-103">Managing Bank Accounts</span></span>
<span data-ttu-id="72ed5-104">A intervalos regulares, debe conciliar sus movimientos bancarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] con las transacciones bancarias relacionadas a cuentas bancarias en su banco y, a continuación, registrar el saldo en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="72ed5-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="72ed5-105">Puede realizar esta tarea, ya sea como parte del procesamiento de los pagos representados en un extracto bancario en el **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="72ed5-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="72ed5-106">Alternativamente, puede realizar la tarea por separado del proceso de pagos, en la página **Conciliación banco** donde coincide (reconcilia) líneas de extracto bancario en el panel izquierdo con los movimientos de cuenta bancaria internos en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="72ed5-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="72ed5-107">En ambas páginas, puede completar la información del extracto de cuenta mediante la importación de un archivo o de una fuente y puede usar sugerencias de coincidencia automática.</span><span class="sxs-lookup"><span data-stu-id="72ed5-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="72ed5-108">En las versiones de EE. UU., también puede realizar las conciliaciones bancarias en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario.</span><span class="sxs-lookup"><span data-stu-id="72ed5-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="72ed5-109">Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="72ed5-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="72ed5-110">Para obtener más información, consulte la sección "Conciliar cuentas bancarias" en Funcionalidad local para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="72ed5-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="72ed5-111">A veces, debe transferir importes entre la cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] para reflejar las transferencias en su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="72ed5-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="72ed5-112">Puede realizar esta tarea en la página **Diario general**, de diferentes maneras en función de la divisa de los fondos.</span><span class="sxs-lookup"><span data-stu-id="72ed5-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="72ed5-113">Para poder gestionar las cuentas bancarias, debe configurar cada cuenta bancaria como una ficha de banco.</span><span class="sxs-lookup"><span data-stu-id="72ed5-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="72ed5-114">Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos.</span><span class="sxs-lookup"><span data-stu-id="72ed5-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="72ed5-115">Para obtener más información, consulte [Configurar cuentas bancarias](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="72ed5-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="72ed5-116">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="72ed5-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="72ed5-117">Para</span><span class="sxs-lookup"><span data-stu-id="72ed5-117">To</span></span> | <span data-ttu-id="72ed5-118">Vea</span><span class="sxs-lookup"><span data-stu-id="72ed5-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="72ed5-119">Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la página **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="72ed5-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="72ed5-120">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="72ed5-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="72ed5-121">Concilie cuentas bancarias, incluidos los movimientos de cheque, como una tarea independiente en la página **Conciliación de cuentas bancarias**.</span><span class="sxs-lookup"><span data-stu-id="72ed5-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="72ed5-122">Conciliar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="72ed5-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="72ed5-123">Registre transferencias entre bancos en la misma divisa o en divisas diferentes.</span><span class="sxs-lookup"><span data-stu-id="72ed5-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="72ed5-124">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="72ed5-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="72ed5-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="72ed5-125">See Also</span></span>
[<span data-ttu-id="72ed5-126">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="72ed5-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="72ed5-127">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="72ed5-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="72ed5-128">[Administrar pagos](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="72ed5-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="72ed5-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72ed5-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="72ed5-130">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="72ed5-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
