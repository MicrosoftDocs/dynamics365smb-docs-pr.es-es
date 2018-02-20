---
title: Registrar y ajustar el uso y los precios de los recursos | Documentos de Microsoft
description: "Describe cómo puede registrar el uso o consumo de recursos asociados a un proyecto, para realizar el seguimiento y administrar costes, precios y tipos de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f86fed1b300df98ef120e2f91fdd0785670d04f1
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="9bf50-103">Uso de recursos para proyectos</span><span class="sxs-lookup"><span data-stu-id="9bf50-103">Use Resources for Jobs</span></span>
<span data-ttu-id="9bf50-104">El consumo de los recursos en el diario de proyectos se registra para hacer un seguimiento de costes, precios y tipos de trabajo que están vinculados a proyectos.</span><span class="sxs-lookup"><span data-stu-id="9bf50-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="9bf50-105">Para obtener más información, consulte [Registro del uso para proyectos](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="9bf50-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="9bf50-106">El consumo de un recurso también se puede registrar en un diario de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bf50-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="9bf50-107">Los movimientos registrados en un diario de recursos no afectan a la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="9bf50-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="9bf50-108">Para asignar recursos a proyectos</span><span class="sxs-lookup"><span data-stu-id="9bf50-108">To assign resources to jobs</span></span>
<span data-ttu-id="9bf50-109">Asigne recursos a proyectos creando líneas de planificación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9bf50-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="9bf50-110">Para obtener más información, vea [Crear proyectos](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="9bf50-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="9bf50-111">Para registrar el uso de recursos de un proyecto</span><span class="sxs-lookup"><span data-stu-id="9bf50-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="9bf50-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9bf50-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bf50-113">Abra una sección del diario de proyectos correspondiente y, a continuación, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9bf50-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="9bf50-114">Cuando el diario esté completo, seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="9bf50-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="9bf50-115">Para ajustar los precios de los recursos</span><span class="sxs-lookup"><span data-stu-id="9bf50-115">To adjust resource prices</span></span>
<span data-ttu-id="9bf50-116">Si desea modificar los precios de coste y de venta de un gran número de recursos, puede utilizar un proceso.</span><span class="sxs-lookup"><span data-stu-id="9bf50-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="9bf50-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Modificar precios recursos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9bf50-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bf50-118">Rellene los campos de una línea según sea necesario y, a continuación, haga clic en el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9bf50-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9bf50-119">Este proceso no crea ni ajusta costes o precios alternativos de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bf50-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="9bf50-120">Solo cambia el contenido del campo de la ficha del recurso del **Campo ajuste** seleccionada en el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="9bf50-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="9bf50-121">Dado que el ajuste surte efecto en los recursos al instante, compruebe los factores de ajuste antes de ejecutar el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="9bf50-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="9bf50-122">Para obtener propuestas de modificación de precios de venta de recursos basadas en precios de venta alternativos existentes</span><span class="sxs-lookup"><span data-stu-id="9bf50-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="9bf50-123">Si ya ha configurado precios de venta alternativos para algunos recursos, puede utilizar un proceso para configurar varios precios de venta de recurso alternativos.</span><span class="sxs-lookup"><span data-stu-id="9bf50-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="9bf50-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cambios de precio en recursos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9bf50-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bf50-125">Elija la acción **Prop. mod. recursos (precio)** y, a continuación, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9bf50-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="9bf50-126">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9bf50-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="9bf50-127">Cuando termine el proceso, la ventana **Cambios de precio en recursos** muestra los resultados del proceso.</span><span class="sxs-lookup"><span data-stu-id="9bf50-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="9bf50-128">Para obtener propuestas de cambio de precio de venta de recursos basadas en precios de venta estándar</span><span class="sxs-lookup"><span data-stu-id="9bf50-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="9bf50-129">Si desea configurar varios precios alternativos basados en los precios estándar que figuran en las fichas de recurso, puede utilizar un proceso.</span><span class="sxs-lookup"><span data-stu-id="9bf50-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="9bf50-130">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cambios de precio en recursos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9bf50-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="9bf50-131">Elija la acción **Prop. mod. recurso (recurso)** y, a continuación, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9bf50-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="9bf50-132">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9bf50-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="9bf50-133">Cuando termine el proceso, abra la ventana **Cambios de precio en recursos** para ver los resultados del proceso.</span><span class="sxs-lookup"><span data-stu-id="9bf50-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="9bf50-134">Para obtener propuestas para la modificación de precios de venta de recursos basadas en los precios de venta estándar</span><span class="sxs-lookup"><span data-stu-id="9bf50-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="9bf50-135">Si ya ha configurado precios de venta alternativos para algunos recursos, puede utilizar un proceso para configurar varios precios de venta de recurso alternativos.</span><span class="sxs-lookup"><span data-stu-id="9bf50-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="9bf50-136">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Prop. &mod. recursos (precio)** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9bf50-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9bf50-137">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9bf50-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="9bf50-138">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9bf50-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="9bf50-139">Cuando termine el proceso, abra la ventana **Cambios de precio en recursos** para ver los resultados del proceso.</span><span class="sxs-lookup"><span data-stu-id="9bf50-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bf50-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9bf50-140">See Also</span></span>
[<span data-ttu-id="9bf50-141">Administración de proyectos</span><span class="sxs-lookup"><span data-stu-id="9bf50-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="9bf50-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="9bf50-142">Finance</span></span>](finance.md)  
<span data-ttu-id="9bf50-143">[Compras](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="9bf50-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="9bf50-144">[Ventas](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="9bf50-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="9bf50-145">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bf50-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

