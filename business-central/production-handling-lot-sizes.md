---
title: Manejo de tamaños de lote | Documentos de Microsoft
description: Este tema describe diferentes formas de manejar los tamaños de lote.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6f07828e969d5a8394657bc1e05d44156ada5411
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749023"
---
# <a name="handling-lot-sizes-in-production"></a><span data-ttu-id="8f8a3-103">Manejo de tamaños de lote en producción</span><span class="sxs-lookup"><span data-stu-id="8f8a3-103">Handling Lot Sizes in Production</span></span>
<span data-ttu-id="8f8a3-104">En términos de cantidad, la cantidad de artículos que produce en una operación de producción puede no correlacionarse con cómo venderlos.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-104">In terms of quantity, the number of items you produce in a production operation might not correlate to how sell them.</span></span> <span data-ttu-id="8f8a3-105">Por ejemplo, puede producir cientos de artículos en un solo lote, pero vender cada artículo individualmente.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-105">For example, you might produce hundreds of items in a single lot, but sell each item individually.</span></span> <span data-ttu-id="8f8a3-106">Cuando configura sus rutas de producción y listas de materiales (LDM), hay algunos matices que debe considerar con respecto a los tamaños de lote.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-106">When you configure your production routes and bills of materials (BOMs), there are few nuances you should consider with regards to lot sizes.</span></span> <span data-ttu-id="8f8a3-107">Este tema describe cómo el tamaño de los lotes afecta los cálculos de costos y la planificación de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-107">This topic describes how lot sizes impact cost calculations and resource planning.</span></span>

## <a name="units-of-measure-in-production-bill-of-materials"></a><span data-ttu-id="8f8a3-108">Unidades de medida en la lista de materiales de producción</span><span class="sxs-lookup"><span data-stu-id="8f8a3-108">Units of Measure in Production Bill of Materials</span></span>
<span data-ttu-id="8f8a3-109">Aunque especifica la unidad de medida base (UOM) para un artículo, su BOM puede usar una UOM diferente para el producto terminado.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-109">Although you specify the base unit of measure (UOM) for an item, your BOM might use a different UOM for the finished product.</span></span> <span data-ttu-id="8f8a3-110">Por ejemplo, la unidad de medida base de un artículo podría ser PCS, pero su lista de materiales podría requerir paleta o tonelada.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-110">For example, the base UOM for an item might be PCS, but your BOM might call for pallet or ton.</span></span> <span data-ttu-id="8f8a3-111">Esto resulta útil cuando sus máquinas o componentes en bruto dictan el volumen.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-111">This comes in handy when your machines or raw components dictate the volume.</span></span> <span data-ttu-id="8f8a3-112">Por ejemplo, probablemente no quieras hornear un solo panecillo porque es difícil usar una porción de huevo.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-112">For example, you probably wouldn't want to bake a single muffin because it is difficult to use a portion of an egg.</span></span> <span data-ttu-id="8f8a3-113">En cambio, hornea un lote de muffins para reducir el desperdicio.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-113">Instead, you bake a batch of muffins to reduce waste.</span></span> <span data-ttu-id="8f8a3-114">Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a3-114">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>

## <a name="lot-size-on-routing-lines"></a><span data-ttu-id="8f8a3-115">Tamaño de lote en líneas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8f8a3-115">Lot size on routing lines</span></span>
<span data-ttu-id="8f8a3-116">Desde una perspectiva de enrutamiento, puede especificar un tamaño de lote en las líneas de enrutamiento para alinearlo con la capacidad de las máquinas que producen los artículos.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-116">From a routing perspective, you can specify a lot size on routing lines to align with the capacity of the machines that produce the items.</span></span> <span data-ttu-id="8f8a3-117">El tiempo de ejecución en las líneas de enrutamiento se reduce proporcionalmente al tamaño del lote.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-117">The run time on routing lines is reduced proportionally to the lot size.</span></span> 

