---
title: "Descripción de los tipos de productos | Documentos de Microsoft"
description: "Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio, por ejemplo, cuando los costes de producto cambien por motivos distintos de las transacciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/18/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 2240840e977bcd1186c74972ce0457deb03058a0
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="about-item-types"></a><span data-ttu-id="39582-103">Acerca de los tipos de productos</span><span class="sxs-lookup"><span data-stu-id="39582-103">About Item Types</span></span>
<span data-ttu-id="39582-104">En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio y, por lo tanto, cómo se administra en el sistema.</span><span class="sxs-lookup"><span data-stu-id="39582-104">In the **Type** field on the **Item Card** page, you can select what the item is used for in your business and therefore how it is managed in the system.</span></span> <span data-ttu-id="39582-105">Existen tres opciones:</span><span class="sxs-lookup"><span data-stu-id="39582-105">Three options exist:</span></span>

|<span data-ttu-id="39582-106">Opción</span><span class="sxs-lookup"><span data-stu-id="39582-106">Option</span></span>|<span data-ttu-id="39582-107">Propósito típico</span><span class="sxs-lookup"><span data-stu-id="39582-107">Typical Purpose</span></span>|
|------|-----------|
|<span data-ttu-id="39582-108">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="39582-108">Inventory</span></span>|<span data-ttu-id="39582-109">Una unidad física, como una bicicleta, para un soporte comercial completo.</span><span class="sxs-lookup"><span data-stu-id="39582-109">A physical unit, such as a bicycle, for full business support.</span></span>|
|<span data-ttu-id="39582-110">No inventario</span><span class="sxs-lookup"><span data-stu-id="39582-110">Non-Inventory</span></span>|<span data-ttu-id="39582-111">Una unidad física, como un tornillo, para soporte comercial limitado, por ejemplo, porque el artículo solo se usa internamente y tiene un bajo coste.</span><span class="sxs-lookup"><span data-stu-id="39582-111">A physical unit, such as a bolt, for limited business support, for example, because the item is only used internally and has a low cost.</span></span>|
|<span data-ttu-id="39582-112">Servicio</span><span class="sxs-lookup"><span data-stu-id="39582-112">Service</span></span>|<span data-ttu-id="39582-113">Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.</span><span class="sxs-lookup"><span data-stu-id="39582-113">A labor time unit, such as a consultancy hour, for limited business support.</span></span>|

<span data-ttu-id="39582-114">El tipo de **inventario** implica el seguimiento completo de la cantidad y el valor del inventario.</span><span class="sxs-lookup"><span data-stu-id="39582-114">The **Inventory** type involves full tracking of inventory quantity and value.</span></span> <span data-ttu-id="39582-115">Por lo tanto, todos los tipos de transacciones de artículos son compatibles y los artículos de tipo Inventario se pueden usar con todas las características de manejo de artículos.</span><span class="sxs-lookup"><span data-stu-id="39582-115">Therefore, all item transaction types are supported, and items of type Inventory can be used with all item-handling features.</span></span>

<span data-ttu-id="39582-116">Los tipos de **Servicio** y **No inventario** no implican el seguimiento de la cantidad y el valor del inventario.</span><span class="sxs-lookup"><span data-stu-id="39582-116">The **Service** and **Non-Inventory** types do not involve tracking of inventory quantity and value.</span></span> <span data-ttu-id="39582-117">Por lo tanto, solo se admiten los tipos y las características de transacción de los elementos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="39582-117">Therefore, only selected item transaction types and features are supported.</span></span>

<span data-ttu-id="39582-118">Los tres tipos de elementos admiten las siguientes características, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="39582-118">The three item types support the following features respectively.</span></span>

