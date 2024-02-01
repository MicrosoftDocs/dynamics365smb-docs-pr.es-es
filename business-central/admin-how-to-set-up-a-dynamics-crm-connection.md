---
title: Conectar a Microsoft Dataverse (contiene vídeo)
description: Configuración de una conexión entre Business Central y Dataverse Las empresas suelen crear la conexión para integrar datos con otra aplicación empresarial de Dynamics 365.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 09/28/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="connect-to-microsoft-dataverse"></a>Conectar a Microsoft Dataverse

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Este artículo describe cómo configurar una conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Por lo general, las empresas crean la conexión para integrar y sincronizar datos con otra aplicación empresarial de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Antes de comenzar

Hay algunos datos que debe tener listos para crear la conexión:  

* La dirección URL del entorno de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] al que desea conectarse. Si usa la guía de configuración asistida **Configuración de la conexión de Dataverse** para crear la conexión, encontraremos sus entornos. También puede introducir la URL de otro entorno en su inquilino.  
* El nombre de usuario y la contraseña de una cuenta que tenga permisos de administrador en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Si tiene [!INCLUDE[prod_short](includes/prod_short.md)], lanzamiento de versiones 1 de 2020, local, versión 16.5, lea el artículo [Algunos problemas conocidos](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Deberá completar la solución alternativa descrita antes de poder crear su conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* Las divisas locales que utiliza cada empresa. Las empresas de [!INCLUDE [prod_short](includes/prod_short.md)] pueden conectarse a un entorno de [!INCLUDE [cds_long_md](includes/cds_long_md.md)] que tenga una divisa base distinta a su moneda local. Para obtener más información sobre cómo administrar configuraciones multidivisa, vaya a [Permitir diferentes divisas](#allow-for-different-currencies).

> [!IMPORTANT]
> Su ambiente [!INCLUDE[cds_long_md](includes/cds_long_md.md)] no debe estar en modo de administración. El modo de administración hará que la conexión falle porque la cuenta de usuario de integración para la conexión no tiene permisos de administrador. Para obtener más información, consulte [Modo de administración](/power-platform/admin/admin-mode).

> [!Note]
> Estos pasos describen el procedimiento para [!INCLUDE[prod_short](includes/prod_short.md)] en línea.
> Si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] on-premises y no está utilizando la cuenta de Microsoft Entra para conectarse a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], también debe especificar un nombre de usuario y una contraseña de una cuenta de usuario para la integración. Esta cuenta se conoce como la cuenta de "usuario de integración". Si está usando una cuenta de Microsoft Entra, la cuenta de usuario de integración no es necesaria ni se muestra. El usuario de integración se configurará automáticamente y no requiere una licencia.

## <a name="allow-for-different-currencies"></a>Permitir distintas divisas

Las empresas de [!INCLUDE [prod_short](includes/prod_short.md)] pueden conectarse a un entorno de [!INCLUDE [cds_long_md](includes/cds_long_md.md)] que tenga una divisa base distinta a su moneda local.

> [!NOTE]
> La sincronización de varias monedas requiere que utilice una sincronización unidireccional, de [!INCLUDE [prod_short](includes/prod_short.md)] a [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Para obtener más información sobre la divisa base en [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vaya a [Entidad de divisa de transacción (divisa)](/powerapps/developer/data-platform/transaction-currency-currency-entity). 

Para obtener más información sobre divisas en [!INCLUDE [prod_short](includes/prod_short.md)], vaya a [Divisas en Business Central](finance-currencies.md).

Para permitir diferentes monedas, antes de conectarse, asegúrese de haber especificado las siguientes configuraciones:

* La configuración de divisa de transacción base en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] tiene el código de divisa que se especifica en la página **Divisas** en [!INCLUDE [prod_short](includes/prod_short.md)].
* Hay al menos un tipo de cambio especificado para la moneda en [!INCLUDE [prod_short](includes/prod_short.md)] en la página **Tipos de cambio de moneda**.

Cuando habilita la conexión a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], [!INCLUDE [prod_short](includes/prod_short.md)] agrega su divisa local a la entidad **Divisa** en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. La moneda local usa la tasa de cambio del campo **Factor de divisa** en la página **Tasas de cambio de divisa**.

