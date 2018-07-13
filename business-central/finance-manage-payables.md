---
title: Administrar cuentas por pagar | Documentos de Microsoft
description: "Resumen de cómo administra las cuentas por pagar (AP), incluidos los pagos de proveedor, acreedores, deuda y saldo vencido."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 1682db5bd62f980e8789613cd2ca4169f98e839d
ms.contentlocale: es-es
ms.lasthandoff: 06/01/2018

---
# <a name="managing-payables"></a><span data-ttu-id="9dd07-103">Administración de pagos</span><span class="sxs-lookup"><span data-stu-id="9dd07-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9dd07-104"> tiene lo que necesita para administrar eficazmente las cuentas de pagos.</span><span class="sxs-lookup"><span data-stu-id="9dd07-104"> has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="9dd07-105">Pagos</span><span class="sxs-lookup"><span data-stu-id="9dd07-105">Payments</span></span>
<span data-ttu-id="9dd07-106">Resulta fácil asignar prioridades a los pagos, tener en cuenta las penalizaciones por pagos atrasados y controlar por pronto pago.</span><span class="sxs-lookup"><span data-stu-id="9dd07-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="9dd07-107">Puede registrar pagos en un diario general e imprimir cheques antes de que se registre el diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="9dd07-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="9dd07-108">Puede liquidar pagos para cerrar facturas cuando registre el pago o después de registrar el pago.</span><span class="sxs-lookup"><span data-stu-id="9dd07-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="9dd07-109">El **Método liquidación** especificado para el proveedor (en la **Ficha del proveedor**) determina si debe liquidar el pago manual o automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9dd07-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="9dd07-110">Siempre puede liquidar las transacciones manualmente.</span><span class="sxs-lookup"><span data-stu-id="9dd07-110">You can always apply transactions manually.</span></span> <span data-ttu-id="9dd07-111">Sin embargo, si el método de liquidación para el proveedor es **Por antigüedad** y no especifica un documento que liquide el pago, este liquida el movimiento abierto más antiguo para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9dd07-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="9dd07-112">Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="9dd07-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9dd07-113"> puede sugerir distintos pagos a proveedores, como pagos que vencerán pronto o pagos en donde hay un descuento disponible.</span><span class="sxs-lookup"><span data-stu-id="9dd07-113"> can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="9dd07-114">La propuesta de pago puede considerar un importe que se especifique como fondos disponibles para el pago y si se pueden aplicar descuentos por pronto pago.</span><span class="sxs-lookup"><span data-stu-id="9dd07-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="9dd07-115">Problemas con los cheques</span><span class="sxs-lookup"><span data-stu-id="9dd07-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9dd07-116"> le permite emitir los cheques a los proveedores manual y electrónicamente.</span><span class="sxs-lookup"><span data-stu-id="9dd07-116"> lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="9dd07-117">Ambos se realizan en la ventana **Diarios de pagos**, donde también puede anular cheques y ver movimientos de cheque.</span><span class="sxs-lookup"><span data-stu-id="9dd07-117">You do both in the **Payment Journals** window, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="9dd07-118">Exportar pagos a un archivo bancario</span><span class="sxs-lookup"><span data-stu-id="9dd07-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="9dd07-119">Cuando esté listo para pagar a un proveedor desde la ventana **Diario de pagos**, puede exportar un archivo con la información de pago de las líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="9dd07-119">When you are ready to pay a vendor, from the **Payment Journal** window you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="9dd07-120">Después, puede cargar el archivo al banco electrónico para procesar las transferencias de dinero.</span><span class="sxs-lookup"><span data-stu-id="9dd07-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="9dd07-121">Si no desea registrar una línea de diario de pagos para un pago exportado, por ejemplo porque se está esperando que el banco confirme la transacción, puede eliminar solo la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="9dd07-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="9dd07-122">Posteriormente, cuando cree una línea de diario de pagos para pagar el importe pendiente en la factura, el campo **Importe total exportado** muestra qué parte del importe del pago se ha exportado ya.</span><span class="sxs-lookup"><span data-stu-id="9dd07-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="9dd07-123">También puede encontrar información detallada acerca del total exportado seleccionando el botón **Movimientos de reg. de transferencia de crédito**.</span><span class="sxs-lookup"><span data-stu-id="9dd07-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="9dd07-124">Si espera a registrar los pagos hasta que el banco confirme que ha procesado las transacciones, hay dos formas de evitar la reexportación accidental de pagos de los documentos pendientes:</span><span class="sxs-lookup"><span data-stu-id="9dd07-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="9dd07-125">En un diario de pagos con líneas de pago propuestas, puede ordenar tanto **Exportado a archivo de pagos** o **Importe total exportado** y después eliminar las propuestas de pago de las facturas pendientes para las que ya se han realizado los pagos y no desea realizar ninguno más.</span><span class="sxs-lookup"><span data-stu-id="9dd07-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="9dd07-126">**Nota** Es posible que tenga que agregar dichas columnas a la lista.</span><span class="sxs-lookup"><span data-stu-id="9dd07-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="9dd07-127">Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="9dd07-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="9dd07-128">En el proceso **Proponer pagos a proveedores**, donde se pueden especificar los pagos que se incluirán en el diario de pagos, también puede especificar que no se inserten las líneas de diario para pagos que ya se hayan exportado eligiendo la casilla **Omitir pagos exportados**.</span><span class="sxs-lookup"><span data-stu-id="9dd07-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dd07-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9dd07-129">See Also</span></span>
[<span data-ttu-id="9dd07-130">Formas de pago</span><span class="sxs-lookup"><span data-stu-id="9dd07-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="9dd07-131">Finanzas</span><span class="sxs-lookup"><span data-stu-id="9dd07-131">Finance</span></span>](finance.md)  
<span data-ttu-id="9dd07-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9dd07-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

