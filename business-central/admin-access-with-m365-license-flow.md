---
title: Flujo de acceso de usuario para licencias de Microsoft 365
description: Obtenga una descripción general de lo que sucede cuando un usuario accede a los datos de Business Central usando su licencia de Microsoft 365 por primera vez.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses" />Flujo de acceso de usuario para licencias de Microsoft 365

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Este artículo describe lo que sucede cuando un usuario accede a los datos de Business Central usando su licencia de Microsoft 365 por primera vez. Comprender este flujo permite a los administradores planificar su enfoque y configurar Business Central para satisfacer sus necesidades comerciales.

1. Primero, se autentica la identidad del usuario. 
2. Business Central verifica que todos los [requerimientos mínimos](admin-access-with-m365-license.md#minimum-requirements) se cumplan.
3. Business Central verifica que este usuario no tenga una licencia superior, como una licencia de Business Central o una función administrativa, como una función de administrador delegado. 
4. Business Central verifica si el usuario está accediendo a datos que pertenecen a un entorno que ha habilitado el acceso con licencias de Microsoft 365. 
5. El registro de usuario se aprovisiona en Business Central, asignando el Grupo de usuarios, Perfil y Conjuntos de permisos definidos en la página de configuración de la licencia de Microsoft 365. De forma predeterminada, se asigna el grupo de usuarios de Teams, se asigna el perfil de empleado y solo se asigna el conjunto de permisos de inicio de sesión. También se aplica cualquier otra configuración predeterminada de usuario, al igual que un usuario de Business Central con licencia. 
6. Se aplica el modelo de seguridad completo de Business Central para determinar si el usuario debe poder acceder al registro, a la página, en la empresa y el entorno especificados. 

Si todos los pasos tienen éxito, el usuario ahora puede ver estos datos de Business Central en Teams. El servicio Business Central garantiza automáticamente el acceso de solo lectura y simplifica la interfaz de usuario. 

La cuenta de usuario ahora está registrada en Business Central y se puede administrar como cualquier usuario de Business Central.

> [!NOTE]
> Los pasos pueden variar según cualquier configuración de seguridad adicional que haya especificado en Microsoft 365 o Business Central.

## <a name="see-also" />Consulte también .

[Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurar acceso con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
