---
title: "Configuración de filtros para las bases de la asignación dinámica | Documentos de Microsoft"
description: "El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de coste o los productos vendidos de un objeto de coste en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ca8e7008c2bfe4a9abeb9d9b7b467a38e2c1971
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Configuración de filtros para las bases de la asignación dinámica
El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de coste o los productos vendidos de un objeto de coste en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Configuración de filtros para las bases de la asignación dinámica  
 La siguiente tabla muestra qué filtros son posibles para distintas bases de asignación y qué valores son válidos en los campos **Filtro nº** y **Filtro grupo**. Presione F1 en el campo **Filtro fecha vto.** para leer descripciones detalladas.  

|**Base**|**Filtro Nº**|**Filtro fecha vto.**|**Filtro centro coste**|**Filtro objeto coste**|**Filtro grupo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Movimientos de contabilidad|Cuenta|Sí|Sí|Sí|N/D|  
|Movs. pptos. contabilidad|Cuenta|Sí|Sí|Sí|Nombres pptos. contabilidad|  
|Movimientos de tipo de coste|Tipo de coste|Sí|Sí|Sí|N/D|  
|Movs. ppto. costes|Tipo de coste|Sí|Sí|Sí|Nombre ppto.|  
|Nº de empleados|N/D|Sí|Sí|Sí|N/D|  
|Productos vendidos (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos comprados (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos vendidos (importe)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos comprados (importe)|N.º producto|Sí|Sí|Sí|Grupo contable inventario|  

## <a name="see-also"></a>Consulte también  
 [Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definición y asignación de costes](finance-define-and-allocate-costs.md)

