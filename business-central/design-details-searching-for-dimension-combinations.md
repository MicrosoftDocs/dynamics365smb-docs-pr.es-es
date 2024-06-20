---
title: 'Detalles de diseño: Búsqueda de combinaciones de dimensiones | Documentos de Microsoft'
description: 'Cuando se cierra una página después de editar un grupo de dimensiones, Business Central evalúa si existe el grupo de dimensiones editado. Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Detalles de diseño: Búsqueda de combinaciones de dimensiones
Cuando se cierra una página después de editar un grupo de dimensiones, [!INCLUDE[prod_short](includes/prod_short.md)] evalúa si existe el grupo de dimensiones editado. Si no existe el grupo, se crea uno nuevo y se devuelve el identificador de la combinación de dimensiones.  

## Creación de árbol de búsqueda  
 La tabla 481 **Nodo árbol grupo dimensiones** se usa cuando [!INCLUDE[prod_short](includes/prod_short.md)] evalúa si ya existe un conjunto de dimensiones en la tabla 480 **Mov. grupo dimensiones**. La evaluación se realiza de forma recursiva recorriendo el árbol desde el nivel superior con el número 0. El nivel superior 0 representa un grupo de dimensiones sin movimientos de grupo de dimensiones. Los elementos secundarios de este grupo de dimensiones representan los grupos de dimensiones con un solo movimiento de grupo de dimensiones. Los elementos secundarios de estos grupos de dimensiones representan los grupos de dimensiones con dos elementos secundarios, etc.  

### Ejemplo 1  
 En el diagrama siguiente se representa un árbol de búsqueda con seis grupos de dimensiones. En el diagrama solo se muestra el movimiento de grupo de dimensiones de diferenciación.  

 ![Ejemplo de estructura de árbol de dimensiones.](media/nav2013_dimension_tree.png "Ejemplo de estructura de árbol de dimensiones")  

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

### Ejemplo 2  
 En este ejemplo se muestra cómo evalúa [!INCLUDE[prod_short](includes/prod_short.md)] si existe un grupo de dimensiones compuesto por movimientos de grupo de dimensiones AREA 40, DEPT PROD.  

 Primero, [!INCLUDE[prod_short](includes/prod_short.md)] también actualiza la tabla **Nodo árbol grupo dimensiones** para garantizar que el árbol de búsqueda obedezca al diagrama siguiente. Por lo tanto, el grupo de dimensiones 7 se convierte en un elemento secundario del grupo de dimensiones 5.  

 ![Ejemplo de estructura de árbol de dimensiones en NAV 2013.](media/nav2013_dimension_tree_example2.png "Ejemplo de estructura de árbol de dimensiones en NAV 2013")  

### Búsqueda del identificador de grupo dimensiones  
 En el nivel conceptual, **Id. principal**, **Dimensión** y **Valor dimensión** en el árbol de búsqueda se agrupan y se utilizan como la clave principal porque [!INCLUDE[prod_short](includes/prod_short.md)] atraviesa el árbol en el mismo orden que los movimientos de dimensiones. La función GET (registro) se usa para buscar el identificador del grupo de dimensiones. En el ejemplo de código siguiente se muestra cómo encontrar el identificador del grupo de dimensiones cuando hay tres valores de dimensión.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

No obstante, para mantener la capacidad de [!INCLUDE[prod_short](includes/prod_short.md)] de cambiar el nombre tanto de una dimensión como de un valor de dimensión, la tabla 349 **Valor dimensión** se amplía con un campo numérico entero de **Id. valor de dimensión**. Esta tabla convierte el par de campos **Dimensión** y **Valor dimensión** en un valor entero. Al cambiar el nombre de la dimensión y del valor de dimensión, no se modifica el valor de entero.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## Consulte también
    
 [Detalles de diseño: Movimientos de grupo de dimensiones](/dynamics365/business-central/design-details-dimension-set-entries-overview)   
 [Información general de los movimientos del grupo dimensiones](design-details-dimension-set-entries-overview.md)   
 [Detalles de diseño: Estructura de tablas](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]