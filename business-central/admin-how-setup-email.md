---
title: Configurar el correo electrónico en Business Central (contiene vídeo)
description: Describe cómo conectar cuentas de correo electrónico a Business Central para que pueda enviar mensajes salientes sin tener que abrir otra aplicación.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 11/22/2022
ms.author: bholtorf
---

# Configurar correo electrónico

Las personas en las empresas envían información y documentos, como órdenes de compra y venta y facturas, por correo electrónico todos los días. Los administradores pueden conectar una o varias cuentas de correo electrónico a [!INCLUDE[prod_short](includes/prod_short.md)], permitiéndole enviar documentos sin tener que abrir una aplicación de correo electrónico. Puede redactar cada mensaje individualmente con herramientas de formato básicas, como fuentes, estilos, colores, etc., y agregar archivos adjuntos de hasta 100 MB. Además, los diseños de informes pueden permitir que los administradores incluyan solo la información clave de los documentos. Obtenga más información en [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

Las capacidades de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] son solo para mensajes salientes. No puede recibir respuestas, es decir, no hay una página de "bandeja de entrada".

> [!NOTE]
> Puede utilizar las capacidades de correo electrónico de [!INCLUDE[prod_short](includes/prod_short.md)] en línea solo con Exchange Online. No admitimos escenarios híbridos, como la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] en línea a una versión local de Exchange.
>
> Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] local, antes de poder configurar el correo electrónico, debe crear un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Azure Portal. El registro de la aplicación permitirá [!INCLUDE[prod_short](includes/prod_short.md)] para autorizar y autenticarse con su proveedor de correo electrónico. Para obtener más información, consulte [Configurar correo electrónico para Business Central local](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). En [!INCLUDE[prod_short](includes/prod_short.md)] en línea, nos encargamos de esto por usted.

## Requisitos

Hay un par de requisitos para configurar y utilizar las funciones de correo electrónico.

