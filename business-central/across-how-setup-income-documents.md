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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241513"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="9e9a6-103">Configurar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9e9a6-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="9e9a6-104">Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="9e9a6-105">Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documento entrante a menos que los documentos se aprueben primero, debe configurar a los aprobadores en la página **Aprobadores de documentos entrantes**.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="9e9a6-106">Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="9e9a6-107">Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="9e9a6-108">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="9e9a6-109">Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="9e9a6-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="9e9a6-110">Para configurar la característica Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9e9a6-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="9e9a6-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Para revisar la nueva ficha de producto**, y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e9a6-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="9e9a6-113">Para configurar aprobadores de registros de documento entrante</span><span class="sxs-lookup"><span data-stu-id="9e9a6-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="9e9a6-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Para revisar la nueva ficha de producto**, y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9e9a6-115">En la página **Configuración de documentos entrantes**, seleccione la opción **Aprobadores**.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="9e9a6-116">La página **Aprobadores de documentos entrantes** muestra todos los usuarios configurados en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9e9a6-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="9e9a6-117">Seleccione uno o más usuarios que pueden aprobar un documento entrante para que un documento o una línea de diario relacionado se pueda crear.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="9e9a6-118">Cuando se hayan configurado los aprobadores en la página **Aprobadores de documentos entrantes**, solo estos usuarios pueden aprobar un documento entrante si la casilla **Requerir aprobación para crear** de la página **Configuración de documentos entrantes** está marcada.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9e9a6-119">Esta configuración de aprobación no está relacionada con flujos de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="9e9a6-120">Para obtener más información, vea [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="9e9a6-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="9e9a6-121">Para configurar un servicio de OCR</span><span class="sxs-lookup"><span data-stu-id="9e9a6-121">To set up an OCR service</span></span>
1. <span data-ttu-id="9e9a6-122">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración del servicio OCR** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e9a6-123">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="9e9a6-124">Los datos de inicio de sesión se cifran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9e9a6-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e9a6-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9e9a6-125">See Also</span></span>
[<span data-ttu-id="9e9a6-126">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9e9a6-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="9e9a6-127">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9e9a6-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="9e9a6-128">Compras</span><span class="sxs-lookup"><span data-stu-id="9e9a6-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9e9a6-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e9a6-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
