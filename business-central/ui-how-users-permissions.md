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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 51c8c4207d9b5311698c7c5575fc67d8c5b2df9d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310905"
---
# <a name="manage-users-and-permissions"></a>Administrar usuarios y permisos
Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://aka.ms/CreateOffice365Users).

Una vez que los usuarios se crean en Office 365, se pueden importar a la página **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. A los usuarios se les asignan conjuntos de permisos según el plan asignado al usuario en Office 365. Para obtener información detallada acerca de las licencias, consulte la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Después podrá asignar conjuntos de permisos a los usuarios para definir a qué objetos de base de datos y, por lo tanto, a qué elementos de la interfaz de usuario, tienen acceso y en qué empresas. Puede agregar usuarios a grupos de usuarios. Esto facilita asignar los mismos conjuntos de permisos a varios usuarios.

Un conjunto de permisos es una colección de permisos para objetos específicos de la base de datos. A todos los usuarios se les debe asignar uno o varios conjuntos de permisos antes de que pueden acceder a [!INCLUDE[d365fin](includes/d365fin_md.md)].

Desde la página de la **Tarjeta de usuario**, puede abrir la página **Permisos efectivos** para ver qué permisos tiene el usuario y a través de qué conjuntos de permisos se otorgan. Aquí también puede cambiar los detalles de los permisos para los conjuntos de permisos del tipo **Definido por el usuario**. Para obtener más información, consulte [Para obtener un resumen de los permisos de un usuario](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="users-in-on-premises-deployments"></a>Usuarios en implementaciones locales
Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios. Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)]. Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="profiles"></a>Perfiles
Después de agregar usuarios, puede definir lo que ven en la interfaz de usuario y cómo interactúan con su funcionalidad permitida a través de las páginas. Esta acción hace a través de perfiles, que reflejan roles o departamentos, que se asignan a diferentes tipos de usuarios. Para obtener más información, [Administración de perfiles](admin-users-profiles-roles.md) y [Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md).

## <a name="to-add-a-user-in-business-central"></a>Agregar un usuario en Business Central
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Elija la acción **Obtener usuarios de Office 365**.

Cualquier usuario nuevo que se haya creado para su suscripción a Office 365 se agregará a la página **Usuarios**.

## <a name="to-edit-or-delete-a-user"></a>Para editar o eliminar un usuario
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario que desea editar y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de usuario**, cambie la información según sea necesario.    
4. Para eliminar un usuario, seleccione el usuario que desea eliminar y, después, seleccione la acción **eliminar**.

## <a name="to-group-users-in-user-groups"></a>Para agrupar usuarios en grupos de usuarios
Puede configurar grupos de usuarios para administrar conjuntos de permisos para grupos de usuarios en su empresa.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos de usuarios** y luego elija el enlace relacionado.
2. Alternativamente, en la página **Usuarios**, seleccione la acción **Grupos de usuarios**.
3. En la página **Grupo usuarios**, seleccione la acción **Miembros de grupo de usuarios**.
4. En la página **Miembros de grupo de usuarios**, seleccione la acción **Agregar usuarios**.

