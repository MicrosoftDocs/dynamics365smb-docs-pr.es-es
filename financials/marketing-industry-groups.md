---
title: Configurar grupos de industria para empresas de contacto | Documentos de Microsoft
description: "Describe cómo definir un grupo de industria y asignarlo a una empresa de contacto, por ejemplo, en la industria minorista o la industria del automóvil."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fef570e7e56e348a25ae660fa9248b529d0bfde
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="99de6-103">Configurar grupos de industria para empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="99de6-103">How to: Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="99de6-104">Puede usar grupos industria para indicar el tipo de industria al que pertenecen sus contactos, por ejemplo, la industria de fabricación o la industria del automóvil.</span><span class="sxs-lookup"><span data-stu-id="99de6-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="99de6-105">El uso de grupos industria en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="99de6-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="99de6-106">Primero, debe definir el código del grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="99de6-106">First, you define the industry group code.</span></span> <span data-ttu-id="99de6-107">Solo debe realzar este paso una vez para cada grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="99de6-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="99de6-108">Una vez tenga código de grupo de industria, puede comenzar a asignar el código a empresas de contacto.</span><span class="sxs-lookup"><span data-stu-id="99de6-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="99de6-109">Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.</span><span class="sxs-lookup"><span data-stu-id="99de6-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="99de6-110">Para definir un código de grupo de industria</span><span class="sxs-lookup"><span data-stu-id="99de6-110">To define an industry group code</span></span>
<span data-ttu-id="99de6-111">El código de grupo de industria define el tipo o la categoría del grupo, como ADVERT para publicidad o PRESS para televisión y radio.</span><span class="sxs-lookup"><span data-stu-id="99de6-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="99de6-112">Puede tener varios códigos de grupo de industria.</span><span class="sxs-lookup"><span data-stu-id="99de6-112">You can have several industry group codes.</span></span> <span data-ttu-id="99de6-113">Para definir los grupos de industria, pude usar la ventana **Grupos industria**.</span><span class="sxs-lookup"><span data-stu-id="99de6-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="99de6-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos industria** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="99de6-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="99de6-115">Seleccione la acción **Nuevo** e introduzca un código y una descripción.</span><span class="sxs-lookup"><span data-stu-id="99de6-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="99de6-116">El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.</span><span class="sxs-lookup"><span data-stu-id="99de6-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="99de6-117"><a name="AssignIndustryGroupContact"></a> Para asignar grupos de industria a un contacto</span><span class="sxs-lookup"><span data-stu-id="99de6-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="99de6-118">No puede asignar grupos de industria a una persona de contacto, solo a empresas.</span><span class="sxs-lookup"><span data-stu-id="99de6-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="99de6-119">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="99de6-119">Open the contact.</span></span>
2. <span data-ttu-id="99de6-120">Elija la acción **Empresa** y, a continuación, elija la acción **Grupos de industria**.</span><span class="sxs-lookup"><span data-stu-id="99de6-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="99de6-121">Se abrirá la ventana **Grupos industria contacto**.</span><span class="sxs-lookup"><span data-stu-id="99de6-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="99de6-122">En el campo **Código de grupos de industria**, seleccione el grupo de industria que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="99de6-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="99de6-123">Repita estos pasos para asignar todos los grupos de industria que desee.</span><span class="sxs-lookup"><span data-stu-id="99de6-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="99de6-124">También puede asignar grupos de industria desde la lista de contactos con el mismo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="99de6-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="99de6-125">Aparece automáticamente el número de grupos de industrias asignados al contacto del campo **N.º grupos industrias** en la sección **Segmentación** en la ventana **Contacto**.</span><span class="sxs-lookup"><span data-stu-id="99de6-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="99de6-126">Después de asignar grupos de industria a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos.</span><span class="sxs-lookup"><span data-stu-id="99de6-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="99de6-127">Para obtener más información, vea [Procedimiento: Agregar contactos a segmentos](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="99de6-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="99de6-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99de6-128">See Also</span></span>
[<span data-ttu-id="99de6-129">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="99de6-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="99de6-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99de6-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

