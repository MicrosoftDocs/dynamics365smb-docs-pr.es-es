---
title: 'Procedimiento: Asignar las ubicaciones predefinidas a los productos | Documentos de Microsoft'
description: Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto.
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
ms.openlocfilehash: 0eb6dc74d9ac050c692c003799c3142bdbdaeeaa
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "927907"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="77db1-104">Asignar las ubicaciones predefinidas a los productos</span><span class="sxs-lookup"><span data-stu-id="77db1-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="77db1-105">Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos.</span><span class="sxs-lookup"><span data-stu-id="77db1-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="77db1-106">Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto.</span><span class="sxs-lookup"><span data-stu-id="77db1-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="77db1-107">Las ubicaciones genéricas se definen en la página **Contenido ubicación**.</span><span class="sxs-lookup"><span data-stu-id="77db1-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="77db1-108">Asignar una ubicación predeterminada a un producto</span><span class="sxs-lookup"><span data-stu-id="77db1-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="77db1-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trab. creac. cont. ubic.** y elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="77db1-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="77db1-110">Rellene la información del código de ubicación y del artículo para cada ubicación que desee configurar como valor predeterminado para un artículo.</span><span class="sxs-lookup"><span data-stu-id="77db1-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="77db1-111">Asegúrese de seleccionar el campo **Predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="77db1-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="77db1-112">Seleccione la acción **Crear contenido ubicación**.</span><span class="sxs-lookup"><span data-stu-id="77db1-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="77db1-113">Las ubicaciones ya están asignadas a su producto.</span><span class="sxs-lookup"><span data-stu-id="77db1-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="77db1-114">Cuando se ubica un producto, si el producto no tiene asignada una ubicación genérica, se asignará aquélla en la que se ubique como genérica.</span><span class="sxs-lookup"><span data-stu-id="77db1-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="77db1-115">Para cambiar las ubicaciones predefinidas de los productos</span><span class="sxs-lookup"><span data-stu-id="77db1-115">To change the default bin for an item</span></span>  
<span data-ttu-id="77db1-116">Puede que tenga que cambiar la asignación de la ubicación predeterminada de un artículo o que tenga que asignar una ubicación predeterminada a un artículo nuevo.</span><span class="sxs-lookup"><span data-stu-id="77db1-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="77db1-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contenidos ubicación** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="77db1-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="77db1-118">En el campo **Filtro almacén**, seleccione el código de almacén correspondiente.</span><span class="sxs-lookup"><span data-stu-id="77db1-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="77db1-119">Busque el movimiento de contenido de ubicación actual del producto y desactive la casilla **Genérica**.</span><span class="sxs-lookup"><span data-stu-id="77db1-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="77db1-120">Busque la línea de contenido de la ubicación que desea que sea la nueva ubicación genérica.</span><span class="sxs-lookup"><span data-stu-id="77db1-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="77db1-121">Seleccione la casilla de verificación **Ubicación predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="77db1-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="77db1-122">Cuando se ubica un producto por primera vez, si el producto no tienen asignada una ubicación genérica, el programa asignará la ubicación como ubicación genérica del producto.</span><span class="sxs-lookup"><span data-stu-id="77db1-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="77db1-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="77db1-123">See Also</span></span>  
[<span data-ttu-id="77db1-124">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="77db1-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="77db1-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="77db1-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="77db1-126">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="77db1-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="77db1-127">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="77db1-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="77db1-128">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="77db1-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="77db1-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="77db1-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
