---
title: Cómo bloquear productos de venta o de compra
description: Puede evitar que se use un artículo, por ejemplo, en documentos de compra o venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 467b43b14f1905018c2a26a06c15abc5a0a17e99
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410649"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="94d47-103">Bloquear productos de venta o de compra</span><span class="sxs-lookup"><span data-stu-id="94d47-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="94d47-104">Puede bloquear que un producto entre en líneas de documentos de compra y venta, y puede bloquearlo para que no se registre en ninguna transacción.</span><span class="sxs-lookup"><span data-stu-id="94d47-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="94d47-105">Por ejemplo, esto es útil cuando un artículo tiene un defecto conocido.</span><span class="sxs-lookup"><span data-stu-id="94d47-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="94d47-106">Si alguien elige un artículo bloqueado en un documento de compra o venta, un mensaje le informará de que el artículo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="94d47-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="94d47-107">En la tabla siguiente se describe qué sucede cuando se bloquean los artículos.</span><span class="sxs-lookup"><span data-stu-id="94d47-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="94d47-108">Opción</span><span class="sxs-lookup"><span data-stu-id="94d47-108">Option</span></span>|<span data-ttu-id="94d47-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="94d47-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="94d47-110">**Venta bloqueada**</span><span class="sxs-lookup"><span data-stu-id="94d47-110">**Sales Blocked**</span></span>|<span data-ttu-id="94d47-111">No puede introducir el producto en un documento de venta ni en un diario de productos de venta.</span><span class="sxs-lookup"><span data-stu-id="94d47-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="94d47-112">**Compra bloqueada**</span><span class="sxs-lookup"><span data-stu-id="94d47-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="94d47-113">No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.</span><span class="sxs-lookup"><span data-stu-id="94d47-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="94d47-114">**Bloqueado**</span><span class="sxs-lookup"><span data-stu-id="94d47-114">**Blocked**</span></span>|<span data-ttu-id="94d47-115">No puede usar el producto en ninguna transacción de producto.</span><span class="sxs-lookup"><span data-stu-id="94d47-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="94d47-116">Los productos bloqueados se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="94d47-116">Blocked items can be returned.</span></span> <span data-ttu-id="94d47-117">Esto significa que ninguna de las opciones de configuración anteriores se aplica cuando se utiliza el producto en devoluciones y abonos.</span><span class="sxs-lookup"><span data-stu-id="94d47-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="94d47-118">Cuando usa la función **Copiar de documento** para crear nuevos documentos basados en documentos existentes, se le notifica si algún producto en las líneas del documento de origen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="94d47-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="94d47-119">Las líneas de documento bloqueadas se excluyen del nuevo documento y una notificación muestra una descripción general de todas las líneas de documento que están bloqueadas en el documento de origen.</span><span class="sxs-lookup"><span data-stu-id="94d47-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="94d47-120">Para bloquear que un producto se introduzca en líneas de venta</span><span class="sxs-lookup"><span data-stu-id="94d47-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="94d47-121">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="94d47-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94d47-122">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="94d47-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="94d47-123">Para bloquear que un producto se introduzca en líneas de compra</span><span class="sxs-lookup"><span data-stu-id="94d47-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="94d47-124">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="94d47-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94d47-125">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="94d47-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="94d47-126">Para bloquear que se registre un producto</span><span class="sxs-lookup"><span data-stu-id="94d47-126">To block an item from being posted</span></span>
1. <span data-ttu-id="94d47-127">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="94d47-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="94d47-128">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="94d47-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="94d47-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94d47-129">See Also</span></span>  
[<span data-ttu-id="94d47-130">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="94d47-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="94d47-131">Inventario</span><span class="sxs-lookup"><span data-stu-id="94d47-131">Inventory</span></span>](inventory-manage-inventory.md)  
