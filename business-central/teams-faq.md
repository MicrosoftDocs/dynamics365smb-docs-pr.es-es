---
title: P+F de Teams
description: Obtenga respuestas a algunas preguntas típicas sobre cómo trabajar con Teams y Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 03/04/2021
ms.author: jswymer
ms.openlocfilehash: d95e97a232cfb7fda8f40f68875b747723abbd4b
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573381"
---
# <a name="teams-faq"></a>P+F de Teams

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo responde algunas de las preguntas que pueda tener sobre cómo trabajar con Teams y [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[General](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>¿Cómo inicio sesión en la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] en Teams? 

Después de instalar la aplicación, se le pedirá que inicie sesión la primera vez que pegue un vínculo a [!INCLUDE [prod_short.md](includes/prod_short.md)] en el chat de Teams o cuando elija la acción **Detalles** en una tarjeta en Teams. Dependiendo de su cliente de Teams, es posible que deba ingresar las credenciales que usa para acceder a [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>¿Cómo inicio sesión fuera de la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] en Teams? 

Para cerrar sesión en su identidad de usuario actual en Teams usada para conectar con [!INCLUDE [prod_short.md](includes/prod_short.md)], vaya a cualquier cuadro de redacción de chat y elija el icono [!INCLUDE [prod_short.md](includes/prod_short.md)] debajo. Cuando aparezca la ventana, verifique su identidad actualmente conectada y luego elija **Desconectar**. Si usa Teams en el navegador, también cerrará sesión en cualquier cliente web [!INCLUDE [prod_short.md](includes/prod_short.md)] en la misma ventana del navegador.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>¿Se conecta la aplicación para Teams a [!INCLUDE [prod_short.md](includes/prod_short.md)] en las instalaciones? 

Nº La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams solo funciona con [!INCLUDE [prod_short.md](includes/prod_short.md)] en línea. No hay planes para apoyar tipos de implementación de [!INCLUDE [prod_short.md](includes/prod_short.md)]&mdash;como en las instalaciones, nube híbrida o nube privada&mdash;que Microsoft no aloja ni administra directamente.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>¿La aplicación funciona con múltiples empresas y entornos? 

Sí. Cuando la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] expande un enlace en una tarjeta, el enlace debe contener el entorno y los nombres de la empresa para que la aplicación coincida con el registro de la empresa correcta. Puede pegar enlaces a cualquier empresa y entorno al que tenga acceso dentro de su organización y desde la cuenta de [!INCLUDE [prod_short.md](includes/prod_short.md)] que utilizó para iniciar sesión. Los participantes en el chat verán la tarjeta. Pero no pueden ver los detalles de la tarjeta a menos que tengan permisos para la empresa o el entorno donde se almacena ese registro.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>¿En qué países o regiones está la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] disponible? 

