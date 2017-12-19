---
title: "Detalles de diseño: Búsqueda de combinaciones de dimensiones | Documentos de Microsoft"
description: "Cuando se cierra una ventana después de editar un grupo de dimensiones, Dynamics 365 evalúa si existe el grupo de dimensiones editado. Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones."
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
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 64e5191fd2947a8e19595d8c9f1ece4eeff77ec0
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-searching-for-dimension-combinations"></a>Detalles de diseño: Búsqueda de combinaciones de dimensiones
Cuando se cierra una ventana después de editar un grupo de dimensiones, [!INCLUDE[d365fin](includes/d365fin_md.md)] evalúa si existe el grupo de dimensiones editado. Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones.  

## <a name="building-search-tree"></a>Creación de árbol de búsqueda  
 La tabla 481 **Nodo árbol grupo dimensiones** se usa cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] evalúa si ya existe un conjunto de dimensiones en la tabla 480 **Mov. grupo dimensiones**. La evaluación se realiza de forma recursiva recorriendo el árbol desde el nivel superior con el número 0. El nivel superior 0 representa un grupo de dimensiones sin movimientos de grupo de dimensiones. Los elementos secundarios de este grupo de dimensiones representan los grupos de dimensiones con un solo movimiento de grupo de dimensiones. Los elementos secundarios de estos grupos de dimensiones representan los grupos de dimensiones con dos elementos secundarios, etc.  

### <a name="example-1"></a>Ejemplo 1  
 En el diagrama siguiente se representa un árbol de búsqueda con seis grupos de dimensiones. En el diagrama solo se muestra el movimiento de grupo de dimensiones de diferenciación.  

 ![Estructura de árbol de dimensiones](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")  

 En la tabla siguiente se describe una lista completa de los movimientos de grupo de dimensiones que componen cada grupo de dimensiones.  

|Conjuntos de dimensiones|Movimientos de grupo de dimensiones|  
|--------------------|---------------------------|  
|Grupo 0|Ninguno|  
|Grupo 1|AREA 30|  
|Grupo 2|AREA 30, DEPT ADM|  
|Grupo 3|AREA 30, DEPT PROD|  
|Grupo 4|AREA 30, DEPT ADM, PROJ VW|  
|Grupo 5|AREA 40|  
|Grupo 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Ejemplo 2  
 En este ejemplo se muestra cómo evalúa [!INCLUDE[d365fin](includes/d365fin_md.md)] si existe un grupo de dimensiones compuesto por movimientos de grupo de dimensiones AREA 40, DEPT PROD.  

 Primero, [!INCLUDE[d365fin](includes/d365fin_md.md)] también actualiza la tabla **Nodo árbol grupo dimensiones** para garantizar que el árbol de búsqueda obedezca al diagrama siguiente. Por lo tanto, el grupo de dimensiones 7 se convierte en un elemento secundario del grupo de dimensiones 5.  

 ![NAV2013; Dimensión; Árbol; Ejemplo 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")  

### <a name="finding-dimension-set-id"></a>Búsqueda del identificador de grupo dimensiones  
 En el nivel conceptual, **Id. principal**, **Dimensión** y **Valor dimensión** en el árbol de búsqueda se agrupan y se utilizan como la clave principal porque [!INCLUDE[d365fin](includes/d365fin_md.md)] atraviesa el árbol en el mismo orden que los movimientos de dimensiones. La función GET (registro) se usa para buscar el identificador del grupo de dimensiones. En el ejemplo de código siguiente se muestra cómo encontrar el identificador del grupo de dimensiones cuando hay tres valores de dimensión.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 No obstante, para mantener la capacidad de [!INCLUDE[d365fin](includes/d365fin_md.md)] de cambiar el nombre de una dimensión y un valor de dimensión, la tabla 348 **Valor dimensión** se amplía con un campo entero de **Id. valor de dimensión**. Esta tabla convierte el par de campos **Dimensión** y **Valor dimensión** en un valor entero. Al cambiar el nombre de la dimensión y del valor de dimensión, no se modifica el valor de entero.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Consulte también  
 [Función GET (Registro)](/dynamics-nav/GET-Function--Record-)    
 [Detalles de diseño: Movimientos de grupo de dimensiones](design-details-dimension-set-entries.md)   
 [Información general de los movimientos del grupo dimensiones](design-details-dimension-set-entries-overview.md)   
 [Detalles de diseño: Estructura de tablas](design-details-table-structure.md)   
 [Detalles de diseño: Gestión de dimensiones de unidad de código 408](design-details-codeunit-408-dimension-management.md)   
 [Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones](design-details-code-examples-of-changed-patterns-in-modifications.md)

