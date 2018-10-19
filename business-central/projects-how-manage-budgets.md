---
title: Configurar y administrar un presupuesto para un proyecto | Documentos de Microsoft
description: "Describe cómo planificar los recursos y prever y controlar los costes de un proyecto mediante la configuración de un presupuesto para cada proyecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 995d181496dc1827f21c0b3edd9e52dd6c15c297
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="34149-103">Gestionar presupuestos de proyecto</span><span class="sxs-lookup"><span data-stu-id="34149-103">Manage Job Budgets</span></span>
<span data-ttu-id="34149-104">Se puede configurar un presupuesto para cada proyecto.</span><span class="sxs-lookup"><span data-stu-id="34149-104">You can set up a budget for each job.</span></span> <span data-ttu-id="34149-105">El presupuesto se utiliza para planificar los recursos que asigna a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="34149-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="34149-106">Puede ser genérico, con pocos movimientos, o bien puede contar con más movimientos divididos en niveles de actividad.</span><span class="sxs-lookup"><span data-stu-id="34149-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="34149-107">Puede comparar los importes presupuestados con el uso real registrado en el diario de proyectos.</span><span class="sxs-lookup"><span data-stu-id="34149-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="34149-108">Si supervisa las diferencias entre el uso real y el uso presupuestado, puede controlar un proyecto en curso y mejorar la calidad de futuros proyectos reduciendo el riesgo de subestimar los costes.</span><span class="sxs-lookup"><span data-stu-id="34149-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="34149-109">El procedimiento siguiente describe cómo calcular los costes presupuestados durante la planificación.</span><span class="sxs-lookup"><span data-stu-id="34149-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="34149-110">Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="34149-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="34149-111">Para estimar los costes presupuestados de un proyecto</span><span class="sxs-lookup"><span data-stu-id="34149-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="34149-112">Si un cliente desea saber el precio de un proyecto que se facturará en función del uso, se deben determinar los costes presupuestados del proyecto.</span><span class="sxs-lookup"><span data-stu-id="34149-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="34149-113">Para hacerlo, debe usar la ventana **Líneas tarea proyecto**.</span><span class="sxs-lookup"><span data-stu-id="34149-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="34149-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="34149-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="34149-115">Abra un proyecto relevante.</span><span class="sxs-lookup"><span data-stu-id="34149-115">Open a relevant job.</span></span>
3. <span data-ttu-id="34149-116">Seleccione una línea de tarea del tipo Registro y, a continuación, elija la acción **Líneas planificación proyecto**.</span><span class="sxs-lookup"><span data-stu-id="34149-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="34149-117">En una línea nueva, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="34149-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="34149-118">En el campo **Tipo de línea**, escriba la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="34149-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="34149-119">Tipo línea</span><span class="sxs-lookup"><span data-stu-id="34149-119">Line Type</span></span> | <span data-ttu-id="34149-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="34149-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="34149-121">**Presupuesto y facturable**</span><span class="sxs-lookup"><span data-stu-id="34149-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="34149-122">Los importes de coste y precio introducidos en la línea de planificación son los costes presupuestados para la línea de planificación concreta.</span><span class="sxs-lookup"><span data-stu-id="34149-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="34149-123">El importe del precio se facturará.</span><span class="sxs-lookup"><span data-stu-id="34149-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="34149-124">**Ppto**</span><span class="sxs-lookup"><span data-stu-id="34149-124">**Budget**</span></span> |<span data-ttu-id="34149-125">Al cliente no se le cobra por el uso.</span><span class="sxs-lookup"><span data-stu-id="34149-125">The customer is not charged for usage.</span></span> <span data-ttu-id="34149-126">La utilización no se transfiere a una factura, pero se utilizará en el cálculo del trabajo en curso.</span><span class="sxs-lookup"><span data-stu-id="34149-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="34149-127">**Facturable**</span><span class="sxs-lookup"><span data-stu-id="34149-127">**Billable**</span></span> |<span data-ttu-id="34149-128">El cliente sí paga por el uso.</span><span class="sxs-lookup"><span data-stu-id="34149-128">The customer is charged for usage.</span></span> <span data-ttu-id="34149-129">La utilización se transfiere a la factura, en función de la cantidad especificada en el campo Cdad. a transferir a factura.</span><span class="sxs-lookup"><span data-stu-id="34149-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="34149-130">El campo **Fecha de planif.** de la línea de planificación contiene la fecha en la que se espera que se complete el uso relacionado con la línea de planificación.</span><span class="sxs-lookup"><span data-stu-id="34149-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="34149-131">También es la fecha en la que la línea de planificación se puede transferir a una factura de venta y registrarla.</span><span class="sxs-lookup"><span data-stu-id="34149-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="34149-132">Cuando rellena el campo **Cantidad**, se calculará el coste y el precio total y se rellenará la línea de planificación.</span><span class="sxs-lookup"><span data-stu-id="34149-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="34149-133">Puede modificarlos en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="34149-133">You can edit them at any time.</span></span>

<span data-ttu-id="34149-134">En la ventana **Ficha proyecto**, puede ver un resumen del total de costes presupuestados, precio presupuestado, coste facturado y el precio facturado para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="34149-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="34149-135">Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="34149-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="34149-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34149-136">See Also</span></span>
[<span data-ttu-id="34149-137">Administración de proyectos</span><span class="sxs-lookup"><span data-stu-id="34149-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="34149-138">Finanzas</span><span class="sxs-lookup"><span data-stu-id="34149-138">Finance</span></span>](finance.md)  
<span data-ttu-id="34149-139">[Compras](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="34149-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="34149-140">[Ventas](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="34149-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="34149-141">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34149-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

