---
title: 'Detalles de diseño: Búsqueda de combinaciones de dimensiones | Documentos de Microsoft'
description: Cuando se cierra una página después de editar un grupo de dimensiones, Business Central evalúa si existe el grupo de dimensiones editado. Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/11/2019
ms.author: sgroespe
ms.openlocfilehash: 499ac8e6e42eeafa12ddee650661200ff876805f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806541"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="c87b9-104">Detalles de diseño: Búsqueda de combinaciones de dimensiones</span><span class="sxs-lookup"><span data-stu-id="c87b9-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="c87b9-105">Cuando se cierra una página después de editar un grupo de dimensiones, [!INCLUDE[d365fin](includes/d365fin_md.md)] evalúa si existe el grupo de dimensiones editado.</span><span class="sxs-lookup"><span data-stu-id="c87b9-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="c87b9-106">Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="c87b9-107">Creación de árbol de búsqueda</span><span class="sxs-lookup"><span data-stu-id="c87b9-107">Building Search Tree</span></span>  
 <span data-ttu-id="c87b9-108">La tabla 481 **Nodo árbol grupo dimensiones** se usa cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] evalúa si ya existe un conjunto de dimensiones en la tabla 480 **Mov. grupo dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="c87b9-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="c87b9-109">La evaluación se realiza de forma recursiva recorriendo el árbol desde el nivel superior con el número 0.</span><span class="sxs-lookup"><span data-stu-id="c87b9-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="c87b9-110">El nivel superior 0 representa un grupo de dimensiones sin movimientos de grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="c87b9-111">Los elementos secundarios de este grupo de dimensiones representan los grupos de dimensiones con un solo movimiento de grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="c87b9-112">Los elementos secundarios de estos grupos de dimensiones representan los grupos de dimensiones con dos elementos secundarios, etc.</span><span class="sxs-lookup"><span data-stu-id="c87b9-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="c87b9-113">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="c87b9-113">Example 1</span></span>  
 <span data-ttu-id="c87b9-114">En el diagrama siguiente se representa un árbol de búsqueda con seis grupos de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="c87b9-115">En el diagrama solo se muestra el movimiento de grupo de dimensiones de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="c87b9-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="c87b9-116">![Ejemplo de estructura de árbol de dimensiones](media/nav2013_dimension_tree.png "Ejemplo de estructura de árbol de dimensiones")</span><span class="sxs-lookup"><span data-stu-id="c87b9-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="c87b9-117">En la tabla siguiente se describe una lista completa de los movimientos de grupo de dimensiones que componen cada grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="c87b9-118">Conjuntos de dimensiones</span><span class="sxs-lookup"><span data-stu-id="c87b9-118">Dimension Sets</span></span>|<span data-ttu-id="c87b9-119">Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="c87b9-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="c87b9-120">Grupo 0</span><span class="sxs-lookup"><span data-stu-id="c87b9-120">Set 0</span></span>|<span data-ttu-id="c87b9-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c87b9-121">None</span></span>|  
|<span data-ttu-id="c87b9-122">Grupo 1</span><span class="sxs-lookup"><span data-stu-id="c87b9-122">Set 1</span></span>|<span data-ttu-id="c87b9-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="c87b9-123">AREA 30</span></span>|  
|<span data-ttu-id="c87b9-124">Grupo 2</span><span class="sxs-lookup"><span data-stu-id="c87b9-124">Set 2</span></span>|<span data-ttu-id="c87b9-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="c87b9-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="c87b9-126">Grupo 3</span><span class="sxs-lookup"><span data-stu-id="c87b9-126">Set 3</span></span>|<span data-ttu-id="c87b9-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="c87b9-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="c87b9-128">Grupo 4</span><span class="sxs-lookup"><span data-stu-id="c87b9-128">Set 4</span></span>|<span data-ttu-id="c87b9-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="c87b9-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="c87b9-130">Grupo 5</span><span class="sxs-lookup"><span data-stu-id="c87b9-130">Set 5</span></span>|<span data-ttu-id="c87b9-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="c87b9-131">AREA 40</span></span>|  
|<span data-ttu-id="c87b9-132">Grupo 6</span><span class="sxs-lookup"><span data-stu-id="c87b9-132">Set 6</span></span>|<span data-ttu-id="c87b9-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="c87b9-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="c87b9-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="c87b9-134">Example 2</span></span>  
 <span data-ttu-id="c87b9-135">En este ejemplo se muestra cómo evalúa [!INCLUDE[d365fin](includes/d365fin_md.md)] si existe un grupo de dimensiones compuesto por movimientos de grupo de dimensiones AREA 40, DEPT PROD.</span><span class="sxs-lookup"><span data-stu-id="c87b9-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="c87b9-136">Primero, [!INCLUDE[d365fin](includes/d365fin_md.md)] también actualiza la tabla **Nodo árbol grupo dimensiones** para garantizar que el árbol de búsqueda obedezca al diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c87b9-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="c87b9-137">Por lo tanto, el grupo de dimensiones 7 se convierte en un elemento secundario del grupo de dimensiones 5.</span><span class="sxs-lookup"><span data-stu-id="c87b9-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="c87b9-138">![Ejemplo de estructura de árbol de dimensiones en NAV 2013](media/nav2013_dimension_tree_example2.png "Ejemplo de estructura de árbol de dimensiones en NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="c87b9-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="c87b9-139">Búsqueda del identificador de grupo dimensiones</span><span class="sxs-lookup"><span data-stu-id="c87b9-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="c87b9-140">En el nivel conceptual, **Id. principal**, **Dimensión** y **Valor dimensión** en el árbol de búsqueda se agrupan y se utilizan como la clave principal porque [!INCLUDE[d365fin](includes/d365fin_md.md)] atraviesa el árbol en el mismo orden que los movimientos de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="c87b9-141">La función GET (registro) se usa para buscar el identificador del grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c87b9-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="c87b9-142">En el ejemplo de código siguiente se muestra cómo encontrar el identificador del grupo de dimensiones cuando hay tres valores de dimensión.</span><span class="sxs-lookup"><span data-stu-id="c87b9-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 <span data-ttu-id="c87b9-143">No obstante, para mantener la capacidad de [!INCLUDE[d365fin](includes/d365fin_md.md)] de cambiar el nombre de una dimensión y un valor de dimensión, la tabla 349 **Valor dimensión** se amplía con un campo numérico entero de **Id. valor de dimensión**.</span><span class="sxs-lookup"><span data-stu-id="c87b9-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename a dimension and dimension value, table 349 **Dimension Value** is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="c87b9-144">Esta tabla convierte el par de campos **Dimensión** y **Valor dimensión** en un valor entero.</span><span class="sxs-lookup"><span data-stu-id="c87b9-144">This table converts the field pair **Dimension** and **Dimension Value** to an integer value.</span></span> <span data-ttu-id="c87b9-145">Al cambiar el nombre de la dimensión y del valor de dimensión, no se modifica el valor de entero.</span><span class="sxs-lookup"><span data-stu-id="c87b9-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="c87b9-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c87b9-146">See Also</span></span>  
 <span data-ttu-id="c87b9-147">[Función GET (Registro)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="c87b9-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="c87b9-148">[Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c87b9-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="c87b9-149">[Información general de los movimientos del grupo dimensiones](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="c87b9-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="c87b9-150">[Detalles de diseño: Estructura de tablas](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="c87b9-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="c87b9-151">[Detalles de diseño: Gestión de dimensiones de codeunit 408](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="c87b9-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="c87b9-152">Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones</span><span class="sxs-lookup"><span data-stu-id="c87b9-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
