---
title: Administre usuarios y roles | Documentos de Microsoft
description: "Obtener información sobre cómo administrar usuarios y áreas de trabajo en Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Comprender usuarios, perfiles y áreas de trabajo

En [!INCLUDE[d365fin](includes/d365fin_md.md)], un administrador añade a los usuarios y también les da acceso a las áreas de [!INCLUDE[d365fin](includes/d365fin_md.md)] que requieren en su trabajo.  

El acceso a la funcionalidad se gestiona a través de *grupos de usuarios* y *perfiles*. Como administrador, puede agregar y quitar usuarios como parte de su suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] y puede asignar permisos de usuario a través de grupos de usuarios.  

## <a name="adding-users"></a>Añadir usuarios

Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://aka.ms/CreateOffice365Users).

A continuación, el administrador puede asignar permisos a cada usuario y grupos de usuarios. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Usuarios de las implementaciones locales

Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios. Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)]. Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Perfiles

La personas de su empresa que tienen acceso a [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen asignado un *perfil* que les da acceso a un *Área de trabajo*.

Los perfiles son colecciones de usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que comparten la misma área de trabajo. Un área de trabajo es el punto de entrada y la página de inicio de [!INCLUDE[d365fin](includes/d365fin_md.md)] que le da acceso rápido a sus tareas más importantes y le muestra varias perspectivas e indicadores de rendimiento clave (KPI) sobre su trabajo.  

> [!NOTE]  
>  En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, no puede agregar, editar, o eliminar perfiles.  

## <a name="configuration-and-personalization"></a>Configuración y personalización
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Los usuarios personalizan la interfaz de usuario de su versión personal mediante la adaptación de la IU en su propio inicio de sesión de usuario. Esta personalización puede ser eliminada por el administrador. Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).  

## <a name="see-also"></a>Consulte también  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)  
[Administrar la personalización como administrador](ui-personalization-manage.md)  
[Personalización de su área de trabajo](ui-personalization-user.md)  

