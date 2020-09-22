---
title: Cómo registrar varios documentos al mismo tiempo | Documentos de Microsoft
description: En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro por lotes, ya sea para registro inmediato o programada para, por ejemplo, al final del día.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782523"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="da0d4-103">Registrar varios documentos al mismo tiempo</span><span class="sxs-lookup"><span data-stu-id="da0d4-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="da0d4-104">En lugar de registrar documentos individuales uno por uno, puede seleccionar varios documentos no registrados en una lista para el registro inmediato o para el registro por lotes según una programación, por ejemplo, al final del día.</span><span class="sxs-lookup"><span data-stu-id="da0d4-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="da0d4-105">Esto puede ser útil solo si un supervisor puede registrar documentos creados por otros usuarios o para evitar problemas de rendimiento del sistema del registro durante las horas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="da0d4-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="da0d4-106">Para registrar varios pedidos de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="da0d4-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="da0d4-107">El siguiente procedimiento explica cómo registrar varios pedidos de compra inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="da0d4-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="da0d4-108">Los pasos son parecidos a todos los documentos de compra y venta.</span><span class="sxs-lookup"><span data-stu-id="da0d4-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="da0d4-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="da0d4-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="da0d4-110">En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:</span><span class="sxs-lookup"><span data-stu-id="da0d4-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="da0d4-111">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="da0d4-111">In the **No.**</span></span> <span data-ttu-id="da0d4-112">elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="da0d4-113">Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="da0d4-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="da0d4-114">Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="da0d4-115">Elija el botón **Sí** en el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="da0d4-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="da0d4-116">Para registrar por lotes varios pedidos de compra</span><span class="sxs-lookup"><span data-stu-id="da0d4-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="da0d4-117">El siguiente procedimiento explica cómo registrar por lotes los pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="da0d4-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="da0d4-118">Los pasos son similares para todos los documentos de compra y venta donde la acción **Registro por lotes** está disponible.</span><span class="sxs-lookup"><span data-stu-id="da0d4-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="da0d4-119">La contabilización por lotes de documentos se realiza en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="da0d4-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="da0d4-120">[!INCLUDE [prodshort](includes/prodshort.md)] online incluye trabajos predeterminados para publicación en segundo plano y publicación por lotes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="da0d4-121">Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="da0d4-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="da0d4-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="da0d4-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da0d4-123">En la página **Pedidos de compra**, seleccione todos los pedidos que se registrarán:</span><span class="sxs-lookup"><span data-stu-id="da0d4-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="da0d4-124">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="da0d4-124">In the **No.**</span></span> <span data-ttu-id="da0d4-125">elija los tres puntos verticales para abrir el menú contextual y luego elija la acción **Seleccionar más**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="da0d4-126">Seleccione la casilla para todas las líneas que representan los pedidos que desea registrar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="da0d4-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="da0d4-127">Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar por lotes**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="da0d4-128">En la página **Reg. lotes pedidos compra**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="da0d4-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="da0d4-129">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="da0d4-130">Para ver posibles problemas que han sucedido durante el registro por lotes de documentos, abra la página **Registro de mensajes de error**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="da0d4-131">Los pedidos de compra ahora se agregarán a una entrada de cola de trabajos dedicada, que define cuándo se registran los documentos.</span><span class="sxs-lookup"><span data-stu-id="da0d4-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="da0d4-132">Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="da0d4-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="da0d4-133">Si selecciona **PDF** en el campo **Tipo de salida de informe**, los pedidos de compra registrados correctamente estarán disponibles en la parte **Bandeja de entrada de informes** de su área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="da0d4-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="da0d4-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="da0d4-134">See Also</span></span>

[<span data-ttu-id="da0d4-135">Registrar documentos y diarios</span><span class="sxs-lookup"><span data-stu-id="da0d4-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="da0d4-136">Uso de colas de proyectos para programar tareas</span><span class="sxs-lookup"><span data-stu-id="da0d4-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="da0d4-137">Editar documentos registrados</span><span class="sxs-lookup"><span data-stu-id="da0d4-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="da0d4-138">Corregir o cancelar facturas de compra sin abonar</span><span class="sxs-lookup"><span data-stu-id="da0d4-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="da0d4-139">Búsqueda de páginas e información con Dígame</span><span class="sxs-lookup"><span data-stu-id="da0d4-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="da0d4-140">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da0d4-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
