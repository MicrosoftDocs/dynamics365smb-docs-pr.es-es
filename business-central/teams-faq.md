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
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: f3c9626fa73247b2109e5f179aef405e80b44b07
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074645"
---
# <a name="teams-faq"></a>P+F de Teams

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo responde algunas de las preguntas que pueda tener sobre cómo trabajar con Teams y [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[General](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>¿Cómo inicio sesión en la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] en Teams?

Después de instalar la aplicación, se le pedirá que inicie sesión la primera vez que use la aplicación, cuando pegue un vínculo de [!INCLUDE [prod_short.md](includes/prod_short.md)] en el chat de Teams o cuando elija la acción **Detalles** en una tarjeta en Teams. Dependiendo de su cliente de Teams, es posible que deba ingresar las credenciales que usa para acceder a [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>¿Cómo inicio sesión fuera de la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] en Teams?

Para cerrar sesión en su identidad de usuario actual en Teams usada para conectar con [!INCLUDE [prod_short.md](includes/prod_short.md)], vaya a cualquier cuadro de redacción de chat, haga clic con el botón derecho en el icono [!INCLUDE [prod_short.md](includes/prod_short.md)] debajo y, a continuación, elija **Configuración**. Cuando aparezca la ventana, verifique su identidad actualmente conectada y luego elija **Cerrar sesión**.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>¿Se conecta la aplicación para Teams a [!INCLUDE [prod_short.md](includes/prod_short.md)] en las instalaciones? 

Nº La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams solo funciona con [!INCLUDE [prod_short.md](includes/prod_short.md)] en línea. No hay planes para apoyar tipos de implementación de [!INCLUDE [prod_short.md](includes/prod_short.md)]&mdash;como en las instalaciones, nube híbrida o nube privada&mdash;que Microsoft no aloja ni administra directamente.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>¿La aplicación funciona con múltiples empresas y entornos? 

Sí. Para buscar contactos en una empresa diferente, vaya a [Configuración](across-teams-settings.md). Cuando la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] expande un enlace en una tarjeta, el enlace debe contener el entorno y los nombres de la empresa para que la aplicación coincida con el registro de la empresa correcta. Puede pegar enlaces a cualquier empresa y entorno al que tenga acceso dentro de su organización y desde la cuenta de [!INCLUDE [prod_short.md](includes/prod_short.md)] que utilizó para iniciar sesión. Los participantes en el chat verán la tarjeta. Pero no pueden ver los detalles de la tarjeta a menos que tengan permisos para la empresa o el entorno donde se almacena ese registro.

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

### <a name="does-the-prod_shortmd-app-work-with-industry-solutions"></a>¿La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] funciona con soluciones del sector?

Sí. Pero solo algunas características de la aplicación funcionan con [Insertar aplicaciones](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- La aplicación funciona con vínculos basados en el patrón **\*.bc.dynamics.com** que se usa normalmente con Insertar aplicaciones.
- La búsqueda de contactos no está disponible para Insertar aplicaciones que reemplazan la aplicación base de Microsoft.

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>¿Dónde puedo encontrar la integración de Teams dentro del cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Actualmente no hay incrustación de controles de Teams o presencia de características de Teams dentro del cliente web de [!INCLUDE [prod_short.md](includes/prod_short.md)] u otros clientes.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>¿Funciona [!INCLUDE [prod_short.md](includes/prod_short.md)] con la aplicación móvil de Teams?

Sí. La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] se puede instalar desde la aplicación de escritorio o el navegador de Teams, o por un administrador para todos los usuarios. Una vez instalada, la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] está disponible automáticamente en Teams para iOS y Android. En dispositivos móviles, solo puede ver tarjetas enviadas por otros, acceder a detalles o mostrar la tarjeta para obtener la experiencia completa en la aplicación móvil [!INCLUDE [prod_short.md](includes/prod_short.md)]. No puede pegar vínculos que se expanden en tarjetas al redactar mensajes o buscar contactos. Para conocer los requisitos mínimos para dispositivos móviles, consulte [Requisitos mínimos para utilizar Business Central](product-requirements.md).

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

- No se puede acceder a la cámara y la ubicación desde la ventana de detalles en la aplicación de escritorio de Teams.
- Los números de teléfono no se pueden activar desde la ventana de detalles en Teams para iOS, Teams para Android o Teams en el navegador.
- Utilizando Microsoft Edge con Teams en el navegador le permite trabajar fácilmente con múltiples identidades y cuentas al iniciar sesión en Teams desde diferentes perfiles. Para aprender a usar perfiles en Microsoft Edge, vea [Iniciar sesión y crear múltiples perfiles en Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) en Soporte de Microsoft.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>¿Cuál es la mejor manera para mí de demostrar [!INCLUDE [prod_short.md](includes/prod_short.md)] y Microsoft Teams a los posibles clientes?

