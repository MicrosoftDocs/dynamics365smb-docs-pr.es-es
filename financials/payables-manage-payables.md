---
title: Resumen de tareas para administrar las cuentas por pagar | Documentos de Microsoft
description: "Describe las tareas para administrar los pagos, por ejemplo, los pagos a acreedores o la liquidación de pagos salientes en movimientos para cerrar facturas o abonos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 4a529d426fbc8da5aab75d308434ba58e5800186
ms.contentlocale: es-es
ms.lasthandoff: 04/16/2018

---
# <a name="managing-payables"></a><span data-ttu-id="6495d-103">Administración de pagos</span><span class="sxs-lookup"><span data-stu-id="6495d-103">Managing Payables</span></span>
<span data-ttu-id="6495d-104">Una gran parte de la gestión de cuentas por pagar es pagar a sus proveedores, o reembolsar los gastos a sus empleados.</span><span class="sxs-lookup"><span data-stu-id="6495d-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="6495d-105">Puede usar funciones para agregar líneas de pagos de facturas de compra pendientes en la ventana **Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="6495d-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="6495d-106">Para enviar transacciones a su banco, puede exportar varias líneas de diario de pagos a un archivo y, a continuación, cargar el archivo a su banco.</span><span class="sxs-lookup"><span data-stu-id="6495d-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="6495d-107">También puede efectuar pagos por cheque, incluida la transmisión de cheques como pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="6495d-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="6495d-108">Otra tarea típica es liquidar pagos salientes a sus movimientos de proveedor o empleado relacionados para cerrar las facturas de compra o los abonos de compra o las cuentas de empleado como pagados.</span><span class="sxs-lookup"><span data-stu-id="6495d-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="6495d-109">Puede realizar esta acción en la ventana **Diario de conciliación de pagos** importando un archivo de extracto bancario para registrar los pagos.</span><span class="sxs-lookup"><span data-stu-id="6495d-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="6495d-110">Los pagos se liquidan en los movimientos de proveedor, cliente o empleado pendiente mediante coincidencias entre el texto de pago y la información de movimiento.</span><span class="sxs-lookup"><span data-stu-id="6495d-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="6495d-111">Existen varias formas de revisar y modificar las coincidencias antes de registrar el diario.</span><span class="sxs-lookup"><span data-stu-id="6495d-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="6495d-112">Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario.</span><span class="sxs-lookup"><span data-stu-id="6495d-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="6495d-113">La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.</span><span class="sxs-lookup"><span data-stu-id="6495d-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="6495d-114">De forma alternativa, puede liquidar los pagos salientes manualmente en la ventana **Diario de pagos** o desde los movimientos de proveedor o empleado relacionados.</span><span class="sxs-lookup"><span data-stu-id="6495d-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="6495d-115">En la tabla siguiente se muestra una secuencia de tareas de cuentas por pagar, con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="6495d-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="6495d-116">Para</span><span class="sxs-lookup"><span data-stu-id="6495d-116">To</span></span> | <span data-ttu-id="6495d-117">Vea</span><span class="sxs-lookup"><span data-stu-id="6495d-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="6495d-118">Generar pagos de proveedores o reembolsos a empleados, preparar pagos con cheques y exportar pagos a un archivo bancario al registrarlos.</span><span class="sxs-lookup"><span data-stu-id="6495d-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="6495d-119">Creación de pagos</span><span class="sxs-lookup"><span data-stu-id="6495d-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="6495d-120">Liquide pagos de proveedores automáticamente con facturas de compra sin abonar importando un archivo de extracto bancario.</span><span class="sxs-lookup"><span data-stu-id="6495d-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="6495d-121">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="6495d-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="6495d-122">Liquide pagos de proveedor con facturas de compra sin abonar manualmente.</span><span class="sxs-lookup"><span data-stu-id="6495d-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="6495d-123">Conciliar pagos de proveedor manualmente</span><span class="sxs-lookup"><span data-stu-id="6495d-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="6495d-124">Asegúrese de la valoración de inventario correcta mediante la asignación de costes de producto, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar.</span><span class="sxs-lookup"><span data-stu-id="6495d-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="6495d-125">Usar los cargos de producto a cuenta para los costes comerciales adicionales</span><span class="sxs-lookup"><span data-stu-id="6495d-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="6495d-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6495d-126">See Also</span></span>
[<span data-ttu-id="6495d-127">Compras</span><span class="sxs-lookup"><span data-stu-id="6495d-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="6495d-128">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="6495d-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="6495d-129">Usar los cargos de producto a cuenta para los costes comerciales adicionales</span><span class="sxs-lookup"><span data-stu-id="6495d-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="6495d-130">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="6495d-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="6495d-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6495d-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]

