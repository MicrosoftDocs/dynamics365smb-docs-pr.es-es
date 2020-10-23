---
title: Uso de referencias cruzadas de productos | Documentos de Microsoft
description: Configure referencias entre las descripciones que usted y su proveedor usan para un producto para que pueda insertar la descripción del artículo del proveedor en los documentos de compra.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919443"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="56570-103">Usar referencias cruzadas de producto</span><span class="sxs-lookup"><span data-stu-id="56570-103">Use Item Cross References</span></span>
<span data-ttu-id="56570-104">Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**.</span><span class="sxs-lookup"><span data-stu-id="56570-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="56570-105">.</span><span class="sxs-lookup"><span data-stu-id="56570-105">field.</span></span> <span data-ttu-id="56570-106">Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.</span><span class="sxs-lookup"><span data-stu-id="56570-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="56570-107">Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra.</span><span class="sxs-lookup"><span data-stu-id="56570-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="56570-108">Los pasos son parecidos para la venta.</span><span class="sxs-lookup"><span data-stu-id="56570-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="56570-109">Es cada vez más común que los identificadores de productos, como GTIN o GUID, contengan 30 o más caracteres, que es más de lo que la función actual para referencias cruzadas de productos puede manejar.</span><span class="sxs-lookup"><span data-stu-id="56570-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="56570-110">Si necesita utilizar referencias que contengan más de 30 caracteres, su administrador puede activar la característica **Escribir referencias de productos más largas** en la página [Gestión de funciones](https://businesscentral.dynamics.com/?page=xzy) (el vínculo requiere que tenga un suscriptor [!INCLUDE[d365fin](includes/d365fin_md.md)]).</span><span class="sxs-lookup"><span data-stu-id="56570-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=xzy) page (link requires that you have a [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant).</span></span> <span data-ttu-id="56570-111">La forma en que usa las referencias no cambia, pero los nombres de cosas como páginas y botones sí.</span><span class="sxs-lookup"><span data-stu-id="56570-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="56570-112">Por ejemplo, la página **Entradas de referencias cruzadas de productos** se convertirá en la página **Entradas de referencia de artículo**.</span><span class="sxs-lookup"><span data-stu-id="56570-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="56570-113">Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor</span><span class="sxs-lookup"><span data-stu-id="56570-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="56570-114">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="56570-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="56570-115">Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.</span><span class="sxs-lookup"><span data-stu-id="56570-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="56570-116">Seleccione la acción **Referencias cruzadas**.</span><span class="sxs-lookup"><span data-stu-id="56570-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="56570-117">Si no puede encontrar la acción **Referencias cruzadas**, elija ver más opciones y luego búsquela en **Relacionado** > **Producto**.</span><span class="sxs-lookup"><span data-stu-id="56570-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="56570-118">En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="56570-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="56570-119">.</span><span class="sxs-lookup"><span data-stu-id="56570-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="56570-120">Para introducir la descripción del producto de un proveedor en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="56570-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="56570-121">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="56570-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="56570-122">Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="56570-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="56570-123">Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="56570-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="56570-124">En el campo **Nº tipo referencia cruzada**</span><span class="sxs-lookup"><span data-stu-id="56570-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="56570-125">seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="56570-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="56570-126">El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.</span><span class="sxs-lookup"><span data-stu-id="56570-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="56570-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="56570-127">See Also</span></span>
[<span data-ttu-id="56570-128">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="56570-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="56570-129">Inventario</span><span class="sxs-lookup"><span data-stu-id="56570-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="56570-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56570-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
