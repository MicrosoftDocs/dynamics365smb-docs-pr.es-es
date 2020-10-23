---
title: 'Detalles de diseño: Aprovisionamiento y demanda | Documentos de Microsoft'
description: Este tema introduce el concepto de demanda, que es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4661104e32e648cc134b3ba0c3d44b5a8c6daca6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911210"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="25810-103">Detalles de diseño: Demanda en almacén vacío</span><span class="sxs-lookup"><span data-stu-id="25810-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="25810-104">Cuando un usuario crea un evento de demanda, como una línea de pedido de venta, unas veces el programa permite que especifique un código de almacén y otras no, es decir, usa un almacén en blanco.</span><span class="sxs-lookup"><span data-stu-id="25810-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="25810-105">En el caso de demanda con o sin códigos de almacén, el programa de planificación funciona directamente cuando:</span><span class="sxs-lookup"><span data-stu-id="25810-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="25810-106">las líneas de demanda siempre incluyen códigos de almacén y el sistema utiliza unidades de almacenamiento por completo, incluida la configuración de almacén correspondiente.</span><span class="sxs-lookup"><span data-stu-id="25810-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="25810-107">Las líneas de demanda nunca incluyen códigos de almacén y el sistema no utiliza unidades de almacenamiento ni configuración de almacén (consulte el último caso en la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="25810-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="25810-108">Sin embargo, si los eventos de demanda a veces incluyen códigos de almacén y en otras ocasiones no, el programa de planificación seguirá determinadas reglas dependiendo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="25810-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="25810-109">Demanda en los almacenes</span><span class="sxs-lookup"><span data-stu-id="25810-109">Demand at Location</span></span>
<span data-ttu-id="25810-110">Cuando el sistema de planificación detecta demanda en un almacén (una línea con un código de almacén), actuará de distinta forma dependiendo de tres valores de configuración críticos.</span><span class="sxs-lookup"><span data-stu-id="25810-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="25810-111">Durante la ejecución de la planificación, el programa comprueba los tres valores de configuración por orden y genera la planificación en consecuencia:</span><span class="sxs-lookup"><span data-stu-id="25810-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="25810-112">¿Tiene una marca de verificación el campo **Almacén obligatorio**?</span><span class="sxs-lookup"><span data-stu-id="25810-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="25810-113">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="25810-113">If yes, then:</span></span>

2. <span data-ttu-id="25810-114">¿Existe unidad de almacenamiento para el producto?</span><span class="sxs-lookup"><span data-stu-id="25810-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="25810-115">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="25810-115">If yes, then:</span></span>

    <span data-ttu-id="25810-116">El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="25810-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="25810-117">Si no es así:</span><span class="sxs-lookup"><span data-stu-id="25810-117">If no, then:</span></span>

3. <span data-ttu-id="25810-118">¿Contiene el campo Componentes en alm. el código de almacén que tiene la demanda?</span><span class="sxs-lookup"><span data-stu-id="25810-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="25810-119">En caso afirmativo:</span><span class="sxs-lookup"><span data-stu-id="25810-119">If yes, then:</span></span>

  <span data-ttu-id="25810-120">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="25810-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="25810-121">Si no es así:</span><span class="sxs-lookup"><span data-stu-id="25810-121">If no, then:</span></span>

  <span data-ttu-id="25810-122">El producto se planifica según estos parámetros: Política reaprov. = Lote por lote, Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos, productos que utilizan la política de reaprovisionamiento = El pedido continúa utilizando el pedido, así como los demás ajustes.</span><span class="sxs-lookup"><span data-stu-id="25810-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="25810-123">La configuración de planificación excepcional que se envía como la última reacción en el paso 3 anterior se denomina en adelante "alternativa mínima".</span><span class="sxs-lookup"><span data-stu-id="25810-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="25810-124">Esta configuración de planificación solo cubre la demanda exacta y se omite todos los demás parámetros de planificación.</span><span class="sxs-lookup"><span data-stu-id="25810-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="25810-125">Para obtener información acerca de las variaciones de esta lógica de planificación, consulte la sección de casos a continuación.</span><span class="sxs-lookup"><span data-stu-id="25810-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="25810-126">Demanda en almacén en blanco</span><span class="sxs-lookup"><span data-stu-id="25810-126">Demand at Blank Location</span></span>
<span data-ttu-id="25810-127">Incluso aunque el campo **Almacén obligatorio** esté marcado, el programa permitirá la creación de líneas de demanda sin código de almacén, lo que también se conoce como "almacén en blanco”.</span><span class="sxs-lookup"><span data-stu-id="25810-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="25810-128">Ésta es una desviación del sistema porque tiene diversos valores de configuración ajustados para tratar con los almacenes (consulte más arriba) y, como resultado, el motor de planificación no creará ninguna línea de planificación para dicha línea de demanda.</span><span class="sxs-lookup"><span data-stu-id="25810-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="25810-129">Si el campo **Almacén obligatorio** no está seleccionado pero existe algún valor de configuración de almacén, también se considera una desviación, y el sistema de planificación reaccionará aplicando la “alternativa mínima”. El producto se planificaría así: directiva de reaprovisionamiento = lote por lote (el pedido sigue siendo pedido), incluir inventario = sí, resto de parámetros de planificación = vacío.</span><span class="sxs-lookup"><span data-stu-id="25810-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="25810-130">Escenarios</span><span class="sxs-lookup"><span data-stu-id="25810-130">Scenarios</span></span>
<span data-ttu-id="25810-131">En los escenarios siguientes se describen las variaciones de la demanda en el almacén en blanco y cómo resuelve el sistema de planificación la "alternativa mínima".</span><span class="sxs-lookup"><span data-stu-id="25810-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="25810-132">Configuración 1:</span><span class="sxs-lookup"><span data-stu-id="25810-132">Setup 1:</span></span>
<span data-ttu-id="25810-133">Almacén obligatorio = Sí</span><span class="sxs-lookup"><span data-stu-id="25810-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="25810-134">La unidad de almacenamiento está configurada para ROJO</span><span class="sxs-lookup"><span data-stu-id="25810-134">SKU is set up for RED</span></span>

