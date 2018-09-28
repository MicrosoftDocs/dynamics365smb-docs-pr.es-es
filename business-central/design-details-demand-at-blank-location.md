---
title: "Detalles de diseño: Aprovisionamiento y demanda | Documentos de Microsoft"
description: "Este tema introduce el concepto de demanda, que es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 492c3edbf6b720e4d297739d6f8c478ca79c82df
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-demand-and-supply"></a>Detalles de diseño: Demanda y aprovisionamiento
"Demanda" es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción. Además, el programa permite tipos de demanda más técnicos, como inventario negativo y devoluciones de compra.  
  
Suministro es el término habitual que se usa para cualquier tipo de cantidad positiva o de entrada, como inventario, compras, ensamblado, producción o transferencias de entrada. Además, una devolución de ventas también puede representar un aprovisionamiento.  
  
Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario. Un perfil contiene eventos de demanda y el otro incluye los eventos de suministro correspondientes. Cada evento representa una entidad de red de pedidos, como una línea de pedido de venta, un movimiento de producto o una línea de orden de producción.  
  
Cuando se cargan los perfiles de inventario, se equilibran los distintos conjuntos de demanda-suministro para generar un plan de suministro que cumpla los objetivos enumerados.  
  
Los parámetros de planificación y los niveles de inventario son otros tipos de demanda y suministro respectivamente, en los que se realizará una contrapartida integrada para reponer los productos en existencias. Para obtener más información, consulte [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
