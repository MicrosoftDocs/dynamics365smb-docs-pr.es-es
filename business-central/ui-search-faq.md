---
title: Preguntas más frecuentes acerca de la opción Dígame | Documentos de Microsoft
description: Este artículo proporciona respuestas a las preguntas que nuestros socios y clientes suelen hacer sobre la función Dígame.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 88a1e6cc711888a3cf68744d0ea6bbfdee41aea3
ms.sourcegitcommit: 49309bdff9b680a35032b355fe97c565845dba15
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/01/2019
ms.locfileid: "2695100"
---
# <a name="tell-me-faq"></a><span data-ttu-id="60b68-103">FAQ acerca de la función Dígame</span><span class="sxs-lookup"><span data-stu-id="60b68-103">Tell Me FAQ</span></span>
<span data-ttu-id="60b68-104">Este tema responde las preguntas que nuestros usuarios avanzados suelen hacer sobre la función Dígame.</span><span class="sxs-lookup"><span data-stu-id="60b68-104">This topic answers questions that our advanced users often ask about the Tell Me feature.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="60b68-105">¿Se pueden ver todas las acciones de mi página actual en la función Dígame?</span><span class="sxs-lookup"><span data-stu-id="60b68-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="60b68-106">No.</span><span class="sxs-lookup"><span data-stu-id="60b68-106">No.</span></span> <span data-ttu-id="60b68-107">Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.</span><span class="sxs-lookup"><span data-stu-id="60b68-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="60b68-108">¿Los resultados de la función Dígame se filtran por permisos?</span><span class="sxs-lookup"><span data-stu-id="60b68-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="60b68-109">Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="60b68-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="60b68-110">Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="60b68-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="60b68-111">Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.</span><span class="sxs-lookup"><span data-stu-id="60b68-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="60b68-112">¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?</span><span class="sxs-lookup"><span data-stu-id="60b68-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="60b68-113">La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones, pero no la documentación de ayuda personalizada.</span><span class="sxs-lookup"><span data-stu-id="60b68-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="60b68-114">Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="60b68-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="60b68-115">¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?</span><span class="sxs-lookup"><span data-stu-id="60b68-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="60b68-116">La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente.</span><span class="sxs-lookup"><span data-stu-id="60b68-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="60b68-117">La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes.</span><span class="sxs-lookup"><span data-stu-id="60b68-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="60b68-118">A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.</span><span class="sxs-lookup"><span data-stu-id="60b68-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365fin_mdmd-does-that-include-tell-me"></a><span data-ttu-id="60b68-119">Utilizo [!INCLUDE[d365fin](includes/d365fin_md.md)] local.</span><span class="sxs-lookup"><span data-stu-id="60b68-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="60b68-120">¿Incluye la función Dígame?</span><span class="sxs-lookup"><span data-stu-id="60b68-120">Does that include Tell Me?</span></span>
<span data-ttu-id="60b68-121">Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero no documentación, o aplicaciones y servicios de consultoría en AppSource.</span><span class="sxs-lookup"><span data-stu-id="60b68-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="60b68-122">¿Está disponible para todos los factores de forma?</span><span class="sxs-lookup"><span data-stu-id="60b68-122">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="60b68-123">La función Dígame solo está disponible en el cliente web o en la aplicación de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="60b68-123">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="60b68-124">¿Los resultados de la documentación están disponibles en algún idioma?</span><span class="sxs-lookup"><span data-stu-id="60b68-124">Are the documentation results available in any language?</span></span>
<span data-ttu-id="60b68-125">Los artículos de ayuda se mostrarán en el idioma que ha especificado en **Mi configuración**, si la ayuda está disponible en ese idioma.</span><span class="sxs-lookup"><span data-stu-id="60b68-125">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a><span data-ttu-id="60b68-126">¿Por qué no veo un icono de marcador para mis resultados de búsqueda?</span><span class="sxs-lookup"><span data-stu-id="60b68-126">Why don't I see a bookmark icon for my search results?</span></span>
<span data-ttu-id="60b68-127">El icono de marcador no se muestra en la ventana Dígame cuando la personalización está deshabilitada para un rol de usuario.</span><span class="sxs-lookup"><span data-stu-id="60b68-127">The bookmark icon is not displayed in the Tell Me window when personalization is disabled for a user role.</span></span>

### <a name="is-the-bookmark-icon-available-for-reports"></a><span data-ttu-id="60b68-128">¿El icono de marcador está disponible para los informes?</span><span class="sxs-lookup"><span data-stu-id="60b68-128">Is the bookmark icon available for reports?</span></span>
<span data-ttu-id="60b68-129">Nº</span><span class="sxs-lookup"><span data-stu-id="60b68-129">No.</span></span> <span data-ttu-id="60b68-130">Solo puede marcar un vínculo a una página o cualquier resultado de búsqueda que se muestre en la sección **Páginas y tareas** de la ventana Dígame.</span><span class="sxs-lookup"><span data-stu-id="60b68-130">You can only bookmark a link to a page or any search results that are displayed in the **Pages and Tasks** section of the Tell Me window.</span></span>


## <a name="see-also"></a><span data-ttu-id="60b68-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60b68-131">See Also</span></span>  
[<span data-ttu-id="60b68-132">Guardar y personalizar vistas de lista</span><span class="sxs-lookup"><span data-stu-id="60b68-132">Save and Personalize List Views</span></span>](ui-views.md)  
[<span data-ttu-id="60b68-133">Búsqueda de páginas e información con Dígame</span><span class="sxs-lookup"><span data-stu-id="60b68-133">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
[<span data-ttu-id="60b68-134">Búsqueda de páginas con el explorador de roles</span><span class="sxs-lookup"><span data-stu-id="60b68-134">Finding Pages with the Role Explorer</span></span>](ui-role-explorer.md)
