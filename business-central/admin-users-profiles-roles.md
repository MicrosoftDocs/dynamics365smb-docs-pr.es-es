---
title: Administrar usuarios y roles
description: Obtener información sobre cómo administrar perfiles de usuari y áreas de trabajo en Business Central. Los perfiles permiten a los administradores definir y gestionar de forma centralizada lo que los usuarios pueden ver y hacer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# <a name="manage-user-profiles" />Administración de perfiles de usuario

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Asigne todos los usuarios a perfiles que reflejen:

* Su rol comercial
* El departamento en el que trabajan
* Otro tipo de categorización

Los perfiles permiten a los administradores definir y gestionar de forma centralizada qué tipos de usuarios pueden acceder en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> El uso de negocio típico de un perfil es un rol. Por lo tanto, un perfil se llama *Perfil (rol)* en la interfaz de usuario.

Como administrador, usted crea y administra perfiles en la página **Perfiles (roles)**. Cada perfil tiene una tarjeta donde administra la configuración para el rol relacionado. Por ejemplo, la tarjeta contiene la siguiente información:

* Nombre de rol
* Ajustes de usuario
* El área de trabajo que utiliza el perfil

Para obtener más información sobre la configuración de usuario y las áreas de trabajo, consulte [Cambiar la configuración básica](ui-change-basic-settings.md).

Para poder administrar los perfiles de los usuarios, los usuarios se deben crear y agregar a través de Centro de administración de Microsoft 365. A continuación, puede asignar permisos a cada usuario o grupo de usuarios. Los permisos definen las características a las que pueden acceder los usuarios. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="page-customization" />Personalización de página

Puede personalizar los diseños de página para un perfil de modo que todos los usuarios asignados al perfil vean las páginas personalizadas. Como administrador, personalice las páginas utilizando la misma funcionalidad que los usuarios cuando realizan la personalización. Para obtener más información, consulte [Personalizar las páginas para los perfiles](ui-personalization-manage.md).

## <a name="to-create-a-profile" />Para crear un perfil

Si no puede copiar un perfil existente, puede crear uno nuevo manualmente.

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Perfiles (roles)** y luego elija el enlace relacionado.  
2. En la página **Perfiles (roles)**, elija la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Si desea que un perfil en particular esté disponible solo para usuarios muy específicos, puede configurar el campo **Descripción** a `Navigation menu only.`. De esta forma, el perfil queda excluido de la lista de roles disponibles en **Mi configuración**.

## <a name="to-copy-a-profile" />Para copiar un perfil

Para ahorrar tiempo, puede crear un nuevo perfil copiando uno existente. Copie uno que tenga una configuración similar al que desea crear.

> [!NOTE]
> Cuando copia un perfil, también se copian todas las personalizaciones de página involucradas, tanto las creadas por el usuario como las derivadas de las extensiones.

1. En la página **Perfiles (roles)**, seleccione la línea para el perfil que desea copiar y luego elija la acción **Copiar perfil**.
2. Complete los campos **Id. perfil** y **Nombre para mostrar** y luego elija el botón **Aceptar**.
3. En la página **Perfiles (roles)**, abra la tarjeta de perfil recién creada y edite otros campos según sea necesario.

## <a name="to-edit-a-profile" />Para editar un perfil

Puede editar un perfil cambiando los campos en la página **Perfil (rol)**. Sin embargo, los cambios no serán visibles para el usuario asignado al perfil hasta que cierre la sesión y vuelva a iniciarla.

> [!Caution]
> No cambie el nombre de un perfil mientras los usuarios asignados al perfil estén conectados, ya que los usuarios pueden experimentar que el producto se congele y debe reiniciarse.

## <a name="to-assign-a-profile-to-a-user" />Para asignar un perfil a un usuario

Los usuarios pueden asignarse un rol (que representa un perfil) eligiendo el campo **Rol** en la página **Mi configuración**. Como administrador, puede hacer lo mismo a través de la página **Perfiles (roles)**.

1. En la página **Perfiles (roles)**, seleccione el perfil que desea asignar y luego elija la acción **Lista personalización usuario**.
2. En la página **Personalizaciones del usuario**, seleccione el usuario al que desea asignar el perfil y luego elija la acción **Editar**.
3. En el campo **Id. perfil**, seleccione el perfil relevante.

> [!NOTE]
> Si asigna otro perfil a un usuario, se conservan las personalizaciones realizadas por el usuario con el perfil anterior.

## <a name="to-define-user-settings-for-a-profile" />Para definir la configuración de usuario para un perfil

Sobre la página **Mi configuración**, los usuarios pueden definir el comportamiento básico de su cuenta, como el área de trabajo, el idioma y las notificaciones que reciben. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).

Como administrador, puede definir la configuración de un perfil. La configuración se aplicará a todos los usuarios asignados al rol.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Perfiles (roles)** y luego elija el enlace relacionado.
2. Seleccione la línea del perfil cuya configuración de usuario desea cambiar y elija la acción **Enumerar personalizaciones de usuario**.
3. En la página **Personalizaciones del usuario**, abra la tarjeta para el usuario cuya configuración desea cambiar.
4. En la página **Tarjeta personalización usuario**, edite los campos según sea necesario.

## <a name="to-activate-a-profile" />Para activar un perfil

