---
title: Exportar e importar flujos de trabajo | Documentos de Microsoft
description: Para transferir flujos de trabajo a otras bases de datos de Business Central, por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a0a67c3b6a706820c8b5fb073c090a6586435ca7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806563"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="998a3-103">Importar y exportar flujos de trabajo</span><span class="sxs-lookup"><span data-stu-id="998a3-103">Export and Import Workflows</span></span>
<span data-ttu-id="998a3-104">Para transferir flujos de trabajo a otras bases de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="998a3-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="998a3-105">Otra forma de crear rápidamente flujos de trabajo es crearlos a partir de plantillas de flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="998a3-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="998a3-106">Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="998a3-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="998a3-107">En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas.</span><span class="sxs-lookup"><span data-stu-id="998a3-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="998a3-108">Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta.</span><span class="sxs-lookup"><span data-stu-id="998a3-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="998a3-109">Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="998a3-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="998a3-110">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="998a3-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="998a3-111">Para exportar un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="998a3-111">To export a workflow</span></span>  
1.  <span data-ttu-id="998a3-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="998a3-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="998a3-113">Seleccione un flujo de trabajo y, a continuación, la acción **Exportar a archivo**.</span><span class="sxs-lookup"><span data-stu-id="998a3-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="998a3-114">En la página **Exportar archivo**, elija el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="998a3-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="998a3-115">En la página **Exportar**, seleccione una ubicación de archivo y elija el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="998a3-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="998a3-116">Para importar un flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="998a3-116">To import a workflow</span></span>  
1.  <span data-ttu-id="998a3-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="998a3-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="998a3-118">Elija la acción **Importar desde archivo**.</span><span class="sxs-lookup"><span data-stu-id="998a3-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="998a3-119">En la página **Importar**, seleccione el archivo XML que contiene el flujo de trabajo y elija el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="998a3-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="998a3-120">Si el código de flujo de trabajo ya existe en la base de datos, los pasos del flujo de trabajo se sobrescribirán con los pasos del flujo de trabajo importado.</span><span class="sxs-lookup"><span data-stu-id="998a3-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="998a3-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="998a3-121">See Also</span></span>  
 <span data-ttu-id="998a3-122">[Crear flujos de trabajo](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="998a3-123">[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="998a3-124">[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="998a3-125">[Eliminar flujos de trabajo](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="998a3-126">[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="998a3-127">[Configuración de flujos de trabajo](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="998a3-128">[Uso de flujos de trabajo](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="998a3-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="998a3-129">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="998a3-129">Workflow</span></span>](across-workflow.md)   
