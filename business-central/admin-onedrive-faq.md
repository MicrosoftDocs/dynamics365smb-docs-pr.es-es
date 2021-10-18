---
title: Preguntas más frecuentes de OneDrive para la Empresa
description: Obtenga respuestas a algunas preguntas típicas sobre cómo trabajar con OneDrive para la Empresa y Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: 3d9058b3b0f751729d5538f36454bd8244a3594f
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589516"
---
# <a name="onedrive-for-business-faq"></a>Preguntas más frecuentes de OneDrive para la Empresa

[!INCLUDE [online_only](includes/online_only.md)]

Este artículo responde algunas de las preguntas que pueda tener sobre cómo trabajar con OneDrive y [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>¿Funciona esto con todos los clientes de [!INCLUDE[prod_short](includes/prod_short.md)]?

Sí. Puede abrir archivos en OneDrive desde las aplicaciones móviles de [!INCLUDE[prod_short](includes/prod_short.md)], al ver los detalles de la tarjeta en Microsoft Teams o incluso desde el complemento de Outlook.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>¿Es OneDrive lo mismo que SharePoint para almacenar archivos?

Como parte de su suscripción a Microsoft 365, su organización le proporciona OneDrive, su almacenamiento de archivos en la nube. OneDrive es privado de forma predeterminada, y le permite organizar su contenido y elegir qué archivos o carpetas compartir y con quién. SharePoint, por otro lado, proporciona un repositorio de archivos en la nube que se comparte con otros miembros de su organización.  

## <a name="does-prod_short-support-consumer-onedrive"></a>¿Admite [!INCLUDE[prod_short](includes/prod_short.md)] OneDrive para consumidores?

Nº Esta integración está destinada exclusivamente a OneDrive para la Empresa y solo es compatible con su cuenta de trabajo. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>¿Se admiten todos los planes de OneDrive para la Empresa?

[!INCLUDE[prod_short](includes/prod_short.md)] no admite planes independientes para OneDrive para la Empresa. OneDrive debe adquirirse como parte de un plan empresarial o de negocios de Microsoft 365. Para más información, vea [Comparar planes y precios de almacenamiento en la nube de OneDrive](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>¿Dónde puedo ver el estado del servicio de OneDrive?

Los administradores pueden acceder al panel de estado del servicio como parte del centro de administración de Microsoft 365. El panel incluye disponibilidad del servicio de OneDrive. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>¿Está disponible la integración de OneDrive en [!INCLUDE[prod_short](includes/prod_short.md)] local?

Si, pero a diferencia de [!INCLUDE[prod_short](includes/prod_short.md)] en línea, requiere una configuración adicional. Para obtener más información, consulte [Configurar Business Central local](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>¿Se conecta [!INCLUDE[prod_short](includes/prod_short.md)] local con SharePoint Server?

Nº Esta combinación de implementación no se admite, incluso si SharePoint Server ha habilitado Mis sitios.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>¿Se conecta [!INCLUDE[prod_short](includes/prod_short.md)] en línea con SharePoint Server?

Nº Esta combinación de implementación no se admite, incluso si SharePoint Server ha habilitado Mis sitios.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>¿Cómo funciona esto en una organización con múltiples entornos?

La integración asume que los nombres de las empresas son únicos en entornos de [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando los nombres de empresas son únicos en toda la organización, al abrir un archivo en OneDrive se copiará el archivo a una carpeta con el nombre de la empresa actual. Si los nombres de las empresas no son únicos en todos los entornos, es posible que los archivos de nombres de empresas idénticos se coloquen juntos en la misma carpeta.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Hemos cambiado el nombre de la empresa. ¿Qué pasa con mis archivos anteriores?

[!INCLUDE[prod_short](includes/prod_short.md)] no migra automáticamente los archivos que abrió anteriormente en OneDrive a la nueva carpeta. Después de cambiar el nombre de su empresa, la acción Abrir en OneDrive copiará los archivos a una carpeta que tenga el nuevo nombre de la empresa.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Al adjuntar archivos a [!INCLUDE[prod_short](includes/prod_short.md)], ¿cómo elijo un archivo de OneDrive? 
[!INCLUDE[prod_short](includes/prod_short.md)] no proporciona un selector de archivos en la nube. Debes descargar el archivo desde OneDrive a su dispositivo y luego cargarlo en [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Quiero abrir archivos en SharePoint. ¿Cómo lo hago?

[!INCLUDE[prod_short](includes/prod_short.md)] no proporciona funciones para copiar archivos a SharePoint y abrirlos desde una biblioteca de SharePoint. Póngase en contacto con su socio de Microsoft para conocer sus opciones o busque aplicaciones en AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>¿Cómo desactivo la integración con OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] en línea no proporciona una forma de habilitar o deshabilitar la integración con OneDrive.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>¿Debo usar la página Configuración de conexión de SharePoint para conectarme con SharePoint?

Esta es una característica heredada donde todos los archivos de [!INCLUDE[prod_short](includes/prod_short.md)] de todos los usuarios se envían a una sola carpeta de SharePoint. Recomendamos que no configure la ficha desplegable Documentos compartidos en la página Configuración de conexión de SharePoint porque estamos trabajando para abandonar esta función.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>¿Qué versión de [!INCLUDE[prod_short](includes/prod_short.md)] admite OneDrive?

La integración con OneDrive pasó a estar disponible en el lanzamiento de versiones 2 de 2021.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>¿Seguirá Microsoft mejorando la integración con OneDrive?

En Microsoft, escuchamos constantemente los comentarios de nuestra diversa comunidad de usuarios y actuamos siguiendo las mejores sugerencias. Para obtener información sobre novedades en integraciones con aplicaciones de Microsoft 365, consulte el [Plan de lanzamiento de Dynamics 365](/dynamics365-release-plan/2021wave1).  

Si desea participar en la mejora de la integración de OneDrive o tiene una idea que mejoraría el intercambio de archivos y la colaboración en [!INCLUDE[prod_short](includes/prod_short.md)], agregue una idea o vote por ideas existentes en [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Solución de problemas

Esta sección proporciona información sobre cómo identificar y solucionar problemas que pueda experimentar al usar OneDrive con [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Tengo que iniciar sesión cada vez que abro un archivo

Lo sentimos, es un problema conocido y estamos trabajando en ello. Esperamos brindar una experiencia más fluida en una próxima actualización.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central no puede encontrar mi OneDrive

Cuando aparece este mensaje, "No se pudo determinar la ubicación de su OneDrive para la Empresa, póngase en contacto con su socio para configurarlo.", compruebe si el usuario ha accedido a su OneDrive al menos una vez. Si no lo ha hecho, pídale a la persona que vaya a portal.office.com/onedrive para configurarlo. Eso puede llevar un tiempo. Si el mensaje sigue apareciendo después de 24 horas, comuníquese con Soporte técnico.  
 

## <a name="see-also"></a>Consulte también
[Integración de Business Central y OneDrive](across-onedrive-overview.md)  
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
