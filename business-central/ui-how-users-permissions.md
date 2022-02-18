---
title: Crear usuarios de acuerdo con las licencias
description: Describe cómo agregar usuarios a Business Central Online o local según las licencias.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9173
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e11c7b88a17998086f0f11e809415248ad8f389
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115345"
---
# <a name="create-users-according-to-licenses"></a>Crear usuarios de acuerdo con las licencias

En este artículo se describe cómo los administradores crean usuarios y definen quién puede iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)], y qué permisos se conceden a los diferentes tipos de usuario según las licencias.

Cuando crea usuarios en [!INCLUDE[prod_short](includes/prod_short.md)], puede asignarles permisos específicos a través de conjuntos de permisos y organizar usuarios en grupos de usuarios. Los grupos de usuarios facilitan la administración de permisos para múltiples usuarios al mismo tiempo. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

Para obtener más información sobre los diferentes tipos de licencias y cómo funcionan las licencias en [!INCLUDE[prod_short](includes/prod_short.md)], [descargue la Guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> El proceso de administración de usuarios y licencias varía según si [!INCLUDE[prod_short](includes/prod_short.md)] se implementa en línea o localmente. Para [!INCLUDE [prod_short](includes/prod_short.md)] Online, debe agregar usuarios desde Microsoft 365. En implementaciones locales, puede crear, editar y eliminar usuarios directamente.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Administración de usuarios y licencias en implementaciones en línea

En la versión en línea de [!INCLUDE[prod_short](includes/prod_short.md)], el número de usuarios se define mediante la suscripción y se agrega a su suscriptor en el Centro de socios de Microsoft, generalmente por parte de su socio de Microsoft. Para obtener más información, vea [Agregar un nuevo cliente](/partner-center/add-a-new-customer) y [Crear, suspender o cancelar suscripciones de clientes](/partner-center/create-a-new-subscription) en la ayuda del Centro de socios de Microsoft.

Para definir quién puede iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)], debe asignar las licencias de producto asignarse a los usuarios de acuerdo con los roles que desempeñarán en [!INCLUDE[prod_short](includes/prod_short.md)]. Se puede hacer de las siguientes maneras:

- El administrador de Microsoft 365 de su empresa puede hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com). Para obtener más información, vea [Agregar usuarios individualmente o en masa a Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un socio de Microsoft puede asignar licencias en el Centro de administración de Microsoft 365 o en el Centro de partners de Microsoft. Para obtener más información, vea [Tareas de administración de usuarios para cuentas de cliente](/partner-center/assign-licenses-to-users) en la ayuda del Centro de socios de Microsoft.

Para obtener más información, vea [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda de administración.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central
Después de agregar usuarios o cambiar la información del usuario en el Centro de administración de Microsoft 365, puede importar rápidamente la información del usuario a [!INCLUDE[prod_short](includes/prod_short.md)]. Esto incluye asignaciones de licencias. 

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de administrador.
2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.  
3. Elija **Actualizar usuarios desde Microsoft 365**.

Si está agregando nuevos usuarios, el siguiente paso es asignar grupos de usuarios y permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md). Si está actualizando la información del usuario y la actualización incluye un cambio de licencia, los usuarios se asignarán al grupo de usuarios apropiado y sus conjuntos de permisos se actualizarán. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md).  

