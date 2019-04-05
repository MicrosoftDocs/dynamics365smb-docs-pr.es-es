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
ms.date: 03/12/2019
ms.author: sgroespe
ms.openlocfilehash: 09fb7c17e2fccbd3b2ad3195cffa37493ad40f61
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2019
ms.locfileid: "852268"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="f7f69-104">Usar referencias cruzadas de producto</span><span class="sxs-lookup"><span data-stu-id="f7f69-104">Use Item Cross References</span></span>
<span data-ttu-id="f7f69-105">Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**.</span><span class="sxs-lookup"><span data-stu-id="f7f69-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="f7f69-106">.</span><span class="sxs-lookup"><span data-stu-id="f7f69-106">field.</span></span> <span data-ttu-id="f7f69-107">Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.</span><span class="sxs-lookup"><span data-stu-id="f7f69-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="f7f69-108">Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra.</span><span class="sxs-lookup"><span data-stu-id="f7f69-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="f7f69-109">Los pasos son parecidos para la venta.</span><span class="sxs-lookup"><span data-stu-id="f7f69-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="f7f69-110">Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor</span><span class="sxs-lookup"><span data-stu-id="f7f69-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="f7f69-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7f69-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7f69-112">Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.</span><span class="sxs-lookup"><span data-stu-id="f7f69-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="f7f69-113">Seleccione la acción **Referencias cruzadas**.</span><span class="sxs-lookup"><span data-stu-id="f7f69-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="f7f69-114">En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f7f69-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="f7f69-115">.</span><span class="sxs-lookup"><span data-stu-id="f7f69-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="f7f69-116">Para introducir la descripción del producto de un proveedor en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="f7f69-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="f7f69-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7f69-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f7f69-118">Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="f7f69-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="f7f69-119">Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="f7f69-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="f7f69-120">En el campo **Nº tipo referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="f7f69-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="f7f69-121">seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f7f69-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="f7f69-122">El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.</span><span class="sxs-lookup"><span data-stu-id="f7f69-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f69-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7f69-123">See Also</span></span>
[<span data-ttu-id="f7f69-124">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="f7f69-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="f7f69-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="f7f69-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f7f69-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7f69-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
