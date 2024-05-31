---
title: Controlar el acceso mediante grupos de seguridad
description: Este artículo describe cómo usar grupos de seguridad para definir permisos de usuario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 04/15/2024
ms.service: dynamics-365-business-central
---

# <a name="control-access-to-business-central-using-security-groups"></a>Controlar el acceso a Business Central mediante grupos de seguridad

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Los grupos de seguridad facilitan a los administradores la gestión de los permisos de usuario. Por ejemplo, para [!INCLUDE [prod_short](includes/prod_short.md)] en línea, son reutilizables en las aplicaciones de Dynamics 365, como SharePoint en línea, CRM Online y [!INCLUDE [prod_short](includes/prod_short.md)]. Los administradores agregan permisos a sus grupos de seguridad de [!INCLUDE [prod_short](includes/prod_short.md)] y, cuando agregan usuarios al grupo, los permisos se aplican a todos los miembros. Por ejemplo, un administrador puede crear un grupo de seguridad de [!INCLUDE [prod_short](includes/prod_short.md)] que brinde a los vendedores la capacidad de crear y publicar pedidos de venta. O bien, deje que los compradores hagan lo mismo con los pedidos de compra.

## <a name="business-central-online-and-on-premises"></a>Business Central online y local

Puede usar grupos de seguridad para las versiones en línea y local de [!INCLUDE [prod_short](includes/prod_short.md)]. Dependiendo de la versión, cree grupos de una de las siguientes formas:

* Para la versión en línea, utilice grupos de seguridad de Microsoft Entra. Para obtener más información sobre cómo crear el grupo, vaya a [Crear, editar o eliminar un grupo de seguridad en el Centro de administración de Microsoft 365](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* En el caso del entorno local, los grupos de seguridad solo son compatibles si la implementación utiliza la autenticación de Windows. Para crear grupos de seguridad para entornos locales, use los grupos de Windows Active Directory. Para obtener más información, vaya a [Crear una cuenta de grupo en Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

A continuación, cree un grupo de seguridad correspondiente en [!INCLUDE [prod_short](includes/prod_short.md)] y luego vincúlelo al grupo que ha creado. Para obtener más información, vaya a [Agregar grupo de seguridad en Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Si ha configurado un tipo especial de usuario con un tipo de licencia de grupo de Windows en una versión de [!INCLUDE [prod_short](includes/prod_short.md)] local anterior al primer lanzamiento de versiones de 2023, cuando actualice [!INCLUDE [prod_short](includes/prod_short.md)] convierte el usuario en un grupo de seguridad. El nuevo grupo de seguridad tiene el mismo nombre que el grupo de Windows. El grupo de seguridad le brinda una mejor visión general de los miembros del grupo y sus permisos efectivos.

## <a name="add-a-security-group-in-business-central"></a>Agregar un grupo de seguridad en Business Central

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de seguridad**, y luego elija el vínculo relacionado.
1. Elija **Nuevo** para crear un grupo.
1. Cree el vínculo a su grupo, de la siguiente manera:

    * Para [!INCLUDE [prod_short](includes/prod_short.md)] en línea, elija el grupo en el campo **Nombre del grupo de seguridad de Microsoft Entra**.
    * Para [!INCLUDE [prod_short](includes/prod_short.md)] local, elija el grupo en el campo **Nombre del grupo de Windows**.

> [!NOTE]
> Los usuarios se muestran en la tarjeta **Miembros** del panel Cuadro informativo o en la página **Miembros del grupo de seguridad** solo si han sido agregados como usuarios en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre la adición de usuarios, vaya a [Para agregar usuarios o actualizar información de usuario y asignaciones de licencia en Business Central](ui-how-users-permissions.md#adduser).  

### <a name="assign-permissions-to-a-security-group"></a>Asignación de permisos a un grupo de seguridad

1. En la página **Grupos de seguridad**, elija el grupo y, a continuación, elija la acción **Permisos**.
1. Asigne permisos de las siguientes maneras:

    * Para asignar conjuntos de permisos individualmente, en el campo **Conjunto de permisos**, elija los permisos que desee asignar.
    * Para asignar varios conjuntos de permisos, elija la acción **Agregar varios** y luego elija los conjuntos que desea asignar.
1. Si desea que los conjuntos de permisos se apliquen solo a una empresa específica, establezca la columna **Empresa** a esa empresa. Si desea que el conjunto de permisos se aplique a todas las empresas, deje la columna **Empresa** en blanco. [Más información](ui-define-granular-permissions.md#control-access-to-specific-companies).

## <a name="review-the-permissions-in-a-security-group"></a>Revisar los permisos de un grupo de seguridad

En la página **Grupos de seguridad** , el panel Cuadro informativo muestra los **Conjuntos de permisos** que están asignados al grupo. Cada usuario que aparece en la tarjeta **Miembros** tiene esos permisos. La acción **Permiso establecido por grupo de seguridad** proporciona una vista más detallada. Allí también puede explorar los permisos individuales en cada grupo de seguridad.

Los permisos también están disponibles en la página **Usuarios**. El panel Cuadro informativo muestra las tarjetas **Conjuntos de permisos del grupo de seguridad** y **Pertenencias a grupos de seguridad** para el usuario seleccionado.

## <a name="security-groups-and-user-groups"></a>Grupos de seguridad y grupos de usuarios

> [!NOTE]
> Los grupos de usuarios ya no estarán disponibles en una versión futura.

Los grupos de seguridad son muy similares a los grupos de usuarios que están disponibles actualmente. Sin embargo, los grupos de usuarios solo son relevantes para [!INCLUDE [prod_short](includes/prod_short.md)]. Los grupos de seguridad se basan en grupos en Microsoft Entra ID o Windows Active Directory, dependiendo de si está usando [!INCLUDE [prod_short](includes/prod_short.md)] en línea o local, respectivamente. Los grupos benefician a los administradores porque pueden usarlos con otras aplicaciones de Dynamics 365. Por ejemplo, si los vendedores usan [!INCLUDE [prod_short](includes/prod_short.md)] y SharePoint, los administradores no tienen que volver a crear el grupo y sus miembros.

### <a name="optional-convert-user-groups-to-permission-sets"></a>Opcional: Convierta grupos de usuarios en conjuntos de permisos

En el primer lanzamiento de versiones de 2023 y posteriores, puede convertir grupos de usuarios en conjuntos de permisos en su inquilino. Los conjuntos de permisos proporcionan la misma funcionalidad que los grupos de usuarios. A continuación se muestran algunos ejemplos:

* Puede usar el cuadro informativo **Usuarios** para gestionar los permisos de los usuarios.
* Puede profundizar en el nombre del conjunto de permisos para agregar otros conjuntos de permisos al conjunto en el que está trabajando. Para obtener más información, vaya a [Para agregar otros conjuntos de permisos](ui-define-granular-permissions.md#to-add-other-permission-sets).

Utilice la guía de configuración asistida **Migración de grupos de usuarios** para convertir sus grupos. Para iniciar la guía, en la página **Administración de características** , busque **Característica: Convertir permisos de grupos de usuarios** y luego seleccione **Todos los usuarios** en el campo **Habilitado para**. La guía de configuración asistida ofrece las siguientes opciones para la conversión.

|Opción  |Descripción  |
|---------|---------|
|Asignar a usuario     | Asignar los permisos de los grupos de usuarios directamente a los usuarios que se asignaron al grupo, y eliminar sus asignaciones de grupos de usuarios.        |
|Convertir a un conjunto de permisos     | Cree un nuevo permiso para los permisos de cada grupo de usuarios. El nuevo conjunto de permisos se asigna a todos los miembros de cada grupo de usuarios.          |

### <a name="license-configurations-still-apply"></a>Las configuraciones de licencia aún se aplican

Puede configurar permisos en [!INCLUDE [prod_short](includes/prod_short.md)] basados en licencias. Esos permisos se asignan directamente a los nuevos usuarios. Estas configuraciones aún se aplican, incluso si comienza a utilizar grupos de seguridad.

Para utilizar grupos de seguridad exclusivamente, le recomendamos que elimine las configuraciones de licencia. Para obtener más información sobre las configuraciones de licencias, vaya a [Crear usuarios según las licencias](ui-how-users-permissions.md).

Puede eliminar configuraciones de licencia en la página **Configuración de licencia**. Elija una licencia y luego elimine todos los conjuntos de permisos asignados a ella.

## <a name="see-also"></a>Consulte también

[Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md)  
[Configurar el acceso a Business Central en Teams con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
[Más información sobre grupos y derechos de acceso en Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Grupos de seguridad de Microsoft Entra](/windows-server/identity/ad-ds/manage/understand-security-groups)  
