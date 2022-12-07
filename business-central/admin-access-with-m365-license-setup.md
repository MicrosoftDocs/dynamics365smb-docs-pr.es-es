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
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.search.forms: 9061
ms.openlocfilehash: 3b3e7d42e077749bd4443506f7423dce03e9e82f
ms.sourcegitcommit: 61f22aeede684f0ae772353ede6530ff03ff2f90
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2022
ms.locfileid: "9804424"
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Configurar el acceso a Business Central en Teams con licencias de Microsoft 365

Los administradores deben completar varias actividades antes de que los usuarios puedan acceder a Business Central con su licencia de Microsoft 365. Los pasos a continuación representan la configuración mínima requerida para comenzar. Para obtener más información sobre el acceso con licencias de Microsoft 365, vaya a [Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md).

## <a name="deploy-the-business-central-app-for-teams"></a>Implementar la aplicación Business Central para Teams

Para que los titulares de licencias de Business Central compartan datos en Teams y para que los titulares de licencias de Microsoft 365 accedan a esos datos, cada uno debe tener instalada la aplicación Business Central para Teams. Aunque los usuarios pueden instalar la aplicación por sí mismos, se recomienda que los administradores utilicen la implementación centralizada. La implementación centralizada le permite implementar la aplicación a una audiencia más amplia en toda la organización y minimizar el esfuerzo del usuario individual. 

Para obtener información sobre cómo implementar de forma centralizada la aplicación Business Central para Teams, consulte [Instalación de la aplicación Business Central mediante la implementación centralizada](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Si ejecutó la implementación centralizada anteriormente y solo implementó la aplicación en el grupo de seguridad de los usuarios de Business Central con licencia, deberá ejecutarla nuevamente para implementarla en grupos adicionales o en toda la organización, según cómo esté configurando el acceso.

> [!TIP]
> ¿Está buscando una forma más rápida de empezar a probar esta característica? Los usuarios de prueba pueden instalar la aplicación en [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Configurar permisos

Business Central es seguro por diseño y minimiza el riesgo al no otorgar permisos a usuarios de Microsoft 365 directamente. Los administradores deben configurar permisos de objetos que determinen a qué tablas, páginas e informes se puede acceder en Teams con solo una licencia de Microsoft 365. Estos permisos son los permisos iniciales asignados cuando un usuario inicia sesión por primera vez con su licencia de Microsoft 365. 

Para configurar los permisos de inicio:

1. En Business Central, busque **Configuración de licencia**.
2. Seleccione la licencia de Microsoft 365.
3. En la parte superior de la página de la licencia de **Microsoft 365**, seleccione el icono de edición ![icono de edición](media/edit-pencil.png), luego active **Personalizar permisos**. 
4. En la sección **Conjuntos de permisos personalizados**, agregue los conjuntos de permisos apropiados y elija si son aplicables a una sola empresa o a todas las empresas dentro del entorno.

Con esta configuración, los usuarios con solo una licencia de Microsoft 365 se agregan a la lista de **Usuarios** cuando acceden a Business Central por primera vez. Para obtener más información sobre los usuarios, vea [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).

> [!NOTE]
> Al sincronizar la lista de usuarios en Business Central con usuarios en Microsoft 365, solo los usuarios que tienen una licencia de Business Central se agregan a la lista de usuarios de Business Central. Para obtener un mayor control administrativo sobre los permisos, los grupos de usuarios y los perfiles, puede asignar un grupo de seguridad al entorno. Cuando los entornos están protegidos mediante un grupo de seguridad y habilitan el acceso con licencias de Microsoft 365 licencias, la acción **Actualizar usuarios desde Microsoft 365** en la página **Usuarios** también incluirá a los usuarios que solo tienen una licencia de Microsoft 365. Para obtener información sobre cómo proteger los entornos, consulte [Administrar el acceso mediante grupos de Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) en la ayuda para desarrolladores y profesionales de TI.

> [!TIP]
> ¿Está buscando una forma más rápida de empezar a probar esta característica de espacio aislado o empresa de evaluación? Asigne el conjunto de permisos **Leer D365**, que otorga permiso a la mayoría de los objetos.  

Cuando se trabaja con varios entornos, la configuración de la licencia se debe aplicar a cada entorno y puede ser diferente en cada entorno. 

Obtenga más información en [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md) y [Componer conjuntos de permisos](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Activar el acceso con licencias de Microsoft 365

El acceso con licencias de Microsoft 365 está desactivado de forma predeterminada. El acceso debe habilitarse para cada entorno de forma independiente, dando a los administradores el control y permitiendo la implementación por etapas en toda la organización. Active el acceso mediante el centro de administración de Business Central: 

1. En la esquina superior derecha, seleccione **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") > **Centro de administración**.  
2. En el centro de administración, seleccione  **Entornos** y, a continuación, seleccione el entorno en el que desea cambiar el acceso a la licencia. 
3. En la página **Detalles del entorno**, seleccione **Modificar** para la configuración **Acceso con licencias de Microsoft 365**.
4. En el panel **Licencias de Microsoft 365**, active el interruptor. 
5. Seleccione **Guardar** cuando termine y acepte la confirmación. El cambio entra en vigor inmediatamente.

## <a name="test-your-setup"></a>Probar su configuración

Para verificar que su configuración esté lista para la producción, los siguientes pasos le ayudarán a generar la confianza de que todo funciona como debería. 

1. Cree o identifique dos usuarios de prueba (A y B).

   - El usuario de prueba A debe tener una licencia de Business Central y de Microsoft 365 con acceso a Teams.
   - El usuario de prueba B debe tener solo una licencia de Microsoft 365 con acceso a Teams.

2. Inicie sesión en el cliente web de Business Central como usuario de prueba A.

   1. Abra un registro al que el usuario de prueba B debería tener acceso, coma ficha de **Artículo** en la empresa y el entorno adecuados.
   2. Seleccione **Compartir** ![Compartir con otras acciones de aplicaciones en las páginas.](media/share-icon.png) > **Compartir con Teams** para abrir la ventana Compartir con Teams.
   3. En el campo **Compartir con**, agregue el usuario de prueba B como destinatario. 
   4. Espere a que el vínculo se expanda a una tarjeta y seleccione Compartir. 

3. Inicie sesión en Microsoft Teams como usuario de prueba B.

   1. Seleccione Chat y abra la conversación con el usuario de prueba A. 
   2. En el mensaje enviado por el usuario de prueba A, seleccione el botón Detalles en la tarjeta. Si se muestra el cliente de Business Central y es de solo lectura, su configuración se ha realizado con éxito. 

> [!TIP]
> ¿Ha habido algún problema? Consulte [Solucionar problemas de acceso con licencias de Microsoft 365](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Consulte también .

[Descripción general del acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Solucionar problemas de acceso con licencias de Microsoft 365](admin-access-with-m365-license-troubleshooting.md)  
[Integración de Business Central y Microsoft Teams](across-teams-overview.md)  
