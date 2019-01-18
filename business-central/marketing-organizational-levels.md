---
title: "Configurar los niveles de organización para las personas de contacto | Documentos de Microsoft"
description: "Puede definir un nivel de organización y asignarlo a su contacto para indicar la posición que tiene en su empresa, por ejemplo alta gestión."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 7f77fec3fad44d280f2337c6f23352ca2a91e00f
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="4070a-103">Configurar niveles de organización en personas de contacto</span><span class="sxs-lookup"><span data-stu-id="4070a-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="4070a-104">Puede usar niveles de organización en sus contactos para especificar su posición en la empresa, por ejemplo, alta gestión.</span><span class="sxs-lookup"><span data-stu-id="4070a-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="4070a-105">Puede usar esta información al introducir información sobre sus contactos.</span><span class="sxs-lookup"><span data-stu-id="4070a-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="4070a-106">El uso de niveles de organización en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="4070a-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="4070a-107">Primero, debe definir el código de nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="4070a-107">First, you define the organizational level code.</span></span> <span data-ttu-id="4070a-108">Solo debe realizar este paso una vez para cada nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="4070a-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="4070a-109">Una vez tenga código de nivel de organización, puede comenzar a asignar el código a personas de contacto.</span><span class="sxs-lookup"><span data-stu-id="4070a-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="4070a-110">Para definir un código de nivel de organización</span><span class="sxs-lookup"><span data-stu-id="4070a-110">To define an organizational level code</span></span>
<span data-ttu-id="4070a-111">El código de nivel de organización define el tipo o la categoría de nivel de organización, por ejemplo DIRGEN o DIRFIN.</span><span class="sxs-lookup"><span data-stu-id="4070a-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="4070a-112">Puede tener varios códigos de nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="4070a-112">You can have several organizational level codes.</span></span> <span data-ttu-id="4070a-113">Para definir el nivel de organización, use la página **Niveles de organización**.</span><span class="sxs-lookup"><span data-stu-id="4070a-113">To define the organizational level, you use the **Organizational Levels** page.</span></span>

1. <span data-ttu-id="4070a-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Niveles organización** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4070a-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="4070a-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="4070a-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="4070a-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="4070a-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="4070a-117">Para asignar niveles de organización a una persona de contacto</span><span class="sxs-lookup"><span data-stu-id="4070a-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="4070a-118">Solo puede asignar niveles de organización a personas de contacto, no a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="4070a-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="4070a-119">Sólo puede asignar un nivel organización a cada contacto.</span><span class="sxs-lookup"><span data-stu-id="4070a-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="4070a-120">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="4070a-120">Open the contact.</span></span>
2. <span data-ttu-id="4070a-121">En el campo **Niveles de organización**, seleccione el código que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="4070a-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="4070a-122">Después de asignar niveles organización a sus contactos, puede utilizar esta información para crear segmentos.</span><span class="sxs-lookup"><span data-stu-id="4070a-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="4070a-123">Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="4070a-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="4070a-124">Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="4070a-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4070a-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4070a-125">See Also</span></span>
[<span data-ttu-id="4070a-126">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="4070a-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="4070a-127">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="4070a-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="4070a-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4070a-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

