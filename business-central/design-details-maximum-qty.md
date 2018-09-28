---
title: "Detalles de diseño: Cantidad máxima | Documentos de Microsoft"
description: "La directiva de cantidad máxima es una forma de mantener el inventario mediante un punto de pedido."
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
ms.openlocfilehash: e35a9269cab0449967889a7c40c1bb831e023cf7
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-maximum-qty"></a><span data-ttu-id="1317e-103">Detalles de diseño: Cantidad máxima</span><span class="sxs-lookup"><span data-stu-id="1317e-103">Design Details: Maximum Qty.</span></span>
<span data-ttu-id="1317e-104">La directiva de cantidad máxima es una forma de mantener el inventario mediante un punto de pedido.</span><span class="sxs-lookup"><span data-stu-id="1317e-104">The Maximum Quantity policy is a way to maintain inventory using a reorder point.</span></span>  
  
 <span data-ttu-id="1317e-105">También se aplica a esta directiva todo lo relacionado con la directiva de cantidad de reaprovisionamiento fija.</span><span class="sxs-lookup"><span data-stu-id="1317e-105">Everything regarding the Fixed Reorder Qty. policy also applies to this policy.</span></span> <span data-ttu-id="1317e-106">La única diferencia es la cantidad del suministro sugerido.</span><span class="sxs-lookup"><span data-stu-id="1317e-106">The only difference is the quantity of the suggested supply.</span></span> <span data-ttu-id="1317e-107">Al usar la directiva de cantidad máxima, la cantidad del nuevo pedido se definirá dinámicamente según el nivel de inventario proyectado y, por lo tanto, normalmente será distinta de un pedido a otro.</span><span class="sxs-lookup"><span data-stu-id="1317e-107">When using the maximum quantity policy, the reorder quantity will be defined dynamically based on the projected inventory level and will therefore usually differ from order to order.</span></span>  
  
## <a name="calculated-per-time-bucket"></a><span data-ttu-id="1317e-108">Calculado por ciclo</span><span class="sxs-lookup"><span data-stu-id="1317e-108">Calculated per Time Bucket</span></span>  
 <span data-ttu-id="1317e-109">La cantidad a pedir se actualmente en el momento (el final de un ciclo) en el que el sistema de planificación detecta que se ha superado el punto de pedido.</span><span class="sxs-lookup"><span data-stu-id="1317e-109">The reorder quantity is determined at the point of time (the end of a time bucket) when the planning system detects that the reorder point has been crossed.</span></span> <span data-ttu-id="1317e-110">En este punto, el programa mide la diferencia entre el nivel de inventario proyectado actual y el inventario máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="1317e-110">At this time, the system measures the gap from the current projected inventory level up to the specified maximum inventory.</span></span> <span data-ttu-id="1317e-111">Esto constituye la cantidad que se debe volver a pedir.</span><span class="sxs-lookup"><span data-stu-id="1317e-111">This constitutes the quantity that should be reordered.</span></span> <span data-ttu-id="1317e-112">A continuación, el sistema comprueba si el suministro ya se ha pedido en otra parte para recibirse en el plazo y, en caso afirmativo, reduce la cantidad del nuevo pedido de suministro en las cantidades ya pedidas.</span><span class="sxs-lookup"><span data-stu-id="1317e-112">The system then checks if supply has already been ordered elsewhere to be received within the lead time and, if so, reduces the quantity of the new supply order by already ordered quantities.</span></span>  
  
 <span data-ttu-id="1317e-113">El programa garantizará que el inventario proyectado llegue como mínimo al nivel de punto de pedido como mínimo, en el caso de que el usuario haya olvidado especificar una cantidad de inventario máxima.</span><span class="sxs-lookup"><span data-stu-id="1317e-113">The system will ensure that the projected inventory at least reaches the reorder point level – in case the user has forgotten to specify a maximum inventory quantity.</span></span>  
  
## <a name="combines-with-order-modifiers"></a><span data-ttu-id="1317e-114">Combina con modificadores de pedido</span><span class="sxs-lookup"><span data-stu-id="1317e-114">Combines with Order Modifiers</span></span>  
 <span data-ttu-id="1317e-115">Dependiendo de la configuración, puede ser mejor agrupar la directiva de cantidad máxima con modificadores de pedido para garantizar una cantidad de pedido mínima o redondearla a un número entero de unidades de medida de compra, o dividirla en más lotes según lo definido en la cantidad de pedido máxima.</span><span class="sxs-lookup"><span data-stu-id="1317e-115">Depending on the setup, it may be best to combine the Maximum Quantity policy with order modifiers to ensure a minimum order quantity or round it to an integer number of purchase units of measure, or split it into more lots as defined by the maximum order quantity.</span></span>  
  
## <a name="combines-with-calendars"></a><span data-ttu-id="1317e-116">Combina con Calendarios</span><span class="sxs-lookup"><span data-stu-id="1317e-116">Combines with Calendars</span></span>  
 <span data-ttu-id="1317e-117">Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el pedido está programado para un día no laborable, según los calendarios definidos en el campo **Código calendario base** en las ventanas **Información empresa** y **Ficha almacén**.</span><span class="sxs-lookup"><span data-stu-id="1317e-117">Before suggesting a new supply order to meet a reorder point, the planning system checks if the order is scheduled for a non-working day, according to any calendars that are  defined in the **Base Calendar Code** field in the **Company Information** and **Location Card** windows.</span></span>  
  
 <span data-ttu-id="1317e-118">Si la fecha programada es un día no laborable, el sistema de planificación mueve el pedido al próximo día laborable.</span><span class="sxs-lookup"><span data-stu-id="1317e-118">If the scheduled date is a non-working day, the planning system moves the order forward to the nearest working date.</span></span> <span data-ttu-id="1317e-119">Esto puede dar lugar a un pedido que cumpla con el punto de pedido pero que no cumpla una demanda específica.</span><span class="sxs-lookup"><span data-stu-id="1317e-119">This may result in an order that meets a reorder point but does not meet some specific demand.</span></span> <span data-ttu-id="1317e-120">Para este tipo de demandas sin saldar, el sistema de planificación crea un suministro extra.</span><span class="sxs-lookup"><span data-stu-id="1317e-120">For such unbalanced demand, the planning system creates an extra supply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1317e-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1317e-121">See Also</span></span>  
 <span data-ttu-id="1317e-122">[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1317e-122">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="1317e-123">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="1317e-123">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="1317e-124">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1317e-124">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="1317e-125">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="1317e-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
