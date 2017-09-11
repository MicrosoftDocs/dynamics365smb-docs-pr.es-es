---
title: Configurar grupos de correo para contactos | Documentos de Microsoft
description: "Puede usar grupos de correo para identificar grupos de contactos que deben recibir la misma información, por ejemplo, para una campaña de marketing o una promoción."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bc1c89b87426b72ce4f9522cb7f0dc31c77acad1
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-mailing-groups-for-contacts"></a><span data-ttu-id="46a62-103">Configurar grupos de correo para contactos</span><span class="sxs-lookup"><span data-stu-id="46a62-103">How to: Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="46a62-104">Puede usar grupos de correo para identificar grupos de contactos que quiere que reciban la misma información.</span><span class="sxs-lookup"><span data-stu-id="46a62-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="46a62-105">Por ejemplo, puede configurar un grupo de direcciones para los contactos a los que desea enviar una notificación de un movimiento de oficina u otro grupo para enviar regalos de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="46a62-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="46a62-106">El uso de grupos de correo en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="46a62-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="46a62-107">Primero, debe definir el código del grupo de correo.</span><span class="sxs-lookup"><span data-stu-id="46a62-107">First, you define the mailing group code.</span></span> <span data-ttu-id="46a62-108">Solo debe realzar este paso una vez para cada grupo de correo.</span><span class="sxs-lookup"><span data-stu-id="46a62-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="46a62-109">Una vez tenga código de grupo de correo, puede comenzar a asignar el código a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="46a62-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="46a62-110">Para definir códigos de grupo de correo</span><span class="sxs-lookup"><span data-stu-id="46a62-110">To define mailing group codes</span></span>
<span data-ttu-id="46a62-111">El código de grupo de correo define el tipo o la categoría del grupo, como MOVE para movimiento de oficina o GIFT para regalo de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="46a62-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="46a62-112">Puede tener varios códigos de grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="46a62-112">You can have several industry group codes.</span></span> <span data-ttu-id="46a62-113">Para definir los grupos de industria, pude usar la ventana **Grupos de correo**.</span><span class="sxs-lookup"><span data-stu-id="46a62-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="46a62-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de correo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="46a62-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="46a62-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="46a62-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="46a62-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="46a62-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="46a62-117"><a name="AssignMailGroupContact"></a> Para asignar grupos de correo a un contacto</span><span class="sxs-lookup"><span data-stu-id="46a62-117"><a name="AssignMailGroupContact"></a> To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="46a62-118">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="46a62-118">Open the contact.</span></span>
2. <span data-ttu-id="46a62-119">Elija la acción **Grupos de correo**.</span><span class="sxs-lookup"><span data-stu-id="46a62-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="46a62-120">Se abrirá la ventana **Grupos direcciones contacto**.</span><span class="sxs-lookup"><span data-stu-id="46a62-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="46a62-121">En el campo **Código de grupos de correo**, seleccione el grupo de correo que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="46a62-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="46a62-122">Repita estos pasos para asignar todos los grupos de direcciones que desee.</span><span class="sxs-lookup"><span data-stu-id="46a62-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="46a62-123">También puede asignar grupos de correo desde la lista de contactos con el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="46a62-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="46a62-124">Aparece automáticamente el número de grupos de direcciones asignados al contacto del campo **N.º grupos direcciones** en la sección **Segmentación** en la ventana **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="46a62-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="46a62-125">Después de asignar grupos de direcciones a sus contactos puede usar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="46a62-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="46a62-126">Para obtener más información, vea [Procedimiento: Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="46a62-126">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46a62-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46a62-127">See Also</span></span>
[<span data-ttu-id="46a62-128">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="46a62-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="46a62-129">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="46a62-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="46a62-130">Trabajar con Financials</span><span class="sxs-lookup"><span data-stu-id="46a62-130">Working with Financials</span></span>](ui-work-product.md)

