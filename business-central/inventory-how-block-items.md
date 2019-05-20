---
title: Cómo bloquear productos de venta o de compra
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
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
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238537"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="ab767-103">Bloquear productos de venta o de compra</span><span class="sxs-lookup"><span data-stu-id="ab767-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="ab767-104">Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.</span><span class="sxs-lookup"><span data-stu-id="ab767-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="ab767-105">La siguiente tabla muestra qué sucede cuando se bloquean los productos.</span><span class="sxs-lookup"><span data-stu-id="ab767-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="ab767-106">Opción</span><span class="sxs-lookup"><span data-stu-id="ab767-106">Option</span></span>|<span data-ttu-id="ab767-107">Description</span><span class="sxs-lookup"><span data-stu-id="ab767-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="ab767-108">**Venta bloqueada**</span><span class="sxs-lookup"><span data-stu-id="ab767-108">**Sales Blocked**</span></span>|<span data-ttu-id="ab767-109">No puede introducir el producto en un documento de venta ni en un diario de productos de venta.</span><span class="sxs-lookup"><span data-stu-id="ab767-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="ab767-110">**Compra bloqueada**</span><span class="sxs-lookup"><span data-stu-id="ab767-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="ab767-111">No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.</span><span class="sxs-lookup"><span data-stu-id="ab767-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="ab767-112">**Bloqueado**</span><span class="sxs-lookup"><span data-stu-id="ab767-112">**Blocked**</span></span>|<span data-ttu-id="ab767-113">No puede usar el producto en ninguna transacción de producto.</span><span class="sxs-lookup"><span data-stu-id="ab767-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="ab767-114">Para obtener más información sobre el bloqueo de un producto para todos los propósitos, consulte la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="ab767-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="ab767-115">Para bloquear que un producto se introduzca en líneas de venta</span><span class="sxs-lookup"><span data-stu-id="ab767-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="ab767-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ab767-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab767-117">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="ab767-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="ab767-118">Si intenta introducir el producto en un documento de venta o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ab767-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="ab767-119">Para bloquear que un producto se introduzca en líneas de compra</span><span class="sxs-lookup"><span data-stu-id="ab767-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="ab767-120">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ab767-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab767-121">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="ab767-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="ab767-122">Si intenta introducir el producto en un documento de compra o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ab767-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="ab767-123">Para bloquear que se registre un producto</span><span class="sxs-lookup"><span data-stu-id="ab767-123">To block an item from being posted</span></span>
1. <span data-ttu-id="ab767-124">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="ab767-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="ab767-125">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="ab767-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="ab767-126">Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ab767-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab767-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab767-127">See Also</span></span>  
[<span data-ttu-id="ab767-128">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="ab767-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="ab767-129">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="ab767-129">Inventory</span></span>](inventory-manage-inventory.md)  