<span data-ttu-id="8f8a3-118">Esto funciona bien cuando la cantidad en una orden de producción es un factor del tamaño del lote en la ruta.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-118">This works well when the quantity on a production order is a factor of the lot size on the route.</span></span> <span data-ttu-id="8f8a3-119">Por ejemplo, si su bandeja para hornear puede contener 10 muffins, debe hornear 10, 20, 30, etc., y no 5 ni 15.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-119">For example, if your baking sheet can hold 10 muffins, you should bake 10, 20, 30, and so on, and not 5 nor 15.</span></span>  <span data-ttu-id="8f8a3-120">Esto es un problema mucho menor si se trata de grandes cantidades.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-120">This is much less of an issue if you are dealing with large quantities.</span></span>

<span data-ttu-id="8f8a3-121">El tamaño de lote también es popular en entornos de fabricación donde la producción se mide como la cantidad que puede producir durante un período de tiempo fijo.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-121">Lot size is also popular in manufacturing environments where output is measured as quantity you can make during fixed amount of time.</span></span> <span data-ttu-id="8f8a3-122">Por ejemplo, si el volumen por turno de 9 horas es de 25000 pies cúbicos, puede establecer el tiempo de ejecución en 9 horas y el tamaño del lote en 25000.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-122">Example, if Volume per 9 hour shift is 25000 cubic feet, you can set run time as 9 hours and lot size as 25000.</span></span>
<span data-ttu-id="8f8a3-123">La cantidad de la orden de producción se vuelve menos importante ya que en la orden de producción el tiempo de ejecución se calcula como el tiempo de ejecución / tamaño del lote para obtener el tiempo de ejecución por pieza.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-123">The production order quantity becomes less important as on the production order the run time gets calculated as the Run time / Lot size to get the run time per piece.</span></span>
 
> [!NOTE]
> <span data-ttu-id="8f8a3-124">El valor definido en Tamaño del lote no tiene impacto en el tiempo especificado en el campo **Tiempo de configuración** de la línea de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-124">The value defined in Lot size doesn't have impact on time specified in **Setup Time** field of the routing line.</span></span> <span data-ttu-id="8f8a3-125">La configuración ocurrirá solo una vez, incluso si hay varios lotes.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-125">The setup will happen only one time, even if there are several lots.</span></span> <span data-ttu-id="8f8a3-126">Por ejemplo, para que no necesite calentar el horno para el segundo lote de muffins.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-126">For example, so that you don’t need to warm the oven for the second lot of muffins.</span></span> <span data-ttu-id="8f8a3-127">Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a3-127">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a><span data-ttu-id="8f8a3-128">Tamaños de lote para artículos y unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8f8a3-128">Lot Sizes for Items and Stockkeeping Units</span></span>
<span data-ttu-id="8f8a3-129">Los tamaños de lote definidos para las rutas no son los mismos que los tamaños de lote para artículos o unidades de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-129">Lot sizes defined for routings are not the same as lot sizes for items or stockkeeping units.</span></span> <span data-ttu-id="8f8a3-130">Estos valores se utilizan para un propósito diferente y no afectan la capacidad de producción.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-130">Those values are used for a different purpose, and do not affect production capacity.</span></span> 

## <a name="lot-size-on-item-and-stockkeeping-units"></a><span data-ttu-id="8f8a3-131">Tamaño de lote en artículos y unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8f8a3-131">Lot size on item and stockkeeping units</span></span>
<span data-ttu-id="8f8a3-132">Para artículos y unidades de almacenamiento, los tamaños de lote tienen los siguientes efectos en el cálculo de costos y la planificación de suministros:</span><span class="sxs-lookup"><span data-stu-id="8f8a3-132">For items and stockkeeping units, lot sizes have the following effects on cost calculation and supply planning:</span></span>

