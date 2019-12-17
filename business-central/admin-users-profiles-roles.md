---
title: Administre usuarios y roles | Documentos de Microsoft
description: Obtener información sobre cómo administrar usuarios y áreas de trabajo en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 11/06/2019
ms.author: sgroespe
ms.openlocfilehash: 4c485d722de2a51f22310308b102ed066b4f01d2
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809038"
---
# <a name="manage-profiles"></a>Administración de perfiles
A todos los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] se les asigna un perfil que refleja su rol de negocio, el departamento en el que trabaja u otra clasificación. Los perfiles permiten a los administradores definir y administrar centralmente lo que los diferentes tipos de usuarios pueden ver y hacer en la interfaz de usuario para que puedan realizar sus tareas de negocio de manera eficiente.

> [!NOTE]
> El uso de negocio típico de un perfil es un rol. Por lo tanto, un perfil se llama *Perfil (rol)* en la interfaz de usuario.

Como administrador, usted crea y administra perfiles en la página **Perfiles (roles)**. Cada perfil tiene una tarjeta en la que administra varias configuraciones para el rol relacionado, como el nombre del rol, la configuración del usuario y el área de trabajo que utiliza el perfil. Para obtener más información sobre la configuración de usuario y las áreas de trabajo, consulte [Cambiar la configuración básica](ui-change-basic-settings.md).

Para poder administrar los perfiles de los usuarios, los usuarios se deben crear y agregar a través de Centro de administración de Microsoft 365. Después, puede asignar permisos a cada usuario o grupo de usuarios para definir qué características se les permite ver o editar. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Personalización de página
Puede personalizar los diseños de página para un perfil de modo que todos los usuarios asignados al perfil vean las páginas personalizadas. Como administrador, personalice las páginas utilizando la misma funcionalidad que los usuarios cuando realizan la personalización. Para obtener más información, consulte [Personalizar las páginas para los perfiles](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Para crear un perfil
Si no puede copiar un perfil existente, puede crear uno nuevo manualmente.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Perfiles (roles)** y, a continuación, seleccione el vínculo relacionado.  
2. En la página **Perfiles (roles)**, elija la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Para copiar un perfil
Para ahorrar tiempo, puede crear un nuevo perfil copiando uno existente. Copie uno que tenga una configuración similar al que desea crear.

> [!NOTE]
> Cuando copia un perfil, también se copian todas las personalizaciones de página involucradas, tanto las creadas por el usuario como las derivadas de las extensiones.

1. En la página **Perfiles (roles)**, seleccione la línea para el perfil que desea copiar y luego elija la acción **Copiar perfil**.
2. Complete los campos **Id. perfil** y **Nombre para mostrar** y luego elija el botón **Aceptar**.
3. En la página **Perfiles (roles)**, abra la tarjeta de perfil recién creada y edite otros campos según sea necesario.

## <a name="to-edit-a-profile"></a>Para editar un perfil
Puede editar un perfil cambiando los campos en la página **Perfil (rol)**. Sin embargo, los cambios no serán visibles para el usuario asignado al perfil hasta que cierre la sesión y vuelva a iniciarla.

> [!Caution]
> No cambie el nombre de un perfil mientras los usuarios asignados al perfil estén conectados, ya que los usuarios pueden experimentar que el producto se congele y debe reiniciarse.

## <a name="to-assign-a-profile-to-a-user"></a>Para asignar un perfil a un usuario
Los usuarios pueden asignarse un rol (que representa un perfil) eligiendo el campo **Rol** en la página **Mi configuración**. Como administrador, puede hacer lo mismo a través de la página **Perfiles (roles)**.

1. En la página **Perfiles (roles)**, seleccione el perfil que desea asignar y luego elija la acción **Lista personalización usuario**.
2. En la página **Personalizaciones del usuario**, seleccione el usuario al que desea asignar el perfil y luego elija la acción **Editar**.
3. En el campo **Id. perfil**, seleccione el perfil relevante.

> [!NOTE]
> Si asigna otro perfil a un usuario, se conservan las personalizaciones realizadas por el usuario con el perfil anterior.

## <a name="to-define-user-settings-for-a-profile"></a>Para definir la configuración de usuario para un perfil
Sobre la página **Mi configuración**, los usuarios pueden definir el comportamiento básico de su cuenta, como el área de trabajo, el idioma y las notificaciones que reciben. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).

