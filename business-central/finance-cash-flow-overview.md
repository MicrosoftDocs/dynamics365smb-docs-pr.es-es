---
title: Descripción del flujo de efectivo
description: Una descripción general de los flujos de entrada y salida de efectivo para ayudar a pronosticar los importes que se recibirán y que se pagarán.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.date: 06/08/2021
ms.author: a-jillk
ms.reviewer: edupont
ms.openlocfilehash: 8359d95b36d6c16b179de2fce400c44fd93ec0f1
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216401"
---
# <a name="cash-flow-overview"></a><span data-ttu-id="b1336-103">Descripción del flujo de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-103">Cash Flow Overview</span></span>

<span data-ttu-id="b1336-104">Conocer las entradas y salidas de efectivo es la clave para una empresa exitosa.</span><span class="sxs-lookup"><span data-stu-id="b1336-104">Understanding cash inflows and outflows is the key to running a successful business.</span></span> <span data-ttu-id="b1336-105">Puede utilizar el flujo de efectivo para crear fácilmente una previsión a corto plazo que prediga cómo y cuándo se espera que su empresa reciba y pague dinero.</span><span class="sxs-lookup"><span data-stu-id="b1336-105">You can use cash flow to easily create a short-term forecast that predicts how and when you expect money to be received and paid out by your business.</span></span> <span data-ttu-id="b1336-106">Es importante que sepa que su empresa tendrá efectivo suficiente para pagar a los acreedores y cubrir los gastos cuando sean sus vencimientos.</span><span class="sxs-lookup"><span data-stu-id="b1336-106">It is important for you to know that your business will have enough cash to pay creditors and expenses when they fall due.</span></span>

## <a name="definition-of-cash-flow"></a><span data-ttu-id="b1336-107">Definición de flujos de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-107">Definition of Cash Flow</span></span>

<span data-ttu-id="b1336-108">El término *flujo de efectivo* se utiliza para designar los cobros menos los pagos en efectivo durante un periodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b1336-108">The term *cash flow* is used to designate cash receipts minus cash payments over a selected period.</span></span> <span data-ttu-id="b1336-109">Es una estimación del importe de dinero que espera que entre y salga de su empresa e incluye todos su ingresos y gastos previstos.</span><span class="sxs-lookup"><span data-stu-id="b1336-109">It is an estimate of the amount of money that you expect to flow in and out of your business, and it includes all your forecasted income and expenses.</span></span>

## <a name="cash-flow-overview"></a><span data-ttu-id="b1336-110">Descripción del flujo de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-110">Cash Flow Overview</span></span>

<span data-ttu-id="b1336-111">El siguiente ejemplo muestra una descripción global de cómo puede trabajar con el flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-111">The following illustration shows an overview of how you can work with cash flow.</span></span>

<span data-ttu-id="b1336-112">![Descripción del flujo de efectivo](media/finance_cash_flow_overview.png "Descripción del flujo de efectivo")</span><span class="sxs-lookup"><span data-stu-id="b1336-112">![Cash Flow overview](media/finance_cash_flow_overview.png "Cash Flow overview")</span></span>

- <span data-ttu-id="b1336-113">Configura una previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-113">You set up a cash flow forecast.</span></span>  

- <span data-ttu-id="b1336-114">Obtiene orígenes de previsiones del flujo de efectivo de las áreas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b1336-114">You get cash flow forecast sources from the following areas:</span></span>  

  - <span data-ttu-id="b1336-115">Contabilidad: información sobre los fondos corrientes e ingresos presupuestarios y los gastos de su empresa.</span><span class="sxs-lookup"><span data-stu-id="b1336-115">General ledger – Information about the liquid funds and the budgeted revenues and expenses of your company.</span></span>  
  - <span data-ttu-id="b1336-116">Compra: información sobre pagos actuales y cualquier deuda prevista de los pedidos de compra abiertos.</span><span class="sxs-lookup"><span data-stu-id="b1336-116">Purchasing – Information about the current payables and any forecasted debts from open purchase orders.</span></span>  
  - <span data-ttu-id="b1336-117">Venta: información sobre cobros actuales y cualquier cobro previsto de los pedidos de venta abiertos.</span><span class="sxs-lookup"><span data-stu-id="b1336-117">Sales – Information about the current receivables and any forecasted receipts from open sales orders.</span></span>  
  - <span data-ttu-id="b1336-118">Servicio: información acerca de pedidos de servicio abiertos.</span><span class="sxs-lookup"><span data-stu-id="b1336-118">Service – Information about open service orders.</span></span>  
  - <span data-ttu-id="b1336-119">Activos fijos: información acerca de la venta/baja planificada y compras presupuestadas de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="b1336-119">Fixed assets – Information about planned disposal and budgeted purchases of fixed assets.</span></span>  
  - <span data-ttu-id="b1336-120">Ingresos y gastos manuales: gestione ingresos y gastos manuales e inclúyalos en la previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-120">Manual revenues and expenses – Manage manual revenues and expenses and include them in the cash flow forecast.</span></span>  
