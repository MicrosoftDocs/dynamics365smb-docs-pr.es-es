---
title: Administrar cuentas bancarias | Documentos de Microsoft
description: Debe reconciliar regularmente los movimientos de banco con las transacciones bancarias relacionadas en sus cuentas bancarias.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c36e906c87cb17acb85d8cde32fdc51ee501469d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381736"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="22b03-103">Conciliar bancos</span><span class="sxs-lookup"><span data-stu-id="22b03-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="22b03-104">Se debe completar una conciliación de banco a intervalos regulares para todos sus bancos para garantizar que los registros de caja de la empresa sean correctos.</span><span class="sxs-lookup"><span data-stu-id="22b03-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="22b03-105">Para ello, compare y haga corresponder los movimientos en sus bancos internos con las transacciones bancarias en su banco, y luego registre los saldos en sus bancos internos para que los totales estén disponibles para los directores financieros.</span><span class="sxs-lookup"><span data-stu-id="22b03-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="22b03-106">La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="22b03-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="22b03-107">Puede realizar la tarea por separado del proceso de pagos, en la página **Conciliación banco** donde hace corresponder (concilia) líneas del extracto de cuenta en el panel izquierdo con los movimientos de banco interno en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="22b03-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="22b03-108">Alternativamente, puede realizar esta tarea en la página **Diario de conciliación de pagos** como parte del procesamiento de pagos que están representados en un extracto de cuenta.</span><span class="sxs-lookup"><span data-stu-id="22b03-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="22b03-109">En ambas páginas, puede completar la información del extracto de cuenta mediante la importación de un archivo o de una fuente y puede usar sugerencias de coincidencia automática.</span><span class="sxs-lookup"><span data-stu-id="22b03-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="22b03-110">En las versiones de EE. UU., también puede realizar las conciliaciones bancarias en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario.</span><span class="sxs-lookup"><span data-stu-id="22b03-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="22b03-111">Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="22b03-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="22b03-112">Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="22b03-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="22b03-113">Para poder gestionar sus bancos en [!INCLUDE[prod_short](includes/prod_short.md)], debe configurar cada banco como una ficha de banco.</span><span class="sxs-lookup"><span data-stu-id="22b03-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="22b03-114">Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos.</span><span class="sxs-lookup"><span data-stu-id="22b03-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="22b03-115">Para obtener más información, consulte [Configurar bancos](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="22b03-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="22b03-116">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="22b03-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="22b03-117">Para</span><span class="sxs-lookup"><span data-stu-id="22b03-117">To</span></span> | <span data-ttu-id="22b03-118">Vea</span><span class="sxs-lookup"><span data-stu-id="22b03-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="22b03-119">Concilie los bancos como una tarea independiente en la página **Conciliación banco**.</span><span class="sxs-lookup"><span data-stu-id="22b03-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="22b03-120">Conciliar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="22b03-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="22b03-121">Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la página **Diario de conciliación de pagos**.</span><span class="sxs-lookup"><span data-stu-id="22b03-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="22b03-122">Liquidación de pagos automáticamente y conciliación de bancos</span><span class="sxs-lookup"><span data-stu-id="22b03-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="22b03-123">Use la conciliación bancaria para ayudar a comprobar que sus libros estén actualizados y no publique la conciliación hasta que esté satisfecho con la conciliación.</span><span class="sxs-lookup"><span data-stu-id="22b03-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="22b03-124">Consulte Formación relacionada en [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="22b03-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="22b03-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22b03-125">See Also</span></span>

[<span data-ttu-id="22b03-126">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="22b03-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="22b03-127">Conciliar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="22b03-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="22b03-128">Liquidación de pagos automáticamente y conciliación de bancos</span><span class="sxs-lookup"><span data-stu-id="22b03-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="22b03-129">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="22b03-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="22b03-130">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="22b03-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="22b03-131">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="22b03-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="22b03-132">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22b03-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="22b03-133">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="22b03-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]