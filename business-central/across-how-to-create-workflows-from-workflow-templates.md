---
title: Procedimiento para crear flujos de trabajo a partir de plantillas de flujo de trabajo | Documentos de Microsoft
description: Para ahorrar el tiempo al crear nuevos flujos de trabajo, puede crear flujos de trabajo a partir de plantillas de flujo de trabajo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6376c38e2580881a6d3fbb7ffd7661302a448c1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384529"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="816ac-103">Crear flujos de trabajo a partir de plantillas de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="816ac-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="816ac-104">Para ahorrar el tiempo al crear nuevos flujos de trabajo, puede crear flujos de trabajo a partir de plantillas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="816ac-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="816ac-105">Las plantillas de flujo de trabajo son flujos de trabajo no editables que existen en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="816ac-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="816ac-106">Los códigos para las plantillas de flujo de trabajo añadidas por Microsoft llevan el prefijo “MS-“.</span><span class="sxs-lookup"><span data-stu-id="816ac-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="816ac-107">Otra manera de crear rápidamente un flujo de trabajo es importar un flujo de trabajo existente que tenga en un archivo fuera de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="816ac-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="816ac-108">Para obtener más información, consulte [Exportación e importación de flujos de trabajo](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="816ac-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="816ac-109">En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="816ac-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="816ac-110">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="816ac-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="816ac-111">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="816ac-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="816ac-112">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="816ac-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="816ac-113">Para crear un flujo de trabajo a partir de una plantilla de flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="816ac-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="816ac-114">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="816ac-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="816ac-115">Seleccione la acción **Crear flujo de trabajo desde una plantilla**.</span><span class="sxs-lookup"><span data-stu-id="816ac-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="816ac-116">Se abre la página **Plantillas de flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="816ac-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="816ac-117">Seleccione una plantilla de flujo de trabajo y haga clic en el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="816ac-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="816ac-118">La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="816ac-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="816ac-119">El valor del campo **Código** se amplia, por ejemplo, con “-01” para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="816ac-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="816ac-120">Empiece a crear el flujo de trabajo modificando los pasos del flujo de trabajo o agregando nuevos pasos.</span><span class="sxs-lookup"><span data-stu-id="816ac-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="816ac-121">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="816ac-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="816ac-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="816ac-122">See Also</span></span>  
 <span data-ttu-id="816ac-123">[Crear flujos de trabajo](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="816ac-124">[Importar y exportar flujos de trabajo](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="816ac-125">[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="816ac-126">[Eliminar flujos de trabajo](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="816ac-127">[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="816ac-128">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="816ac-129">[Uso de flujos de trabajo](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="816ac-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="816ac-130">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="816ac-130">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]