Debido a que la sincronización de moneda es unidireccional, desde [!INCLUDE [prod_short](includes/prod_short.md)] a [!INCLUDE [cds_long_md](includes/cds_long_md.md)], las cantidades monetarias se convierten y sincronizan de la siguiente manera:

* Si está en los importes en la moneda base [!INCLUDE [cds_long_md](includes/cds_long_md.md)] se convierten a la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] según el último tipo de cambio sincronizado desde [!INCLUDE [prod_short](includes/prod_short.md)].
* Los importes en la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] se sincronizan con la moneda local [!INCLUDE [prod_short](includes/prod_short.md)] en una de las monedas adicionales (no base) en [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

## <a name="set-up-a-connection-to-"></a>Configurar una conexión a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

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

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y luego elija el enlace relacionado.
2. Elija **Configurar una conexión a Microsoft Dataverse** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.

> [!NOTE]
> Si no se le solicita que inicie sesión con su cuenta de administrador, probablemente se deba a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Para crear o mantener la conexión manualmente

El procedimiento siguiente describe cómo configurar la conexión manualmente en la página **Configuración de conexión de Dataverse**. La página **Configuración de la conexión de Dataverse** es donde administra la configuración de la integración.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Dataverse** y luego elija el enlace relacionado.
2. Escriba la siguiente información para la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Campo|Descripción|
    |-----|-----|
    |**URL de entorno**|Si posee entornos en [!INCLUDE[cds_long_md](includes/cds_long_md.md)], los encontraremos cuando ejecute la guía de configuración. Si desea conectarse a un entorno diferente en otro inquilino, puede introducir las credenciales de administrador del entorno y lo encontraremos. |
    |**Habilitado**|Comience a usar la integración. Si no activa la conexión ahora, la configuración de la conexión se guardará pero los usuarios no podrán tener acceso a los datos de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] desde [!INCLUDE[prod_short](includes/prod_short.md)]. Puede volver a esta página y activar la conexión más adelante.  |

3. En el campo **Modelo de propiedad**, elija si desea una tabla de equipo en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] para poseer nuevos registros o uno o más usuarios específicos. Si elige **Persona**, debe especificar cada usuario. Si elige **Equipo**, la unidad de negocio predeterminada se mostrará en el campo **Unidad de negocios emparejada**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Para probar la configuración de conexión, elija **Conexión** y luego **Probar conexión**.  

    > [!NOTE]  
    > Si el cifrado de datos no se ha habilitado en [!INCLUDE[prod_short](includes/prod_short.md)], se le preguntará si desea habilitarlo. Si desea habilitar el cifrado de datos, seleccione **Sí** y proporcione la información necesaria. Si no, elija **No**. Puede habilitar el cifrado de datos más adelante. Para obtener más información, consulte [Cifrado de datos en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) en la ayuda para desarrolladores y administradores.  
5. Si aún no está configurada la sincronización de [!INCLUDE[cds_long_md](includes/cds_long_md.md)], se le preguntará si desea utilizar la configuración de sincronización predeterminada. Dependiendo de si desea mantener los registros alineados en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)], elija **Sí** o **No**.

<!--
## <a name="show-me-the-process"></a>Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Personalizar el emparejamiento basado en coincidencias

A partir del lanzamiento de versiones 2 de 2021, un administrador puede introducir criterios para emparejar registros basados en coincidencias. Puede iniciar el algoritmo para emparejar registros desde los siguientes lugares en [!INCLUDE [prod_short](includes/prod_short.md)]:

* Lista de páginas que muestran registros sincronizados con [!INCLUDE [cds_long_md](includes/cds_long_md.md)], como las páginas Clientes y Productos.  

    Seleccione varios registros y luego elija la acción **Relacionado**, elija **Dataverse**, elija **Emparejamiento** y luego **Emparejamiento basado en coincidencias**.

    Cuando inicia el proceso de emparejamiento basado en coincidencias desde una lista de datos maestros, se programa un trabajo de emparejamiento después de especificar los criterios de emparejamiento.  
