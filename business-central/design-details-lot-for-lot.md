---
title: 'Detalles de diseño: Lote por lote | Documentos de Microsoft'
description: Aprender cómo utilizar la directiva de lote por lote para establecer la cantidad del pedido basada en la demanda.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 5669378383d94b33a25a60a882709885e1463a6d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303110"
---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="3be9d-103">Detalles de diseño: Lote por lote</span><span class="sxs-lookup"><span data-stu-id="3be9d-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="3be9d-104">La directiva de lote por lote es la más flexible porque el sistema solo reacciones ante la demanda real, además de actuar ante la demanda anticipada de los pedidos de previsión y abiertos; a continuación, liquida la cantidad del pedido según la demanda.</span><span class="sxs-lookup"><span data-stu-id="3be9d-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="3be9d-105">La directiva de lote por lote está dirigida a los productos A y B, donde el inventario se puede aceptar pero se debe evitar.</span><span class="sxs-lookup"><span data-stu-id="3be9d-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  

<span data-ttu-id="3be9d-106">De algún modo, la directiva del lote por lote se parece a la directiva de pedido, pero su acercamiento a los productos es genérico; puede aceptar cantidades en el inventario y une demandas con aprovisionamientos correspondientes en ciclos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3be9d-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  

<span data-ttu-id="3be9d-107">El ciclo se define en el campo **Ciclo**.</span><span class="sxs-lookup"><span data-stu-id="3be9d-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="3be9d-108">El programa trabaja con un ciclo mínimo de un día, ya que es la unidad de medida de tiempo menor en los eventos de demanda y de suministro del sistema (aunque, en la práctica, la unidad de medida de tiempo en las órdenes de producción y las necesidades de componentes puede ser segundos).</span><span class="sxs-lookup"><span data-stu-id="3be9d-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  

<span data-ttu-id="3be9d-109">El ciclo también establece límites con respecto a cuándo se debe reprogramar un pedido de suministro existente para cubrir una demanda determinada.</span><span class="sxs-lookup"><span data-stu-id="3be9d-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="3be9d-110">Si el aprovisionamiento entra dentro del ciclo, se volverá a programar dentro o fuera para cubrir la demanda.</span><span class="sxs-lookup"><span data-stu-id="3be9d-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="3be9d-111">De lo contrario, si es anterior, se producirá una acumulación innecesaria del inventario y se debe cancelar.</span><span class="sxs-lookup"><span data-stu-id="3be9d-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="3be9d-112">Si es posterior, se creará un nuevo pedido de aprovisionamiento en su lugar.</span><span class="sxs-lookup"><span data-stu-id="3be9d-112">If it lies later, a new supply order will be created instead.</span></span>  

<span data-ttu-id="3be9d-113">Con esta directiva, también se puede definir un stock de seguridad para compensar las fluctuaciones posibles en el suministro, o para satisfacer la demanda repentina.</span><span class="sxs-lookup"><span data-stu-id="3be9d-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  

<span data-ttu-id="3be9d-114">Dado que la cantidad del pedido de aprovisionamiento se basa en la demanda real, puede tener sentido usar los modificadores de pedido: redondear la cantidad del pedido para satisfacer un múltiplo de pedido especificado (o unidad de medida de compra), incrementar el pedido a una cantidad mínima especificada o disminuir la cantidad máxima especificada (y crear así dos aprovisionamientos o más para alcanzar la cantidad total necesaria).</span><span class="sxs-lookup"><span data-stu-id="3be9d-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  

## <a name="see-also"></a><span data-ttu-id="3be9d-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3be9d-115">See Also</span></span>  
<span data-ttu-id="3be9d-116">[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3be9d-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="3be9d-117">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="3be9d-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="3be9d-118">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="3be9d-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="3be9d-119">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="3be9d-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