Cuando crea un perfil, puede definir si, dónde y cómo el perfil y su información se ponen a disposición de los usuarios.

En la página **Perfil (rol)**, seleccione las casillas siguientes:

* **Habilitado** para especificar si el rol relacionado es visible en la página **Roles disponibles** para que los usuarios elijan.  
* **Usar como perfil predeterminado** para especificar el perfil que se aplica a los usuarios que no tienen asignado un rol específico.
* **Deshabilitar personalización** para especificar si los usuarios del rolo relacionado pueden personalizar su espacio de trabajo.
* **Mostrar en Explorador de roles** para especificar si las acciones de las características empresariales incluidas en el perfil se muestran en la vista ampliada del explorador de roles, una descripción general de las funciones. Para obtener más información, vea [Búsqueda de páginas con el explorador de roles](ui-role-explorer.md).

## <a name="to-export-profiles" />Para exportar perfiles

Puede exportar perfiles desde [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo para reutilizarlos en otro suscriptor. Los perfiles se exportan a un archivo zip que contiene los archivos AL. Puede reutilizar los archivos AL para desarrollar extensiones. Para obtener más información, consulte [Usar el cliente para crear perfiles y personalizaciones de página](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* En la página **Perfiles (roles)**, elija la acción **Exportar perfiles**.

    Esta acción exporta un archivo zip que congiene archivos AL para todos los perfiles.

## <a name="to-import-profiles" />Para importar perfiles

Puede importar perfiles que se han exportado desde [!INCLUDE[prod_short](includes/prod_short.md)]. Los pasos son más o menos lo opuesto a los pasos para exportar perfiles. Para obtener más información, consulte [Para exportar perfiles](admin-users-profiles-roles.md#to-export-profiles).

1. En la página **Perfiles (roles)**, elija la acción **Importar perfiles**.
2. Siga los pasos en el asistente **Importar perfiles**.

    Si solo desea importar los perfiles seleccionados, use la casilla **Seleccionado** para indicar cuál importar.
3. Elija el botón **Importar seleccionado**.

    Esta acción importa un archivo zip que congiene archivos AL para los perfiles seleccionados.

## <a name="to-delete-a-profile" />Para eliminar un perfil

Puede eliminar un perfil eligiendo la acción **Eliminar** acción en la página **Perfiles (roles)**. Sin embargo, se aplican las siguientes limitaciones:

* No puede eliminar un perfil asignado a un usuario o grupo de usuarios.
*-* No puede eliminar perfiles que se originan a partir de extensiones. La extensión debe desinstalarse primero.
*-* Solo puede eliminar un perfil cada vez.

## <a name="to-delete-all-personalizations-made-by-a-user" />Para eliminar todas las personalizaciones efectuadas por un usuario

Puede eliminar todos los cambios que un usuario ha realizado en las páginas. Eliminar cambios puede ser útil, por ejemplo, si un empleado ha cambiado de rol y ya no los necesita. Las eliminaciones revierten el diseño de la página al definido por el perfil.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Personalizaciones de usuario** y luego elija el enlace relacionado.

    La página **Personalizaciones del usuario** muestra todos los usuarios que han realizado personalizaciones.

2. Abra la tarjeta de un usuario cuyas personalizaciones desea eliminar.
3. En la página **Ficha de personalización de usuario**, elija la acción **Borrar páginas personalizadas** y luego acepte el mensaje que aparece.

El usuario podrá ver los cambios la próxima vez que inicie sesión.

También puede eliminar todas las personalizaciones de página para un perfil. Para obtener más información, consulte [Para eliminar todas las personalizaciones de un perfil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages" />Para eliminar las personalizaciones de páginas específicas

Puede eliminar las personalizaciones que uno o más usuarios han realizado en páginas específicas. Eliminar personalizaciones puede ser útil, por ejemplo, si un cambio en el proceso de negocio significa que ya no se puede usar una personalización. Las eliminaciones revierten el diseño de la página al definido por el perfil.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Personalizaciones de página de usuario** y luego elija el enlace relacionado.

    La página **Personalizaciones de página de usuario** enumera todas las páginas que se han personalizado y el usuario al que pertenecen.

    > [!Note]
    > Una marca de verificación en el campo **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[prod_short](includes/prod_short.md)] que manejaba la personalización de forma diferente. Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página. Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

2. Seleccione la línea de la personalización de página que desea eliminar y, después, seleccione la acción **Eliminar**.

El usuario podrá ver los cambios la próxima vez que inicie sesión.  

También puede eliminar personalizaciones de página individuales para un perfil. Para obtener más información, consulte [Para eliminar la personalización de páginas específicas de un perfil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions" />Administrar sesiones de usuario

Como administrador de [!INCLUDE[prod_short](includes/prod_short.md)] online, puede administrar sesiones de usuario en el centro de administración. Para más información, vea [Administrar sesiones](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions) en el contenido de la administración.  

Para [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, puede administrar sesiones usando SQL Server Management Studio, por ejemplo. Para más información, consulte [Documentación técnica de SQL Server](/sql/sql-server).  

## <a name="see-related-microsoft-trainingtrainingmodulesusers-security-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/modules/users-security-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Personalizar páginas para perfiles](ui-personalization-manage.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
