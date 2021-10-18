---
title: Definir permisos granulares
description: Este tema describe cómo definir permisos granulares dando acceso a determinados usuarios a objetos y asignándoles conjuntos de permisos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: d048350c9963ae889b5320b3c78b87336197a7a9
ms.sourcegitcommit: 81a35248e6f1e8773339281b6f5c0ebd4942e05a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547028"
---
# <a name="assign-permissions-to-users-and-groups"></a>Asignar permisos a usuarios y grupos

El sistema de seguridad de [!INCLUDE[prod_short](includes/prod_short.md)] le permite controlar a qué objetos puede acceder un usuario en cada base de datos o entorno. Puede especificar para cada usuario si puede leer, modificar o introducir datos en los objetos de la base de datos seleccionados. Para obtener información detallada, vea [Seguridad de datos](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) en la ayuda para desarrolladores y profesionales de TI para [!INCLUDE[prod_short](includes/prod_short.md)].

Antes de asignar permisos a usuarios y grupos de usuarios, debe definir quién puede iniciar sesión creando usuarios de acuerdo con la licencia tal como se define en el Centro de administración de Microsoft 365. Para obtener más información, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).

En [!INCLUDE[prod_short](includes/prod_short.md)], hay dos niveles de permisos para los objetos de la base de datos:

- Permisos generales de acuerdo con la licencia, también se denominan derecho.
- Permisos más detallados según lo asignado desde [!INCLUDE[prod_short](includes/prod_short.md)].