* La página **Revisión sincronización completa de Dataverse**.  

    Cuando el proceso de sincronización completo detecta que tiene registros desemparejados en [!INCLUDE [prod_short](includes/prod_short.md)] y en [!INCLUDE [cds_long_md](includes/cds_long_md.md)], aparece un vínculo **Seleccionar criterios de emparejamiento** para la tabla de integración.  

    Puede iniciar el proceso **Ejecutar sincronización completa** desde las páginas **Configuración de la conexión de Dataverse** y **Configuración de conexión de Dynamics 365**. También puede iniciarlo en la guía de configuración asistida **Configurar una conexión a Dataverse** cuando complete su configuración.  

    Cuando inicie el proceso de emparejamiento basado en coincidencias desde la página **Revisión sincronización completa de Dataverse**, se programa un trabajo de emparejamiento después de completar la configuración.  
* La lista **Asignaciones de tablas de integración**.  

    Seleccione una asignación, elija la acción **Emparejamiento** y luego elija **Emparejamiento basado en coincidencias**.

    Cuando inicia el proceso de emparejamiento basado en coincidencias desde una asignación de tablas de integración, se ejecuta un trabajo de emparejamiento para todos los registros desemparejados en la asignación. También puede seleccionar registros desemparejados en la lista para ejecutar el trabajo solo para esos registros.

En los tres casos, la página **Seleccionar criterios de emparejamiento** se abre para que pueda definir los criterios de emparejamiento relevantes. En esta página, personalice el emparejamiento con las siguientes tareas:

* Elija los campos que desea utilizar para hacer coincidir registros de [!INCLUDE [prod_short](includes/prod_short.md)] con entidades [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Puede especificar si la coincidencia distingue entre mayúsculas y minúsculas.  

* Especifique si desea sincronizar después de emparejar registros. Si los registros utilizan una asignación bidireccional, también puede especificar qué sucede si los conflictos se indican en la página **Resolver conflictos de actualizaciones**.  

* Priorice el orden en el que se buscan los registros especificando un *prioridad de coincidencia* para los campos de asignación relevantes. [!INCLUDE [prod_short](includes/prod_short.md)] buscará una coincidencia en orden ascendente según el valor en el campo **Prioridad de coincidencia**. Un valor en blanco en el campo **Prioridad de coincidencia** es igual a la prioridad 0, que es la prioridad más alta. Los campos con la prioridad 0 se consideran en primer lugar.  

* Especifique si desea crear una nueva instancia de entidad en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] en caso de que no se pueda encontrar ninguna coincidencia desemparejada única utilizando los criterios de coincidencia. Para activar esta capacidad, elija la acción **Crear nuevo si no se encuentra una coincidencia**.  

### <a name="view-the-results-of-the-coupling-job"></a>Ver los resultados del trabajo de emparejamiento

Para ver los resultados del trabajo de emparejamiento, abra la página **Asignaciones de tablas de integración**, seleccione la asignación relevante, elija la acción **Emparejamiento** y luego elija la acción **Registro de trabajo de emparejamiento de integración**.  

Si los registros no se emparejan, puede elegir el valor en la columna **Erróneo** para abrir una lista de errores que describen por qué sucedió eso.  

Normalmente, el emparejamiento produce un error por las siguientes razones:

* No se definieron criterios de coincidencia

    Vuelva a ejecutar el emparejamiento basado en coincidencias, pero recuerde definir los criterios de acoplamiento.

* No se encontraron coincidencias para los campos especificados en los criterios de coincidencia

    Repita el emparejamiento usando diferentes campos.

* Se encontraron múltiples coincidencias para varios registros, según los campos especificados en los criterios de coincidencia  

    Repita el emparejamiento usando diferentes campos.