* Para configurar el correo electrónico, debe tener el conjunto de permisos **CONFIGURACIÓN DE CORREO ELECTRÓNICO**. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).
* Todos los que vayan a utilizar las funciones de correo electrónico deben tener una licencia completa [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, los administradores delegados y los usuarios invitados no pueden usar la cuenta de correo electrónico del inquilino.

## Agregar cuentas de correo electrónico

Agrega cuentas de correo electrónico a través de extensiones que permiten que se conecten cuentas de diferentes proveedores a [!INCLUDE[prod_short](includes/prod_short.md)]. Las extensiones estándar le permiten usar cuentas de Microsoft Exchange Online. Sin embargo, es posible que estén disponibles otras extensiones que le permitan conectar cuentas de otros proveedores, como Gmail.

Puede especificar escenarios comerciales predefinidos en los que usar una cuenta de correo electrónico para enviar correos electrónicos. Por ejemplo, puede especificar que todos los usuarios envíen documentos de ventas desde una cuenta y compren documentos de otra. Más información en [Asignar escenarios de correo electrónico a cuentas de correo electrónico](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

La siguiente tabla describe las extensiones de correo electrónico que están disponibles de forma predeterminada.

|Extensión  |Descripción  |Ejemplos de cuando usar  |
|---------|---------|---------|
|**Conector de Microsoft 365**|Todos envían correos electrónicos desde un buzón compartido en Exchange Online.|Cuando todos los mensajes provienen del mismo departamento, por ejemplo, su organización de ventas envía mensajes desde una cuenta sales@cronus.com. Esta opción requiere que configure un buzón compartido en el centro de administración de Microsoft 365. Para más información, vea [Buzones de correo compartidos](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Conector de usuario actual**|Todos envían correos electrónicos desde la cuenta que usaron para iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].|Permitir comunicaciones de cuentas individuales.|
|**Conector SMTP**|Usar el protocolo SMTP para enviar mensajes de correo electrónico.|Permita las comunicaciones a través de su servidor de correo SMTP. |

> [!NOTE]
> Las extensiones de **Conector de Microsoft 365** y **Conector de usuario actual** usan las cuentas que configura para los usuarios en el centro de administración de Microsoft 365 para su suscripción a Microsoft 365. Para enviar correo electrónico utilizando las extensiones, los usuarios deben tener una licencia válida para Exchange Online. Además, en entornos de espacio aislado, estas extensiones requieren que la configuración **Permitir solicitudes HttpClient** esté habilitada. Para comprobar si está habilitada para estas extensiones, vaya a la página **Administración de extensiones**, elija la extensión y luego la opción **Configurar**.

> Los usuarios externos, como administradores delegados y contables externos, no pueden utilizar estas extensiones para enviar mensajes de correo electrónico desde [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## Uso de SMTP

Si desea utilizar el protocolo SMTP para enviar correos electrónicos desde [!INCLUDE[prod_short](includes/prod_short.md)], puede utilizar la extensión de Conector SMTP. Cuando configura una cuenta que utiliza SMTP, el **tipo de remitente** es un campo importante. Si elige **Usuario específico**, los correos electrónicos se enviarán con el nombre y otra información de la cuenta que está configurando. Sin embargo, si elige **Usuario actual**, los correos electrónicos se enviarán desde la cuenta de correo electrónico especificada para la cuenta de cada usuario. Usuario actual es parecido a la función Enviar como. Para más información, compruebe [Usar una dirección de remitente sustituta en los mensajes de correo electrónico salientes](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] local, puede usar el protocolo OAuth 2.0 para autenticación. Debe crear un registro de aplicación en Azure Portal y luego ejecutar la guía de configuración asistida **Configurar Azure Active Directory** en [!INCLUDE[prod_short](includes/prod_short.md)] para conectarse a Azure AD. Para obtener más información, consulte [Crear un registro de aplicación para Business Central en Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online está desaprobando el uso de la autenticación básica para SMPT. Los inquilinos que actualmente usan SMTP AUTH no se verán afectados por este cambio. Sin embargo, recomendamos enfáticamente usar la última versión de [!INCLUDE [prod_short](includes/prod_short.md)] y configurar la autenticación OAuth 2.0 para SMTP. No agregaremos autenticación basada en certificados para versiones anteriores de [!INCLUDE [prod_short](includes/prod_short.md)], por ejemplo, la versión 14. Si no puede configurar la autenticación OAuth 2.0, le recomendamos que explore alternativas de terceros si desea utilizar el correo electrónico SMTP en versiones anteriores.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## Agregar cuentas de correo electrónico

La guía de configuración asistida para **Configurar correo electrónico** puede ayudarlo a comenzar rápidamente con los correos electrónicos.

> [!NOTE]
> Debe tener una cuenta de correo electrónico predeterminada, incluso si agrega solo una cuenta. La cuenta predeterminada se utilizará para todos los escenarios de correo electrónico que no estén asignados a una cuenta. Más información en [Asignar escenarios de correo electrónico a cuentas de correo electrónico](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configurar cuentas de correo electrónico** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## Asignar escenarios de correo electrónico a cuentas de correo electrónico

Los escenarios de correo electrónico son procesos que implican el envío de un documento. Por ejemplo, un pedido de compra o venta o una notificación, como una invitación a un contable externo. Puede utilizar cuentas de correo electrónico específicas para escenarios concretos. Por ejemplo, puede especificar que todos los usuarios envíen siempre documentos de ventas de una cuenta, documentos de compra de otra y documentos de almacén o producción de una tercera cuenta. Puede asignar, reasignar y eliminar escenarios cuando lo desee. Un escenario solo se puede asignar a una cuenta de correo electrónico a la vez. La cuenta predeterminada se utilizará para todos los escenarios de correo electrónico que no estén asignados a una cuenta.

En la página **Asignación de escenario por correo electrónico**, puede elegir la acción **Establecer archivos adjuntos predeterminados** para agregar archivos adjuntos a escenarios de correo electrónico. Los archivos adjuntos siempre estarán disponibles cuando redacte un correo electrónico para un documento relacionado con el escenario. Cada escenario de correo electrónico puede tener uno o más archivos adjuntos predeterminados. Los archivos adjuntos predeterminados se agregan automáticamente a los correos electrónicos para el escenario de correo electrónico. Por ejemplo, cuando envía un pedido de ventas por correo electrónico, se agregará el archivo adjunto predeterminado especificado para el escenario Pedido de ventas. Los archivos adjuntos predeterminados se muestran en la sección **Archivos adjuntos** en la parte inferior de la página **Redactar un correo electrónico**. Puede agregar manualmente archivos adjuntos no predeterminados al correo electrónico.

<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## Configurar directivas de visualización

Puede controlar los mensajes de correo electrónico que un usuario puede acceder en las páginas Bandeja de salida de correo electrónico y Correos electrónicos enviados.

En **Directivas de visualización de correo electrónico de usuario**, elija un usuario y luego una de las siguientes opciones en el campo **Directiva de visualización de correo electrónico**:

* **Ver correos electrónicos propios**: el usuario solo puede ver sus propios mensajes de correo electrónico.
* **Ver todos los correos electrónicos**: el usuario puede ver todos los mensajes de correo electrónico, incluidos los correos electrónicos enviados por otros usuarios.
* **Ver si se tiene acceso a todos los registros relacionados**: esta directiva de visualización se utiliza si no se especifica ninguna otra directiva. Un usuario puede ver los mensajes de correo electrónico que enviaron otros usuarios si el usuario tiene acceso al registro que se envió y todos los registros relacionados. Por ejemplo, el usuario A envió un histórico de facturas de venta a un cliente. El usuario B puede ver el mensaje de correo electrónico si tiene acceso tanto a la factura como al cliente.
* **Ver si se tiene acceso a los registros relacionados**: el usuario puede ver los mensajes de correo electrónico que enviaron otras personas si el usuario tiene acceso a como mínimo un registro relacionado con el registro que se envió. Por ejemplo, el usuario A envió un histórico de facturas de venta a un cliente. El usuario B puede ver el mensaje de correo electrónico si tiene acceso a la factura o al cliente.

> [!NOTE]
> Si deja vacío el campo **ID de usuario** y luego elige la acción **Directiva de visualización de correo electrónico**, la directiva que defina se aplica a todos los usuarios.

## Especificar cuántos mensajes puede enviar una cuenta por minuto

Algunos proveedores de correo electrónico (ISP) limitan la cantidad de mensajes de correo electrónico que una cuenta de correo electrónico puede enviar de una sola vez, dentro de un cierto período de tiempo, o en ambos. Conocida como *limitación del correo electrónico*, la práctica ayuda a los ISP a controlar el tráfico en sus servidores y evitar el spam. Si una cuenta de correo electrónico supera el límite, el ISP podría bloquear los mensajes. Para asegurarse de que la cantidad de mensajes que envía desde [!INCLUDE [prod_short](includes/prod_short.md)] cumpla con el límite de su ISP, especifique el límite para cada una de sus cuentas de correo electrónico.

El límite predeterminado para los tipos de cuenta Microsoft 365 y Usuario actual es 30, que coincide con el límite establecido por Exchange Online.

Hay dos formas de especificar el límite:

* Cuando utilice la guía de configuración asistida Configurar correo electrónico para crear una nueva cuenta, especifique el límite en el campo **Límite de tasa por minuto** .
* Para las cuentas de correo electrónico existentes, especifique el límite en el campo **Límite de tasa de correo electrónico** de la cuenta.

## Configure textos y diseños de correo electrónico reutilizables

Puede utilizar informes para incluir información clave de documentos de venta, compra y servicio en textos para correos electrónicos. Los diseños de informe definen el estilo y el contenido del texto en el correo electrónico. Por ejemplo, el contenido podría incluir textos como un saludo o instrucciones que preceden a la información del documento. Este procedimiento describe cómo configurar el informe **Factura de venta** para facturas de ventas registradas, pero el proceso es similar para otros informes.

> [!NOTE]
> Para usar el diseño para crear contenido para mensajes de correo electrónico, debe usar el tipo de archivo de Word para su diseño.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección informes - Ventas** y luego elija el enlace relacionado.
2. En la página **Informe selección - ventas**, en el campo **Uso**, seleccione **Facturar**.
3. En una línea nueva, en el campo **Id. informe**, seleccione, por ejemplo, informe estándar 1306.
4. Seleccione la casilla **Usar para el cuerpo del correo electrónico**.
5. Elija el campo **Descripción de diseño del cuerpo del correo electrónico** y seleccione un diseño en la lista.
6. Para ver o editar el diseño en el que se basa el texto del correo electrónico, seleccione el diseño en la página **Diseños de informe personalizados** y, a continuación, elija la acción **Exportar diseño**. Si personaliza el diseño, utilice la acción **Importar diseño** para cargar el nuevo diseño.
    > [!NOTE]
    > Para personalizar un diseño de informe estándar, como 1306, debe hacer una copia del informe. [!INCLUDE [prod_short](includes/prod_short.md)] le ayudará a crear una copia cuando importe un diseño personalizado para un informe estándar. El nombre de su nuevo diseño de informe personalizado tendrá el prefijo "Copia de".
7. Si desea permitir que los clientes utilicen un servicio de pago, como PayPal, deberá configurar el servicio. Después, la información y el vínculo de PayPal se insertan en el texto del correo electrónico. Para obtener más información, consulte [Permitir pagos de cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).
8. Elija el botón **Aceptar**.

Ahora bien, cuando selecciona, por ejemplo, la acción **Enviar** en la página **Factura venta reg.**, el cuerpo del correo electrónico contendrá la información del documento del informe 1306 precedida por el texto estándar siguiendo el diseño de informe que seleccionó en el paso 5.

## Usar una dirección de remitente sustituta en los mensajes de correo electrónico salientes

Si usa la extensión Conector SMTP, puede utilizar las funciones **Enviar como** o **Enviar en nombre de** en Microsoft Exchange para cambiar la dirección del remitente en los mensajes salientes. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará la cuenta SMTP para autenticarse en Exchange, pero sustituirá la dirección del remitente por la que especifique o la modificará con "en nombre de".

Cuando configura una cuenta y desea utilizar las funciones Enviar como o Enviar en nombre de Exchange, en el campo **Tipo de remitente**, elija **Usuario específico**.

Alternativamente, puede elegir **Usuario actual** para permitir que las personas envíen mensajes a través del conector SMTP. El mensaje parecerá enviado desde la cuenta de correo electrónico especificada en el campo Correo electrónico de contacto de la ficha de usuario para el usuario con el que inició sesión. Sin embargo, funcionará de manera similar a la característica Enviar como y se enviará desde la cuenta especificada en la configuración del Connector forde SMTP.

A continuación se ofrecen ejemplos de cómo se usan Enviar como y Enviar en nombre de en [!INCLUDE[prod_short](includes/prod_short.md)]:

* Puede que desee que los pedidos de compra o de venta que envía a proveedores y clientes parezcan proceder de una dirección _noreply@yourcompanyname.com_.
* Cuando su flujo de trabajo envía una solicitud de aprobación por correo electrónico utilizando la dirección de correo electrónico del solicitante.

> [!Note]
> Solo puede utilizar una cuenta para sustituir las direcciones de remitente. Es decir, no puede tener una dirección sustituta para los procesos de compra y otra para los procesos de venta.

<!--
### To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## Configurar perfiles de envío de documentos

Puede ahorrar tiempo configurando un método preferido de envío de documentos de ventas para cada uno de sus clientes. No tendrá que seleccionar una opción de envío, como enviar el documento por correo electrónico o como documento electrónico, cada vez que envíe un documento. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

## Opcional: Configurar el registro de correo electrónico en Exchange Online

Aproveche al máximo las comunicaciones entre comerciales y sus clientes actuales o potenciales. Puede realizar un seguimiento de los intercambios de correo electrónico y luego convertirlos en oportunidades procesables. Más información en [Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## Configuración del correo electrónico para Business Central en las instalaciones

[!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones se puede integrar con servicios que se basan en Microsoft Azure. Por ejemplo, puede utilizar Cortana Intelligence para previsiones de flujo de caja más inteligentes, Power BI para visualizar su negocio y Exchange Online para enviar correo electrónico. La integración con estos servicios se basa en el registro de una aplicación en Azure Active Directory. El registro de la aplicación proporciona servicios de autenticación y autorización para las comunicaciones. Para utilizar las capacidades de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones, debe registrar [!INCLUDE[prod_short](includes/prod_short.md)] como una aplicación en el portal de Azure y luego conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de la aplicación. En el siguiente apartado se explica cómo.

### Crear un registro de aplicación para Business Central en Azure Portal

Los pasos para registrar [!INCLUDE[prod_short](includes/prod_short.md)] en Azure Portal se describen en [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Para usar las características de correo electrónico, el registro de su aplicación debe usar una configuración de múltiples inquilinos.

Las configuraciones que son específicas de las capacidades de correo electrónico son los permisos delegados que otorga al registro de su aplicación. La siguiente tabla enumera los permisos mínimos.

|API / Nombre de permiso  |Escriba  |Descripción  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegado|Iniciar sesión y leer el perfil de usuario.         |
|Microsoft Graph / Mail.ReadWrite |Delegado|Redactar mensajes de correo electrónico.         |
|Microsoft Graph / Mail.Send|Delegado|Enviar mensajes de correo electrónico.         |
|Microsoft Graph / offline_access|Delegado|Consentimiento de acceso para mantener los datos.|

Si está usando un Conector SMTP y desea usar OAuth 2.0 para autenticación, los permisos son algo diferentes. La siguiente tabla enumera los permisos.

|API / Nombre de permiso  |Escriba  |Descripción  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegado|Consentimiento de acceso para mantener los datos.|
|Microsoft Graph / openid|Delegado|Iniciar sesión de usuarios.|
|Microsoft Graph / User.Read |Delegado|Iniciar sesión y leer el perfil de usuario.         |
|Microsoft Graph / SMTP.Send|Delegado|Enviar correos electrónicos desde usando SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Delegado|Iniciar sesión y leer el perfil de usuario.         |

Cuando crea el registro de la aplicación , tenga en cuenta la siguiente información. La necesitará para conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de la aplicación.
 
* ID de la aplicación (cliente)
* Redirigir URI (opcional)
* Secreto del cliente

Más información sobre directrices generales sobre cómo registrar una aplicación, en [Inicio rápido: Registrar una aplicación con la plataforma de identidad de Microsoft.](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Si tiene problemas para usar el protocolo SMTP para enviar correos electrónicos después de conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de su aplicación, podría deberse a que SMTP AUTH no está habilitado para su suscriptor. En su lugar, le recomendamos que use los conectores de correo electrónico de Microsoft 365 y del usuario actual, ya que usan las API de Microsoft Graph Mail. Sin embargo, si debe usar el protocolo SMTP, puede habilitar SMTP AUTH. Para obtener más información, consulte [Habilitar o deshabilitar el envío SMTP de cliente autenticado (SMTP AUTH) en Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### Conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de su aplicación

Después de registrar su aplicación en Azure Portal, en [!INCLUDE[prod_short](includes/prod_short.md)], utilice la guía de configuración asistida **Registro de AAD para aplicaciones de correo electrónico** para conectar [!INCLUDE[prod_short](includes/prod_short.md)].

1. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de AAD para aplicaciones de correo electrónico** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Alternativamente, si se conecta por primera vez, puede ejecutar la guía de configuración asistida **Configurar correo electrónico**. La guía requerirá la información para conectarse al registro de su aplicación. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## Consultar la [formación de Microsoft](/training/modules/set-up-email/) relacionada

## Consulte también

[Buzones compartidos en Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como su bandeja de entrada de empresa en Outlook](admin-outlook.md)  
[Obtener [!INCLUDE[prod_short](includes/prod_short.md)] en el dispositivo móvil](install-mobile-app.md)
[Obtener [!INCLUDE[prod_short](includes/prod_short.md)] en el dispositivo móvil](install-mobile-app.md)
[Análisis de la telemetría de correo electrónico (contenido de administración)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
