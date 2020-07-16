---
title: Cómo configurar plantillas de ubicación | Documentos de Microsoft
description: Con la funcionalidad de ubicación y picking directo, se sugiere la ubicación más adecuada para los productos en un momento determinado, según la plantilla de ubicación que ha configurado para el almacén, los rankings que ha dado a las ubicaciones y las cantidades máxima y mínima que ha definido para las ubicaciones fijas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: 46dc891937ec4046a0403ca418296d1d7ee24a99
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529318"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="ad170-103">Configurar plantillas de ubicación</span><span class="sxs-lookup"><span data-stu-id="ad170-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="ad170-104">Con la funcionalidad de ubicación y picking directo, se sugiere la ubicación más adecuada para los productos en un momento determinado, según la plantilla de ubicación que ha configurado para el almacén, los rankings que ha dado a las ubicaciones y las cantidades máxima y mínima que ha definido para las ubicaciones fijas.</span><span class="sxs-lookup"><span data-stu-id="ad170-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="ad170-105">Puede configurar varias plantillas de ubicación y seleccionar una para controlar las ubicaciones en general en el almacén.</span><span class="sxs-lookup"><span data-stu-id="ad170-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="ad170-106">También puede seleccionar una plantilla de ubicación para cualquier producto o unidad de almacenamiento que tenga unos requisitos de ubicación especiales.</span><span class="sxs-lookup"><span data-stu-id="ad170-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="ad170-107">Para configurar las plantillas de ubicación</span><span class="sxs-lookup"><span data-stu-id="ad170-107">To set up put-away templates</span></span>

1. <span data-ttu-id="ad170-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plantillas de ubicación** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ad170-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ad170-109">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ad170-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ad170-110">Escriba un código que sea el identificador exclusivo de la plantilla que va a crear.</span><span class="sxs-lookup"><span data-stu-id="ad170-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="ad170-111">Escriba una breve descripción, si lo desea.</span><span class="sxs-lookup"><span data-stu-id="ad170-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="ad170-112">Rellene la primera línea con los requisitos de la ubicación que desea que se rellenen en primer lugar cuando se sugiera una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad170-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="ad170-113">Por ejemplo, si desea que el método de almacenamiento predeterminado se base en ubicaciones fijas, elija el campo **Buscar ubicación fija**.</span><span class="sxs-lookup"><span data-stu-id="ad170-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="ad170-114">Rellene la segunda línea con los requisitos de ubicación que serán la segunda opción a seguir para utilizar esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad170-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="ad170-115">El programa sólo se utilizará si no encuentra una ubicación que cumpla los requisitos de la primera línea.</span><span class="sxs-lookup"><span data-stu-id="ad170-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="ad170-116">Continúe rellenando las líneas hasta que haya descrito todos los lugares de ubicación adecuados que desea utilizar en el proceso de ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad170-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="ad170-117">En la última línea de la plantilla de ubicación, seleccione la casilla **Busca ubicación aleatoria**.</span><span class="sxs-lookup"><span data-stu-id="ad170-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="ad170-118">Puede crear varias plantillas de ubicación y, a continuación, aplicarlas como necesite.</span><span class="sxs-lookup"><span data-stu-id="ad170-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="ad170-119">Se utilizará primero la plantilla de ubicación que ha seleccionado para el producto o unidad de almacenamiento, si existe.</span><span class="sxs-lookup"><span data-stu-id="ad170-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="ad170-120">Si estos campos no están rellenos, se utilizará la plantilla que ha seleccionado para el almacén en la ficha desplegable **Políticas ubic.** de la ficha de almacén.</span><span class="sxs-lookup"><span data-stu-id="ad170-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ad170-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad170-121">See Also</span></span>

[<span data-ttu-id="ad170-122">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="ad170-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ad170-123">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="ad170-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ad170-124">Configuración de la gestión del almacén</span><span class="sxs-lookup"><span data-stu-id="ad170-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="ad170-125">Gestión de ensamblaje</span><span class="sxs-lookup"><span data-stu-id="ad170-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="ad170-126">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="ad170-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ad170-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ad170-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