La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams no está restringida por país o región. La aplicación está disponible en todos los mercados actualmente admitidos por el mercado de Teams. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>¿La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] funciona con cualquier localización de [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Sí. La aplicación está diseñada para funcionar con cualquier localización de [!INCLUDE [prod_short.md](includes/prod_short.md)], ya sea que la localización se ofrezca directamente desde Microsoft oa través de un socio. Para más información, vea [Disponibilidad nacional y regional e idiomas compatibles](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>¿Qué idiomas admite la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Dos cosas determinan el idioma que se usa para las tarjetas y los detalles de las tarjetas en Teams:

1. Su idioma en Teams, que puede ver en la configuración de su cuenta en Teams. 
2. Su idioma en [!INCLUDE [prod_short.md](includes/prod_short.md)], que puede ver en el cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)] (vea [Cambiar la configuración básica: idioma](ui-change-basic-settings.md#language)).

La siguiente tabla explica en qué se diferencia la experiencia de los autores y destinatarios de mensajes, según la configuración de idioma y la disponibilidad de idiomas.

|Quién|Ficha|Detalles de tarjeta |
|-|----|--------------| 
|Autor del mensaje |Se muestra en el idioma especificado para usted en Teams. Si [!INCLUDE [prod_short.md](includes/prod_short.md)] no ofrece el mismo idioma, la tarjeta se muestra en inglés. |Se muestra en el idioma especificado para usted en [!INCLUDE [prod_short.md](includes/prod_short.md)].  que puede incluir idiomas de aplicaciones de idiomas proporcionadas por socios. |
|Destinatario del mensaje |Se muestra en el idioma del autor del mensaje. |Se muestra en el idioma especificado para usted en [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Para ver la lista de idiomas admitidos para [!INCLUDE [prod_short.md](includes/prod_short.md)], vea [Idiomas admitidos](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the-business-central-app-work-with-industry-solutions"></a>¿La aplicación Business Central funciona con soluciones del sector?

Sí. La aplicación funciona con enlaces basados en el patrón **\*.bc.dynamics.com** que se usa típicamente con [Insertar aplicaciones](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview).

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>¿Dónde puedo encontrar la integración de Teams dentro del cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Actualmente no hay incrustación de controles de Teams o presencia de características de Teams dentro del cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)] u otros clientes.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>¿Funciona [!INCLUDE [prod_short.md](includes/prod_short.md)] con la aplicación móvil de Teams?

Sí. La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] se puede instalar desde la aplicación de escritorio o el navegador de Teams, o por un administrador para todos los usuarios. Una vez instalada, la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] está disponible automáticamente en Teams para iOS y Android. En dispositivos móviles, puede ver tarjetas enviadas por otros, acceder a detalles o mostrar la tarjeta para obtener la experiencia completa en la aplicación móvil [!INCLUDE [prod_short.md](includes/prod_short.md)]. Sin embargo, no puede pegar enlaces que se expanden en tarjetas al redactar mensajes. Para conocer los requisitos mínimos para dispositivos móviles, consulte [Requisitos mínimos para utilizar Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>¿Es la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams igual que la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para iOS y Android?

Nº La aplicación para Teams es un complemento de Microsoft Teams y diseñado exclusivamente para experiencias colaborativas que se iluminan dentro de Teams. Por otro lado, la aplicación móvil [!INCLUDE [prod_short.md](includes/prod_short.md)] ofrece una rica experiencia con la que trabajar con datos de [!INCLUDE [prod_short.md](includes/prod_short.md)] en sus dispositivos móviles.

Se anima a los usuarios móviles a instalar tanto la aplicación móvil como la aplicación para que Teams aproveche al máximo [!INCLUDE [prod_short.md](includes/prod_short.md)]. Con ambos instalados, puede elegir la acción **Salir** en una tarjeta en Teams para abrir los detalles de la tarjeta en la aplicación móvil [!INCLUDE [prod_short.md](includes/prod_short.md)]. Para obtener información sobre la instalación de las aplicaciones móviles de [!INCLUDE [prod_short.md](includes/prod_short.md)] y Teams, consulte:

- [Obtener Business Central en el dispositivo móvil](install-mobile-app.md)
- [Obtener la aplicación móvil de Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) en Soporte de Microsoft

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>¿La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] funciona en todos los clientes de Teams?

Nº La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams no es compatible cuando se instala como un paquete para macOS o Linux. En estas plataformas, puede acceder a Teams utilizando un navegador compatible.

