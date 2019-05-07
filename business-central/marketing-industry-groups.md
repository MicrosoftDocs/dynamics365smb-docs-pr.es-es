---
title: Configurar grupos de industria para empresas de contacto | Documentos de Microsoft
description: Describe cómo definir un grupo de industria y asignarlo a una empresa de contacto, por ejemplo, en la industria minorista o la industria del automóvil.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6f4fd9ef35c9a5287b01740861ad0b835c319ff4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "921584"
---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="d4c7f-103">Configurar grupos industria para empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="d4c7f-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="d4c7f-104">Puede usar grupos industria para indicar el tipo de industria al que pertenecen sus contactos, por ejemplo, la industria de fabricación o la industria del automóvil.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="d4c7f-105">El uso de grupos industria en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="d4c7f-106">Primero, debe definir el código del grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-106">First, you define the industry group code.</span></span> <span data-ttu-id="d4c7f-107">Solo debe realzar este paso una vez para cada grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="d4c7f-108">Una vez tenga código de grupo de industria, puede comenzar a asignar el código a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d4c7f-109">Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="d4c7f-110">Para definir un código de grupo de industria</span><span class="sxs-lookup"><span data-stu-id="d4c7f-110">To define an industry group code</span></span>
<span data-ttu-id="d4c7f-111">El código de grupo de industria define el tipo o la categoría del grupo, como ADVERT para publicidad o PRESS para televisión y radio.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="d4c7f-112">Puede tener varios códigos de grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-112">You can have several industry group codes.</span></span> <span data-ttu-id="d4c7f-113">Para definir los grupos de industria, puede usar la página **Grupos industria**.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-113">To define the industry groups, you use the **Industry Groups** page.</span></span>

1. <span data-ttu-id="d4c7f-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos industria** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="d4c7f-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="d4c7f-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignIndustryGroupContact"></a> <span data-ttu-id="d4c7f-117">Para asignar grupos de industria a un contacto</span><span class="sxs-lookup"><span data-stu-id="d4c7f-117">To assign industry groups to a contact</span></span>
<span data-ttu-id="d4c7f-118">No puede asignar grupos de industria a una persona de contacto, solo a empresas.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="d4c7f-119">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-119">Open the contact.</span></span>
2. <span data-ttu-id="d4c7f-120">Elija la acción **Empresa** y, a continuación, elija la acción **Grupos de industria**.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="d4c7f-121">Se abrirá la página **Grupos industria contacto**.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-121">The **Contact Industry Groups** page opens.</span></span>
3. <span data-ttu-id="d4c7f-122">En el campo **Código de grupos de industria**, seleccione el grupo de industria que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="d4c7f-123">Repita estos pasos para asignar todos los grupos de industria que desee.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="d4c7f-124">También puede asignar grupos de industria desde la lista de contactos con el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="d4c7f-125">Aparece automáticamente el número de grupos de industrias asignados al contacto del campo **N.º grupos industrias** en la sección **Segmentación** en la página **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="d4c7f-126">Después de asignar grupos de industria a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="d4c7f-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="d4c7f-127">Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="d4c7f-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c7f-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d4c7f-128">See Also</span></span>
[<span data-ttu-id="d4c7f-129">Crear contactos</span><span class="sxs-lookup"><span data-stu-id="d4c7f-129">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="d4c7f-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4c7f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
