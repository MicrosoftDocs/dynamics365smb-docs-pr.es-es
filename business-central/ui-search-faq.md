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
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d04f78b31b9fb0403201cb9e5cb1f98f1ef935e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248022"
---
# <a name="tell-me-faq"></a><span data-ttu-id="f8a87-103">FAQ acerca de la función Dígame</span><span class="sxs-lookup"><span data-stu-id="f8a87-103">Tell Me FAQ</span></span>
<span data-ttu-id="f8a87-104">Este tema responde a las preguntas que nuestros usuarios avanzados suelen hacer sobre la nueva función Dígame que ha reemplazado la función anterior de búsqueda de páginas conocida como **Buscar páginas e informes**.</span><span class="sxs-lookup"><span data-stu-id="f8a87-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="f8a87-105">¿Se pueden ver todas las acciones de mi página actual en la función Dígame?</span><span class="sxs-lookup"><span data-stu-id="f8a87-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="f8a87-106">No.</span><span class="sxs-lookup"><span data-stu-id="f8a87-106">No.</span></span> <span data-ttu-id="f8a87-107">Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.</span><span class="sxs-lookup"><span data-stu-id="f8a87-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="f8a87-108">¿Los resultados de la función Dígame se filtran por permisos?</span><span class="sxs-lookup"><span data-stu-id="f8a87-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="f8a87-109">Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="f8a87-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="f8a87-110">Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="f8a87-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="f8a87-111">Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.</span><span class="sxs-lookup"><span data-stu-id="f8a87-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="f8a87-112">¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?</span><span class="sxs-lookup"><span data-stu-id="f8a87-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="f8a87-113">La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones, pero no la documentación de ayuda personalizada.</span><span class="sxs-lookup"><span data-stu-id="f8a87-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="f8a87-114">Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="f8a87-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="f8a87-115">¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?</span><span class="sxs-lookup"><span data-stu-id="f8a87-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="f8a87-116">La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente.</span><span class="sxs-lookup"><span data-stu-id="f8a87-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="f8a87-117">La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes.</span><span class="sxs-lookup"><span data-stu-id="f8a87-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="f8a87-118">A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.</span><span class="sxs-lookup"><span data-stu-id="f8a87-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="f8a87-119">Utilizo [!INCLUDE[d365fin](includes/d365fin_md.md)] local.</span><span class="sxs-lookup"><span data-stu-id="f8a87-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f8a87-120">¿Incluye la función Dígame?</span><span class="sxs-lookup"><span data-stu-id="f8a87-120">Does that include Tell Me?</span></span>
<span data-ttu-id="f8a87-121">Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero no documentación, o aplicaciones y servicios de consultoría en AppSource.</span><span class="sxs-lookup"><span data-stu-id="f8a87-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span> <span data-ttu-id="f8a87-122">Los usuarios que se conectan a [!INCLUDE[d365fin](includes/d365fin_md.md)] desde el cliente de Dynamics NAV continúan usando la Búsqueda de páginas.</span><span class="sxs-lookup"><span data-stu-id="f8a87-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="f8a87-123">¿Está disponible para todos los factores de forma?</span><span class="sxs-lookup"><span data-stu-id="f8a87-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="f8a87-124">La función Dígame solo está disponible en el cliente web o en la aplicación de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a87-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="f8a87-125">¿Los resultados de la documentación están disponibles en algún idioma?</span><span class="sxs-lookup"><span data-stu-id="f8a87-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="f8a87-126">Los artículos de ayuda se mostrarán en el idioma que ha especificado en **Mi configuración**, si la ayuda está disponible en ese idioma.</span><span class="sxs-lookup"><span data-stu-id="f8a87-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8a87-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f8a87-127">See Also</span></span>  
[<span data-ttu-id="f8a87-128">Encontrar características e información</span><span class="sxs-lookup"><span data-stu-id="f8a87-128">Finding Features and Information</span></span>](ui-search.md)