Para conocer los requisitos mínimos en [!INCLUDE [prod_short.md](includes/prod_short.md)], vea [Requisitos mínimos para utilizar Business Central](product-requirements.md#teams).

Para obtener información sobre la elección de los clientes de Teams y cómo instalarlos, consulte [Obtener clientes para Microsoft Teams](/microsoftteams/get-clients) en la documentación de Teams.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>¿Para qué cliente de Teams es mejor [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Solo hay pequeñas diferencias y limitaciones entre los clientes de Teams que pueden afectar su experiencia con la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams. Al elegir un cliente de Teams, tenga en cuenta:

- No se puede acceder a la cámara y la ubicación desde la ventana de detalles en la aplicación de escritorio de Teams 
- Utilizando Microsoft Edge con Teams en el navegador le permite trabajar fácilmente con múltiples identidades y cuentas al iniciar sesión en Teams desde diferentes perfiles. Para aprender a usar perfiles en Microsoft Edge, vea [Iniciar sesión y crear múltiples perfiles en Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) en Soporte de Microsoft.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>¿Cuál es la mejor manera para mí de demostrar [!INCLUDE [prod_short.md](includes/prod_short.md)] y Microsoft Teams a los posibles clientes?

Si es un socio revendedor, es posible que desee tener un entorno que pueda mostrar a los clientes potenciales como parte de las demostraciones previas a la venta. Para evitar afectar a Microsoft Teams en su organización, puede obtener una cuenta de demostración de Microsoft 365 en [https://aka.ms/CDX](https://aka.ms/CDX). Esta cuenta le brinda el control total de una organización independiente de Azure que incluye Microsoft Teams y [!INCLUDE [prod_short.md](includes/prod_short.md)]. Para obtener más información, consulte [Preparación de entornos de demostración de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>¿La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams se adapta a mi personalización y personalización?

La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams puede mostrar tarjetas para enlaces a páginas y tablas de clientes en [!INCLUDE [prod_short.md](includes/prod_short.md)], como las páginas y tablas que se originan en sus propias extensiones personalizadas o en AppSource.

Los campos que se muestran en una tarjeta en Teams también pueden verse afectados por las personalizaciones de [!INCLUDE [prod_short.md](includes/prod_short.md)] instaladas para su organización. Las tarjetas no tienen en cuenta las personalizaciones específicas de la función o la personalización del usuario. Sin embargo, la ventana de detalles de la tarjeta muestra los detalles del registro como los vería en [!INCLUDE [prod_short.md](includes/prod_short.md)], incluidas las extensiones, personalizaciones de funciones y personalización de usuarios.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>¿Cómo afectan a mi privacidad los permisos requeridos por la aplicación?

Antes de instalar la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams, puede revisar los permisos mínimos requeridos para que la aplicación funcione. Al instalar la aplicación, acepta que la aplicación tiene permiso para recibir mensajes y datos que usted le proporciona, y Teams tiene permiso para almacenar y procesar esos mensajes.

Además, algunas características de [!INCLUDE [prod_short.md](includes/prod_short.md)] requieren la apertura de enlaces externos o el acceso a su cámara o ubicación geográfica. Por ejemplo, suponga que desea capturar una foto de una factura de compra para procesarla. La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] no usa estas capacidades sin su consentimiento y solo las usan funciones específicas en la ventana **Detalles**. Cuando use una de estas características por primera vez, Teams mostrará un cuadro de diálogo que le pedirá que otorgue acceso a las capacidades requeridas del dispositivo.

- En el escritorio de Teams, revise y ajuste los permisos de la aplicación desde la ventana **Ajustes**. Seleccione su foto de perfil en la parte superior de la aplicación, seleccione **Configuración** > **Permisos**, y luego seleccione la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)].

- Para Teams en el navegador y Teams para iOS o Android, puede revisar o ajustar los permisos desde la configuración de su navegador o dispositivo.

> [!NOTE]
> Exactamente qué características de [!INCLUDE [prod_short.md](includes/prod_short.md)] le solicitan permisos depende de las aplicaciones complementarias y las personalizaciones aplicadas al ambiente [!INCLUDE [prod_short.md](includes/prod_short.md)] al que se conecta.

### <a name="where-can-i-learn-about-my-privacy"></a>¿Dónde puedo obtener información sobre mi privacidad? 

