---
title: Configuración de cuentas de usuario para la integración con Microsoft Dataverse | Documentos de Microsoft
description: Obtenga información sobre cómo configurar las cuentas de usuario que las aplicaciones usan para intercambiar datos y que los usuarios usan para acceder y sincronizar datos en las aplicaciones.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 7683c301131fa5729d74e1c6ef70880db7f3327d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607343"
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse"></a>Configuración de cuentas de usuario para la integración con Microsoft Dataverse

Este artículo proporciona una visión general de cómo configurar las cuentas de usuario que se necesitan para integrar [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-administrator-user-account"></a>Configurar la cuenta de usuario administrador

Debe agregar su cuenta de usuario administrador para [!INCLUDE[prod_short](includes/prod_short.md)] como usuario en [!INCLUDE[cds_long](includes/cds_long_md.md)]. Cuando configure la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)], utilizaremos esta cuenta una vez para instalar y configurar algunos componentes necesarios.

> [!IMPORTANT]
> La cuenta de usuario administrador debe ser un usuario con licencia con el rol de seguridad **Administrador de sistema**  en el entorno de [!INCLUDE[prod_short](includes/cds_long_md.md)] y administrador global en el arrendatario al que pertenece el entorno. Esta cuenta no necesita una licencia para [!INCLUDE[prod_short](includes/prod_short.md)], ya que se utilizará únicamente para la prestación del servicio en el arrendatario de [!INCLUDE[prod_short](includes/cds_long_md.md)] y para realizar tareas de configuración.
>
> Una vez finalizada la configuración de la conexión, este usuario de [!INCLUDE[prod_short](includes/cds_long_md.md)] puede ser eliminado. La integración continuará utilizando la cuenta de usuario creada automáticamente para la integración.

## <a name="permissions-and-security-roles-for-user-accounts-in-prod_short"></a>Permisos y roles de seguridad para cuentas de usuario en [!INCLUDE[prod_short](includes/cds_long_md.md)]

La solución de integración base crea los roles siguientes en [!INCLUDE[cds_long](includes/cds_long_md.md)] para la integración:

* **Administrador de integración**: permite a los usuarios administrar la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long](includes/cds_long_md.md)]. Normalmente, solo se asigna a la cuenta de usuario creada automáticamente para la sincronización.
* **Usuario de integración**: permite a los usuarios acceder a los datos sincronizados. Normalmente, se asigna a la cuenta de usuario creada automáticamente para la sincronización y a otros usuarios que necesiten ver los datos sincronizados o acceder a ellos.

> [!NOTE]
>
> Los roles **Administrador de integración** y **Usuario de integración** solo deben ser utilizados por el usuario de la aplicación que ejecuta la integración. El usuario de la aplicación no necesita tener la licencia [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[cds_long](includes/cds_long_md.md)] asignada.

Cuando instala la solución de integración base de CDS, se configuran los permisos para la cuenta de usuario de integración. Si se cambian manualmente esos permisos, puede restablecerlos. Elija **Volver a implementar la solución de integración** en la página **Configuración de conexión de Dataverse** para volver a instalar la solución de integración base. Este paso implementa el rol de seguridad de integración de Business Central.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Consulte también .

[Integración con Microsoft Dataverse](admin-common-data-service.md)  
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
