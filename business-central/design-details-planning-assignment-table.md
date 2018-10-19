---
title: "Detalles de diseño: Tabla de asignación de planificación | Documentos de Microsoft"
description: "Este tema proporciona una perspectiva de qué ocurre cuando se modifica la forma en que realiza un plan para un producto."
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
ms.openlocfilehash: 9a1661d71bd28009a0c0b83a50e27cae3c833ea7
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="e568f-103">Detalles de diseño: Tabla de asignación de planificación</span><span class="sxs-lookup"><span data-stu-id="e568f-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="e568f-104">Todos los productos se deben planificar; no obstante, no hay razón para calcular un plan para un producto a menos que haya habido un cambio en el patrón de demanda o de aprovisionamiento desde la última vez que se calculó un plan.</span><span class="sxs-lookup"><span data-stu-id="e568f-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  

<span data-ttu-id="e568f-105">Si el usuario ha introducido un nuevo pedido de venta o ha cambiado uno existente, existen motivos para volver a calcular el plan.</span><span class="sxs-lookup"><span data-stu-id="e568f-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="e568f-106">Entre otros motivos se incluye un cambio en la previsión o en el stock de seguridad deseado.</span><span class="sxs-lookup"><span data-stu-id="e568f-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="e568f-107">Un cambio en una lista de materiales mediante la adición o eliminación de un componente indicaría probablemente un cambio, pero para el producto componente solo.</span><span class="sxs-lookup"><span data-stu-id="e568f-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  

<span data-ttu-id="e568f-108">En el caso de ubicaciones múltiples, la asignación se realiza en el nivel de producto por combinación de almacén.</span><span class="sxs-lookup"><span data-stu-id="e568f-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="e568f-109">Si, por ejemplo, se ha creado un pedido de venta en solo una ubicación, el programa asignará el producto a esa ubicación específica para planificar.</span><span class="sxs-lookup"><span data-stu-id="e568f-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  

<span data-ttu-id="e568f-110">El motivo para seleccionar productos para la planificación es cuestión de rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="e568f-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="e568f-111">Si no se ha producido ningún cambio en el patrón de demanda-aprovisionamiento de un producto, el sistema de planificación no sugerirá ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="e568f-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="e568f-112">Sin la asignación de planificación, el sistema tendría que realizar cálculos para todos los productos a fin de averiguar para qué debe planificar y lo que agotaría los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="e568f-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  

<span data-ttu-id="e568f-113">La tabla **Asignar planificación** supervisa los eventos de demanda y aprovisionamiento y asigna los productos adecuados para realizar la planificación.</span><span class="sxs-lookup"><span data-stu-id="e568f-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="e568f-114">Se supervisan los eventos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e568f-114">The following events are monitored:</span></span>  

* <span data-ttu-id="e568f-115">Un nuevo pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e568f-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="e568f-116">Cambio de un pedido, cantidad, almacén, variante o fecha en un pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e568f-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="e568f-117">Cancelación de un pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.</span><span class="sxs-lookup"><span data-stu-id="e568f-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="e568f-118">El consumo de productos distintos de los planificados.</span><span class="sxs-lookup"><span data-stu-id="e568f-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="e568f-119">Salida de productos distintos de los planificados.</span><span class="sxs-lookup"><span data-stu-id="e568f-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="e568f-120">Cambios en inventario no planificados.</span><span class="sxs-lookup"><span data-stu-id="e568f-120">Unplanned changes in inventory.</span></span>  

<span data-ttu-id="e568f-121">Para estas desubicaciones de aprovisionamiento y demanda directos, el sistema de mensajes de acción y de seguimiento de pedidos mantiene la tabla de asignación de planificación e indica una causa de planificación como mensaje de acción.</span><span class="sxs-lookup"><span data-stu-id="e568f-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  

<span data-ttu-id="e568f-122">Los siguientes cambios en los datos maestros también pueden provocar un desequilibrio de planificación:</span><span class="sxs-lookup"><span data-stu-id="e568f-122">The following changes in master data can also cause a planning imbalance:</span></span>  

* <span data-ttu-id="e568f-123">Cambio del estado a certificado en cabecera de L.M. de producción (para todos los productos con esa cabecera).</span><span class="sxs-lookup"><span data-stu-id="e568f-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="e568f-124">Línea eliminada (producto secundario).</span><span class="sxs-lookup"><span data-stu-id="e568f-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="e568f-125">Cambio del estado a certificado en cabecera de ruta (para todos los productos con esa ruta).</span><span class="sxs-lookup"><span data-stu-id="e568f-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="e568f-126">Cambios en los campos de ficha de producto siguientes.</span><span class="sxs-lookup"><span data-stu-id="e568f-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="e568f-127">Stock de seguridad o plazo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e568f-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="e568f-128">Plazo entrega (días).</span><span class="sxs-lookup"><span data-stu-id="e568f-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="e568f-129">Punto de pedido.</span><span class="sxs-lookup"><span data-stu-id="e568f-129">Reorder Point.</span></span>  
* <span data-ttu-id="e568f-130">Número de L.M. de producción (y todos los elementos secundarios de referencia de la L.M. anterior).</span><span class="sxs-lookup"><span data-stu-id="e568f-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="e568f-131">Nº ruta</span><span class="sxs-lookup"><span data-stu-id="e568f-131">Routing No.</span></span>  
* <span data-ttu-id="e568f-132">Directiva reaprov.</span><span class="sxs-lookup"><span data-stu-id="e568f-132">Reordering Policy.</span></span>  

<span data-ttu-id="e568f-133">En estos casos, una nueva función, la de gestión de planificación de asignaciones, mantiene la tabla e indica la causa de la planificación como Saldos periodo.</span><span class="sxs-lookup"><span data-stu-id="e568f-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  

<span data-ttu-id="e568f-134">Los siguientes cambios no provocan una asignación de planificación:</span><span class="sxs-lookup"><span data-stu-id="e568f-134">The following changes do not cause a planning assignment:</span></span>  

* <span data-ttu-id="e568f-135">Calendarios</span><span class="sxs-lookup"><span data-stu-id="e568f-135">Calendars</span></span>  
* <span data-ttu-id="e568f-136">Otros parámetros de planificación en la ficha de producto</span><span class="sxs-lookup"><span data-stu-id="e568f-136">Other planning parameters on the item card</span></span>  

<span data-ttu-id="e568f-137">Al calcular un MPS o un MRP, se aplican las siguientes restricciones:</span><span class="sxs-lookup"><span data-stu-id="e568f-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  

* <span data-ttu-id="e568f-138">MPS: el sistema de planificación comprueba que el producto incluye una previsión de demanda o un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="e568f-138">MPS: The planning system checks that the item carries a demand forecast or a sales order.</span></span> <span data-ttu-id="e568f-139">Si no, el producto no se incluye en el plan.</span><span class="sxs-lookup"><span data-stu-id="e568f-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="e568f-140">MRP: si el sistema de planificación detecta que el producto se repone mediante una línea de planificación MPS o un pedido de suministro MRP, el producto quedará fuera de la planificación.</span><span class="sxs-lookup"><span data-stu-id="e568f-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="e568f-141">No obstante, se incluyen las demandas de los componentes relevantes.</span><span class="sxs-lookup"><span data-stu-id="e568f-141">However, any demand from relevant components is included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e568f-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e568f-142">See Also</span></span>  
<span data-ttu-id="e568f-143">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="e568f-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="e568f-144">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="e568f-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="e568f-145">[Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e568f-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="e568f-146">Detalles de diseño: Parámetros de la planificación</span><span class="sxs-lookup"><span data-stu-id="e568f-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  

