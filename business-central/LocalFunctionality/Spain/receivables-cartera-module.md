---
title: Módulo Docs. cartera a cobrar
description: El módulo Docs. cartera a cobrar permite administrar las facturas generadas a partir de facturas de ventas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cd59069487a3c3f2717b8dd28e66e58d1b9ad4b2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301085"
---
# <a name="receivables-cartera-module"></a><span data-ttu-id="2cc84-103">Módulo Docs. cartera a cobrar</span><span class="sxs-lookup"><span data-stu-id="2cc84-103">Receivables Cartera Module</span></span>
<span data-ttu-id="2cc84-104">El módulo Docs. cartera a cobrar permite administrar las facturas generadas a partir de facturas de ventas.</span><span class="sxs-lookup"><span data-stu-id="2cc84-104">The Receivables Cartera module allows you to manage bills generated from sales invoices.</span></span> <span data-ttu-id="2cc84-105">Los documentos se pueden administrar por:</span><span class="sxs-lookup"><span data-stu-id="2cc84-105">The documents can be managed by:</span></span>  

- <span data-ttu-id="2cc84-106">Fecha de vencimiento</span><span class="sxs-lookup"><span data-stu-id="2cc84-106">Due date</span></span>  
- <span data-ttu-id="2cc84-107">Banco</span><span class="sxs-lookup"><span data-stu-id="2cc84-107">Bank</span></span>  
- <span data-ttu-id="2cc84-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2cc84-108">Value</span></span>  
- <span data-ttu-id="2cc84-109">Tipo de documento</span><span class="sxs-lookup"><span data-stu-id="2cc84-109">Document type</span></span>  
- <span data-ttu-id="2cc84-110">Divisa</span><span class="sxs-lookup"><span data-stu-id="2cc84-110">Currency</span></span>  

<span data-ttu-id="2cc84-111">Mediante el **Diario Cartera** se pueden crear facturas manualmente.</span><span class="sxs-lookup"><span data-stu-id="2cc84-111">You can manually create bills using the **Cartera Journal**.</span></span> <span data-ttu-id="2cc84-112">También se puede utilizar el módulo Docs. cartera a cobrar para administrar todas las facturas de ventas que la empresa proporciona a una entidad de factoring.</span><span class="sxs-lookup"><span data-stu-id="2cc84-112">You can also use the Receivables Cartera module to manage all sales invoices that the company yields to a factoring company.</span></span>  

## <a name="bill-groups"></a><span data-ttu-id="2cc84-113">Remesas</span><span class="sxs-lookup"><span data-stu-id="2cc84-113">Bill Groups</span></span>  
<span data-ttu-id="2cc84-114">Mediante el módulo Docs. cartera a cobrar, se pueden administrar remesas y remesas de descuento en la divisa local u original.</span><span class="sxs-lookup"><span data-stu-id="2cc84-114">With the Receivables Cartera module, you can manage bill groups and discount bill groups in your local currency or original currency.</span></span>  

<span data-ttu-id="2cc84-115">Existen diferentes criterios para agrupar documentos en una remesa.</span><span class="sxs-lookup"><span data-stu-id="2cc84-115">There are various criteria for grouping documents in a bill group.</span></span> <span data-ttu-id="2cc84-116">Se pueden agrupar documentos girados para el mismo cliente, se pueden agrupar documentos que tengan la misma fecha de vencimiento, documentos girados en la misma plaza, etc.</span><span class="sxs-lookup"><span data-stu-id="2cc84-116">You can group documents for the same customer, documents with the same due date, documents drawn in the same market, and so on.</span></span> <span data-ttu-id="2cc84-117">Pueden agruparse en una remesa uno o más documentos a cobrar.</span><span class="sxs-lookup"><span data-stu-id="2cc84-117">You can group one or more receivable documents in one bill group.</span></span>  

<span data-ttu-id="2cc84-118">Una remesa se compone de uno o varios documentos que se agrupan para su entrega a un banco.</span><span class="sxs-lookup"><span data-stu-id="2cc84-118">A bill group consists of one or more documents grouped together to submit to a bank.</span></span> <span data-ttu-id="2cc84-119">Se puede enviar al cobro o descuento.</span><span class="sxs-lookup"><span data-stu-id="2cc84-119">A bill group can be submitted for collection or discount.</span></span>  

