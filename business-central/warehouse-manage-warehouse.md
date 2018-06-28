---
title: "Actividades de almacén | de Microsoft"
description: "Una vez recibidos los bienes, antes de que se envíen, se llevan a cabo una serie de actividades internas de almacén para garantizar un flujo eficaz por todo el almacén y para organizar y mantener las existencias de la empresa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: ddc2e9bdf131a68fb5ea280011971b8a8f7220f0
ms.contentlocale: es-es
ms.lasthandoff: 06/28/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="14647-103">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="14647-103">Warehouse Management</span></span>
<span data-ttu-id="14647-104">Una vez recibidos los bienes, antes de que se envíen, se llevan a cabo una serie de actividades internas de almacén para garantizar un flujo eficaz por todo el almacén y para organizar y mantener las existencias de la empresa.</span><span class="sxs-lookup"><span data-stu-id="14647-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="14647-105">Entre las actividades de almacén habituales se encuentran la ubicación de productos, los movimientos de productos dentro de un mismo almacén o entre distintos almacenes y el picking de productos para las fases de ensamblado, producción o envío.</span><span class="sxs-lookup"><span data-stu-id="14647-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="14647-106">Los productos de ensamblaje para la venta o el inventario también se pueden considerar actividades del almacén, pero éstos se cubren en otra parte.</span><span class="sxs-lookup"><span data-stu-id="14647-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="14647-107">Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="14647-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="14647-108">En almacenes de grandes dimensiones, las distintas tareas de manipulación pueden distribuirse entre distintos departamentos y la integración puede gestionarse mediante un flujo de trabajo dirigido.</span><span class="sxs-lookup"><span data-stu-id="14647-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="14647-109">En instalaciones más sencillas, el flujo no está tan formalizado y las actividades de almacén se llevan a cabo con las llamadas ubicaciones y picking de inventario.</span><span class="sxs-lookup"><span data-stu-id="14647-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="14647-110">Para obtener más información sobre configuraciones de almacén básicas y avanzadas, consulte [Detalles de diseño: Vista general de almacén](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14647-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="14647-111">Antes de poder realizar actividades de almacén, debe configurar el sistema para la complejidad relevante del procesamiento del almacén.</span><span class="sxs-lookup"><span data-stu-id="14647-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="14647-112">Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="14647-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="14647-113">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="14647-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="14647-114">**Para**</span><span class="sxs-lookup"><span data-stu-id="14647-114">**To**</span></span>|<span data-ttu-id="14647-115">**Vea**</span><span class="sxs-lookup"><span data-stu-id="14647-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="14647-116">Registre la recepción de productos en las ubicaciones del almacén, ya sea solo con una orden de compra, en configuraciones de ubicación sencillas o con un recibo de almacén, en caso de procesamiento semi o totalmente automatizado del almacén en la ubicación.</span><span class="sxs-lookup"><span data-stu-id="14647-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="14647-117">Recibir productos</span><span class="sxs-lookup"><span data-stu-id="14647-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="14647-118">Evite los procesos de ubicación y picking para acelerar un elemento directamente desde la recepción o producción hasta el envío.</span><span class="sxs-lookup"><span data-stu-id="14647-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="14647-119">Productos de tránsito directo</span><span class="sxs-lookup"><span data-stu-id="14647-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="14647-120">Ubicar los productos recibidos de compras, devoluciones de ventas, transferencias o salidas de producción de acuerdo con lo configurado en el proceso del almacén.</span><span class="sxs-lookup"><span data-stu-id="14647-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="14647-121">Configurando los artículos componentes</span><span class="sxs-lookup"><span data-stu-id="14647-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="14647-122">Mover productos de una ubicación a otra en el almacén.</span><span class="sxs-lookup"><span data-stu-id="14647-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="14647-123">Mover artículos</span><span class="sxs-lookup"><span data-stu-id="14647-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="14647-124">Realizar el picking de los productos para su envío, transferencia o consumo en producción o ensamblado, de acuerdo con lo configurado en el proceso del almacén.</span><span class="sxs-lookup"><span data-stu-id="14647-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="14647-125">Realización de picking de artículos</span><span class="sxs-lookup"><span data-stu-id="14647-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="14647-126">Registre la envío de productos desde las ubicaciones del almacén, ya sea solo con una orden de ventas, en configuraciones de ubicación sencillas o con un envío de almacén, en caso de proceso semi o totalmente automatizado del almacén en la ubicación.</span><span class="sxs-lookup"><span data-stu-id="14647-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="14647-127">Enviar productos</span><span class="sxs-lookup"><span data-stu-id="14647-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="14647-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14647-128">See Also</span></span>  
[<span data-ttu-id="14647-129">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="14647-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="14647-130">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="14647-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="14647-131">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="14647-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="14647-132">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="14647-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="14647-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14647-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

