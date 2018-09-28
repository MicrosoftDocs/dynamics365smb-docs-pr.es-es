---
title: "Detalles de diseño: Gestión de directivas de reaprovisionamiento | Documentos de Microsoft"
description: "Resumen de las tareas de definición de una directiva de reaprovisionamiento de planificación del suministro."
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
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a>Detalles de diseño: Gestión de directivas de reaprovisionamiento
Para que un producto participe en la planificación de aprovisionamiento es necesario definir una directiva de reaprovisionamiento. Existen las cuatro directivas de reaprovisionamiento siguientes:  
  
* Cdad. fija reaprov.  
* Cdad. máxima  
* Pedido  
* Lote a lote  
  
Las directivas Cdad. fija reaprov. y Cdad. máxima están relacionadas con la planificación de inventario. Aunque la planificación del inventario es técnicamente más sencilla que el procedimiento de compensación, estas directivas deben coexistir con el proceso de compensación paso a paso del seguimiento de aprovisionamiento y pedidos. Para controlar la integración entre los dos y proporcionar la información en la lógica de planificación implicada, hay unos principios estrictos que rigen cómo se tratan las directivas de reaprovisionamiento.  
  
## <a name="in-this-section"></a>En esta sección  
[Detalles de diseño: Función del punto de pedido](design-details-the-role-of-the-reorder-point.md)  
[Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de pedido](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Detalles de diseño: Función del ciclo](design-details-the-role-of-the-time-bucket.md)  
[Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento](design-details-staying-under-the-overflow-level.md)  
[Detalles de diseño: Gestión de inventario negativo proyectado](design-details-handling-projected-negative-inventory.md)  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
