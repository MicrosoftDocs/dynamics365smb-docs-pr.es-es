---
title: Conectar a Microsoft Dataverse
description: Puede integrar otras aplicaciones con Business Central a través de Microsoft Dataverse. Este artículo proporciona consejos y trucos para configurar las conexiones.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/26/2021
ms.author: bholtorf
ms.openlocfilehash: ebe708efacbaa03d5f10deb7b21b090222f28818
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6063482"
---
# <a name="connect-to-microsoft-dataverse"></a>Conectar a Microsoft Dataverse

[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Este tema describe cómo configurar una conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Por lo general, las empresas crean la conexión para integrar y sincronizar datos con otra aplicación empresarial de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Antes de comenzar

Hay algunos datos que debe tener listos para crear la conexión:  

* La dirección URL del entorno de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] al que desea conectarse. Si usa la guía de configuración asistida **Configuración de conexión de Dataverse** para crear la conexión descubriremos los entornos, pero también puede introducir la URL de otro entorno en su suscriptor.  
* El nombre de usuario y la contraseña de una cuenta que tenga permisos de administrador en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Si tiene [!INCLUDE[prod_short](includes/prod_short.md)], lanzamiento de versiones 1 de 2020, local, versión 16.5, lea el artículo [Algunos problemas conocidos](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Deberá completar la solución alternativa descrita antes de poder crear su conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* La divisa local de la empresa en [!INCLUDE[prod_short](includes/prod_short.md)] debe ser la misma que la divisa base de la transacción en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Después de que se establece una transacción base en [!INCLUDE[cds_long_md](includes/cds_long_md.md)], no se puede cambiar. Para más información, vea [Entidad de divisa de transacción (divisa)](/powerapps/developer/data-platform/transaction-currency-currency-entity). Esto significa que todas las empresas [!INCLUDE[prod_short](includes/prod_short.md)] que conecta a una organización [!INCLUDE[cds_long_md](includes/cds_long_md.md)] deben utilizar la misma divisa.

> [!IMPORTANT]
> Su ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] no debe estar en modo de administración. El modo de administración hará que la conexión falle porque la cuenta de usuario de integración para la conexión no tiene permisos de administrador. Para obtener más información, consulte [Modo de administración](/power-platform/admin/admin-mode).

> [!Note]
> Estos pasos describen el procedimiento para [!INCLUDE[prod_short](includes/prod_short.md)] en línea.
> Si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] on-premises y no está utilizando la cuenta de Azure Active Directory para conectarse a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], también debe especificar un nombre de usuario y una contraseña de una cuenta de usuario para la integración. Esta cuenta se conoce como la cuenta de "usuario de integración". Si está usando una cuenta de Azure Active Directory la cuenta de usuario de integración no es necesaria ni se muestra. El usuario de integración se configurará automáticamente y no requiere una licencia.

## <a name="set-up-a-connection-to-cds_long_md"></a>Configurar una conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

En todos los tipos de autenticación distintos de la autenticación de Microsoft 365, configure la conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en la página **Configuración de la conexión de Dataverse**. Para la autenticación de Microsoft 365, es recomendable que use la guía de configuración asistida **Configuración de conexión de Dataverse**. La guía simplifica la configuración de la conexión y permite especificar características avanzadas, como el modelo de propiedad y la sincronización inicial.  

