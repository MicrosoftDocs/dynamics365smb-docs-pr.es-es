---
title: 'Procedimiento: Restringir y permitir el uso de un registro | Documentos de Microsoft'
description: Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a95eaa2f0933c6724b1e9158c675ad1a27e0ba2a
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="8ea21-103">Restringir y permitir el uso de un registro</span><span class="sxs-lookup"><span data-stu-id="8ea21-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="8ea21-104">Si desea restringir un registro para que no se use en ciertas actividades, por ejemplo, hasta que se haya aprobado el registro, puede introducir dos respuestas de flujo de trabajo en un flujo de trabajo que controle el uso del registro.</span><span class="sxs-lookup"><span data-stu-id="8ea21-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="8ea21-105">Una respuesta del flujo de trabajo restringirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8ea21-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="8ea21-106">Otra respuesta del flujo de trabajo permitirá la utilización del registro definida por el evento y las condiciones del flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8ea21-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="8ea21-107">Hay dos respuestas existentes en la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] con este fin: **Restringir el uso de un registro**</span><span class="sxs-lookup"><span data-stu-id="8ea21-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="8ea21-108">y **Permitir el uso de un registro**.</span><span class="sxs-lookup"><span data-stu-id="8ea21-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="8ea21-109">La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] permite restringir el registro de un registro, que se exporte como pago o que se imprima como cheque.</span><span class="sxs-lookup"><span data-stu-id="8ea21-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="8ea21-110">Para utilizar otras restricciones, un socio de Microsoft debe personalizar el código de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8ea21-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8ea21-111">La funcionalidad de flujo de trabajo para restringir y para permitir usar registros no está relacionada con la funcionalidad para bloquear el registro de registros de producto, cliente y proveedor.</span><span class="sxs-lookup"><span data-stu-id="8ea21-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="8ea21-112">El procedimiento siguiente describe cómo restringir el registro de pedidos de compra hasta que se hayan aprobado.</span><span class="sxs-lookup"><span data-stu-id="8ea21-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="8ea21-113">El nuevo flujo de trabajo se basará en la plantilla existente de flujo de trabajo de aprobación de factura de compra.</span><span class="sxs-lookup"><span data-stu-id="8ea21-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="8ea21-114">Para crear un paso de flujo de trabajo que restrinja el registro de pedidos de compra no aprobados</span><span class="sxs-lookup"><span data-stu-id="8ea21-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="8ea21-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ea21-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8ea21-116">En la página **Flujos de trabajo**, cree un nuevo flujo de trabajo denominado Flujo de trabajo de aprobación pedido compra.</span><span class="sxs-lookup"><span data-stu-id="8ea21-116">On the **Workflows** page, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="8ea21-117">Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="8ea21-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="8ea21-118">Seleccione la acción **Copiar desde plantilla de flujo de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="8ea21-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="8ea21-119">Elija el campo **Código de flujo de trabajo** de origen y, a continuación, en la página **Plantillas de flujo de trabajo**, seleccione la plantilla de flujo de trabajo de aprobación de factura de compra.</span><span class="sxs-lookup"><span data-stu-id="8ea21-119">Choose the **Source Workflow Code** field, and then, on the **Workflow Templates** page, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="8ea21-120">Tenga en cuenta que los dos primeros pasos del flujo de trabajo se aplican a restringir y permitir el uso de facturas de compra.</span><span class="sxs-lookup"><span data-stu-id="8ea21-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="8ea21-121">Proceda a modificar la condición del evento en el primer paso del nuevo flujo de trabajo para especificar que se aplica a los pedidos de compra.</span><span class="sxs-lookup"><span data-stu-id="8ea21-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="8ea21-122">En la ficha desplegable **Pasos de flujo de trabajo**, elija el campo **Condiciones de evento** y, a continuación, para el filtro **Tipo documento**, seleccione **Pedido**.</span><span class="sxs-lookup"><span data-stu-id="8ea21-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="8ea21-123">Empiece a editar, eliminar o agregar otros pasos de flujo de trabajo de acuerdo con un proceso empresarial que empiece por restringir el registro de los pedidos de compra no aprobados.</span><span class="sxs-lookup"><span data-stu-id="8ea21-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ea21-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ea21-124">See Also</span></span>  
<span data-ttu-id="8ea21-125">[Crear flujos de trabajo](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="8ea21-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="8ea21-126">Flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="8ea21-126">Workflow</span></span>](across-workflow.md)   

