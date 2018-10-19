---
title: "Configurar una ficha de almacén y definir las rutas de transferencia | Documentos de Microsoft"
description: "Puede crear una ficha de almacén para cada lugar donde almacene productos de inventario, por ejemplo, un almacén o un centro de distribución, y configurar rutas para transferir los productos entre almacenes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 503655e65b7df83c89e52d76a22396b672b2d28e
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="4e225-103">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="4e225-103">Set Up Locations</span></span>
<span data-ttu-id="4e225-104">Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="4e225-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="4e225-105">Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes.</span><span class="sxs-lookup"><span data-stu-id="4e225-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="4e225-106">Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="4e225-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="4e225-107">Para crear una ficha de almacén</span><span class="sxs-lookup"><span data-stu-id="4e225-107">To create a location card</span></span>
1. <span data-ttu-id="4e225-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Ubicaciones** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4e225-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="4e225-109">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="4e225-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="4e225-110">En la ventana **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4e225-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="4e225-111">Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.</span><span class="sxs-lookup"><span data-stu-id="4e225-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="4e225-112">Muchos campos de la ficha de almacén se refieren a la manipulación de productos en los procesos de almacén de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="4e225-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="4e225-113">Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4e225-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="4e225-114">Para crear una ruta de transferencia</span><span class="sxs-lookup"><span data-stu-id="4e225-114">To create a transfer route</span></span>
1. <span data-ttu-id="4e225-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Rutas de transferencia** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4e225-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="4e225-116">Opcionalmente, desde cualquier ventana **Ficha almacén**, elija la acción **Rutas de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="4e225-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="4e225-117">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="4e225-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="4e225-118">En la ventana **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4e225-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="4e225-119">Ahora puede transferir productos de inventario entre dos almacenes.</span><span class="sxs-lookup"><span data-stu-id="4e225-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="4e225-120">Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="4e225-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="4e225-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e225-121">See Also</span></span>
[<span data-ttu-id="4e225-122">Gestionar inventario</span><span class="sxs-lookup"><span data-stu-id="4e225-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4e225-123">[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="4e225-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="4e225-124">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e225-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4e225-125">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="4e225-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="4e225-126">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="4e225-126">General Business Functionality</span></span>](ui-across-business-areas.md)

