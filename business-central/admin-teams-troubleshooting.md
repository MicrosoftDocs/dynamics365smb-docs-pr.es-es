---
title: Solución de problemas de integración de Microsoft Teams
description: Obtenga más información sobre lo que puede hacer como administrador para controlar la integración de Microsoft Teams.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 09/19/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="troubleshoot-microsoft-teams-integration-with-"></a>Solución de problemas de integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo proporciona información sobre cómo identificar y solucionar problemas que puede experimentar al usar Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)], como un usuario o administrador típico.

## <a name="the-sign-in-link-doesnt-work"></a>El vínculo de inicio de sesión no funciona

Si intenta iniciar sesión en la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams justo después de instalar la aplicación, y el vínculo de inicio de sesión no reacciona, puede deberse a que la aplicación no haya completado por completo la instalación. Para intentar solucionar el problema, cierre sesión en su cliente de Teams y vuelva a iniciar sesión.

## <a name="the-settings-page-is-empty"></a>La página Configuración está vacía

Primero debe iniciar sesión para acceder a su configuración. Para iniciar sesión en la aplicación, pegue un vínculo en un registro de [!INCLUDE [prod_short.md](includes/prod_short.md)] o intente buscar contactos. Ambas acciones le guiarán a través de una experiencia de registro, después de la cual podrá usar la página **Configuración**.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a>Cambié de empresa, pero no pareció funcionar

Después de cambiar de empresa en la página **Configuración**, es posible que observe que el menú desplegable del cuadro de comando indica que todavía sigue buscando en la empresa anterior. Este problema se produce al abrir la página **Configuración** directamente desde el cuadro de comando. En este caso, la empresa se cambió correctamente y, de hecho, buscará la empresa a la que se ha cambiado. El problema es que el menú desplegable del cuadro de comando aún no se ha actualizado. Para que el menú desplegable refleje con precisión la empresa en la que buscará, cierre o desancle [!INCLUDE [prod_short.md](includes/prod_short.md)] desde el cuadro de comando y, a continuación, abra de nuevo la aplicación. 


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a>Error "Algo salió mal" al buscar contactos

Puede experimentar este error cuando busca en una empresa que no se ha inicializado o que no responde. Por ejemplo, no puede buscar en una nueva empresa de prueba que aún no haya aceptado los términos de uso. Para resolver este problema, intente iniciar sesión en el cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)] y actúe en cuadro de diálogo inicial que aparezca o descártelo.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>Error "No se puede encontrar la API de contacto/resumen de contactos" al buscar contactos

Este problema puede deberse a personalizaciones o soluciones de la industria que afectan o modifican [!INCLUDE [prod_short.md](includes/prod_short.md)] o no proporcionan un contacto o una API de resumen de contactos. Si el problema continúa, póngase en contacto con su administrador o socio de soporte.

## <a name="none-of-my-links-expand-into-a-card"></a>Ninguno de mis enlaces se expande en una tarjeta

Si tiene este problema, aquí hay algunas cosas que puede probar:

