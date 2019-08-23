---
title: Por qué no puedo personalizar una página | Documentos de Microsoft
description: Explica por qué no puede personalizar una página y qué puede hacer para desbloquearla.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796771"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="7b288-103">Por qué la página está bloqueada para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="7b288-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="7b288-104">Hay dos condiciones que le impiden personalizar una página.</span><span class="sxs-lookup"><span data-stu-id="7b288-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="7b288-105">La página está bloqueada (como se indica en ![Personalización bloqueada](media/personalization-lock-icon.png "Personalización bloqueada")) o está bloqueada (como se indica en ![Bloqueo de personalización](media/personalization-blocked-icon.png "Bloqueo de personalización")).</span><span class="sxs-lookup"><span data-stu-id="7b288-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="7b288-106">Bloqueado para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="7b288-106">Locked from Personalizing</span></span>

<span data-ttu-id="7b288-107">Si hay un icono ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") en el banner de **Personalización** cuando abre una página (como se muestra), significa que actualmente se le impide realizar más cambios de personalización en la página.</span><span class="sxs-lookup"><span data-stu-id="7b288-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="7b288-108">![Personalización bloqueada](media/personalization-locked.png "Personalización bloqueada")</span><span class="sxs-lookup"><span data-stu-id="7b288-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="7b288-109">Puede haber dos razones para ello:</span><span class="sxs-lookup"><span data-stu-id="7b288-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="7b288-110">Ha personalizado la página antes, pero lo ha hecho con una versión anterior del producto.</span><span class="sxs-lookup"><span data-stu-id="7b288-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="7b288-111">Hemos cambiado la manera en que la personalización funciona en segundo plano desde la última vez que personalizó la página.</span><span class="sxs-lookup"><span data-stu-id="7b288-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="7b288-112">Desafortunadamente, la formas de hacer las cosas antigua y nueva no funcionan juntas.</span><span class="sxs-lookup"><span data-stu-id="7b288-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="7b288-113">Hasta ahora, ha utilizado únicamente el [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] para personalizar la página.</span><span class="sxs-lookup"><span data-stu-id="7b288-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="7b288-114">Desbloqueo de la página</span><span class="sxs-lookup"><span data-stu-id="7b288-114">Unlocking the Page</span></span>

<span data-ttu-id="7b288-115">Si desea desbloquear una página y seguir personalizándola, seleccione ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") y, a continuación, **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="7b288-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="7b288-116">Antes de desbloquear la página, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7b288-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="7b288-117">Se borrará la personalización actual de la página.</span><span class="sxs-lookup"><span data-stu-id="7b288-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="7b288-118">La página volverá a su diseño original y tendrá que empezar desde cero.</span><span class="sxs-lookup"><span data-stu-id="7b288-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="7b288-119">En [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], la página permanecerá tal cual y no se verá afectada por los nuevos cambios de personalización realizados en el cliente de Business Central.</span><span class="sxs-lookup"><span data-stu-id="7b288-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="7b288-120">En el futuro, la personalización en [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] y el cliente de Business Central serán completamente independientes entre sí.</span><span class="sxs-lookup"><span data-stu-id="7b288-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="7b288-121">Bloqueado para evitar la personalización</span><span class="sxs-lookup"><span data-stu-id="7b288-121">Blocked from Personalizing</span></span>

<span data-ttu-id="7b288-122">Si hay un icono ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner Personalización, significa que se le impide hacer cualquier personalización de la página.</span><span class="sxs-lookup"><span data-stu-id="7b288-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="7b288-123">![Personalización bloqueada](media/personalization-blocked.png "Bloqueo de personalización")</span><span class="sxs-lookup"><span data-stu-id="7b288-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="7b288-124">La razón de esto es que el área de trabajo o rol que está actualmente asociado con su cuenta de usuario modifica esta página específicamente para su rol.</span><span class="sxs-lookup"><span data-stu-id="7b288-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="7b288-125">Póngase en contacto con su administrador para obtener ayuda o, si tiene sentido, intente cambiar a un área de trabajo (desde [**Mi configuración**](https://businesscentral.dynamics.com?page=9176 "Vaya directamente a la página de configuración del usuario en Business Central")) que incluya la personalización de rol para esta página.</span><span class="sxs-lookup"><span data-stu-id="7b288-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b288-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7b288-126">See Also</span></span>
[<span data-ttu-id="7b288-127">Personalización de su área de trabajo</span><span class="sxs-lookup"><span data-stu-id="7b288-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="7b288-128">Administrar la personalización</span><span class="sxs-lookup"><span data-stu-id="7b288-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="7b288-129">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="7b288-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="7b288-130">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="7b288-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
