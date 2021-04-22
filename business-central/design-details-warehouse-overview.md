---
title: 'Detalles de diseño: Resumen de almacén | Documentos de Microsoft'
description: Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén. Se administra en la tabla **Movimiento almacén**. Cada transacción se almacena en un registro de almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8a972cebc919e0e308f22b417a62f33cb8b06f62
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785140"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="183e5-105">Detalles de diseño: Resumen de almacén</span><span class="sxs-lookup"><span data-stu-id="183e5-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="183e5-106">Para respaldar la manipulación física de los productos en el nivel de zona y de ubicación, se debe realizar el seguimiento de toda la información por cada transacción o movimiento que se produzca en el almacén.</span><span class="sxs-lookup"><span data-stu-id="183e5-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="183e5-107">Se administra en la tabla **Movimiento almacén**.</span><span class="sxs-lookup"><span data-stu-id="183e5-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="183e5-108">Cada transacción se almacena en un registro de almacén.</span><span class="sxs-lookup"><span data-stu-id="183e5-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="183e5-109">Los documentos de almacén y el diario de almacén se usan para registrar los movimientos de producto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="183e5-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="183e5-110">Cada vez que se mueve, recibe, ubica, selecciona, envía o ajusta un producto en el almacén, los movimientos de almacén se registran para almacenar la información física sobre zona, ubicación y cantidad.</span><span class="sxs-lookup"><span data-stu-id="183e5-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="183e5-111">La tabla **Contenido ubicación** se usa para controlar todas las dimensiones del contenido de una ubicación por producto, como la unidad de medida, la cantidad máxima y la cantidad mínima.</span><span class="sxs-lookup"><span data-stu-id="183e5-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="183e5-112">La tabla **Contenido ubicación** también contiene los campos de flujo para los movimientos de almacén, las instrucciones de almacén y las líneas de diario de almacén, lo que garantiza que se puede calcular rápidamente la disponibilidad de un producto por ubicación y una ubicación para un producto.</span><span class="sxs-lookup"><span data-stu-id="183e5-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="183e5-113">Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="183e5-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="183e5-114">Cuando los registros de producto se producen fuera del módulo de almacén, se usa una ubicación de ajuste predeterminado por ubicación para sincronizar los movimientos de almacén con los movimientos de inventario.</span><span class="sxs-lookup"><span data-stu-id="183e5-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="183e5-115">Durante el inventario físico del almacén, cualquier diferencia entre las cantidades calculadas y contadas se registra en la ubicación de ajuste y después se registra como corrección de los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="183e5-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="183e5-116">Para obtener más información, consulte [Detalles de diseño: Integración con inventario](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="183e5-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="183e5-117">En la ilustración siguiente se describen los flujos de almacén típicos.</span><span class="sxs-lookup"><span data-stu-id="183e5-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="183e5-118">![Resumen de procesos de almacén](media/design_details_warehouse_management_overview.png "Resumen de procesos de almacén")</span><span class="sxs-lookup"><span data-stu-id="183e5-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="183e5-119">Gestión avanzada o básica de almacén</span><span class="sxs-lookup"><span data-stu-id="183e5-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="183e5-120">La funcionalidad de almacén en [!INCLUDE[prod_short](includes/prod_short.md)] se puede implementar en distintos niveles de complejidad, en función de los procesos de una empresa y del volumen de pedidos.</span><span class="sxs-lookup"><span data-stu-id="183e5-120">Warehouse functionality in [!INCLUDE[prod_short](includes/prod_short.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="183e5-121">La diferencia principal es que las actividades se realizan pedido a pedido en el almacenamiento básico, mientras que se consolidan para varios pedidos en el almacenamiento avanzado.</span><span class="sxs-lookup"><span data-stu-id="183e5-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="183e5-122">Para diferenciar los distintos niveles de complejidad, en esta documentación se hace referencia a dos denominaciones generales: almacenamiento básico y avanzado.</span><span class="sxs-lookup"><span data-stu-id="183e5-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="183e5-123">Esta diferenciación sencilla abarca diferentes niveles de complejidad, tal como se define mediante los módulos de producto y de ubicación, cada uno respaldado por distintos documentos de IU.</span><span class="sxs-lookup"><span data-stu-id="183e5-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="183e5-124">Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="183e5-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="183e5-125">El nivel más avanzado del almacenamiento se denomina “instalaciones SGA” en esta documentación, ya que este nivel requiere el módulo más avanzado: Sistemas de gestión de almacén.</span><span class="sxs-lookup"><span data-stu-id="183e5-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="183e5-126">Los documentos de IU siguientes se usan en el almacenamiento básico y avanzado.</span><span class="sxs-lookup"><span data-stu-id="183e5-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="183e5-127">Documentos básicos de la IU</span><span class="sxs-lookup"><span data-stu-id="183e5-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="183e5-128">**Ubicación existencias**</span><span class="sxs-lookup"><span data-stu-id="183e5-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="183e5-129">**Picking inventario**</span><span class="sxs-lookup"><span data-stu-id="183e5-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="183e5-130">**Movimiento inventario**</span><span class="sxs-lookup"><span data-stu-id="183e5-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="183e5-131">**Diario productos**</span><span class="sxs-lookup"><span data-stu-id="183e5-131">**Item Journal**</span></span>  
-   <span data-ttu-id="183e5-132">**Diario reclasificación producto**</span><span class="sxs-lookup"><span data-stu-id="183e5-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="183e5-133">(Varios informes)</span><span class="sxs-lookup"><span data-stu-id="183e5-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="183e5-134">Documentos avanzados de la IU</span><span class="sxs-lookup"><span data-stu-id="183e5-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="183e5-135">**Recep. almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="183e5-136">**Hoja trabajo ubic.**</span><span class="sxs-lookup"><span data-stu-id="183e5-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="183e5-137">**Ubicar almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="183e5-138">**Hoja trabajo picking**</span><span class="sxs-lookup"><span data-stu-id="183e5-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="183e5-139">**Picking almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="183e5-140">**Hoja trabajo mov.**</span><span class="sxs-lookup"><span data-stu-id="183e5-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="183e5-141">**Movimiento almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="183e5-142">**Picking almacén interno**</span><span class="sxs-lookup"><span data-stu-id="183e5-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="183e5-143">**Ubicación almacén interno**</span><span class="sxs-lookup"><span data-stu-id="183e5-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="183e5-144">**Hoja trab. creación ubicación**</span><span class="sxs-lookup"><span data-stu-id="183e5-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="183e5-145">**Hoja trab. creac. cont. ubic.**</span><span class="sxs-lookup"><span data-stu-id="183e5-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="183e5-146">**Diario producto almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="183e5-147">**Diario recl. prod. almacén**</span><span class="sxs-lookup"><span data-stu-id="183e5-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="183e5-148">(Varios informes)</span><span class="sxs-lookup"><span data-stu-id="183e5-148">(Various reports)</span></span>  

<span data-ttu-id="183e5-149">Para obtener más información acerca de cada documento, consulte los temas correspondientes en la página.</span><span class="sxs-lookup"><span data-stu-id="183e5-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="183e5-150">Terminología</span><span class="sxs-lookup"><span data-stu-id="183e5-150">Terminology</span></span>  
<span data-ttu-id="183e5-151">Para establecer la correspondencia con los conceptos financieros de compras y ventas, en la documentación de almacén de [!INCLUDE[prod_short](includes/prod_short.md)] se hace referencia a los siguientes términos para el flujo de productos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="183e5-151">To align with the financial concepts of purchases and sales, [!INCLUDE[prod_short](includes/prod_short.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="183e5-152">Periodo</span><span class="sxs-lookup"><span data-stu-id="183e5-152">Term</span></span>|<span data-ttu-id="183e5-153">Description</span><span class="sxs-lookup"><span data-stu-id="183e5-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="183e5-154">Flujo de entrada</span><span class="sxs-lookup"><span data-stu-id="183e5-154">Inbound flow</span></span>|<span data-ttu-id="183e5-155">Productos que se trasladan a la ubicación del almacén, como compras y transferencias de entrada.</span><span class="sxs-lookup"><span data-stu-id="183e5-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="183e5-156">Flujo interno</span><span class="sxs-lookup"><span data-stu-id="183e5-156">Internal flow</span></span>|<span data-ttu-id="183e5-157">Productos que se mueven dentro de la ubicación del almacén, como componentes de producción y salida.</span><span class="sxs-lookup"><span data-stu-id="183e5-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="183e5-158">Flujo de salida</span><span class="sxs-lookup"><span data-stu-id="183e5-158">Outbound flow</span></span>|<span data-ttu-id="183e5-159">Productos que salen de la ubicación del almacén, como ventas y transferencias de salida.</span><span class="sxs-lookup"><span data-stu-id="183e5-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="183e5-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="183e5-160">See Also</span></span>  
 [<span data-ttu-id="183e5-161">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="183e5-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]