<span data-ttu-id="2cc84-120">Si se envían al cobro, el banco sólo es responsable de procesar el cobro de los documentos en la fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="2cc84-120">If submitted for collection, the bank is only responsible for processing the collection of the documents on the due date.</span></span>  

<span data-ttu-id="2cc84-121">Si la remesa se envía al descuento, el banco avanzará el importe de la remesa (o una parte de este, en el caso de factoring) a la empresa y será responsable de cobrar en las fechas de vencimiento de los documentos que forman la remesa.</span><span class="sxs-lookup"><span data-stu-id="2cc84-121">If the bill group is submitted for discount, the bank will advance the amount of the bill group (or a portion of it, in the case of factoring) to the company, and will take responsibility for collecting on the due dates of the documents that make up the bill group.</span></span>  

<span data-ttu-id="2cc84-122">Una remesa de facturas se puede enviar a una entidad de crédito (factor) para factoring con recurso (la empresa cubre el riesgo de insolvencia) o factoring sin recurso (el factor cubre el riesgo de insolvencia).</span><span class="sxs-lookup"><span data-stu-id="2cc84-122">A bill group of invoices can be submitted to a financial institution (factor) for risked factoring (the risk of insolvency is covered by the company) or unrisked factoring (the risk of insolvency is covered by the factor).</span></span>  

<span data-ttu-id="2cc84-123">Las remesas incluyen:</span><span class="sxs-lookup"><span data-stu-id="2cc84-123">Bill groups include:</span></span>  

- <span data-ttu-id="2cc84-124">Administración de intereses al cobro o descuento</span><span class="sxs-lookup"><span data-stu-id="2cc84-124">Finance charges for collection or discount management</span></span>  
- <span data-ttu-id="2cc84-125">Intereses de facturas devueltas</span><span class="sxs-lookup"><span data-stu-id="2cc84-125">Finance charges for returned bills</span></span>  
- <span data-ttu-id="2cc84-126">Interés al descuento</span><span class="sxs-lookup"><span data-stu-id="2cc84-126">Interest for discounts</span></span>  

<span data-ttu-id="2cc84-127">Con el módulo Docs. cartera a cobrar, se pueden proporcionar créditos o factoring de remesas de facturas de ventas, incluido el cálculo de intereses de la entidad de factoring.</span><span class="sxs-lookup"><span data-stu-id="2cc84-127">With the Receivables Cartera module, you can yield credits or factoring of sales invoice bill groups, including the finance charge calculation by the factoring company.</span></span> <span data-ttu-id="2cc84-128">Se puede solicitar el valor anticipado de las facturas proporcionadas o sólo la administración del cobro.</span><span class="sxs-lookup"><span data-stu-id="2cc84-128">You can request the anticipated value of the yielded invoices, or only the management of the collection.</span></span>  

<span data-ttu-id="2cc84-129">Se pueden utilizar remesas para:</span><span class="sxs-lookup"><span data-stu-id="2cc84-129">You can use bill groups for the following:</span></span>  

- <span data-ttu-id="2cc84-130">Factoring sin recurso: la entidad de factoring asume los riesgos asociados con el no-pago.</span><span class="sxs-lookup"><span data-stu-id="2cc84-130">Factoring without risk - The factoring company takes on the risks associated with non-payment.</span></span>  
- <span data-ttu-id="2cc84-131">Factoring con recurso: usted asume los riesgos asociados con el no-pago.</span><span class="sxs-lookup"><span data-stu-id="2cc84-131">Factoring with risk - You take on the risks associated with non-payment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2cc84-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2cc84-132">See Also</span></span>  
 <span data-ttu-id="2cc84-133">[Módulo Cartera](cartera-module.md) </span><span class="sxs-lookup"><span data-stu-id="2cc84-133">[Cartera Module](cartera-module.md) </span></span>  
 [<span data-ttu-id="2cc84-134">Módulo Docs. cartera a pagar</span><span class="sxs-lookup"><span data-stu-id="2cc84-134">Payments Cartera Module</span></span>](payments-cartera-module.md)
