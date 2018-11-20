---
title: "Cómo configurar centros de coste | Documentos de Microsoft"
description: "Los centros de coste son departamentos que son responsables de los costes y de los ingresos. El plan de centros de coste es similar a la información de dimensión de contabilidad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 352933268e482424033d2213d2a6849c3702cb03
ms.contentlocale: es-es
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="a5bce-104">Configurar centros de costes</span><span class="sxs-lookup"><span data-stu-id="a5bce-104">Set Up Cost Centers</span></span>
<span data-ttu-id="a5bce-105">Los centros de coste son departamentos que son responsables de los costes y de los ingresos.</span><span class="sxs-lookup"><span data-stu-id="a5bce-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="a5bce-106">El plan de centros de coste es similar a la información de dimensión de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="a5bce-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="a5bce-107">Puede configurar el plan de centros de coste de la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="a5bce-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="a5bce-108">Transfiera los valores de dimensión en la contabilidad al plan de centros de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="a5bce-109">Puede hacer los ajustes necesarios después de la transferencia.</span><span class="sxs-lookup"><span data-stu-id="a5bce-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="a5bce-110">Cree un nuevo plan de centro de coste que es independiente de la contabilidad o agregue un nuevo centro de coste a un plan existente de centro de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="a5bce-111">Debe crear cada centro de coste por separado.</span><span class="sxs-lookup"><span data-stu-id="a5bce-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="a5bce-112">Para transferir los valores de dimensión en la contabilidad al plan de centros de coste</span><span class="sxs-lookup"><span data-stu-id="a5bce-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="a5bce-113">Configure una dimensión para que sea la dimensión del centro de coste en la ventana **Actualizar dimensiones contabilidad costes**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="a5bce-114">Sólo los valores de esta dimensión se transfieren.</span><span class="sxs-lookup"><span data-stu-id="a5bce-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="a5bce-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan centros coste** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="a5bce-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="a5bce-116">En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Traer centros de coste de dimensión** para transferir los valores de dimensión al plan de centros de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="a5bce-117">La función transfiere los valores de dimensión que definió en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="a5bce-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a5bce-118">Puede configurar el campo **Alinear dimensión centro coste** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de centros de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="a5bce-119">No puede definir una sincronización del plan de centros de coste a los valores de dimensión de la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="a5bce-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="a5bce-120">El plan de centros de coste contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.</span><span class="sxs-lookup"><span data-stu-id="a5bce-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="a5bce-121">Crear nuevos centros de coste en la ventana Plan centros coste</span><span class="sxs-lookup"><span data-stu-id="a5bce-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="a5bce-122">Puede configurar y mantener centros de coste en la ficha **Ficha centro de coste** o bien en la ventana **Plan centros coste**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="a5bce-123">En este procedimiento, va a configurar centros de coste en la ventana **Plan de centros de coste**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="a5bce-124">Abra la ventana **Plan centros coste** en el modo de edición.</span><span class="sxs-lookup"><span data-stu-id="a5bce-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="a5bce-125">En el campo **Código**, introduzca el código del centro de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="a5bce-126">Todos los centros de coste deben disponer de un código.</span><span class="sxs-lookup"><span data-stu-id="a5bce-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="a5bce-127">En el campo **Nombre**, introduzca el nombre del centro de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="a5bce-128">Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del centro de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="a5bce-129">Para los centros de coste de la línea **Total** debe rellenar el campo **Totales**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="a5bce-130">Utilice el operador **or**, que es una línea vertical (**&#124;**) para establecer rangos de centros de coste.</span><span class="sxs-lookup"><span data-stu-id="a5bce-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="a5bce-131">Para centros de coste del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Aplicar sangría.</span><span class="sxs-lookup"><span data-stu-id="a5bce-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="a5bce-132">Rellene los campos **Orden clasificación** y **Subtipo de coste** .</span><span class="sxs-lookup"><span data-stu-id="a5bce-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="a5bce-133">Seleccione la siguiente línea vacía para crear un centro de coste nuevo y, a continuación, repita del paso 2 al 5.</span><span class="sxs-lookup"><span data-stu-id="a5bce-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="a5bce-134">Cuando haya configurado todos los centros de coste, elija la acción **Aplicar sangría a centros coste**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="a5bce-135">Elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="a5bce-136">Si ha introducido definiciones en los campos **Totales** para los centros de coste de **Total-final** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas.</span><span class="sxs-lookup"><span data-stu-id="a5bce-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="a5bce-137">La función sobrescribe los valores de todos los campos de **Total final**.</span><span class="sxs-lookup"><span data-stu-id="a5bce-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5bce-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5bce-138">See Also</span></span>  
[<span data-ttu-id="a5bce-139">Contabilidad para costes</span><span class="sxs-lookup"><span data-stu-id="a5bce-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="a5bce-140">[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a5bce-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="a5bce-141">[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="a5bce-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="a5bce-142">Acerca de la contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="a5bce-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="a5bce-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5bce-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