> [!NOTE]
> Todos los usuarios deben tener asignada la misma licencia, Essential o Premium. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Para obtener más información sobre la sincronización de la información de usuario con Microsoft 365, vea la sección [Sincronización con Microsoft 365](#m365).

> [!NOTE]
> Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su Business Central para que pueda trabajar con usted en los datos fiscales. Para obtener más información, consulte [Invitar a un contable externo a Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Para eliminar el acceso de un usuario al sistema

En implementaciones en línea, puede eliminar el acceso de un usuario a [!INCLUDE[prod_short](includes/prod_short.md)]. Se mantienen todas las referencias al usuario, pero el usuario no puede iniciar sesión y las sesiones activas para el usuario se detienen.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Abra la página **Ficha de usuario** para el usuario relevante y, a continuación, en el campo **Estado**, seleccione **Deshabilitado**.
3. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

También puede eliminar la licencia de un usuario en el Centro de administración de Microsoft 365. El usuario no puede iniciar sesión. Para obtener más información, consulte [Quitar la asignación de las licencias de los usuarios](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Sincronización con Microsoft 365

Cuando asigna una licencia para [!INCLUDE[prod_short](includes/prod_short.md)] a un usuario en Microsoft 365, hay dos formas de crear el usuario en [!INCLUDE[prod_short](includes/prod_short.md)].  

- El administrador puede agregar el usuario eligiendo la página **Actualizar usuarios de Microsoft 365** en la página **Usuarios** como se describe en la sección [Para agregar un usuario o actualizar la información del usuario en Business Central](#adduser).
- La información de la licencia se actualizará automáticamente cuando el usuario inicie sesión por primera vez.

En ambos casos, se realizan automáticamente varias configuraciones. Estas se enumeran en la segunda y tercera columnas de la tabla siguiente.

Si cambia la información del usuario en Microsoft 365, puede actualizar [!INCLUDE[prod_short](includes/prod_short.md)] para reflejar el cambio. Según lo que desee actualizar, use una de las acciones en la página **Usuarios**. Las acciones se describen en las tres últimas columnas de la tabla siguiente.

> [!NOTE]
> Las acciones descritas en la siguiente tabla son precisas, sin embargo, la única que necesita es **Actualizar usuarios de Microsoft 365**, que se agregó para simplificar el proceso. Las otras acciones se eliminarán en una versión futura de [!INCLUDE[prod_short](includes/prod_short.md)].

|Qué pasa cuando:|Primer usuario, primer inicio de sesión|Obtener usuarios desde Microsoft 365|Actualizar usuarios desde Microsoft 365|Restaurar los grupos de usuarios predeterminados del usuario|Actualizar grupos de usuarios|Actualizar información del usuario desde Microsoft 365|
|-|-|-|-|-|-|-|
|Ámbito:|Usuario actual|Nuevos usuarios en Microsoft 365|Varios usuarios seleccionados|Usuario individual seleccionado (excepto el actual)|Varios usuarios seleccionados|Varios usuarios seleccionados|
|Cree el nuevo usuario y asigne el conjunto de permisos SUPER.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Actualice el usuario en función de la información en Microsoft 365: Estado, Nombre completo, Correo electrónico de contacto, Correo electrónico de autenticación.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Sincronice planes de usuario (licencias) con licencias y roles asignados en Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Agregue el usuario a grupos de usuarios de acuerdo con los planes de usuario actuales. Quite el conjunto de permisos SUPER para todos los usuarios que no sean el primer usuario en iniciar sesión y los [administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Se necesita al menos un SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Quita los grupos de usuarios y permisos asignados manualmente.|**X**<br /><br />Actualice las asignaciones de grupos de usuarios.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Administración de usuarios y licencias en implementaciones locales

Para las implementaciones locales, el número de licencias de usuario se especifica en el archivo de licencia (.flf). Cuando un administrador o el partner de Microsoft carga el archivo de licencia, el administrador puede especificar qué usuarios pueden iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].

Para las implementaciones locales, el administrador crea, edita y elimina usuarios directamente desde la página **Usuarios**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Para editar o eliminar un usuario en una implementación local

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.  
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **Eliminar**.

> [!NOTE]
> Para implementaciones locales, un administrador puede especificar cómo autenticar las credenciales de usuario en la instancia de [!INCLUDE[server](includes/server.md)]. Cuando crea un usuario, proporciona el tipo de credencial que está utilizando.
>
> Para obtener más información, consulte [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la ayuda de administración de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Consulte también

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Licencias en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Agregar usuarios para Microsoft 365 para empresas](/microsoft-365/admin/add-users/add-users)  
[Seguridad y protección en Business Central (contenido de administración)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]