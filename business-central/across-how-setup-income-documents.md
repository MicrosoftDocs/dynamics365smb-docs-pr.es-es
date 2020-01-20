---
title: Configurar documentos entrantes | Documentos de Microsoft
description: Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 12/09/2019
ms.author: sgroespe
ms.openlocfilehash: e67ca1c0b26d7e4a81e53854ca31efc64a366c3f
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910497"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="e0f68-103">Configurar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="e0f68-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="e0f68-104">Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.</span><span class="sxs-lookup"><span data-stu-id="e0f68-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="e0f68-105">Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documentos entrantes a menos que los documentos se aprueben primero, debe configurar aprobadores de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e0f68-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="e0f68-106">Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="e0f68-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="e0f68-107">Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="e0f68-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="e0f68-108">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="e0f68-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="e0f68-109">Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="e0f68-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="e0f68-110">Para configurar la característica Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="e0f68-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="e0f68-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de ventas y cobros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e0f68-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="e0f68-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e0f68-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="e0f68-113">Para configurar aprobadores de registros de documento entrante</span><span class="sxs-lookup"><span data-stu-id="e0f68-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="e0f68-114">Se deben configurar a los aprobadores de documentos entrantes como usuarios de flujo de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="e0f68-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="e0f68-115">Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación.</span><span class="sxs-lookup"><span data-stu-id="e0f68-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="e0f68-116">En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente.</span><span class="sxs-lookup"><span data-stu-id="e0f68-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="e0f68-117">Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="e0f68-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="e0f68-118">Para configurar un servicio de OCR</span><span class="sxs-lookup"><span data-stu-id="e0f68-118">To set up an OCR service</span></span>
1. <span data-ttu-id="e0f68-119">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración del servicio OCR** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e0f68-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="e0f68-120">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e0f68-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="e0f68-121">Los datos de inicio de sesión se cifran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e0f68-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0f68-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e0f68-122">See Also</span></span>
[<span data-ttu-id="e0f68-123">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="e0f68-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="e0f68-124">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="e0f68-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="e0f68-125">Compras</span><span class="sxs-lookup"><span data-stu-id="e0f68-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="e0f68-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e0f68-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
