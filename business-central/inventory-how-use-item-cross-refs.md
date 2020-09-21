---
title: Uso de referencias cruzadas de productos | Documentos de Microsoft
description: Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2c676af23e5a6e988ab5d89d07118b9ff1cce86b
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777966"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="b5aa1-104">Usar referencias cruzadas de producto</span><span class="sxs-lookup"><span data-stu-id="b5aa1-104">Use Item Cross References</span></span>
<span data-ttu-id="b5aa1-105">Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="b5aa1-106">.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-106">field.</span></span> <span data-ttu-id="b5aa1-107">Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="b5aa1-108">Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="b5aa1-109">Los pasos son parecidos para la venta.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="b5aa1-110">Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b5aa1-110">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="b5aa1-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b5aa1-112">Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="b5aa1-113">Seleccione la acción **Referencias cruzadas**.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-113">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="b5aa1-114">Si no puede encontrar la acción **Referencias cruzadas**, elija ver más opciones y luego búsquela en **Navegar**, **Producto**.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-114">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Navigate**, **Item**.</span></span>
  
4. <span data-ttu-id="b5aa1-115">En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-115">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="b5aa1-116">.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-116">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="b5aa1-117">Para introducir la descripción del producto de un proveedor en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="b5aa1-117">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="b5aa1-118">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b5aa1-119">Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-119">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="b5aa1-120">Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-120">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="b5aa1-121">En el campo **Nº tipo referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="b5aa1-121">In the **Cross-Reference No.**</span></span> <span data-ttu-id="b5aa1-122">seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-122">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="b5aa1-123">El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.</span><span class="sxs-lookup"><span data-stu-id="b5aa1-123">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5aa1-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5aa1-124">See Also</span></span>
[<span data-ttu-id="b5aa1-125">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="b5aa1-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b5aa1-126">Inventario</span><span class="sxs-lookup"><span data-stu-id="b5aa1-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b5aa1-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b5aa1-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