> [!IMPORTANT]
> Durante la configuración de la conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], se pedirá al administrador que otorgue los siguientes permisos a la aplicación de Azure registrada denominada Integración de [!INCLUDE[prod_short](includes/prod_short.md)] para [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * Se necesita permiso de **Acceso a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] como el suyo** para que [!INCLUDE[prod_short](includes/prod_short.md)] pueda, en nombre del administrador, crear automáticamente un usuario de la aplicación de integración [!INCLUDE[prod_short](includes/prod_short.md)] no interactivo y sin licencia, asignar roles de seguridad a este usuario e implmentar la solución de integración [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Este permiso se usa solo una vez durante la configuración de la conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * El permiso **Tener acceso completo a Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** se necesita para que el usuario de la aplicación [!INCLUDE[prod_short](includes/prod_short.md)] Integration creado automáticamente pueda obtener acceso a los datos de [!INCLUDE[prod_short](includes/prod_short.md)] que se sincronizarán.  
> * El permiso **Iniciar sesión y leer su perfil** se necesita para verificar que el inicio de sesión del usuario realmente tenga asignado el rol de seguridad del administrador del sistema en [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Al dar su consentimiento en nombre de la organización, el administrador da derecho a la aplicación de Azure registrada denominada [!INCLUDE[prod_short](includes/prod_short.md)] Integration a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] para sincronizar datos usando las credenciales de usuario automáticamente creadas de [!INCLUDE[prod_short](includes/prod_short.md)] Integration.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Para usar la guía de configuración asistida Configuración de conexión de Dataverse
La guía de configuración de la conexión de Dataverse puede facilitar la conexión de las aplicaciones e incluso puede ayudarlo a ejecutar una sincronización inicial. Si elige ejecutar la sincronización inicial, [!INCLUDE[prod_short](includes/prod_short.md)] revisará los datos en ambas aplicaciones y brindará recomendaciones sobre cómo abordar la sincronización inicial. La siguiente tabla describe las recomendaciones.

|Recomendación  |Descripción  |
|---------|---------|
|**Sincronización completa**|Los datos solo existen en [!INCLUDE[prod_short](includes/prod_short.md)], o solo en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. ¿La recomendación es sincronizar todos los datos del servicio que lo tiene con el otro servicio?|
|**Sin sincronización**|Los datos existen en ambas aplicaciones y ejecutar una sincronización completa duplicaría los datos. La recomendación es acoplar registros.|
|**Dependencia no satisfecha**|Los datos existen en ambas aplicaciones, pero la fila o tabla no se puede sincronizar porque depende de una fila o tabla que tiene la recomendación de Sin sincronización. Por ejemplo, si los clientes no se pueden sincronizar, los datos de los contactos que dependen de los datos del cliente tampoco se pueden sincronizar.|

> [!IMPORTANT]
> Normalmente, solo utiliza la sincronización completa cuando integra las aplicaciones por primera vez y solo una aplicación contiene datos. La sincronización completa puede ser útil en un entorno de demostración porque crea y acopla automáticamente registros en cada aplicación, lo que hace que sea más rápido comenzar a trabajar con datos sincronizados. Sin embargo, solo debe ejecutar la sincronización completa si desea una fila en [!INCLUDE[prod_short](includes/prod_short.md)] para cada fila en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] para las asignaciones de tablas. De lo contrario, el resultado puede ser registros duplicados.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración asistida** y luego elija el vínculo relacionado.
2. Elija **Configurar una conexión a Microsoft Dataverse** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.

> [!NOTE]
> Si no se le solicita que inicie sesión con su cuenta de administrador, probablemente se deba a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Para crear o mantener la conexión manualmente

El procedimiento siguiente describe cómo configurar la conexión manualmente en la página **Configuración de conexión de Dataverse**. También es la página donde administra los valores para la integración.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de la conexión de Dataverse** y luego elija el enlace relacionado.
2. Escriba la siguiente información para la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Campo|Descripción|
    |-----|-----|
    |**URL de entorno**|Si posee entornos en [!INCLUDE[cds_long_md](includes/cds_long_md.md)], los encontraremos cuando ejecute la guía de configuración. Si desea conectarse a un entorno diferente en otro suscriptor, puede introducir las credenciales de administrador del entorno y lo descubriremos. |
    |**Habilitado**|Comience a usar la integración. Si no activa la conexión ahora, la configuración de la conexión se guardará pero los usuarios no podrán tener acceso a los datos de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] desde [!INCLUDE[prod_short](includes/prod_short.md)]. Puede volver a esta página y activar la conexión más adelante.  |

3. En el campo **Modelo de propiedad**, elija si desea una tabla de equipo en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] para poseer nuevos registros o uno o más usuarios específicos. Si elige **Persona**, debe especificar cada usuario. Si elige **Equipo**, la unidad de negocio predeterminada se mostrará en el campo **Unidad de negocios emparejada**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|
4. Para probar la configuración de conexión, elija **Conexión** y luego **Probar conexión**.  

    > [!NOTE]  
    > Si el cifrado de datos no se ha habilitado en [!INCLUDE[prod_short](includes/prod_short.md)], se le preguntará si desea habilitarlo. Si desea habilitar el cifrado de datos, seleccione **Sí** y proporcione la información necesaria. Si no, elija **No**. Puede habilitar el cifrado de datos más adelante. Para obtener más información, consulte [Cifrado de datos en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) en la ayuda para desarrolladores y administradores.  
