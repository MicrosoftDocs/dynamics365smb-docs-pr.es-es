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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e06d91bc1c293e7015af0fe21d918361f322c10d
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="c64fd-103">Detalles de diseño: Gestión de directivas de reaprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="c64fd-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="c64fd-104">Para que un producto participe en la planificación de aprovisionamiento es necesario definir una directiva de reaprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="c64fd-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="c64fd-105">Existen las cuatro directivas de reaprovisionamiento siguientes:</span><span class="sxs-lookup"><span data-stu-id="c64fd-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="c64fd-106">Cdad. fija reaprov.</span><span class="sxs-lookup"><span data-stu-id="c64fd-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="c64fd-107">Cdad. máxima</span><span class="sxs-lookup"><span data-stu-id="c64fd-107">Maximum Qty.</span></span>  
* <span data-ttu-id="c64fd-108">Pedido</span><span class="sxs-lookup"><span data-stu-id="c64fd-108">Order</span></span>  
* <span data-ttu-id="c64fd-109">Lote a lote</span><span class="sxs-lookup"><span data-stu-id="c64fd-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="c64fd-110">Las directivas Cdad. fija reaprov. y Cdad. máxima están relacionadas con la planificación de inventario.</span><span class="sxs-lookup"><span data-stu-id="c64fd-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="c64fd-111">Aunque la planificación del inventario es técnicamente más sencilla que el procedimiento de compensación, estas directivas deben coexistir con el proceso de compensación paso a paso del seguimiento de aprovisionamiento y pedidos.</span><span class="sxs-lookup"><span data-stu-id="c64fd-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="c64fd-112">Para controlar la integración entre los dos y proporcionar la información en la lógica de planificación implicada, hay unos principios estrictos que rigen cómo se tratan las directivas de reaprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="c64fd-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c64fd-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c64fd-113">In This Section</span></span>  
[<span data-ttu-id="c64fd-114">Detalles de diseño: Función del punto de pedido</span><span class="sxs-lookup"><span data-stu-id="c64fd-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="c64fd-115">Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de pedido</span><span class="sxs-lookup"><span data-stu-id="c64fd-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="c64fd-116">Detalles de diseño: Función del ciclo</span><span class="sxs-lookup"><span data-stu-id="c64fd-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="c64fd-117">Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="c64fd-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="c64fd-118">Detalles de diseño: Gestión de inventario negativo proyectado</span><span class="sxs-lookup"><span data-stu-id="c64fd-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="c64fd-119">Detalles de diseño: Directivas de reaprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="c64fd-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="c64fd-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c64fd-120">See Also</span></span>  
<span data-ttu-id="c64fd-121">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="c64fd-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="c64fd-122">[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="c64fd-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="c64fd-123">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="c64fd-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="c64fd-124">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="c64fd-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="c64fd-125">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="c64fd-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
