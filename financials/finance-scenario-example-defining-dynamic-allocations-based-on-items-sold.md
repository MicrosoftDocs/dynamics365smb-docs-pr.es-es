---
title: "Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos | Documentos de Microsoft"
description: "Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="47891-103">Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos</span><span class="sxs-lookup"><span data-stu-id="47891-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="47891-104">Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica.</span><span class="sxs-lookup"><span data-stu-id="47891-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="47891-105">En el ejemplo, se cambia la asignación dinámica de los costes del centro de coste VENTAS para admitir el nuevo EQUIPO TI del objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="47891-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="47891-106">Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W.</span><span class="sxs-lookup"><span data-stu-id="47891-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="47891-107">Utiliza las cifras de ventas del año anterior para calcular el reparto.</span><span class="sxs-lookup"><span data-stu-id="47891-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="47891-108">La asignación se registra al tipo de coste de ayuda 9903.</span><span class="sxs-lookup"><span data-stu-id="47891-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="47891-109">El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="47891-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="47891-110">Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior</span><span class="sxs-lookup"><span data-stu-id="47891-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="47891-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignaciones coste** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="47891-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="47891-112">En la ventana **Asignación de costes**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="47891-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="47891-113">En el campo **ID**, presione Entrar o escriba un Id.</span><span class="sxs-lookup"><span data-stu-id="47891-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="47891-114">En el campo **Nivel**, introduzca **1**.</span><span class="sxs-lookup"><span data-stu-id="47891-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="47891-115">Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.</span><span class="sxs-lookup"><span data-stu-id="47891-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="47891-116">En el campo **Código centro coste**, introduzca **VENTAS**.</span><span class="sxs-lookup"><span data-stu-id="47891-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="47891-117">En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.</span><span class="sxs-lookup"><span data-stu-id="47891-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="47891-118">En el campo **Tipo coste destino**, especifique un tipo de coste **9903**.</span><span class="sxs-lookup"><span data-stu-id="47891-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="47891-119">En el campo **Objeto de coste de destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de coste y rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="47891-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="47891-120">Seleccione **EQUIPO TI**.</span><span class="sxs-lookup"><span data-stu-id="47891-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="47891-121">Deje en blanco el campo **Centro de coste de destino**.</span><span class="sxs-lookup"><span data-stu-id="47891-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="47891-122">En el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.</span><span class="sxs-lookup"><span data-stu-id="47891-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="47891-123">En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.</span><span class="sxs-lookup"><span data-stu-id="47891-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="47891-124">En el campo **Nº filtro**, especifique **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="47891-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="47891-125">En el campo **Filtro fecha vto.**, especifique **Año anterior**.</span><span class="sxs-lookup"><span data-stu-id="47891-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="47891-126">Elija la acción **Calcular clave de asignación** para calcular el reparto.</span><span class="sxs-lookup"><span data-stu-id="47891-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="47891-127"> utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 DL con el 100 por ciento para los paquetes de EQUIPO TI.</span><span class="sxs-lookup"><span data-stu-id="47891-127"> uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="47891-128">Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="47891-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="47891-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47891-129">See Also</span></span>  
 <span data-ttu-id="47891-130">[Configuración de filtros para las bases de la asignación dinámica](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="47891-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="47891-131">[Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="47891-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="47891-132">[Definición y asignación de costes](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="47891-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="47891-133">[Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="47891-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="47891-134">Acerca de la contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="47891-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

