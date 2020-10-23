---
title: Utilizar flujos de trabajo | Documentos de Microsoft
description: Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d608841bf5d5586bd0ef84ef554055517def0eb8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917956"
---
# <a name="using-workflows"></a><span data-ttu-id="6e5a9-105">Uso de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="6e5a9-105">Using Workflows</span></span>
<span data-ttu-id="6e5a9-106">Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="6e5a9-107">Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="6e5a9-108">Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="6e5a9-109">Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo, crear los flujos de trabajo, potencialmente precedidos por personalización del código y especificar cómo reciben notificaciones los usuarios.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="6e5a9-110">Para obtener más información, consulte [Configurar flujos de trabajo](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="6e5a9-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6e5a9-111">Los pasos habituales del flujo de trabajo están relacionados con usuarios que solicitan aprobación de tareas y aprobadores que aceptan o rechazan las solicitudes de aprobación.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="6e5a9-112">Por tanto, muchos temas sobre cómo utilizar los flujos de trabajo hacen referencia a las aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="6e5a9-113">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="6e5a9-114">**Para**</span><span class="sxs-lookup"><span data-stu-id="6e5a9-114">**To**</span></span>|<span data-ttu-id="6e5a9-115">**Consulte**</span><span class="sxs-lookup"><span data-stu-id="6e5a9-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6e5a9-116">Establecer un flujo de trabajo para comenzar cuando se produzca el primer evento de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="6e5a9-117">Activar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="6e5a9-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="6e5a9-118">Solicitar aprobación de una tarea como aprobador, aceptar, rechazar o delegar aprobaciones, y enviar o ver notificaciones de aprobación.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="6e5a9-119">Usar flujos de trabajo de aprobación del producto</span><span class="sxs-lookup"><span data-stu-id="6e5a9-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="6e5a9-120">Cree pasos de flujo de trabajo que restrinjan el uso de cierto tipo de registros antes de producirse un determinado evento, por ejemplo que el registro se apruebe.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="6e5a9-121">Restringir y permitir el uso de un registro</span><span class="sxs-lookup"><span data-stu-id="6e5a9-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="6e5a9-122">Ver los casos del paso del flujo de trabajo con estado de completado.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="6e5a9-123">Ver instancias de paso de flujo de trabajo archivadas</span><span class="sxs-lookup"><span data-stu-id="6e5a9-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="6e5a9-124">Eliminar un flujo de trabajo que está seguro que no se utilizará más.</span><span class="sxs-lookup"><span data-stu-id="6e5a9-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="6e5a9-125">Eliminar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="6e5a9-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="6e5a9-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e5a9-126">See Also</span></span>  
<span data-ttu-id="6e5a9-127">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="6e5a9-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="6e5a9-128">[Flujo de trabajo](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="6e5a9-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="6e5a9-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e5a9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