5. Si aún no está configurada la sincronización de [!INCLUDE[cds_long_md](includes/cds_long_md.md)], se le preguntará si desea utilizar la configuración de sincronización predeterminada. Dependiendo de si desea mantener los registros alineados en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)], elija **Sí** o **No**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Conexión a las versiones locales

Para conectar [!INCLUDE[prod_short](includes/prod_short.md)] local a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], debe especificar alguna información en la página **Configuración de la conexión de Dataverse**.

Si quiere conectarte usando una cuenta de Azure Active Directory (Azure AD), debe registrar una solicitud en Azure AD, y proporcionar el identificador de la aplicación, el secreto de Key Vault y redirigir a la URL que se va a utilizar. La URL de redireccionamiento se rellena previamente y debería funcionar para la mayoría de las instalaciones. Debe configurar su instalación para usar HTTPS. Para más información, vea [Configuración SSL para proteger la conexión del cliente web de Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si está configurando su servidor para tener una página de inicio diferente, siempre puede cambiar la dirección URL. El secreto del cliente se guardará como una cadena encriptada en su base de datos. 

### <a name="prerequisites"></a>Requisitos previos

Dataverse debe usar uno de los siguientes tipos de autenticación:

* Office365 (heredado)

  > [!IMPORTANT]
  > A partir de abril de 2022, Office365 (heredado) ya no será compatible. Para obtener más información, consulte [Próximos cambios importantes (ceses de uso) en Power Apps, Power Automate y aplicaciones de interacción con el cliente](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (moderno, basado en secreto de cliente OAuth2)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Para registrar una solicitud en Azure AD para conectarse desde Business Central a Dataverse

Se parte de la base que para los siguientes pasos está usando Azure AD para gestionar identidades y accesos. Para obtener más información sobre cómo registrar una aplicación en Azure AD, vea [Inicio rápido: Registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. En el Portal de Azure, en **Administrar** en el oanel de navegación, elija **Autenticación**.  
2. En **Redirigir URL**, agregue la URL de redireccionamiento que se sugiere en la página **Configuración de la conexión de Dataverse** en [!INCLUDE[prod_short](includes/prod_short.md)].
3. En **Administrar**, elija **Permisos de API**.
4. En **Permisos configurados**, elija **Agregar un permiso**, y luego agregue permisos delegados en la pestaña **API de Microsoft** de la siguiente manera:
    * Para Business Central, agregue el permiso **Financials.ReadWrite.All**.
    * Para Dynamics CRM, agregue el permiso **person_impersonation**.  

    > [!NOTE]
    > El nombre de la API de Dynamics CRM puede cambiar.

5. En **Administrar**, elija **Certificados y secretos** y, luego, cree un nuevo secreto para la aplicación. Usará el secreto en [!INCLUDE[prod_short](includes/prod_short.md)], en el campo **Secreto del cliente** en la página **Configuración de la conexión Dataverse** o lo almacenará en un almacenamiento seguro y lo proporcionará en un suscriptor de eventos como se describe anteriormente en este tema.
6. Elija **Panorama** y luego encuentre el valor **Id. de la aplicación (cliente)**. Este es el identificador de cliente de su aplicación. Debe especificarlo en la página **Configuración de la conexión de Dataverse** en el campo **Id. del cliente** o almacenarlo en un almacenamiento seguro y proporcionarlo en un suscriptor de eventos.
7. En [!INCLUDE[prod_short](includes/prod_short.md)], en la página **Configuración de la conexión de Dataverse**, en el campo **URL del entorno**, especifique la URL para su entorno de [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
8. Para habilitar la conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], active el control de alternancia a **Habilitada**.
9. Inicie sesión con su cuenta de administrador para Azure Active Directory (esta cuenta debe tener una licencia válida para [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y ser administrador en su entorno de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Después de iniciar sesión, se le pedirá que permita que su aplicación registrada inicie sesión en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en nombre de la organización. Debe dar su consentimiento para completar la configuración.

   > [!NOTE]
   > Si no se le solicita que inicie sesión con su cuenta de administrador, probablemente se deba a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-cds_long_md"></a>Para desconectar de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de la conexión de Dataverse** y luego elija el enlace relacionado.
2. En la página **Configuración de conexión de Dataverse**, desactive **Habilitado**.  

## <a name="see-also"></a>Consulte también

[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]