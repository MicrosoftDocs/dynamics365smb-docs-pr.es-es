---
title: 'Solución de problemas: acceso a la cámara y a la ubicación'
description: Este artículo describe cómo solucionar problemas de acceso a la información de la cámara y la ubicación en Business Central.
author: bholtorf
ms.author: bholtorf
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
---

# Solución de problemas: acceso a la cámara y a la ubicación

Puede encontrar algunos problemas al intentar acceder a la cámara y a la información de ubicación de un dispositivo desde [!INCLUDE[prod_short](includes/prod_short.md)]. Puede encontrar las causas posibles de estos problemas y cómo solucionarlos a continuación.

## El dispositivo debe tener capacidades de cámara y ubicación

Para acceder a la cámara o la ubicación de un usuario desde un dispositivo, el dispositivo debe tener una cámara física o la capacidad de recuperar información de ubicación.

Si su dispositivo tiene capacidades de cámara y ubicación, pero sigue teniendo problemas, es posible que algunos controladores deban actualizarse o reinstalarse. Incluso si no está seguro, siempre recomendamos que actualice el sistema operativo, los controladores y el navegador de su dispositivo a la última versión para obtener la mejor experiencia.

## Permisos de acceso no habilitados

Debe habilitar el acceso general a la cámara y la ubicación desde la configuración de privacidad de su dispositivo y otorgar permiso explícitamente para [!INCLUDE[prod_short](includes/prod_short.md)] para acceder a ellos. Por ejemplo, para ver o cambiar los permisos de un dispositivo ejecutando Windows, vaya a **Configuración**, elija **Privacidad** y, a continuación, **Permisos de la aplicación**. 

Para dispositivos móviles, debe dar permisos de acceso a la cámara y a la ubicación para la Aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)]. Para hacerlo en un dispositivo iOS, vaya a **Configuración**, elija **Privacidad**, y después a **Cámara** o **Almacén**. Para los dispositivos Android, vaya a **Configuración**, elija **Aplicaciones y notificaciones**, **Avanzado**, **Administrador de permisos** y después, **Cámara** o **Ubicación**.

Además, si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en un navegador, también debe dar permiso al sitio de [!INCLUDE[prod_short](includes/prod_short.md)] para acceder a la información de la cámara o ubicación. Para ver o cambiar los permisos de un sitio en el navegador de Microsoft Edge, vaya a **Configuración**, elija **Permisos del sitio** y después, **Cámara** o **Ubicación**. Tenga en cuenta que esto puede ser diferente para otros navegadores.

De manera predeterminada, el dispositivo o navegador mostrará una solicitud para acceder a estas características cuando el usuario las active por primera vez.

> [!NOTE]  
> Algunos navegadores antiguos no dan acceso a la cámara ni a la ubicación. Por ejemplo, la cámara no está disponible en Internet Explorer o el navegador Microsoft Edge (versión heredada).

## La conexión del cliente web no es segura

Las capacidades de cámara y ubicación solo están disponibles cuando se accede al cliente web a través de conexiones HTTP con seguridad SSL, utilizando el esquema de URI `https://`. 

La única excepción es conectarse a `http://localhost`, utilizado para fines de desarrollo y prueba.


## Trabajar con tecnologías de virtualización

Cuando se conecte a [!INCLUDE[prod_short](includes/prod_short.md)] mediante el Escritorio remoto u otra virtualización, es posible que el acceso a la cámara o la ubicación no esté disponible. Si este es el caso, use el sistema físico en su lugar.

## Software antivirus
Algunos software antivirus bloquean el acceso a la cámara y la ubicación de forma predeterminada. Recuerde comprobar la configuración de su software antivirus.

## Consulte también
[Implementación de la cámara en AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementación de la ubicación en AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]