|<span data-ttu-id="39582-119">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="39582-119">Item Type</span></span>|<span data-ttu-id="39582-120">Ccial</span><span class="sxs-lookup"><span data-stu-id="39582-120">Sales</span></span>|<span data-ttu-id="39582-121">Compra</span><span class="sxs-lookup"><span data-stu-id="39582-121">Purchasing</span></span>|<span data-ttu-id="39582-122">Consumo de proyecto</span><span class="sxs-lookup"><span data-stu-id="39582-122">Job Consumption</span></span>|<span data-ttu-id="39582-123">Consumo de servicio</span><span class="sxs-lookup"><span data-stu-id="39582-123">Service Consumption</span></span>|<span data-ttu-id="39582-124">Consumo de ensamblado</span><span class="sxs-lookup"><span data-stu-id="39582-124">Assembly Consumption</span></span>|<span data-ttu-id="39582-125">Producción Consumo</span><span class="sxs-lookup"><span data-stu-id="39582-125">Production Consumption</span></span>|<span data-ttu-id="39582-126">Salida de ensamblado</span><span class="sxs-lookup"><span data-stu-id="39582-126">Assembly Output</span></span>|<span data-ttu-id="39582-127">Salida de producción</span><span class="sxs-lookup"><span data-stu-id="39582-127">Production Output</span></span>|<span data-ttu-id="39582-128">Transferencia de ubicación</span><span class="sxs-lookup"><span data-stu-id="39582-128">Location Transfer</span></span>|<span data-ttu-id="39582-129">Recuento físico</span><span class="sxs-lookup"><span data-stu-id="39582-129">Physical Counting</span></span>|<span data-ttu-id="39582-130">Revalorización de inventario</span><span class="sxs-lookup"><span data-stu-id="39582-130">Inventory Revaluation</span></span>|<span data-ttu-id="39582-131">Inventario y valoración</span><span class="sxs-lookup"><span data-stu-id="39582-131">Inventory Costing</span></span>|<span data-ttu-id="39582-132">Seguim. prod.</span><span class="sxs-lookup"><span data-stu-id="39582-132">Item Tracking</span></span>|<span data-ttu-id="39582-133">Reserva</span><span class="sxs-lookup"><span data-stu-id="39582-133">Reservation</span></span>|<span data-ttu-id="39582-134">Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="39582-134">Warehousing</span></span>|<span data-ttu-id="39582-135">Planificación</span><span class="sxs-lookup"><span data-stu-id="39582-135">Planning</span></span>|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|<span data-ttu-id="39582-136">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="39582-136">Inventory</span></span>|<span data-ttu-id="39582-137">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-137">Yes</span></span>|<span data-ttu-id="39582-138">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-138">Yes</span></span>|<span data-ttu-id="39582-139">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-139">Yes</span></span>|<span data-ttu-id="39582-140">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-140">Yes</span></span>|<span data-ttu-id="39582-141">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-141">Yes</span></span>|<span data-ttu-id="39582-142">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-142">Yes</span></span>|<span data-ttu-id="39582-143">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-143">Yes</span></span>|<span data-ttu-id="39582-144">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-144">Yes</span></span>|<span data-ttu-id="39582-145">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-145">Yes</span></span>|<span data-ttu-id="39582-146">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-146">Yes</span></span>|<span data-ttu-id="39582-147">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-147">Yes</span></span>|<span data-ttu-id="39582-148">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-148">Yes</span></span>|<span data-ttu-id="39582-149">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-149">Yes</span></span>|<span data-ttu-id="39582-150">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-150">Yes</span></span>|<span data-ttu-id="39582-151">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-151">Yes</span></span>|<span data-ttu-id="39582-152">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-152">Yes</span></span>|
|<span data-ttu-id="39582-153">No inventario</span><span class="sxs-lookup"><span data-stu-id="39582-153">Non-Inventory</span></span>|<span data-ttu-id="39582-154">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-154">Yes</span></span>|<span data-ttu-id="39582-155">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-155">Yes</span></span>|<span data-ttu-id="39582-156">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-156">Yes</span></span>|<span data-ttu-id="39582-157">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-157">Yes</span></span>|<span data-ttu-id="39582-158">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-158">Yes</span></span>|<span data-ttu-id="39582-159">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-159">Yes</span></span>|<span data-ttu-id="39582-160">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-160">No</span></span>|<span data-ttu-id="39582-161">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-161">No</span></span>|<span data-ttu-id="39582-162">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-162">No</span></span>|<span data-ttu-id="39582-163">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-163">No</span></span>|<span data-ttu-id="39582-164">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-164">No</span></span>|<span data-ttu-id="39582-165">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-165">No</span></span>|<span data-ttu-id="39582-166">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-166">No</span></span>|<span data-ttu-id="39582-167">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-167">No</span></span>|<span data-ttu-id="39582-168">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-168">No</span></span>|<span data-ttu-id="39582-169">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-169">No</span></span>|
|<span data-ttu-id="39582-170">Servicio</span><span class="sxs-lookup"><span data-stu-id="39582-170">Service</span></span>|<span data-ttu-id="39582-171">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-171">Yes</span></span>|<span data-ttu-id="39582-172">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-172">Yes</span></span>|<span data-ttu-id="39582-173">Sí</span><span class="sxs-lookup"><span data-stu-id="39582-173">Yes</span></span>|<span data-ttu-id="39582-174">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-174">No</span></span>|<span data-ttu-id="39582-175">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-175">No</span></span>|<span data-ttu-id="39582-176">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-176">No</span></span>|<span data-ttu-id="39582-177">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-177">No</span></span>|<span data-ttu-id="39582-178">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-178">No</span></span>|<span data-ttu-id="39582-179">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-179">No</span></span>|<span data-ttu-id="39582-180">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-180">No</span></span>|<span data-ttu-id="39582-181">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-181">No</span></span>|<span data-ttu-id="39582-182">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-182">No</span></span>|<span data-ttu-id="39582-183">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-183">No</span></span>|<span data-ttu-id="39582-184">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-184">No</span></span>|<span data-ttu-id="39582-185">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-185">No</span></span>|<span data-ttu-id="39582-186">N.º</span><span class="sxs-lookup"><span data-stu-id="39582-186">No</span></span>|

