---
title: Conectar a Common Data Service | Documentos de Microsoft
description: Puede integrar otras aplicaciones con Business Central a través de Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2020
ms.author: bholtorf
ms.openlocfilehash: 4c57d8c79f91319675527f514b01b6ddeb83e722
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529218"
---
# <a name="connect-to-common-data-service"></a>Conectar a Common Data Service
Este tema describe cómo configurar una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)]. Por lo general, las empresas crean la conexión para integrar y sincronizar datos con otra aplicación empresarial de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Antes de comenzar
Hay algunos datos que debe tener listos para crear la conexión:  

* La dirección URL del entorno de [!INCLUDE[d365fin](includes/cds_long_md.md)] al que desea conectarse. Si usa la guía de configuración asistida **Configuración de conexión de CDS** para crear la conexión descubriremos los entornos, pero también puede introducir la URL de otro entorno en su suscriptor.  
* El nombre de usuario y la contraseña de una cuenta que tenga permisos de administrador en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Estos pasos describen el procedimiento para la versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Si está utilizando Business Central on-premises y no está utilizando la cuenta Azure Active Directory para conectarse a Common Data Service, también debe especificar un nombre de usuario y una contraseña de una cuenta de usuario para la integración. Esta cuenta se conoce como la cuenta de "usuario de integración". Si está usando una cuenta de Azure Active Directory la cuenta de usuario de integración no es necesaria ni se muestra. El usuario de integración se configurará automáticamente y no requiere una licencia.

## <a name="set-up-a-connection-to-d365fin"></a>Configurar una conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)]  
En todos los tipos de autenticación distintos de la autenticación de Office 365, configure la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)] en la página **Configuración de la conexión de CDS**. Para la autenticación de Office 365, es recomendable que use la guía de configuración asistida **Configuración de conexión de Common Data Service**. La guía simplifica la configuración de la conexión y permite especificar características avanzadas, como el modelo de propiedad y la sincronización inicial.  

