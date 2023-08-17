---
title: Configurar acceso con licencias de Microsoft 365
description: Una guía sobre cómo los administradores pueden configurar el acceso a Business Central con licencias de Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: 9061
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Configurar el acceso a Business Central en Teams con licencias de Microsoft 365

Los administradores deben completar varias actividades antes de que los usuarios puedan acceder a [!INCLUDE [prod_short](includes/prod_short.md)] con su licencia de Microsoft 365. Los pasos a continuación representan la configuración mínima requerida para comenzar. Para obtener más información sobre el acceso con licencias de Microsoft 365, vaya a [Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Directrices

Configurar el acceso con licencias de Microsoft 365 implica las siguientes tareas:

||Tarea|Requerido|
|-|-|-|
|1|[Configurar qué datos de Business Central tienen permiso para ver los usuarios con licencia de Microsoft 365](#configure-permissions)|![marca de verificación](media/check.png "comprobar")|
|2|[Habilite el acceso con licencias de Microsoft 365 en el entorno de Business Central](#enable-access-with-microsoft-365-licenses)|![marca de verificación](media/check.png "comprobar")|
|3|[Asigne un grupo de seguridad al entorno](#choose-who-gets-access-by-using-security-group)|
|4|[Implementar la aplicación Business Central para usuarios de Teams](#deploy-the-business-central-app-for-teams)|![marca de verificación](media/check.png "comprobar")|
|5|[Pruebe la configuración](#test-your-setup)||

> [!TIP]
> Excepto por la última tarea, puede completar las tareas en cualquier orden. Puede realizar las tareas por separado, como se describe en las secciones siguientes o utilizar la guía de configuración asistida **Acceso con licencias Microsoft 365** para explicárselas.
>
> Para ejecutar la guía de configuración asistida, realice los pasos siguientes:
>
> 1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y luego elija el enlace relacionado.
> 2. En la página **Configuración asistida**, vaya a la sección **Haga más con Business Central** y seleccione **Acceso con licencias de Microsoft 365**.
> 3. Siga estas instrucciones.  

## <a name="configure-permissions"></a>Configurar permisos

[!INCLUDE [prod_short](includes/prod_short.md)] es seguro por diseño y minimiza el riesgo al no otorgar permisos a usuarios de Microsoft 365 directamente. Los administradores deben configurar permisos de objetos que determinen a qué tablas, páginas e informes se puede acceder en Teams con solo una licencia de Microsoft 365. Estos permisos son los permisos iniciales asignados cuando un usuario inicia sesión por primera vez con su licencia de Microsoft 365. 

Para configurar los permisos de inicio:

1. En [!INCLUDE [prod_short](includes/prod_short.md)], busque **Configuración de licencia**.
2. Seleccione la licencia de Microsoft 365.
3. En la parte superior de la página de la licencia de **Microsoft 365**, seleccione el icono de edición ![icono de edición](media/edit-pencil.png), luego active **Personalizar permisos**. 
4. En la sección **Conjuntos de permisos personalizados**, agregue los conjuntos de permisos apropiados y elija si son aplicables a una sola empresa o a todas las empresas dentro del entorno.

Con esta configuración, los usuarios con solo una licencia de Microsoft 365 se agregan a la lista de **Usuarios** cuando acceden a [!INCLUDE [prod_short](includes/prod_short.md)] por primera vez. Para obtener más información sobre los usuarios, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).

> [!NOTE]
> Al sincronizar la lista de usuarios en [!INCLUDE [prod_short](includes/prod_short.md)] con usuarios en Microsoft 365, solo los usuarios que tienen una licencia de [!INCLUDE [prod_short](includes/prod_short.md)] se agregan a la lista de usuarios de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener un mayor control administrativo sobre los permisos y los perfiles, puede asignar un grupo de seguridad al entorno. Cuando los entornos están protegidos mediante un grupo de seguridad y habilitan el acceso con licencias de Microsoft 365 licencias, la acción **Actualizar usuarios desde Microsoft 365** en la página **Usuarios** también incluirá a los usuarios que solo tienen una licencia de Microsoft 365. Para obtener información sobre cómo proteger los entornos, consulte [Administrar el acceso mediante grupos de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) en la ayuda para desarrolladores y profesionales de TI.

> [!TIP]
> ¿Está buscando una forma más rápida de empezar a probar esta característica de espacio aislado o empresa de evaluación? Asigne el conjunto de permisos **Leer D365**, que otorga permiso a la mayoría de los objetos.  

Cuando se trabaja con varios entornos, la configuración de la licencia se debe aplicar a cada entorno y puede ser diferente en cada entorno.

Obtenga más información en [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md) y [Componer conjuntos de permisos](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="enable-access-with-microsoft-365-licenses"></a>Habilitar el acceso con licencias de Microsoft 365

El acceso con licencias de Microsoft 365 está desactivado de forma predeterminada. El acceso debe habilitarse para cada entorno de forma independiente, dando a los administradores el control y permitiendo la implementación por etapas en toda la organización. Active el acceso mediante el centro de administración de [!INCLUDE [prod_short](includes/prod_short.md)]: 

1. En la esquina superior derecha, seleccione **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") > **Centro de administración**.  
2. En el centro de administración, seleccione  **Entornos** y, a continuación, seleccione el entorno en el que desea cambiar el acceso a la licencia. 
3. En la página **Detalles del entorno**, seleccione **Modificar** para la configuración **Acceso con licencias de Microsoft 365**.
4. En el panel **Licencias de Microsoft 365**, active el interruptor. 
5. Seleccione **Guardar** cuando termine y acepte la confirmación. El cambio entra en vigor inmediatamente.

## <a name="choose-who-gets-access-by-using-security-group"></a>Elija quién obtiene acceso mediante el uso del grupo de seguridad

En el centro de administración de Business Center, se puede asignar un entorno a uno o más grupos de seguridad para controlar el acceso. Puede asignar un grupo de Azure Active Directory (Azure AD) al entorno. Al asignar un grupo de Azure AD a un entorno, solo los miembros directos e indirectos del grupo tienen acceso al entorno. Los miembros indirectos son usuarios de otro grupo, que a su vez es miembro del grupo asignado al entorno. Aunque todos los usuarios con licencia de Azure AD se agregarán al entorno cuando se sincronice con Microsoft 365, solo los miembros del grupo pueden iniciar sesión. Para obtener información, consulte [Administrar el acceso mediante grupos de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) en la ayuda para desarrolladores y profesionales de TI.

## <a name="deploy-the-business-central-app-for-teams"></a>Implementar la aplicación Business Central para Teams

Para que los titulares de licencias de [!INCLUDE [prod_short](includes/prod_short.md)] compartan datos en Teams y para que los titulares de licencias de Microsoft 365 accedan a esos datos, cada uno debe tener instalada la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams. Aunque los usuarios pueden instalar la aplicación por sí mismos, se recomienda que los administradores utilicen la implementación centralizada. La implementación centralizada le permite implementar la aplicación a una audiencia más amplia en toda la organización y minimizar el esfuerzo del usuario individual. 

Para obtener información sobre cómo implementar de forma centralizada la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams, consulte [Instalación de la aplicación Business Central mediante la implementación centralizada](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Si ejecutó la implementación centralizada anteriormente y solo implementó la aplicación en el grupo de seguridad de los usuarios de [!INCLUDE [prod_short](includes/prod_short.md)] con licencia, deberá ejecutarla nuevamente para implementarla en grupos adicionales o en toda la organización, según cómo esté configurando el acceso.

> [!TIP]
> ¿Está buscando una forma más rápida de empezar a probar esta característica? Los usuarios de prueba pueden instalar la aplicación en [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="test-your-setup"></a>Probar su configuración

Para verificar que su configuración esté lista para la producción, los siguientes pasos le ayudarán a generar la confianza de que todo funciona como debería.

1. Cree o identifique dos usuarios de prueba (A y B).

   - El usuario de prueba A debe tener una licencia de [!INCLUDE [prod_short](includes/prod_short.md)] y de Microsoft 365 con acceso a Teams.
   - El usuario de prueba B debe tener solo una licencia de Microsoft 365 con acceso a Teams.

2. Inicie sesión en el cliente web de [!INCLUDE [prod_short](includes/prod_short.md)] como usuario de prueba A.

   1. Abra un registro al que el usuario de prueba B debería tener acceso, coma ficha de **Artículo** en la empresa y el entorno adecuados.
   2. Seleccione **Compartir** ![Compartir con otras acciones de aplicaciones en las páginas.](media/share-icon.png) > **Compartir con Teams** para abrir la ventana Compartir con Teams.
   3. En el campo **Compartir con**, agregue el usuario de prueba B como destinatario.
   4. Espere a que el vínculo se expanda a una tarjeta y seleccione Compartir.

3. Inicie sesión en Microsoft Teams como usuario de prueba B.

   1. Seleccione Chat y abra la conversación con el usuario de prueba A.
   2. En el mensaje enviado por el usuario de prueba A, seleccione el botón Detalles en la tarjeta. Si se muestra el cliente de [!INCLUDE [prod_short](includes/prod_short.md)] y es de solo lectura, su configuración se ha realizado con éxito.

> [!TIP]
> ¿Ha habido algún problema? Consulte [Solucionar problemas de acceso con licencias de Microsoft 365](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Consulte también .

[Descripción general del acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Solucionar problemas de acceso con licencias de Microsoft 365](admin-access-with-m365-license-troubleshooting.md)  
[Integración de Business Central y Microsoft Teams](across-teams-overview.md)  