Si es un socio revendedor, es posible que desee tener un entorno que pueda mostrar a los clientes potenciales como parte de las demostraciones previas a la venta. Para evitar afectar a Microsoft Teams en su organización, puede obtener una cuenta de demostración de Microsoft 365 en [https://aka.ms/CDX](https://aka.ms/CDX). Esta cuenta le brinda el control total de una organización independiente de Azure que incluye Microsoft Teams y [!INCLUDE [prod_short.md](includes/prod_short.md)]. Para obtener más información, consulte [Preparación de entornos de demostración de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>¿La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams se adapta a mi personalización y personalización?

La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams puede mostrar tarjetas para enlaces a páginas y tablas de clientes en [!INCLUDE [prod_short.md](includes/prod_short.md)], como las páginas y tablas que se originan en sus propias extensiones personalizadas o en AppSource.

Los campos que se muestran en una tarjeta en Teams también pueden verse afectados por las personalizaciones de [!INCLUDE [prod_short.md](includes/prod_short.md)] instaladas para su organización. Las tarjetas no tienen en cuenta las personalizaciones específicas de la función o la personalización del usuario. Sin embargo, la ventana de detalles de la tarjeta muestra los detalles del registro como los vería en [!INCLUDE [prod_short.md](includes/prod_short.md)], incluidas las extensiones, personalizaciones de funciones y personalización de usuarios.

Cuando busca contactos, los campos que coinciden en la tabla **Contactos** y los campos que se muestran en los resultados de búsqueda no se ven afectados por ninguna personalización.

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

Para eliminar la aplicación que instaló usted mismo, vaya a cualquier cuadro de redacción de chat, busque el icono [!INCLUDE [prod_short.md](includes/prod_short.md)] debajo, haga clic con el botón derecho en el icono y seleccione **Desinstalar**.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>¿Seguirá Microsoft mejorando la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams?

En Microsoft, escuchamos constantemente los comentarios de nuestra diversa comunidad de usuarios y actuamos siguiendo las mejores sugerencias. Para conocer lo que sigue para la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams, consulte [Plan de lanzamiento de Dynamics 365](/dynamics365-release-plan/2021wave1/).

Si desea participar en la mejora de la aplicación para Teams, o tiene una idea que ayudaría a simplificar su trabajo o experiencias colaborativas en Teams, agregue una idea o vote por ideas existentes en [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="searching-for-contacts"></a>[Buscar contactos](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>¿En qué tablas busca la aplicación?

Al buscar contactos desde la aplicación de [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams, los términos de búsqueda se comparan con los registros en la tabla **Contactos** en [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>¿Qué campos de la tabla de contactos puedo buscar?

A medida que escribe los términos de búsqueda en el cuadro de búsqueda, los términos se comparan con la mayoría de los campos de la tabla **Contactos**. Los campos incluyen, por ejemplo, los campos **Nº**, **Nombre**, **Dirección**, **Nº teléfono** o **Nº teléfono móvil** y **Correo electrónico**. 

Los términos de búsqueda no se comparan con ningún campo personalizado agregado a la tabla **Contactos** por aplicaciones y extensiones.

### <a name="do-search-results-include-companies-and-persons"></a>¿Los resultados de búsqueda incluyen empresas y personas?

Sí. En [!INCLUDE [prod_short.md](includes/prod_short.md)], los contactos pueden ser de tipo **Empresa** o escriba **Persona**, donde una o varias personas pueden estar asociadas a una empresa. En los resultados de búsqueda, las empresas y las personas tienen diferentes iconos.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>¿Los resultados contactos de cualquier relación de negocio aparecerán en los resultados?

Sí. Algunos contactos pueden representar clientes o proveedores, o ambos. Otros contactos sin relación de negocio definida suelen representar clientes potenciales. Los contactos con otras relaciones de negocio, incluidas las relaciones personalizadas que haya configurado en [!INCLUDE [prod_short.md](includes/prod_short.md)], también se mostrarán en los resultados de la búsqueda.

### <a name="can-i-look-up-contact-details-during-meetings"></a>¿Puedo buscar datos de contacto durante las reuniones?

Sí. Puede buscar información de contacto, historial de interacción y documentos relacionados para su cliente o proveedor durante una reunión o llamada de Teams mientras se lleva a cabo la reunión, sin salir de Teams.

De hecho, puede buscar detalles de contacto desde cualquier lugar de Teams mediante el cuadro de comando. Por ejemplo, puede buscar detalles de contacto en el calendario de Teams para ayudarle a configurar reuniones.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>¿Cómo puede ver mis últimas interacciones con un contacto?

La ventana de detalles de un contacto muestra los movimientos del registro de interacción. Los movimientos del registro de interacción proporcionan el historial de interacciones que su organización ha tenido con el contacto específico. Las interacciones pueden incluir correos electrónicos que haya intercambiado, llamadas que haya recibido o documentos que haya enviado.

Para que se muestren las interacciones, [!INCLUDE [prod_short.md](includes/prod_short.md)] debe configurarse para realizar un seguimiento de las interacciones. Para obtener más información sobre las interacciones del registro, consulte [Registrar interacciones con contactos](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>¿Cómo puedo registrar una llamada o reunión de Teams como una interacción?

En la ventana de detalles de un contacto, busque la acción **Crear interacción** y elija entre las llamadas entrantes o salientes como plantillas de interacción. También puede crear sus propias plantillas de interacción personalizadas específicamente para usar con las conversaciones de Teams.

### <a name="can-i-call-a-contact-from-the-prod_shortmd-app-for-teams"></a>¿Puedo llamar a un contacto desde la aplicación de [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] tiene una integración limitada con las capacidades de llamada de Teams. No es posible iniciar instantáneamente una llamada VOIP desde la ficha de contacto o la ventana de detalles de contacto. Sin embargo, cuando ve los detalles de contacto en la aplicación de escritorio de Teams, puede seleccionar el campo de número de teléfono para marcar ese número si Teams está configurado como su aplicación de marcación predeterminada en su dispositivo. Para marcar números de teléfonos fijos o móviles mediante PSTN, el sistema telefónico tradicional, Teams requiere que tenga la aplicación Microsoft 365 Business Voice. Para obtener más información, consulte [¿Qué es Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>¿Cómo veo los documentos recientes de un cliente o proveedor?

[!INCLUDE [prod_short.md](includes/prod_short.md)] normalmente relaciona un contacto con un registro de cliente o proveedor que, a su vez, está relacionado con registros de transacciones comerciales, como ofertas de ventas o facturas de compra. Para ver documentos relacionados para un contacto, vaya a la ventana de detalles del contacto, elija el valor de campo **Relación de negocio** o use las acciones para navegar hasta el cliente o proveedor asociado. En la página del cliente o proveedor, expanda el panel del cuadro informativo para revelar estadísticas de varios documentos en los que puede profundizar. Su experiencia puede diferir según sus personalizaciones.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>¿Cómo puedo buscar contactos usando caracteres especiales?

Puede introducir criterios de búsqueda usando casi cualquier carácter Unicode. Sin embargo, [!INCLUDE [prod_short.md](includes/prod_short.md)] se reserva los siguientes símbolos para otros usos: **=**, **.**, **\**_ y _*@**. Es posible que el uso de estos símbolos en los términos de búsqueda no arroje los resultados esperados. Si no ve los resultados esperados, incluya los símbolos en sus términos de búsqueda entre comillas simples, por ejemplo, **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>¿Cómo puedo buscar contactos almacenados en una empresa diferente?

La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams puede buscar clientes, proveedores y otros contactos en una empresa a la vez.  
Para buscar contactos almacenados en una empresa de [!INCLUDE [prod_short.md](includes/prod_short.md)], abra [Configuración](across-teams-settings.md) y, a continuación, cambie el entorno y la empresa desde ahí.

### <a name="are-prod_shortmd-contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>¿Los contactos de [!INCLUDE [prod_short.md](includes/prod_short.md)] son diferentes de los de la pantalla de contactos de Teams?

Sí. Los contactos almacenados en [!INCLUDE [prod_short.md](includes/prod_short.md)] representan los contactos profesionales disponibles para su organización. Son contactos con los que tiene una relación de negocio establecida y bien definida, o contactos que representan a clientes potenciales. Estos contactos suelen ser contactos externos. En comparación, los contactos que se muestran en la lista de contactos de llamada de Teams son sus propios contactos. Estos contactos no se comparten necesariamente con otros miembros de su organización y, por lo general, representan contactos internos de su organización.

### <a name="does-prod_shortmd-synchronize-contacts-with-teams"></a>¿[!INCLUDE [prod_short.md](includes/prod_short.md)] sincroniza los contactos con Teams?

Nº Los contactos almacenados en [!INCLUDE [prod_short.md](includes/prod_short.md)] se mantienen separados de sus contactos almacenados en Teams.
Actualmente no hay planes para sincronizar las dos listas juntas.

### <a name="what-is-the-minimum-version-of-prod_shortmd-for-contact-search"></a>¿Cuál es la versión mínima de [!INCLUDE [prod_short.md](includes/prod_short.md)] para la búsqueda de contactos?

La búsqueda de contactos requiere que haya instalado la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams versión 1.0.4 o superior y se conecte a entornos de [!INCLUDE [prod_short.md](includes/prod_short.md)] de la versión 18 o superior.

### <a name="can-i-search-from-my-mobile-device"></a>¿Puedo buscar desde mi dispositivo móvil?

En este momento, la búsqueda de contactos no está disponible en Teams para iOS y Teams para Android.

### <a name="which-permissions-do-i-need-for-contact-search"></a>¿Qué permisos necesito para buscar contactos?

Para buscar contactos, necesita permiso de nivel de objeto para la tabla **Contactos** dentro de la empresa de [!INCLUDE [prod_short.md](includes/prod_short.md)] que está buscando. Para ver la ventana de detalles de un contacto, necesita al menos permiso de lectura para la página **Contacto** dentro de la empresa de [!INCLUDE [prod_short.md](includes/prod_short.md)] y cualquier otro objeto relacionado.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>¿Puedo usar la búsqueda de contactos si soy administrador delegado?

Sí. También puede buscar contactos y detalles de contacto si tiene un rol de administrador delegado en una organización.

### <a name="is-contact-search-affected-by-api-limits"></a>¿La búsqueda de contactos se ve afectada por los límites de la API?

Sí. La búsqueda de contactos de Teams se basa en las API de [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 y está sujeta a los límites de la API que administran el uso. Puede obtener más información sobre los límites en [Límites de la API actuales](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>¿Por qué a veces me pide que configure la aplicación?

Después de iniciar sesión por primera vez en la aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams, la aplicación intentará determinar su empresa preferida en [!INCLUDE [prod_short.md](includes/prod_short.md)]. Si la aplicación no puede determinar la empresa, es posible que tenga que ir a la **Configuración** y elegir la empresa en la que desea buscar. Esta situación se produce, por ejemplo, si tiene acceso a varias empresas en distintos entornos de su organización. En este caso, tendrá que elegir una empresa antes de poder empezar a buscar.  

La aplicación también puede pedirle que visite la **Configuración** si no tiene una suscripción de [!INCLUDE [prod_short.md](includes/prod_short.md)], no existen entornos de [!INCLUDE [prod_short.md](includes/prod_short.md)], o su cuenta no tiene una licencia de [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Me gustaría buscar productos o registros de otras tablas. ¿Puedo hacer esto desde Teams?

En este momento no es posible buscar en otras tablas. La aplicación [!INCLUDE [prod_short.md](includes/prod_short.md)] para Teams solo busca en la lista de contactos de [!INCLUDE [prod_short.md](includes/prod_short.md)], que puede incluir proveedores, clientes y otros contactos.

Si desea que las funcionalidades de búsqueda evolucionen para incluir otras tablas, animamos a nuestra comunidad a que agregue una idea o vote por ideas existentes en https://aka.ms/BusinessCentralIdeas.

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

Nº Si bien todos en el chat o la reunión pueden ver la tarjeta en sí, la ventana de detalles solo aparece para usted en su dispositivo cuando elige **Detalles**. Otros usuarios deben elegir **Detalles** si desean ver la ventana de detalles en su dispositivo.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>¿Puedo iniciar una llamada de Teams desde la ventana de detalles en Teams?

Sí. Si usa la aplicación de escritorio de Teams, inicie una llamada eligiendo el número vinculado en un campo de número de teléfono, como el campo **Nº teléfono móvil** en la tarjeta de **Contacto**. Teams debe ser su aplicación de marcación designada.

Para llamar a teléfonos fijos y móviles locales o internacionales, Teams requiere que tenga una licencia de Business Voice para llamadas empresariales. Además, debe configurar Teams como su solución de llamadas. Para obtener más información, consulte [Planificar la solución de voz de Teams](/microsoftteams/cloud-voice-landing-page) en la documentación de Teams.

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

---

## <a name="see-also"></a>Consulte también

[Información general sobre [!INCLUDE [prod_short](includes/prod_short.md)] y la integración de Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]