---
title: Config. registro correo elect.
description: Aprenda a convertir las interacciones de correo electrónico entre vendedores y clientes en oportunidades de venta reales.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos

Aproveche al máximo las comunicaciones entre sus vendedores y sus clientes transformando los intercambios de correos electrónicos en oportunidades procesables. [!INCLUDE[prod_short](includes/prod_short.md)] puede funcionar con Exchange Online para mantener un registro de los mensajes entrantes y salientes. Puede ver y analizar el contenido de cada mensaje en la página **Movimientos del log de interacción**.

> [!IMPORTANT]
> Para [!INCLUDE[prod_short](includes/prod_short.md)] en línea, [!INCLUDE[prod_short](includes/prod_short.md)] y Exchange Online deben estar en el mismo suscriptor.

## <a name="to-set-up-email-logging"></a><a name="to-set-up-email-logging"></a><a name="to-set-up-email-logging"></a>Para configurar el registro de correo electrónico

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurar carpetas públicas y reglas para registro de correo electrónico en Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Luego, te conectas [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online.

### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a><a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a><a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Configurar un buzón de correo compartido y las reglas para el registro de correo electrónico en Exchange Online

> [!NOTE]
> Estos pasos requieren acceso de administrador para Exchange Online.

Prepare un buzón compartido en el centro de administración de Exchange. Alternativamente, también puede usar Exchange Online PowerShell. Para más información, vea [Crear un buzón compartido](/microsoft-365/admin/email/create-a-shared-mailbox) o [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Si usa PowerShell de administración de Exchange, sus cambios están disponibles en el centro de administración de Exchange después de un tiempo. El retraso puede ser de varias horas.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a><a name="add-a-user-account-for-members-of-the-shared-mailbox"></a><a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Agregar una cuenta de usuario para los miembros del buzón compartido

La cuenta que utilizará para el registro de correo electrónico es una cuenta de Exchange Online. El trabajo programado usará la cuenta para conectar el buzón compartido y procesar correos electrónicos. Esta cuenta no debe estar asociada con una persona específica. Agregue la cuenta de correo electrónico a los miembros del buzón compartido. Para más información, vea [Usar el EAC para editar la delegación de buzones compartidos](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a><a name="allow-other-users-to-see-logged-emails"></a><a name="allow-other-users-to-see-logged-emails"></a>Permitir que otros usuarios vean los correos electrónicos registrados

Puede permitir que otro usuario abra un mensaje de correo electrónico en Exchange relacionado con una entrada del registro de interacción de [!INCLUDE[prod_short](includes/prod_short.md)]. Para hacer eso, dele al usuario el permiso ``Read`` en la carpeta **Archivo** en el buzón compartido. Para obtener más información, vea [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a>Crear reglas de flujo de correo

Las reglas de flujo de correo buscan condiciones específicas en los mensajes y toman medidas al respecto. Cree dos reglas de flujo de correo basadas en la información de la siguiente tabla. Para obtener más información, consulte [Administrar reglas de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) y [Acciones de regla de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Propósito  |Name  |Aplique esta regla si...  |Haga lo siguiente...  |
|---------|---------|---------|---------|
|Una regla para el correo electrónico entrante     |Registrar el correo electrónico enviado a esta organización|El remitente se encuentra fuera de la organización y el destinatario se encuentra dentro de la organización|Incluya en CCO la cuenta de correo electrónico que se especifica para el buzón compartido.|
|Una regla para el correo electrónico saliente     |Registrar el correo electrónico enviado desde esta organización|El remitente se encuentra dentro de la organización y el destinatario se encuentra fuera de la organización.|Incluya en CCO la cuenta de correo electrónico que se especifica para el buzón compartido.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] solo procesa mensajes en la carpeta Bandeja de entrada en el buzón compartido. Si una regla mueve mensajes de la Bandeja de entrada a otra carpeta, esos mensajes no se procesarán. Además, los mensajes de la carpeta Correo no deseado también se ignoran.

## <a name="set-up--to-log-email-messages"></a><a name="set-up--to-log-email-messages"></a><a name="set-up--to-log-email-messages"></a>Configurar [!INCLUDE[prod_short](includes/prod_short.md)] para registrar mensajes de correo electrónico

Comience con el registro de correo electrónico en dos sencillos pasos:

1. Conecte [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online para su suscripción de Microsoft 365. Exchange Online gestiona sus mensajes de correo electrónico. Hemos facilitado este paso al proporcionar una guía de configuración asistida. Solo necesita sus credenciales de administrador para su cuenta de administrador en Microsoft 365. Para comenzar la guía, vaya a la página **Configuración asistida** y, a continuación, seleccione la guía **Configurar registro de correo electrónico**.  

2. Asegúrese de que las direcciones de correo electrónico de sus vendedores y contactos en [!INCLUDE[prod_short](includes/prod_short.md)] son válidos. Para ello, para cada cliente o vendedor, abra la ficha **Contacto** o **Vendedor/Comprador** y consulte el campo **Correo electrónico**.

    > [!Tip]
    > Después de completar los pasos de la guía, puede comprobar si la conexión se ha realizado correctamente. Busque **Registro de correo electrónico**, elija **Acciones** y, a continuación, **Validar configuración**.

## <a name="view-email-message-exchanges-in-the-interaction-log"></a><a name="view-email-message-exchanges-in-the-interaction-log"></a><a name="view-email-message-exchanges-in-the-interaction-log"></a>Ver intercambios de mensajes de correo electrónico en el registro de interacciones

[!INCLUDE[prod_short](includes/prod_short.md)] crea una entrada en la página **Log de interacción** cada vez que un vendedor y un contacto intercambian un mensaje de correo electrónico. Para ver el registro de interacción, abra la tarjeta **Contacto** para la persona o elija **Relacionado** y, a continuación, elija **Historial** y luego **Mov. log interacción**. Hay algunas cosas que puede hacer con cada entrada del registro, por ejemplo:

* Ver el contenido del mensaje de correo electrónico que se ha intercambiado seleccionando **Proceso** y, después **Mostrar datos adjuntos**.
* Convierta un intercambio de correo electrónico en una oportunidad de venta. Si una entrada parece prometedora, puede convertirla en una oportunidad y luego administrar su progreso hasta una venta. Para convertir un intercambio de correo electrónico en una oportunidad, seleccione la entrada y después **Proceso**, y **Crear oportunidad**. Para obtener más información, consulte [Administrar oportunidades de venta](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online"></a><a name="mailbox-and-folder-limits-in-exchange-online"></a><a name="mailbox-and-folder-limits-in-exchange-online"></a>Límites de buzones y carpetas en Exchange Online

Hay límites de buzones y carpetas en Exchange Online, como límites para el tamaño de las carpetas y el número de mensajes. Para obtener más información, vea [Límites de Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) y [Límites de carpetas públicas en Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] almacena los mensajes de correo electrónico registrados en una carpeta en Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] también almacena un vínculo para cada mensaje registrado. Los vínculos abren los mensajes registrados en Exchange Online de las páginas Movimientos del log de interacción, Ficha de contacto y Ficha de vendedor en [!INCLUDE[prod_short](includes/prod_short.md)]. Si un mensaje registrado se mueve a otra carpeta, el vínculo se romperá. Por ejemplo, un mensaje puede moverse manualmente o Exchange Online podría iniciar automáticamente AutoSplit cuando se alcanza un límite de almacenamiento.

Los siguientes pasos pueden ayudarle a evitar romper vínculos a mensajes en formato Exchange Online.

1. No mueva los mensajes existentes a otra carpeta después de cambiar la configuración de registro de correo electrónico. Mantener los mensajes existentes donde están preservará los vínculos. Los vínculos a los mensajes en la nueva carpeta serán válidos.
2. Evite alcanzar los límites de buzones y carpetas. Si está a punto de alcanzar un límite, siga los siguientes pasos:
    1. Configurar un nuevo buzón compartido en Exchange Online.
    2. Actualice sus reglas de flujo de correo electrónico en Exchange Online.
    3. Actualice su configuración de registro de correo electrónico en Business Central en consecuencia

## <a name="connect-on-premises-versions-to-microsoft-exchange"></a><a name="connect-on-premises-versions-to-microsoft-exchange"></a><a name="connect-on-premises-versions-to-microsoft-exchange"></a>Conectar versiones locales a Microsoft Exchange

Puedes conectar [!INCLUDE[prod_short](includes/prod_short.md)] local a Exchange local o Exchange Online para el registro de correo electrónico. Para ambas versiones de Exchange, la configuración de la conexión está disponible en la página **Configuración de marketing**. Para Exchange Online, también puede utilizar una guía de configuración asistida.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## <a name="connect-to-exchange-on-premises"></a><a name="connect-to-exchange-on-premises"></a><a name="connect-to-exchange-on-premises"></a>Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## <a name="connect-to-exchange-online"></a><a name="connect-to-exchange-online"></a><a name="connect-to-exchange-online"></a>Conectar con Exchange Online

Para conectarse a Exchange Online debe registrar una aplicación en Azure Active Directory. Proporcione el identificador de la aplicación, el secreto de Key Vault y la URL de redireccionamiento que se va a utilizar para el registro. La URL de redireccionamiento se establece previamente y debería funcionar para la mayoría de las instalaciones. Para más información, vea [Para registrar una aplicación en Azure AD para conectarse desde Business Central a Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

También debe usar **OAuth2** como **Tipo de autenticación**. También debe registrar una aplicación en Azure Active Directory. Proporcione el identificador de la aplicación, el secreto de Key Vault y la URL de redireccionamiento que se va a utilizar para el registro. La URL de redireccionamiento se rellena previamente y debería funcionar para la mayoría de las instalaciones. Para más información, vea Para registrar una aplicación en Azure AD para conectarse desde Business Central a Exchange Online a continuación.

Debe configurar su instalación para usar HTTPS. Para más información, vea [Configuración SSL para proteger la conexión del cliente web de Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si está configurando su servidor para tener una página de inicio diferente, puede cambiar la dirección URL. El secreto del cliente se guardará como una cadena encriptada en su base de datos.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a><a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a><a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Para registrar una solicitud en Azure AD para conectarse desde Business Central a Exchange Online

Se parte de la base que para los siguientes pasos está usando Azure Active Directory para gestionar identidades y accesos. Para obtener más información, consulte [Inicio rápido: registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. En el Portal de Azure, en **Administrar** elija **Autenticación**.
2. En **Redirigir URL**, agregue la URL de redireccionamiento que se sugiere en la página **Registro de correo electrónico** en [!INCLUDE[prod_short](includes/prod_short.md)]. Si el campo URL de redireccionamiento en la página Registro de correo electrónico está vacío, busque la URL de redireccionamiento sugerida en la página **Configuración asistida**. Para abrir la página, en la página **Registro de correo electrónico**, elija **Acciones**, y luego **Configuración asistida**.

    > [!NOTE]
    > Si no especifica la URL de redireccionamiento, puede hacerlo más tarde eligiendo **Agregar una plataforma** y luego elegir **Web** para agregar la aplicación web y la URL de redireccionamiento.

3. En **Administrar**, elija **Permisos de la API**, y elija **Microsoft Graph** y luego elija **Permisos delegados**.
4. Utilice el cuadro de búsqueda para buscar y seleccionar **Correo** y, a continuación, agregue el permiso **Mail.ReadWrite.Shared**. 
5. En **Administrar**, elija **Certificados y secretos** y, luego, cree un nuevo secreto para la aplicación. Usará el secreto ya sea en el campo **Secreto del cliente** en la página **Registro de correo electrónico** en [!INCLUDE[prod_short](includes/prod_short.md)].
6. Elija **Panorama** y luego encuentre el valor **Id. de la aplicación (cliente)**. Este es el identificador de cliente de su aplicación. Debe introducirlo ya sea en el campo **Identificación del cliente** en la página **Registro de correo electrónico**.
7. En [!INCLUDE[prod_short](includes/prod_short.md)], configure el registro de correo electrónico en la página **Registro de correo electrónico** o utilice la guía **Configuración asistida** para obtener ayuda.

### <a name="use-another-identity-and-access-management-service"></a><a name="use-another-identity-and-access-management-service"></a><a name="use-another-identity-and-access-management-service"></a>Usar otro servicio de administración de identidades y accesos

Si no estas usando Azure Active Directory para administrar las identidades y el acceso, necesitará ayuda de un desarrollador. Si prefiere almacenar el identificador y el secreto de la aplicación en una ubicación diferente, puede dejar en blanco los campos Id . del cliente y Secreto del cliente y escribir una extensión para obtener el identificador y el secreto de la ubicación. Puede proporcionar el secreto en tiempo de ejecución suscribiéndose a los eventos OnGetEmailLoggingClientId y OnGetEmailLoggingClientSecret en la codeunit 1641 "Impl. de CDS Integration".

## <a name="to-start-logging-email"></a><a name="to-start-logging-email"></a><a name="to-start-logging-email"></a>Para empezar a registrar correo electrónico

1. Para comenzar a registrar el correo electrónico, en la página **Registro de correo electrónico**, active la opción **Habilitado**.
2. Inicie sesión con la cuenta de Exchange Online que el trabajo programado usará para conectar el buzón compartido y procesar correos electrónicos.

    > [!NOTE]
    > Si no se le solicita que inicie sesión en la cuenta de Exchange Online, podría deberse a que las ventanas emergentes de su navegador están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a><a name="to-stop-logging-email"></a><a name="to-stop-logging-email"></a>Para dejar de registrar correo electrónico

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Registro de correo electrónico** y luego elija el enlace relacionado.
2. Desactive el botón de alternancia **Habilitado**.

## <a name="to-change-the-user-account-used-for-email-logging"></a><a name="to-change-the-user-account-used-for-email-logging"></a><a name="to-change-the-user-account-used-for-email-logging"></a>Para cambiar la cuenta de usuario utilizada para el registro de correo electrónico

### <a name="-online"></a><a name="-online"></a><a name="-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Inicie sesión en [!INCLUDE[prod_short](includes/prod_short.md)] con la cuenta que el trabajo programado usará para conectar el buzón compartido y procesar correos electrónicos. Esta cuenta debe tener acceso a [!INCLUDE[prod_short](includes/prod_short.md)] y Exchange Online.
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Registro de correo electrónico** y luego elija el enlace relacionado. 
3. Elija **Relacionados**, y después **Entrada de la cola de trabajos**.
4. Reinicie el trabajo **Registro de correo electrónico**.

### <a name="-on-premises"></a><a name="-on-premises"></a><a name="-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Local

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Registro de correo electrónico** y luego elija el enlace relacionado.
2. Elija **Acciones**, y luego **Renovar token**.
3. Inicie sesión con la cuenta de Exchange Online que el trabajo programado usará para conectar el buzón compartido y procesar correos electrónicos.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Gestionar las relaciones](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
