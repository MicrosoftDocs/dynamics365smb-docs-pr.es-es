---
title: 'Detalles de diseño: Función del ciclo | Documentos de Microsoft'
description: El propósito del ciclo es recopilar los eventos de demanda dentro del intervalo de tiempo para crear un pedido de suministro conjunto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 54d4a4aed94b562b82d94d6a5a75a3050c054fc3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239319"
---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="fecfe-103">Detalles de diseño: Función del ciclo</span><span class="sxs-lookup"><span data-stu-id="fecfe-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="fecfe-104">El propósito del ciclo es recopilar los eventos de demanda dentro del intervalo de tiempo para crear un pedido de suministro conjunto.</span><span class="sxs-lookup"><span data-stu-id="fecfe-104">The purpose of the time bucket is to collect demand events within the time page in order to make a joint supply order.</span></span>  

 <span data-ttu-id="fecfe-105">En el caso de directivas de reaprovisionamiento que utilizan un punto de pedido se puede definir un ciclo.</span><span class="sxs-lookup"><span data-stu-id="fecfe-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="fecfe-106">De este modo se garantiza que se acumula la demanda en el mismo periodo de tiempo antes de comprobar el impacto en el inventario proyectado y si se ha superado el último punto de pedido.</span><span class="sxs-lookup"><span data-stu-id="fecfe-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="fecfe-107">Si se sobrepasa el punto de pedido, se programa de forma anticipada un nuevo pedido de aprovisionamiento desde el final del periodo definido por el ciclo.</span><span class="sxs-lookup"><span data-stu-id="fecfe-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="fecfe-108">Los ciclos comienzan en la fecha inicial de planificación.</span><span class="sxs-lookup"><span data-stu-id="fecfe-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="fecfe-109">El concepto por ciclos refleja el proceso manual de comprobación del nivel de inventario de un modo frecuente en vez de hacerlo por cada transacción.</span><span class="sxs-lookup"><span data-stu-id="fecfe-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="fecfe-110">El usuario debe definir la frecuencia (el ciclo).</span><span class="sxs-lookup"><span data-stu-id="fecfe-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="fecfe-111">Por ejemplo, el usuario recopila todas las exigencias de producto de un proveedor para hacer un pedido semanal.</span><span class="sxs-lookup"><span data-stu-id="fecfe-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="fecfe-112">![Ejemplo de ciclo en la planificación](media/nav_app_supply_planning_2_reorder_cycle.png "Ejemplo de ciclo en la planificación")</span><span class="sxs-lookup"><span data-stu-id="fecfe-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="fecfe-113">Por lo general, el ciclo se usa para evitar un efecto de cascada.</span><span class="sxs-lookup"><span data-stu-id="fecfe-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="fecfe-114">Por ejemplo, una fila equilibrada de demanda y aprovisionamiento donde se cancela una demanda temprana, o se crea una nueva.</span><span class="sxs-lookup"><span data-stu-id="fecfe-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="fecfe-115">El resultado podría ser que se programe cada pedido de suministro (sin incluir el último).</span><span class="sxs-lookup"><span data-stu-id="fecfe-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fecfe-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fecfe-116">See Also</span></span>  
 <span data-ttu-id="fecfe-117">[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fecfe-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="fecfe-118">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="fecfe-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="fecfe-119">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fecfe-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="fecfe-120">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="fecfe-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
