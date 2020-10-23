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
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Habilitar la integración de Microsoft Teams con Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Este artículo proporciona una descripción general de lo que puede hacer como administrador para controlar la integración de Microsoft Teams con [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>En Microsoft Teams

### <a name="minimum-requirements"></a>Requisitos mínimos

Esta sección describe los requisitos mínimos para que la características de la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] trabajen en Teams.

- Licencias requeridas

    Esta tabla le ofrece una descripción general de las licencias necesarias que la características de la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] trabajen en Teams.

    |Qué|Licencia de Teams|Licencia de Business Central|
    |----|---|---|
    |Pegue un vínculo a un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación y envíelo como una tarjeta.|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|
    |Vea una tarjeta de un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación.|![marca de verificación](media/check.png "comprobar")||
    |Vea más detalles de la tarjeta de un registro de [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación.|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|

- Permitir vistas previas de URL

    La configuración de directiva **Permitir vistas previas de URL** debe estar activada. De lo contrario, no se puede generar una tarjeta para los vínculos de Business Central pegados en una conversación de Teams. Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Administrar la aplicación Business Central (opcional)

Como administrador de Teams, puede administrar todas las aplicaciones de su organización, incluida la aplicación [!INCLUDE [prodshort](includes/prodshort.md)]. Puede aprobar o instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para su organización, bloquear la instalación de la aplicación para el usuario y más.

Para obtener más información, consulte los siguientes productos de la documentación en Microsoft Teams:

- [Administre sus aplicaciones en el centro de administración de Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Administrar las directivas de configuración de la aplicación en Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>En [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Requisitos mínimos

- Versión de [!INCLUDE [prodshort](includes/prodshort.md)]:

    Lanzamiento de versiones 2 (versión 17) de 2020 de [!INCLUDE [prodshort](includes/prodshort.md)], o posterior. La integración de Teams solo es compatible con [!INCLUDE [prodshort](includes/prodshort.md)] en línea; no en las instalaciones.

- Codeunit **Proveedor de resumen de página 2718** se publica como servicio web:

    Esta codeunit se publica como un servicio web de forma predeterminada. La codeunit es parte de la aplicación del sistema [!INCLUDE [prodshort](includes/prodshort.md)]. Se utiliza para obtener los datos de campo de una página [!INCLUDE [prodshort](includes/prodshort.md)] agregada a una conversación de Teams. 

- Permisos de usuario:

    En su mayor parte, las páginas y los datos que los usuarios pueden ver y editar en una conversación de Teams están controlados por sus permisos en [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Para pegar un vínculo [!INCLUDE [prodshort](includes/prodshort.md)] en una conversación de Teams y hacer que se expanda en una tarjeta, los usuarios deben tener al menos permiso de lectura en la página y sus datos.
    - Una vez que se envía una tarjeta a una conversación, cualquier usuario de esa conversación puede ver esa tarjeta sin permiso de Business Central.
    - Para ver más detalles de una tarjeta o abrir el registro en [!INCLUDE [prodshort](includes/prodshort.md)], los usuarios deben tener permiso de lectura en la página y sus datos.
    - Para cambiar los datos, el usuario necesita modificar los permisos.
    
    Para obtener información sobre permisos, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="see-also"></a>Consulte también
[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introducción](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
