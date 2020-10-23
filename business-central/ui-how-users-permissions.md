---
title: Crear usuarios según las licencias | Microsoft Docs
description: Describe cómo agregar usuarios a Business Central Online o local según las licencias.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df34469bc28b081800ddf583e7aa9cf08a15dc27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925652"
---
# <a name="create-users-according-to-licenses"></a>Crear usuarios de acuerdo con las licencias

En este artículo se describe cómo los administradores crean usuarios y definen quién puede iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)], y qué permisos se conceden a los diferentes tipos de usuario según las licencias.

Cuando crea usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede asignarles permisos específicos a través de conjuntos de permisos y organizar usuarios en grupos de usuarios. Los grupos de usuarios facilitan la administración de permisos para múltiples usuarios al mismo tiempo. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

> [!NOTE]
> El proceso de administración de usuarios y licencias varía según si [!INCLUDE[d365fin](includes/d365fin_md.md)] se implementa en línea o localmente. Para [!INCLUDE [prodshort](includes/prodshort.md)] en línea, debe agregar usuarios desde Microsoft 365. En implementaciones locales, puede crear, editar y eliminar usuarios directamente.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Administración de usuarios y licencias en implementaciones en línea

En la versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)], el número de usuarios se define mediante la suscripción y se agrega a su suscriptor en el Centro de socios de Microsoft, generalmente por parte de su socio de Microsoft. Para obtener más información, vea [Agregar un nuevo cliente](/partner-center/add-a-new-customer) y [Crear, suspender o cancelar suscripciones de clientes](/partner-center/create-a-new-subscription) en la ayuda del Centro de socios de Microsoft.

Para definir quién puede iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe asignar las licencias de producto asignarse a los usuarios de acuerdo con los roles que desempeñarán en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se puede hacer de las siguientes maneras:

- El administrador de Microsoft 365 de su empresa puede hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com). Para obtener más información, consulte [Agregar usuarios individualmente o en masa a Microsoft 365](https://aka.ms/CreateOffice365Users).  
- Un socio de Microsoft puede asignar licencias en el Centro de administración de Microsoft 365 o en el Centro de socios de Microsoft. Para obtener más información, vea [Tareas de administración de usuarios para cuentas de cliente](/partner-center/assign-licenses-to-users) en la ayuda del Centro de socios de Microsoft.

Para obtener más información, vea [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda de administración.

Cuando se asigna una licencia de [!INCLUDE[d365fin](includes/d365fin_md.md)] a los usuarios en Microsoft 365, se pueden importar en la página **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)], mediante la acción **Obtener nuevos usuarios desde Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Para agregar un usuario o actualizar información de usuario en Business Central

Use funciones de importación dedicadas para agregar nuevos usuarios o actualizar la información del usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde el Centro de administración de Microsoft 365.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.  
2. Elija la acción **Obtener nuevos usuarios de Office 365**.

    Si es la primera vez que agrega usuarios desde Microsoft 365, elija la acción **Obtener nuevos usuarios de Office 365**.  
3. Siga los pasos de la guía que aparece.

Los usuarios y la información de usuario nuevos de su suscripción a Microsoft 365 se agregarán a la página **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ahora puede asignar permisos y grupos de usuarios. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

