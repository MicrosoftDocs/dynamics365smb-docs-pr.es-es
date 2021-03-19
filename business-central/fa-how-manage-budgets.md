---
title: Administrar presupuestos de activos fijos | Documentos de Microsoft
description: Puede configurar la información sobre inversiones, ventas/bajas y amortizaciones futuras de activos fijos como ayuda para preparar presupuestos y previsiones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: acdff4ac5879ee3b9c4237d4bcf6e2d30af72dff
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380511"
---
# <a name="manage-budgets-for-fixed-assets"></a><span data-ttu-id="0a53c-103">Gestionar presupuestos de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="0a53c-103">Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="0a53c-104">Puede configurar activos fijos presupuestados.</span><span class="sxs-lookup"><span data-stu-id="0a53c-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="0a53c-105">Por ejemplo, esto le permite incluir adquisiciones y ventas anticipadas en los informes.</span><span class="sxs-lookup"><span data-stu-id="0a53c-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="0a53c-106">Para preparar sus presupuestos de ingresos, presupuestos de cuentas de balance y el presupuesto de caja, necesitará información acerca de las inversiones futuras, ventas/bajas y amortización de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="0a53c-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="0a53c-107">Puede obtener esta información desde el informe **A/F - Proyección amort**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="0a53c-108">Antes de imprimir este informe, debe preparar el presupuesto.</span><span class="sxs-lookup"><span data-stu-id="0a53c-108">Before you print this report, you must prepare the budget.</span></span>  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="0a53c-109">Para presupuestar el coste de un activo</span><span class="sxs-lookup"><span data-stu-id="0a53c-109">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="0a53c-110">Para preparar presupuestos, necesita configurar fiches de activos para los activos que quiera comprar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0a53c-110">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="0a53c-111">Los activos fijos presupuestados se configuran como activos normales, pero deben configurarse para que no se registren en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="0a53c-111">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="0a53c-112">Al registrar el coste, introduzca el número de activos presupuestados en el campo **A/F N.º pptdo.**</span><span class="sxs-lookup"><span data-stu-id="0a53c-112">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="0a53c-113">Esto provocará que se registre un coste con signo inverso en el activo presupuestado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-113">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="0a53c-114">Significa que el coste total del activo presupuestado es la diferencia entre el coste presupuestado y el real.</span><span class="sxs-lookup"><span data-stu-id="0a53c-114">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="0a53c-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a53c-116">Elija la acción **Nuevo** para crear una nueva ficha del activo para el activo presupuestado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-116">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="0a53c-117">Seleccione la casilla **Activo presupuestado** para evitar su registro en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="0a53c-117">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="0a53c-118">Rellene los campos restantes, asigne un libro de amortización y, a continuación, registre el primer coste con el activo presupuestado especificado en el campo **A/F N. º pptdo.** en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="0a53c-118">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="0a53c-119">Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="0a53c-119">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="0a53c-120">Para presupuestar la venta/baja de un activo fijo</span><span class="sxs-lookup"><span data-stu-id="0a53c-120">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="0a53c-121">Si desea vender activos en el periodo de presupuesto, puede especificar información acerca del precio y fecha de venta.</span><span class="sxs-lookup"><span data-stu-id="0a53c-121">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="0a53c-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a53c-123">Seleccione el activo que desee dar de baja o vender y, a continuación, elija la acción **Libros amortización**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-123">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="0a53c-124">En la página **Libros amortización A/F**, rellene los campos **Fecha prevista venta/baja** y **Ingresos previstos venta/baja**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-124">On the **FA Depreciation Books** page, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="0a53c-125">Para ver valores venta/baja previstos</span><span class="sxs-lookup"><span data-stu-id="0a53c-125">To view projected disposal values</span></span>
<span data-ttu-id="0a53c-126">Para ver los valores venta/baja previstos y que se calculen las ganancias y pérdidas, puede usar el informe **Proyección de la amortización A/F**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-126">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="0a53c-127">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyección de la amortización A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a53c-128">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0a53c-128">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="0a53c-129">Haga clic en el botón **Imprimir** o **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-129">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="0a53c-130">Para presupuestar amortización</span><span class="sxs-lookup"><span data-stu-id="0a53c-130">To budget depreciation</span></span>
<span data-ttu-id="0a53c-131">Puede usar el informe **A/F - Proyección amort.** para calcular la amortización futura.</span><span class="sxs-lookup"><span data-stu-id="0a53c-131">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="0a53c-132">El informe muestra el valor neto y la amortización acumulada al principio del periodo seleccionado, los cambios durante el periodo y el valor neto y la amortización acumulada al final del periodo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-132">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="0a53c-133">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Valor proyectado de activo fijo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a53c-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a53c-134">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0a53c-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="0a53c-135">Para ver los valores totales de todos los activos, desactive la casilla **Imprimir por activo fijo**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-135">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="0a53c-136">Deje en blanco la ficha desplegable **Activo** para incluir todos los activos.</span><span class="sxs-lookup"><span data-stu-id="0a53c-136">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="0a53c-137">En el campo **Activo presupuestado**, puede especificar **No** para excluir los activos presupuestados o **Sí** para ver solo los activos presupuestados.</span><span class="sxs-lookup"><span data-stu-id="0a53c-137">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="0a53c-138">Haga clic en el botón **Imprimir** o **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="0a53c-138">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a53c-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a53c-139">See Also</span></span>
[<span data-ttu-id="0a53c-140">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="0a53c-140">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="0a53c-141">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="0a53c-141">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="0a53c-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="0a53c-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="0a53c-143">Introducción</span><span class="sxs-lookup"><span data-stu-id="0a53c-143">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="0a53c-144">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a53c-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]