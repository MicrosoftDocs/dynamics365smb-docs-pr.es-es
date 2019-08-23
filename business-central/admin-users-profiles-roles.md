---
title: Administre usuarios y roles | Documentos de Microsoft
description: Obtener información sobre cómo administrar usuarios y áreas de trabajo en Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 08/02/2019
ms.author: edupont
ms.openlocfilehash: 27a57490101195f8dc05cc39538260e7db5e46af
ms.sourcegitcommit: 5bcc5f95e450ee9a3d9f7a380e592a5e75c4185b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/05/2019
ms.locfileid: "1858225"
---
# <a name="understanding-users-roles-and-profiles"></a>Comprensión de usuarios, roles y perfiles

En [!INCLUDE[d365fin](includes/d365fin_md.md)], un administrador añade a los usuarios y también les da acceso a las áreas de [!INCLUDE[d365fin](includes/d365fin_md.md)] que requieren en su trabajo.  

El acceso a la funcionalidad se gestiona a través de *grupos de usuarios* y *perfiles (roles)*. Como administrador, puede agregar y quitar usuarios como parte de su suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] y puede asignar permisos de usuario a través de grupos de usuarios.  

## <a name="adding-users"></a>Añadir usuarios

Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://aka.ms/CreateOffice365Users).

A continuación, el administrador puede asignar permisos a cada usuario y grupos de usuarios. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).  

Los permisos más potentes que un usuario puede tener es el conjunto de permisos SUPER. Cada empresa debe tener al menos un usuario con este conjunto de permisos, pero es una práctica recomendada dar a cada usuario permisos que coincidan con sus necesidades de trabajo en [!INCLUDE[prodshort](includes/prodshort.md)] y no más que eso. Esto contribuye a garantizar que los usuarios solo tengan acceso a los datos relevantes para su trabajo, por ejemplo.  

> [!TIP]
> Es una práctica recomendada asegurarse de que el administrador de Office 365 también tiene el permiso SUPER configurado en [!INCLUDE[prodshort](includes/prodshort.md)], ya que esto facilita muchas tareas administrativas, incluida la configuración de la integración con otras aplicaciones.

### <a name="users-of-on-premises-deployments"></a>Usuarios de las implementaciones locales

Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios. Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)]. Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles-roles"></a>Perfiles (roles)

La personas de su empresa que tienen acceso a [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen asignado un rol que les da acceso a un *Área de trabajo*.

Los perfiles son colecciones de usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que comparten el mismo rol. Un área de trabajo es el punto de entrada y la página de inicio de [!INCLUDE[d365fin](includes/d365fin_md.md)] que le da acceso rápido a sus tareas más importantes y le muestra varias perspectivas e indicadores de rendimiento clave (KPI) sobre su trabajo.  

> [!NOTE]  
>  En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, no puede agregar, editar, o eliminar perfiles.  

### <a name="CreateProfile"></a>Para crear un perfil

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Perfiles** y, a continuación, seleccione el vínculo relacionado.  

2.  En la página **Perfiles**, seleccione la acción **Nuevo** para abrir la página **Nueva ficha de perfil**.  

3.  En el campo **Id. perfil**, escriba un nombre que describa el rol previsto de los usuarios.  

4.  En el campo **Descripción**, escriba una descripción del identificador de perfil, como por ejemplo, **Procesador de pedidos**.  

5.  Establezca el campo **Id. área de trabajo** al área de trabajo que desea asignar al perfil.  

El procedimiento para modificar un perfil existente es el mismo, excepto que se selecciona un perfil existente en la página de perfiles **Perfiles** en lugar de elegir la acción **Nuevo**.  


### <a name="copy-a-profile"></a>Copiar un perfil
Copiar un perfil puede ahorrarle tiempo si desea utilizar una configuración similar en un perfil y solo desea modificar algunos ajustes.

1.  Abra el perfil que desea copiar y elija la acción **Copiar perfil**.

2.  En el campo **Nuevo id. de perfil**, introduzca el nombre del perfil que desea copiar.

3.  Establezca el campo **Nuevo ámbito de perfil** en una de las siguientes opciones:

    - **Sistema** para hacer que el nuevo perfil esté disponible para todas las bases de datos de inquilinos que usan la aplicación.
    - **Suscriptor** para hacer que el nuevo perfil esté disponible para la base de datos actual del suscriptor.
4. Cuando haya finalizado, elija el botón **Aceptar**.

### <a name="ExportImportProfile"></a>Exportar e importar perfiles

Puede exportar e importar perfiles como archivos XML a o desde la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. La exportación e importación de un perfil puede ahorrarle tiempo al configurar la interfaz de usuario porque reutiliza una configuración de perfil existente en lugar de tener que configurar un perfil desde cero. Si tiene un perfil configurado en una base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y desea reutilizar todas o algunas de las mismas configuraciones de perfil en otra base de datos, puede exportar el perfil a un archivo XML. A continuación, puede importar el archivo XML de perfil a otra base de datos.

-   Para exportar un perfil, puede elegir la acción **Exportar perfiles** en la página **Lista de perfiles** o **Ficha de perfil**, o puede buscar y abrir la página **Exportar perfiles**. Guarde el archivo XML en una ubicación del equipo o red.

-   Para importar un perfil, puede elegir la acción **Importar perfil** en la página **Lista de perfiles** o puede buscar y abrir la página **Importar perfiles**.

    > [!NOTE]  
    >  No puede importar un perfil que ya exista en la base de datos, aunque nombre o el contenido del archivo XML sean distintos. Debe eliminar el perfil existente para poder importar el perfil nuevo.


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
