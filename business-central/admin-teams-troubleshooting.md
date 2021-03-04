---
title: Solución de problemas de integración de Microsoft Teams
description: Obtenga más información sobre lo que puede hacer como administrador para controlar la integración de Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046537"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Solución de problemas de integración de Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo proporciona información sobre cómo identificar y solucionar problemas que puede experimentar al usar Microsoft Teams con [!INCLUDE [prod_short](includes/prod_short.md)], como un usuario o administrador típico.

## <a name="none-of-my-links-expand-into-a-card"></a>Ninguno de mis enlaces se expande en una tarjeta 

Si tiene este problema, aquí hay algunas cosas que puede probar:

1. Primero, asegúrese de que la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams está instalada.

    Para comprobarlo, inicie sesión en la aplicación de escritorio de Teams o Teams en el navegador. Luego, en el lado izquierdo, seleccione **Aplicaciones** y busque **[!INCLUDE [prod_short](includes/prod_short.md)]**. Cuando encuentre la aplicación **[!INCLUDE [prod_short](includes/prod_short.md)]**, selecciónela para abrir la página de detalles de la aplicación. Si se muestra el botón **Agregar para mi**, la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] no está instalada. Para obtener más información sobre cómo instalar la aplicación, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Los usuarios invitados no pueden instalar aplicaciones de inmediato. Para obtener más información sobre los usuarios invitados, consulte nuestras preguntas frecuentes sobre la colaboración con invitados. 

2. A continuación, verifique que haya iniciado sesión con la identidad correcta.

    En Teams, vaya a cualquier chat y, en el cuadro de redacción del mensaje, elija el icono [!INCLUDE [prod_short](includes/prod_short.md)]. Cuando aparezca la ventana, verifique si el usuario al que dice que está conectado coincide con lo que usa para conectarse a [!INCLUDE [prod_short](includes/prod_short.md)].

3. Asegúrese de que la codeunit **Proveedor de resumen de página 2718** se publica como servicio web.

    Teams se conecta a [!INCLUDE [prod_short](includes/prod_short.md)] usando un punto final para esta codeunit en el servicio [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

4. Su organización también puede restringirle la posibilidad de pegar enlaces que se expanden en tarjetas. Póngase en contacto con su administrador para comprender las políticas organizativas de Teams que pueden aplicarse a usted.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mi enlace a veces no se expande en una tarjeta 

Un enlace no se expandirá a una tarjeta en las siguientes situaciones:

- El enlace apunta a una página de un tipo que no representa un registro. Por ejemplo, podría ser un enlace al área de trabajo de [!INCLUDE [prod_short](includes/prod_short.md)]. Puede verificar el tipo de página usando el panel de inspección de página en el cliente web en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la inspección de páginas, consulte [Inspección de páginas](across-inspect-page.md).
- El enlace apunta a una página que (a nivel técnico) no está conectada a una tabla de origen en formato [!INCLUDE [prod_short](includes/prod_short.md)]. Puede verificar si una página tiene una tabla de origen usando el panel de inspección de página en el cliente web en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la inspección de páginas, consulte [Inspección de páginas](across-inspect-page.md). 
- Teams no admite vistas previas de vínculos en algunas características. Por ejemplo, cuando aparece un chat, está en una reunión o es un invitado de otra organización.
- Teams abandona silenciosamente el intento de mostrar la tarjeta después de 15 segundos, por ejemplo, debido a problemas de red.
- Es posible que Teams no expanda el enlace si ya pegó un enlace en el mismo cuadro de redacción de mensajes y eliminó la tarjeta.

El enlace también debe contener toda la información necesaria para ubicar el registro y mostrar la tarjeta correspondiente. Esta informacion incluye:

- El nombre del entorno, incluyéndolo en la ruta de la URL. Si no especifica el nombre del entorno, Teams asume que está intentando llegar al entorno llamado "Producción".
- El nombre de la empresa, utilizando el parámetro *company=*
- El identificador de página, utilizando el parámetro *page =*
- El marcador del registro, utilizando el parámetro *bookmark=*

Por ejemplo:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Para obtener detalles técnicos sobre las URL de [!INCLUDE [prod_short](includes/prod_short.md)], consulte [URL del cliente web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) en la ayuda de [!INCLUDE [prod_short](includes/prod_short.md)] para desarrolladores y profesionales de TI.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>La tarjeta se muestra en el cuadro de redacción del mensaje, pero seleccionar el botón Detalles no hace nada 

Después de que un enlace se expande en una tarjeta en el cuadro de redacción del mensaje, debe enviar el mensaje al chat antes de poder usar el botón **Detalles**.

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

Los cambios que realice en un campo en las ventanas de detalles se guardan automáticamente cuando abandona el campo. Antes de cerrar la ventana después de cambiar un campo, asegúrese de presionar la tecla Tab o hacer clic / tocar fuera del campo.

## <a name="see-also"></a>Consulte también

[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]