---
title: Asignar o editar los permisos de usuario | Documentos de Microsoft
description: Describe cómo agregar usuarios de Office 365 a Business Central y asignarles permisos, derechos de acceso y opciones de seguridad.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 01/06/2020
ms.author: sgroespe
ms.openlocfilehash: b9fbf0b2793c6239f3a1a416230d4afb17bdb5c6
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943238"
---
# <a name="create-users-according-to-licenses"></a>Crear usuarios de acuerdo con las licencias
A continuación se describe cómo usted, como administrador, crea usuarios y define quién puede iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)], y qué derechos fundamentales tienen los diferentes tipos de usuario según las licencias.

Cuando se crean los usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede proceder a asignar permisos específicos a los usuarios a través de conjuntos de permisos y organizar a los usuarios en grupos de usuarios para una fácil administración de los permisos. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

> [!NOTE]
> El proceso de administración de usuarios y licencias varía según si su solución está implementada en línea o localmente. Por ejemplo, en la implementaciones en línea, solo puede deshabilitar y habilitar un usuario una vez agregado a [!INCLUDE[d365fin](includes/d365fin_md.md)]. En implementaciones locales, puede crear, editar y eliminar usuarios.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Administración de usuarios y licencias en implementaciones en línea
En [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el número de usuarios se define mediante la suscripción y se agrega a su suscriptor en el Centro de socios de Microsoft, generalmente por parte de su socio de Microsoft. Para obtener más información, vea [Agregar un nuevo cliente](https://docs.microsoft.com/partner-center/add-a-new-customer) y [Crear, suspender o cancelar suscripciones de clientes](https://docs.microsoft.com/partner-center/create-a-new-subscription) en la ayuda del Centro de socios de Microsoft.

Para definir quién puede iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)], las licencias de producto deben asignarse a los usuarios de acuerdo con los roles que desempeñarán en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se puede hacer de las siguientes maneras:
- El administrador de Office 365 de su empresa puede hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com). Para obtener más información, vea [Agregar usuarios individualmente o en masa a Office 365](https://aka.ms/CreateOffice365Users).  
- Un socio de Microsoft puede asignar licencias en el Centro de administración de Microsoft 365 o en el Centro de socios de Microsoft. Para obtener más información, vea [Tareas de administración de usuarios para cuentas de cliente](https://docs.microsoft.com/partner-center/assign-licenses-to-users) en la ayuda del Centro de socios de Microsoft.

Para obtener más información, vea [Administración de Business Central en línea](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda para desarrolladores y profesionales de TI.

Cuando los usuarios con una licencia de [!INCLUDE[d365fin](includes/d365fin_md.md)] se crean en Office 365, se pueden importar en la página **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Obtener nuevos usuarios desde Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Agregar un usuario en Business Central
Para agregar usuarios desde el Centro de administración de Microsoft 365 a [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, utilice una función de importación dedicada.  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Elija la acción **Obtener nuevos usuarios de Office 365**.

Cualquier usuario nuevo que se haya creado para su suscripción a Office 365 se agregará a la página **Usuarios**. A los usuarios se les asignan conjuntos de permisos de acuerdo con la licencia asignada al usuario en Office 365. Después podrá continuar con la asignación de permisos más detallados a usuarios y la organización en grupos de usuarios para facilitar la administración de permisos. Para obtener más información, vea [Para asignar conjuntos de permisos a los usuarios](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su Business Central para que pueda trabajar con usted en los datos fiscales. Para obtener más información, vea [Invitar a contable externo a Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Para eliminar el acceso de un usuario al sistema
En las implementaciones en línea, puede eliminar el acceso de un usuario al sistema configurando el campo **Estado** en **Deshabilitado**. Todas las referencias al usuario se conservarán, pero el usuario ya no podrá iniciar sesión en el sistema y finalizarán las sesiones activas para el usuario.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Abre la página **Ficha de usuario** para el usuario relevante y, a continuación, en el campo **Estado**, seleccione **Deshabilitado**.
3. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

Además de deshabilitar a un usuario, puede anular la asignación de la licencia de un usuario en el Centro de administración de Microsoft 365. El usuario no puede iniciar sesión. Para obtener más información, vea [Anular la asignación de las licencias de los usuarios](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Para cambiar la licencia asignada para un usuario
En ocasiones, es posible que deba cambiar la licencia asignada a un usuario. Por ejemplo, si decide usar el módulo Administración de servicios y, por lo tanto, necesita actualizar todas las licencias Essential a Premium. O si la responsabilidad de un usuario ha cambiado y necesita reemplazar una licencia Team Member a Essential.

1. Cambie la licencia en el Centro de administración de Microsoft 365. Para obtener más información, vea [Agregar usuarios individualmente o en masa a Office 365](https://aka.ms/CreateOffice365Users).
2. Inicie sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como administrador.
3. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
4. En la página **Usuarios**, seleccione la acción **Actualizar todos los grupos de usuarios**.

Los usuarios se trasladarán a un grupo de usuarios adecuado y se actualizarán los conjuntos de permisos. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Todos los usuarios habituales de una solución deben tener asignada la misma licencia, Essential o Premium.
> Para obtener información acerca de las licencias, consulte la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Sincronización con Office 365
Cuando se asigna una licencia a un usuario en Office 365, hay dos formas de crear el usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El sistema lo hará automáticamente cuando el usuario inicie sesión por primera vez, o el administrador puede agregar al usuario seleccionando la acción **Obtener usuarios desde Office 365** en la página **Usuarios**.

En ambos casos, se realizan automáticamente varias configuraciones adicionales. Estas se enumeran en la segunda y tercera columnas de la tabla siguiente.

Si cambia el usuario en Office 365 posteriormente, y necesita sincronizar los cambios con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede usar diferentes acciones en la página **Usuarios** dependiendo de qué es exactamente lo que desea sincronizar. Estas se enumeran en las tres últimas columnas de la tabla siguiente.

|Qué pasa cuando:|Primer inicio de sesión|Obtener usuarios desde Office 365|Actualizar usuarios desde Office 365|Restaurar los grupos de usuarios predeterminados del usuario|Actualizar grupos de usuarios|
|-|-|-|-|-|-|
|Ámbito:|Usuario actual|Nuevos usuarios en Office 365|Varios usuarios seleccionados|Usuario individual seleccionado (excepto el actual)|Varios usuarios seleccionados|
|Cree el nuevo usuario y asigne el conjunto de permisos SUPER.<br /><br />Plataforma|**X**|**X**| | | |
|Actualice el registro de usuario en función de la información real en Office 365 : Estado, Nombre completo, Correo electrónico de contacto, Correo electrónico de autenticación.<br /><br />Codeunit " Usuario de Azure AD Graph".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Sincronice planes de usuario (licencias) con licencias y roles asignados en Office 365.<br /><br />Codeunit " Usuario de Azure AD Graph".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Agregue el usuario a grupos de usuarios de acuerdo con los planes de usuario actuales. Revoque el conjunto de permisos SUPER. (Se necesita al menos un SUPER. No revoque desde [administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration)).<br /><br />Codeunit "Administrador de permisos". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Sobrescribir: elimine al usuario de otros grupos. Elimine conjuntos de permisos asignados manualmente.|**X**<br /><br />Aditivo: mantenga intactos la pertenencia actual en el grupo de usuarios y los conjuntos de permisos asignados. Agregue únicamente el usuario a los grupos si es necesario.|

## <a name="the-device-license"></a>La licencia de dispositivo
Con la licencia de dispositivo de Dynamics 365 Business Central, varios usuarios pueden utilizar un dispositivo con licencia Dispositivo para operar un dispositivo de punto de venta, un dispositivo de planta o un dispositivo de almacén. Para obtener más información, consulte la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

La licencia Dispositivo se implementa como un modelo de usuario concurrente. Cuando ha comprado X número de licencias de dispositivo, hasta X número de usuarios del grupo designado llamado Usuarios* de dispositivo de Dynamics 365 Business Central pueden iniciar sesión simultáneamente.

El administrador de Office 365 de su empresa o el socio de Microsoft debe crear el grupo de dispositivos designado y agregar usuarios de dispositivos como miembros de ese grupo. Pueden hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com/) o en [Azure Portal](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Limitaciones del usuario del dispositivo
Los usuarios con la licencia Dispositivo no pueden realizar las siguientes tareas en [!INCLUDE[d365fin](includes/d365fin_md.md)]:

-   Configurar proyectos para que se ejecuten como tareas programadas en la cola de proyectos. Los usuarios del dispositivo son usuarios concurrentes y, por lo tanto, no podemos garantizar que el usuario involucrado esté presente en el sistema cuando se ejecuta una tarea, lo cual es obligatorio.

-   Un usuario de dispositivo no puede ser el primer usuario que inicie sesión. Un usuario de tipo Administrador, Usuario completo o Contable externo debe ser el primero en iniciar sesión para poder configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Para crear un grupo de Usuarios de dispositivo de Dynamics 365 Business Central
1.  En el Centro de administración de Microsoft 365, vaya a la página **Grupos**.
2.  Elija la acción **Agregar un grupo**.
3.  En la página **Elegir un tipo de grupo**, seleccione la acción **Seguridad** y, a continuación, seleccione la acción **Agregar**.
4.  En la página **Conceptos básicos**, escriba *Usuarios de dispositivos de Dynamics 365 Business Central* como el nombre del grupo.

    > [!Note]
    > El nombre del grupo debe escribirse exactamente igual que arriba, también en una configuración no esté en inglés.
5. Elija el botón **Cerrar**.

> [!NOTE]
> También puede crear un grupo de tipo Office 365. Para obtener más información, consulte [Comparar grupos](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Para agregar miembros al grupo
1.  En el Centro de administración de Microsoft 365, actualice la página **Grupos** para que aparezca el nuevo grupo.
2.  Seleccione el grupo **Usuarios de dispositivos de Dynamics 365 Business Central** y, a continuación, elija la acción **Ver todos y administrar miembros**.
3.  Elija la acción **Agregar miembros**.
4.  Seleccione los usuarios que desea agregar y, a continuación, elija el botón **Guardar**.
5.  Seleccione el botón **Cerrar** tres veces.

Puede agregar tantos usuarios al grupo Usuarios de dispositivos de Dynamics 365 Business Central como necesite. El número de dispositivos a los que los usuarios pueden acceder simultáneamente se define por el número de licencias de dispositivo adquiridas.

> [!NOTE]
> No es necesario asignar una licencia de [!INCLUDE[d365fin](includes/d365fin_md.md)] a los usuarios que son miembros del grupo Usuarios de dispositivos de Dynamics 365 Business Central.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Administración de usuarios y licencias en implementaciones locales
Para las implementaciones locales, se especifica una cantidad de usuarios con licencia en el archivo de licencia (.flf). Cuando el administrador o el socio de Microsoft carga el archivo de licencia, el administrador puede especificar qué usuarios pueden iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para las implementaciones locales, el administrador crea, edita y elimina usuarios directamente desde la página **Usuarios**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Para editar o eliminar un usuario local
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.    
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **eliminar**.

> [!NOTE]
> Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios. Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)].<br /><br />
> Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Agregar usuarios para Office 365 para empresas](https://aka.ms/CreateOffice365Users)  
[Guía sobre licencias de Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)  
[Seguridad y protección en Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) en Ayuda para desarrolladores y profesionales de TI