Puede obtener información sobre cómo Microsoft maneja sus datos en la [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Comuníquese con su administrador para conocer cómo su organización maneja la privacidad de sus datos.

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>¿Cómo desinstalo la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams?

Para eliminar la aplicación que instaló usted mismo, vaya a cualquier cuadro de redacción de chat, busque el icono [!INCLUDE [prod_short.md](includes/prod_short.md)] debajo, haga clic con el botón derecho en el icono y seleccione Desinstalar.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>¿Seguirá Microsoft mejorando la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams?

En Microsoft, escuchamos constantemente los comentarios de nuestra diversa comunidad de usuarios y actuamos siguiendo las mejores sugerencias. Para conocer lo que sigue para la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams, consulte [Plan de lanzamiento de Dynamics 365](https://aka.ms/dynamics365releaseplan).

Si desea participar en la mejora de la aplicación para Teams, o tiene una gran idea que ayudaría a simplificar su trabajo o experiencias colaborativas en Teams, agregue una idea o vote por ideas existentes en [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="working-with-cards"></a>[Trabajando con tarjetas](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>¿Qué tipos de enlaces admite la aplicación?

La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams reacciona a la mayoría de los vínculos de clientes web [!INCLUDE [prod_short.md](includes/prod_short.md)]. Cuando el enlace se refiere a un solo registro en una página, la tarjeta mostrará campos para ese registro. Los tipos de página admitidos incluyen: 

- Páginas de tarjeta, como la tarjeta de artículo
- Páginas de documento, como el documento de orden de venta
- Páginas de ListPlus que representan un solo registro compuesto por otros registros, como un estado de conciliación de cuenta bancaria
- Páginas de listas simples en las que un registro no ofrece la posibilidad de profundizar en una página de detalles separada, como la lista de códigos postales

Al pegar un enlace a la URL del cliente web raíz, como https://businesscentral.dynamics.com, la tarjeta muestra información para ayudar a los nuevos usuarios a comenzar a acceder a [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>¿Cómo elimino una tarjeta que envié a un chat? 

No puede eliminar una tarjeta que ya envió al chat. Pero puede eliminar todo el mensaje del que forma parte la tarjeta.

Como autor del mensaje, puede eliminar los mensajes que envió a los chats con una persona, grupo o canal&mdash;a menos que su administrador haya configurado políticas que impidan eliminar mensajes. Si modera un canal como propietario del canal, es posible que su administrador también le haya otorgado permiso para eliminar cualquier mensaje en el canal, incluidos los mensajes enviados por otros usuarios.

Eliminar un mensaje que contiene una tarjeta no elimina ni afecta ningún dato en [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="do-cards-always-show-up-to-date-information"></a>¿Las tarjetas siempre muestran información actualizada?

Nº Los valores de campo de una tarjeta en Teams, incluidas las imágenes, se basan en los datos disponibles cuando esa tarjeta se envió al chat. Las tarjetas de [!INCLUDE [prod_short.md](includes/prod_short.md)] no se actualizan automáticamente en Teams. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>¿Verán otros mi tarjeta si no tienen la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams? 

Cuando redacta y envía un mensaje al chat que incluye una tarjeta, todos los usuarios verán la tarjeta, incluso si no han instalado la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>¿Cómo puedo saber a qué empresa pertenece una tarjeta en Teams?

Si trabaja en empresas de [!INCLUDE [prod_short.md](includes/prod_short.md)], hable con su administrador sobre la habilitación de un distintivo de empresa para cada empresa. Cuando está habilitada, esta sugerencia llamativa aparece en cualquier ventana de detalles en Teams y muestra la empresa y el ambiente al que pertenece el registro. Para saber cómo configurar el distintivo de la empresa, consulte [Para mostrar un distintivo de la empresa para acceder rápidamente a la información de la empresa](ui-change-basic-settings.md#badge).

## <a name="working-with-card-details"></a>[Trabajar con detalles de tarjetas](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>¿Dónde está el botón guardar en la ventana de detalles en Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] guarda automáticamente los cambios que realiza en cualquier campo tan pronto como abandona el campo. Para salir de un campo, haga clic / toque en cualquier lugar fuera del campo o use la tecla Tab para pasar al siguiente campo. Cuando aparecen datos en un cuadro de diálogo dentro de la ventana de detalles, es posible que deba elegir el botón **Aceptar** para que [!INCLUDE [prod_short.md](includes/prod_short.md)] guarde sus cambios.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Si elijo ver los detalles de una tarjeta, ¿otros usuarios verán mi ventana de detalles?

Nº Si bien todos en el chat pueden ver la tarjeta en sí, la ventana de detalles solo aparece para usted en su dispositivo cuando elige **Detalles**. Otros usuarios deben elegir **Detalles** si desean ver la ventana de detalles en su dispositivo.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>¿Puedo iniciar una llamada de Teams desde la ventana de detalles en Teams?

Sí. Puede iniciar una llamada eligiendo el número de marcación vinculado en un campo de número de teléfono, como el campo **Número de teléfono móvil** en la tarjeta de **Contacto**. Teams debe ser su aplicación de marcación designada.

Para llamar a teléfonos fijos y móviles locales o internacionales desde Teams, debe tener una licencia de Teams para llamadas empresariales. Además, debe configurar Teams como su solución de llamadas. Para obtener más información, consulte [Planificar la solución de voz de Teams](/microsoftteams/cloud-voice-landing-page) en la documentación de Teams.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>¿Puedo imprimir documentos desde la ventana de detalles en Teams?

Sí. Imprime informes y otros documentos utilizando la funcionalidad de impresión de [!INCLUDE [prod_short.md](includes/prod_short.md)] y cualquier impresora habilitada para la nube configurada en la página **Gestión de impresoras** en [!INCLUDE [prod_short.md](includes/prod_short.md)]. No puede imprimir desde Teams en impresoras locales conocidas por su dispositivo cliente, como impresoras en las que normalmente imprime desde su navegador. Por esta razón, no puede imprimir desde la ventana de vista previa del informe, sino solo desde la página principal de solicitud de informe, directamente en sus impresoras en la nube.

Para obtener más información sobre cómo configurar impresoras en la nube, consulte [Configurar impresoras](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>¿Puedo acceder a la cámara desde la ventana de detalles en Teams?

Sí. Las funciones de [!INCLUDE [prod_short.md](includes/prod_short.md)] de la ventana de detalles que usan la cámara están disponibles en todos los clientes de Teams.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>¿Puedo acceder a mi ubicación desde la ventana de detalles en Teams?

Si está utilizando la funcionalidad en [!INCLUDE [prod_short.md](includes/prod_short.md)] que accede a las coordenadas de su ubicación actual, como con mapas, debe usar Teams en el navegador o en la aplicación móvil de Teams. La ubicación no está disponible cuando se usa la aplicación de escritorio de Teams. 

## <a name="collaborating-with-guests"></a>[Colaborando con invitados ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>¿Puedo compartir tarjetas con usuarios fuera de mi organización?

Sí. Cuando redacta y envía un mensaje que incluye una tarjeta, todos los destinatarios del chat verán la tarjeta&mdash;incluso si son invitados o externos a su organización. Los invitados también pueden abrir la ventana de detalles si se les ha otorgado permisos para acceder a esos datos en [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>¿La experiencia es diferente para los usuarios invitados?

Sí. Invitar a usuarios invitados de fuera de su organización a participar en el chat o en un canal les brinda una experiencia similar, pero no idéntica, en comparación con los usuarios de su organización. Cuando un invitado recibe un mensaje que incluye una tarjeta, puede verlo. Los invitados también pueden abrir la ventana de detalles si se les ha otorgado permisos para acceder a esos datos en [!INCLUDE [prod_short.md](includes/prod_short.md)] y asignado una licencia de [!INCLUDE [prod_short.md](includes/prod_short.md)] dentro de su organización. Cuando un invitado redacta un mensaje, los enlaces a [!INCLUDE [prod_short.md](includes/prod_short.md)] no se expandirán en tarjetas.

Para conocer otras similitudes y diferencias entre los invitados y los miembros del equipo, consulte [Experiencia de invitado en Teams](/MicrosoftTeams/guest-experience) en la documentación de Teams.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>¿Cómo instala un usuario invitado la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Los invitados no tienen acceso al mercado de aplicaciones para instalarlas ellos mismos. Sin embargo, la aplicación se puede instalar automáticamente en función de las políticas de su organización. Otra forma de que un usuario invitado instale la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] es al recibir un mensaje de chat que incluye una tarjeta de [!INCLUDE [prod_short.md](includes/prod_short.md)]. En este caso, el usuario elige el botón **Detalles** o el menú de la tarjeta, luego instala la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para usar con su organización. Después de instalar la aplicación, un usuario no recibe automáticamente ningún permiso para acceder a los datos de su [!INCLUDE [prod_short.md](includes/prod_short.md)].

<!--TODO - check with Mike on this -->
---

## <a name="see-also"></a>Consulte también

[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]