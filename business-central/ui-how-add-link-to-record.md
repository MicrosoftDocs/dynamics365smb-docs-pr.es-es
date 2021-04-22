---
title: Agregar archivos adjuntos, vínculos y notas en los registros | Documentos de Microsoft
description: Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3acc0113cb14170b84363ab40a803da8b7551c75
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771140"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="b66df-103">Administrar archivos adjuntos, vínculos y notas en fichas y documentos</span><span class="sxs-lookup"><span data-stu-id="b66df-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="b66df-104">En el cuadro informativo en la mayoría de las fichas y documentos, puede adjuntar archivos, agregar vínculos y escribir notas.</span><span class="sxs-lookup"><span data-stu-id="b66df-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="b66df-105">Para vínculos y notas, también puede hacer esto en la página de lista seleccionando primero la línea relacionada.</span><span class="sxs-lookup"><span data-stu-id="b66df-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="b66df-106">Para ver o cambiar cualquiera de estos tipos de información adjunta, primero debe abrir la pestaña **Archivos adjuntos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b66df-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="b66df-107">El número situado detrás del título de la pestaña indica cuántos archivos adjuntos, vínculos o notas existen para la ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="b66df-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="b66df-108">Los archivos adjuntos, vínculos y notas permanecen adjuntos a medida que la ficha o el documento se procesan en otros estados, por ejemplo, desde un pedido de ventas en curso hasta una factura de ventas registrada.</span><span class="sxs-lookup"><span data-stu-id="b66df-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="b66df-109">Sin embargo, ninguno de los tipos de archivos adjuntos se envían del sistema, por ejemplo, al imprimir o al guardar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="b66df-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="b66df-110">Cuando envía y factura parcialmente un pedido de venta o de compra, el archivo adjunto solo se adjuntará a la factura final del pedido.</span><span class="sxs-lookup"><span data-stu-id="b66df-110">When you partially ship and invoice a sales or purchase order, the attachment will only be attached to the final invoice of the order.</span></span> <span data-ttu-id="b66df-111">Del mismo modo, cuando factura con la característica Fraccionamientos, el archivo adjunto se adjunta a los movimientos contables del documento, pero no para los movimientos de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b66df-111">Similarly, when you invoice using the Deferrals feature, the attachment is attached to the G/L entries for the document but not for the deferral entries.</span></span>
>
> <span data-ttu-id="b66df-112">Si elimina un pedido antes de que se facture, el archivo adjunto también se elimina.</span><span class="sxs-lookup"><span data-stu-id="b66df-112">If you delete an order before it is invoiced, the attachment is also removed.</span></span> <span data-ttu-id="b66df-113">Cuando factura pedidos de compra mediante la acción Traer albaranes de una factura de compra, el archivo adjunto de los pedidos de compra no se agrega a la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="b66df-113">When you invoice purchase orders using the Get Receipt Lines action from a purchase invoice, the attachment on the purchase orders is not added to the purchase invoice.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="b66df-114">Para adjuntar un archivo a una factura de compra</span><span class="sxs-lookup"><span data-stu-id="b66df-114">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="b66df-115">Puede adjuntar cualquier tipo de archivo, que contenga texto, imagen o vídeo, a una ficha o documento.</span><span class="sxs-lookup"><span data-stu-id="b66df-115">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="b66df-116">Esto es útil, por ejemplo, cuando desea almacenar la factura de un proveedor como un archivo PDF en la factura de compra relacionada en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b66df-116">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="b66df-117">Los archivos adjuntos con la función Documentos entrantes no se incluyen en la pestaña **Anexos**. Para obtener más información, consulte [Documentos entrantes](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="b66df-117">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="b66df-118">El procedimiento siguiente se basa en una factura de compra.</span><span class="sxs-lookup"><span data-stu-id="b66df-118">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="b66df-119">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="b66df-119">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="b66df-120">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b66df-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="b66df-121">Abra el pedido de venta al que desea adjuntar un archivo.</span><span class="sxs-lookup"><span data-stu-id="b66df-121">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="b66df-122">En el cuadro informativo, abra la pestaña **Anexos**.</span><span class="sxs-lookup"><span data-stu-id="b66df-122">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="b66df-123">Elija el valor que va detrás del campo **Documentos**, como "0".</span><span class="sxs-lookup"><span data-stu-id="b66df-123">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="b66df-124">En la página **Documentos adjuntos**, en el campo **Archivo adjunto**, seleccione la acción **Seleccionar archivo**.</span><span class="sxs-lookup"><span data-stu-id="b66df-124">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="b66df-125">Seleccione un archivo de cualquier ubicación y, a continuación, elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="b66df-125">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="b66df-126">El archivo se adjunta ahora a la factura de compra.</span><span class="sxs-lookup"><span data-stu-id="b66df-126">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="b66df-127">Para ver un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="b66df-127">To view an attached file</span></span>
1. <span data-ttu-id="b66df-128">En el cuadro informativo, abra la pestaña **Anexos**.</span><span class="sxs-lookup"><span data-stu-id="b66df-128">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="b66df-129">Elija el valor que va detrás del campo **Documentos**, como "1".</span><span class="sxs-lookup"><span data-stu-id="b66df-129">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="b66df-130">En la página **Documentos adjuntos**, seleccione la acción **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="b66df-130">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="b66df-131">Abra el archivo descargado.</span><span class="sxs-lookup"><span data-stu-id="b66df-131">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="b66df-132">Para guardar un documento como un archivo PDF adjunto</span><span class="sxs-lookup"><span data-stu-id="b66df-132">To save a document as a PDF attachment</span></span>
<span data-ttu-id="b66df-133">Siempre que necesite guardar un documento como un archivo, puede usar la acción **Adjuntar como PDF** para capturar el contenido actual del documento como un archivo PDF adjunto al cuadro informativo del documento.</span><span class="sxs-lookup"><span data-stu-id="b66df-133">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="b66df-134">Esto es útil, por ejemplo, cuando los documentos siguen varios pasos de un proceso, como un proceso de ventas o un flujo de trabajo de aprobación, y desea consultar una copia impresa del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="b66df-134">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="b66df-135">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b66df-135">The following procedure is based on a sales order.</span></span> <span data-ttu-id="b66df-136">Los pasos son similares para todos los documentos admitidos.</span><span class="sxs-lookup"><span data-stu-id="b66df-136">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="b66df-137">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b66df-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b66df-138">Seleccione un pedido de ventas y después seleccione la acción **Adjuntar como PDF** .</span><span class="sxs-lookup"><span data-stu-id="b66df-138">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="b66df-139">Se agrega un archivo PDF con el contenido actual del pedido de cliente a la pestaña **Archivos adjuntos** del cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b66df-139">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="b66df-140">Para añadir un enlace de una ficha de producto</span><span class="sxs-lookup"><span data-stu-id="b66df-140">To add a link from an item card</span></span>
<span data-ttu-id="b66df-141">Puede añadir un enlace de una ficha o un documento a cualquier URL o ruta.</span><span class="sxs-lookup"><span data-stu-id="b66df-141">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="b66df-142">Esto es útil, por ejemplo, cuando desea vincular una ficha de producto con el catálogo de producto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b66df-142">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="b66df-143">El procedimiento siguiente se basa en una ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="b66df-143">The following procedure is based on an item card.</span></span> <span data-ttu-id="b66df-144">Los pasos son parecidos a los de las demás fichas y documentos admitidos.</span><span class="sxs-lookup"><span data-stu-id="b66df-144">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="b66df-145">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b66df-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b66df-146">Seleccione el producto del que desea agregar un vínculo y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b66df-146">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="b66df-147">En **Vínculos**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="b66df-147">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="b66df-148">En el campo **Vincular dirección**, especifique el vínculo.</span><span class="sxs-lookup"><span data-stu-id="b66df-148">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="b66df-149">El enlace debe ser una URL válida de Internet o intranet.</span><span class="sxs-lookup"><span data-stu-id="b66df-149">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="b66df-150">En el campo **Descripción**, escriba cualquier información sobre el vínculo.</span><span class="sxs-lookup"><span data-stu-id="b66df-150">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="b66df-151">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b66df-151">Choose the **OK** button.</span></span>

