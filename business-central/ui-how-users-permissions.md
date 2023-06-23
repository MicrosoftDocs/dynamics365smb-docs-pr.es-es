---
title: Crear usuarios de acuerdo con las licencias
description: Describe cómo agregar usuarios a Business Central Online o local según las licencias.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="create-users-according-to-licenses" />Crear usuarios de acuerdo con las licencias

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Este artículo describe cómo los administradores crean usuarios y definen quién puede iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)]. También verá cómo asignar permisos a diferentes usuarios según las licencias de sus productos.

Cuando crea usuarios en [!INCLUDE[prod_short](includes/prod_short.md)], les otorga permisos a través de conjuntos de permisos. También puede organizar a los usuarios en grupos de usuarios. Los grupos de usuarios facilitan la administración de permisos y otras configuraciones para múltiples usuarios al mismo tiempo. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

Para obtener más información sobre los diferentes tipos de licencias y cómo funcionan las licencias en [!INCLUDE[prod_short](includes/prod_short.md)], [descargue la Guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> El proceso de administración de usuarios y licencias varía según si [!INCLUDE[prod_short](includes/prod_short.md)] se implementa en línea o localmente. Para [!INCLUDE [prod_short](includes/prod_short.md)] Online, debe agregar usuarios desde Microsoft 365. En implementaciones locales, puede crear, editar y eliminar usuarios directamente.  

## <a name="manage-users-and-licenses-in-online-tenants" />Administrar usuarios y licencias en los suscriptores en línea

Las cuentas de usuario en [!INCLUDE[prod_short](includes/prod_short.md)] deben crearse primero en el centro de administración de Microsoft 365. Estas cuentas de usuario no son exclusivas de Business Central. Si se suscribe a otros planes, se pueden usar para iniciar sesión en otras aplicaciones, como Power BI. Para obtener información sobre cómo crear usuarios en el centro de administración de Microsoft 365, vaya a [Agregar usuarios en el centro de administración de Microsoft](/microsoft-365/admin/add-users/add-users).

Su suscripción a [!INCLUDE[prod_short](includes/prod_short.md)] en línea define el número de licencias de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] que se le permiten. Los usuarios se agregan a su suscriptor en el Centro de socios de Microsoft, generalmente por su socio de Microsoft. Para obtener más información, consulte [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Asigna licencias a los usuarios de acuerdo con el trabajo que cada usuario realizará en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede asignar licencias de distintas formas:

- El administrador de Microsoft 365 de su empresa puede hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com). Para obtener más información, vea [Agregar usuarios individualmente o en masa a Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un socio de Microsoft puede asignar licencias en el Centro de administración de Microsoft 365 o en el Centro de partners de Microsoft. Para obtener más información, vea [Tareas de administración de usuarios para cuentas de cliente](/partner-center/assign-licenses-to-users) en la ayuda del Centro de socios de Microsoft.

Para obtener más información, vea [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda de administración.

Una vez creadas las cuentas de usuario en el centro de administración de Microsoft 365, existen dos formas de importarlas a Business Central:

- Una cuenta de usuario se importa automáticamente cuando el usuario se registra en [!INCLUDE [prod_short](includes/prod_short.md)] la primera vez.

- El administrador puede importar usuarios eligiendo la acción  **Actualizar usuarios de Microsoft 365** en la página **Usuarios* .

Ambos enfoques tienen sus propias ventajas y puede usarlos simultáneamente. Cada enfoque permite a los administradores configurar proactivamente [!INCLUDE [prod_short](includes/prod_short.md)] para asignar los permisos de inicio, los grupos de usuarios y los perfiles de usuario. El uso de la acción **Actualizar usuarios desde Microsoft 365** brinda a los administradores más control para ajustar permisos, grupos de usuarios y perfiles. Es un enfoque ideal cuando está estableciendo [!INCLUDE [prod_short](includes/prod_short.md)] la primera vez, antes de que ningún usuario se registre, o al añadir un nuevo equipo de usuarios.

> [!NOTE]
> Después de agregar usuarios en el Centro de administración de Microsoft 365, le recomendamos que actualice la información de usuario en [!INCLUDE[prod_short](includes/prod_short.md)] tan pronto como sea posible. Mantener la información de los usuarios actualizada es fácil y ayuda a garantizar que las personas siempre puedan iniciar sesión. Para obtener más información, consulte [Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central](#adduser).<br>
>
> La actualización de la información del usuario es especialmente importante si ha personalizado conjuntos de permisos para la licencia. Si un nuevo usuario intenta iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] antes de agregarlo, es posible que no pueda hacerlo. Para obtener más información, consulte [Configurar permisos basados en licencias](#licensespermissions).
>
> Sin embargo, los usuarios que experimentan este problema en realidad no están bloqueados. Pueden usar la acción **Volver al inicio** o simplemente volver a iniciar sesión para resolver el problema.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Para más información, vea [Acceso de administrador delegado a Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="a-namelicensespermissionsaconfigure-permissions-based-on-licenses" /><a name="licensespermissions"></a>Configurar permisos basados en licencias

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Los administradores pueden configurar conjuntos de permisos y grupos de usuarios para cada licencia.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Por ejemplo, la licencia de uso común, *Miembro del equipo de Dynamics 365 Business Central*, tiene los siguientes conjuntos de permisos de forma predeterminada:

- LEER D365
- MIEMBRO DEL EQUIPO D365
- EDITAR EN EXCEL - VER
- EXPORTAR EXCEL DE INFORME
- LOCAL

Otros conjuntos de permisos se agregan automáticamente en función de los grupos de usuarios asignados a la licencia. Al crear un nuevo usuario basado en esta licencia, [!INCLUDE[prod_short](includes/prod_short.md)] asigna los conjuntos de permisos que se originan en los grupos de usuarios y los conjuntos de permisos de la licencia. Se asignan los mismos permisos iniciales al usuario si su cuenta de usuario se creó automáticamente en [!INCLUDE[prod_short](includes/prod_short.md)] o si el administrador usó la acción **Actualizar usuarios desde Microsoft 365** en la página **Usuarios**.

Si esta configuración predeterminada no es la correcta para un entorno en particular, el administrador puede cambiar esa configuración. Sin embargo, los permisos personalizados solo afectarán a los nuevos usuarios a los que se les asigne esa licencia. Los permisos para los usuarios existentes a los que se les asigna la licencia no se verán afectados.  

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de administrador.  
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de licencia** y luego elija el vínculo relacionado.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. En la página **Configuración de licencia** seleccione la licencia que desea personalizar y, a continuación, seleccione la acción **Configurar**.  
4. Elija el campo **Personalizar permisos** para activar la personalización y, a continuación, realice los cambios relevantes.  

    En nuestro ejemplo, el administrador quiere eliminar el permiso para editar en Excel, por lo que elimina el grupo de usuarios *Acción exportación Excel* de la licencia de miembro del equipo. En el futuro, los nuevos usuarios a los que se les asigne la licencia de miembro del equipo no tendrán la opción de exportar datos a Excel. Si la organización cambia de opinión sobre el tema, simplemente puede volver a la página **Configuración de licencia** y desactivar la personalización para ese tipo de licencia.  

> [!IMPORTANT]
> Esta personalización de permisos solo surtirá efecto para los nuevos usuarios a los que les asigne la licencia correspondiente. Los usuarios existentes no se actualizan. Recomendamos que personalice los permisos antes de comenzar a asignar licencias de usuarios en el Centro de administración de Microsoft 365.

### <a name="a-nameadduserato-add-users-or-update-user-information-and-license-assignments-in-business-central" /><a name="adduser"></a>Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central

Después de agregar usuarios o cambiar la información del usuario en el Centro de administración de Microsoft 365, puede importar rápidamente la información del usuario a [!INCLUDE[prod_short](includes/prod_short.md)]. La importación incluye asignaciones de licencias.  

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de administrador.
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.  
3. Elija **Actualizar usuarios desde Microsoft 365**.

> [!IMPORTANT]  
> Ejecutar la sincronización de usuarios desde Microsoft 365 mediante la guía **Actualizar usuarios desde Microsoft 365** requiere el conjunto de permisos SUPER.

> [!NOTE]
> La guía **Actualizar usuarios de Microsoft 365** no actualiza a los usuarios que no tienen asignada una licencia, como alguien que sea administrador global y administrador de Dynamics 365. Esos usuarios se actualizarán la próxima vez que inicien sesión en el entorno.

El siguiente paso para los usuarios recién creados es asignar grupos de usuarios y permisos. Vaya a [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md) para obtener información. Si está actualizando un usuario y la actualización incluye un cambio de licencia, los usuarios se asignarán al grupo de usuarios apropiado y sus conjuntos de permisos se actualizarán. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md).  

> [!NOTE]
> Todos los usuarios de un entorno deben tener asignada la misma licencia, Essentials o Premium. Para obtener más información sobre las licencias, visite el sitio web [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Para obtener más información sobre la sincronización de la información de usuario con Microsoft 365, vaya a la sección [Sincronización con Microsoft 365](#m365).

> [!NOTE]
> Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[prod_short](includes/prod_short.md)] para que pueda trabajar con usted en los datos fiscales. Para obtener más información, consulte [Invitar a un contable externo a Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system" />Para eliminar el acceso de un usuario al sistema

Puede eliminar el acceso de un usuario a [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Se conservan todas las referencias al usuario. Sin embargo, el usuario no puede iniciar sesión y las sesiones activas para el usuario se detienen.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Abra la página **Ficha de usuario** para el usuario relevante y, a continuación, en el campo **Estado**, seleccione **Deshabilitado**.
3. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

También puede eliminar la licencia de un usuario en el Centro de administración de Microsoft 365. El usuario no puede iniciar sesión. Para obtener más información, consulte [Quitar la asignación de las licencias de los usuarios](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="a-namem365asynchronization-with-microsoft-365" /><a name="m365"></a>Sincronización con Microsoft 365

Cuando asigna una licencia para [!INCLUDE[prod_short](includes/prod_short.md)] a un usuario en Microsoft 365, hay dos formas de crear el usuario en [!INCLUDE[prod_short](includes/prod_short.md)].  

- El administrador puede agregar el usuario eligiendo la página **Actualizar usuarios de Microsoft 365** en la página **Usuarios** como se describe en la sección [Para agregar un usuario o actualizar la información del usuario en Business Central](#adduser).
- La información de la licencia se actualizará automáticamente cuando el usuario inicie sesión por primera vez.

En ambos casos, se aplican automáticamente varias configuraciones. Estas configuraciones se enumeran en la segunda y tercera columnas de la tabla siguiente.

Si cambia la información del usuario en Microsoft 365, puede actualizar [!INCLUDE[prod_short](includes/prod_short.md)] para reflejar el cambio. Según lo que desee actualizar, use una de las acciones en la página **Usuarios**. Las acciones se describen en las dos últimas columnas de la tabla siguiente.

|Qué pasa cuando:|Primer usuario, primer inicio de sesión|Actualizar usuarios desde Microsoft 365|Restaurar los grupos de usuarios predeterminados del usuario|
|-|-|-|-|
|Ámbito:|Usuario actual|Varios usuarios seleccionados|Usuario individual seleccionado (excepto el actual)|
|Cree el nuevo usuario y asigne el conjunto de permisos SUPER.<br /><br /><!--Platform-->|**X**|**X** | | 
|Actualice el usuario en función de la información en Microsoft 365: Estado, Nombre completo, Correo electrónico de contacto, Correo electrónico de autenticación.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Sincronice planes de usuario (licencias) con licencias y roles asignados en Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Agregue el usuario a grupos de usuarios de acuerdo con los planes de usuario actuales. Quite el conjunto de permisos SUPER para todos los usuarios que no sean el primer usuario en iniciar sesión y los [administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Se necesita al menos un SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Quita los grupos de usuarios y permisos asignados manualmente.|

Los usuarios pueden acceder a los registros de [!INCLUDE[prod_short](includes/prod_short.md)] en Teams usando solo su licencia de Microsoft 365. Cuando el acceso está habilitado para un entorno, la sincronización mediante la acción **Actualizar usuarios de Microsoft 365** no incluirá a los usuarios que solo tienen una licencia Microsoft 365 . Para incluir a estos usuarios en la sincronización, primero debe actualizar la configuración del entorno asignando un grupo de seguridad que contenga usuarios con una licencia de [!INCLUDE[prod_short](includes/prod_short.md)] y usuarios con solo una licencia de Microsoft 365.

Obtenga información sobre cómo proteger el acceso a los entornos mediante grupos de seguridad en [Administrar el acceso mediante grupos de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Obtenga una descripción general de cómo acceder a [!INCLUDE[prod_short](includes/prod_short.md)] en Teams con licencias de Microsoft 365 en [admin-access-with-m365-license](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments" />Administrar usuarios y licencias en implementaciones locales

Para las implementaciones locales, el número de licencias de usuario se especifica en el archivo de licencia (.bclicense or .flf). Cuando un administrador o el partner de Microsoft carga el archivo de licencia, puede especificar qué usuarios pueden iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].

Para las implementaciones locales, el administrador crea, edita y elimina usuarios directamente desde la página **Usuarios**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment" />Para editar o eliminar un usuario en una implementación local

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.  
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **Eliminar**.

> [!NOTE]
> Para implementaciones locales, un administrador puede especificar cómo autenticar las credenciales de usuario en la instancia de [!INCLUDE[server](includes/server.md)]. Cuando crea un usuario, proporciona el tipo de credencial que está utilizando.
>
> Para obtener más información, consulte [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la ayuda de administración de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also" />Consulte también

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Licencias en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Agregar usuarios para Microsoft 365 para empresas](/microsoft-365/admin/add-users/add-users)  
[Seguridad y protección en Business Central (contenido de administración)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Asignar un Id. de telemetría a usuarios](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
