---
title: Crear una factura de venta para facturar un proyecto | Documentos de Microsoft
description: "Describe cómo facturar a clientes por los costes del proyecto a medida que progresa un proyecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 73894bb8c7193d96ca1f4c4f7c8b8394b1f26f5f
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="invoice-jobs"></a><span data-ttu-id="dd7ff-103">Facturar proyectos</span><span class="sxs-lookup"><span data-stu-id="dd7ff-103">Invoice Jobs</span></span>
<span data-ttu-id="dd7ff-104">Durante el proyecto, pueden acumularse los costes del proyecto por el uso de recursos, materiales y compras relacionadas con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="dd7ff-105">Según progresa el proyecto, estas transacciones se registran en el diario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="dd7ff-106">Es importante que se registren todos los costes en el diario del proyecto antes de facturar al cliente.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="dd7ff-107">Puede facturar el proyecto completo desde la página **Líneas tareas proyecto** o facturar solo las líneas de la factura seleccionada desde la página **Líneas de planificación**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-107">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="dd7ff-108">La facturación se puede realizar una vez finalizado el proyecto o a ciertos intervalos durante el progreso del proyecto, basándose en un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="dd7ff-109">Si selecciona **Facturable** en el campo **Tipo línea proyecto** en los documentos de compra de las compras relacionadas con el proyecto, se crearán las líneas de planificación de proyecto que estén listas para facturarse al cliente.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="dd7ff-110">Para obtener más información, vea [Administrar suministros de proyecto](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="dd7ff-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="dd7ff-111">Para crear y registrar una factura de venta del proyecto</span><span class="sxs-lookup"><span data-stu-id="dd7ff-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="dd7ff-112">Puede crear la factura de un proyecto o de una o varias tareas del proyecto para un cliente cuando se haya terminado el trabajo que se va a facturar o cuando se llegue a la fecha de facturación en función de un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="dd7ff-113">En la página **Proyectos** puede facturar a un cliente seleccionando el proyecto y eligiendo la acción **Crear factura venta proyecto**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-113">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="dd7ff-114">El siguiente procedimiento muestra cómo utilizar un proceso para facturar varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="dd7ff-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Crear factura venta proyecto** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd7ff-116">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="dd7ff-117">Seleccione filtros si desea limitar los proyectos que el proceso va a procesar.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="dd7ff-118">Elija el botón **Aceptar** para crear las facturas.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="dd7ff-119">Para crear varias facturas de venta de proyecto desde líneas de planificación de proyecto</span><span class="sxs-lookup"><span data-stu-id="dd7ff-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="dd7ff-120">Puede crear una factura a partir de las líneas de planificación de proyecto e indicar en ese momento la cantidad del producto, recurso o cuenta que desea facturar.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="dd7ff-121">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="dd7ff-122">Abra un proyecto relevante.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-122">Open a relevant job.</span></span>
3. <span data-ttu-id="dd7ff-123">Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="dd7ff-124">En una línea de planificación de proyecto, en el campo **Cdad. para transferir a factura**, introduzca la cantidad del producto, recurso y el tipo de la cuenta de contabilidad que desee facturar.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="dd7ff-125">Elija la acción **Crear factura venta**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="dd7ff-126">En la página **Crear factura venta proyecto**, escriba la fecha de registro y decida si desea crear una nueva factura o anexar esta factura a una existente.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-126">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="dd7ff-127">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="dd7ff-128">En la línea de planificación de proyecto, en el campo **Cdad. transferida a factura**, puede ver la cantidad.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="dd7ff-129">En la página **Líneas planificación proyecto**, elija la acción **Facturas venta/Abonos venta**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-129">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="dd7ff-130">Se abre la página **Factura venta** que muestra la cantidad que ha transferido a la factura.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-130">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="dd7ff-131">Realice cualquier cambio adicional y, a continuación, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="dd7ff-132">El procedimiento anterior es similar para crear, revisar y registrar un abono de venta relacionado con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="dd7ff-133">Para calcular y registrar los movimientos de finalización de proyecto</span><span class="sxs-lookup"><span data-stu-id="dd7ff-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="dd7ff-134">Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="dd7ff-135">Después, debe revertir cualquier WIP que haya registrado en contabilidad.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="dd7ff-136">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dd7ff-137">Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="dd7ff-138">En el campo **Estado**, seleccione **Completado**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="dd7ff-139">Siga los pasos de la ayuda para calcular y registrar WIP.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="dd7ff-140">También puede seguir los pasos 5 y 6 para hacerlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="dd7ff-141">Elija la acción **Calcular WIP**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="dd7ff-142">En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-142">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="dd7ff-143">Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="dd7ff-144">Elija la acción **Registrar WIP en C/G proyecto**.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="dd7ff-145">En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-145">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="dd7ff-146">Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="dd7ff-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd7ff-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dd7ff-147">See Also</span></span>
[<span data-ttu-id="dd7ff-148">Administrar proyectos</span><span class="sxs-lookup"><span data-stu-id="dd7ff-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="dd7ff-149">Finanzas</span><span class="sxs-lookup"><span data-stu-id="dd7ff-149">Finance</span></span>](finance.md)  
<span data-ttu-id="dd7ff-150">[Compras](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="dd7ff-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="dd7ff-151">[Ccial](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="dd7ff-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="dd7ff-152">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dd7ff-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