Para obtener más información sobre la sincronización de la información de usuario con Microsoft 365, consulte la sección [Sincronización con Microsoft 365](#m365).

> [!NOTE]
> Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su Business Central para que pueda trabajar con usted en los datos fiscales. Para obtener más información, vea [Invitar a contable externo a Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Para cambiar la licencia asignada para un usuario

En ocasiones, es posible que deba cambiar la licencia asignada a un usuario. Por ejemplo, si decide usar el módulo Administración de servicios y, por lo tanto, necesita actualizar todas las licencias Essential a Premium. O si la responsabilidad de un usuario ha cambiado y necesita reemplazar una licencia Team Member a Essential.

1. Cambie la licencia en el Centro de administración de Microsoft 365. Para obtener más información, consulte [Agregar usuarios individualmente o en masa a Microsoft 365](https://aka.ms/CreateOffice365Users).
2. Inicie sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como administrador.
3. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
4. En la página **Usuarios**, seleccione la acción **Restaurar los grupos de usuarios predeterminados del usuario**.

Los usuarios se trasladarán a un grupo de usuarios adecuado y se actualizarán los conjuntos de permisos. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md).

> [!NOTE]
> Todos los usuarios deben tener asignada la misma licencia, Essential o Premium. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

### <a name="to-remove-a-users-access-to-the-system"></a>Para eliminar el acceso de un usuario al sistema

En implementaciones en línea, puede eliminar el acceso de un usuario a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se mantienen todas las referencias al usuario, pero el usuario no puede iniciar sesión y las sesiones activas para el usuario se detienen.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Abre la página **Ficha de usuario** para el usuario relevante y, a continuación, en el campo **Estado**, seleccione **Deshabilitado**.
3. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

También puede eliminar la licencia de un usuario en el Centro de administración de Microsoft 365. El usuario no puede iniciar sesión. Para obtener más información, vea [Quitar la asignación de las licencias de los usuarios](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Sincronización con Microsoft 365

Cuando asigna una licencia para [!INCLUDE[d365fin](includes/d365fin_md.md)] a un usuario en Microsoft 365, hay dos formas de crear el usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- El administrador puede agregar el usuario eligiendo la página **Actualizar usuarios de Office 365** en la página **Usuarios** como se describe en la sección [Para agregar un usuario o actualizar la información del usuario en Business Central ](#adduser).
- La información de la licencia se actualizará automáticamente cuando el usuario inicie sesión por primera vez.

En ambos casos, se realizan automáticamente varias configuraciones. Estas se enumeran en la segunda y tercera columnas de la tabla siguiente.

Si cambia la información del usuario en Microsoft 365, puede actualizar [!INCLUDE[d365fin](includes/d365fin_md.md)] para reflejar el cambio. Según lo que desee actualizar, use una de las acciones en la página **Usuarios**. Las acciones se describen en las tres últimas columnas de la tabla siguiente.

|Qué pasa cuando:|Primer usuario, primer inicio de sesión|Obtener usuarios desde Microsoft 365|Actualizar usuarios desde Microsoft 365|Restaurar los grupos de usuarios predeterminados del usuario|Actualizar grupos de usuarios|
|-|-|-|-|-|-|
|Ámbito:|Usuario actual|Nuevos usuarios en Microsoft 365|Varios usuarios seleccionados|Usuario individual seleccionado (excepto el actual)|Varios usuarios seleccionados|
|Cree el nuevo usuario y asigne el conjunto de permisos SUPER.<br /><br /><!--Platform-->|**X**|| | | |
|Actualice el registro de usuario en función de la información real en Microsoft 365: Estado, Nombre completo, Correo electrónico de contacto, Correo electrónico de autenticación.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Sincronice planes de usuario (licencias) con licencias y roles asignados en Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Agregue el usuario a grupos de usuarios de acuerdo con los planes de usuario actuales. Quite el conjunto de permisos SUPER para todos los usuarios que no sean el primer usuario en iniciar sesión y los [administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Se necesita al menos un SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Quita los grupos de usuarios y permisos asignados manualmente.|**X**<br /><br />Actualice las asignaciones de grupos de usuarios.|

## <a name="the-device-license"></a>La licencia de dispositivo

La licencia de dispositivo de Dynamics 365 Business Central permite que varios usuarios usen simultáneamente un dispositivo cubierto por la licencia. Por ejemplo, podría ser un punto de venta, taller o dispositivo de almacén. Cuando ha comprado un número de licencias de dispositivo, ese número máximo de usuarios asignado al grupo Usuarios de dispositivo de Dynamics 365 Business Central puede iniciar sesión simultáneamente. Para obtener más información, consulte la Guía de licencias de Microsoft Dynamics 365 Business Central. La guía está disponible para descargar en el sitio web de [Business Central](https://dynamics.microsoft.com/business-central/overview/).

El administrador de Microsoft 365 de su empresa o el socio de Microsoft pueden crear el grupo Usuarios de dispositivo de Dynamics 365 Business Central y agregar usuarios de dispositivo como miembros en el [Centro de administración de Microsoft 365](https://admin.microsoft.com/) o en [Azure Portal](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Limitaciones del usuario del dispositivo

Los usuarios con la licencia Dispositivo no pueden realizar las siguientes tareas en [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Configurar proyectos para que se ejecuten como tareas programadas en la cola de proyectos. Los usuarios del dispositivo son usuarios concurrentes y, por lo tanto, no podemos garantizar que el usuario involucrado esté presente en el sistema cuando se ejecuta una tarea, lo cual es obligatorio.

- Un usuario de dispositivo no puede ser el primer usuario que inicie sesión. Un usuario de tipo Administrador, Usuario completo o Contable externo debe ser el primero en iniciar sesión para poder configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda de administración.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Para crear un grupo de Usuarios de dispositivo de Dynamics 365 Business Central

1. En el Centro de administración de Microsoft 365, vaya a la página **Grupos**.
2. Elija la acción **Agregar un grupo**.
3. En la página **Elegir un tipo de grupo**, seleccione la acción **Seguridad** y, a continuación, seleccione la acción **Agregar**.
4. En la página **Conceptos básicos**, introduzca **Usuarios de dispositivos de Dynamics 365 Business Central** como el nombre del grupo.
  
   >[!NOTE]
   >El nombre del grupo debe estar escrito en inglés exactamente como se muestra en el paso 4, incluso si está utilizando otro idioma.
5. Elija el botón **Cerrar**.

> [!NOTE]
> También puede crear un grupo de tipo Microsoft 365. Para obtener más información, consulte [Comparar grupos](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Para agregar miembros al grupo

1. En el Centro de administración de Microsoft 365, actualice la página **Grupos** para que aparezca el nuevo grupo.
2. Seleccione el grupo **Usuarios de dispositivos de Dynamics 365 Business Central** y, a continuación, elija la acción **Ver todos y administrar miembros**.
3. Elija la acción **Agregar miembros**.
4. Seleccione los usuarios que desea agregar y, a continuación, elija el botón **Guardar**.
5. Seleccione el botón **Cerrar** tres veces.

Puede agregar tantos usuarios al grupo Usuarios de dispositivos de Dynamics 365 Business Central como necesite. Sin embargo, el número de dispositivos en los que los usuarios pueden iniciar sesión simultáneamente se define por el número de licencias de dispositivo adquiridas.

> [!NOTE]
> No es necesario asignar una licencia de [!INCLUDE[d365fin](includes/d365fin_md.md)] a los usuarios que son miembros del grupo Usuarios de dispositivos de Dynamics 365 Business Central.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Administración de usuarios y licencias en implementaciones locales

Para las implementaciones locales, el número de licencias de usuario se especifica en el archivo de licencia (.flf). Cuando un administrador o el partner de Microsoft carga el archivo de licencia, el administrador puede especificar qué usuarios pueden iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para las implementaciones locales, el administrador crea, edita y elimina usuarios directamente desde la página **Usuarios**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Para editar o eliminar un usuario en una implementación local

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.  
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **Eliminar**.

> [!NOTE]
> Para implementaciones locales, un administrador puede especificar cómo autenticar las credenciales de usuario en la instancia de [!INCLUDE[server](includes/server.md)]. Cuando crea un usuario, proporciona el tipo de credencial que está utilizando.
>
> Para obtener más información, consulte [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la ayuda de administración de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Agregar usuarios a Microsoft 365 para empresas](https://aka.ms/CreateOffice365Users)  
[Seguridad y protección en Business Central (contenido de administración)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
