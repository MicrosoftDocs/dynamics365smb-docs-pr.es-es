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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6381fc0949c3f6789a6b3387d119051403bcbb4a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="f4314-103">Configurar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="f4314-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="f4314-104">Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la ventana **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.</span><span class="sxs-lookup"><span data-stu-id="f4314-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="f4314-105">Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documento entrante a menos que los documentos se aprueben primero, debe configurar a los aprobadores en la ventana **Aprobadores de documentos entrantes**.</span><span class="sxs-lookup"><span data-stu-id="f4314-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="f4314-106">Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="f4314-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="f4314-107">Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="f4314-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="f4314-108">Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.</span><span class="sxs-lookup"><span data-stu-id="f4314-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="f4314-109">Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="f4314-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="f4314-110">Para configurar la característica Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="f4314-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="f4314-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f4314-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f4314-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f4314-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="f4314-113">Para configurar aprobadores de registros de documento entrante</span><span class="sxs-lookup"><span data-stu-id="f4314-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="f4314-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f4314-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f4314-115">En la ventana **Configuración de documentos entrantes**, seleccione la opción **Aprobadores**.</span><span class="sxs-lookup"><span data-stu-id="f4314-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="f4314-116">La ventana **Aprobadores de documentos entrantes** muestra todos los usuarios configurados en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f4314-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="f4314-117">Seleccione uno o más usuarios que pueden aprobar un documento entrante para que un documento o una línea de diario relacionado se pueda crear.</span><span class="sxs-lookup"><span data-stu-id="f4314-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="f4314-118">Cuando se hayan configurado los aprobadores en la ventana **Aprobadores de documentos entrantes**, solo estos usuarios pueden aprobar un documento entrante si la casilla **Requerir aprobación para crear** de la ventana **Configuración de documentos entrantes** está marcada.</span><span class="sxs-lookup"><span data-stu-id="f4314-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f4314-119">Esta configuración de aprobación no está relacionada con flujos de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="f4314-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="f4314-120">Para obtener más información, vea [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f4314-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="f4314-121">Para configurar un servicio de OCR</span><span class="sxs-lookup"><span data-stu-id="f4314-121">To set up an OCR service</span></span>
1. <span data-ttu-id="f4314-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio OCR** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f4314-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="f4314-123">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f4314-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a><span data-ttu-id="f4314-124">Para cifrar la información de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="f4314-124">To encrypt your login information</span></span>
<span data-ttu-id="f4314-125">Se recomienda usar esta función para proteger la información de inicio de sesión que se introduce en la ventana **Configuración del servicio OCR**.</span><span class="sxs-lookup"><span data-stu-id="f4314-125">It is recommended that you protect the logon information that you enter in the **OCR Service Setup** window.</span></span> <span data-ttu-id="f4314-126">Puede cifrar datos en el servidor generando claves de cifrado nuevas o importando claves existentes que se activarán en la instancia del servidor que conecta con la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f4314-126">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span>

1. <span data-ttu-id="f4314-127">En la ventana **Configuración del servicio OCR**, seleccione la acción **Administración del cifrado**.</span><span class="sxs-lookup"><span data-stu-id="f4314-127">In the **OCR Service Setup** window, choose the **Encryption Management** action.</span></span>
2. <span data-ttu-id="f4314-128">En la ventana **Administración del cifrado de datos**, habilite el cifrado de los datos.</span><span class="sxs-lookup"><span data-stu-id="f4314-128">In the **Data Encryption Management** window, enable encryption of your data.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4314-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4314-129">See Also</span></span>
[<span data-ttu-id="f4314-130">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="f4314-130">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="f4314-131">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="f4314-131">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="f4314-132">Compras</span><span class="sxs-lookup"><span data-stu-id="f4314-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f4314-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f4314-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