<span data-ttu-id="b66df-152">El vínculo ahora está adjunto a la ficha de producto.</span><span class="sxs-lookup"><span data-stu-id="b66df-152">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="b66df-153">Para escribir una nota en un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="b66df-153">To write a note on a sales order</span></span>
<span data-ttu-id="b66df-154">Puede escribir una nota en un documento o ficha, por ejemplo, para comunicar instrucciones especiales a otros usuarios del documento o ficha.</span><span class="sxs-lookup"><span data-stu-id="b66df-154">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="b66df-155">Puede incluir vínculos de archivo y URL en las notas.</span><span class="sxs-lookup"><span data-stu-id="b66df-155">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="b66df-156">Las notas en la pestaña **Anexos** no están relacionadas con la funcionalidad de notas internas, que se utiliza principalmente para comunicarse entre los usuarios del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b66df-156">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="b66df-157">Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b66df-157">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="b66df-158">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b66df-158">The following procedure is based on a sales order.</span></span> <span data-ttu-id="b66df-159">Los pasos son parecidos a los de los demás documentos y las fichas admitidos.</span><span class="sxs-lookup"><span data-stu-id="b66df-159">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="b66df-160">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b66df-160">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b66df-161">Seleccione el pedido de venta del en el que desea escribir una nota y luego elija la pestaña **Anexos** en el cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="b66df-161">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="b66df-162">En la sección **Notas**, elija el icono **+**.</span><span class="sxs-lookup"><span data-stu-id="b66df-162">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="b66df-163">En el campo **Nota**, escriba cualquier texto, por ejemplo, "Este pedido es urgente.".</span><span class="sxs-lookup"><span data-stu-id="b66df-163">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="b66df-164">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b66df-164">Choose the **OK** button.</span></span>

<span data-ttu-id="b66df-165">La nota ahora está adjuntada al pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="b66df-165">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="b66df-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b66df-166">See Also</span></span>  
<span data-ttu-id="b66df-167">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b66df-167">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b66df-168">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="b66df-168">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="b66df-169">Configurar notificaciones de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="b66df-169">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]