> [!NOTE]
> <span data-ttu-id="39582-187">Los productos que ofrece a sus clientes pero que no desea administrar en su sistema hasta que comience a venderlos se pueden configurar como productos del catálogo.</span><span class="sxs-lookup"><span data-stu-id="39582-187">Items that you offer to your customers but you do not want manage in your system until you start selling them can be set up as catalog items.</span></span> <span data-ttu-id="39582-188">Los productos del catálogo no deben confundirse con artículos regulares de tipo No inventario.</span><span class="sxs-lookup"><span data-stu-id="39582-188">Catalog items are not to be mistaken with regular items of type Non-Inventory.</span></span> <span data-ttu-id="39582-189">Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).</span><span class="sxs-lookup"><span data-stu-id="39582-189">For more information, see [Work with Catalog Items](inventory-how-work-nonstock-items.md).</span></span>

> [!NOTE]
> <span data-ttu-id="39582-190">Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="39582-190">Customers' items that you perform service on, such as a printer, are called service items.</span></span> <span data-ttu-id="39582-191">Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo.</span><span class="sxs-lookup"><span data-stu-id="39582-191">Service items have nothing to do with regular or catalog items.</span></span> <span data-ttu-id="39582-192">Sin embargo, los componentes del servicio pueden ser productos regulares.</span><span class="sxs-lookup"><span data-stu-id="39582-192">However, service components can be regular items.</span></span> <span data-ttu-id="39582-193">Para obtener más información, consulte [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).</span><span class="sxs-lookup"><span data-stu-id="39582-193">For more information, see [Set Up Service Items and Service Item Components](service-how-setup-service-items.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="39582-194">Consulte también</span><span class="sxs-lookup"><span data-stu-id="39582-194">See Also</span></span>
[<span data-ttu-id="39582-195">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="39582-195">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="39582-196">Configurar inventario</span><span class="sxs-lookup"><span data-stu-id="39582-196">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
[<span data-ttu-id="39582-197">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="39582-197">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="39582-198">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="39582-198">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="39582-199">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39582-199">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
