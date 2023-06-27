---
title: Administrar la integración de Microsoft Teams con Business Central | Microsoft Docs
description: Administrar la integración de Business Central con Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics365-business-central
---

# <a name="managing-microsoft-teams-integration-with-"></a><a name="managing-microsoft-teams-integration-with-"></a>Gestionar la integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo proporciona una descripción general de lo que puede hacer como administrador para controlar la integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a><a name="in-microsoft-teams"></a>En Microsoft Teams

### <a name="minimum-requirements"></a><a name="minimum-requirements"></a>Requisitos mínimos

Esta sección describe los requisitos mínimos para que la características de la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] trabajen en Teams.

- Licencias requeridas

    La aplicación [!INCLUDE[prod_short](includes/prod_short.md)] necesita una licencia de Teams a través de una suscripción empresarial o de negocios de Microsoft 365. No se admiten suscripciones de Teams independientes como Microsoft Teams (gratuitas) o Microsoft Teams Essentials.

    La mayoría de las características de la aplicación [!INCLUDE[prod_short](includes/prod_short.md)] para Teams también requiere una licencia [!INCLUDE [prod_short](includes/prod_short.md)], como se muestra en la siguiente tabla.

    |Qué|Licencia de [!INCLUDE [prod_short](includes/prod_short.md)]|
    |----|---|
    |Buscar contactos de [!INCLUDE [prod_short](includes/prod_short.md)].|![marca de verificación](media/check.png "comprobar")|
    |Pegue un vínculo a un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación y envíelo como una tarjeta.|![marca de verificación](media/check.png "comprobar")|
    |Comparta un enlace de una página en [!INCLUDE [prod_short](includes/prod_short.md)] con una conversación de Teams.|![marca de verificación](media/check.png "comprobar")|
    |Vea una tarjeta de un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación.||
    |Vea más detalles de la tarjeta de un registro de [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación.|![marca de verificación](media/check.png "comprobar")|
    |Abra un enlace de página en [!INCLUDE [prod_short](includes/prod_short.md)] desde una conversación.|![marca de verificación](media/check.png "comprobar")|

- Permitir vistas previas de URL

    La configuración de directiva **Permitir vistas previas de URL** debe estar activada. De lo contrario, no se puede generar una tarjeta para los vínculos de [!INCLUDE [prod_short](includes/prod_short.md)] pegados en una conversación de Teams. Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the--app-optional"></a><a name="managing-the--app-optional"></a>Gestionar la aplicación de [!INCLUDE [prod_short](includes/prod_short.md)] (opcional)

Como administrador de Teams, puede administrar todas las aplicaciones de su organización, incluida la aplicación [!INCLUDE [prod_short](includes/prod_short.md)]. Puede aprobar o instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para su organización, bloquear la instalación de la aplicación para el usuario y más.

Para obtener más información, consulte los siguientes productos de la documentación en Microsoft Teams:

- [Administre sus aplicaciones en el centro de administración de Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Administrar las directivas de configuración de la aplicación en Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-"></a><a name="in-"></a>En [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements-1"></a><a name="minimum-requirements-1"></a>Requisitos mínimos

- Versión de [!INCLUDE [prod_short](includes/prod_short.md)]:

    Lanzamiento de versiones 1 de 2021 de [!INCLUDE [prod_short](includes/prod_short.md)] o posterior. La integración de Teams solo es compatible con [!INCLUDE [prod_short](includes/prod_short.md)] en línea; no en las instalaciones.

- Codeunit **Proveedor de resumen de página 2718** se publica como servicio web:

    Esta codeunit se publica como un servicio web de forma predeterminada. La codeunit es parte de la aplicación del sistema [!INCLUDE [prod_short](includes/prod_short.md)]. Se utiliza para obtener los datos de campo de una página [!INCLUDE [prod_short](includes/prod_short.md)] agregada a una conversación de Teams. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

- <a name="permissions"></a>Permisos de usuario:

    En su mayor parte, la búsqueda de contactos, las páginas y los datos que los usuarios pueden ver y editar en una conversación de Teams están controlados por sus permisos en [!INCLUDE [prod_short](includes/prod_short.md)].

    - Para buscar contactos, los usuarios deben tener al menos permiso de lectura para la tabla **Contactos**. 
    - Para pegar un vínculo [!INCLUDE [prod_short](includes/prod_short.md)] en una conversación de Teams y hacer que se expanda en una tarjeta, los usuarios deben tener al menos permiso de lectura en la página y sus datos.
    - Una vez que se envía una tarjeta a una conversación, cualquier usuario de esa conversación puede ver esa tarjeta sin permiso de [!INCLUDE [prod_short](includes/prod_short.md)].
    - Para ver más detalles de una tarjeta o abrir el registro en [!INCLUDE [prod_short](includes/prod_short.md)], los usuarios deben tener permiso de lectura en la página y sus datos.
    - Para cambiar los datos, el usuario necesita modificar los permisos.
    
    Para obtener información sobre permisos, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a><a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Instalación de la aplicación Business Central mediante Implementación centralizada

El centro de administración de Microsoft Teams es donde se configuran las políticas de configuración de aplicaciones de Teams para la organización. En el centro de administración de Teams, puede usar la función Implementación centralizada para instalar automáticamente la aplicación Business Central en Teams para todos los usuarios de su organización, grupos específicos o usuarios individuales.

> [!NOTE]
> Para configurar Implementación centralizada, su cuenta de Teams debe tener el rol **Administrador de servicio de Teams** o el rol **Administrador global**.

1. En Business Central, seleccione el icono ![Lupa que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entre en **Implementación centralizada de la aplicación Teams**, y luego elija el enlace relacionado. O seleccione [aquí](https://businesscentral.dynamics.com/?page=1833) para abrir la página directamente.
2. Lea la información en **Configurar la aplicación Business Central para Teams**, y luego **Siguiente** cuando esté listo.
3. Abre el [Centro de administración de Teams](https://go.microsoft.com/fwlink/?linkid=2163970) y complete los siguientes pasos.
    1. Vaya a **Aplicaciones de Teams** > **Directivas de configuración**.
    2. Cree una nueva directiva o seleccione la directiva que desea usar para instalar la aplicación Business Central, luego seleccione **Agregar aplicaciones**.
    3. En la página **Agregar aplicaciones instaladas**, busque y seleccione **Business Central**.
    4. Elija **Agregar**.

       Business Central debería aparecer ahora bajo **Aplicaciones instaladas** para la directiva.
    5. Configure ajustes adicionales según necesite y, a continuación, elija **Guardar**.

    Para obtener más información sobre las directivas de configuración en Teams, consulte [Administrar directivas de configuración de aplicaciones en Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) en la documentación de Teams.
4. Vuelva a **Implementación centralizada de aplicaciones de Teams** en Business Central y seleccione **Listo**.

> [!IMPORTANT]
> La directiva de configuración de aplicaciones y la implementación de la aplicación para los usuarios pueden tardar hasta 24 horas.

## <a name="managing-privacy-and-compliance"></a><a name="managing-privacy-and-compliance"></a>Gestionar la privacidad y el cumplimiento

Microsoft Teams proporciona amplios controles para el cumplimiento y la gestión de datos confidenciales o de identificación personal&mdash;incluidos los datos agregados a los chats y canales por la aplicación [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="understanding-where--cards-are-stored"></a><a name="understanding-where--cards-are-stored"></a>Saber dónde se almacenan las tarjetas de [!INCLUDE [prod_short](includes/prod_short.md)]

Después de enviar una tarjeta a un chat, la tarjeta y los campos que se muestran en la tarjeta se copian en Teams. Esta información está sujeta a las políticas de Teams de su organización, como las políticas de retención de datos. Cuando se muestran los detalles de la tarjeta, ninguno de los datos de la ventana de detalles se almacena en Teams. Los datos permanecen almacenados en [!INCLUDE [prod_short](includes/prod_short.md)] y Teams solo lo recuperará cuando el usuario elija ver los detalles. 

- Para obtener más información sobre dónde almacena Teams esos datos, consulte [Ubicación de los datos en Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Para obtener más información sobre las políticas de retención en Teams, consulte [Políticas de retención en Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a><a name="restricting-sharing-of-cards"></a>Restringir el intercambio de tarjetas

Evita que usuarios o grupos específicos envíen tarjetas a chats o canales configurando políticas de mensajería que desactivan la configuración de **Vistas previas de URL**. Para obtener más información sobre esta configuración, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams). 

También puede utilizar barreras de información para evitar que las personas o los grupos se comuniquen entre sí. Para obtener más información, consulte [Barreras de información en Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Las características de prevención de pérdida de datos del Centro de cumplimiento y seguridad de Microsoft 365 no se pueden aplicar específicamente a las tarjetas. Pero se pueden aplicar a los mensajes de chat que contienen las tarjetas. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a><a name="responding-to-data-requests"></a>Responder a solicitudes de datos

Permite que los miembros del equipo y los propietarios del equipo eliminen mensajes que contienen tarjetas confidenciales configurando políticas de mensajería, como: **Los propietarios pueden eliminar los mensajes enviados** y **Los usuarios pueden eliminar los mensajes enviados**. Para obtener más información, consulte [Administrar directivas de mensajería en Teams](/microsoftteams/messaging-policies-in-teams).

Las características de búsqueda de contenido y cumplimiento de eDiscovery del Centro de cumplimiento y seguridad de Microsoft 365 no se pueden aplicar también a las tarjetas.

Dado que los datos de la tarjeta en Teams son una copia de los datos en [!INCLUDE [prod_short](includes/prod_short.md)], también puede usar las características de [!INCLUDE [prod_short](includes/prod_short.md)] para exportar los datos de un cliente si se solicita. Para obtener más información sobre la privacidad en [!INCLUDE [prod_short](includes/prod_short.md)], vea [Preguntas frecuentes sobre privacidad para clientes de Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="show-or-hide-record-data-on-cards"></a><a name="show-or-hide-record-data-on-cards"></a>Mostrar u ocultar datos de registro en tarjetas

Cuando se comparte un registro con otras personas en un chat o canal de Teams, se muestra una tarjeta con campos que contienen datos sobre el registro. Todos los destinatarios pueden ver estos datos (o resumen de registros) de forma predeterminada, independientemente de su licencia o permisos en Business Central. Si es administrador, puede usar la guía de configuración asistida **Configuración de la tarjeta** para ocultar el resumen del registro, para que no aparezca en las tarjetas en Teams. Ocultar el resumen del registro elimina todos los campos e imágenes, pero sigue mostrando el botón **Detalles** y otra información que no pertenece al registro en la tarjeta.

|Resumen de registro activado|Resumen de registro desactivado|
|-|-|
|![Imagen que muestra una tarjeta en Teams cuando el resumen de registros está activado.](media/card-settings-example-on.png)|![Imagen que muestra una tarjeta en Teams cuando el resumen de registros está desactivado.](media/card-settings-example-off.png)|

Usted configura la configuración por entorno. Por lo tanto, cuando active o desactive el resumen de registros, afectará a todas las empresas del entorno.

1. En Business Central, abra el entorno que desea modificar.

   > [!TIP]
   > Para cambiar el entorno, seleccione <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Elija el icono ![Lupa que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de tarjeta** y luego elija el vínculo relacionado. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Lea la información de **Configuración de tarjeta** y luego seleccione **Siguiente** cuando esté listo.
4. En la página **Visibilidad de datos**, active el conmutador **Mostrar resumen de registro** para mostrar los datos de las tarjetas o desactive para ocultar los datos.
5. Seleccione **Siguiente** y siga las instrucciones para completar la guía de configuración.

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