* Se encontró una coincidencia, pero el registro ya está emparejado a un registro en [!INCLUDE [prod_short](includes/prod_short.md)]  

    Repita el emparejamiento usando diferentes campos o investigue por qué esa entidad de [!INCLUDE [cds_long_md](includes/cds_long_md.md)] está emparejada al registro en [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Para ayudarle a obtener una descripción general del progreso de emparejamiento, el campo **Emparejado con Dataverse** muestra si un registro está emparejado con una entidad [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Puede usar el campo **Emparejado con Dataverse** para filtrar la lista de registros que está sincronizando.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Actualice las conexiones de Business Central Online para usar autenticación basada en certificados

> [!NOTE]
> Esta sección es relevante solo para los inquilinos de [!INCLUDE[prod_short](includes/prod_short.md)] en línea hospedados por Microsoft. Los inquilinos online hospedados por ISV y las instalaciones locales no se ven afectados.

En abril de 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] está abandonando el tipo de autenticación de Office365 (nombre de usuario/contraseña). Para más información, vea [Cese en el uso del tipo de autenticación de Office365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Además, en marzo de 2022, [!INCLUDE[prod_short](includes/prod_short.md)] está abandonando el uso de la autenticación de servicio a servicio basada en el secreto de cliente para los inquilinos en línea. Debe usar la autenticación de servicio a servicio basada en certificados para las conexiones a [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Los inquilinos de [!INCLUDE[prod_short](includes/prod_short.md)] en línea hospedados por ISV y las instalaciones locales pueden seguir utilizando secretos de cliente para la autenticación.

Para evitar interrumpir las integraciones, _debe actualizar_ la conexión para utilizar autenticación basada en certificados. Aunque el cambio está programado para marzo de 2022, le recomendamos encarecidamente que actualice lo antes posible. Los siguientes pasos describen cómo actualizar a la autenticación basada en certificados. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Para actualizar la conexión de Business Central Online para usar autenticación basada en certificados

1. Dependiendo de si se integra con Dynamics 365 Sales, realice una de las siguientes acciones:
   * Si lo hace, abra la página **Configuración de la conexión de Microsoft Dynamics 365**.
   * Si no lo hace, abra la página **Configuración de la conexión de Dataverse**.
2. Elija **Conexión** y luego **Usar autenticación de certificado** para actualizar la conexión para utilizar autenticación basada en certificados.
3. Inicie sesión con credenciales de administrador para Dataverse. Debería tardar menos de un minuto en iniciar sesión.

> [!NOTE]
> Debe repetir estos pasos en cada entorno de [!INCLUDE[prod_short](includes/prod_short.md)], incluidos los entornos de producción y entorno aislado, y en cada empresa donde tenga una conexión con [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Conectar versiones locales

Para conectar [!INCLUDE[prod_short](includes/prod_short.md)] local a [!INCLUDE[cds_long_md](includes/cds_long_md.md)], debe especificar alguna información en la página **Configuración de la conexión de Dataverse**.

Para conectarse usando una cuenta de Microsoft Entra, debe registrar una aplicación en Microsoft Entra ID. Tendrá que proporcionar el identificador de la aplicación, el secreto de Key Vault y la URL de redireccionamiento que se va a utilizar. La URL de redireccionamiento se rellena previamente y debería funcionar para la mayoría de las instalaciones. Debe configurar su instalación para usar HTTPS. Para más información, vea [Configuración SSL para proteger la conexión del cliente web de Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si está configurando su servidor para tener una página de inicio diferente, puede cambiar la dirección URL. El secreto del cliente se guardará como una cadena encriptada en su base de datos. 

### <a name="to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-dataverse"></a>Para registrar una solicitud en Microsoft Entra ID para conectarse desde Business Central a Dataverse

Se parte de la base que para los siguientes pasos está usando Microsoft Entra ID para gestionar identidades y accesos. Para obtener más información sobre cómo registrar una aplicación en Microsoft Entra ID, vea [Inicio rápido: Registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app). 

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
9. Inicie sesión con su cuenta de administrador para Microsoft Entra ID (esta cuenta debe tener una licencia válida para [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y ser administrador en su entorno de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]). Después de iniciar sesión, se le pedirá que permita que su aplicación registrada inicie sesión en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en nombre de la organización. Debe dar su consentimiento para completar la configuración.

   > [!NOTE]
   > Si no se le solicita que inicie sesión con su cuenta de administrador, probablemente se deba a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-"></a>Para desconectar de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Dataverse** y luego elija el enlace relacionado.
2. En la página **Configuración de conexión de Dataverse**, desactive **Habilitado**.  

## <a name="see-also"></a>Consulte también

[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
