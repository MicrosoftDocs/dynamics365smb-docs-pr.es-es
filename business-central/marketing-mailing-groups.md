---
title: Configurar grupos de correo para contactos | Documentos de Microsoft
description: Puede usar grupos de correo para identificar grupos de contactos que deben recibir la misma información, por ejemplo, para una campaña de marketing o una promoción.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6c089b772c139d0c0e9465f383ab39bd3c125dca
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805805"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="0d3a9-103">Configurar grupos de correo para contactos</span><span class="sxs-lookup"><span data-stu-id="0d3a9-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="0d3a9-104">Puede usar grupos de correo para identificar grupos de contactos que quiere que reciban la misma información.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="0d3a9-105">Por ejemplo, puede configurar un grupo de direcciones para los contactos a los que desea enviar una notificación de un movimiento de oficina u otro grupo para enviar regalos de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="0d3a9-106">El uso de grupos de correo en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="0d3a9-107">Primero, debe definir el código del grupo de correo.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-107">First, you define the mailing group code.</span></span> <span data-ttu-id="0d3a9-108">Solo debe realzar este paso una vez para cada grupo de correo.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="0d3a9-109">Una vez tenga código de grupo de correo, puede comenzar a asignar el código a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="0d3a9-110">Para definir códigos de grupo de correo</span><span class="sxs-lookup"><span data-stu-id="0d3a9-110">To define mailing group codes</span></span>
<span data-ttu-id="0d3a9-111">El código de grupo de correo define el tipo o la categoría del grupo, como MOVE para movimiento de oficina o GIFT para regalo de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="0d3a9-112">Puede tener varios códigos de grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-112">You can have several industry group codes.</span></span> <span data-ttu-id="0d3a9-113">Para definir los grupos de industria, puede usar la página **Grupos de correo**.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="0d3a9-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos de correo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d3a9-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="0d3a9-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="0d3a9-117">Para asignar grupos de correo a un contacto</span><span class="sxs-lookup"><span data-stu-id="0d3a9-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="0d3a9-118">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-118">Open the contact.</span></span>
2. <span data-ttu-id="0d3a9-119">Elija la acción **Grupos de correo**.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="0d3a9-120">Se abrirá la página **Grupos correo contacto**.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="0d3a9-121">En el campo **Código de grupos de correo**, seleccione el grupo de correo que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="0d3a9-122">Repita estos pasos para asignar todos los grupos de direcciones que desee.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="0d3a9-123">También puede asignar grupos de correo desde la lista de contactos con el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="0d3a9-124">Aparece automáticamente el número de grupos de direcciones asignados al contacto del campo **N.º grupos direcciones** en la sección **Segmentación** en la página **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="0d3a9-125">Después de asignar grupos de direcciones a sus contactos puede usar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="0d3a9-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="0d3a9-126">Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="0d3a9-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0d3a9-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d3a9-127">See Also</span></span>
[<span data-ttu-id="0d3a9-128">Crear contactos</span><span class="sxs-lookup"><span data-stu-id="0d3a9-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="0d3a9-129">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="0d3a9-129">Working with Business Central</span></span>](ui-work-product.md)