<span data-ttu-id="25810-135">Componentes en almacén = AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="25810-136">Caso 1.1: La demanda está en el almacén ROJO</span><span class="sxs-lookup"><span data-stu-id="25810-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="25810-137">El producto se planifica en función de los parámetros de planificación de la ficha de la unidad de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="25810-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="25810-138">Caso 1.2: La demanda está en el almacén AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="25810-139">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="25810-140">Caso 1.3: La demanda está en el almacén VERDE</span><span class="sxs-lookup"><span data-stu-id="25810-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="25810-141">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="25810-142">Caso 1.4: La demanda está en el almacén EN BLANCO</span><span class="sxs-lookup"><span data-stu-id="25810-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="25810-143">El producto no se planifica porque no hay definido ningún almacén en la línea de demanda.</span><span class="sxs-lookup"><span data-stu-id="25810-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="25810-144">Configuración 2:</span><span class="sxs-lookup"><span data-stu-id="25810-144">Setup 2:</span></span>
<span data-ttu-id="25810-145">Almacén obligatorio = Sí</span><span class="sxs-lookup"><span data-stu-id="25810-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="25810-146">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="25810-146">No SKU exists</span></span>

<span data-ttu-id="25810-147">Componentes en almacén = AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="25810-148">Caso 2.1: La demanda está en el almacén ROJO</span><span class="sxs-lookup"><span data-stu-id="25810-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="25810-149">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="25810-150">Caso 2.2: La demanda está en el almacén AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="25810-151">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="25810-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="25810-152">Configuración 3:</span><span class="sxs-lookup"><span data-stu-id="25810-152">Setup 3:</span></span>
<span data-ttu-id="25810-153">Almacén obligatorio = No</span><span class="sxs-lookup"><span data-stu-id="25810-153">Location Mandatory = No</span></span>

<span data-ttu-id="25810-154">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="25810-154">No SKU exists</span></span>

<span data-ttu-id="25810-155">Componentes en almacén = AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="25810-156">Caso 3.1: La demanda está en el almacén ROJO</span><span class="sxs-lookup"><span data-stu-id="25810-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="25810-157">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="25810-158">Caso 3.2: La demanda está en el almacén AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="25810-159">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="25810-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="25810-160">Caso 3.3: La demanda está en el almacén EN BLANCO</span><span class="sxs-lookup"><span data-stu-id="25810-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="25810-161">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="25810-162">Configuración 4:</span><span class="sxs-lookup"><span data-stu-id="25810-162">Setup 4:</span></span>
<span data-ttu-id="25810-163">Almacén obligatorio = No</span><span class="sxs-lookup"><span data-stu-id="25810-163">Location Mandatory = No</span></span>

<span data-ttu-id="25810-164">No existe unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="25810-164">No SKU exists</span></span>

<span data-ttu-id="25810-165">Componentes en almacén = EN BLANCO</span><span class="sxs-lookup"><span data-stu-id="25810-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="25810-166">Caso 4.1: La demanda está en el almacén AZUL</span><span class="sxs-lookup"><span data-stu-id="25810-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="25810-167">El producto se planifica en función de los siguientes parámetros: Política reaprov. = Lote por lote (el pedido sigue siendo pedido), Incluir existencias = Sí, todos los demás parámetros de planificación = vacíos.</span><span class="sxs-lookup"><span data-stu-id="25810-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="25810-168">Caso 4.2: La demanda está en el almacén EN BLANCO</span><span class="sxs-lookup"><span data-stu-id="25810-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="25810-169">El producto se planifica en función de los parámetros de planificación de la ficha del producto.</span><span class="sxs-lookup"><span data-stu-id="25810-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="25810-170">Como se ilustra en el último caso, la única manera de conseguir un resultado correcto para una línea de demanda sin código de ubicación consiste en deshabilitar todos los valores de configuración relativos a los almacenes.</span><span class="sxs-lookup"><span data-stu-id="25810-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="25810-171">De forma similar, la única manera de obtener resultados de planificación estables para la demanda en los almacenes es utilizar unidades de almacenamiento (UA).</span><span class="sxs-lookup"><span data-stu-id="25810-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="25810-172">Por consiguiente, si las empresas normalmente planifican la demanda en los almacenes, es muy recomendable utilizar el módulo Unidades de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="25810-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="25810-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="25810-173">See Also</span></span>  
<span data-ttu-id="25810-174">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="25810-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="25810-175">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="25810-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="25810-176">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="25810-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
