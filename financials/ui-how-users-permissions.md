---
title: Asignar permisos de usuario y crear o modifican conjuntos de permisos | Documentos de Microsoft
description: "Describe cómo agregar usuarios de Office 365 a Financials y asignarles permisos, derechos de acceso y opciones de seguridad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 564ef68a1571611efee32db1cf3759cda6a04c80
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Administrar usuarios y permisos
Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Una vez se hayan creado los usuarios en Office 365, se pueden importar en la ventana **Usuarios** mediante la acción **Obtener usuarios desde Office 365**. A los usuarios se les asignan conjuntos de permisos según el plan asignado al usuario en Office 365.

Después podrá asignar conjuntos de permisos a los usuarios para definir a qué objetos de base de datos y, por lo tanto, a qué elementos de la interfaz de usuario, tienen acceso y en qué empresas.

Un conjunto de permisos es una colección de permisos para objetos específicos de la base de datos. A todos los usuarios se les debe asignar uno o varios conjuntos de permisos antes de que pueden acceder a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un número de conjuntos de permisos predefinidos se proporcionan de forma predeterminada. Puede utilizar estos conjuntos de permisos como están definidos, modificar los conjuntos de permisos predeterminados o crear sus propios conjuntos de permisos adicionales.

Puede agregar usuarios a grupos de usuarios. Esto facilita asignar los mismos conjuntos de permisos a varios usuarios.

Los administradores pueden usar la ventana **Configuración usuarios** para definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión.

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en Conjunto de aplicaciones. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Para asignar permisos a un usuario
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el usuario al que desea asignar el permiso.
Los conjuntos de permisos ya asignados al usuario se muestran en el cuadro informativo **Conjuntos de permisos**.
3. Seleccione la acción **Editar** para abrir la ventana **Ficha de usuario**.
4. En la ficha desplegable **Conjuntos de permisos de usuario**, en una línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Para agrupar usuarios en grupos de usuarios
Puede configurar grupos de usuarios para administrar conjuntos de permisos para grupos de usuarios en su empresa. Puede usar una función para copiar todos los conjuntos de permisos de un grupo de usuarios existente al nuevo grupo de usuarios. No copian los miembros del grupo de usuarios.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de usuarios** y, a continuación, seleccione el vínculo relacionado.
2. Alternativamente, en la ventana **Usuarios**, seleccione la acción **Grupos de usuarios**.
3. En la ventana **Grupos de usuarios**, seleccione un grupo de usuarios existente que desee copiar y después seleccione la acción **Copiar el grupo de usuarios**.
4. En el campo **Nuevo código de grupo de usuarios**, especifique el nombre del nuevo grupo de usuarios y después seleccione el botón **Aceptar**.

    Como alternativa a copiar, puede elegir la acción Nuevo para crear una nueva línea para un grupo de usuarios vacío, que después rellenará manualmente.
5. Para agregar usuarios nuevos o adicionales, en la ventana **Grupo de usuarios**, seleccione la acción **Miembros de grupo de usuarios**.
6. En la ventana **Miembros de grupo de usuarios**, en una línea nueva, rellene los campos según sea necesario seleccionando entre los usuarios existentes.
7. Para agregar conjuntos de permisos nuevos o adicionales, en la ventana **Grupo de usuarios**, seleccione la acción **Conjuntos de permisos de grupo de usuarios**.
8. En la ventana **Conjuntos de permisos de grupo de usuarios**, en una línea nueva, rellene los campos según sea necesario seleccionando entre los conjuntos de permisos existentes.

## <a name="to-create-or-modify-permission-sets"></a>Para crear o modificar conjuntos de permisos
Si los conjuntos de permisos predeterminados que se proporcionan con [!INCLUDE[d365fin](includes/d365fin_md.md)] no son suficientes o no son adecuados para su organización, puede crear nuevos conjuntos de permisos. Y si los permisos de objeto individuales que definen un conjunto de permisos no son adecuados, puede modificar un conjunto de permisos. Puede crear un conjunto de permisos manualmente, o bien usar una función de registro que registre las acciones al explorar un escenario y después genere el conjunto de permisos solicitado.

