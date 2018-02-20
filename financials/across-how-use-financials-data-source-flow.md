---
title: Conectar los datos con Flow | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="60c5a-103">Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado</span><span class="sxs-lookup"><span data-stu-id="60c5a-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="60c5a-104">Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="60c5a-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="60c5a-105">Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.</span><span class="sxs-lookup"><span data-stu-id="60c5a-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="60c5a-106">Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow</span><span class="sxs-lookup"><span data-stu-id="60c5a-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="60c5a-107">En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="60c5a-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="60c5a-108">Seleccione **Mis flujos** en la cinta en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="60c5a-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="60c5a-109">En la ventana **Mis flujos**, elija la opción **Crear desde cero**.</span><span class="sxs-lookup"><span data-stu-id="60c5a-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="60c5a-110">En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles:</span><span class="sxs-lookup"><span data-stu-id="60c5a-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="60c5a-111">*Cuando se cree un registro*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-111">*When a record is created*,</span></span>  
    <span data-ttu-id="60c5a-112">*Cuando se elimine un registro*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="60c5a-113">*Cuando se modifique un registro*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="60c5a-114">*Cuando se solicite la aprobación de un cliente*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="60c5a-115">*Cuando se solicite la aprobación de un lote de diario general*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="60c5a-116">*Cuando se solicite la aprobación de una línea de diario general*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="60c5a-117">*Cuando se solicite la aprobación de un artículo*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="60c5a-118">*Cuando se solicite la aprobación de un documento de compra*,</span><span class="sxs-lookup"><span data-stu-id="60c5a-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="60c5a-119">*Cuando se solicite la aprobación de un documento de ventas*, o</span><span class="sxs-lookup"><span data-stu-id="60c5a-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="60c5a-120">*Cuando se solicite la aprobación de un proveedor*.</span><span class="sxs-lookup"><span data-stu-id="60c5a-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="60c5a-121">Flow le solicitará la información necesaria para conectarse con los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60c5a-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="60c5a-122">Si ha seleccionado uno de los disparadores siguientes: *Cuando se cree un registro*, *Cuando se modifique un registro* o *Cuando se elimine un registro*, debe seleccionar un nombre de la empresa y un nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="60c5a-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="60c5a-123">Si utiliza otro disparador, únicamente será necesario el nombre de la empresa para conectarse.</span><span class="sxs-lookup"><span data-stu-id="60c5a-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="60c5a-124">Flow mostrará una lista de empresas y tablas que están disponibles en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60c5a-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60c5a-125">Estas tablas, o extremos, representan todos los servicios web que haya publicado desde [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="60c5a-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="60c5a-126">Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.</span><span class="sxs-lookup"><span data-stu-id="60c5a-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="60c5a-127">Ya se ha conectado correctamente con los datos de Finance and Operations, Business edition y está preparado para comenzar a crear su flujo.</span><span class="sxs-lookup"><span data-stu-id="60c5a-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="60c5a-128">Para obtener más información, consulte la [documentación de Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="60c5a-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="60c5a-129">Para solucionar problemas de Microsoft Flow, vea [Solución de problemas de integración con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="60c5a-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="60c5a-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60c5a-130">See Also</span></span>
<span data-ttu-id="60c5a-131">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="60c5a-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="60c5a-132">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="60c5a-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="60c5a-133">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="60c5a-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="60c5a-134">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="60c5a-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="60c5a-135">Finanzas</span><span class="sxs-lookup"><span data-stu-id="60c5a-135">Finance</span></span>](finance.md)  