Para facilitar la administración de permisos para varios usuarios, puede organizarlos en grupos de usuarios y así asignar o cambiar un conjunto de permisos para muchos usuarios en una sola acción. Para obtener más información, vea [Para administrar permisos mediante grupos de usuarios](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Un método adicional para definir a qué características tiene acceso un usuario consiste en establecer el campo **Experiencia** en la página **Información de la empresa**. Para obtener más información, consulte [Cambiar las funciones que se muestran](ui-experiences.md).
>
> También puede definir lo que ven los usuarios en la interfaz de usuario y cómo interactúan con su funcionalidad permitida a través de las páginas. Esta acción se hace a través de los perfiles que asigna a diferentes tipos de usuarios según su función de trabajo o departamento. Para obtener más información, [Administración de perfiles](admin-users-profiles-roles.md) y [Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Para asignar conjuntos de permisos a los usuarios

Un conjunto de permisos es una colección de permisos para objetos de base de datos específicos. A todos los usuarios se les debe asignar uno o varios conjuntos de permisos antes de que pueden acceder a [!INCLUDE[prod_short](includes/prod_short.md)].

Una solución de [!INCLUDE[prod_short](includes/prod_short.md)] contiene una serie de conjuntos de permisos predefinidos que Microsoft o su proveedor de soluciones agregan. También puede agregar nuevos conjuntos de permisos personalizados para satisfacer las necesidades de su organización. Para obtener más información, consulte [Para crear o editar un conjunto de permisos](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Si no desea restringir el acceso de un usuario más allá de lo definido por la licencia, puede asignar un conjunto de permisos especial llamado SUPER al usuario. Este conjunto de permisos garantiza que el usuario pueda acceder a todos los objetos especificados en la licencia.
>
> Un usuario con la licencia Essential y el conjunto de permisos SUPER tiene acceso a más funciones que los usuarios con la licencia Team Member y el conjunto de permisos SUPER.

Puede asignar conjuntos de permisos a los usuarios de dos formas:

- En la página **Ficha de usuario** seleccionando los conjuntos de permisos para asignarlos al usuario.
- En la página **Conjunto de permisos por usuario** seleccionando los usuarios a los que se ha asignado un conjunto de permisos.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Para asignar un conjunto de permisos en una tarjeta de usuario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Seleccione el usuario al que desea asignar el permiso.
Los conjuntos de permisos ya asignados al usuario se muestran en el cuadro informativo **Conjuntos de permisos**.
3. Seleccione la acción **Editar** para abrir la página **Ficha de usuario**.
4. En la ficha desplegable **Conjuntos de permisos de usuario**, en una línea nueva, rellene los campos según sea necesario. Para obtener más información, consulte [Para crear o editar un conjunto de permisos](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Para asignar un conjunto de permisos en la página Conjunto de permisos por usuario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. En la página **Usuarios**, seleccione el usuario relevante y luego elija la acción **Conjunto de permisos por usuario**.
3. En la página **Conjunto de permisos por usuario**, seleccione la casilla de verificación **[nombre de usuario]** en una línea del conjunto de permisos relevante para asignarlo al usuario.
4. Seleccione la casilla de verificación **Todos los usuarios** para asignar el conjunto de permisos a todos los usuarios.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Para obtener un resumen de los permisos de un usuario

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. Abra la ficha del usuario correspondiente.
3. Elija la acción **Permisos eficaces**.

    La parte de **Permisos** enumera todos los objetos de la base de datos a los que el usuario tiene acceso. Esta sección no se puede modificar.

    La parte **Por conjunto de permisos** muestra los conjuntos de permisos asignados a través de los cuales se otorgan los permisos al usuario, la fuente y el tipo de conjunto de permisos y a qué extensión se permiten los diferentes tipos de acceso.

    Para cada fila que seleccione en la sección **Permisos**, la sección **Por conjunto de permisos** muestra a qué conjunto de permisos o conjuntos de permisos se otorga. En esta sección, puede editar el valor en cada uno de los cinco campos de tipo de acceso, **Permiso de lectura**, **Permiso de inserción**, **Permiso de modificación**, **Permiso de eliminación** y **Permiso de ejecución**.

    > [!NOTE]  
    > Solo se pueden editar los conjuntos de permisos del tipo **Definido por el usuario**.
    >
    > Las filas del derecho de origen se originan a partir de la licencia de suscripción. Los valores del permiso del derecho anulan los valores en otros conjuntos de permisos si tienen un ranking mayor. Un valor en un conjunto de permisos sin derecho que tiene una clasificación más alta que el valor relacionado en el derecho estará entre paréntesis para indicar que no es efectivo ya que está invalidado por el derecho.
    >
    > Para obtener una explicación del ranking, consulte [Para crear o editar permisos](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Para editar un conjunto de permisos, en la parte **Por conjunto de permisos**, en la línea para un conjunto de permisos relevante de tipo **Definido por el usuario**, elija uno de los cinco campos de tipo de acceso y seleccione un valor diferente.

5. Para editar permisos individuales dentro del conjunto de permisos, elija el valor en el campo **Conjunto de permisos** para abrir la página **Permisos**. Siga los pasos descritos en [Para crear o editar permisos](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Cuando edite un conjunto de permisos, los cambios también se aplicarán a otros usuarios que tengan asignado el conjunto de permisos.

## <a name="to-create-or-modify-a-permission-set"></a>Para crear o modificar un conjunto de permisos

Los conjuntos de permisos funcionan como contenedores de permisos, de modo que puede administrar fácilmente múltiples permisos en un registro.

> [!NOTE]  
> Una solución de [!INCLUDE[prod_short](includes/prod_short.md)] generalmente contiene una serie de conjuntos de permisos predefinidos que Microsoft o su proveedor de software agregan. Estos conjuntos de permisos son de tipo **Sistema** o **Extensión**. No puede crear o editar estos tipos de conjuntos de permisos ni los permisos que estos contienen. Sin embargo, puede copiarlos para definir sus propios permisos y conjuntos de permisos.
>
> Los conjuntos de permisos que los usuarios crean, de nuevo o como copias, son del tipo **Definido por el usuario** y se pueden editar.

### <a name="to-create-new-permission-set-from-scratch"></a>Para crear un nuevo conjunto de permisos desde cero

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conjuntos de permisos** y luego elija el enlace relacionado.
2. Para crear un conjunto de permisos nuevo, elija la acción **Crear**.
3. En la línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Cuando haya creado un conjunto de permisos, debe agregar los permisos reales. Para obtener más información, consulte [Para crear o modificar permisos manualmente](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Copiar un conjunto de permisos

También puede utilizar una función de copia para transferir rápidamente todos los permisos de otro conjunto a uno nuevo.

> [!NOTE]  
> Si se modifica un conjunto de permisos del sistema que ha copiado, se le notificará (dependiendo de su selección), para que pueda considerar si los cambios son relevantes para copiarlos o escribirlos en su conjunto.

1. En la página **Conjuntos de permisos**, seleccione la línea para el conjunto de permisos que desea copiar y luego elija la acción **Copiar conjunto de permisos**.
2. En la página **Copiar conjunto de permisos**, especifique el nombre del nuevo conjunto de permisos y después seleccione el botón **Aceptar**.
3. Seleccione la casilla de verificación **Notificar sobre el conjunto de permisos modificado** si desea mantener un enlace entre el original y los conjuntos de permisos copiados. El enlace se usa para notificarle si el nombre o el contenido del conjunto de permisos original cambia en una versión futura a la que se actualiza la solución más adelante.

El nuevo conjunto de permisos, que contiene todos los permisos del conjunto de permisos copiado, se agrega como una nueva línea en la página **Conjuntos de permisos**. Ahora puede modificar el permiso en el nuevo conjunto de permisos. Tenga en cuenta que las líneas están ordenadas alfabéticamente dentro de cada tipo.

### <a name="to-export-and-import-a-permission-set"></a>Para exportar e importar un conjunto de permisos

Para configurar rápidamente permisos, puede importar conjuntos de permisos que haya exportado desde otro suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)].

En entornos multiempresa, se importará un conjunto de permisos a un suscriptor específico, es decir, el alcance de la importación es "Suscriptor".

1. En el primer suscriptor, en la página **Conjuntos de permisos**, seleccione la línea o líneas para el conjunto de permisos que se exportará y luego elija la acción **Exportar conjuntos de permisos**.

    Se crea un archivo xml en la carpeta de descargas de su máquina. De manera predeterminada, se denomina "Export Permission Sets.xml".

2. En el segundo suscriptor, en de la página **Conjuntos de permisos**, seleccione la acción **Importar conjuntos de permisos**.
3. En la página de diálogo **Importar conjuntos de permisos**, piense si desea fusionar los conjuntos de permisos existentes con cualquier nuevo conjunto de permisos en el archivo xml.

    Si selecciona la casilla de verificación **Actualizar permisos existentes**, los conjuntos de permisos existentes con el mismo nombre que los que existen en el archivo xml se fusionarán con los conjuntos de permisos importados.

    Si no selecciona la casilla de verificación **Actualizar permisos existentes**, los conjuntos de permisos con el mismo nombre que los que existen en el archivo xml se omitirán durante la importación. En ese caso, se le notificará sobre los conjuntos de permisos que se omiten.

4. En la página de diálogo **Importar**, busque y seleccione el archivo xml que se va a importar, y luego elija la acción **Abrir**.

Los conjuntos de permisos se importan.

## <a name="to-create-or-modify-permissions-manually"></a>Para crear o modificar permisos manualmente

Este procedimiento explica cómo agregar o editar permisos manualmente. Puede tener permisos generados automáticamente a partir de las acciones en la interfaz de usuario. Para obtener más información, consulte [Para crear o modificar permisos registrando las acciones](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Cuando edite un permiso y, por lo tanto, el conjunto de permisos relacionado, los cambios también se aplicarán a otros usuarios que tengan asignado el conjunto de permisos.

1. En la página **Conjuntos de permisos**, seleccione la línea para el conjunto de permisos y luego elija la acción **Permisos**.
2. En la página **Permisos**, cree una nueva línea o modifique los campos de la línea existente.

En cada uno de los cinco campos de tipo de acceso, **Permiso de lectura**, **Permiso de inserción**, **Permiso de modificación**, **Permiso de eliminación** y **Permiso de ejecución**, puede seleccionar una de las siguientes tres opciones de permiso:

|Opción|Description|Ranking|
|------|-----------|-------|
|**Sí**|El usuario puede realizar la acción del objeto en cuestión.|El mayor|
|**Indirecto**|El usuario puede realizar la acción del objeto en cuestión pero solo a través de otro objeto relacionado con el que el usuario tiene acceso a total. Para obtener más información sobre los permisos indirectos, consulte [Propiedad Permissions](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) en la Ayuda para desarrolladores e informáticos|En segundo mayor|
|**En blanco**|El usuario no puede realizar la acción del objeto en cuestión.|El menor|

> [!IMPORTANT]
> Tenga cuidado al asignar **Permiso de inserción** o **Permiso de modificación** a la tabla **Miembro de grupo de usuarios 9001** o **Conjunto de permisos de grupo de usuarios 9003**. Cualquier usuario asignado al conjunto de permisos podría potencialmente asignarse a otros grupos de usuarios, lo que a su vez puede otorgarles permisos no deseados.

### <a name="example---indirect-permission"></a>Ejemplo: permiso indirecto

Puede asignar un permiso indirecto para usar un objeto solo a través de otro objeto.
Por ejemplo, un usuario puede tener permiso para ejecutar la codeunit 80, Venta-Registrar. La codeunit Venta-Registrar realiza muchas tareas, incluida la modificación de la tabla 37, Línea de venta. Cuando el usuario registra un documento de venta, la codeunit Venta-Registrar, [!INCLUDE[prod_short](includes/prod_short.md)] comprueba si el usuario tiene permiso para modificar la tabla Línea de venta. Si no es así, la codeunit no puede completar sus tareas y el usuario recibe un mensaje de error. Si es así, la codeunit se ejecuta correctamente.

Sin embargo, el usuario no necesita tener acceso total a la tabla Línea de venta para ejecutar la codeunit. Si el usuario tiene permiso indirecto para la tabla Línea de venta, la codeunit Venta-Registrar se ejecuta correctamente. Cuando un usuario tiene permiso indirecto, solo puede modificar la tabla Línea de venta al ejecutar la codeunit Venta-Registrar u otro objeto que tenga permiso para modificar la tabla Línea de venta. El usuario sólo puede modificar la tabla Línea de venta en las áreas compatibles de la aplicación. El usuario no puede ejecutar la característica de forma inadvertida o malintencionada mediante otros métodos.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Para crear o modificar permisos registrando las acciones

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conjuntos de permisos** y luego elija el enlace relacionado.
2. Alternativamente, en la página **Usuarios**, seleccione la acción **Conjuntos de permisos**.
3. En la página **Conjuntos de permisos**, elija la acción **Nuevo**.
4. En una línea nueva, rellene los campos según sea necesario.
5. Elija la acción **Permisos**.
6. En la página **Permisos**, seleccione la acción **Registrar permisos** y, a continuación elija la acción **Iniciar**.

    Se inicia un proceso de registro que captura todas las acciones en la interfaz de usuario.
7. Vaya a las diferentes páginas y actividades en [!INCLUDE[prod_short](includes/prod_short.md)] a las que desea que accedan los usuarios con este conjunto de permisos. Debe realizar las tareas para las que desea registrar permisos.
8. Cuando desea finalizar el registro, vuelva a la página **Permisos** y, a continuación elija la acción **Paro**.
9. Seleccione el botón **Sí** para agregar los permisos registrados al nuevo conjunto de permisos.
10. Para cada objeto de la lista registrada especifique si los usuarios pueden insertar, modificar o eliminar los registros de las tablas registradas.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Filtros de seguridad: para restringir el acceso de un usuario a registros específicos en una tabla

Para seguridad de nivel registro en [!INCLUDE[prod_short](includes/prod_short.md)], utilice los filtros de seguridad para restringir el acceso a un usuario a los datos de una tabla. Cree los filtros de seguridad en los datos de la tabla. Un filtro de seguridad describe un conjunto de registros de una tabla a la que un usuario tiene permisos para acceder. Puede especificar, por ejemplo, que el usuario puede leer solo los registros que contienen información acerca de un determinado cliente. Esto significa que el usuario no puede acceder a los registros que contienen información sobre otros clientes. Para obtener más información, consulte [Usar filtros de seguridad](/dynamics365/business-central/dev-itpro/security/security-filters) en la Ayuda para desarrolladores y profesionales de TI.

## <a name="to-manage-permissions-through-user-groups"></a>Para administrar permisos a través de grupos de usuarios

Puede configurar grupos de usuarios para administrar conjuntos de permisos para grupos de usuarios en su empresa.

Se empieza con la creación de un grupo de usuarios. Después, asigna los conjuntos de permisos al grupo para definir a qué objetos pueden acceder los usuarios del grupo. Cuando agrega un usuario al grupo, los conjuntos de permisos definidos para el grupo se aplicarán al usuario.

Los conjuntos de permisos asignados a un usuario a través de un grupo de usuarios permanecen sincronizados para que un cambio en los permisos del grupo de usuarios se propague automáticamente al usuario. Si elimina un usuario de un grupo de usuarios, los permisos involucrados se revocan automáticamente.

### <a name="to-group-users-in-user-groups"></a>Para agrupar usuarios en grupos de usuarios

El siguiente procedimiento explica cómo crear grupos de usuarios manualmente. Para crear grupos de usuarios automáticamente, vea [Para copiar un grupo de usuarios y todos los conjuntos de permisos](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de usuarios** y luego elija el enlace relacionado.
2. Alternativamente, en la página **Usuarios**, seleccione la acción **Grupos de usuarios**.
3. En la página **Grupo usuarios**, seleccione la acción **Miembros de grupo de usuarios**.
4. En la página **Miembros de grupo de usuarios**, seleccione la acción **Agregar usuarios**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Para copiar un grupo de usuarios y todos los conjuntos de permisos

Para definir rápidamente un nuevo grupo de usuarios, puede copiar todos los conjuntos de permisos de un grupo de usuarios existente al nuevo grupo de usuarios.

> [!NOTE]
> No copian los miembros del grupo de usuarios al nuevo grupo de usuarios. Debe añadirlos manualmente posteriormente. Para obtener más información, consulte [Para agrupar usuarios en grupos de usuarios](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de usuarios** y luego elija el enlace relacionado.
2. Seleccione el grupo de usuarios que desea copiar y, a continuación, seleccione la acción **Copiar el grupo de usuarios**.
3. En el campo **Nuevo código de grupo de usuarios**, introduzca el nombre del grupo y después seleccione el botón **Aceptar**.

El nuevo grupo de usuarios se agrega a la página **Grupos de usuarios**. Empiece a agregar usuarios. Para obtener más información, consulte [Para agrupar usuarios en grupos de usuarios](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Para asignar conjuntos de permisos a grupos de usuarios

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de usuarios** y luego elija el enlace relacionado.
2. Seleccione el grupo de usuarios al que desea asignar el permiso.
Los conjuntos de permisos ya asignados al usuario se muestran en el cuadro informativo **Conjuntos de permisos**.
3. Elija la acción **Conjuntos de permisos de usuario** para abrir la página **Conjuntos de permisos de usuario**.
4. En la página **Conjuntos de permisos de usuario**, en una línea nueva, rellene los campos según sea necesario.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Para asignar un conjunto de permisos en la página **Conjunto de permisos por grupo de usuarios**

El siguiente procedimiento explica cómo asignar conjuntos de permisos a un grupo de usuarios en la página **Conjunto de permisos por grupo de usuarios**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.
2. En la página **Usuarios**, seleccione el usuario relevante y luego elija la acción **Conjunto de permisos por grupo de usuarios**.
3. En la página **Conjunto de permisos por grupo de usuarios**, seleccione la casilla de verificación **[nombre de grupo de usuarios]** en una línea del conjunto de permisos relevante para asignarlo al grupo de usuarios.
4. Seleccione la casilla de verificación **Todos los grupos de usuarios** para asignar el conjunto de permisos a todos los grupos de usuarios.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Para eliminar permisos obsoletos de todos los conjuntos de permisos

1. En la página **conjunto de permisos**, seleccione la acción **Eliminar permisos obsoletos**.

## <a name="to-set-up-user-time-constraints"></a>Para configurar restricciones de tiempo de usuarios

Los administradores pueden definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión. Los administradores también pueden asignar centros de responsabilidad a los usuarios. Para obtener más información, consulte [Trabajar con centros de responsabilidad](inventory-responsibility-centers.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de usuario** y luego elija el enlace relacionado.
2. En la página **Configuración usuarios** que se abre, seleccione la acción **Nuevo**.
3. En el campo **Id. usuario**, escriba el identificador de un usuario o elija el campo para ver todos los usuarios de Windows actuales en el sistema.
4. Rellene los campos según sea necesario.


## <a name="viewing-permission-changes-telemetry"></a>Ver los cambios de permisos de telemetría 

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para enviar cambios realizados en el permiso a un recurso de Application Insights en Microsoft Azure. Luego, con Azure Monitor, crea informes y configura alertas sobre los datos recopilados. Para obtener más información, consulte los siguientes artículos en la ayuda para desarrolladores y profesionales de TI de [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Supervisión y análisis de telemetría: habilitación de Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Análisis de la telemetría de monitoreo de campo](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Consulte también

[Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md)  
[Administración de perfiles](admin-users-profiles-roles.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Personalización de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Agregar usuarios a Microsoft 365 para empresas](/microsoft-365/admin/add-users/add-users)  
[Seguridad y protección en Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) en Ayuda para desarrolladores y profesionales de TI


[!INCLUDE[footer-include](includes/footer-banner.md)]