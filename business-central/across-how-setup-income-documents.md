---
title: Configurar documentos entrantes | Documentos de Microsoft
description: "Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: ea5673f341954960852de33cb94ee5722c8dbe26
ms.contentlocale: es-es
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="c2414-103">Configurar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="c2414-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="c2414-104">Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la ventana **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.</span><span class="sxs-lookup"><span data-stu-id="c2414-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="c2414-105">Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documento entrante a menos que los documentos se aprueben primero, debe configurar a los aprobadores en la ventana **Aprobadores de documentos entrantes**.</span><span class="sxs-lookup"><span data-stu-id="c2414-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="c2414-106">Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c2414-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="c2414-107">Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="c2414-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="c2414-108">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="c2414-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="c2414-109">Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="c2414-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="c2414-110">Para configurar la característica Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="c2414-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="c2414-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c2414-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2414-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c2414-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="c2414-113">Para configurar aprobadores de registros de documento entrante</span><span class="sxs-lookup"><span data-stu-id="c2414-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="c2414-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c2414-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c2414-115">En la ventana **Configuración de documentos entrantes**, seleccione la opción **Aprobadores**.</span><span class="sxs-lookup"><span data-stu-id="c2414-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="c2414-116">La ventana **Aprobadores de documentos entrantes** muestra todos los usuarios configurados en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2414-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="c2414-117">Seleccione uno o más usuarios que pueden aprobar un documento entrante para que un documento o una línea de diario relacionado se pueda crear.</span><span class="sxs-lookup"><span data-stu-id="c2414-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="c2414-118">Cuando se hayan configurado los aprobadores en la ventana **Aprobadores de documentos entrantes**, solo estos usuarios pueden aprobar un documento entrante si la casilla **Requerir aprobación para crear** de la ventana **Configuración de documentos entrantes** está marcada.</span><span class="sxs-lookup"><span data-stu-id="c2414-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c2414-119">Esta configuración de aprobación no está relacionada con flujos de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="c2414-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="c2414-120">Para obtener más información, vea [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c2414-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="c2414-121">Para configurar un servicio de OCR</span><span class="sxs-lookup"><span data-stu-id="c2414-121">To set up an OCR service</span></span>
1. <span data-ttu-id="c2414-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio OCR** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c2414-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2414-123">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c2414-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="c2414-124">Los datos de inicio de sesión se cifran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c2414-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2414-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2414-125">See Also</span></span>
[<span data-ttu-id="c2414-126">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="c2414-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="c2414-127">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="c2414-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="c2414-128">Compras</span><span class="sxs-lookup"><span data-stu-id="c2414-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c2414-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2414-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

