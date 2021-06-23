---
title: Configurar una ficha de almacén y definir las rutas de transferencia
description: Puede crear una ficha de almacén para cada lugar donde almacene productos de inventario, por ejemplo, un almacén o un centro de distribución, y configurar rutas para transferir los productos entre almacenes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184329"
---
# <a name="set-up-locations"></a><span data-ttu-id="cf06b-103">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="cf06b-103">Set Up Locations</span></span>

<span data-ttu-id="cf06b-104">Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="cf06b-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="cf06b-105">[!INCLUDE [prod_short](includes/prod_short.md)] utiliza ubicaciones para ayudar a realizar un seguimiento del inventario tanto en los casos más simples como en los procesos de almacén más complejos.</span><span class="sxs-lookup"><span data-stu-id="cf06b-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="cf06b-106">Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes.</span><span class="sxs-lookup"><span data-stu-id="cf06b-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="cf06b-107">Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="cf06b-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="cf06b-108">Fichas de almacén</span><span class="sxs-lookup"><span data-stu-id="cf06b-108">Location cards</span></span>

<span data-ttu-id="cf06b-109">La ficha de almacén especifica información sobre una ubicación, como un almacén o un centro de distribución.</span><span class="sxs-lookup"><span data-stu-id="cf06b-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="cf06b-110">Proporcione un nombre y un código que represente a cada almacén.</span><span class="sxs-lookup"><span data-stu-id="cf06b-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="cf06b-111">A continuación, puede introducir el código de almacén en otras partes del sistema cuando desee registrar transacciones de un almacén determinado.</span><span class="sxs-lookup"><span data-stu-id="cf06b-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="cf06b-112">Puede introducir información sobre ubicaciones y políticas de almacén para cada almacén.</span><span class="sxs-lookup"><span data-stu-id="cf06b-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="cf06b-113">Basándose en las políticas de almacén que seleccione, puede utilizar las opciones de la ficha desplegable **Ubic**. para definir las ubicaciones que se utilizarán como genéricas al realizar transacciones.</span><span class="sxs-lookup"><span data-stu-id="cf06b-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="cf06b-114">Si utiliza ubicación y picking directos, puede usar la mayoría de las opciones de la ficha desplegable **Políticas ubic.** para definir cómo desea utilizar las diversas funcionalidades ampliadas de almacén.</span><span class="sxs-lookup"><span data-stu-id="cf06b-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="cf06b-115">Algunos campos de opción están grises y deshabilitados por otras opciones en la página **Ficha almacén** para restringir las combinaciones de configuración no compatibles.</span><span class="sxs-lookup"><span data-stu-id="cf06b-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="cf06b-116">Seleccione la acción **Zonas** o **Ubicaciones** para ver información acerca de las zonas y ubicaciones que se pueden definir para el almacén.</span><span class="sxs-lookup"><span data-stu-id="cf06b-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="cf06b-117">Para crear una ficha de almacén</span><span class="sxs-lookup"><span data-stu-id="cf06b-117">To create a location card</span></span>

1. <span data-ttu-id="cf06b-118">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="cf06b-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf06b-119">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="cf06b-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="cf06b-120">En la página **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cf06b-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cf06b-121">Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.</span><span class="sxs-lookup"><span data-stu-id="cf06b-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="cf06b-122">Muchos campos de la ficha de almacén se refieren a la manipulación de productos en los procesos de almacén de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="cf06b-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="cf06b-123">Los campos no son relevantes para empresas que no requieren funcionalidades de almacén más complejas.</span><span class="sxs-lookup"><span data-stu-id="cf06b-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="cf06b-124">Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="cf06b-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="cf06b-125">Puede cambiar la configuración de una ubicación más adelante, pero no puede editar la configuración de las ubicaciones que tienen movimientos contables de productos.</span><span class="sxs-lookup"><span data-stu-id="cf06b-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="cf06b-126">A continuación, si tiene varios almacenes, puede definir rutas de transferencia entre almacenes.</span><span class="sxs-lookup"><span data-stu-id="cf06b-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="cf06b-127">Para crear una ruta de transferencia</span><span class="sxs-lookup"><span data-stu-id="cf06b-127">To create a transfer route</span></span>

