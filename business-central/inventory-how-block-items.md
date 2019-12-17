---
title: Cómo bloquear productos de venta o de compra
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896066"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="57ea7-103">Bloquear productos de venta o de compra</span><span class="sxs-lookup"><span data-stu-id="57ea7-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="57ea7-104">Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.</span><span class="sxs-lookup"><span data-stu-id="57ea7-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="57ea7-105">La siguiente tabla muestra qué sucede cuando se bloquean los productos.</span><span class="sxs-lookup"><span data-stu-id="57ea7-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="57ea7-106">Opción</span><span class="sxs-lookup"><span data-stu-id="57ea7-106">Option</span></span>|<span data-ttu-id="57ea7-107">Description</span><span class="sxs-lookup"><span data-stu-id="57ea7-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="57ea7-108">**Venta bloqueada**</span><span class="sxs-lookup"><span data-stu-id="57ea7-108">**Sales Blocked**</span></span>|<span data-ttu-id="57ea7-109">No puede introducir el producto en un documento de venta ni en un diario de productos de venta.</span><span class="sxs-lookup"><span data-stu-id="57ea7-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="57ea7-110">**Compra bloqueada**</span><span class="sxs-lookup"><span data-stu-id="57ea7-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="57ea7-111">No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.</span><span class="sxs-lookup"><span data-stu-id="57ea7-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="57ea7-112">**Bloqueado**</span><span class="sxs-lookup"><span data-stu-id="57ea7-112">**Blocked**</span></span>|<span data-ttu-id="57ea7-113">No puede usar el producto en ninguna transacción de producto.</span><span class="sxs-lookup"><span data-stu-id="57ea7-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="57ea7-114">Los productos bloqueados se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="57ea7-114">Blocked items can be returned.</span></span> <span data-ttu-id="57ea7-115">Esto significa que ninguna de las opciones de configuración anteriores se aplica cuando se utiliza el producto en devoluciones y abonos.</span><span class="sxs-lookup"><span data-stu-id="57ea7-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="57ea7-116">Cuando usa la función **Copiar documento** para crear nuevos documentos basados en documentos existentes, se le notifica si algún producto en las líneas del documento de origen está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-116">When you use the **Copy Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="57ea7-117">Las líneas de documento bloqueadas se excluyen del nuevo documento y una notificación muestra una descripción general de todas las líneas de documento que están bloqueadas en el documento de origen.</span><span class="sxs-lookup"><span data-stu-id="57ea7-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="57ea7-118">Para bloquear que un producto se introduzca en líneas de venta</span><span class="sxs-lookup"><span data-stu-id="57ea7-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="57ea7-119">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57ea7-120">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="57ea7-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="57ea7-121">Si intenta introducir el producto en un documento de venta o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="57ea7-122">Para bloquear que un producto se introduzca en líneas de compra</span><span class="sxs-lookup"><span data-stu-id="57ea7-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="57ea7-123">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57ea7-124">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="57ea7-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="57ea7-125">Si intenta introducir el producto en un documento de compra o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="57ea7-126">Para bloquear que se registre un producto</span><span class="sxs-lookup"><span data-stu-id="57ea7-126">To block an item from being posted</span></span>
1. <span data-ttu-id="57ea7-127">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="57ea7-128">Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="57ea7-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="57ea7-129">Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="57ea7-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="57ea7-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="57ea7-130">See Also</span></span>  
[<span data-ttu-id="57ea7-131">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="57ea7-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="57ea7-132">Inventario</span><span class="sxs-lookup"><span data-stu-id="57ea7-132">Inventory</span></span>](inventory-manage-inventory.md)  
