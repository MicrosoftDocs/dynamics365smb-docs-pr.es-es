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
ms.date: 04/27/2020
ms.author: edupont
ms.openlocfilehash: 39aae609e588635a07fdc406faa63dd4ced3606d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789380"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="d8100-103">Administrar archivos adjuntos, vínculos y notas en fichas y documentos</span><span class="sxs-lookup"><span data-stu-id="d8100-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="d8100-104">En el cuadro informativo en la mayoría de las fichas y documentos, puede adjuntar archivos, agregar vínculos y escribir notas.</span><span class="sxs-lookup"><span data-stu-id="d8100-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="d8100-105">Para vínculos y notas, también puede hacer esto en la página de lista seleccionando primero la línea relacionada.</span><span class="sxs-lookup"><span data-stu-id="d8100-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="d8100-106">Para ver o cambiar cualquiera de estos tipos de información adjunta, primero debe abrir la pestaña **Archivos adjuntos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="d8100-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="d8100-107">El número situado detrás del título de la pestaña indica cuántos archivos adjuntos, vínculos o notas existen para la ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="d8100-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="d8100-108">Los archivos adjuntos, vínculos y notas permanecen adjuntos a medida que la ficha o el documento se procesan en otros estados, por ejemplo, desde un pedido de ventas en curso hasta una factura de ventas registrada.</span><span class="sxs-lookup"><span data-stu-id="d8100-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="d8100-109">Sin embargo, ninguno de los tipos de archivos adjuntos se envían del sistema, por ejemplo, al imprimir o al guardar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="d8100-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="d8100-110">Cuando envía y factura parcialmente un pedido de venta o un pedido de compra, el archivo adjunto solo se adjuntará a la factura final de ese pedido.</span><span class="sxs-lookup"><span data-stu-id="d8100-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="d8100-111">Del mismo modo, cuando factura con la función Fraccionamientos, el archivo adjunto solo se adjunta a los movimientos contables del documento, pero no para los movimientos de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d8100-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="d8100-112">Para adjuntar un archivo a una factura de compra</span><span class="sxs-lookup"><span data-stu-id="d8100-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="d8100-113">Puede adjuntar cualquier tipo de archivo, que contenga texto, imagen o vídeo, a una ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="d8100-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="d8100-114">Esto es útil, por ejemplo, cuando desea almacenar la factura de un proveedor como un archivo PDF en la factura de compra relacionada en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d8100-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="d8100-115">Los archivos adjuntos con la función Documentos entrantes no se incluyen en la pestaña **Anexos**. Para obtener más información, consulte [Documentos entrantes](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="d8100-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="d8100-116">El procedimiento siguiente se basa en una factura de compra.</span><span class="sxs-lookup"><span data-stu-id="d8100-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="d8100-117">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="d8100-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="d8100-118">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d8100-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8100-119">Abra el pedido de venta al que desea adjuntar un archivo.</span><span class="sxs-lookup"><span data-stu-id="d8100-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="d8100-120">En el cuadro informativo, abra la pestaña **Anexos**.</span><span class="sxs-lookup"><span data-stu-id="d8100-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="d8100-121">Elija el valor que va detrás del campo **Documentos**, como "0".</span><span class="sxs-lookup"><span data-stu-id="d8100-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="d8100-122">En la página **Documentos adjuntos**, en el campo **Archivo adjunto**, seleccione la acción **Seleccionar archivo**.</span><span class="sxs-lookup"><span data-stu-id="d8100-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="d8100-123">Seleccione un archivo de cualquier ubicación y, a continuación, elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="d8100-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="d8100-124">El archivo se adjunta ahora a la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="d8100-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="d8100-125">Para ver un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="d8100-125">To view an attached file</span></span>
1. <span data-ttu-id="d8100-126">En el cuadro informativo, abra la pestaña **Anexos**.</span><span class="sxs-lookup"><span data-stu-id="d8100-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="d8100-127">Elija el valor que va detrás del campo **Documentos**, como "1".</span><span class="sxs-lookup"><span data-stu-id="d8100-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="d8100-128">En la página **Documentos adjuntos**, seleccione la acción **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="d8100-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="d8100-129">Abra el archivo descargado.</span><span class="sxs-lookup"><span data-stu-id="d8100-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="d8100-130">Para guardar un documento como un archivo PDF adjunto</span><span class="sxs-lookup"><span data-stu-id="d8100-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="d8100-131">Siempre que necesite guardar un documento como un archivo, puede usar la acción **Adjuntar como PDF** para capturar el contenido actual del documento como un archivo PDF adjunto al cuadro informativo del documento.</span><span class="sxs-lookup"><span data-stu-id="d8100-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="d8100-132">Esto es útil, por ejemplo, cuando los documentos siguen varios pasos de un proceso, como un proceso de ventas o un flujo de trabajo de aprobación, y desea consultar una copia impresa del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="d8100-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="d8100-133">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d8100-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="d8100-134">Los pasos son similares para todos los documentos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d8100-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="d8100-135">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d8100-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8100-136">Seleccione un pedido de ventas y después seleccione la acción **Adjuntar como PDF** .</span><span class="sxs-lookup"><span data-stu-id="d8100-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="d8100-137">Se agrega un archivo PDF con el contenido actual del pedido de cliente a la pestaña **Archivos adjuntos** del cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="d8100-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="d8100-138">Para añadir un enlace de una ficha de producto</span><span class="sxs-lookup"><span data-stu-id="d8100-138">To add a link from an item card</span></span>
<span data-ttu-id="d8100-139">Puede añadir un enlace de una ficha o un documento a cualquier URL o ruta.</span><span class="sxs-lookup"><span data-stu-id="d8100-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="d8100-140">Esto es útil, por ejemplo, cuando desea vincular una ficha de producto con el catálogo de producto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d8100-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="d8100-141">El procedimiento siguiente se basa en una ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="d8100-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="d8100-142">Los pasos son parecidos a los de las demás fichas y documentos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d8100-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="d8100-143">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d8100-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8100-144">Seleccione el producto del que desea agregar un vínculo y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="d8100-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="d8100-145">En **Vínculos**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="d8100-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="d8100-146">En el campo **Vincular dirección**, especifique el vínculo.</span><span class="sxs-lookup"><span data-stu-id="d8100-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="d8100-147">El enlace debe ser una URL válida de Internet o intranet.</span><span class="sxs-lookup"><span data-stu-id="d8100-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="d8100-148">En el campo **Descripción**, escriba cualquier información sobre el vínculo.</span><span class="sxs-lookup"><span data-stu-id="d8100-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="d8100-149">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d8100-149">Choose the **OK** button.</span></span>

