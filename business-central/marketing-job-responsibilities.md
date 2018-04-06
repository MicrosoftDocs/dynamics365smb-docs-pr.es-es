---
title: Configurar responsabilidades de cargo para contactos | Documentos de Microsoft
description: "Puede definir una responsabilidad de cargo y asignarla a un contacto para indicar las tareas de las que es responsable que su contacto en su empresa, por ejemplo, TI o producción."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c62aea1e830b1b37e470fdf7ffbe8227bec41f6
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-job-responsibilities-for-contact-persons"></a><span data-ttu-id="c199f-103">Configurar responsabilidades cargo para las personas de contacto.</span><span class="sxs-lookup"><span data-stu-id="c199f-103">Set Up Job Responsibilities for Contact Persons</span></span>
<span data-ttu-id="c199f-104">Puede agregar información sobre las responsabilidades cargo de las personas de contacto para indicar que son responsables en su empresa, por ejemplo, en TI, gestión o producción.</span><span class="sxs-lookup"><span data-stu-id="c199f-104">You can add information about the job responsibilities of contact persons to indicate what the contact person is responsible for within their company, for example, IT, management, or production.</span></span> <span data-ttu-id="c199f-105">Puede usar esta información al introducir información sobre sus contactos.</span><span class="sxs-lookup"><span data-stu-id="c199f-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="c199f-106">El uso de las responsabilidades cargo en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="c199f-106">Using job responsibilities on contacts is a two-step process.</span></span> <span data-ttu-id="c199f-107">Primero, debe definir el código de la responsabilidad cargo.</span><span class="sxs-lookup"><span data-stu-id="c199f-107">First, you define the job responsibility code.</span></span> <span data-ttu-id="c199f-108">Solo debe realzar este paso una vez para cada una.</span><span class="sxs-lookup"><span data-stu-id="c199f-108">You only have to perform this step one time for each job responsibility.</span></span> <span data-ttu-id="c199f-109">Una vez tenga un código de responsabilidad cargo, puede empezar a asignarlo a sus personas de contacto.</span><span class="sxs-lookup"><span data-stu-id="c199f-109">Once you have a job responsibility code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-job-responsibility-code"></a><span data-ttu-id="c199f-110">Para definir un código de responsabilidad de cargo</span><span class="sxs-lookup"><span data-stu-id="c199f-110">To define a job responsibility code</span></span>
<span data-ttu-id="c199f-111">El código de responsabilidad cargo define el tipo o la categoría del trabajo, por ejemplo MARKETING o COMPRA.</span><span class="sxs-lookup"><span data-stu-id="c199f-111">The job responsibility code defines the type or category of the job, such a MARKETING or PURCHASE.</span></span> <span data-ttu-id="c199f-112">Puede tener varios códigos de responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="c199f-112">You can have several job responsibility codes.</span></span> <span data-ttu-id="c199f-113">Para definir la responsabilidad cargo, use la ventana **Responsabilidades cargo**.</span><span class="sxs-lookup"><span data-stu-id="c199f-113">To define the job responsibility, you use the **Job Responsibilities** window.</span></span>

1. <span data-ttu-id="c199f-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Responsabilidades cargo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c199f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Responsibilities**, and then choose the related link.</span></span>
2. <span data-ttu-id="c199f-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="c199f-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="c199f-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="c199f-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a><span data-ttu-id="c199f-117">Para asignar responsabilidades de cargo a una persona de contacto</span><span class="sxs-lookup"><span data-stu-id="c199f-117">To assign job responsibilities to a contact person</span></span>
<span data-ttu-id="c199f-118">No puede asignar responsabilidades cargo a contactos que sean empresas.</span><span class="sxs-lookup"><span data-stu-id="c199f-118">You cannot assign job responsibilities to contact companies.</span></span>

1. <span data-ttu-id="c199f-119">Abra la persona de contacto.</span><span class="sxs-lookup"><span data-stu-id="c199f-119">Open the contact person.</span></span>
2. <span data-ttu-id="c199f-120">Elija la acción **Persona** y, a continuación, elija la acción **Responsabilidades cargo**.</span><span class="sxs-lookup"><span data-stu-id="c199f-120">Choose the **Person** action, and then choose the **Job Responsibilities** action.</span></span> <span data-ttu-id="c199f-121">Aparecerá la ventana **Cargos contactos**.</span><span class="sxs-lookup"><span data-stu-id="c199f-121">The **Contact Job Responsibilities** window opens.</span></span>
3. <span data-ttu-id="c199f-122">En el campo **Cód. cargo contacto**, seleccione la responsabilidad cargo que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="c199f-122">In the **Job Responsibility Code** field, select the job responsibility that you want to assign.</span></span>

<span data-ttu-id="c199f-123">Repita estos pasos para asignar todas las responsabilidades del cargo que desee.</span><span class="sxs-lookup"><span data-stu-id="c199f-123">Repeat these steps to assign as many job responsibilities as you want.</span></span> <span data-ttu-id="c199f-124">También puede asignar responsabilidades cargo de la lista de contactos siguiendo el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c199f-124">You can also assign job responsibilities from the contact list by following the same procedure.</span></span>

<span data-ttu-id="c199f-125">El número de responsabilidades cargo que ha asignado al contacto se muestra en el campo **N.º responsabilidades cargo** en la sección **Segmentación** en la ventana **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="c199f-125">The number of job responsibilities you have assigned to the contact is displayed in the **No. of Job Responsibilities** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="c199f-126">Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="c199f-126">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="c199f-127">Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="c199f-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c199f-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c199f-128">See Also</span></span>
[<span data-ttu-id="c199f-129">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="c199f-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="c199f-130">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="c199f-130">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="c199f-131">Trabajar con Financials</span><span class="sxs-lookup"><span data-stu-id="c199f-131">Working with Financials</span></span>](ui-work-product.md)