1. Primero, asegúrese de que la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams está instalada.

    Para comprobarlo, inicie sesión en la aplicación de escritorio de Teams o Teams en el navegador. Luego, en el lado izquierdo, seleccione **Aplicaciones** y busque **[!INCLUDE [prod_short](includes/prod_short.md)]**. Cuando encuentre la aplicación **[!INCLUDE [prod_short](includes/prod_short.md)]**, selecciónela para abrir la página de detalles de la aplicación. Si se muestra el botón **Agregar**, la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] no está instalada. Para obtener más información sobre cómo instalar la aplicación, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Los usuarios invitados no pueden instalar aplicaciones de inmediato. Para obtener más información sobre los usuarios invitados, consulte nuestras [Preguntas frecuentes sobre la colaboración con invitados](teams-faq.md?tabs=collaborating#language). 

2. A continuación, verifique que haya iniciado sesión con la identidad correcta.

    En Teams, vaya a cualquier chat y, en el cuadro de redacción del mensaje, haga clic con el botón derecho en el icono [!INCLUDE [prod_short](includes/prod_short.md)] y, a continuación, elija **Configuración**. La ventana que aparece indica la cuenta de usuario con la que inició sesión. Verifique que sea la cuenta de usuario correcta.

3. Asegúrese de que la codeunit **Proveedor de resumen de página 2718** se publica como servicio web.

    Teams se conecta a [!INCLUDE [prod_short](includes/prod_short.md)] usando un punto final para esta codeunit en el servicio [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

4. Su organización también puede restringirle la posibilidad de pegar enlaces que se expanden en tarjetas. Póngase en contacto con su administrador para comprender las políticas organizativas de Teams que pueden aplicarse a usted.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mi enlace a veces no se expande en una tarjeta

Un enlace no se expandirá a una tarjeta en las siguientes situaciones:

- El enlace apunta a una página que (a nivel técnico) no está conectada a una tabla de origen en formato [!INCLUDE [prod_short](includes/prod_short.md)]. Puede verificar si una página tiene una tabla de origen usando el panel de inspección de página en el cliente web en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la inspección de páginas, consulte [Inspección de páginas](across-inspect-page.md).
- Teams no admite vistas previas de vínculos en algunas de sus características. Por ejemplo, cuando aparece un chat o es un invitado de otra organización.
- Los probemas de red hacen que Teams abandone silenciosamente el intento de mostrar la tarjeta después de 15 segundos, por ejemplo.
- Es posible que Teams no expanda el enlace si ya pegó un enlace en el mismo cuadro de redacción de mensajes y eliminó la tarjeta.

El enlace también debe contener toda la información necesaria para ubicar el registro y mostrar la tarjeta correspondiente. Esta informacion incluye:

- El nombre del entorno, incluyéndolo en la ruta de la URL. Si no especifica el nombre del entorno, Teams asume que está intentando llegar al entorno llamado "Producción".
- El nombre de la empresa, utilizando el parámetro *company=*
- El identificador de página, utilizando el parámetro *page =*
- El marcador del registro, utilizando el parámetro *bookmark=*

Por ejemplo:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Para obtener detalles técnicos sobre las URL de [!INCLUDE [prod_short](includes/prod_short.md)], consulte [URL del cliente web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) en la ayuda de [!INCLUDE [prod_short](includes/prod_short.md)] para desarrolladores y profesionales de TI.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Se abre la ventana de detalles, pero muestra un error antes de que se muestren los detalles

Este problema puede deberse a un par de cosas: falta de permisos en [!INCLUDE [prod_short](includes/prod_short.md)] o la configuración del navegador (cuando se usa Teams en el navegador).

1. Verifique sus permisos en [!INCLUDE [prod_short](includes/prod_short.md)].

    Para ver los detalles de una tarjeta, [!INCLUDE [prod_short](includes/prod_short.md)] comprueba su licencia y permisos para ver ese registro y página específicos en la empresa y el entorno específicos. Si no está autorizado para ninguna de estas cosas, en la ventana de detalles aparecen mensajes de error estándar de [!INCLUDE [prod_short](includes/prod_short.md)] sobre permisos. 

    Para obtener más información sobre los permisos, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

2. Verifique la configuración de su navegador si usa Teams en el navegador.

    - El bloqueador de ventanas emergentes de su navegador debe estar desactivado o configurado para permitir ventanas emergentes en los dominios *businesscentral.dynamics.com* o *bc.dynamics.com*. Para obtener información sobre cómo permitir ventanas emergentes de [!INCLUDE [prod_short](includes/prod_short.md)], vea [Configuración de su navegador](across-browser-settings.md#popup).
    - Su navegador debe tener acceso al almacenamiento local del navegador para cookies y preferencias mientras trabaja.
    - Evite el uso de la navegación privada o de invitados a menos que sea necesario, ya que descartan o bloquean cierto contenido en algunos navegadores.

    Para obtener más información sobre los requisitos mínimos del navegador, consulte [Requisitos mínimos de uso de [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Tengo problemas con la cámara o la ubicación en Teams

Cuando usa características de [!INCLUDE [prod_short](includes/prod_short.md)] en la ventana de detalles que requieren acceso a su ubicación o cámara del dispositivo, primero debe dar su consentimiento para que Teams acceda a estas capacidades del dispositivo.  

- Para Teams en el navegador, asegúrese de que la configuración de su navegador permita el acceso a la cámara y la ubicación para https://teams.microsoft.com. 

- Para Teams para iOS o Android, asegúrese de que la configuración de su dispositivo permita el acceso a la cámara y la ubicación para la aplicación móvil Teams. 

Para obtener ayuda sobre cómo cambiar esta configuración, consulte [Mi cámara no funciona en Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) en Soporte de Microsoft.

La aplicación [!INCLUDE [prod_short](includes/prod_short.md)] no admite la ubicación en la aplicación de escritorio de Teams. Para obtener más información sobre la ubicación, consulte [Preguntas frecuentes de Teams](teams-faq.md#location).

Algunos navegadores, como el nuevo Microsoft Edge, le permite elegir qué cámara del dispositivo usar cuando su dispositivo admite varias cámaras. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams muestra varios idiomas para mis tarjetas y detalles de tarjetas

Para que las tarjetas y los detalles de las tarjetas se muestren de manera coherente en el mismo idioma en Teams, el idioma de su cliente de Teams y el idioma que usa en el cliente web de [!INCLUDE [prod_short](includes/prod_short.md)] deben coincidir.

- Para obtener información sobre cómo cambiar el idioma en Teams, consulte [Cambiar la configuración en Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) en Soporte de Microsoft. 

- Para aprender a cambiar el idioma en [!INCLUDE [prod_short](includes/prod_short.md)], vea [Cambiar la configuración básica: idioma](ui-change-basic-settings.md#language).

Para obtener más información sobre cómo funcionan los idiomas entre Teams y [!INCLUDE [prod_short](includes/prod_short.md)], vea [Preguntas frecuentes de Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Edité un campo en la ventana de detalles, pero mi cambio no se guardó

Los cambios que realice en un campo en las ventanas de detalles se guardan automáticamente cuando abandona el campo. Antes de cerrar la ventana después de cambiar un campo, asegúrese de seleccionar la tecla <kbd>Tab</kbd> o hacer clic / tocar fuera del campo.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Apareció un nuevo mosaico en el Iniciador de aplicaciones. ¿Cómo puedo eliminarlo?

Cuando ve sus aplicaciones en la página Web de Office 365 (https://home.office.com) o en el iniciador de aplicaciones, aparecerá un nuevo mosaico llamado "Conector del servicio de integración de equipos de Business Central" después de instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams. Este mosaico no proporciona ningún valor en sí mismo y se puede ocultar de forma segura.

Como administrador, quién tiene permisos de administrador de Microsoft Entra, puede ocultar el mosaico siguiendo estos pasos:

1. Inicie sesión en el [centro de administración de Microsoft Entra](https://entra.microsoft.com/).
2. Seleccione **Aplicaciones empresariales**, luego seleccione **Conector del servicio de integración de equipos de Business Central Teams**.
3. Seleccione **Propiedades** y luego configure el conmutador **Visible para los usuarios** en **No**.
4. Seleccione **Guardar**.

> [!NOTE]
> Pasará un tiempo antes de que este cambio entre en vigor.

## <a name="duplicate-text-in-the-share-to-teams-window"></a>Texto duplicado en la ventana Compartir con Teams

Cuando pega texto en el cuadro de mensaje en la ventana **Compartir con Teams**, el texto se duplica. Microsoft conoce este problema y se solucionará en una actualización posterior. 

## <a name="unable-to-sign-in-to-the-share-to-teams-window"></a>No se puede iniciar sesión en la ventana Compartir con Teams

Este problema puede deberse a varias razones. Por ejemplo, la identidad que está utilizando para iniciar sesión debe tener acceso a Microsoft Teams, como a través de una suscripción a Microsoft 365.

## <a name="my-cards-no-longer-have-a-popout-button"></a>Mis tarjetas ya no tienen un botón emergente

A partir de abril de 2022, los vínculos que se muestran como tarjeta compacta en Teams ya no contendrán el botón **emergente**. Para abrir esa tarjeta en su propia ventana, elija el botón **Detalles** y luego **Abrir en navegador** del menú de puntos suspensivos (**...**) en la esquina superior derecha de la ventana.

## <a name="cant-pin-a-card-to-tab"></a>No se puede anclar una tarjeta a la pestaña

Existen dos motivos para este problema.

- Si la tarjeta se compartió desde Search ME, entonces no se puede anclar a una pestaña. 

- No se puede anclar hasta que agregue su primera pestaña de Business Central. Este problema se conoce en Teams. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Alguien agregó una pestaña, pero no me aparece la pestaña

Este problema se debe a que no tiene instalada la aplicación BC para Teams. Solo aquellos que tengan la aplicación instalada verán las pestañas de Business Central.

## <a name="others-see-a-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Otros ven una ordenación o disposición de columnas diferente a la que ve el autor de la pestaña

Es probable que este problema se deba a que compartió una vista de lista que es una vista personal. En este caso, trabaje con su administrador para crear vistas de lista específicas de roles que cubran los diferentes roles en el canal/chat, o cree esta vista para toda la organización para que todos puedan obtener una vista uniforme.


## <a name="related-information"></a>Consulte también .

[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Búsqueda de clientes, proveedores y otros contactos desde Microsoft Teams](across-search-contacts-teams.md)  
[Compartir registros en Microsoft Teams](across-working-with-teams.md)  
[P+F de Teams](teams-faq.md)  
[Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
