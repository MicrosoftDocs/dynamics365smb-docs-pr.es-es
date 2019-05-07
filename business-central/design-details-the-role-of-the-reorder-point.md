---
title: 'Detalles de diseño: Función del punto de pedido | Documentos de Microsoft'
description: En este tema se destaca la importancia de establecer el punto de pedido, de forma que sepa cuándo solicitar más inventario.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "924192"
---
# <a name="design-details-the-role-of-the-reorder-point"></a>Detalles de diseño: Función del punto de pedido
Además del equilibrado general de la oferta y la demanda, el sistema de planificación debe supervisar los niveles de inventario para que los productos afectados respeten las directivas de pedido definidas.  

Un punto de pedido representa la demanda durante un plazo de entrega. Cuando el inventario proyectado está por debajo del nivel de inventario definido por el punto de pedido, ha llegado el momento de pedir más cantidad. Mientras tanto, se prevé que el inventario se reduzca gradualmente y posiblemente alcance cero (o el nivel de stock de seguridad), hasta que llegue la reposición.  

Por consiguiente, el sistema de planificación sugerirá un pedido de suministros de programación anticipada en el momento en el que el inventario proyectado quede por debajo del punto de reaprovisionamiento.  

El punto de pedido refleja un determinado nivel de inventario. No obstante, los niveles de inventario pueden variar significativamente durante el ciclo y, por tanto, el sistema de planificación debe supervisar constantemente el inventario disponible proyectado.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
