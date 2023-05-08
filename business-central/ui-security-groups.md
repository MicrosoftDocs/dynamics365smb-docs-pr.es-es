---
title: Controlar el acceso mediante grupos de seguridad
description: Este artículo describe cómo usar grupos de seguridad para definir permisos de usuario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Controlar el acceso a Business Central mediante grupos de seguridad

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Los grupos de seguridad facilitan a los administradores la administración de permisos de usuario en sus aplicaciones de Dynamics 365, como SharePoint Online, CRM Online y la versión en línea de [!INCLUDE [prod_short](includes/prod_short.md)]. Los administradores agregan permisos a sus grupos de seguridad y, cuando agregan usuarios al grupo, los permisos se aplican a todos los miembros. Por ejemplo, un administrador puede crear un grupo de seguridad que brinde a los vendedores la capacidad de crear y publicar pedidos de venta. O bien, deje que los compradores hagan lo mismo con los pedidos de compra.

Cree sus grupos de seguridad en su Centro de administración de Microsoft 365 o Azure Active Directory. Este artículo describe los pasos en el Centro de administración de Microsoft 365, pero los pasos son similares en ambos casos.

## Agregar un grupo de seguridad en el Centro de administración de Microsoft 365

1. En el Centro de administración de Microsoft 365, vaya a la página **Activar equipos y grupos**.
2. Elija **Agregar un grupo**.
3. Escoja el tipo de grupo **Seguridad** y luego elija **Siguiente**.
4. Especifique los conceptos básicos para su grupo.
5. Opcional: haga que los miembros del grupo estén disponibles para la asignación de roles. Para obtener más información sobre las asignaciones, vaya a [Usar grupos de Azure AD para administrar asignaciones de roles](/azure/active-directory/roles/groups-concept).
6. Abra el grupo y luego use la pestaña **Agregar miembros** para incluir personas en el grupo.

## Agregar un grupo de seguridad en Business Central

En [!INCLUDE [prod_short](includes/prod_short.md)], cree un grupo de seguridad y luego vincúlelo al grupo de seguridad en el Centro de administración de Microsoft 365. Su nuevo grupo contiene los miembros que agregó en el Centro de administración de Microsoft 365.

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de seguridad**, y luego elija el vínculo relacionado.
2. Elija **Nuevo** para crear un grupo.
3. En el campo **Nombre**, escriba un nombre para el grupo.
4. En el campo **Nombre del grupo de seguridad de AAD**, introduzca el nombre del grupo de seguridad exactamente como aparece en el Centro de administración de Microsoft 365. [!INCLUDE [prod_short](includes/prod_short.md)] encontrará ese grupo y lo vinculará a este grupo.

> [!NOTE]
> Los usuarios que se muestran en la tarjeta **Miembros** del panel Cuadro informativo o en la página **Miembros del grupo de seguridad** solo si han sido agregados como usuarios en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la adición de usuarios, vaya a [Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central](ui-how-users-permissions.md#adduser).  

### Asignar permisos al grupo

1. En la página **Grupos de seguridad**, elija el grupo y, a continuación, elija la acción **Permisos**.
1. Asigne permisos de las siguientes maneras:
    * Para asignar conjuntos de permisos individualmente, en el campo **Conjunto de permisos**, elija los permisos que desee asignar.
    * Para asignar varios conjuntos de permisos, elija la acción **Seleccionar conjuntos de permisos** y luego elija los conjuntos que desea asignar.

## Revisar los permisos de un grupo de seguridad

En la página **Grupos de seguridad** , el panel Cuadro informativo muestra los **Conjuntos de permisos** que están asignados al grupo. Cada usuario que aparece en la tarjeta **Miembros** tiene esos permisos. La acción **Permiso establecido por grupo de seguridad** proporciona una vista más detallada. Allí también puede explorar los permisos individuales en cada grupo de seguridad.

Los permisos también están disponibles en la página **Usuarios**. El panel Cuadro informativo muestra las tarjetas **Conjuntos de permisos del grupo de seguridad** y **Pertenencias a grupos de seguridad** para el usuario seleccionado.

## Grupos de seguridad y grupos de usuarios

Si tiene grupos de usuarios, puede convertirlos en conjuntos de permisos en su suscriptor mediante la guía de configuración asistida **Migración de grupos de usuarios**. Para iniciar la guía, en la página **Administración de características** , busque **Característica: Convertir permisos de grupos de usuarios** y luego seleccione **Todos los usuarios** en el campo **Habilitado para**. La guía de configuración asistida ofrece las siguientes opciones para la conversión.

|Opción  |Descripción  |
|---------|---------|
|Asignar a usuario     | Asignar los permisos de los grupos de usuarios directamente a los usuarios que se asignaron al grupo, y eliminar sus asignaciones de grupos de usuarios.        |
|Convertir a un conjunto de permisos     | Cree un nuevo permiso para los permisos de cada grupo de usuarios. El nuevo conjunto de permisos se asigna a todos los miembros de cada grupo de usuarios.          |

## Consulte también

[Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md)  
[Configurar el acceso a Business Central en Teams con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
[Más información sobre grupos y derechos de acceso en Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Grupos de seguridad de Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  