* <span data-ttu-id="8f8a3-133">Para el cálculo de costos estándar, si habilita **Configuración de costo incluido** en la página **Configuración de fabricación**, el costo de la instalación se agrega al costo estándar.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-133">For standard cost calculation, if you enable **Cost Incl Setup** on the **Manufacturing Setup** page, the cost for the setup is added to the standard cost.</span></span> <span data-ttu-id="8f8a3-134">Si especifica un tamaño de lote, el costo de configuración para la operación de enrutamiento se reducirá de acuerdo con un tamaño de lote.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-134">If you specify a lot size, the setup cost for routing operation will be reduced according to one lot size.</span></span> <span data-ttu-id="8f8a3-135">Por ejemplo, si el tamaño de su lote definido en la ficha del artículo es 10 y se tarda 15 minutos en calentar el horno, el costo del combustible se asignará a los 10 muffins como aproximadamente 1,5 minutos.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-135">For example, if your lot size defined on item card is 10, and it takes 15 minutes to heat the oven, the cost of the fuel will be allocated to the 10 muffins as roughly 1.5 minutes.</span></span> 

> [!NOTE]
> <span data-ttu-id="8f8a3-136">Los costos de instalación se manejan de manera diferente a las perspectivas de asignación de capacidad y costos estándar.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-136">Setup costs are handled differently from a standard cost and capacity allocation perspectives.</span></span> <span data-ttu-id="8f8a3-137">Si la cantidad producida no coincide con el tamaño del lote definido en la ficha del artículo, se producirán variaciones.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-137">If produced quantity doesn't match lot size defined in the item card that will lead to variation.</span></span> <span data-ttu-id="8f8a3-138">Para obtener más información, vea [Administrar costes de inventario](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a3-138">For more information, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span> <!--not sure that I got this part right seems to repeat the first example.-->

<span data-ttu-id="8f8a3-139">Para la planificación de suministros, la configuración del tamaño de lote de los artículos funciona con **% predet. amortiguador** en la página **Configuración de fabricación**.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-139">For supply planning, the lot size setting on items works with the **Default Dampener %** on the **Manufacturing Setup** page.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8f8a3-140">ignorará los cambios en la demanda que estén por debajo del porcentaje del amortiguador y no creará sugerencias de planificación.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-140">will ignore changes in demand that are below the dampener percentage and will not create planning suggestions.</span></span> <span data-ttu-id="8f8a3-141">Por ejemplo, se especifica 15 en el campo% de amortiguador predeterminado, y tenemos una orden de producción de 20 muffins para alimentar a 20 invitados, pero un invitado no puede asistir.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-141">For example, 15 is specified in the Default Dampener % field, and we have a production order for 20 muffins to feed 20 guests, but one guest cannot attend.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8f8a3-142">ignorará al único invitado que falta porque es solo el 10% del tamaño de lote 10 definido en el artículo.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-142">will ignore the single missing guest because it's only 10% of the lot size 10 defined on the item.</span></span> <span data-ttu-id="8f8a3-143">Sin embargo, si dos invitados no pueden asistir, [!INCLUDE[prod_short](includes/prod_short.md)] sugerirá que reduzcamos la cantidad del pedido porque dos es el 20 % del tamaño del lote.</span><span class="sxs-lookup"><span data-stu-id="8f8a3-143">However, if two guests cannot make it, [!INCLUDE[prod_short](includes/prod_short.md)] will suggest that we reduce the order quantity because two is 20% of the lot size.</span></span> <span data-ttu-id="8f8a3-144">Para obtener más información sobre la planificación, consulte [Planificación](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a3-144">For more information about planning, see [Planning](production-planning.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f8a3-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f8a3-145">See Also</span></span>
[<span data-ttu-id="8f8a3-146">Crear LM de producción</span><span class="sxs-lookup"><span data-stu-id="8f8a3-146">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
<span data-ttu-id="8f8a3-147">[Trabajar con unidades de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Crear enrutamientos](production-how-to-create-routings.md)</span><span class="sxs-lookup"><span data-stu-id="8f8a3-147">[Work with Manufacturing Batch Units of Measure](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Create Routings](production-how-to-create-routings.md)</span></span>  
[<span data-ttu-id="8f8a3-148">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="8f8a3-148">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)