---
title: Asignar y administrar tareas | Documentos de Microsoft
description: Obtener información sobre cómo asignar tareas a los usuarios, incluido su contable, en Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 5befadf7a162cc2094fbb1ef426e25d02d50e856
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241173"
---
# <a name="define-user-tasks"></a><span data-ttu-id="e2adf-103">Definir tareas de usuario</span><span class="sxs-lookup"><span data-stu-id="e2adf-103">Define User Tasks</span></span>
<span data-ttu-id="e2adf-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], puede crear tareas para recordarle que debe realizar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="e2adf-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="e2adf-105">Puede crear tareas para usted, pero también puede asignar tareas a otras personas o a otra persona en su organización</span><span class="sxs-lookup"><span data-stu-id="e2adf-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="e2adf-106">Gestionar tareas de usuario</span><span class="sxs-lookup"><span data-stu-id="e2adf-106">Managing User Tasks</span></span>
<span data-ttu-id="e2adf-107">La página **Tareas del usuario** muestra todas las tareas, y podrá crear y asignar fácilmente tareas nuevas.</span><span class="sxs-lookup"><span data-stu-id="e2adf-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="e2adf-108">Cuando crea una tarea, puede especificar la fecha de inicio y la fecha de vencimiento, y puede agregar un enlace a la página [!INCLUDE[d365fin](includes/d365fin_md.md)] donde el usuario debe realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e2adf-108">When you create a task, you can specify the start date and due date, and you can add a link to the page in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="e2adf-109">Por ejemplo, puede crear una tarea para ver todas las facturas de ventas publicadas.</span><span class="sxs-lookup"><span data-stu-id="e2adf-109">For example, you can create a task for yourself to view all posted sales invoices.</span></span> <span data-ttu-id="e2adf-110">En ese caso, vincule la tarea a la página 143, Histórico facturas venta.</span><span class="sxs-lookup"><span data-stu-id="e2adf-110">In that case, you link the task to page 143, Posted Sales Invoices.</span></span>  

<span data-ttu-id="e2adf-111">![Ejemplo de tarea de usuario](media/across-user-tasks/sample-user-task.png "Ejemplo de tarea de usuario")</span><span class="sxs-lookup"><span data-stu-id="e2adf-111">![Example of a User Task](media/across-user-tasks/sample-user-task.png "Example of a user task")</span></span>

> [!TIP]  
>  <span data-ttu-id="e2adf-112">Use la búsqueda en el campo **Página** y el campo **Buscar página o informe** para encontrar la página que desea.</span><span class="sxs-lookup"><span data-stu-id="e2adf-112">Use the look-up in the **Page** field and then use the **Search for Page or Report** field to find the page that you want.</span></span> <span data-ttu-id="e2adf-113">Para obtener más información, vea [Búsqueda de una página o un informe](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="e2adf-113">For more information, see [Searching for a Page or Report](ui-search.md).</span></span>  

### <a name="picking-up-user-tasks"></a><span data-ttu-id="e2adf-114">Selección de tareas de usuario</span><span class="sxs-lookup"><span data-stu-id="e2adf-114">Picking Up User Tasks</span></span>
<span data-ttu-id="e2adf-115">En las Áreas de trabajo Administrador de negocio y Contable, un mosaico muestra las tareas pendientes que se asignan a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="e2adf-115">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="e2adf-116">Para elegir una tarea, simplemente selecciónela de la lista de tareas pendientes del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2adf-116">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="e2adf-117">En la cinta de opciones, el vínculo **Ir al elemento de la tarea** abrirá la página en la que puede realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e2adf-117">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="e2adf-118">Cuando haya terminado una tarea, simplemente márquela como completada.</span><span class="sxs-lookup"><span data-stu-id="e2adf-118">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="e2adf-119">Eliminar tareas de usuario</span><span class="sxs-lookup"><span data-stu-id="e2adf-119">Deleting User Tasks</span></span>
<span data-ttu-id="e2adf-120">Si desea eliminar de forma masiva todas o algunas tareas del usuario, puede usar el informe **Eliminar tareas de usuario**.</span><span class="sxs-lookup"><span data-stu-id="e2adf-120">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="e2adf-121">En la página de solicitud, puede establecer filtros para determinar qué tareas deben eliminarse.</span><span class="sxs-lookup"><span data-stu-id="e2adf-121">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2adf-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e2adf-122">See Also</span></span>
[<span data-ttu-id="e2adf-123">Buscar una página o informe</span><span class="sxs-lookup"><span data-stu-id="e2adf-123">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="e2adf-124">[Experiencias contables en [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="e2adf-124">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