- <span data-ttu-id="b1336-121">Se utiliza un trabajo por lotes para transferir la información de las áreas de contabilidad, compras, ventas, servicio y activos fijos, a la hoja de flujo de efectivo. Posteriormente, puede registrar las líneas de la hoja de trabajo crear una previsión de flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-121">You use a batch job to transfer information from the areas of general ledger, sales, purchasing, service, and fixed assets to the worksheet Then, you register worksheet lines to make a cash flow forecast.</span></span>  
- <span data-ttu-id="b1336-122">Utiliza distintas ventanas, informes y cuadros para analizar e imprimir una previsión del flujo de efectivo que se relaciona con descripciones de la disponibilidad y de la cronología.</span><span class="sxs-lookup"><span data-stu-id="b1336-122">You use various windows, reports, and charts to analyze and print a cash flow forecast that relates to availability and timeline overviews.</span></span>  

## <a name="making-a-cash-flow-forecast"></a><span data-ttu-id="b1336-123">Realización de una previsión flujo efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-123">Making a Cash Flow Forecast</span></span>

<span data-ttu-id="b1336-124">Basándose en las líneas registradas de la hoja de trabajo, puede hacer periódicamente un flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-124">Based on the registered worksheet lines, you can periodically make a cash flow forecast.</span></span> <span data-ttu-id="b1336-125">El siguiente diseño es un diseño que se utiliza con frecuencia para una previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-125">The following layout is a frequently used layout for a cash flow forecast.</span></span> <span data-ttu-id="b1336-126">El diseño tiene tres secciones:</span><span class="sxs-lookup"><span data-stu-id="b1336-126">The layout has three sections:</span></span>

  - <span data-ttu-id="b1336-127">Cobros</span><span class="sxs-lookup"><span data-stu-id="b1336-127">Cash receipts</span></span>  
  - <span data-ttu-id="b1336-128">Desembolso de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-128">Cash disbursements</span></span>  
  - <span data-ttu-id="b1336-129">Flujo de efectivo o efectivo-en-mano neto</span><span class="sxs-lookup"><span data-stu-id="b1336-129">Net cash flow or cash-in-hand</span></span>  

<span data-ttu-id="b1336-130">Los cobros proporcionan detalles de los ingresos que el negocio recibe.</span><span class="sxs-lookup"><span data-stu-id="b1336-130">Cash receipts provide details of the income that the business receives.</span></span>

<span data-ttu-id="b1336-131">*cobros totales* = *cobros* + *pedidos de venta abiertos* + *pedidos de servicio abiertos* + *ventas/bajas de activos fijos* + *ingresos manuales* + *ingresos presupuestados*</span><span class="sxs-lookup"><span data-stu-id="b1336-131">*total cash receipts* = *receivables* + *open sales orders* + *open service orders* + *fixed assets disposals* + *manual revenues* + *budgeted revenues*</span></span>

> [!NOTE]
> <span data-ttu-id="b1336-132">Los ingresos manuales pueden ser ingresos de alquiler, intereses de los activos financieros o nuevo capital privado.</span><span class="sxs-lookup"><span data-stu-id="b1336-132">Manual revenues can be rental income, interest from financial assets, or new private capital.</span></span> <span data-ttu-id="b1336-133">Puede planificar ingresos manuales por un periodo de tiempo y usarlos en el cálculo de previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-133">You can plan manual revenues for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="b1336-134">Los desembolsos de efectivo proporcionan detalles de los pagos realizados por el negocio.</span><span class="sxs-lookup"><span data-stu-id="b1336-134">Cash disbursements provide details of the payments made by the business.</span></span>

<span data-ttu-id="b1336-135">*desembolsos de efectivo totales* = *pagos* + *órdenes de compra abiertas* + *inversión en activosfijos* + *gastos manuales* + *gastos presupuestados*</span><span class="sxs-lookup"><span data-stu-id="b1336-135">*total cash disbursements* = *payables* + *open purchase orders* + *fixed asset investment* + *manual expenses* + *budgeted expenses*</span></span>

> [!NOTE]
> <span data-ttu-id="b1336-136">Los gastos manuales pueden ser salarios, intereses a crédito o consumos privados.</span><span class="sxs-lookup"><span data-stu-id="b1336-136">Manual expenses can be salaries, interest on credit, or private consumptions.</span></span> <span data-ttu-id="b1336-137">Puede planificar gastos manuales por un periodo de tiempo y usarlos en el cálculo de previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="b1336-137">You can plan manual expenses for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="b1336-138">El flujo de efectivo o el efectivo-en-mano neto se calcula como cobros totales menos desembolsos totales al final de cada periodo.</span><span class="sxs-lookup"><span data-stu-id="b1336-138">Net cash flow or cash-in-hand is calculated as total receipts minus total disbursements at the end of each period.</span></span>

<span data-ttu-id="b1336-139">*flujo de efectivo neto* = *cobros totales* – *desembolsos de efectivo totales* + *fondos corrientes*</span><span class="sxs-lookup"><span data-stu-id="b1336-139">*net cash flow* = *total cash receipts* – *total cash disbursements* + *liquid funds*</span></span>

<span data-ttu-id="b1336-140">La previsión puede utilizarse como herramienta interna de toma de decisiones de gestión que contribuye a la planificación y la toma de decisiones estratégicas e importantes sobre la operación del negocio.</span><span class="sxs-lookup"><span data-stu-id="b1336-140">The forecast can then be used as an internal management decision-making tool that helps you plan ahead and make important strategic decisions about the operation of the business.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1336-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1336-141">See Also</span></span>
[<span data-ttu-id="b1336-142">Configuración del análisis de flujo de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
[<span data-ttu-id="b1336-143">Analizar el flujo de efectivo</span><span class="sxs-lookup"><span data-stu-id="b1336-143">Analyze Cash Flow</span></span>](finance-analyze-cash-flow.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
