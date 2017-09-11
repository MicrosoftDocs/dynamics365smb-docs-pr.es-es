---
title: "Configurar los niveles de organización para las personas de contacto | Documentos de Microsoft"
description: "Puede definir un nivel de organización y asignarlo a su contacto para indicar la posición que tiene en su empresa, por ejemplo alta gestión."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 927c27998bfaeb8d7247158cde1d1eb958a6911f
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="75515-103">Configurar niveles de organización en personas de contacto</span><span class="sxs-lookup"><span data-stu-id="75515-103">How to: Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="75515-104">Puede usar niveles de organización en sus contactos para especificar su posición en la empresa, por ejemplo, alta gestión.</span><span class="sxs-lookup"><span data-stu-id="75515-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="75515-105">Puede usar esta información al introducir información sobre sus contactos.</span><span class="sxs-lookup"><span data-stu-id="75515-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="75515-106">El uso de niveles de organización en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="75515-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="75515-107">Primero, debe definir el código de nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="75515-107">First, you define the organizational level code.</span></span> <span data-ttu-id="75515-108">Solo debe realizar este paso una vez para cada nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="75515-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="75515-109">Una vez tenga código de nivel de organización, puede comenzar a asignar el código a personas de contacto.</span><span class="sxs-lookup"><span data-stu-id="75515-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="75515-110">para definir un código de nivel de organización</span><span class="sxs-lookup"><span data-stu-id="75515-110">to define an organizational level code</span></span>
<span data-ttu-id="75515-111">El código de nivel de organización define el tipo o la categoría de nivel de organización, por ejemplo DIRGEN o DIRFIN.</span><span class="sxs-lookup"><span data-stu-id="75515-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="75515-112">Puede tener varios códigos de nivel de organización.</span><span class="sxs-lookup"><span data-stu-id="75515-112">You can have several organizational level codes.</span></span> <span data-ttu-id="75515-113">Para definir el nivel de organización, use la ventana **Niveles de organización**.</span><span class="sxs-lookup"><span data-stu-id="75515-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="75515-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Niveles de organización** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="75515-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="75515-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="75515-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="75515-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="75515-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="75515-117">para asignar niveles de organización a una persona de contacto</span><span class="sxs-lookup"><span data-stu-id="75515-117">to assign organizational levels to a contact person</span></span>
<span data-ttu-id="75515-118">Solo puede asignar niveles de organización a personas de contacto, no a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="75515-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="75515-119">Sólo puede asignar un nivel organización a cada contacto.</span><span class="sxs-lookup"><span data-stu-id="75515-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="75515-120">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="75515-120">Open the contact.</span></span>
2. <span data-ttu-id="75515-121">En el campo **Niveles de organización**, seleccione el código que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="75515-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="75515-122">Después de asignar niveles organización a sus contactos, puede utilizar esta información para crear segmentos.</span><span class="sxs-lookup"><span data-stu-id="75515-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="75515-123">Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="75515-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="75515-124">Para obtener más información, vea [Procedimiento: Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="75515-124">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="75515-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75515-125">See Also</span></span>
[<span data-ttu-id="75515-126">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="75515-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="75515-127">Crear personas de contacto</span><span class="sxs-lookup"><span data-stu-id="75515-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="75515-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75515-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

