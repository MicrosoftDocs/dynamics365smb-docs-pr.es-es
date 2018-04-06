---
title: "Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento | Documentos de Microsoft"
description: "Cuando se usa Cdad. máxima y Cdad. fija reaprov., el sistema de planificación se centra en el inventario proyectado únicamente en el ciclo indicado. Esto significa que el sistema de planificación puede sugerir un suministro superfluo cuando se producen cambios de demanda negativa o de suministro positivo fuera del ciclo determinado."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="8d00d-104">Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="8d00d-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="8d00d-105">Cuando se usan políticas de cantidad máxima y cantidad fija, el sistema de planificación se centra en el inventario proyectado únicamente en el ciclo indicado.</span><span class="sxs-lookup"><span data-stu-id="8d00d-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="8d00d-106">Esto significa que el sistema de planificación puede sugerir un suministro superfluo cuando se producen cambios de demanda negativa o de suministro positivo fuera del ciclo determinado.</span><span class="sxs-lookup"><span data-stu-id="8d00d-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="8d00d-107">Si, por esta razón, se sugiere un aprovisionamiento superfluo, el sistema de planificación calcula qué cantidad de aprovisionamiento debe disminuirse (o eliminarse) para evitar un aprovisionamiento superfluo.</span><span class="sxs-lookup"><span data-stu-id="8d00d-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="8d00d-108">Esta cantidad se denomina “nivel de desbordamiento.”</span><span class="sxs-lookup"><span data-stu-id="8d00d-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="8d00d-109">El desbordamiento se comunica como una línea de planificación con una acción de **Cambiar cantidad. (salida)** o **Cancelar** y el mensaje de advertencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="8d00d-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="8d00d-110">*Atención: El inventario proyectado [xx] es superior al nivel de desbordamiento [xx] en la fecha de vencimiento [xx].*</span><span class="sxs-lookup"><span data-stu-id="8d00d-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="8d00d-111">![Nivel de desbordamiento de inventario](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="8d00d-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="8d00d-112">Cálculo del nivel de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="8d00d-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="8d00d-113">El nivel de desbordamiento se calcula de diferentes modos según la configuración de planificación.</span><span class="sxs-lookup"><span data-stu-id="8d00d-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="8d00d-114">Directiva de reaprovisionamiento de cantidad máxima</span><span class="sxs-lookup"><span data-stu-id="8d00d-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="8d00d-115">Nivel de desbordamiento = stock máximo</span><span class="sxs-lookup"><span data-stu-id="8d00d-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8d00d-116">Si existe una cantidad mínima pedido, se agregará de la siguiente forma: nivel de desbordamiento = inventario máximo + cantidad mínima pedido.</span><span class="sxs-lookup"><span data-stu-id="8d00d-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="8d00d-117">Directiva de reaprovisionamiento Cdad. fija reaprov.</span><span class="sxs-lookup"><span data-stu-id="8d00d-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="8d00d-118">Nivel de desbordamiento = cantidad a pedir + punto de pedido</span><span class="sxs-lookup"><span data-stu-id="8d00d-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8d00d-119">Si la cantidad mínima de pedido es más alta que el punto de pedido, se reemplazará de la siguiente forma: nivel de desbordamiento = cantidad a pedir + cantidad mínima de pedido.</span><span class="sxs-lookup"><span data-stu-id="8d00d-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="8d00d-120">Múltiplo de pedido</span><span class="sxs-lookup"><span data-stu-id="8d00d-120">Order Multiple</span></span>  
<span data-ttu-id="8d00d-121">Si existe un múltiplo de pedido, se ajustará el nivel de desbordamiento para las directivas de reaprovisionamiento de cantidad máxima y cantidad fija de reaprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="8d00d-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="8d00d-122">Crear la línea de planificación con advertencia de desbordamiento</span><span class="sxs-lookup"><span data-stu-id="8d00d-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="8d00d-123">Cuando un suministro existente provoca que el inventario proyectado sea superior al nivel de desbordamiento al final de un ciclo, se crea una línea de planificación.</span><span class="sxs-lookup"><span data-stu-id="8d00d-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="8d00d-124">Para advertir del posible suministro superfluo, la línea de planificación tiene un mensaje de advertencia, el campo **Aceptar mensaje acción** no está seleccionado y el mensaje de acción es Cancelar o Cambiar cdad.</span><span class="sxs-lookup"><span data-stu-id="8d00d-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="8d00d-125">Cálculo de la cantidad en la línea de planificación</span><span class="sxs-lookup"><span data-stu-id="8d00d-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="8d00d-126">Cantidad de planificación de línea = cantidad de suministro actual – (inventario proyectado – nivel de desbordamiento)</span><span class="sxs-lookup"><span data-stu-id="8d00d-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8d00d-127">Como con todas las líneas de advertencia, se omitirá cualquier cantidad de pedido máximo y mínimo o múltiplo de pedido.</span><span class="sxs-lookup"><span data-stu-id="8d00d-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="8d00d-128">Definir el tipo de mensaje de acción</span><span class="sxs-lookup"><span data-stu-id="8d00d-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="8d00d-129">Si la cantidad de la línea de planificación es superior a 0, el mensaje de acción es Cambiar cdad.</span><span class="sxs-lookup"><span data-stu-id="8d00d-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="8d00d-130">Si la cantidad de la línea de planificación es igual o menor a 0, el mensaje de acción es Cancelar.</span><span class="sxs-lookup"><span data-stu-id="8d00d-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="8d00d-131">Composición del mensaje de advertencia</span><span class="sxs-lookup"><span data-stu-id="8d00d-131">Composing the Warning Message</span></span>  
<span data-ttu-id="8d00d-132">En el caso de desbordamiento, la ventana **Elementos planificación sin seguimiento** muestra un mensaje de advertencia con la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="8d00d-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="8d00d-133">Nivel de inventario proyectado que ha activado la advertencia</span><span class="sxs-lookup"><span data-stu-id="8d00d-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="8d00d-134">Nivel de desbordamiento calculado</span><span class="sxs-lookup"><span data-stu-id="8d00d-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="8d00d-135">Fecha de vencimiento del evento de suministro.</span><span class="sxs-lookup"><span data-stu-id="8d00d-135">The due date of the supply event.</span></span>  

