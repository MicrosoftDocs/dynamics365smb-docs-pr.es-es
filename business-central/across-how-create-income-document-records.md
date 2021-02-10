---
title: Crear registros de documento entrantes | Documentos de Microsoft
description: Puede crear registros de los documentos entrantes, como facturas electrónicas, y administrar las tareas de OCR, comercio electrónico e intercambio de documentos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 722e69389413dc06db4f2b7fd2f8447d9033d030
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753297"
---
# <a name="create-incoming-document-records"></a><span data-ttu-id="62ab7-103">Crear registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="62ab7-103">Create Incoming Document Records</span></span>
<span data-ttu-id="62ab7-104">En la página **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="62ab7-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="62ab7-105">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="62ab7-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="62ab7-106">Para registrar un documento externo en [!INCLUDE[prod_short](includes/prod_short.md)], debe crear o completar un registro de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="62ab7-106">To record an external document in [!INCLUDE[prod_short](includes/prod_short.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="62ab7-107">Puede hacerlo manualmente o tomar una foto del documento externo y crear el registro de documento entrante con el archivo de imagen adjunto.</span><span class="sxs-lookup"><span data-stu-id="62ab7-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="62ab7-108">Para poder usar la función Documentos entrantes, debe realizar la configuración necesaria.</span><span class="sxs-lookup"><span data-stu-id="62ab7-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="62ab7-109">Para obtener más información, vea [Configurar documentos entrantes](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="62ab7-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="62ab7-110">Para aprobar o rechazar un documento entrante</span><span class="sxs-lookup"><span data-stu-id="62ab7-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="62ab7-111">Si desea que los usuarios creen facturas o líneas de diario general a partir de los registros de documento entrante a menos que se aprueben, puede configurar aprobadores que deben aprobar los registros antes de que se puedan procesar.</span><span class="sxs-lookup"><span data-stu-id="62ab7-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="62ab7-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos entrantes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="62ab7-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="62ab7-113">Seleccione la línea con el documento que desea aprobar o rechazar y, a continuación, elija las acciones **Aprobar** o **Rechazar**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="62ab7-114">Si aprueba el registro de documento entrante, se marca la casilla **Lanzado** de la línea de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="62ab7-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="62ab7-115">El usuario responsable de crear, por ejemplo, facturas de compra puede procesar el registro.</span><span class="sxs-lookup"><span data-stu-id="62ab7-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="62ab7-116">Para crear un registro de documento entrante tomando una foto</span><span class="sxs-lookup"><span data-stu-id="62ab7-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="62ab7-117">El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62ab7-117">The following procedure only applies to the [!INCLUDE[prod_short](includes/prod_short.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="62ab7-118">En la barra de aplicaciones, seleccione el mosaico **Crear documento entrante desde la cámara** y, a continuación, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="62ab7-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="62ab7-119">O bien, en la barra de aplicaciones, seleccione el botón de opciones, elija **Documentos entrantes** y, a continuación, elija **Todo**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="62ab7-120">En la página **Documentos entrantes**, elija el botón de puntos suspensivos y seleccione **Crear desde la cámara**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="62ab7-121">La cámara de la tableta o del teléfono se activará.</span><span class="sxs-lookup"><span data-stu-id="62ab7-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="62ab7-122">Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="62ab7-123">Se crea un nuevo registro de documento entrante con la imagen adjunta.</span><span class="sxs-lookup"><span data-stu-id="62ab7-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="62ab7-124">Para adjuntar una imagen en un registro de documento entrante</span><span class="sxs-lookup"><span data-stu-id="62ab7-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="62ab7-125">El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62ab7-125">The following procedure only applies to the [!INCLUDE[prod_short](includes/prod_short.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="62ab7-126">En la barra de aplicaciones, elija el botón opciones, seleccione **Documentos entrantes** y, a continuación, elija **Todo**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="62ab7-127">Abra la ficha de un registro entrante de documento entrante existente.</span><span class="sxs-lookup"><span data-stu-id="62ab7-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="62ab7-128">En la página **Documento entrante**, elija el botón de puntos suspensivos y seleccione **Adjuntar imagen desde la cámara**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="62ab7-129">La cámara de la tableta o del teléfono se activará.</span><span class="sxs-lookup"><span data-stu-id="62ab7-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="62ab7-130">Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="62ab7-131">La imagen se adjunta al registro de documento entrante.</span><span class="sxs-lookup"><span data-stu-id="62ab7-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="62ab7-132">Para crear un registro de documento entrante manualmente</span><span class="sxs-lookup"><span data-stu-id="62ab7-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="62ab7-133">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos entrantes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="62ab7-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="62ab7-134">Elija la acción **Crear desde archivo**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="62ab7-135">En la página **Insertar archivo**, seleccione un archivo y, a continuación, elija **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="62ab7-136">El campo se adjunta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="62ab7-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="62ab7-137">De forma alternativa, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="62ab7-138">Para adjuntar un archivo, elija la acción **Adjuntar archivo**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="62ab7-139">En la página **Insertar archivo**, seleccione el archivo que representa el documento entrante en cuestión y, a continuación, elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="62ab7-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="62ab7-140">En la página **Documento entrante**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="62ab7-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="62ab7-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62ab7-141">See Also</span></span>
[<span data-ttu-id="62ab7-142">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="62ab7-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="62ab7-143">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="62ab7-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="62ab7-144">Compras</span><span class="sxs-lookup"><span data-stu-id="62ab7-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="62ab7-145">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="62ab7-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
