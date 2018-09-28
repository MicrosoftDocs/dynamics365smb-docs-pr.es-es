---
title: Flujo de trabajo | Documentos de Microsoft
description: "Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7a7782fcb51eb9078cb62c4892814cd178518332
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="workflow"></a><span data-ttu-id="e11f7-105">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="e11f7-105">Workflow</span></span>
<span data-ttu-id="e11f7-106">Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios.</span><span class="sxs-lookup"><span data-stu-id="e11f7-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="e11f7-107">Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario.</span><span class="sxs-lookup"><span data-stu-id="e11f7-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="e11f7-108">Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="e11f7-109">En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="e11f7-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="e11f7-110">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e11f7-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="e11f7-111">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e11f7-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="e11f7-112">La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un número de flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="e11f7-113">El código para las plantillas de flujo de trabajo agregadas por Microsoft llevan el prefijo “MS-“.</span><span class="sxs-lookup"><span data-stu-id="e11f7-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="e11f7-114">Para más información, consulta las plantillas de la lista de flujo de trabajo en la ventana Plantillas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="e11f7-115">Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos personalizando el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e11f7-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="e11f7-116">Para obtener más información, consulte [Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) en la ayuda para desarrolladores e informáticos.</span><span class="sxs-lookup"><span data-stu-id="e11f7-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="e11f7-117">Los flujos de trabajo también se pueden iniciar desde Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e11f7-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="e11f7-118">Para obtener más información, vea [Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="e11f7-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="e11f7-119">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="e11f7-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="e11f7-120">**Para**</span><span class="sxs-lookup"><span data-stu-id="e11f7-120">**To**</span></span>|<span data-ttu-id="e11f7-121">**Consulte**</span><span class="sxs-lookup"><span data-stu-id="e11f7-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e11f7-122">Configure usuarios de flujo de trabajo, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="e11f7-123">Para nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e11f7-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="e11f7-124">Configuración de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="e11f7-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="e11f7-125">Habilite flujos de trabajo, actúe al recibir notificaciones de flujos de trabajo, incluida la aprobación de solicitudes, para realizar un paso del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="e11f7-126">Archive y elimine flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e11f7-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="e11f7-127">Uso de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="e11f7-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="e11f7-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e11f7-128">See Also</span></span>  
[<span data-ttu-id="e11f7-129">Ccial</span><span class="sxs-lookup"><span data-stu-id="e11f7-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="e11f7-130">Compras</span><span class="sxs-lookup"><span data-stu-id="e11f7-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="e11f7-131">Administrar proyectos</span><span class="sxs-lookup"><span data-stu-id="e11f7-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="e11f7-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e11f7-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