Como administrador, puede definir esta configuración para un perfil y, por lo tanto, aplicar la configuración a todos los usuarios del rol relacionado.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Perfiles (roles)** y luego elija el enlace relacionado.
2. Seleccione la línea del perfil cuya configuración de usuario desea cambiar, elija la acción **Navegar** y luego elija la acción **Personalizaciones del usuario**.
3. En la página **Personalizaciones del usuario**, abra la tarjeta para el usuario cuya configuración desea cambiar.
4. En la página **Tarjeta personalización usuario**, edite los campos según sea necesario.

## <a name="to-activate-a-profile"></a>Para activar un perfil
Cuando se crea un perfil, puede seleccionar diferentes casillas que definen si, dónde y cómo el perfil y su información se ponen a disposición de los usuarios.

* En la página **Perfil (rol)**, seleccione las casillas siguientes:
    - **Habilitado** para especificar si el rol relacionado es visible en la página **Roles disponibles** para que los usuarios elijan.  
    - **Usar como perfil predeterminado** para especificar el perfil que se aplica a los usuarios que no tienen asignado un rol específico.
    - **Deshabilitar personalización** para especificar si los usuarios del rolo relacionado pueden personalizar su espacio de trabajo.
    - **Mostrar en Explorador de roles** para especificar si las acciones de las características empresariales incluidas en el perfil se muestran en la vista ampliada del explorador de roles, una descripción general de las funciones. Para obtener más información, vea [Búsqueda de páginas con el explorador de roles](ui-role-explorer.md).

## <a name="to-export-user-created-profiles"></a>Para exportar los perfiles creados por el usuario
Puede exportar perfiles que hayan cambiado usted o los usuarios, como lo indica **(Creado por el usuario)** en el campo **Origen**. El perfil se exporta a un archivo comprimido que contiene archivos .al que se pueden reutilizar para desarrollar extensiones. Para obtener más información, consulte [Uso del cliente para crear perfiles y personalizaciones de página](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* En la página **Perfiles (roles)**, elija la acción **Exportar perfiles creados por el usuario**.

Se exporta un archivo comprimido con los archivos .al para los perfiles que se han agregado o modificado recientemente.

## <a name="to-delete-a-profile"></a>Para eliminar un perfil
Puede eliminar un perfil eligiendo la acción **Eliminar** acción en la página **Perfiles (roles)**. Sin embargo, se aplican las siguientes limitaciones:

- No puede eliminar un perfil asignado a un usuario o grupo de usuarios.
- No puede eliminar perfiles que se originan a partir de extensiones. La extensión debe desinstalarse primero.
- Solo puede eliminar un perfil cada vez.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Para eliminar todas las personalizaciones efectuadas por un usuario
Puede eliminar todos los cambios que un usuario ha realizado en las páginas que constituyen su espacio de trabajo. Esto puede ser útil, por ejemplo, si un empleado ha cambiado de rol y ya no necesita las personalizaciones. Al eliminar las personalizaciones de los usuarios, el diseño de la página vuelve a ser el definido por el perfil.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Personalizaciones del usuario** y luego elija el enlace relacionado.

    La página **Personalizaciones del usuario** muestra todos los usuarios que han realizado personalizaciones.

2. Abra la tarjeta de un usuario cuyas personalizaciones desea eliminar.
3. En la página **Ficha de personalización de usuario**, elija la acción **Borrar páginas personalizadas** y luego acepte el mensaje que aparece.

El usuario podrá ver los cambios la próxima vez que inicie sesión.

También puede eliminar todas las personalizaciones de página para un perfil. Para obtener más información, consulte [Para eliminar todas las personalizaciones de un perfil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Para eliminar las personalizaciones de páginas específicas
Puede eliminar las personalizaciones que uno o más usuarios han realizado en páginas específicas que constituyen su espacio de trabajo. Esto puede ser útil, por ejemplo, si un proceso de negocio modificado significa que los usuarios ya no deben usar una personalización. Al eliminar las personalizaciones de los usuarios, el diseño de la página vuelve a ser el definido por el perfil.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Personalizaciones de página de usuario** y luego elija el enlace relacionado.

    La página **Personalizaciones de página de usuario** enumera todas las páginas que se han personalizado y el usuario al que pertenecen.

    > [!Note]
    > Una marca de verificación en el campo **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[d365fin](includes/d365fin_md.md)] que manejaba la personalización de forma diferente. Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página. Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

2. Seleccione la línea de la personalización de página que desea eliminar y, después, seleccione la acción **Eliminar**.

El usuario podrá ver los cambios la próxima vez que inicie sesión.    

También puede eliminar personalizaciones de página individuales para un perfil. Para obtener más información, consulte [Para eliminar la personalización de páginas específicas de un perfil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Consulte también  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Personalizar páginas para perfiles](ui-personalization-manage.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  
