---
title: Crear una factura de venta para facturar un proyecto | Documentos de Microsoft
description: "Describe cómo facturar a clientes por los costes del proyecto a medida que progresa un proyecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2fdc8f99fa81a0eecd55438bba33b1a93335a416
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-invoice-jobs"></a><span data-ttu-id="9f0e7-103">Facturación de proyectos</span><span class="sxs-lookup"><span data-stu-id="9f0e7-103">How to: Invoice Jobs</span></span>
<span data-ttu-id="9f0e7-104">Durante el proyecto, pueden acumularse los costes del proyecto por el uso de recursos, materiales y compras relacionadas con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="9f0e7-105">Según progresa el proyecto, estas transacciones se registran en el diario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="9f0e7-106">Es importante que se registren todos los costes en el diario del proyecto antes de facturar al cliente.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="9f0e7-107">Puede facturar el proyecto completo desde la ventana **Líneas tareas proyecto** o facturar solo las líneas de la factura seleccionada desde la ventana **Líneas de planificación**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="9f0e7-108">La facturación se puede realizar una vez finalizado el proyecto o a ciertos intervalos durante el progreso del proyecto, basándose en un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9f0e7-109">Si selecciona **Facturable** en el campo **Tipo línea proyecto** en los documentos de compra de las compras relacionadas con el proyecto, se crearán las líneas de planificación de proyecto que estén listas para facturarse al cliente.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="9f0e7-110">Para obtener más información, vea [Administrar suministros de proyecto](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="9f0e7-110">For more information, see [How to: Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="9f0e7-111">Para crear y registrar una factura de venta del proyecto</span><span class="sxs-lookup"><span data-stu-id="9f0e7-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="9f0e7-112">Puede crear la factura de un proyecto o de una o varias tareas del proyecto para un cliente cuando se haya terminado el trabajo que se va a facturar o cuando se llegue a la fecha de facturación en función de un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="9f0e7-113">En la ventana **Proyectos** puede facturar a un cliente seleccionando el proyecto y eligiendo la acción **Crear factura venta proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="9f0e7-114">El siguiente procedimiento muestra cómo utilizar un proceso para facturar varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="9f0e7-115">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Crear factura venta proyecto** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9f0e7-116">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9f0e7-117">Seleccione filtros si desea limitar los proyectos que el proceso va a procesar.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="9f0e7-118">Elija el botón **Aceptar** para crear las facturas.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="9f0e7-119">Para crear varias facturas de venta de proyecto desde líneas de planificación de proyecto</span><span class="sxs-lookup"><span data-stu-id="9f0e7-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="9f0e7-120">Puede crear una factura a partir de las líneas de planificación de proyecto e indicar en ese momento la cantidad del producto, recurso o cuenta que desea facturar.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="9f0e7-121">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="9f0e7-122">Abra un proyecto relevante.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-122">Open a relevant job.</span></span>
3. <span data-ttu-id="9f0e7-123">Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="9f0e7-124">En una línea de planificación de proyecto, en el campo **Cdad. para transferir a factura**, introduzca la cantidad del producto, recurso y el tipo de la cuenta de contabilidad que desee facturar.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="9f0e7-125">Elija la acción **Crear factura venta**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="9f0e7-126">En la ventana **Crear factura venta proyecto**, escriba la fecha de registro y decida si desea crear una nueva factura o anexar esta factura a una existente.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="9f0e7-127">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="9f0e7-128">En la línea de planificación de proyecto, en el campo **Cdad. transferida a factura**, puede ver la cantidad.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="9f0e7-129">En la ventana **Líneas planificación proyecto**, elija la acción **Facturas venta/Abonos venta**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="9f0e7-130">Se abre la ventana **Factura venta** que muestra la cantidad que ha transferido a la factura.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="9f0e7-131">Realice cualquier cambio adicional y, a continuación, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9f0e7-132">El procedimiento anterior es similar para crear, revisar y registrar un abono de venta relacionado con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="9f0e7-133">Para calcular y registrar los movimientos de finalización de proyecto</span><span class="sxs-lookup"><span data-stu-id="9f0e7-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="9f0e7-134">Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="9f0e7-135">Después, debe revertir cualquier WIP que haya registrado en contabilidad.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="9f0e7-136">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9f0e7-137">Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9f0e7-138">En el campo **Estado**, seleccione **Completado**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="9f0e7-139">Siga los pasos de la ayuda para calcular y registrar WIP.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="9f0e7-140">También puede seguir los pasos 5 y 6 para hacerlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="9f0e7-141">Elija la acción **Calcular WIP**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="9f0e7-142">En la ventana **Calcular WIP proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="9f0e7-143">Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="9f0e7-144">Elija la acción **Registrar WIP en C/G proyecto**.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="9f0e7-145">En la ventana **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="9f0e7-146">Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="9f0e7-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f0e7-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f0e7-147">See Also</span></span>
[<span data-ttu-id="9f0e7-148">Administrar proyectos</span><span class="sxs-lookup"><span data-stu-id="9f0e7-148">Manage Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="9f0e7-149">Finanzas</span><span class="sxs-lookup"><span data-stu-id="9f0e7-149">Finance</span></span>](finance.md)  
<span data-ttu-id="9f0e7-150">[Compras](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="9f0e7-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="9f0e7-151">[Ventas](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="9f0e7-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="9f0e7-152">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9f0e7-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

