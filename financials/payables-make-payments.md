---
title: Resumen de tareas para administrar los pagos a proveedores | Documentos de Microsoft
description: "Describe las tareas para administrar los pagos a proveedores o acreedores, incluido el registro de líneas de pago, y obtener un resumen de saldo vencido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="44018-103">Hacer los pagos</span><span class="sxs-lookup"><span data-stu-id="44018-103">Make Payments</span></span>
<span data-ttu-id="44018-104">Cuando efectúa pagos a proveedores, registra las líneas de pago relacionadas en la ventana **Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="44018-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="44018-105">Puede usar la función **Proponer pagos a proveedores** para buscar los pagos vencidos.</span><span class="sxs-lookup"><span data-stu-id="44018-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="44018-106">También puede usar el informe **Proveedor - Pagos por periodos** para obtener una visión general de los pagos vencidos.</span><span class="sxs-lookup"><span data-stu-id="44018-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="44018-107">Desde el diario de pagos, puede imprimir cheques automáticos o registrar cuándo se escriben los cheques.</span><span class="sxs-lookup"><span data-stu-id="44018-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="44018-108">Si selecciona **Cheque automático** en el campo **Tipo pago por banco**, las líneas que representan cheques se deben imprimir antes de que se pueda registrar el diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="44018-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="44018-109">Cuando se registran los pagos, puede exportarlos a un archivo de banco que se cargará al sitio de banco electrónico para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="44018-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="44018-110">Cuando se hayan efectuado los pagos en su banco, debe liquidarlos a sus movimientos de proveedor abiertos relacionados.</span><span class="sxs-lookup"><span data-stu-id="44018-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="44018-111">Puede hacerlo manualmente o importando un archivo de extracto bancario y liquidando los pagos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="44018-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="44018-112">Para obtener más información, vea [Liquidar pagos automáticamente y conciliar cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="44018-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="44018-113">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="44018-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="44018-114">Para</span><span class="sxs-lookup"><span data-stu-id="44018-114">To</span></span> | <span data-ttu-id="44018-115">Vea</span><span class="sxs-lookup"><span data-stu-id="44018-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="44018-116">Use una función para sugerir pagos de proveedores según los criterios seleccionados, como la fecha de vencimiento, la posibilidad de aplicar descuentos o su liquidez.</span><span class="sxs-lookup"><span data-stu-id="44018-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="44018-117">Propuesta de pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="44018-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="44018-118">Emita cheques para realizar pagos, ya sea como copias impresas o como cheques automáticos.</span><span class="sxs-lookup"><span data-stu-id="44018-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="44018-119">Anule los cheques antes o después del registro.</span><span class="sxs-lookup"><span data-stu-id="44018-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="44018-120">Trabajar con cheques</span><span class="sxs-lookup"><span data-stu-id="44018-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="44018-121">Asegúrese de que su banco solo compensa cheques e importes validados enviándoles un archivo que contenga la información de proveedor, cheque y pago.</span><span class="sxs-lookup"><span data-stu-id="44018-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="44018-122">Exportar un archivo de Positive Pay</span><span class="sxs-lookup"><span data-stu-id="44018-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="44018-123">Exporte los pagos desde la ventana **Diario de pagos** a un archivo de banco que envíe a su banco para su procesamiento, incluido EFT (transferencia electrónica de fondos) en Norteamérica.</span><span class="sxs-lookup"><span data-stu-id="44018-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="44018-124">Exportación de pagos a un archivo de banco</span><span class="sxs-lookup"><span data-stu-id="44018-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="44018-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="44018-125">See Also</span></span>
[<span data-ttu-id="44018-126">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="44018-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="44018-127">Compras</span><span class="sxs-lookup"><span data-stu-id="44018-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="44018-128">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="44018-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="44018-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44018-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

