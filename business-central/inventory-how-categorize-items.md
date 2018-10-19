---
title: "Organizar los productos en categorías | Documentos de Microsoft"
description: "Como ayuda para buscar y encontrar productos, puede asignar atributos de producto y organizar los productos en categorías."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c62d26dc9dc444359c0d8b5a9354b29132857de1
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="categorize-items"></a><span data-ttu-id="0fe20-103">Clasificar productos</span><span class="sxs-lookup"><span data-stu-id="0fe20-103">Categorize Items</span></span>
<span data-ttu-id="0fe20-104">Para mantener una visión general de sus productos y ayudarle a ordenar y encontrar los productos, es muy útil organizar los productos en categorías.</span><span class="sxs-lookup"><span data-stu-id="0fe20-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="0fe20-105">Para buscar productos por características, puede asignar los atributos de producto a los productos y también a las categorías.</span><span class="sxs-lookup"><span data-stu-id="0fe20-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="0fe20-106">Para obtener más información sobre cómo trabajar con el formulario, consulte [Trabajar con atributos de producto](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0fe20-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="0fe20-107">Para crear una categoría de producto</span><span class="sxs-lookup"><span data-stu-id="0fe20-107">To create an item category</span></span>
1. <span data-ttu-id="0fe20-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Categorías producto** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0fe20-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="0fe20-109">En la ventana **Categorías de producto**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="0fe20-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="0fe20-110">En la ficha desplegable **General** de la ventana **Ficha de categoría de producto**, complete los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0fe20-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="0fe20-111">En la ficha desplegable **Atributos**, especifique atributos de producto a la categoría.</span><span class="sxs-lookup"><span data-stu-id="0fe20-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="0fe20-112">Para obtener más información, vea la sección "Para asignar atributos de producto a una categoría" en [Trabajar con atributos de producto](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0fe20-112">For more information, see the "To assign item attributes to an item category" section in [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="0fe20-113">Si la categoría del producto tiene una categoría principal, como se indica en el campo **Categoría principal**, todos los atributos que se asignen a esa categoría principal se rellenan previamente en la ficha desplegable **Atributos**.</span><span class="sxs-lookup"><span data-stu-id="0fe20-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0fe20-114">Los atributos de producto que asigna a una categoría se aplicarán automáticamente al producto al que se le ha asignado la categoría.</span><span class="sxs-lookup"><span data-stu-id="0fe20-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="0fe20-115">Para asignar una categoría de producto a un producto</span><span class="sxs-lookup"><span data-stu-id="0fe20-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="0fe20-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0fe20-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="0fe20-117">Abra la ficha del producto al que desee asignar una categoría de producto.</span><span class="sxs-lookup"><span data-stu-id="0fe20-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="0fe20-118">Elija el botón de búsqueda en el campo **Cód. categoría producto** y seleccione una categoría existente.</span><span class="sxs-lookup"><span data-stu-id="0fe20-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="0fe20-119">De forma alternativa, elija la acción **Nuevo** para crear primero una nueva categoría de producto como se explica en la sección "Para crear una categoría de producto".</span><span class="sxs-lookup"><span data-stu-id="0fe20-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fe20-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0fe20-120">See Also</span></span>
[<span data-ttu-id="0fe20-121">Trabajar con atributos de producto</span><span class="sxs-lookup"><span data-stu-id="0fe20-121">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="0fe20-122">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="0fe20-122">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0fe20-123">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="0fe20-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0fe20-124">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0fe20-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

