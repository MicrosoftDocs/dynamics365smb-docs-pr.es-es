---
title: 'Detalles de diseño: Gestión de pedidos antes de la fecha de inicio de la planificación | Documentos de Microsoft'
description: En este tema se describen las reglas que la planificación aplica a los pedidos en la zona congelada.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 9fee9eff60b441ef2d4782a77a6fbbbe8b01af03
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806261"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="b4587-103">Detalles de diseño: Gestión de pedidos antes de la fecha de inicio de planificación</span><span class="sxs-lookup"><span data-stu-id="b4587-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="b4587-104">Para evitar que un plan de suministro muestre sugerencias imposibles y, por tanto, de poca utilidad, el sistema de planificación considera el periodo hasta la fecha inicial como una zona congelada donde no hay nada planificado.</span><span class="sxs-lookup"><span data-stu-id="b4587-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="b4587-105">La regla siguiente se aplica a la zona congelada:</span><span class="sxs-lookup"><span data-stu-id="b4587-105">The following rule applies to the frozen zone:</span></span>  

<span data-ttu-id="b4587-106">Toda la demanda y aprovisionamiento antes de la fecha de inicio del periodo de planificación se tendrá como parte del inventario o enviado.</span><span class="sxs-lookup"><span data-stu-id="b4587-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  

<span data-ttu-id="b4587-107">Por consiguiente, el sistema de planificación, salvo algunas excepciones, no sugerirá ningún cambio en los pedidos de aprovisionamiento en la zona congelada, y no se creará ni se guardará ningún vínculo de seguimiento de pedidos para ese periodo.</span><span class="sxs-lookup"><span data-stu-id="b4587-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  

<span data-ttu-id="b4587-108">Las excepciones a esta regla son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b4587-108">The exceptions to this rule are as follows:</span></span>  

* <span data-ttu-id="b4587-109">Si el inventario disponible proyectado, incluida la suma de aprovisionamiento y la demanda en la zona congelada, es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="b4587-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="b4587-110">Si hacen falta números de serie o lote en los pedidos con fecha anterior.</span><span class="sxs-lookup"><span data-stu-id="b4587-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="b4587-111">Si el conjunto de aprovisionamiento y demanda se vincula por una directiva de pedido a pedido.</span><span class="sxs-lookup"><span data-stu-id="b4587-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  

<span data-ttu-id="b4587-112">Si el inventario disponible inicial es menor que cero, el sistema de planificación sugiere un pedido de aprovisionamiento de emergencia el día antes del periodo de planificación para cubrir la cantidad que falta.</span><span class="sxs-lookup"><span data-stu-id="b4587-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="b4587-113">Por tanto, el inventario proyectado y disponible será siempre al menos cero cuando empiece la planificación para el periodo futuro.</span><span class="sxs-lookup"><span data-stu-id="b4587-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="b4587-114">La línea de planificación de este pedido de suministro mostrará un icono de advertencia de emergencia y, tras la búsqueda, se proporciona información adicional.</span><span class="sxs-lookup"><span data-stu-id="b4587-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="b4587-115">Los números de serie y de lote y las conexiones de pedido contra pedido están exentos de la zona congelada</span><span class="sxs-lookup"><span data-stu-id="b4587-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="b4587-116">Si se requieren números de serie y de lote o si hay un vínculo de pedido a pedido, el sistema de planificación no tendrá en cuenta la zona congelada e incorporará estas cantidades con fecha anterior a partir de la fecha de inicio y potencialmente propondrá acciones correctivas si la demanda y el aprovisionamiento no están sincronizados.</span><span class="sxs-lookup"><span data-stu-id="b4587-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="b4587-117">El motivo empresarial de este principio es que dichos conjuntos de demanda-suministro específicos deben coincidir para garantizar que se cumple esta demanda específica.</span><span class="sxs-lookup"><span data-stu-id="b4587-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b4587-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b4587-118">See Also</span></span>  
<span data-ttu-id="b4587-119">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="b4587-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="b4587-120">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="b4587-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="b4587-121">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="b4587-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
