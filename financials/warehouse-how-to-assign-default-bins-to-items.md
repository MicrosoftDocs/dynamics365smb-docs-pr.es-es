---
title: 'Procedimiento: Asignar las ubicaciones predefinidas a los productos | Documentos de Microsoft'
description: "Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 826e1392143b166566619c5aef8c28ac2b09bc22
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="bc09a-104">Asignar las ubicaciones predefinidas a los productos</span><span class="sxs-lookup"><span data-stu-id="bc09a-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="bc09a-105">Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos.</span><span class="sxs-lookup"><span data-stu-id="bc09a-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="bc09a-106">Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto.</span><span class="sxs-lookup"><span data-stu-id="bc09a-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="bc09a-107">Las ubicaciones genéricas se definen en la ventana **Contenido ubicación**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="bc09a-108">Asignar una ubicación predeterminada a un producto</span><span class="sxs-lookup"><span data-stu-id="bc09a-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="bc09a-109">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja trabajo creación contenido ubicación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="bc09a-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="bc09a-110">Rellene la información del código de ubicación y del artículo para cada ubicación que desee configurar como valor predeterminado para un artículo.</span><span class="sxs-lookup"><span data-stu-id="bc09a-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="bc09a-111">Asegúrese de seleccionar el campo **Predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="bc09a-112">Seleccione la acción **Crear contenido ubicación**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="bc09a-113">Las ubicaciones ya están asignadas a su producto.</span><span class="sxs-lookup"><span data-stu-id="bc09a-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bc09a-114">Cuando se ubica un producto, si el producto no tiene asignada una ubicación genérica, se asignará aquélla en la que se ubique como genérica.</span><span class="sxs-lookup"><span data-stu-id="bc09a-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="bc09a-115">Para cambiar las ubicaciones predefinidas de los productos</span><span class="sxs-lookup"><span data-stu-id="bc09a-115">To change the default bin for an item</span></span>  
<span data-ttu-id="bc09a-116">Puede que tenga que cambiar la asignación de la ubicación predeterminada de un artículo o que tenga que asignar una ubicación predeterminada a un artículo nuevo.</span><span class="sxs-lookup"><span data-stu-id="bc09a-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="bc09a-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contenidos ubicación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="bc09a-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bc09a-118">En el campo **Filtro almacén**, seleccione el código de almacén correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bc09a-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="bc09a-119">Busque el movimiento de contenido de ubicación actual del producto y desactive la casilla **Genérica**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="bc09a-120">Busque la línea de contenido de la ubicación que desea que sea la nueva ubicación genérica.</span><span class="sxs-lookup"><span data-stu-id="bc09a-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="bc09a-121">Seleccione la casilla de verificación **Ubicación predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="bc09a-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bc09a-122">Cuando se ubica un producto por primera vez, si el producto no tienen asignada una ubicación genérica, el programa asignará la ubicación como ubicación genérica del producto.</span><span class="sxs-lookup"><span data-stu-id="bc09a-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bc09a-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc09a-123">See Also</span></span>  
[<span data-ttu-id="bc09a-124">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="bc09a-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="bc09a-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="bc09a-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="bc09a-126">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="bc09a-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="bc09a-127">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="bc09a-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="bc09a-128">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="bc09a-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="bc09a-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bc09a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

