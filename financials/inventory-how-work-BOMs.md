---
title: Trabajar con listas de materiales para administrar componentes | Documentos de Microsoft
description: La lista de materiales de ensamblado se crea para especificar los componentes o los recursos necesarios para combinar el producto que representa la lista de materiales de ensamblado, y se pueden ver los componentes de un elemento de ensamblado.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="baff1-103">Trabajar con listas de materiales</span><span class="sxs-lookup"><span data-stu-id="baff1-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="baff1-104">La versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] solo contiene la primera parte de la función de administración de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="baff1-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="baff1-105">Por el momento, solo puede crear listas de materiales de ensamblados y gestionar los productos principales relacionados como productos de inventario normales.</span><span class="sxs-lookup"><span data-stu-id="baff1-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="baff1-106">En una actualización futura, podrá administrar el ensamblado real de productos desde los componentes, en los flujos ensamblar para stock o ensamblar para pedido, y puede vender componentes como kits.</span><span class="sxs-lookup"><span data-stu-id="baff1-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="baff1-107">Utilice listas de materiales para estructurar los productos principales que vende como kits que constan de los componentes del principal o que ensamble para pedido o para stock.</span><span class="sxs-lookup"><span data-stu-id="baff1-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="baff1-108">En [!INCLUDE[d365fin](includes/d365fin_md.md)], una lista de materiales se denomina "L.M. de ensamblado".</span><span class="sxs-lookup"><span data-stu-id="baff1-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="baff1-109">Las L.M. de ensamblado especifican los componentes que contienen las líneas principales.</span><span class="sxs-lookup"><span data-stu-id="baff1-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="baff1-110">En esta documentación, un producto principal se denomina "elemento del ensamblado".</span><span class="sxs-lookup"><span data-stu-id="baff1-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="baff1-111">Las L.M. de ensamblado normalmente contienen productos pero también pueden contener uno o varios recursos que son necesarios para que combinar el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="baff1-112">Las L.M. de ensamblado pueden tener varios niveles, lo que significa que un componente de la L.M. de ensamblado puede ser un elemento del ensamblado en sí.</span><span class="sxs-lookup"><span data-stu-id="baff1-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="baff1-113">En ese caso, el campo **L.M. de ensamblado** en la línea de L.M. de producto contiene **Sí**.</span><span class="sxs-lookup"><span data-stu-id="baff1-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="baff1-114">Se aplican requisitos especiales a los productos de la L.M. de ensamblado en lo que respecta a la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="baff1-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="baff1-115">Para obtener más información, vea la sección "Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado" en [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="baff1-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="baff1-116">Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="baff1-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="baff1-117">Para obtener más información, consulte [Personalizar la experiencia de Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="baff1-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="baff1-118">Para crear una L.M. de ensamblado</span><span class="sxs-lookup"><span data-stu-id="baff1-118">To create an assembly BOM</span></span>
<span data-ttu-id="baff1-119">Para definir un producto principal que conste de otros productos y, potencialmente, de recursos necesarios para combinar el principal, debe crear una L.M. de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="baff1-120">Existen dos partes para crear una L.M. de ensamblado:</span><span class="sxs-lookup"><span data-stu-id="baff1-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="baff1-121">Configuración de un producto nuevo</span><span class="sxs-lookup"><span data-stu-id="baff1-121">Setting up a new item</span></span>
- <span data-ttu-id="baff1-122">Definición de la estructura de la lista de materiales del elemento del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="baff1-123">Configure un producto nuevo.</span><span class="sxs-lookup"><span data-stu-id="baff1-123">Set up a new item.</span></span> <span data-ttu-id="baff1-124">Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="baff1-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="baff1-125">Continúe para introducir los componentes o recursos en la L.M. de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="baff1-126">En la ventana **Ficha producto** de un elemento del ensamblado, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.</span><span class="sxs-lookup"><span data-stu-id="baff1-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="baff1-127">En la ventana **L.M. de ensamblado**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="baff1-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="baff1-128">Para ver los componentes de un elemento del ensamblado con sangría según la estructura de la L.M.</span><span class="sxs-lookup"><span data-stu-id="baff1-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="baff1-129">En la ventana **L.M. de ensamblado** puede abrir una ventana independiente que muestre que los componentes y cualquier recurso con sangría de acuerdo con la posición de la L.M. debajo del elemento del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="baff1-130">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="baff1-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="baff1-131">Abra la ficha de un elemento del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="baff1-131">Open the card for an assembly item.</span></span> <span data-ttu-id="baff1-132">(El campo **L.M. de ensamblado** de la ventana **Productos** contiene **Sí**).</span><span class="sxs-lookup"><span data-stu-id="baff1-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="baff1-133">En la ventana **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.</span><span class="sxs-lookup"><span data-stu-id="baff1-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="baff1-134">En la ventana **L.M. de ensamblado**, elija la acción **Mostrar L.M.**.</span><span class="sxs-lookup"><span data-stu-id="baff1-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="baff1-135">Para comprar, vender o transferir elementos del ensamblado</span><span class="sxs-lookup"><span data-stu-id="baff1-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="baff1-136">Como la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] solo contiene la capacidad de definir y asignar la L.M. de ensamblado a productos, puede manipular los elementos del ensamblado en las líneas de documento como productos normales únicamente.</span><span class="sxs-lookup"><span data-stu-id="baff1-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="baff1-137">**Precaución**: La cantidad de existencias de los componentes de la L.M. no se ajustará si lo hace así.</span><span class="sxs-lookup"><span data-stu-id="baff1-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="baff1-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="baff1-138">See Also</span></span>
[<span data-ttu-id="baff1-139">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="baff1-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="baff1-140">[Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="baff1-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="baff1-141">Inventario</span><span class="sxs-lookup"><span data-stu-id="baff1-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="baff1-142">[Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="baff1-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

