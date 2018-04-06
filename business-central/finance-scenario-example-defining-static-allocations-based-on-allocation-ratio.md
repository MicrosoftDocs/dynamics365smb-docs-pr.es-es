---
title: "Definición de asignaciones estáticas basadas en la proporción de asignación | Documentos de Microsoft"
description: "El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b4d26e3cb8a1364745dd25ca5341635c49a5718
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="21d6c-103">Ejemplo: definición de asignaciones estáticas basadas en la proporción de asignación</span><span class="sxs-lookup"><span data-stu-id="21d6c-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="21d6c-104">El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="21d6c-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="21d6c-105">Este tema describe cómo definir tres nuevos objetos de coste de destino de asignación para el centro de coste PROD del origen de asignación mediante la proporción 5:2:4 de asignación establecida.</span><span class="sxs-lookup"><span data-stu-id="21d6c-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="21d6c-106">Los tres objetos de coste de destino son ACCESORIOS, PINTURA y COLOCACIONES.</span><span class="sxs-lookup"><span data-stu-id="21d6c-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="21d6c-107">El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="21d6c-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="21d6c-108">Para definir el centro de coste PROD de origen de asignación en la ficha desplegable General</span><span class="sxs-lookup"><span data-stu-id="21d6c-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="21d6c-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignación costes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="21d6c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="21d6c-110">En la ventana **Asignación de costes**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="21d6c-111">En el campo **ID**, presione Entrar o escriba un Id.</span><span class="sxs-lookup"><span data-stu-id="21d6c-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="21d6c-112">En el campo **Nivel**, introduzca **1**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="21d6c-113">Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="21d6c-114">En el campo **Código centro coste**, introduzca **PROD**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="21d6c-115">En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="21d6c-116">Para definir los objetos de coste de destino de asignación en la Ficha desplegable Líneas</span><span class="sxs-lookup"><span data-stu-id="21d6c-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="21d6c-117">En la primera línea, en el campo **Tipo coste destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="21d6c-118">En la primera línea, en el campo **Objeto de coste de destino**, seleccione **ACCESORIOS**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="21d6c-119">En la primera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.</span><span class="sxs-lookup"><span data-stu-id="21d6c-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="21d6c-120">En la primera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="21d6c-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="21d6c-121">En la primera línea, en el campo **Compartir**, especifique la proporción de asignación **5**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="21d6c-122">En la segunda línea, en el campo **Tipo coste destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="21d6c-123">En la segunda línea, en el campo **Objeto de coste de destino**, seleccione **PINTURA**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="21d6c-124">En la segunda línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.</span><span class="sxs-lookup"><span data-stu-id="21d6c-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="21d6c-125">En la segunda línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="21d6c-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="21d6c-126">En la segunda línea, en el campo **Compartir**, especifique la proporción de asignación **2**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="21d6c-127">En la tercera línea, en el campo **Tipo coste destino**, especifique **9903**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="21d6c-128">En la tercera línea, en el campo **Objeto de coste de destino**, seleccione **COMPLEM**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="21d6c-129">En la tercera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.</span><span class="sxs-lookup"><span data-stu-id="21d6c-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="21d6c-130">En la tercera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.</span><span class="sxs-lookup"><span data-stu-id="21d6c-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="21d6c-131">En la tercera línea, en el campo **Compartir**, especifique la proporción de asignación **4**.</span><span class="sxs-lookup"><span data-stu-id="21d6c-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="21d6c-132"> calcula automáticamente el campo **Porcentaje** con un porcentaje que depende de las tres relaciones de asignación que se han introducido en el campo **Compartir** para las tres líneas.</span><span class="sxs-lookup"><span data-stu-id="21d6c-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21d6c-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="21d6c-133">See Also</span></span>  
<span data-ttu-id="21d6c-134">[Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="21d6c-134">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="21d6c-135">[Definición y asignación de costes](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="21d6c-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="21d6c-136">[Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="21d6c-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="21d6c-137">Definición y asignación de costes</span><span class="sxs-lookup"><span data-stu-id="21d6c-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

