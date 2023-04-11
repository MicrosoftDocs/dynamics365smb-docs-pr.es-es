---
title: Solucionar problemas de acceso con licencias de Microsoft 365
description: Aprenda cómo puede solucionar los problemas de acceso a Business Central con solo una licencia de Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Solucionar problemas de acceso con licencias de Microsoft 365

## Mensaje de error "Esta página utiliza datos de tablas relacionadas a las que no tiene acceso"

### Síntomas

Al acceder a un registro en Teams, se le muestra un mensaje de error en una pestaña o detalles de la tarjeta similar a:

"Esta página utiliza datos de tablas relacionadas a las que no tiene acceso. Para trabajar con todas las características de esta página, comuníquese con su administrador".

### Causa

Lo más probable es que le falten permisos de objeto para las tablas a las que se vincula la página actual o el registro.

## Se ha habilitado el acceso a Microsoft 365, pero los usuarios obtienen un error de permiso

### Síntomas

Se ha habilitado el acceso con Microsoft 365 en el Centro de administración de Business Central, pero los usuarios obtienen un error de permiso al acceder a cualquier registro.

### Causa

Si habilita el acceso en el Centro de administración de Business Central, pero no asigna permisos en la página **Configuración de licencias**, cualquiera que intente acceder a los registros de Business Central en Teams tendrá su registro de usuario aprovisionado sin permiso para ningún objeto. Business Central es seguro por diseño: los administradores primero deben configurar a qué datos se puede acceder en Teams. 

### Resolución

La personalización de los permisos en la página Configuración de licencia solo afectará a los usuarios recién creados. También debe asignar los permisos que faltan a los usuarios que ya se han creado a través de la página de lista de usuarios. 

## Compartió un vínculo en Teams, pero los usuarios reciben un mensaje de que solo pueden ver datos

### Síntomas

Cuando comparte un vínculo en Teams como usuario de Business Central, otros reciben el error "Al acceder a Business Central con una licencia de Microsoft 365, solo se pueden ver los datos en Microsoft Teams".

### Causa

Al compartir un vínculo de Business Central a un chat o canales de Teams, al navegar por un vínculo siempre se navegará fuera de Microsoft Teams cuando los datos ya no sean accesibles para una persona que tenga una licencia de Microsoft 365.

### Resolución

Al compartir páginas o registros, incluya la versión preliminar del vínculo como una tarjeta o comparta los datos como una pestaña en el chat o el canal.

## La tarjeta del vínculo compartido es mínima y no incluye el botón Detalles

### Síntomas 

Cuando un titular de licencia de Microsoft 365 sin una licencia de Business Central comparte un vínculo de Business Central en Teams, automáticamente se expande en una tarjeta que no tiene información útil y solo muestra Business Central sin el botón **Detalles** .

### Causa

Los usuarios que tienen una licencia de Microsoft 365 pero no una licencia de Business Central no pueden compartir vínculos como tarjetas. Si el usuario tiene instalada la aplicación Business Central para Teams y pega un vínculo en el área de redacción, solo se muestra una tarjeta mínima. 

## Consulte también .

[Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurar acceso con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
[Integración de Business Central y Microsoft Teams](across-teams-overview.md)
[Compartir registros de Business Central y vínculos de página en Microsoft Teams](across-working-with-teams.md)  
[Solución de problemas de integración de Teams](admin-teams-troubleshooting.md)  