1. <span data-ttu-id="cf06b-128">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas de transferencia** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="cf06b-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf06b-129">Opcionalmente, desde cualquier página **Ficha almacén**, elija la acción **Rutas de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="cf06b-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="cf06b-130">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="cf06b-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="cf06b-131">En la página **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cf06b-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="cf06b-132">Ahora puede transferir productos de inventario entre dos almacenes.</span><span class="sxs-lookup"><span data-stu-id="cf06b-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="cf06b-133">Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="cf06b-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="cf06b-134">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="cf06b-134">Bins</span></span>

<span data-ttu-id="cf06b-135">Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos.</span><span class="sxs-lookup"><span data-stu-id="cf06b-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="cf06b-136">Cuando haya creado sus ubicaciones, puede definir con precisión el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico.</span><span class="sxs-lookup"><span data-stu-id="cf06b-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="cf06b-137">Las ubicaciones se utilizan principalmente en operaciones de almacén básicas y avanzadas.</span><span class="sxs-lookup"><span data-stu-id="cf06b-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="cf06b-138">Si administra el inventario en una configuración más sencilla, probablemente no necesite ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="cf06b-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="cf06b-139">Para utilizar la función de contenedor en una ubicación, primero active la función en la ficha **Almacén** seleccionando el campo **Ubicaciones obligatorias** en la ficha desplegable **Almacén**.</span><span class="sxs-lookup"><span data-stu-id="cf06b-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="cf06b-140">A continuación podrá diseñar el flujo del artículo en la ubicación especificando los códigos de ubicación en los campos de instalación que representan a los distintos flujos.</span><span class="sxs-lookup"><span data-stu-id="cf06b-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="cf06b-141">Para poder especificar los códigos de ubicación en la ficha de almacén, deben crearse.</span><span class="sxs-lookup"><span data-stu-id="cf06b-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="cf06b-142">Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md) y [Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="cf06b-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="cf06b-143">Zonas</span><span class="sxs-lookup"><span data-stu-id="cf06b-143">Zones</span></span>

<span data-ttu-id="cf06b-144">Si desea estructurar sus ubicaciones en zonas, puede hacerlo en la página **Zonas**.</span><span class="sxs-lookup"><span data-stu-id="cf06b-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="cf06b-145">[!INCLUDE [prod_short](includes/prod_short.md)] copia los campos que ha definido para una zona determinada se copian en las ubicaciones de la misma.</span><span class="sxs-lookup"><span data-stu-id="cf06b-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="cf06b-146">De esta forma, puede asignar una zona a una ubicación o a una plantilla de ubicación (filtro de creación de ubicación) y otros campos se rellenarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cf06b-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="cf06b-147">No obstante, puede configurar sólo una zona y organizar el almacén según ubicaciones independientes.</span><span class="sxs-lookup"><span data-stu-id="cf06b-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="cf06b-148">Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="cf06b-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf06b-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf06b-149">See Also</span></span>

[<span data-ttu-id="cf06b-150">Gestionar inventario</span><span class="sxs-lookup"><span data-stu-id="cf06b-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cf06b-151">Transferir el inventario entre almacenes</span><span class="sxs-lookup"><span data-stu-id="cf06b-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="cf06b-152">Crear ubicaciones</span><span class="sxs-lookup"><span data-stu-id="cf06b-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="cf06b-153">Configurar tipos de ubicación</span><span class="sxs-lookup"><span data-stu-id="cf06b-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="cf06b-154">Configuración de la gestión del almacén</span><span class="sxs-lookup"><span data-stu-id="cf06b-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="cf06b-155">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf06b-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cf06b-156">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="cf06b-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="cf06b-157">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="cf06b-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]