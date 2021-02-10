---
title: Cómo hacer un seguimiento de las relaciones entre demanda y suministro | Documentos de Microsoft
description: Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25eed1edd8aeb92c875e093a177e59c40d3c3a12
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758924"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="7ba42-103">Realizar un seguimiento de las relaciones entre demanda y suministro</span><span class="sxs-lookup"><span data-stu-id="7ba42-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="7ba42-104">Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión.</span><span class="sxs-lookup"><span data-stu-id="7ba42-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="7ba42-105">Las hojas de planificación también presentan información de planificación complementaria, acerca de entidades sin pedidos para ayudar al planificador a elaborar un plan de suministro óptimo.</span><span class="sxs-lookup"><span data-stu-id="7ba42-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="7ba42-106">Para obtener más información, consulte [Elementos de planificación sin seguimiento](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="7ba42-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="7ba42-107">Para seguir productos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ba42-107">To track linked items</span></span>
<span data-ttu-id="7ba42-108">El seguimiento de pedidos muestra cómo se relacionan los pedidos de venta, las órdenes de producción y los pedidos de compra con las órdenes de fabricación en los sistemas de planificación y reservas.</span><span class="sxs-lookup"><span data-stu-id="7ba42-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="7ba42-109">A continuación se describe cómo seguir productos asociados en una orden de producción planificada en firme.</span><span class="sxs-lookup"><span data-stu-id="7ba42-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="7ba42-110">Los pasos son parecidos a los de todos los tipos de pedidos y planificación de las líneas de hoja de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7ba42-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="7ba42-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Orden produc. planif. en firme** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="7ba42-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="7ba42-112">Abra la orden de producción planificada en firme pertinente de la lista.</span><span class="sxs-lookup"><span data-stu-id="7ba42-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="7ba42-113">En la ficha desplegable **Líneas**, elija la acción **Funciones** y, a continuación, seleccione la acción **Seguimiento de pedido**.</span><span class="sxs-lookup"><span data-stu-id="7ba42-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="7ba42-114">Las líneas de **Seguimiento de pedido** muestran los documentos que están relacionados con la línea de pedido de producción actual.</span><span class="sxs-lookup"><span data-stu-id="7ba42-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="7ba42-115">Elementos planificación sin seguimiento</span><span class="sxs-lookup"><span data-stu-id="7ba42-115">Untracked Planning Elements</span></span>
<span data-ttu-id="7ba42-116">Se abre la página **Elementos de planificación sin seguimiento** cuando elige el campo **Cantidad sin seguimiento** en la página **Planificación de pedidos**.</span><span class="sxs-lookup"><span data-stu-id="7ba42-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="7ba42-117">Responde a dos propósitos:</span><span class="sxs-lookup"><span data-stu-id="7ba42-117">It serves two purposes:</span></span>

1. <span data-ttu-id="7ba42-118">Albergar información sobre cantidades sin seguimiento que se muestran cuando el usuario busca desde la página Seguimiento pedido las cantidades sin seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7ba42-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="7ba42-119">Albergar los mensajes de advertencia que se muestran cuando el usuario selecciona el icono de **Advertencia** en la página **Hoja de planificación**.</span><span class="sxs-lookup"><span data-stu-id="7ba42-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="7ba42-120">La página contiene entradas que contabilizan la cantidad de excedentes sin seguimiento con el objeto de realizar un seguimiento de la red.</span><span class="sxs-lookup"><span data-stu-id="7ba42-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="7ba42-121">Estas entradas se generan durante la ejecución de la planificación y explican la procedencia de dicha cantidad en las líneas de seguimiento de pedido.</span><span class="sxs-lookup"><span data-stu-id="7ba42-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="7ba42-122">La procedencia de este excedente sin seguimiento puede ser:</span><span class="sxs-lookup"><span data-stu-id="7ba42-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="7ba42-123">Previsión de producción</span><span class="sxs-lookup"><span data-stu-id="7ba42-123">Production forecast</span></span>
- <span data-ttu-id="7ba42-124">Pedidos abiertos</span><span class="sxs-lookup"><span data-stu-id="7ba42-124">Blanket orders</span></span>
- <span data-ttu-id="7ba42-125">Stock de seguridad</span><span class="sxs-lookup"><span data-stu-id="7ba42-125">Safety stock quantity</span></span>
- <span data-ttu-id="7ba42-126">Punto de pedido</span><span class="sxs-lookup"><span data-stu-id="7ba42-126">Reorder point</span></span>
- <span data-ttu-id="7ba42-127">Stock máximo</span><span class="sxs-lookup"><span data-stu-id="7ba42-127">Maximum inventory</span></span>
- <span data-ttu-id="7ba42-128">Cantidad a solicitar</span><span class="sxs-lookup"><span data-stu-id="7ba42-128">Reorder quantity</span></span>
- <span data-ttu-id="7ba42-129">Cantidad máxima pedido</span><span class="sxs-lookup"><span data-stu-id="7ba42-129">Maximum order quantity</span></span>
- <span data-ttu-id="7ba42-130">Cantidad mínima pedido</span><span class="sxs-lookup"><span data-stu-id="7ba42-130">Minimum order quantity</span></span>
- <span data-ttu-id="7ba42-131">Múltiplos de pedido</span><span class="sxs-lookup"><span data-stu-id="7ba42-131">Order multiple</span></span>
- <span data-ttu-id="7ba42-132">Amort. (% tamaño lote)</span><span class="sxs-lookup"><span data-stu-id="7ba42-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="7ba42-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ba42-133">See Also</span></span>  
<span data-ttu-id="7ba42-134">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7ba42-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="7ba42-135">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="7ba42-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7ba42-136">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7ba42-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7ba42-137">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="7ba42-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7ba42-138">Compras</span><span class="sxs-lookup"><span data-stu-id="7ba42-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7ba42-139">Detalles de diseño: Reserva, seguimiento y mensajes de acciones</span><span class="sxs-lookup"><span data-stu-id="7ba42-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="7ba42-140">[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7ba42-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="7ba42-141">Procedimientos recomendados de configuración: planificación de suministros</span><span class="sxs-lookup"><span data-stu-id="7ba42-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="7ba42-142">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7ba42-142">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
