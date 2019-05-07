---
title: Cómo calcular la reposición de ubicaciones | Documentos de Microsoft
description: Cuando la ubicación se configure para utilizar ubicación y picking directos, se tendrán en cuenta las prioridades de la plantilla de ubicación para esa ubicación al situar las recepciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ae66b96665431de66e964384835e7e3b06080345
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "920824"
---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="5f42a-103">Calcular reposición ubicación</span><span class="sxs-lookup"><span data-stu-id="5f42a-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="5f42a-104">Cuando la ubicación se configure para utilizar ubicación y picking directos, se tendrán en cuenta las prioridades de la plantilla de ubicación para esa ubicación al situar las recepciones.</span><span class="sxs-lookup"><span data-stu-id="5f42a-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="5f42a-105">Las prioridades incluyen las cantidades mínimas y máximas de contenido de la ubicación que se han establecido para una ubicación determinada, y los ranking de ubicación.</span><span class="sxs-lookup"><span data-stu-id="5f42a-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="5f42a-106">Por tanto, si llegan productos a un ritmo estable, se rellenarán las ubicaciones de picking más utilizadas en cuanto se vacíen.</span><span class="sxs-lookup"><span data-stu-id="5f42a-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="5f42a-107">Pero las existencias no siempre llegan a un ritmo constante.</span><span class="sxs-lookup"><span data-stu-id="5f42a-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="5f42a-108">A veces, los productos se compran en grandes cantidades por lo que la empresa puede obtener un mejor precio, o su departamento de producción puede fabricar un lote de un producto para conseguir un menor precio de coste unitario.</span><span class="sxs-lookup"><span data-stu-id="5f42a-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="5f42a-109">Así los productos no se volverán a recibir en el almacén durante algún tiempo y el almacén necesita mover productos periódicamente a las ubicaciones de picking desde las áreas de almacenamiento masivas.</span><span class="sxs-lookup"><span data-stu-id="5f42a-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="5f42a-110">También es posible que el almacén espere pronto la llegada de nuevas existencias y desee vaciar el área de almacenamiento masivo de productos antes de que llegue la mueva mercancía.</span><span class="sxs-lookup"><span data-stu-id="5f42a-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="5f42a-111">Finalmente, si ha definido sus ubicaciones de almacenamiento masivo con un tipo de ubicación sólo con la acción **Ubicar**, es decir, que el tipo de ubicación no tiene activada la acción **Picking**, siempre debe mantener las ubicaciones de picking llenas, ya que no se sugerirá un picking de existencias desde ubicaciones de tipo Ubicación.</span><span class="sxs-lookup"><span data-stu-id="5f42a-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="5f42a-112">Para reponer ubicaciones de picking</span><span class="sxs-lookup"><span data-stu-id="5f42a-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="5f42a-113">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trabajo mov.** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="5f42a-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f42a-114">Elija la acción **Calcular reposición ubicación** para abrir la página de solicitud de informes.</span><span class="sxs-lookup"><span data-stu-id="5f42a-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="5f42a-115">Rellene la página del proceso para limitar el alcance de las sugerencias de reposición que se calcularán.</span><span class="sxs-lookup"><span data-stu-id="5f42a-115">Fill in the batch job request page to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="5f42a-116">Por ejemplo, puede que esté preocupado por determinadas zonas, ubicaciones o productos.</span><span class="sxs-lookup"><span data-stu-id="5f42a-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="5f42a-117">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5f42a-117">Choose the **OK** button.</span></span> <span data-ttu-id="5f42a-118">Se crearán líneas para los movimientos de reposición que es necesario realizar según las reglas que se han configurado para las ubicaciones y contenido de ubicaciones, es decir, productos en ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="5f42a-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="5f42a-119">Si desea ejecutar todas las sugerencias de reposición, elija la acción **Crear movimiento**.</span><span class="sxs-lookup"><span data-stu-id="5f42a-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="5f42a-120">Los empleados pueden encontrar instrucciones en el elemento de menú **Movimientos**, ejecutarlas y registrarlas.</span><span class="sxs-lookup"><span data-stu-id="5f42a-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="5f42a-121">Si sólo desea ejecutar algunas sugerencias, elimine las líneas menos importantes y, a continuación, cree un movimiento.</span><span class="sxs-lookup"><span data-stu-id="5f42a-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="5f42a-122">La próxima vez que calcule la reposición de la ubicación, se volverán a crear las sugerencias que ha eliminado, si siguen siendo válidas en ese momento.</span><span class="sxs-lookup"><span data-stu-id="5f42a-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5f42a-123">Si un producto cumple las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="5f42a-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="5f42a-124">El producto tiene fecha de caducidad y</span><span class="sxs-lookup"><span data-stu-id="5f42a-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="5f42a-125">Se selecciona el campo **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén. y</span><span class="sxs-lookup"><span data-stu-id="5f42a-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="5f42a-126">Utilice la funcionalidad **Calcular reposición ubicación**</span><span class="sxs-lookup"><span data-stu-id="5f42a-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="5f42a-127">los campos **Desde zona** y **Desde ubicación** estarán en blanco, ya que el algoritmo para calcular desde dónde se van a mover los productos sólo se ejecuta al activar la función **Crear movimiento**.</span><span class="sxs-lookup"><span data-stu-id="5f42a-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5f42a-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f42a-128">See Also</span></span>  
[<span data-ttu-id="5f42a-129">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="5f42a-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5f42a-130">Realización de picking por el FEFO</span><span class="sxs-lookup"><span data-stu-id="5f42a-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="5f42a-131">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="5f42a-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5f42a-132">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5f42a-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5f42a-133">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5f42a-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5f42a-134">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="5f42a-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5f42a-135">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f42a-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
