---
title: Registrar gastos o ingresos directamente en contabilidad | Documentos de Microsoft
description: Para las actividades empresariales que no está representadas por un documento, como los gastos o recibos de efectivo más pequeños, puede crear las transacciones relacionadas registrando líneas de diario en la página Diario general.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1603ad8a107e4d879a3a17605f35b23b9db526cd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778948"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="1c5b4-103">Registrar transacciones directamente en la contabilidad</span><span class="sxs-lookup"><span data-stu-id="1c5b4-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="1c5b4-104">Puede usar diarios generales para registrar transacciones financieras directamente en cuentas generales y otras cuentas, como cuentas bancarias, de cliente, proveedor y empleado.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="1c5b4-105">El diario general normalmente se utiliza para publicar los gastos propios de los empleados durante actividades comerciales, para su posterior reembolso.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="1c5b4-106">Para obtener más información, consulte [Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="1c5b4-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="1c5b4-107">Los diarios generales registran las transacciones financieras directamente en cuentas contables y otras cuentas, como bancarias, de clientes, de proveedores y de empleados.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="1c5b4-108">Registrar con un diario general siempre crea movimientos en cuentas contables.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="1c5b4-109">Esto es así incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="1c5b4-110">Puede personalizar la versión de un diario general configurando una sección o una plantilla de diario.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="1c5b4-111">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="1c5b4-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="1c5b4-112">A diferencia de los movimientos que se registran en documentos, que requieren un proceso de abono, puede revertir correctamente los movimientos que se registran con el diario general.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="1c5b4-113">Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="1c5b4-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="1c5b4-114">Para registrar una transacción directamente en una cuenta contable</span><span class="sxs-lookup"><span data-stu-id="1c5b4-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="1c5b4-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diarios generales** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c5b4-116">Abra la sección del diario general correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="1c5b4-117">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="1c5b4-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="1c5b4-118">En una línea nueva de diario, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="1c5b4-119">Repita el paso 3 para todas las transacciones independientes que desee registrar.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="1c5b4-120">Si desea introducir varias líneas de transacción sobre una línea de cuenta de contrapartida, por ejemplo, de una cuenta bancaria, seleccione la casilla de verificación **Sugerir importe de compensación** en la línea de la sección en la página **Secciones diario general**.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="1c5b4-121">El campo **Importe** de la línea de la cuenta de contrapartida se rellena previamente de forma automática con el valor que se requiere para compensar las transacciones.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="1c5b4-122">Seleccione la acción **Registrar** para registrar las transacciones en las cuentas contables especificadas.</span><span class="sxs-lookup"><span data-stu-id="1c5b4-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c5b4-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c5b4-123">See Also</span></span>

[<span data-ttu-id="1c5b4-124">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="1c5b4-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1c5b4-125">Registro y reembolso de los costes de los empleados</span><span class="sxs-lookup"><span data-stu-id="1c5b4-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="1c5b4-126">Revertir los registros de diario y deshacer los recibos/envíos</span><span class="sxs-lookup"><span data-stu-id="1c5b4-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="1c5b4-127">Finanzas</span><span class="sxs-lookup"><span data-stu-id="1c5b4-127">Finance</span></span>](finance.md)  
<span data-ttu-id="1c5b4-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c5b4-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
