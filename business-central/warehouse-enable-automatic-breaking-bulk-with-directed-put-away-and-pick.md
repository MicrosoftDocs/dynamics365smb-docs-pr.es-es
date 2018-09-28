---
title: "Interrupción automática masiva con picking y ubicaciones directas | Documentos de Microsoft"
description: "En almacenes que utilizan ubicación y picking directos, puede dividir una unidad de medida grande en otras unidades de medida más pequeñas, cuando crea instrucciones de almacén que cubren las necesidades de los documentos de origen, órdenes de producción o ubicaciones y picking internos."
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
ms.openlocfilehash: 38a7db3aa4884c1fc5a5d3a3b6e7f9c942673b3c
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="9799e-103">Habilitar interrupción automática masiva con ubicaciones y picking directos</span><span class="sxs-lookup"><span data-stu-id="9799e-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="9799e-104">En almacenes que utilizan ubicación y picking directos, [!INCLUDE[d365fin](includes/d365fin_md.md)] puede dividir los bultos automáticamente, es decir, dividir una unidad de medida grande en otras unidades de medida más pequeñas, cuando crea instrucciones de almacén que cubren las necesidades de los documentos de origen, órdenes de producción o ubicaciones y picking internos.</span><span class="sxs-lookup"><span data-stu-id="9799e-104">For locations that use directed put-away and pick, [!INCLUDE[d365fin](includes/d365fin_md.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="9799e-105">A veces, dividir bultos también significa reunir unidades de medida menores, si es necesario, para cumplir las solicitudes de salida dividiendo una unidad de medida grande del documento de origen u orden de producción en unidades de medida menores que están disponibles en el almacén.</span><span class="sxs-lookup"><span data-stu-id="9799e-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="9799e-106">Dividir bultos en picking</span><span class="sxs-lookup"><span data-stu-id="9799e-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="9799e-107">Si desea almacenar productos en varias unidades de medida distintas y permitir que se combinen automáticamente según las necesidades en el proceso de picking, seleccione el campo **Permite división bulto** de la ficha de almacén.</span><span class="sxs-lookup"><span data-stu-id="9799e-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="9799e-108">Para cubrir una tarea, el programa busca automáticamente un producto en la misma unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="9799e-108">To fulfill a task, the program automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="9799e-109">Pero si no encuentra este formato de producto, y ha seleccionado el campo, el programa sugerirá que divida una unidad de medida grande en las unidades de medida necesarias.</span><span class="sxs-lookup"><span data-stu-id="9799e-109">But if it cannot find this form of the item, and this field is selected, the program will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="9799e-110">Si el sistema sólo encuentra unidades de medida pequeñas, sugerirá que reúna productos para hacer frente a la cantidad de la recepción o la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="9799e-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="9799e-111">De hecho, divide la unidad de medida grande del documento de origen en unidades menores para el picking.</span><span class="sxs-lookup"><span data-stu-id="9799e-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="9799e-112">Dividir bultos en ubicaciones</span><span class="sxs-lookup"><span data-stu-id="9799e-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="9799e-113">En la ubicación de almacén, el programa sugiere automáticamente líneas de acción de apartado en la unidad de medida de ubicación, por ejemplo, piezas, aunque los productos hayan llegado en una unidad de medida diferente.</span><span class="sxs-lookup"><span data-stu-id="9799e-113">In the warehouse put-away, the program automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="9799e-114">Dividir bultos en movimientos</span><span class="sxs-lookup"><span data-stu-id="9799e-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="9799e-115">El programa también realiza la división de bultos automáticamente en los movimientos de reposición, si el campo **Permitir división bulto** está seleccionado en la ficha desplegable **Opción** de la ventana **Calcular reposición ubicación**.</span><span class="sxs-lookup"><span data-stu-id="9799e-115">The program also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab in the **Calculate Bin Replenishment** window.</span></span>  

<span data-ttu-id="9799e-116">Puede ver el resultado del proceso de conversión de una unidad de medida a otra como líneas de división de bulto intermedias en las instrucciones de movimiento, picking o ubicación.</span><span class="sxs-lookup"><span data-stu-id="9799e-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9799e-117">Si selecciona el campo **Define filtro div. bulto** en la cabecera de instrucciones del almacén, el programa ocultará las líneas de división de bultos siempre que se utilice íntegramente la unidad de medida más grande.</span><span class="sxs-lookup"><span data-stu-id="9799e-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, the program will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="9799e-118">Por ejemplo, si un palé tiene 12 unidades y va a utilizar esas 12 unidades, el picking indicará que utilice 1 palé y que coloque 12 unidades.</span><span class="sxs-lookup"><span data-stu-id="9799e-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="9799e-119">No obstante, si sólo tiene que hacer picking de 9 unidades, no se ocultarán las líneas de división de bultos, aunque haya seleccionado el campo **Filtro división de bultos**, porque ha colocado las tres unidades restantes en alguna parte del almacén.</span><span class="sxs-lookup"><span data-stu-id="9799e-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9799e-120">Si desea que sus unidades de medida se distribuyan de una forma óptima en el almacén, junto con la funcionalidad de división de bultos, debería intentar:</span><span class="sxs-lookup"><span data-stu-id="9799e-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="9799e-121">Configurar la unidad de medida base de un producto según la unidad de medida más pequeña que espera manipular en los procesos de almacén.</span><span class="sxs-lookup"><span data-stu-id="9799e-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="9799e-122">Configurar unidades de medida alternativas del producto como múltiplos de la unidad de medida base.</span><span class="sxs-lookup"><span data-stu-id="9799e-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9799e-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9799e-123">See Also</span></span>  
[<span data-ttu-id="9799e-124">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="9799e-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="9799e-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="9799e-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9799e-126">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="9799e-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="9799e-127">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="9799e-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="9799e-128">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="9799e-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="9799e-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9799e-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

