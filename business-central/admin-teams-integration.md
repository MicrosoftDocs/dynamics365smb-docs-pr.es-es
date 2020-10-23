---
title: Administrar la integración de Microsoft Teams con Business Central | Microsoft Docs
description: Administrar la integración de Business Central con Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989363"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="5ee6e-103">Habilitar la integración de Microsoft Teams con Business Central</span><span class="sxs-lookup"><span data-stu-id="5ee6e-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="5ee6e-104">Este artículo proporciona una descripción general de lo que puede hacer como administrador para controlar la integración de Microsoft Teams con [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5ee6e-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="5ee6e-105">En Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="5ee6e-106">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5ee6e-106">Minimum requirements</span></span>

<span data-ttu-id="5ee6e-107">Esta sección describe los requisitos mínimos para que la características de la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] trabajen en Teams.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="5ee6e-108">Licencias requeridas</span><span class="sxs-lookup"><span data-stu-id="5ee6e-108">Required licenses</span></span>

    <span data-ttu-id="5ee6e-109">Esta tabla le ofrece una descripción general de las licencias necesarias que la características de la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] trabajen en Teams.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="5ee6e-110">Qué</span><span class="sxs-lookup"><span data-stu-id="5ee6e-110">What</span></span>|<span data-ttu-id="5ee6e-111">Licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-111">Teams license</span></span>|<span data-ttu-id="5ee6e-112">Licencia de Business Central</span><span class="sxs-lookup"><span data-stu-id="5ee6e-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="5ee6e-113">Pegue un vínculo a un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación y envíelo como una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="5ee6e-114">![marca de verificación](media/check.png "comprobar")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="5ee6e-115">![marca de verificación](media/check.png "comprobar")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="5ee6e-116">Vea una tarjeta de un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="5ee6e-117">![marca de verificación](media/check.png "comprobar")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="5ee6e-118">Vea más detalles de la tarjeta de un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="5ee6e-119">![marca de verificación](media/check.png "comprobar")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="5ee6e-120">![marca de verificación](media/check.png "comprobar")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="5ee6e-121">Permitir vistas previas de URL</span><span class="sxs-lookup"><span data-stu-id="5ee6e-121">Allow URL previews</span></span>

    <span data-ttu-id="5ee6e-122">La configuración de directiva **Permitir vistas previas de URL** debe estar activada.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="5ee6e-123">De lo contrario, no se puede generar una tarjeta para los vínculos de Business Central pegados en una conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="5ee6e-124">Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="5ee6e-125">Administrar la aplicación Business Central (opcional)</span><span class="sxs-lookup"><span data-stu-id="5ee6e-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="5ee6e-126">Como administrador de Teams, puede administrar todas las aplicaciones de su organización, incluida la aplicación [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5ee6e-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="5ee6e-127">Puede aprobar o instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para su organización, bloquear la instalación de la aplicación para el usuario y más.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="5ee6e-128">Para obtener más información, consulte los siguientes productos de la documentación en Microsoft Teams:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="5ee6e-129">Administre sus aplicaciones en el centro de administración de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="5ee6e-130">Administrar las directivas de configuración de la aplicación en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="5ee6e-131">En [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="5ee6e-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="5ee6e-132">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5ee6e-132">Minimum requirements</span></span>

- <span data-ttu-id="5ee6e-133">Versión de [!INCLUDE [prodshort](includes/prodshort.md)]:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="5ee6e-134">Lanzamiento de versiones 2 (versión 17) de 2020 de [!INCLUDE [prodshort](includes/prodshort.md)], o posterior.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="5ee6e-135">La integración de Teams solo es compatible con [!INCLUDE [prodshort](includes/prodshort.md)] en línea; no en las instalaciones.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="5ee6e-136">Codeunit **Proveedor de resumen de página 2718** se publica como servicio web:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="5ee6e-137">Esta codeunit se publica como un servicio web de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="5ee6e-138">La codeunit es parte de la aplicación del sistema [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5ee6e-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="5ee6e-139">Se utiliza para obtener los datos de campo de una página [!INCLUDE [prodshort](includes/prodshort.md)] agregada a una conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="5ee6e-140">Permisos de usuario:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-140">User permissions:</span></span>

    <span data-ttu-id="5ee6e-141">En su mayor parte, las páginas y los datos que los usuarios pueden ver y editar en una conversación de Teams están controlados por sus permisos en [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="5ee6e-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="5ee6e-142">Para pegar un vínculo [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación de Teams y hacer que se expanda en una tarjeta, los usuarios deben tener al menos permiso de lectura en la página y sus datos.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="5ee6e-143">Una vez que se envía una tarjeta a una conversación, cualquier usuario de esa conversación puede ver esa tarjeta sin permiso de Business Central.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="5ee6e-144">Para ver más detalles de una tarjeta o abrir el registro en [!INCLUDE [prodshort](includes/prodshort.md)], los usuarios deben tener permiso de lectura en la página y sus datos.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="5ee6e-145">Para cambiar los datos, el usuario necesita modificar los permisos.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="5ee6e-146">Para obtener información sobre permisos, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee6e-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ee6e-147">See Also</span></span>
[<span data-ttu-id="5ee6e-148">Descripción general de la integración de Business Central y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="5ee6e-149">[Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="5ee6e-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="5ee6e-150">Desarrollo para la integración de Teams</span><span class="sxs-lookup"><span data-stu-id="5ee6e-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="5ee6e-151">Introducción</span><span class="sxs-lookup"><span data-stu-id="5ee6e-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
