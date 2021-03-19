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
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 5fc5957695145ad3bbc4225c7c7e18dd7ca0c728
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386304"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Gestionar la integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo proporciona una descripción general de lo que puede hacer como administrador para controlar la integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>En Microsoft Teams

### <a name="minimum-requirements"></a>Requisitos mínimos

Esta sección describe los requisitos mínimos para que la características de la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] trabajen en Teams.

- Licencias requeridas

    Esta tabla le ofrece una descripción general de las licencias necesarias que la características de la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] trabajen en Teams.

    |Qué|Licencia de Teams|Licencia de [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|---|
    |Pegue un vínculo a un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación y envíelo como una tarjeta.|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|
    |Vea una tarjeta de un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación.|![marca de verificación](media/check.png "comprobar")||
    |Vea más detalles de la tarjeta de un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación.|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|

- Permitir vistas previas de URL

    La configuración de directiva **Permitir vistas previas de URL** debe estar activada. De lo contrario, no se puede generar una tarjeta para los vínculos de [!INCLUDE [prod_short](includes/prod_short.md)] pegados en una conversación de Teams. Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Gestionar la aplicación de [!INCLUDE [prod_short](includes/prod_short.md)] (opcional)

Como administrador de Teams, puede administrar todas las aplicaciones de su organización, incluida la aplicación [!INCLUDE [prod_short](includes/prod_short.md)]. Puede aprobar o instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para su organización, bloquear la instalación de la aplicación para el usuario y más.

Para obtener más información, consulte los siguientes productos de la documentación en Microsoft Teams:

- [Administre sus aplicaciones en el centro de administración de Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Administrar las directivas de configuración de la aplicación en Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>En [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Requisitos mínimos

- Versión de [!INCLUDE [prod_short](includes/prod_short.md)]:

    Lanzamiento de versiones 2 (actualización 17.3) de 2020 de [!INCLUDE [prod_short](includes/prod_short.md)], o posterior. La integración de Teams solo es compatible con [!INCLUDE [prod_short](includes/prod_short.md)] en línea; no en las instalaciones.

- Codeunit **Proveedor de resumen de página 2718** se publica como servicio web:

    Esta codeunit se publica como un servicio web de forma predeterminada. La codeunit es parte de la aplicación del sistema [!INCLUDE [prod_short](includes/prod_short.md)]. Se utiliza para obtener los datos de campo de una página [!INCLUDE [prod_short](includes/prod_short.md)] agregada a una conversación de Teams. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

- <a name="permissions"></a>Permisos de usuario:

    En su mayor parte, las páginas y los datos que los usuarios pueden ver y editar en una conversación de Teams están controlados por sus permisos en [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Para pegar un vínculo [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación de Teams y hacer que se expanda en una tarjeta, los usuarios deben tener al menos permiso de lectura en la página y sus datos.
    - Una vez que se envía una tarjeta a una conversación, cualquier usuario de esa conversación puede ver esa tarjeta sin permiso de [!INCLUDE [prod_short](includes/prod_short.md)].
    - Para ver más detalles de una tarjeta o abrir el registro en [!INCLUDE [prod_short](includes/prod_short.md)], los usuarios deben tener permiso de lectura en la página y sus datos.
    - Para cambiar los datos, el usuario necesita modificar los permisos.
    
    Para obtener información sobre permisos, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Gestionar la privacidad y el cumplimiento 

Microsoft Teams proporciona amplios controles para el cumplimiento y la gestión de datos confidenciales o de identificación personal&mdash;incluidos los datos agregados a los chats y canales por la aplicación [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="understanding-where-prod_short-cards-are-stored"></a>Saber dónde se almacenan las tarjetas de [!INCLUDE [prod_short](includes/prod_short.md)] 

Después de enviar una tarjeta a un chat, la tarjeta y los campos que se muestran en la tarjeta se copian en Teams. Esta información está sujeta a las políticas de Teams de su organización, como las políticas de retención de datos. Cuando se muestran los detalles de la tarjeta, ninguno de los datos de la ventana de detalles se almacena en Teams. Los datos permanecen almacenados en [!INCLUDE [prod_short](includes/prod_short.md)] y Teams solo lo recuperará cuando el usuario elija ver los detalles. 

- Para obtener más información sobre dónde almacena Teams esos datos, consulte [Ubicación de los datos en Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Para obtener más información sobre las políticas de retención en Teams, consulte [Políticas de retención en Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Restringir el intercambio de tarjetas 

Evita que usuarios o grupos específicos envíen tarjetas a chats o canales configurando políticas de mensajería que desactivan la configuración de **Vistas previas de URL**. Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams). 

También puede utilizar barreras de información para evitar que las personas o los grupos se comuniquen entre sí. Para obtener más información, consulte [Barreras de información en Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Las características de prevención de pérdida de datos del Centro de cumplimiento y seguridad de Microsoft 365 no se pueden aplicar específicamente a las tarjetas. Pero se pueden aplicar a los mensajes de chat que contienen las tarjetas. Para realizar un seguimiento de las próximas funciones avanzadas que incluyen la habilitación de DLP para tarjetas, consulte [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Responder a solicitudes de datos

Permite que los miembros del equipo y los propietarios del equipo eliminen mensajes que contienen tarjetas confidenciales configurando políticas de mensajería, como: **Los propietarios pueden eliminar los mensajes enviados** y **Los usuarios pueden eliminar los mensajes enviados**. Para obtener más información, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).

Las características de búsqueda de contenido y cumplimiento de eDiscovery del Centro de cumplimiento y seguridad de Microsoft 365 no se pueden aplicar específicamente a las tarjetas. Pero se pueden aplicar a los mensajes de chat que contienen las tarjetas. Para realizar un seguimiento de las próximas funciones de cumplimiento de las tarjetas, consulte [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Dado que los datos de la tarjeta en Teams son una copia de los datos en [!INCLUDE [prod_short](includes/prod_short.md)], también puede usar las características de [!INCLUDE [prod_short](includes/prod_short.md)] para exportar los datos de un cliente si se solicita. Para obtener más información sobre la privacidad en [!INCLUDE [prod_short](includes/prod_short.md)], vea [Preguntas frecuentes sobre privacidad para clientes de Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Consulte también
[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]