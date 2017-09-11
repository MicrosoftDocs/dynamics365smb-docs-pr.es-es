---
title: "Configurar una ficha de almacén y definir las rutas de transferencia | Documentos de Microsoft"
description: "Puede crear una ficha de almacén para cada lugar donde almacene productos de inventario, por ejemplo, un almacén o un centro de distribución, y configurar rutas para transferir los productos entre almacenes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 146fc08f389a5c068044358c59b7d8911f0b3343
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-locations"></a><span data-ttu-id="ae810-103">Configuración de almacenes</span><span class="sxs-lookup"><span data-stu-id="ae810-103">How to: Set Up Locations</span></span>
<span data-ttu-id="ae810-104">Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="ae810-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="ae810-105">Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes.</span><span class="sxs-lookup"><span data-stu-id="ae810-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="ae810-106">Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="ae810-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="ae810-107">Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="ae810-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="ae810-108">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="ae810-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="ae810-109">Para crear una ficha de almacén</span><span class="sxs-lookup"><span data-stu-id="ae810-109">To create a location card</span></span>
1. <span data-ttu-id="ae810-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae810-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae810-111">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ae810-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="ae810-112">En la ventana **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ae810-112">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="ae810-113">Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.</span><span class="sxs-lookup"><span data-stu-id="ae810-113">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="ae810-114">Para crear una ruta de transferencia</span><span class="sxs-lookup"><span data-stu-id="ae810-114">To create a transfer route</span></span>
1. <span data-ttu-id="ae810-115">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Rutas de transferencia** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ae810-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae810-116">Opcionalmente, desde cualquier ventana **Ficha almacén**, elija la acción **Rutas de transferencia**.</span><span class="sxs-lookup"><span data-stu-id="ae810-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="ae810-117">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ae810-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="ae810-118">En la ventana **Ficha de almacén**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ae810-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="ae810-119">Ahora puede transferir productos de inventario entre dos almacenes.</span><span class="sxs-lookup"><span data-stu-id="ae810-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="ae810-120">Para obtener más información, vea [Procedimiento: Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="ae810-120">For more information, see [How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="ae810-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae810-121">See Also</span></span>
[<span data-ttu-id="ae810-122">Gestionar inventario</span><span class="sxs-lookup"><span data-stu-id="ae810-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ae810-123">Cadena de suministro</span><span class="sxs-lookup"><span data-stu-id="ae810-123">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="ae810-124">[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="ae810-124">[How to: Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="ae810-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae810-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="ae810-126">[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="ae810-126">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="ae810-127">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="ae810-127">General Business Functionality</span></span>](ui-across-business-areas.md)

