---
title: Crear una factura de venta para facturar un proyecto | Documentos de Microsoft
description: Describe cómo facturar a clientes por los costes del proyecto a medida que progresa un proyecto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 05/25/2020
ms.author: edupont
ms.openlocfilehash: 66e5dd52eb01e8a396156d0c646a43916fdc0021
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783962"
---
# <a name="invoice-jobs"></a><span data-ttu-id="aff3c-103">Facturar proyectos</span><span class="sxs-lookup"><span data-stu-id="aff3c-103">Invoice Jobs</span></span>
<span data-ttu-id="aff3c-104">Durante el proyecto, pueden acumularse los costes del proyecto por el uso de recursos, materiales y compras relacionadas con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="aff3c-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="aff3c-105">Según progresa el proyecto, estas transacciones se registran en el diario del proyecto.</span><span class="sxs-lookup"><span data-stu-id="aff3c-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="aff3c-106">Es importante que se registren todos los costes en el diario del proyecto antes de facturar al cliente.</span><span class="sxs-lookup"><span data-stu-id="aff3c-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="aff3c-107">Puede comprar recursos externos no relacionados con un proyecto, por ejemplo, para facturar a un proveedor por el trabajo entregado.</span><span class="sxs-lookup"><span data-stu-id="aff3c-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="aff3c-108">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="aff3c-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="aff3c-109">Puede facturar el proyecto completo desde la página **Líneas tareas proyecto** o facturar solo las líneas de la factura seleccionada desde la página **Líneas de planificación**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="aff3c-110">La facturación se puede realizar una vez finalizado el proyecto o a ciertos intervalos durante el progreso del proyecto, basándose en un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="aff3c-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
> <span data-ttu-id="aff3c-111">Si selecciona **Facturable** en el campo **Tipo línea proyecto** en los documentos de compra de las compras relacionadas con el proyecto, se crearán las líneas de planificación de proyecto que estén listas para facturarse al cliente.</span><span class="sxs-lookup"><span data-stu-id="aff3c-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="aff3c-112">Para obtener más información, vea [Administrar suministros de proyecto](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="aff3c-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-multiple-job-sales-invoices"></a><span data-ttu-id="aff3c-113">Para crear varias facturas de venta de proyecto</span><span class="sxs-lookup"><span data-stu-id="aff3c-113">To create multiple job sales invoices</span></span>
<span data-ttu-id="aff3c-114">Puede crear la factura de un proyecto o de una o varias tareas del proyecto para un cliente cuando se haya terminado el trabajo que se va a facturar o cuando se llegue a la fecha de facturación en función de un programa de facturación.</span><span class="sxs-lookup"><span data-stu-id="aff3c-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="aff3c-115">El siguiente procedimiento muestra cómo utilizar un proceso para facturar varios proyectos.</span><span class="sxs-lookup"><span data-stu-id="aff3c-115">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="aff3c-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Crear factura venta proyecto** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="aff3c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aff3c-117">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="aff3c-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="aff3c-118">Seleccione filtros si desea limitar los proyectos que el proceso va a procesar.</span><span class="sxs-lookup"><span data-stu-id="aff3c-118">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="aff3c-119">Elija el botón **Aceptar** para crear las facturas.</span><span class="sxs-lookup"><span data-stu-id="aff3c-119">Choose the **OK** button to create the invoices.</span></span>  

<span data-ttu-id="aff3c-120">Puede revisar y registrar facturas creadas en la ventana **Facturas de venta**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-120">You can review and post created invoices in the **Sales Invoices** window.</span></span>

> [!NOTE]
> <span data-ttu-id="aff3c-121">También puede facturar a un cliente seleccionando el proyecto y eligiendo la acción **Crear factura venta proyecto**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-121">Alternatively, invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a><span data-ttu-id="aff3c-122">Para crear y registrar facturas de venta de proyecto desde líneas de planificación de proyecto</span><span class="sxs-lookup"><span data-stu-id="aff3c-122">To create and post job sales invoice from job planning lines</span></span>
<span data-ttu-id="aff3c-123">Puede crear una factura a partir de las líneas de planificación de proyecto e indicar en ese momento la cantidad del producto, recurso o cuenta que desea facturar.</span><span class="sxs-lookup"><span data-stu-id="aff3c-123">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="aff3c-124">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="aff3c-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="aff3c-125">Abra un proyecto relevante.</span><span class="sxs-lookup"><span data-stu-id="aff3c-125">Open a relevant job.</span></span>
3. <span data-ttu-id="aff3c-126">Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-126">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="aff3c-127">En una línea de planificación de proyecto, en el campo **Cdad. para transferir a factura**, introduzca la cantidad del producto, recurso y el tipo de la cuenta de contabilidad que desee facturar.</span><span class="sxs-lookup"><span data-stu-id="aff3c-127">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="aff3c-128">Elija la acción **Crear factura venta**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-128">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="aff3c-129">En la página **Crear factura venta proyecto**, escriba la fecha de registro y decida si desea crear una nueva factura o anexar esta factura a una existente.</span><span class="sxs-lookup"><span data-stu-id="aff3c-129">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="aff3c-130">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-130">Choose the **OK** button.</span></span>  
8. <span data-ttu-id="aff3c-131">En la página **Líneas planificación proyecto**, elija la acción **Facturas venta/Abonos venta**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="aff3c-132">Se abre la página **Factura venta** que muestra la cantidad que ha transferido a la factura.</span><span class="sxs-lookup"><span data-stu-id="aff3c-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>
9. <span data-ttu-id="aff3c-133">Realice cualquier cambio adicional y, a continuación, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="aff3c-134">El procedimiento anterior es similar para crear, revisar y registrar un abono de venta relacionado con el proyecto.</span><span class="sxs-lookup"><span data-stu-id="aff3c-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="aff3c-135">Para calcular y registrar los movimientos de finalización de proyecto</span><span class="sxs-lookup"><span data-stu-id="aff3c-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="aff3c-136">Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="aff3c-137">Después, debe revertir cualquier WIP que haya registrado en contabilidad.</span><span class="sxs-lookup"><span data-stu-id="aff3c-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="aff3c-138">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="aff3c-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aff3c-139">Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="aff3c-140">En el campo **Estado**, seleccione **Completado**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="aff3c-141">Siga los pasos de la ayuda para calcular y registrar WIP.</span><span class="sxs-lookup"><span data-stu-id="aff3c-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="aff3c-142">También puede seguir los pasos 5 y 6 para hacerlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="aff3c-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="aff3c-143">Elija la acción **Calcular WIP**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="aff3c-144">En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="aff3c-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="aff3c-145">Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="aff3c-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="aff3c-146">Elija la acción **Registrar WIP en C/G proyecto**.</span><span class="sxs-lookup"><span data-stu-id="aff3c-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="aff3c-147">En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="aff3c-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="aff3c-148">Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.</span><span class="sxs-lookup"><span data-stu-id="aff3c-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="aff3c-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aff3c-149">See Also</span></span>
[<span data-ttu-id="aff3c-150">Administrar proyectos</span><span class="sxs-lookup"><span data-stu-id="aff3c-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="aff3c-151">Finanzas</span><span class="sxs-lookup"><span data-stu-id="aff3c-151">Finance</span></span>](finance.md)  
<span data-ttu-id="aff3c-152">[Compras](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="aff3c-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="aff3c-153">[Ventas](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="aff3c-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="aff3c-154">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aff3c-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
