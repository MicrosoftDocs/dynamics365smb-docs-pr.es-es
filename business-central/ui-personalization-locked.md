---
title: Por qué no puedo personalizar una página | Documentos de Microsoft
description: Explica por qué no puede personalizar una página y qué puede hacer para desbloquearla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c77664a1013804de13303c8e1d162c437cf5d6e7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315137"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="d61e6-103">Por qué la página está bloqueada para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="d61e6-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="d61e6-104">Hay dos condiciones que le impiden personalizar una página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="d61e6-105">La página está bloqueada (como se indica en el icono ![Personalización bloqueada](media/personalization-lock-icon.png "Personalización bloqueada")) o está bloqueada (como se indica en el icono ![Bloqueo de personalización](media/personalization-blocked-icon.png "Bloqueo de personalización")).</span><span class="sxs-lookup"><span data-stu-id="d61e6-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="d61e6-106">Bloqueado para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="d61e6-106">Locked from Personalizing</span></span>

<span data-ttu-id="d61e6-107">Si hay un icono ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") en el banner **Personalización** cuando abre una página, significa que actualmente se le impide realizar más cambios de personalización en la página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="d61e6-108">Puede haber dos razones para ello:</span><span class="sxs-lookup"><span data-stu-id="d61e6-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="d61e6-109">Ha personalizado la página antes, pero lo ha hecho con una versión anterior del producto.</span><span class="sxs-lookup"><span data-stu-id="d61e6-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="d61e6-110">Hemos cambiado la manera en que la personalización funciona en segundo plano desde la última vez que personalizó la página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="d61e6-111">Desafortunadamente, la formas de hacer las cosas antigua y nueva no funcionan juntas.</span><span class="sxs-lookup"><span data-stu-id="d61e6-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="d61e6-112">Hasta ahora, ha utilizado únicamente el [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] para personalizar la página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="d61e6-113">Desbloqueo de la página</span><span class="sxs-lookup"><span data-stu-id="d61e6-113">Unlocking the Page</span></span>

<span data-ttu-id="d61e6-114">Si desea desbloquear una página y seguir personalizándola, seleccione el icono ![Personalización bloqueada](media/personalization-lock-icon.png "Personalización bloqueada") y, a continuación, elija la acción **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="d61e6-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="d61e6-115">Antes de desbloquear la página, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d61e6-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="d61e6-116">Se borrará la personalización actual de la página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="d61e6-117">La página volverá a su diseño original y tendrá que empezar desde cero.</span><span class="sxs-lookup"><span data-stu-id="d61e6-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="d61e6-118">En [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la página permanecerá tal cual y no se verá afectada por los nuevos cambios de personalización realizados en el cliente de Business Central.</span><span class="sxs-lookup"><span data-stu-id="d61e6-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="d61e6-119">En el futuro, la personalización en [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] y el cliente de Business Central serán completamente independientes entre sí.</span><span class="sxs-lookup"><span data-stu-id="d61e6-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="d61e6-120">Bloqueado para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="d61e6-120">Blocked from Personalizing</span></span>

<span data-ttu-id="d61e6-121">Si hay un icono ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner **Personalización**, significa que se le impide hacer cualquier personalización de la página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="d61e6-122">La razón de esto es que el área de trabajo o rol que está actualmente asociado con su cuenta de usuario modifica esta página específicamente para su rol.</span><span class="sxs-lookup"><span data-stu-id="d61e6-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="d61e6-123">Póngase en contacto con su administrador para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="d61e6-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="d61e6-124">Alternativamente, intente cambiar a un área de trabajo que incluya la adaptación de roles para esta página.</span><span class="sxs-lookup"><span data-stu-id="d61e6-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="d61e6-125">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d61e6-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d61e6-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d61e6-126">See Also</span></span>
[<span data-ttu-id="d61e6-127">Personalizar el área de trabajo</span><span class="sxs-lookup"><span data-stu-id="d61e6-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="d61e6-128">Personalizar páginas para perfiles</span><span class="sxs-lookup"><span data-stu-id="d61e6-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="d61e6-129">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="d61e6-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="d61e6-130">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="d61e6-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
