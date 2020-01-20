---
title: Agregar archivos adjuntos, vínculos y notas en los registros | Documentos de Microsoft
description: Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 84d9c0768a457fd13a73b3d70d2b8c329098fe82
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953282"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="8a8f6-103">Administrar archivos adjuntos, vínculos y notas en fichas y documentos</span><span class="sxs-lookup"><span data-stu-id="8a8f6-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="8a8f6-104">En el cuadro informativo en la mayoría de las fichas y documentos, puede adjuntar archivos, agregar vínculos y escribir notas.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="8a8f6-105">Para vínculos y notas, también puede hacer esto en la página de lista seleccionando primero la línea relacionada.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="8a8f6-106">Para ver o cambiar cualquiera de estos tipos de información adjunta, primero debe abrir la pestaña **Archivos adjuntos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="8a8f6-107">El número situado detrás del título de la pestaña indica cuántos archivos adjuntos, vínculos o notas existen para la ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="8a8f6-108">Los archivos adjuntos, vínculos y notas permanecen adjuntos a medida que la ficha o el documento se procesan en otros estados, por ejemplo, desde un pedido de ventas en curso hasta una factura de ventas registrada.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="8a8f6-109">Sin embargo, ninguno de los tipos de archivos adjuntos se envían del sistema, por ejemplo, al imprimir o al guardar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="8a8f6-110">Cuando envía y factura parcialmente un pedido de venta o un pedido de compra, el archivo adjunto solo se adjuntará a la factura final de ese pedido.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="8a8f6-111">Del mismo modo, cuando factura con la función Fraccionamientos, el archivo adjunto solo se adjunta a los movimientos contables del documento, pero no para los movimientos de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="8a8f6-112">Para adjuntar un archivo a una factura de compra</span><span class="sxs-lookup"><span data-stu-id="8a8f6-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="8a8f6-113">Puede adjuntar cualquier tipo de archivo, que contenga texto, imagen o vídeo, a una ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="8a8f6-114">Esto es útil, por ejemplo, cuando desea almacenar la factura de un proveedor como un archivo PDF en la factura de compra relacionada en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8a8f6-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="8a8f6-115">Los archivos adjuntos con la función Documentos entrantes no se incluyen en la pestaña **Anexos**. Para obtener más información, consulte [Documentos entrantes](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="8a8f6-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="8a8f6-116">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-116">The following procedure is based on a sales order.</span></span> <span data-ttu-id="8a8f6-117">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="8a8f6-118">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a8f6-119">Abra el pedido de venta al que desea adjuntar un archivo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="8a8f6-120">En el cuadro informativo, abra la pestaña **Anexos**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="8a8f6-121">Elija el valor que va detrás del campo **Documentos**, como "0".</span><span class="sxs-lookup"><span data-stu-id="8a8f6-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="8a8f6-122">En la página **Documentos adjuntos**, en el campo **Archivo adjunto**, seleccione el botón **Seleccionar archivo**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="8a8f6-123">Seleccione un archivo de cualquier ubicación y, a continuación, elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="8a8f6-124">El archivo se adjunta ahora a la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="8a8f6-125">Para añadir un enlace de una ficha de producto</span><span class="sxs-lookup"><span data-stu-id="8a8f6-125">To add a link from an item card</span></span>
<span data-ttu-id="8a8f6-126">Puede añadir un enlace de una ficha o un documento a cualquier URL o ruta.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-126">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="8a8f6-127">Esto es útil, por ejemplo, cuando desea vincular una ficha de producto con el catálogo de producto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-127">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="8a8f6-128">El procedimiento siguiente se basa en una ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-128">The following procedure is based on an item card.</span></span> <span data-ttu-id="8a8f6-129">Los pasos son parecidos a los de las demás fichas y documentos admitidos.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-129">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="8a8f6-130">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a8f6-131">Seleccione el producto del que desea agregar un vínculo y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-131">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="8a8f6-132">En **Vínculos**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-132">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="8a8f6-133">En el campo **Vincular dirección**, especifique el vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-133">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="8a8f6-134">El enlace debe ser una URL válida de Internet o intranet.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-134">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="8a8f6-135">En el campo **Descripción**, escriba cualquier información sobre el vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-135">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="8a8f6-136">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-136">Choose the **OK** button.</span></span>

<span data-ttu-id="8a8f6-137">El vínculo ahora está adjunto a la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-137">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="8a8f6-138">Para escribir una nota en un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="8a8f6-138">To write a note on a sales order</span></span>
<span data-ttu-id="8a8f6-139">Puede escribir una nota en un documento o ficha, por ejemplo, para comunicar instrucciones especiales a otros usuarios del documento o ficha.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-139">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="8a8f6-140">Puede incluir vínculos de archivo y URL en las notas.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-140">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="8a8f6-141">Las notas en la pestaña **Anexos** no están relacionadas con la funcionalidad de notas internas, que se utiliza principalmente para comunicarse entre los usuarios del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-141">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="8a8f6-142">Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="8a8f6-142">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="8a8f6-143">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-143">The following procedure is based on a sales order.</span></span> <span data-ttu-id="8a8f6-144">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-144">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="8a8f6-145">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="8a8f6-146">Seleccione el pedido de venta del en el que desea escribir una nota y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-146">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="8a8f6-147">En la sección **Notas**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-147">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="8a8f6-148">En el campo **Nota**, escriba cualquier texto, por ejemplo, "Este pedido es urgente.".</span><span class="sxs-lookup"><span data-stu-id="8a8f6-148">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="8a8f6-149">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-149">Choose the **OK** button.</span></span>

<span data-ttu-id="8a8f6-150">La nota ahora está adjuntada al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="8a8f6-150">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a8f6-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a8f6-151">See Also</span></span>  
<span data-ttu-id="8a8f6-152">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8a8f6-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8a8f6-153">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="8a8f6-153">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="8a8f6-154">Configurar notificaciones de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="8a8f6-154">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
