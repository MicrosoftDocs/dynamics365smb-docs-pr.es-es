---
title: Estado de los avisos de privacidad en Business Central
description: Una descripción general de la página de estado de los avisos de privacidad en Business Central
author: javariya
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: null
ms.search.form: 1565
audience: null
ms.author: a-jaaamir
ms.date: 07/21/2022
---

# <a name="privacy-notices-status-in-"></a><a name="privacy-notices-status-in-"></a><a name="privacy-notices-status-in-"></a>Estado de avisos de privacidad en [!INCLUDE[prod_long](includes/prod_long.md)]

Este artículo analiza qué es un aviso de privacidad y explica el propósito de la página **Estado de los avisos de privacidad** en [!INCLUDE[prod_short](includes/prod_short.md)]. También aprenderá cómo los administradores pueden usar esta página.

## <a name="privacy-notice"></a><a name="privacy-notice"></a><a name="privacy-notice"></a>Aviso de privacidad

Un aviso de privacidad establece las políticas de recopilación de datos, procesamiento de datos y privacidad de datos seguidas por el controlador de datos de la organización. Es un documento que describe qué datos se recopilan y con qué fines, cómo se procesan los datos del usuario, cómo se almacenan y a quién contactar si un usuario quiere preguntar algo sobre sus datos. 

## <a name="privacy-notices-status-page"></a><a name="privacy-notices-status-page"></a><a name="privacy-notices-status-page"></a>Página Estado de avisos de privacidad

En [!INCLUDE[prod_short](includes/prod_short.md)], si los usuarios quieren integrar sus datos con Microsoft Exchange, Microsoft OneDrive y Microsoft Teams, deberán aceptar el aviso de privacidad de cada entidad. O un administrador puede aprobar los avisos de privacidad en su nombre. Los administradores pueden ver el estado de los avisos de privacidad en la página **Estado de los avisos de privacidad**. Puede encontrar la página **Estado de los avisos de privacidad** en [!INCLUDE[prod_short](includes/prod_short.md)] escribiendo el nombre de la página en la barra de búsqueda.  

En esa página, encontrará una tabla con opciones de aprobación para cada uno de los servicios mencionados anteriormente. 

| Columna | Descripción |
| ----------- | ----------- | 
| **Nombre de integración** | Nombre del servicio, como Microsoft OneDrive. |
| **Aceptar para todos** | Un administrador aprueba el aviso de privacidad para todos los usuarios. |
| **No aceptar para todos** | Un administrador no aprueba el aviso de privacidad para todos los usuarios. |
| **Permitir que el usuario decida** | Los usuarios deciden aprobar o no el aviso de privacidad del servicio. |

> [!NOTE]
> Solo puede ver el estado de los avisos de privacidad en la página **Estado de los avisos de privacidad** principal. Para editar las respuestas, vaya a **Lista de edición** en la barra de acción de la página donde ahora se puede hacer clic en las opciones y no están atenuadas.

## <a name="privacy-notice-approvals"></a><a name="privacy-notice-approvals"></a><a name="privacy-notice-approvals"></a>Aprobaciones de aviso de privacidad

Los administradores pueden ver las aprobaciones individuales y administrarlas en la subpágina **Aprobaciones de avisos de privacidad**. Vaya a la barra *Acción* de la página **Acción de Avisos de privacidad**, bajo *Comportamiento*, para encontrar la opción *Mostrar aprobaciones individuales*. Esta opción va a la página **Aprobaciones de avisos de privacidad**.<br>

En esa página, encontrará una tabla con opciones de aprobación. 

| Columna | Descripción |
| ----------- | ----------- | 
| **Nombre de integración** | Nombre del servicio, como Microsoft OneDrive. |
| **Nombre usuario** | El usuario que posee esta aprobación. Si *Organización* está escrito en la columna Nombre de usuario, la aprobación pertenece a toda la organización. 
| **Aceptar** | El usuario aprueba el aviso de privacidad. |
| **No aceptar** | El usuario no aprueba el aviso de privacidad. |
| **Nombre de usuario del aprobador** | Quien aprueba el aviso de privacidad. |

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Información general sobre cumplimiento  ](/dynamics365/business-central/compliance/compliance-overview)  
[Responder a las solicitudes de datos personales  ](/dynamics365/business-central/admin-responding-to-requests-about-personal-data)  
[Política de privacidad y condiciones de uso ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-checklist-i-privacypolicy-termsofuse)  
[Directivas de retención de datos](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/define-retention-policies) 
