---
title: Pagos en efectivo
description: A partir del 1 de enero de 2012, las empresas en España están obligadas a presentar un resumen de los pagos en efectivo que superen los 6.000,00 EUR por cada cliente por cada año.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 06fa93cca6f2f5ad75b2204ffcae09d268c86367
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778114"
---
# <a name="payments-in-cash"></a><span data-ttu-id="5ed1f-103">Pagos en efectivo</span><span class="sxs-lookup"><span data-stu-id="5ed1f-103">Payments in Cash</span></span>
<span data-ttu-id="5ed1f-104">A partir del 1 de enero de 2012, las empresas en España están obligadas a presentar un resumen de los pagos en efectivo que superen los 6.000,00 EUR por cada cliente por cada año.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-104">As of January 1, 2012, companies in Spain are required to submit a summary for payments in cash that are greater than EUR 6.000.00 for each customer for each year.</span></span>  

## <a name="reporting-payments-in-cash"></a><span data-ttu-id="5ed1f-105">Realizar pagos en efectivo</span><span class="sxs-lookup"><span data-stu-id="5ed1f-105">Reporting Payments in Cash</span></span>  
<span data-ttu-id="5ed1f-106">Si está realizando pagos en efectivo, la siguiente secuencia de tareas enumera el orden en que generalmente se realizan:</span><span class="sxs-lookup"><span data-stu-id="5ed1f-106">If you are reporting payments in cash, the following sequence of tasks are listed in the order in which they are generally performed:</span></span>  

- <span data-ttu-id="5ed1f-107">Liquidación de pagos en efectivo a las facturas.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-107">Applying payments in cash to invoices.</span></span>  
- <span data-ttu-id="5ed1f-108">Creación de pagos 340 en declaración de efectivo.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-108">Making 340 Payments in cash declaration.</span></span>  

## <a name="applying-payments-in-cash-to-invoices"></a><span data-ttu-id="5ed1f-109">Liquidación de pagos en efectivo a las facturas</span><span class="sxs-lookup"><span data-stu-id="5ed1f-109">Applying Payments in Cash to Invoices</span></span>  
<span data-ttu-id="5ed1f-110">Liquide los pagos en efectivo a las facturas que ha recibido de clientes.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-110">You apply payments in cash to invoices that you have received from customers.</span></span> <span data-ttu-id="5ed1f-111">Para obtener información acerca de cómo liquidar pagos en facturas, vea [Administrar cobros](../../receivables-manage-receivables.md).</span><span class="sxs-lookup"><span data-stu-id="5ed1f-111">For information about how to apply payments to invoices, see [Managing Receivables](../../receivables-manage-receivables.md).</span></span> <span data-ttu-id="5ed1f-112">Solo los pagos liquidados en efectivo se utilizan para realizar pagos en efectivo.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-112">Only the applied payments in cash are used for reporting payments in cash.</span></span> <span data-ttu-id="5ed1f-113">Si no liquida los pagos en efectivo a las facturas, no puede indicar pagos en efectivo.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-113">If you do not apply payments in cash to invoices, you cannot report payments in cash.</span></span>  

## <a name="making-340-payments-in-cash-declaration"></a><span data-ttu-id="5ed1f-114">Creación de pagos 340 en declaración de efectivo</span><span class="sxs-lookup"><span data-stu-id="5ed1f-114">Making 340 Payments in Cash Declaration</span></span>  
<span data-ttu-id="5ed1f-115">Utilice el proceso **Modelo 340** para informar realizar pagos 340 en la declaración de efectivo.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-115">You use the **Make 340 Declaration** batch job to report 340 payments in cash declaration.</span></span> <span data-ttu-id="5ed1f-116">Para obtener información acerca de cómo especificar y seleccionar la información para generar la declaración, consulte Modelo 340.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-116">For information about how to specify and select information to generate the declaration, see Make 340 Declaration.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5ed1f-117">Los pagos creados a través de los bancos se excluyen.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-117">The payments made through banks are excluded.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5ed1f-118">El importe recibido en efectivo en el archivo .txt del modelo puede contener valores distintos al importe total facturado para un cliente.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-118">The amount received in cash in the declaration .txt file can contain values that differ from the total invoiced amount for a customer.</span></span> <span data-ttu-id="5ed1f-119">Esto se debe a que no todos los pagos se realizan en efectivo.</span><span class="sxs-lookup"><span data-stu-id="5ed1f-119">This is because not all of the payments are made in cash.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5ed1f-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ed1f-120">See Also</span></span>  
<span data-ttu-id="5ed1f-121">[Administrar cobros](../../receivables-manage-receivables.md)   </span><span class="sxs-lookup"><span data-stu-id="5ed1f-121">[Managing Receivables](../../receivables-manage-receivables.md)   </span></span>  
 [<span data-ttu-id="5ed1f-122">Informe 340</span><span class="sxs-lookup"><span data-stu-id="5ed1f-122">Report 340</span></span>](report-340.md)