<span data-ttu-id="8d00d-136">Ejemplo: "El inventario proyectado 120 es superior al nivel de desbordamiento 60 el 28-01-11".</span><span class="sxs-lookup"><span data-stu-id="8d00d-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="8d00d-137">Caso</span><span class="sxs-lookup"><span data-stu-id="8d00d-137">Scenario</span></span>  
<span data-ttu-id="8d00d-138">En este ejemplo, un cliente cambia un pedido de venta de 70 a 40 piezas entre dos ejecuciones de planificación.</span><span class="sxs-lookup"><span data-stu-id="8d00d-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="8d00d-139">La característica de desbordamiento empieza a reducir la compra que se ha sugerido para la cantidad de venta inicial.</span><span class="sxs-lookup"><span data-stu-id="8d00d-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="8d00d-140">Configuración de producto</span><span class="sxs-lookup"><span data-stu-id="8d00d-140">Item setup</span></span>  

|<span data-ttu-id="8d00d-141">Política reaprov.</span><span class="sxs-lookup"><span data-stu-id="8d00d-141">Reordering Policy</span></span>|<span data-ttu-id="8d00d-142">Cdad. máxima</span><span class="sxs-lookup"><span data-stu-id="8d00d-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="8d00d-143">Cantidad máxima pedido</span><span class="sxs-lookup"><span data-stu-id="8d00d-143">Maximum Order Quantity</span></span>|<span data-ttu-id="8d00d-144">100</span><span class="sxs-lookup"><span data-stu-id="8d00d-144">100</span></span>|  
|<span data-ttu-id="8d00d-145">Punto pedido</span><span class="sxs-lookup"><span data-stu-id="8d00d-145">Reorder Point</span></span>|<span data-ttu-id="8d00d-146">50</span><span class="sxs-lookup"><span data-stu-id="8d00d-146">50</span></span>|  
|<span data-ttu-id="8d00d-147">Existencias</span><span class="sxs-lookup"><span data-stu-id="8d00d-147">Inventory</span></span>|<span data-ttu-id="8d00d-148">80</span><span class="sxs-lookup"><span data-stu-id="8d00d-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="8d00d-149">Situación antes de la disminución de venta</span><span class="sxs-lookup"><span data-stu-id="8d00d-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="8d00d-150">Evento</span><span class="sxs-lookup"><span data-stu-id="8d00d-150">Event</span></span>|<span data-ttu-id="8d00d-151">Cambiar cdad.</span><span class="sxs-lookup"><span data-stu-id="8d00d-151">Change Qty.</span></span>|<span data-ttu-id="8d00d-152">Inventario proyectado</span><span class="sxs-lookup"><span data-stu-id="8d00d-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="8d00d-153">Día uno</span><span class="sxs-lookup"><span data-stu-id="8d00d-153">Day one</span></span>|<span data-ttu-id="8d00d-154">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d00d-154">None</span></span>|<span data-ttu-id="8d00d-155">80</span><span class="sxs-lookup"><span data-stu-id="8d00d-155">80</span></span>|  
|<span data-ttu-id="8d00d-156">Venta</span><span class="sxs-lookup"><span data-stu-id="8d00d-156">Sale</span></span>|<span data-ttu-id="8d00d-157">-70</span><span class="sxs-lookup"><span data-stu-id="8d00d-157">-70</span></span>|<span data-ttu-id="8d00d-158">10</span><span class="sxs-lookup"><span data-stu-id="8d00d-158">10</span></span>|  
|<span data-ttu-id="8d00d-159">Final del ciclo</span><span class="sxs-lookup"><span data-stu-id="8d00d-159">End of time bucket</span></span>|<span data-ttu-id="8d00d-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d00d-160">None</span></span>|<span data-ttu-id="8d00d-161">10</span><span class="sxs-lookup"><span data-stu-id="8d00d-161">10</span></span>|  
|<span data-ttu-id="8d00d-162">Sugerir nuevo pedido de compra</span><span class="sxs-lookup"><span data-stu-id="8d00d-162">Suggest new purchase order</span></span>|<span data-ttu-id="8d00d-163">+90</span><span class="sxs-lookup"><span data-stu-id="8d00d-163">+90</span></span>|<span data-ttu-id="8d00d-164">100</span><span class="sxs-lookup"><span data-stu-id="8d00d-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="8d00d-165">Situación después de la disminución de venta</span><span class="sxs-lookup"><span data-stu-id="8d00d-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="8d00d-166">Cambiar</span><span class="sxs-lookup"><span data-stu-id="8d00d-166">Change</span></span>|<span data-ttu-id="8d00d-167">Cambiar cdad.</span><span class="sxs-lookup"><span data-stu-id="8d00d-167">Change Qty.</span></span>|<span data-ttu-id="8d00d-168">Inventario proyectado</span><span class="sxs-lookup"><span data-stu-id="8d00d-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="8d00d-169">Día uno</span><span class="sxs-lookup"><span data-stu-id="8d00d-169">Day one</span></span>|<span data-ttu-id="8d00d-170">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d00d-170">None</span></span>|<span data-ttu-id="8d00d-171">80</span><span class="sxs-lookup"><span data-stu-id="8d00d-171">80</span></span>|  
|<span data-ttu-id="8d00d-172">Venta</span><span class="sxs-lookup"><span data-stu-id="8d00d-172">Sale</span></span>|<span data-ttu-id="8d00d-173">-40</span><span class="sxs-lookup"><span data-stu-id="8d00d-173">-40</span></span>|<span data-ttu-id="8d00d-174">nº 40</span><span class="sxs-lookup"><span data-stu-id="8d00d-174">40</span></span>|  
|<span data-ttu-id="8d00d-175">Compra</span><span class="sxs-lookup"><span data-stu-id="8d00d-175">Purchase</span></span>|<span data-ttu-id="8d00d-176">+90</span><span class="sxs-lookup"><span data-stu-id="8d00d-176">+90</span></span>|<span data-ttu-id="8d00d-177">130</span><span class="sxs-lookup"><span data-stu-id="8d00d-177">130</span></span>|  
|<span data-ttu-id="8d00d-178">Final del ciclo</span><span class="sxs-lookup"><span data-stu-id="8d00d-178">End of time bucket</span></span>|<span data-ttu-id="8d00d-179">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d00d-179">None</span></span>|<span data-ttu-id="8d00d-180">130</span><span class="sxs-lookup"><span data-stu-id="8d00d-180">130</span></span>|  
|<span data-ttu-id="8d00d-181">Sugerir disminución de compra</span><span class="sxs-lookup"><span data-stu-id="8d00d-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="8d00d-182">pedido a partir de 90 a 60</span><span class="sxs-lookup"><span data-stu-id="8d00d-182">order from 90 to 60</span></span>|<span data-ttu-id="8d00d-183">-30</span><span class="sxs-lookup"><span data-stu-id="8d00d-183">-30</span></span>|<span data-ttu-id="8d00d-184">100</span><span class="sxs-lookup"><span data-stu-id="8d00d-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="8d00d-185">Líneas de planificación resultantes</span><span class="sxs-lookup"><span data-stu-id="8d00d-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="8d00d-186">Se crea una línea de planificación (advertencia) para reducir la compra con 30 de 90 a 60 para mantener el inventario proyectado en 100 según el nivel de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="8d00d-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="8d00d-187">![Plan según el nivel de desbordamiento](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="8d00d-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8d00d-188">Sin la característica de desbordamiento, no se crea ninguna advertencia si el nivel de inventario proyectado está por encima del inventario máximo.</span><span class="sxs-lookup"><span data-stu-id="8d00d-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="8d00d-189">Esto podría provocar un suministro superfluo de 30.</span><span class="sxs-lookup"><span data-stu-id="8d00d-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d00d-190">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8d00d-190">See Also</span></span>  
<span data-ttu-id="8d00d-191">[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="8d00d-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="8d00d-192">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="8d00d-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="8d00d-193">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="8d00d-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="8d00d-194">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="8d00d-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

