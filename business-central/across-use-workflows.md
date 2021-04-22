---
title: Uso de flujos de trabajo
description: Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Conozca los diferentes pasos que debe seguir para comenzar a usar los flujos de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92b32957bb7b20dda304be8a99bb17c5c5947498
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787012"
---
# <a name="using-workflows"></a><span data-ttu-id="1b04e-104">Uso de flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="1b04e-104">Using Workflows</span></span>
<span data-ttu-id="1b04e-105">Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios.</span><span class="sxs-lookup"><span data-stu-id="1b04e-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="1b04e-106">Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario.</span><span class="sxs-lookup"><span data-stu-id="1b04e-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="1b04e-107">Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1b04e-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="1b04e-108">Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo, crear los flujos de trabajo, potencialmente precedidos por personalización del código y especificar cómo reciben notificaciones los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1b04e-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="1b04e-109">Para obtener más información, consulte [Configurar flujos de trabajo](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="1b04e-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1b04e-110">Los pasos habituales del flujo de trabajo están relacionados con usuarios que solicitan aprobación de tareas y aprobadores que aceptan o rechazan las solicitudes de aprobación.</span><span class="sxs-lookup"><span data-stu-id="1b04e-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="1b04e-111">Por tanto, muchos temas sobre cómo utilizar los flujos de trabajo hacen referencia a las aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="1b04e-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="1b04e-112">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="1b04e-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="1b04e-113">**Para**</span><span class="sxs-lookup"><span data-stu-id="1b04e-113">**To**</span></span>|<span data-ttu-id="1b04e-114">**Consulte**</span><span class="sxs-lookup"><span data-stu-id="1b04e-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="1b04e-115">Establecer un flujo de trabajo para comenzar cuando se produzca el primer evento de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1b04e-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="1b04e-116">Activar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="1b04e-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="1b04e-117">Solicitar aprobación de una tarea como aprobador, aceptar, rechazar o delegar aprobaciones, y enviar o ver notificaciones de aprobación.</span><span class="sxs-lookup"><span data-stu-id="1b04e-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="1b04e-118">Usar flujos de trabajo de aprobación del producto</span><span class="sxs-lookup"><span data-stu-id="1b04e-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="1b04e-119">Cree pasos de flujo de trabajo que restrinjan el uso de cierto tipo de registros antes de producirse un determinado evento, por ejemplo que el registro se apruebe.</span><span class="sxs-lookup"><span data-stu-id="1b04e-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="1b04e-120">Restringir y permitir el uso de un registro</span><span class="sxs-lookup"><span data-stu-id="1b04e-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="1b04e-121">Ver los casos del paso del flujo de trabajo con estado de completado.</span><span class="sxs-lookup"><span data-stu-id="1b04e-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="1b04e-122">Ver instancias de paso de flujo de trabajo archivadas</span><span class="sxs-lookup"><span data-stu-id="1b04e-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="1b04e-123">Eliminar un flujo de trabajo que está seguro que no se utilizará más.</span><span class="sxs-lookup"><span data-stu-id="1b04e-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="1b04e-124">Eliminar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="1b04e-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="1b04e-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1b04e-125">See Also</span></span>  
<span data-ttu-id="1b04e-126">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="1b04e-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="1b04e-127">[Flujo de trabajo](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="1b04e-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="1b04e-128">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b04e-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]