> [!Important]
> Durante la configuración de la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)], se pedirá al administrador que otorgue los siguientes permisos a la aplicación de Azure registrada denominada Integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] para [!INCLUDE[d365fin](includes/cds_long_md.md)]:
> * Se necesita permiso de **Acceso a [!INCLUDE[d365fin](includes/cds_long_md.md)] como usted** para que [!INCLUDE[d365fin](includes/d365fin_md.md)] pueda, en nombre del administrador, automáticamente un usuario de la aplicación [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration no interactivo y sin licencia, asignar roles de seguridad a este usuario y deplegar la solución [!INCLUDE[d365fin](includes/d365fin_md.md)] Base CDS Integration en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Este permiso se usa solo una vez durante la configuración de la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
> * El permiso **Tener acceso completo a Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** se necesita para que el usuario de la aplicación [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration creado automáticamente pueda obtener acceso a los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] que se sincronizarán. 
> * El permiso **Iniciar sesión y leer su perfil** se necesita para verificar que el inicio de sesión del usuario realmente tenga asignado el rol de seguridad del administrador del sistema en [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
>
> Al dar su consentimiento en nombre de la organización, el administrador da derecho a la aplicación de Azure registrada denominada [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration a [!INCLUDE[d365fin](includes/cds_long_md.md)] para sincronizar datos usando las credenciales de usuario automáticamente creadas de [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Para usar la guía de configuración asistida para Configurar la conexión de Common Data Service 
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración asistida** y luego elija el vínculo relacionado.
2. Elija **Configurar la conexión de Common Data Service** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.

### <a name="to-create-or-maintain-the-connection-manually"></a>Para crear o mantener la conexión manualmente
El procedimiento siguiente describe cómo configurar la conexión manualmente en la página **Configuración de conexión de CDS**. También es la página donde administra los valores para la integración.

1. Elija el icono de ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de conexión de CDS** y luego elija el enlace relacionado.
2. Escriba la siguiente información para la conexión de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Campo|Descripción|
|-----|-----|
|**URL de entorno**|Si posee entornos en [!INCLUDE[d365fin](includes/cds_long_md.md)], los encontraremos cuando ejecute la guía de configuración. Si desea conectarse a un entorno diferente en otro suscriptor, puede introducir las credenciales de administrador del entorno y lo descubriremos. |
|**Habilitado**|Comience a usar la integración. Si no activa la conexión ahora, la configuración de la conexión se guardará pero los usuarios no podrán tener acceso a los datos de [!INCLUDE[d365fin](includes/cds_long_md.md)] desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede volver a esta página y activar la conexión más adelante.  |

3. En el campo **Modelo de propiedad**, elija si desea una entidad de equipo en [!INCLUDE[d365fin](includes/cds_long_md.md)] para poseer nuevos registros o uno o más usuarios específicos. Si elige **Persona**, debe especificar cada usuario. Si elige **Equipo**, la unidad de negocio predeterminada BCI_Company se mostrará en el campo **Unidad de negocios emparejada**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Para probar la configuración de conexión, elija **Conexión** y luego **Probar conexión**.  

    > [!NOTE]  
    >  Si el cifrado de datos no se ha habilitado en [!INCLUDE[d365fin](includes/d365fin_md.md)], se le preguntará si desea habilitarlo. Si desea habilitar el cifrado de datos, seleccione **Sí** y proporcione la información necesaria. Si no, elija **No**. Puede habilitar el cifrado de datos más adelante. Para obtener más información, consulte [Cifrado de datos en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) en la ayuda para desarrolladores y administradores.  

5. Si aún no está configurada la sincronización de [!INCLUDE[d365fin](includes/cds_long_md.md)], se le preguntará si desea utilizar la configuración de sincronización predeterminada. Dependiendo de si desea mantener los registros alineados en [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)], elija **Sí** o **No**.

## <a name="connecting-on-premises-versions"></a>Conexión a las versiones locales
Para conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] local a [!INCLUDE[d365fin](includes/cds_long_md.md)], debe especificar alguna información en la página **Configuración de la conexión de Common Data Service**.

Si quiere conectarte usando una cuenta de Azure Active Directory (Azure AD), debe registrar una solicitud en Azure AD, y proporcionar el identificador de la aplicación, el secreto de Key Vault y redirigir a la URL que se va a utilizar. La URL de redireccionamiento se rellena previamente y debería funcionar para la mayoría de las instalaciones. Debe configurar su instalación para usar HTTPS. Para más información, vea [Configuración SSL para proteger la conexión del cliente web de Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si está configurando su servidor para tener una página de inicio diferente, siempre puede cambiar la dirección URL. El secreto del cliente se guardará como una cadena encriptada en su base de datos. 

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Para registrar una solicitud en Azure AD para conectarse desde Business Central a Common Data Service
Se parte de la base que para los siguientes pasos está usando Azure AD para gestionar identidades y accesos. Para obtener más información sobre cómo registrar una aplicación en Azure AD, vea [Inicio rápido: Registrar una aplicación con la plataforma de identidad de Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app). Si no usa Azure AD, vea [Usar otro servicio de administración de identidades y accesos](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service). 

1. En el Portal de Azure, en **Administrar** en el oanel de navegación, elija **Autenticación**. 
2. En **Redirigir URL**, agregue la URL de redireccionamiento que se sugiere en la página **Configuración de la conexión de Common Data Service** en [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. En **Administrar**, elija **Permisos de API**.
4. En **Permisos configurados**, elija **Agregar un permiso**, y luego agregue permisos delegados en la pestaña **API de Microsoft** de la siguiente manera:
    * Para Business Central, agregue el permiso **Financials.ReadWrite.All**.
    * Para Dynamics CRM, agregue el permiso **person_impersonation**. 

> [!NOTE]
> El nombre de la API de Dynamics CRM puede cambiar.

5.  En **Administrar**, elija **Certificados y secretos** y, luego, cree un nuevo secreto para la aplicación. Usará el secreto en [!INCLUDE[d365fin](includes/d365fin_md.md)], en el campo **Secreto del cliente** en la página **Configuración de la conexión Common Data Service** o lo almacenará en un almacenamiento seguro y lo proporcionará en un suscriptor de eventos como se describe anteriormente en este tema.
6. Elija **Panorama** y luego encuentre el valor **Id. de la aplicación (cliente)**. Este es el identificador de cliente de su aplicación. Debe especificarlo en la página **Configuración de la conexión de Common Data Service** en el campo **Id. del cliente** o almacenarlo en un almacenamiento seguro y proporcionarlo en un suscriptor de eventos.
7. En [!INCLUDE[d365fin](includes/d365fin_md.md)], en la página **Configuración de la conexión de Common Data Service**, en el campo **URL del entorno**, especifique la URL para su entorno de [!INCLUDE[d365fin](includes/cds_long_md.md)].
8. Para habilitar la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)], active el control de alternancia a **Habilitada**.
9. Inicie sesión con su cuenta de administrador para Azure Active Directory (esta cuenta debe tener una licencia válida para [!INCLUDE[d365fin](includes/cds_long_md.md)] y ser administrador en su entorno de [!INCLUDE[d365fin](includes/cds_long_md.md)]). Después de iniciar sesión, se le pedirá que permita que su aplicación registrada inicie sesión en [!INCLUDE[d365fin](includes/cds_long_md.md)] en nombre de la organización. Debe dar su consentimiento para completar la configuración.

   > [!NOTE]
   > Si no se le solicita que inicie sesión con su cuenta de administrador, probablemente se deba a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de https://login.microsoftonline.com.

#### <a name="using-another-identity-and-access-management-service"></a>Usar otro servicio de administración de identidades y accesos
Si no estas usando Azure Active Directory para administrar las identidades y el acceso, necesitará ayuda de un desarrollador. Si prefiere almacenar el identificador y el secreto de la aplicación en una ubicación diferente, puede dejar en blanco los campos Id . del cliente y Secreto del cliente y escribir una extensión para obtener el identificador y el secreto de la ubicación. Puede proporcionar el secreto en tiempo de ejecución suscribiéndose a los eventos OnGetCDSConnectionClientId y OnGetCDSConnectionClientSecret en codeunit 7201 "Impl. de CDS Integration".

### <a name="to-disconnect-from-d365fin"></a>Para desconectar de [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Elija el icono de ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de conexión de CDS** y luego elija el enlace relacionado.
2. En la página **Configuración de conexión de CDS**, desactive **Habilitado**.  

## <a name="see-also"></a>Consulte también  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  
