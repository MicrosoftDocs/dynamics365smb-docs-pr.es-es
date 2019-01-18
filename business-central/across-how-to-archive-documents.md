---
title: "Cómo archivar ventas y documentos de compra | Documentos de Microsoft"
description: "Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos y puede usar el documento archivado para recrear el documento desde el que se archivó."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4827e25d97127faf691b96df9868320bb47dee39
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="archive-documents"></a><span data-ttu-id="01846-103">Archivar documentos</span><span class="sxs-lookup"><span data-stu-id="01846-103">Archive Documents</span></span>
<span data-ttu-id="01846-104">Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos y puede usar el documento archivado para recrear el documento desde el que se archivó.</span><span class="sxs-lookup"><span data-stu-id="01846-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="01846-105">Para configurar el archivado automático de documentos</span><span class="sxs-lookup"><span data-stu-id="01846-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="01846-106">Puede configurar el archivado automático de pedidos de venta y compra, presupuestos, pedidos abiertos y órdenes de devolución antes de eliminar documentos.</span><span class="sxs-lookup"><span data-stu-id="01846-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="01846-107">El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="01846-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="01846-108">Los pasos son parecidos para documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="01846-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="01846-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración ventas y cobros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01846-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="01846-110">En la página **Conf. ventas y cobros**, rellene los campos del modo que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="01846-110">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="01846-111">Campo</span><span class="sxs-lookup"><span data-stu-id="01846-111">Field</span></span>|<span data-ttu-id="01846-112">Description</span><span class="sxs-lookup"><span data-stu-id="01846-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="01846-113">**Archivar ofertas venta**</span><span class="sxs-lookup"><span data-stu-id="01846-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="01846-114">**Nunca** para no archivar las ofertas de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="01846-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="01846-115">**Pregunta** para solicitar al usuario que elija si desea archivar ofertas de ventas cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="01846-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="01846-116">**Siempre** para archivar automáticamente las ofertas de venta cuando se eliminan.</span><span class="sxs-lookup"><span data-stu-id="01846-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="01846-117">**Archivar pedidos de venta abiertos**</span><span class="sxs-lookup"><span data-stu-id="01846-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="01846-118">Seleccione archivar pedidos de venta genéricos automáticamente cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="01846-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="01846-119">**Ped. arch. y Ped. dev.**</span><span class="sxs-lookup"><span data-stu-id="01846-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="01846-120">Seleccione archivar automáticamente pedidos de venta cada vez que se eliminen.</span><span class="sxs-lookup"><span data-stu-id="01846-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="01846-121">Archivar pedidos de venta</span><span class="sxs-lookup"><span data-stu-id="01846-121">To archive a sales order</span></span>
<span data-ttu-id="01846-122">El siguiente procedimiento describe cómo archivar una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="01846-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="01846-123">Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.</span><span class="sxs-lookup"><span data-stu-id="01846-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="01846-124">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01846-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="01846-125">Abra un pedido de venta del que desee archivar.</span><span class="sxs-lookup"><span data-stu-id="01846-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="01846-126">Elija la acción **Archivar documento**.</span><span class="sxs-lookup"><span data-stu-id="01846-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="01846-127">El pedido de ventas está archivado.</span><span class="sxs-lookup"><span data-stu-id="01846-127">The sales order is archived.</span></span> <span data-ttu-id="01846-128">Puede verlo en la página **Pedidos de venta archivados**.</span><span class="sxs-lookup"><span data-stu-id="01846-128">You can view it on the **Archived Sales orders** page.</span></span> <span data-ttu-id="01846-129">Desde este momento, también puede usarlo para volver a crear el pedido de venta desde el que se archivó.</span><span class="sxs-lookup"><span data-stu-id="01846-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="01846-130">Para volver a crear un pedido de venta desde el archivo</span><span class="sxs-lookup"><span data-stu-id="01846-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="01846-131">El siguiente procedimiento describe cómo volver a crear una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="01846-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="01846-132">Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.</span><span class="sxs-lookup"><span data-stu-id="01846-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="01846-133">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta archivados** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01846-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="01846-134">Seleccione el pedido de venta archivado que desea volver a crear y después seleccione **Volver a crear**.</span><span class="sxs-lookup"><span data-stu-id="01846-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="01846-135">El pedido de venta se crea y se agrega a la página **Pedidos venta**.</span><span class="sxs-lookup"><span data-stu-id="01846-135">The sales order is created and added to the **Sales Orders** page.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="01846-136">Para eliminar pedidos de venta archivados</span><span class="sxs-lookup"><span data-stu-id="01846-136">To delete archived sales orders</span></span>
<span data-ttu-id="01846-137">El siguiente procedimiento describe cómo eliminar pedidos de venta archivados.</span><span class="sxs-lookup"><span data-stu-id="01846-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="01846-138">Los pasos son similares para otros documentos de compra y venta archivados.</span><span class="sxs-lookup"><span data-stu-id="01846-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="01846-139">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar versiones pedido venta archiv.** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01846-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="01846-140">En la página **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="01846-140">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="01846-141">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="01846-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="01846-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="01846-142">See Also</span></span>
[<span data-ttu-id="01846-143">Seguimiento de líneas de documentos</span><span class="sxs-lookup"><span data-stu-id="01846-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="01846-144">Ventas</span><span class="sxs-lookup"><span data-stu-id="01846-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="01846-145">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="01846-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="01846-146">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="01846-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

