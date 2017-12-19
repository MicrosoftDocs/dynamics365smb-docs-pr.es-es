---
title: Crear presupuestos contables | Documentos de Microsoft
description: "Describe cómo crear presupuestos contables para prever diferentes actividades financieras y asignar dimensiones para fines de inteligencia empresarial."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: 34642192e74992953b569cabeb5dbeb4112a0f44
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-create-gl-budgets"></a><span data-ttu-id="9d8f4-103">Crear presupuestos contables</span><span class="sxs-lookup"><span data-stu-id="9d8f4-103">How to: Create G/L Budgets</span></span>
<span data-ttu-id="9d8f4-104">Puede tener varios presupuestos para idénticos periodos de tiempo si crea presupuestos con nombres distintos.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="9d8f4-105">En primer lugar, debe configurar el nombre del presupuesto e introducir las cifras del presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="9d8f4-106">El nombre del presupuesto se incluye en todos los movimientos de presupuesto que cree.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="9d8f4-107">Al crear un presupuesto, puede definir cuatro dimensiones para cada presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="9d8f4-108">Estas dimensiones específicas de presupuesto se denominan dimensiones de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="9d8f4-109">Seleccione las dimensiones de presupuesto para cada uno de los presupuestos a partir de las dimensiones que ya ha configurado.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="9d8f4-110">Es posible utilizar las dimensiones de presupuesto para filtrar en un presupuesto y para agregar información de dimensiones a movimientos de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="9d8f4-111">Para obtener más información, consulte [Trabajar con dimensiones](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f4-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="9d8f4-112">Los presupuestos desempeñan una función importante en la inteligencia empresarial, como los extractos financieros en función de los esquemas de cuentas que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="9d8f4-113">Para obtener más información, consulte [Inteligencia empresarial](bi.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f4-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="9d8f4-114">Los presupuestos desempeñan una función importante en la inteligencia empresarial, como los extractos financieros en función de los esquemas de cuentas que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="9d8f4-115">Para obtener más información, consulte [Inteligencia empresarial](bi.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f4-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="9d8f4-116">En contabilidad de costes, trabaja con los presupuestos de costes de forma similar.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="9d8f4-117">Para obtener más información, consulte [Crear presupuestos de costes](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f4-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="9d8f4-118">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="9d8f4-119">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="9d8f4-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="9d8f4-120">Para crear un nuevo presupuesto contable</span><span class="sxs-lookup"><span data-stu-id="9d8f4-120">To create a new G/L budget</span></span>  
1. <span data-ttu-id="9d8f4-121">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Presupuestos contables** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9d8f4-122">Elija la acción **Editar lista** y, a continuación, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="9d8f4-123">Seleccione la acción **Editar presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="9d8f4-124">En la parte superior de la ventana **Presupuesto** rellene los campos según sea necesario para definir lo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="9d8f4-125">Solo se mostrarán los movimientos que contengan el nombre del presupuesto que ha introducido en el campo **Nombre presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="9d8f4-126">Dado que el nombre de presupuesto acaba de crearse, no hay movimientos que coincidan con el filtro.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="9d8f4-127">Por tanto, la ventana está vacía.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="9d8f4-128">Para escribir una cantidad, seleccione la celda correspondiente de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="9d8f4-129">Se abre la ventana **Movs. pptos. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="9d8f4-130">Cree una nueva línea y rellene el campo **Importe**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="9d8f4-131">Cierre la ventana **Movs. pptos. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="9d8f4-132">Repita los pasos de 5 y 6 hasta que escriba todos los importes del presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9d8f4-133">En la ficha desplegable **Filtros** puede filtrar la información de presupuesto por las dimensiones de presupuesto que haya configurado con ese nombre de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="9d8f4-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="9d8f4-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d8f4-134">See Also</span></span>
[<span data-ttu-id="9d8f4-135">Finanzas</span><span class="sxs-lookup"><span data-stu-id="9d8f4-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="9d8f4-136">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="9d8f4-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="9d8f4-137">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="9d8f4-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="9d8f4-138">Libro mayor y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="9d8f4-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="9d8f4-139">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9d8f4-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

