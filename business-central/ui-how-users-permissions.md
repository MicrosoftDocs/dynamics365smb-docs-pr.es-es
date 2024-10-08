---
title: Crear usuarios de acuerdo con las licencias
description: Describe cómo agregar usuarios a Business Central Online o local según las licencias.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800_Primary, 9807_Primary, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173, 774_Primary'
ms.date: 05/03/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-users-according-to-licenses"></a>Crear usuarios de acuerdo con las licencias

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Este artículo describe cómo los administradores crean usuarios y definen quién puede iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)]. Este artículo también describe cómo asignar permisos a diferentes usuarios según las licencias de sus productos.

Cuando crea usuarios en [!INCLUDE[prod_short](includes/prod_short.md)], les otorga permisos a través de conjuntos de permisos. También puede organizar a los usuarios en grupos de usuarios. Los grupos de usuarios facilitan la administración de permisos y otras configuraciones para múltiples usuarios al mismo tiempo. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

Para obtener más información sobre los diferentes tipos de licencias y cómo funcionan las licencias en [!INCLUDE[prod_short](includes/prod_short.md)], [descargue la Guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> El proceso de administración de usuarios y licencias varía según si [!INCLUDE[prod_short](includes/prod_short.md)] se implementa en línea o localmente. Para [!INCLUDE [prod_short](includes/prod_short.md)] Online, debe agregar usuarios desde Microsoft 365. En implementaciones locales, puede crear, editar y eliminar usuarios directamente.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Administrar usuarios y licencias en los suscriptores en línea

Las cuentas de usuario en [!INCLUDE[prod_short](includes/prod_short.md)] deben crearse primero en el centro de administración de Microsoft 365. Estas cuentas de usuario no son exclusivas de [!INCLUDE [prod_short](includes/prod_short.md)]. Si se suscribe a otros planes, se pueden usar para iniciar sesión en otras aplicaciones, como Power BI. Para obtener información sobre cómo crear usuarios en el centro de administración de Microsoft 365, vaya a [Agregar usuarios en el centro de administración de Microsoft](/microsoft-365/admin/add-users/add-users).

Su suscripción a [!INCLUDE[prod_short](includes/prod_short.md)] en línea define el número de licencias de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] que se le permiten. Los usuarios se agregan a su suscriptor en el Centro de socios de Microsoft, generalmente por su socio de Microsoft. Para obtener más información, consulte [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Asigna licencias a los usuarios de acuerdo con el trabajo que cada usuario realiza en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede asignar licencias de distintas formas:

- El administrador de Microsoft 365 de su empresa puede hacerlo en el [Centro de administración de Microsoft 365](https://admin.microsoft.com). Para obtener más información, vea [Agregar usuarios individualmente o en masa a Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Un socio de Microsoft puede asignar licencias en el Centro de administración de Microsoft 365 o en el Centro de partners de Microsoft. Para obtener más información, vea [Tareas de administración de usuarios para cuentas de cliente](/partner-center/assign-licenses-to-users) en la ayuda del Centro de socios de Microsoft.

Para obtener más información, vea [Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) en la ayuda de administración.

Una vez creadas las cuentas de usuario en el centro de administración de Microsoft 365, existen dos formas de importarlas a [!INCLUDE [prod_short](includes/prod_short.md)]:

- Una cuenta de usuario se importa automáticamente cuando el usuario se registra en [!INCLUDE [prod_short](includes/prod_short.md)] la primera vez.

   > [!NOTE]
   > Después de que un usuario inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] en línea, no puede eliminarlo.

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

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Configurar permisos basados en licencias

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Los administradores pueden configurar conjuntos de permisos y grupos de usuarios para cada licencia.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Por ejemplo, la licencia de uso común, *Miembro del equipo de Dynamics 365 Business Central*, tiene los siguientes conjuntos de permisos de forma predeterminada:

- LEER D365
- MIEMBRO DEL EQUIPO D365
- EDITAR EN EXCEL - VER
- EXPORTAR EXCEL DE INFORME
- LOCAL

Otros conjuntos de permisos se agregan automáticamente en función de los grupos de usuarios asignados a la licencia. Al crear un nuevo usuario basado en esta licencia, [!INCLUDE[prod_short](includes/prod_short.md)] asigna los conjuntos de permisos que se originan en los grupos de usuarios y los conjuntos de permisos de la licencia. Se asignan los mismos permisos iniciales al usuario si su cuenta de usuario se creó automáticamente en [!INCLUDE[prod_short](includes/prod_short.md)] o si el administrador usó la acción **Actualizar usuarios desde Microsoft 365** en la página **Usuarios**.

Si esta configuración predeterminada no es la correcta para un entorno en particular, el administrador puede cambiar esa configuración. Sin embargo, los permisos personalizados solo afectan a los nuevos usuarios a los que se les asigne esa licencia. Los permisos para los usuarios existentes a los que se les asigna la licencia no se ven afectados.  

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de administrador.  
2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Configuración de licencia** y luego elija el vínculo relacionado.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. En la página **Configuración de licencia** seleccione la licencia que desea personalizar y, a continuación, seleccione la acción **Configurar**.  
4. Elija el campo **Personalizar permisos** para activar la personalización y, a continuación, realice los cambios.  

    En nuestro ejemplo, el administrador quiere eliminar el permiso para editar en Excel, por lo que elimina el grupo de usuarios *Acción exportación Excel* de la licencia de miembro del equipo. En el futuro, los nuevos usuarios a los que se les asigne la licencia de miembro del equipo no podrán exportar datos a Excel. Si la organización cambia de opinión sobre el tema, simplemente puede volver a la página **Configuración de licencia** y desactivar la personalización para ese tipo de licencia.  

> [!IMPORTANT]
> Esta personalización de permisos solo surtirá efecto para los nuevos usuarios a los que les asigne la licencia correspondiente. Los usuarios existentes no se actualizan. Recomendamos que personalice los permisos antes de comenzar a asignar licencias de usuarios en el Centro de administración de Microsoft 365.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central

Después de agregar usuarios o cambiar la información del usuario en el Centro de administración de Microsoft 365, puede importar rápidamente la información del usuario a [!INCLUDE[prod_short](includes/prod_short.md)]. La importación incluye asignaciones de licencias.  

> [!TIP]
> Si necesita actualizar la información del usuario y tiene muchos usuarios, puede usar el panel de filtro para reducir la lista. Puede filtrar información básica como el nombre de usuario o establecer filtros más técnicos, como la identificación de seguridad del usuario.

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con una cuenta de administrador.
2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.  
3. Elija **Actualizar usuarios desde Microsoft 365**.

> [!IMPORTANT]  
> Ejecutar la sincronización de usuarios desde Microsoft 365 mediante la guía **Actualizar usuarios desde Microsoft 365** requiere el conjunto de permisos SUPER.

> [!NOTE]
> La opción  **Actualizar usuarios de Microsoft 365** guía no actualiza a los usuarios que no tienen asignada una licencia, como alguien que es administrador de Dynamics 365 [.](/entra/identity/role-based-access-control/permissions-reference#dynamics-365-administrator) Esos usuarios se actualizarán la próxima vez que inicien sesión en ambiente.

El siguiente paso para los usuarios recién creados es asignar grupos de usuarios y permisos. Vaya a [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md) para obtener información. Si actualiza un usuario con un cambio de licencia, [!INCLUDE [prod_short](includes/prod_short.md)] asigna los usuarios al grupo de usuarios adecuado y actualiza sus conjuntos de permisos. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md).  

> [!NOTE]
> Con el primer lanzamiento de versiones de 2024, un usuario de licencia Premium puede iniciar sesión en una empresa donde el campo **Experiencia de usuario** está configurado en **Esenciales** en la página **Información de la empresa**. Sin embargo, el usuario Premium no puede utilizar ninguna de las funciones que proporciona la licencia Premium. Esto no funciona en sentido contrario. Los usuarios que tienen una licencia Essentials no pueden iniciar sesión en una empresa en la que la **Experiencia del usuario** está configurada como **Premium** en la página **Información de la empresa**. Para obtener más información sobre las licencias, visite el sitio web [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[prod_short](includes/prod_short.md)] para que pueda trabajar con usted en los datos fiscales. Para obtener más información, consulte [Invitar a un contable externo a Business Central](finance-accounting.md#inviteaccountant).

Para obtener más información sobre la sincronización de la información de usuario con Microsoft 365, vaya a la sección [Sincronización con Microsoft 365](#m365).

> [!NOTE]
> Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[prod_short](includes/prod_short.md)] para que pueda trabajar con usted en los datos fiscales. Para obtener más información, consulte [Invitar a un contable externo a Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Para eliminar el acceso de un usuario al sistema

Puede eliminar el acceso de un usuario a [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Se conservan todas las referencias al usuario. Sin embargo, el usuario no puede iniciar sesión y las sesiones activas para el usuario se detienen.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Abra la página **Ficha de usuario** para el usuario relevante y, a continuación, en el campo **Estado**, seleccione **Deshabilitado**.
3. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

También puede eliminar la licencia de un usuario en el Centro de administración de Microsoft 365. El usuario no puede iniciar sesión. Para obtener más información, consulte [Quitar la asignación de las licencias de los usuarios](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Sincronización con Microsoft 365

Cuando asigna una licencia para [!INCLUDE[prod_short](includes/prod_short.md)] a un usuario en Microsoft 365, hay dos formas de crear el usuario en [!INCLUDE[prod_short](includes/prod_short.md)].  

- El administrador puede agregar el usuario eligiendo la página **Actualizar usuarios de Microsoft 365** en la página **Usuarios** como se describe en la sección [Para agregar un usuario o actualizar la información del usuario en Business Central](#adduser).
- La información de la licencia se actualiza automáticamente cuando el usuario inicie sesión por primera vez.

En ambos casos, se aplican automáticamente varias configuraciones. Estas configuraciones se enumeran en la segunda y tercera columnas de la tabla siguiente.

Si cambia la información del usuario en Microsoft 365, puede actualizar [!INCLUDE[prod_short](includes/prod_short.md)] para reflejar el cambio. Según lo que desee actualizar, use una de las acciones en la página **Usuarios**. Las acciones se describen en las dos últimas columnas de la tabla siguiente.

|Qué pasa cuando:|Primer usuario, primer inicio de sesión|Actualizar usuarios desde Microsoft 365|Restaurar los grupos de usuarios predeterminados del usuario|
|-|-|-|-|
|Ámbito:|Usuario actual|Varios usuarios seleccionados|Usuario individual seleccionado (excepto el actual)|
|Cree el nuevo usuario y asigne el conjunto de permisos SUPER.<br /><br /><!--Platform-->|**X**|**X** | | 
|Actualice el usuario en función de la información en Microsoft 365: Estado, Nombre completo, Correo electrónico de contacto, Correo electrónico de autenticación.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Sincronice planes de usuario (licencias) con licencias y roles asignados en Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Agregue el usuario a grupos de usuarios de acuerdo con los planes de usuario actuales. Quite el conjunto de permisos SUPER para todos los usuarios que no sean el primer usuario en iniciar sesión y los [administradores](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Se necesita al menos un SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Quita los grupos de usuarios y permisos asignados manualmente.|

Los usuarios pueden acceder a los registros de [!INCLUDE[prod_short](includes/prod_short.md)] en Teams usando solo su licencia de Microsoft 365. Cuando el acceso está habilitado para un entorno, la sincronización mediante la acción **Actualizar usuarios de Microsoft 365** omitirá a los usuarios que solo tienen una licencia Microsoft 365. Para incluir a estos usuarios en la sincronización, primero debe actualizar la configuración del entorno asignando un grupo de seguridad que contenga usuarios con una licencia de [!INCLUDE[prod_short](includes/prod_short.md)] y usuarios con solo una licencia de Microsoft 365.

Obtenga información sobre cómo proteger el acceso a los entornos mediante grupos de seguridad en [Administrar el acceso mediante grupos de Microsoft Entra](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Obtenga una descripción general de cómo acceder a [!INCLUDE[prod_short](includes/prod_short.md)] en Teams con licencias de Microsoft 365 en [admin-access-with-m365-license](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Administrar usuarios y licencias en implementaciones locales

Para las implementaciones locales, el número de licencias de usuario se especifica en el archivo de licencia (.bclicense or .flf). Cuando un administrador o el partner de Microsoft carga el archivo de licencia, puede especificar qué usuarios pueden iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].

Para las implementaciones locales, el administrador crea, edita y elimina usuarios directamente desde la página **Usuarios**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Para editar o eliminar un usuario en una implementación local

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.  
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **Eliminar**.

> [!NOTE]
> Para implementaciones locales, un administrador puede especificar cómo autenticar las credenciales de usuario en la instancia de [!INCLUDE[server](includes/server.md)]. Cuando crea un usuario, proporciona el tipo de credencial que está utilizando.
>
> Para obtener más información, consulte [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la ayuda de administración de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="analyze-user-status-by-license-type"></a>Analizar el estado del usuario por tipo de licencia

Puede usar la función **Análisis de los datos** para analizar datos en la página [Usuarios](https://businesscentral.dynamics.com/?page=9800). No es necesario ejecutar un informe ni abrir otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Usuarios por estado" o "Usuarios por tipo de licencia", o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

### <a name="user-analysis-scenarios"></a>Escenarios de análisis de usuarios

Las siguientes secciones proporcionan ejemplos de escenarios en los que el análisis de la lista de usuarios puede ayudarle a supervisar el estado de sus usuarios.

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Usuarios por estado](#example-users-by-status) | Vea una lista de usuarios según su estado (habilitado/deshabilitado). | [Usuarios](https://businesscentral.dynamics.com/?page=9800) | **Estado**, **Nombre de usuario**, **Nombre completo**, **Correo electrónico de autorización** y **Tipo de licencia**. |
| [Usuarios por tipo de licencia](#example-users-by-license-type) | Vea una lista de usuarios según su tipo de licencia. | [Usuarios](https://businesscentral.dynamics.com/?page=9800) | **Tipo de licencia**, **Estado**, **Nombre de usuario**, **Nombre completo** y **Correo electrónico de autorización**. |

### <a name="example-users-by-status"></a>Ejemplo: Usuarios por estado

Para analizar a los usuarios por estado, siga estos pasos:

1. Abra la lista [Usuarios](https://businesscentral.dynamics.com/?page=9800) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: icono para activar el modo de análisis.
1. En el menú **Columnas**, elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre los campos **Estado** (usuario habilitado/deshabilitado) y **Tipo de licencia** al área **Grupos de filas**.
1. Elija los campos **Nombre de usuario**, **Nombre completo** y **Correo electrónico de autorización**.
1. Cambie el nombre de su pestaña de análisis a **Usuarios por estado** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source=" media/data-analysis-users.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Entradas del registro de cambios (Quién ha cambiado qué datos y cuándo)." lightbox="media/data-analysis-users.png":::

### <a name="example-users-by-license-type"></a>Ejemplo: Usuarios por tipo de licencia

Para analizar a los usuarios por tipo de licencia, siga estos pasos:

1. Abra la lista [Usuarios](https://businesscentral.dynamics.com/?page=9800) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: icono para activar el modo de análisis.
1. En el menú **Columnas**, elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre los campos **Tipo de licencia** y **Estado** (usuario habilitado/deshabilitado) al área **Grupos de filas**.
1. Elija los campos **Nombre de usuario**, **Nombre completo** y **Correo electrónico de autorización**.
1. Cambie el nombre de su pestaña de análisis a **Usuarios por tipo de licencia** o algo que describa este análisis.

## <a name="see-also"></a>Consulte también

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administrar perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Licencias en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Agregar usuarios para Microsoft 365 para empresas](/microsoft-365/admin/add-users/add-users)  
[Seguridad y protección en Business Central (contenido de administración)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Asignar un Id. de telemetría a usuarios](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
