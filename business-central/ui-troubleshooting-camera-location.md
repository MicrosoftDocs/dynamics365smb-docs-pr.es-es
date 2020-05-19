---
title: 'Solución de problemas: acceso a la cámara y a la ubicación'
description: Este artículo describe cómo solucionar problemas de acceso a la información de la cámara y la ubicación en Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics365-business-central
ms.openlocfilehash: befb7af01ba26512a4b62005e81b5a3ff351b02f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324478"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Solución de problemas: acceso a la cámara y a la ubicación

Puede encontrar algunos problemas al intentar acceder a la cámara y a la información de ubicación de un dispositivo desde [!INCLUDE[prodshort](includes/prodshort.md)]. Puede encontrar las causas posibles de estos problemas y cómo solucionarlos a continuación.

## <a name="device-must-have-camera-and-location-capabilities"></a>El dispositivo debe tener capacidades de cámara y ubicación

Para acceder a la cámara o la ubicación de un usuario desde un dispositivo, el dispositivo debe tener una cámara física o la capacidad de recuperar información de ubicación.

Si su dispositivo tiene capacidades de cámara y ubicación, pero sigue teniendo problemas, es posible que algunos controladores deban actualizarse o reinstalarse. Incluso si no está seguro, siempre recomendamos que actualice el sistema operativo, los controladores y el navegador de su dispositivo a la última versión para obtener la mejor experiencia.

## <a name="access-permissions-not-enabled"></a>Permisos de acceso no habilitados

Debe habilitar el acceso general a la cámara y la ubicación desde la configuración de privacidad de su dispositivo y otorgar permiso explícitamente para [!INCLUDE[prodshort](includes/prodshort.md)] para acceder a ellos. Por ejemplo, para ver o cambiar los permisos de un dispositivo ejecutando Windows, vaya a **Configuración**, elija **Privacidad** y, a continuación, **Permisos de la aplicación**. 

Para dispositivos móviles, debe dar permisos de acceso a la cámara y a la ubicación para la Aplicación móvil de [!INCLUDE[prodshort](includes/prodshort.md)]. Para hacerlo en un dispositivo iOS, vaya a **Configuración**, elija **Privacidad**, y después a **Cámara** o **Localización**. Para los dispositivos Android, vaya a **Configuración**, elija **Aplicaciones y notificaciones**, **Avanzado**, **Administrador de permisos** y después, **Cámara** o **Ubicación**.

Además, si está utilizando [!INCLUDE[prodshort](includes/prodshort.md)] en un navegador, también debe dar permiso al sitio de [!INCLUDE[prodshort](includes/prodshort.md)] para acceder a la información de la cámara o ubicación. Para ver o cambiar los permisos de un sitio en el navegador de Microsoft Edge, vaya a **Configuración**, elija **Permisos del sitio** y después, **Cámara** o **Ubicación**. Tenga en cuenta que esto puede ser diferente para otros navegadores.

De manera predeterminada, el dispositivo o navegador mostrará una solicitud para acceder a estas características cuando el usuario las active por primera vez.

> [!NOTE]  
> Algunos navegadores antiguos no dan acceso a la cámara ni a la ubicación. Por ejemplo, la cámara no está disponible en Internet Explorer o el navegador Edge (versión heredada).

## <a name="web-client-connection-not-secure"></a>La conexión del cliente web no es segura

Las capacidades de cámara y ubicación solo están disponibles cuando se accede al cliente web a través de conexiones HTTP con seguridad SSL, utilizando el esquema de URI `https://`. 

La única excepción es conectarse a `http://localhost`, utilizado para fines de desarrollo y prueba.


## <a name="working-with-virtualization-technologies"></a>Trabajo con tecnologías de virtualización

Cuando se conecte a [!INCLUDE[prodshort](includes/prodshort.md)] mediante el Escritorio remoto u otra virtualización, es posible que el acceso a la cámara o la ubicación no esté disponible. Si este es el caso, use el sistema físico en su lugar.

## <a name="antivirus-software"></a>Software antivirus
Algunos software antivirus bloquean el acceso a la cámara y la ubicación de forma predeterminada. Recuerde comprobar la configuración de su software antivirus.

## <a name="see-also"></a>Consulte también
[Implementación de la cámara en AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementación de la ubicación en AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)