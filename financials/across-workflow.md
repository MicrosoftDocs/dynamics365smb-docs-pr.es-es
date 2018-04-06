---
title: Flujo de trabajo | Documentos de Microsoft
description: "Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 861ff6ac3c2789f83379e4c01c0e1b8f5847d2d6
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="workflow"></a><span data-ttu-id="37fc2-105">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="37fc2-105">Workflow</span></span>
<span data-ttu-id="37fc2-106">Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios.</span><span class="sxs-lookup"><span data-stu-id="37fc2-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="37fc2-107">Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario.</span><span class="sxs-lookup"><span data-stu-id="37fc2-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="37fc2-108">Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="37fc2-109">En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="37fc2-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="37fc2-110">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="37fc2-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="37fc2-111">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="37fc2-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="37fc2-112">La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un número de flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="37fc2-113">El código para las plantillas de flujo de trabajo agregadas por Microsoft llevan el prefijo “MS-“.</span><span class="sxs-lookup"><span data-stu-id="37fc2-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="37fc2-114">Para más información, consulta las plantillas de la lista de flujo de trabajo en la ventana Plantillas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="37fc2-115">Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos personalizando el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="37fc2-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="37fc2-116">Para obtener más información, consulte [Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) en la ayuda para desarrolladores e informáticos.</span><span class="sxs-lookup"><span data-stu-id="37fc2-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>  

 <span data-ttu-id="37fc2-117">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="37fc2-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="37fc2-118">**Para**</span><span class="sxs-lookup"><span data-stu-id="37fc2-118">**To**</span></span>|<span data-ttu-id="37fc2-119">**Consulte**</span><span class="sxs-lookup"><span data-stu-id="37fc2-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="37fc2-120">Configure usuarios de flujo de trabajo, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-120">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="37fc2-121">Para nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="37fc2-121">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="37fc2-122">Configuración de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="37fc2-122">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="37fc2-123">Habilite flujos de trabajo, actúe al recibir notificaciones de flujos de trabajo, incluida la aprobación de solicitudes, para realizar un paso del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-123">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="37fc2-124">Archive y elimine flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37fc2-124">Archive and delete workflows.</span></span>|[<span data-ttu-id="37fc2-125">Uso de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="37fc2-125">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="37fc2-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37fc2-126">See Also</span></span>  
[<span data-ttu-id="37fc2-127">Ccial</span><span class="sxs-lookup"><span data-stu-id="37fc2-127">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="37fc2-128">Compras</span><span class="sxs-lookup"><span data-stu-id="37fc2-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="37fc2-129">Administrar proyectos</span><span class="sxs-lookup"><span data-stu-id="37fc2-129">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="37fc2-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37fc2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