Cuando se crean usuarios o grupos de usuarios, se deben asignar conjuntos de permisos a cada uno para definir a qué objeto puede acceder un usuario. En primer lugar, debe organizar los permisos relevantes en los conjuntos de permisos. Para obtener más información, consulte [Para obtener un resumen de los permisos de un usuario](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Para copiar un grupo de usuarios y todos los conjuntos de permisos
Para definir rápidamente un nuevo grupo de usuarios, puede copiar todos los conjuntos de permisos de un grupo de usuarios existente al nuevo grupo de usuarios.

No copian los miembros del grupo de usuarios al nuevo grupo de usuarios. Debe añadirlos manualmente posteriormente.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos de usuarios** y luego elija el enlace relacionado.
2. Seleccione el grupo de usuarios que desea copiar y, a continuación, seleccione la acción **Copiar el grupo de usuarios**.
3. En el campo **Nuevo código de grupo de usuarios**, introduzca el nombre del grupo y después seleccione el botón **Aceptar**.

El nuevo grupo de usuarios se agrega a la página **Grupos de usuarios**. Empiece a agregar usuarios. Para obtener más información, consulte [Para agrupar usuarios en grupos de usuarios](ui-how-users-permissions.md#to-group-users-in-user-groups).  

## <a name="to-set-up-user-time-constraints"></a>Para configurar restricciones de tiempo de usuarios
Los administradores pueden definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión. Los administradores también pueden asignar centros de responsabilidad a los usuarios. Para obtener más información, consulte [Trabajar con centros de responsabilidad](inventory-responsibility-centers.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración del usuario** y luego elija el enlace relacionado.
2. En la página **Configuración usuarios** que se abre, seleccione la acción **Nuevo**.
3. En el campo **Id. usuario**, escriba el identificador de un usuario o elija el campo para ver todos los usuarios de Windows actuales en el sistema.
4. Rellene los campos según sea necesario.

## <a name="to-create-or-modify-a-permission-set"></a>Para crear o modificar un conjunto de permisos
Los conjuntos de permisos funcionan como contenedores de permisos, de modo que puede administrar fácilmente múltiples permisos en un registro. Cuando haya creado un conjunto de permisos, debe agregar los permisos reales. Para obtener más información, consulte [Para crear o editar permisos manualmente](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> Una solución de [!INCLUDE[d365fin](includes/d365fin_md.md)] generalmente contiene una serie de conjuntos de permisos predefinidos que Microsoft o su proveedor de software agregan. Estos conjuntos de permisos son de tipo **Sistema** o **Extensión**. No puede crear o editar estos tipos de conjuntos de permisos ni los permisos que estos contienen. Sin embargo, puede copiarlos para definir sus propios permisos y conjuntos de permisos. <br /><br />
Los conjuntos de permisos que los usuarios crean, de nuevo o como copias, son del tipo **Definido por el usuario** y se pueden editar.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Conjunto de permisos** y luego elija el enlace relacionado.
2. Para crear un conjunto de permisos nuevo, elija la acción **Crear**.
3. En la línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Copiar un conjunto de permisos
Cuando crea conjuntos de permisos nuevos, puede utilizar una función de copia para transferir rápidamente todos los permisos de otro conjunto a uno nuevo.

> [!NOTE]  
> Si se modifica un conjunto de permisos del sistema que ha copiado, se le notificará (dependiendo de su selección), para que pueda considerar si los cambios son relevantes para copiarlos o escribirlos en su conjunto.

1. En la página **Conjuntos de permisos**, seleccione la línea para el conjunto de permisos que desea copiar y luego elija la acción **Copiar conjunto de permisos**.
2. En la página **Copiar conjunto de permisos**, especifique el nombre del nuevo conjunto de permisos y después seleccione el botón **Aceptar**.
3. Seleccione la casilla de verificación **Notificar sobre el conjunto de permisos modificado** si desea mantener un enlace entre el original y los conjuntos de permisos copiados. El enlace se usa para notificarle si el nombre o el contenido del conjunto de permisos original cambia en una versión futura a la que se actualiza la solución más adelante.

El nuevo conjunto de permisos, que contiene todos los permisos del conjunto de permisos copiado, se agrega como una nueva línea en la página **Conjuntos de permisos**. Tenga en cuenta que las líneas están ordenadas alfabéticamente dentro de cada tipo.

## <a name="to-create-or-modify-permissions-manually"></a>Para crear o modificar permisos manualmente
Este procedimiento explica cómo agregar o editar permisos manualmente. Puede tener conjuntos de permisos generados automáticamente de las acciones en la interfaz de usuario. Para obtener más información, consulte [Para crear o modificar conjuntos de permisos grabando la sección de las acciones](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. En la página **Conjuntos de permisos**, seleccione la línea para el conjunto de permisos y luego elija la acción **Permisos**.
2. En la página **Permisos**, cree una nueva línea o modifique los campos de la línea existente.

En cada uno de los cinco campos de tipo de acceso, **Permiso de lectura**, **Permiso de inserción**, **Permiso de modificación**, **Permiso de eliminación** y **Permiso de ejecución**, puede seleccionar una de las siguientes tres opciones de permiso:

|Opción|Description|Ranking|
|------|-----------|
|**Sí**|El usuario puede realizar la acción del objeto en cuestión.|El mayor|
|**Indirecto**|El usuario puede realizar la acción del objeto en cuestión pero solo a través de otro objeto relacionado con el que el usuario tiene acceso a total.|En segundo mayor|
|**En blanco**|El usuario no puede realizar la acción del objeto en cuestión.|El menor|

### <a name="example---indirect-permission"></a>Ejemplo: permiso indirecto
Puede asignar un permiso indirecto para usar un objeto solo a través de otro objeto.
Por ejemplo, un usuario puede tener permiso para ejecutar la codeunit 80, Venta-Registrar. La codeunit Venta-Registrar realiza muchas tareas, incluida la modificación de la tabla 37, Línea de venta. Cuando el usuario registra un documento de venta, la codeunit Venta-Registrar, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si el usuario tiene permiso para modificar la tabla Línea de venta. Si no es así, la codeunit no puede completar sus tareas y el usuario recibe un mensaje de error. Si es así, la codeunit se ejecuta correctamente.

Sin embargo, el usuario no necesita tener acceso total a la tabla Línea de venta para ejecutar la codeunit. Si el usuario tiene permiso indirecto para la tabla Línea de venta, la codeunit Venta-Registrar se ejecuta correctamente. Cuando un usuario tiene permiso indirecto, solo puede modificar la tabla Línea de venta al ejecutar la codeunit Venta-Registrar u otro objeto que tenga permiso para modificar la tabla Línea de venta. El usuario sólo puede modificar la tabla Línea de venta en las áreas compatibles de la aplicación. El usuario no puede ejecutar la característica de forma inadvertida o malintencionada mediante otros métodos.

## <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Para restringir el acceso de un usuario a registros específicos en una tabla
Para seguridad de nivel registro en [!INCLUDE[d365fin](includes/d365fin_md.md)], utilice los filtros de seguridad para restringir el acceso a un usuario a los datos de una tabla. Cree los filtros de seguridad en los datos de la tabla. Un filtro de seguridad describe un conjunto de registros de una tabla a la que un usuario tiene permisos para acceder. Puede especificar, por ejemplo, que el usuario puede leer solo los registros que contienen información acerca de un determinado cliente. Esto significa que el usuario no puede acceder a los registros que contienen información sobre otros clientes. Para obtener más información, consulte [Usar filtros de seguridad](/dynamics365/business-central/dev-itpro/security/security-filters) en la Ayuda para desarrolladores y profesionales de TI.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Para crear o modificar conjuntos de permisos registrando las acciones
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Conjunto de permisos** y luego elija el enlace relacionado.
2.  Alternativamente, en la página **Usuarios**, seleccione la acción **Conjuntos de permisos**.
3.  En la página **Conjuntos de permisos**, elija la acción **Nuevo**.
4.  En una línea nueva, rellene los campos según sea necesario.
5.  Elija la acción **Permisos**.
6.  En la página **Permisos**, seleccione la acción **Registrar permisos** y, a continuación elija la acción **Iniciar**.

    Se inicia un proceso de registro que captura todas las acciones en la interfaz de usuario.
7.  Vaya a las diferentes páginas y actividades en [!INCLUDE[d365fin](includes/d365fin_md.md)] a las que desea que accedan los usuarios con este conjunto de permisos. Debe realizar las tareas para las que desea registrar permisos.
8.  Cuando desea finalizar el registro, vuelva a la página **Permisos** y, a continuación elija la acción **Paro**.
9.  Seleccione el botón **Sí** para agregar los permisos registrados al nuevo conjunto de permisos.
10. Para cada objeto de la lista registrada especifique si los usuarios pueden insertar, modificar o eliminar los registros de las tablas registradas.

> [!NOTE]  
> Cuando edite un permiso y, por lo tanto, el conjunto de permisos relacionado, los cambios también se aplicarán a otros usuarios que tengan asignado el conjunto de permisos.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Para asignar conjuntos de permisos a usuarios o grupos de usuarios
Puede asignar permisos a los usuarios de dos formas:
- Definir conjuntos de permisos en la tarjeta de usuario de un usuario.
- Seleccione la casilla de verificación para un usuario, en una columna, para un conjunto de permisos relacionado, en una fila, en la página **Conjunto de permisos por usuario**.
    Con este método, también puede asignar conjuntos de permisos a grupos de usuarios.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Para asignar un conjunto de permisos en una tarjeta de usuario
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario al que desea asignar el permiso.
Los conjuntos de permisos ya asignados al usuario se muestran en el cuadro informativo **Conjuntos de permisos**.
3. Seleccione la acción **Editar** para abrir la página **Ficha de usuario**.
4. En la ficha desplegable **Conjuntos de permisos de usuario**, en una línea nueva, rellene los campos según sea necesario. Para obtener más información, consulte [Para crear o editar un conjunto de permisos](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Para asignar un conjunto de permisos en la página **Conjunto de permisos por usuario**  
El siguiente procedimiento explica cómo asignar conjuntos de permisos a un usuario en la página **Conjunto de permisos por usuario**. Los pasos son similares en la página **Conjunto de permisos por grupo de usuarios**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. En la página **Usuarios**, seleccione el usuario relevante y luego elija la acción **Conjunto de permisos por usuario**.
3. En la página **Conjunto de permisos por usuario**, seleccione la casilla de verificación **[nombre de usuario]** en una línea del conjunto de permisos relevante para asignarlo al usuario.
4. Seleccione la casilla de verificación **Todos los usuarios** para asignar el conjunto de permisos a todos los usuarios.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Para obtener un resumen de los permisos de un usuario
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios** y luego elija el enlace relacionado.
2. Abra la ficha del usuario correspondiente.
3. Elija la acción **Permisos eficaces**.

    La parte de **Permisos** enumera todos los objetos de la base de datos a los que el usuario tiene acceso. Esta sección no se puede modificar.

    La parte **Por conjunto de permisos** muestra los conjuntos de permisos asignados a través de los cuales se otorgan los permisos al usuario, la fuente y el tipo de conjunto de permisos y a qué extensión se permiten los diferentes tipos de acceso.

    Para cada fila que seleccione en la sección **Permisos**, la sección **Por conjunto de permisos** muestra a qué conjunto de permisos o conjuntos de permisos se otorga. En esta sección, puede editar el valor en cada uno de los cinco campos de tipo de acceso, **Permiso de lectura**, **Permiso de inserción**, **Permiso de modificación**, **Permiso de eliminación** y **Permiso de ejecución**.   

    > [!NOTE]  
    > Solo se pueden editar los conjuntos de permisos del tipo **Definido por el usuario**.<br /><br />
    > Las filas del derecho de origen se originan del plan de suscripción. Los valores del permiso del derecho anulan los valores en otros conjuntos de permisos si tienen un ranking mayor. Un valor en un conjunto de permisos sin derecho que tiene una clasificación más alta que el valor relacionado en el derecho estará entre paréntesis para indicar que no es efectivo ya que está invalidado por el derecho. Para obtener una explicación del ranking, consulte [Para crear o editar permisos](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Para editar un conjunto de permisos, en la parte **Por conjunto de permisos**, en la línea para un conjunto de permisos relevante de tipo **Definido por el usuario**, elija uno de los cinco campos de tipo de acceso y seleccione un valor diferente.

5. Para editar permisos individuales dentro del conjunto de permisos, elija el valor en el campo **Conjunto de permisos** para abrir la página **Permisos**. Siga los pasos descritos en [Para crear o editar permisos](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Cuando edite un conjunto de permisos, los cambios también se aplicarán a otros usuarios que tengan asignado el conjunto de permisos.

## <a name="to-remove-a-users-access-to-the-system"></a>Para eliminar el acceso de un usuario al sistema

Como administrador, puede eliminar el acceso de un usuario al sistema configurando el campo **Estado** en **Deshabilitado**. Todas las referencias al usuario se conservarán, pero el usuario ya no podrá iniciar sesión en el sistema y finalizarán las sesiones activas para el usuario. Para dar acceso de nuevo al usuario, configure el campo **Estado** en **Habilitado**.

## <a name="see-also"></a>Consulte también
[Seguridad y protección en Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Administración](admin-setup-and-administration.md)  
[Agregar usuarios para Office 365 para empresas](https://aka.ms/CreateOffice365Users)  
[Guía sobre licencias de Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)
