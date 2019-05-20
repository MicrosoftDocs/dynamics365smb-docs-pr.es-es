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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244050"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="c5966-104">Usar referencias cruzadas de producto</span><span class="sxs-lookup"><span data-stu-id="c5966-104">Use Item Cross References</span></span>
<span data-ttu-id="c5966-105">Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**.</span><span class="sxs-lookup"><span data-stu-id="c5966-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="c5966-106">.</span><span class="sxs-lookup"><span data-stu-id="c5966-106">field.</span></span> <span data-ttu-id="c5966-107">Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.</span><span class="sxs-lookup"><span data-stu-id="c5966-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="c5966-108">Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra.</span><span class="sxs-lookup"><span data-stu-id="c5966-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="c5966-109">Los pasos son parecidos para la venta.</span><span class="sxs-lookup"><span data-stu-id="c5966-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="c5966-110">Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor</span><span class="sxs-lookup"><span data-stu-id="c5966-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="c5966-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="c5966-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5966-112">Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.</span><span class="sxs-lookup"><span data-stu-id="c5966-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="c5966-113">Seleccione la acción **Referencias cruzadas**.</span><span class="sxs-lookup"><span data-stu-id="c5966-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="c5966-114">En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c5966-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="c5966-115">.</span><span class="sxs-lookup"><span data-stu-id="c5966-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="c5966-116">Para introducir la descripción del producto de un proveedor en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="c5966-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="c5966-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="c5966-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5966-118">Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="c5966-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="c5966-119">Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="c5966-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="c5966-120">En el campo **Nº tipo referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="c5966-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="c5966-121">seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c5966-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="c5966-122">El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.</span><span class="sxs-lookup"><span data-stu-id="c5966-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5966-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5966-123">See Also</span></span>
[<span data-ttu-id="c5966-124">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="c5966-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c5966-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="c5966-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c5966-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c5966-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
