---
title: Configurar documentos entrantes | Documentos de Microsoft
description: Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/23/2020
ms.author: sgroespe
ms.openlocfilehash: 09047315c701bd2076f59b6c3f4840ba95eb06cc
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503549"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="afa86-103">Configurar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="afa86-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="afa86-104">Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.</span><span class="sxs-lookup"><span data-stu-id="afa86-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="afa86-105">Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documentos entrantes a menos que los documentos se aprueben primero, debe configurar aprobadores de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="afa86-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="afa86-106">Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="afa86-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="afa86-107">Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="afa86-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="afa86-108">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="afa86-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="afa86-109">Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="afa86-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="afa86-110">Para configurar la característica Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="afa86-110">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="afa86-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de ventas y cobros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="afa86-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="afa86-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="afa86-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="afa86-113">Como parte de la configuración, debe decidir si desea solicitar la aprobación de los documentos entrantes.</span><span class="sxs-lookup"><span data-stu-id="afa86-113">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="afa86-114">Para requerir aprobación, debe configurar aprobadores y flujos de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="afa86-114">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="afa86-115">Si su organización no tiene la intención de requerir aprobación, puede omitir la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="afa86-115">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="afa86-116">Finalmente, si utiliza un servicio para convertir archivos PDF o de imagen que representan documentos entrantes, debe configurarlo.</span><span class="sxs-lookup"><span data-stu-id="afa86-116">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="afa86-117">De lo contrario, también puede omitir esa sección.</span><span class="sxs-lookup"><span data-stu-id="afa86-117">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="afa86-118">Para configurar aprobadores de registros de documento entrante</span><span class="sxs-lookup"><span data-stu-id="afa86-118">To set up approvers of incoming document records</span></span>

<span data-ttu-id="afa86-119">Se deben configurar a los aprobadores de documentos entrantes como usuarios de flujo de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="afa86-119">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="afa86-120">Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación.</span><span class="sxs-lookup"><span data-stu-id="afa86-120">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="afa86-121">En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente.</span><span class="sxs-lookup"><span data-stu-id="afa86-121">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="afa86-122">Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="afa86-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="afa86-123">Para configurar un servicio de OCR</span><span class="sxs-lookup"><span data-stu-id="afa86-123">To set up an OCR service</span></span>

1. <span data-ttu-id="afa86-124">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración del servicio OCR** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="afa86-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="afa86-125">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="afa86-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="afa86-126">Los datos de inicio de sesión se cifran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="afa86-126">You login data is automatically encrypted.</span></span>

<span data-ttu-id="afa86-127">Para obtener más información, vea [Usar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="afa86-127">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="afa86-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="afa86-128">See Also</span></span>

[<span data-ttu-id="afa86-129">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="afa86-129">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="afa86-130">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="afa86-130">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="afa86-131">Compras</span><span class="sxs-lookup"><span data-stu-id="afa86-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="afa86-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="afa86-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