<span data-ttu-id="d8100-150">El vínculo ahora está adjunto a la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="d8100-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="d8100-151">Para escribir una nota en un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="d8100-151">To write a note on a sales order</span></span>
<span data-ttu-id="d8100-152">Puede escribir una nota en un documento o ficha, por ejemplo, para comunicar instrucciones especiales a otros usuarios del documento o ficha.</span><span class="sxs-lookup"><span data-stu-id="d8100-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="d8100-153">Puede incluir vínculos de archivo y URL en las notas.</span><span class="sxs-lookup"><span data-stu-id="d8100-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="d8100-154">Las notas en la pestaña **Anexos** no están relacionadas con la funcionalidad de notas internas, que se utiliza principalmente para comunicarse entre los usuarios del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d8100-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="d8100-155">Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d8100-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="d8100-156">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d8100-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="d8100-157">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="d8100-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="d8100-158">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d8100-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8100-159">Seleccione el pedido de venta del en el que desea escribir una nota y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="d8100-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="d8100-160">En la sección **Notas**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="d8100-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="d8100-161">En el campo **Nota**, escriba cualquier texto, por ejemplo, "Este pedido es urgente.".</span><span class="sxs-lookup"><span data-stu-id="d8100-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="d8100-162">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d8100-162">Choose the **OK** button.</span></span>

<span data-ttu-id="d8100-163">La nota ahora está adjuntada al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d8100-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8100-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8100-164">See Also</span></span>  
<span data-ttu-id="d8100-165">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8100-165">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d8100-166">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="d8100-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d8100-167">Configurar notificaciones de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="d8100-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