### <a name="to-create-or-modify-permission-sets-manually"></a>Para crear o modificar conjuntos de permisos manualmente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Usuarios**, seleccione la acción **Conjuntos de permisos**.
3. En la ventana **Conjuntos de permisos**, elija la acción **Nuevo**.
4. En una línea nueva, rellene los campos según sea necesario.
5. Elija la acción **Permisos**.
6. En la ventana **Permisos**, rellene los campos en el encabezado según sea necesario.
7. En una línea nueva, rellene los cinco campos de los diferentes tipos de permisos tal como se describe en la tabla siguiente.

    |Opción|Descripción|
    |------|-----------|
    |En blanco|Especifica que el tipo de permiso no se concede al objeto.|
    |**Sí**|Especifica que el tipo de permiso se concede con acceso directo al objeto.|
    |**Indirecto**|Especifica que el tipo de permiso se concede con acceso indirecto al objeto.|

    El permiso indirecto a una tabla significa que no puede abrir la tabla y leerla, pero puede consultar los datos de la tabla a través de otro objeto, como una página, que tenga permiso directo para acceder. Para obtener más información, consulte la sección "Ejemplo: permiso indirecto" en este tema.

8. En el campo **Filtro seguridad**, introduzca un filtro que desee aplicar al permiso seleccionando el campo en el que desea limitar el acceso de un usuario.

    Por ejemplo, si desea crear un filtro de seguridad de modo que un usuario solo pueda ver ventas con un código específico de vendedor, elija el número de campo correspondiente al campo **Cód. vendedor**. A continuación, en el campo **Filtro de campo**, escriba el valor que desea usar para restringir el acceso. Por ejemplo, para limitar el acceso de un usuario sólo a las ventas de Annette Hill, introduzca AH.
9. Repita los pasos 7 y 8 para agregar permisos de objetos adicionales al conjunto de permisos.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Para crear o modificar conjuntos de permisos registrando las acciones
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Usuarios**, seleccione la acción **Conjuntos de permisos**.
3. En la ventana **Conjuntos de permisos**, elija la acción **Nuevo**.
4. En una línea nueva, rellene los campos según sea necesario.
5. Elija la acción **Permisos**.
6. En la ventana **Permisos**, elija la acción **Iniciar**.

    Se inicia un proceso de registro para capturar todas las acciones en la interfaz de usuario.
7. Vaya a las diferentes ventanas y actividades en [!INCLUDE[d365fin](includes/d365fin_md.md)] a las que desea que accedan los usuarios con este conjunto de permisos. Debe realizar las tareas para las que desea registrar permisos.
8. Cuando desea finalizar el registro, vuelva a la ventana **Permisos** y, a continuación elija la acción **Paro**.
9. Seleccione el botón **Sí** para agregar los permisos registrados al nuevo conjunto de permisos.
10. Para cada objeto de la lista registrada especifique si los usuarios pueden insertar, modificar o eliminar los registros de las tablas registradas. Vea el paso 7 de la sección "Para crear o modificar conjuntos de permisos manualmente".

### <a name="example---indirect-permission"></a>Ejemplo: permiso indirecto
Puede asignar un permiso indirecto para usar un objeto solo a través de otro objeto.
Por ejemplo, un usuario puede tener permiso para ejecutar la unidad de código 80, **Venta-Registrar**. La unidad de código **Venta-Registrar** realiza muchas tareas, incluida la modificación de la tabla 37, **Línea de venta**. Cuando el usuario registra un documento de venta, la unidad de código **Venta-Registrar**, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si el usuario tiene permiso para modificar la tabla **Línea de venta**. Si no es así, la unidad de código no puede completar sus tareas y el usuario recibe un mensaje de error. Si es así, la unidad de código se ejecuta correctamente.

Sin embargo, el usuario no necesita tener acceso total a la tabla **Línea de venta** para ejecutar la unidad de código. Si el usuario tiene permiso indirecto a la tabla **Línea de venta**, la unidad de código **Venta-Registrar** se ejecuta correctamente. Cuando un usuario tiene permiso indirecto, solo puede modificar la tabla **Línea de venta** al ejecutar la unidad de código **Venta-Registrar** u otro objeto que tenga permiso para modificar la tabla **Línea de venta**. El usuario sólo puede modificar la tabla **Línea de venta** en las áreas compatibles de la aplicación. El usuario no puede ejecutar la característica de forma inadvertida o malintencionada mediante otros métodos.

## <a name="to-set-up-user-time-constraints"></a>Para configurar restricciones de tiempo de usuarios
Los administradores pueden definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión. Los administradores también pueden asignar centros de responsabilidad a los usuarios.

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración usuarios** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Configuración usuarios** que se abre, seleccione la acción **Nuevo**.
3. En el campo **Id. usuario**, escriba el identificador de un usuario o elija el campo para ver todos los usuarios de Windows actuales en el sistema.
4. Rellene los campos según sea necesario.

## <a name="see-also"></a>Consulte también
[Preparación para hacer negocios](ui-get-ready-business.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

