---
title: Configurar el correo electrónico en Business Central | Documentos de Microsoft
description: Describe cómo conectar cuentas de correo electrónico a Business Central para que pueda enviar mensajes salientes sin tener que abrir otra aplicación.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 06/15/2020
ms.author: bholtorf
ms.openlocfilehash: 44fb1f467b0b44c41456a64c8de3f5ae9dc85786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752755"
---
# <a name="set-up-email"></a>Configurar correo electrónico
Las personas en las empresas envían información y documentos, como órdenes de compra y venta y facturas, por correo electrónico todos los días. Los administradores pueden facilitarlo conectando una o más cuentas de correo electrónico a [!INCLUDE[prod_short](includes/prod_short.md)], para que pueda enviar documentos sin tener que abrir una aplicación de correo electrónico. Puede redactar cada mensaje individualmente con herramientas de formato básicas, como fuentes, estilos, colores, etc., y agregar archivos adjuntos de hasta 100 MB. Los administradores también pueden configurar diseños de informes que incluyan solo la información clave de los documentos. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

Las capacidades de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] son solo para mensajes salientes. No puede recibir respuestas, es decir, no hay una página de bandeja de entrada en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] local, antes de poder configurar el correo electrónico, debe crear un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Azure Portal. El registro de la aplicación permitirá [!INCLUDE[prod_short](includes/prod_short.md)] para autorizar y autenticarse con su proveedor de correo electrónico. Para obtener más información, consulte [Configurar correo electrónico para Business Central local](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). En [!INCLUDE[prod_short](includes/prod_short.md)] en línea, nos encargamos de esto por usted.

## <a name="required-permissions"></a>Permisos requeridos
Para configurar el correo electrónico, debe tener el conjunto de permisos **CONFIGURACIÓN DE CORREO ELECTRÓNICO**. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Agregar cuentas de correo electrónico
Agrega cuentas de correo electrónico a través de extensiones que permiten que se conecten cuentas de diferentes proveedores a [!INCLUDE[prod_short](includes/prod_short.md)]. Las extensiones estándar le permiten usar cuentas de Microsoft Exchange Online, pero puede haber otras extensiones disponibles que le permitan conectar cuentas de otros proveedores, como Gmail.

Después de agregar una cuenta de correo electrónico, puede especificar escenarios comerciales predefinidos en los que usar la cuenta para enviar correos electrónicos. Por ejemplo, puede especificar que todos los usuarios envíen documentos de ventas desde una cuenta y compren documentos de otra. Para más información, vea [Asignar escenarios de correo electrónico a cuentas de correo electrónico](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

La siguiente tabla describe las extensiones de correo electrónico que están disponibles de forma predeterminada.

|Extensión  |Descripción  |Ejemplos de cuando usar  |
|---------|---------|---------|
|**Microsoft 365**|Todos envían correos electrónicos desde un buzón compartido en Exchange Online.|Cuando todos los mensajes provienen del mismo departamento, por ejemplo, su organización de ventas envía mensajes desde una cuenta sales@cronus.com. Esto requiere que configure un buzón compartido en el centro de administración de Office 365. Para más información, vea [Buzones de correo compartidos](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Usuario actual**|Todos envían correos electrónicos desde la cuenta que usaron para iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].|Permitir comunicaciones de cuentas individuales.|
|**Otro (SMTP)**|Usar el protocolo SMTP para enviar mensajes de correo electrónico.|Permita las comunicaciones a través de su servidor de correo SMTP. |

> [!NOTE]
> Las extensiones de **Microsoft 365** y **Usuario actual** usan las cuentas que configura para los usuarios en el centro de administración de Microsoft 365 para su suscripción a Office 365. Para enviar correo electrónico utilizando las extensiones, los usuarios deben tener una licencia válida para Exchange Online. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Configuración de SMTP heredada y correo electrónico: extensión del conector SMTP
Si ya está usando [!INCLUDE[prod_short](includes/prod_short.md)] y ha configurado el correo electrónico a través de la configuración SMTP heredada, puede continuar usando su configuración en paralelo con la extensión Correo electrónico - Conector SMTP. Cuando actualizamos su [!INCLUDE[prod_short](includes/prod_short.md)] a la próxima versión de lanzamiento, copiaremos su configuración SMTP heredada en la extensión Correo electrónico - Conector SMTP. Cuando esté listo, su administrador puede activar las capacidades mejoradas de correo electrónico y comenzará a usar la extensión Correo electrónico - Conector SMTP. Para obtener más información, consulte [Acerca de la gestión de características](/dynamics365/business-central/dev-itpro/administration/feature-management.md#about-feature-management). Sin embargo, no hay sincronización entre la extensión del conector SMTP y la configuración heredada. Si cambia la configuración de SMTP en la extensión, debe realizar los mismos cambios en la configuración de SMTP heredada, o viceversa.

> [!NOTE]
> Si tiene personalizaciones que se basan en la configuración de correo electrónico SMTP heredada, existe la posibilidad de que algo salga mal con sus personalizaciones si comienza a usar extensiones de correo electrónico. Le recomendamos que configure y pruebe las extensiones antes de activar el interruptor de función para mejorar las capacidades de correo electrónico.

## <a name="add-email-accounts"></a>Agregar cuentas de correo electrónico
La guía de configuración asistida para **Configurar correo electrónico** puede ayudarlo a comenzar rápidamente con los correos electrónicos.

> [!NOTE]
> Debe tener una cuenta de correo electrónico predeterminada, incluso si agrega solo una cuenta. La cuenta predeterminada se utilizará para todos los escenarios de correo electrónico que no estén asignados a una cuenta. Para más información, vea [Asignar escenarios de correo electrónico a cuentas de correo electrónico](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configurar cuentas de correo electrónico** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Office 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Asignar escenarios de correo electrónico a cuentas de correo electrónico
Los escenarios de correo electrónico son procesos que implican el envío de un documento, como una orden de compra o de venta, o una notificación, como una invitación a un contador externo. Puede utilizar cuentas de correo electrónico específicas para escenarios específicos. Por ejemplo, puede especificar que todos los usuarios envíen siempre documentos de ventas de una cuenta, documentos de compra de otra y documentos de almacén o producción de una tercera cuenta. Puede asignar, reasignar y eliminar escenarios cuando lo desee, pero solo puede asignar un escenario a una cuenta de correo electrónico a la vez. La cuenta de correo electrónico predeterminada se utilizará para todos los escenarios que no estén asignados a una cuenta.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Configurar textos y diseños de correo electrónico reutilizables para documentos de compra y venta
Puede utilizar informes para incluir información clave de documentos de compra y venta en textos para correos electrónicos. Este procedimiento describe cómo configurar el informe **Factura de venta** para facturas de ventas registradas, pero el proceso es similar para otros informes.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Selección informes ventas** y luego elija el enlace relacionado.
2. En la página **Informe selección - ventas**, en el campo **Uso**, seleccione **Facturar**.
3. En una línea nueva, en el campo **Id. informe**, seleccione, por ejemplo, informe estándar 1306.
4. Seleccione la casilla **Usar para el cuerpo del correo electrónico**.
5. Elija el campo **Código de diseño del cuerpo del correo electrónico** y seleccione una plantilla en la lista desplegable.

    Las plantillas de informes definen tanto el estilo como el contenido del texto del correo, incluyendo textos como saludos o instrucciones que preceden a la información del documento. Puede ver todos los diseños de informe disponibles si elige **Seleccionar de la lista completa**.
6. Para ver o editar el diseño en el que se basa el texto del correo electrónico, seleccione el diseño en la página **Diseños de informe personalizados** y, a continuación, elija la acción **Editar diseño**.
7. Si desea ofrecer a sus clientes el pago de las ventas de forma electrónica puede configurar el servicio de pago relacionado, como por ejemplo PayPal y, a continuación, puede disponer también de su información y su vínculo en el texto del correo. Para obtener más información, consulte [Permitir pagos de cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).
8. Elija el botón **Aceptar**.

Ahora bien, cuando selecciona, por ejemplo, la acción **Enviar** en la página **Factura venta reg.**, el cuerpo del correo electrónico contendrá la información del documento del informe 1306 precedida por el texto estándar siguiendo el diseño de informe que seleccionó en el paso 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Uso de una dirección de remitente sustituta en los mensajes de correo electrónico salientes
Si usa la configuración SMTP heredada, puede utilizar las funciones **Enviar como** o **Enviar en nombre de** en Microsoft Exchange para cambiar la dirección del remitente en los mensajes salientes. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará la cuenta SMTP para autenticarse en Exchange, pero sustituirá la dirección del remitente por la que especifique o la modificará con "en nombre de".

A continuación se ofrecen ejemplos de cómo se usan Enviar como y Enviar en nombre de en [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Al enviar documentos como pedidos de compra o de venta a proveedores y clientes, es posible que desee que parezcan proceder de una dirección _noreply@yourcompanyname.com_.
 * Cuando su flujo de trabajo envía una solicitud de aprobación por correo electrónico utilizando la dirección de correo electrónico del solicitante.

> [!Note]
> Solo puede utilizar una cuenta para sustituir las direcciones de remitente. Es decir, no puede tener una dirección sustituta para los procesos de compra y otra para los procesos de venta.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Para configurar la dirección de remitente sustituta para todos los mensajes de correo electrónico salientes
1. En el **centro de administración de Exchange** de su cuenta de Microsoft 365, busque el buzón de correo para utilizarlo como dirección sustitutoria y, a continuación, copie o anote la dirección. Si necesita una nueva dirección, vaya a su centro de administración de Microsoft 365 para crear un nuevo usuario y configurar su buzón de correo.
2. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
3. En el campo **Enviar como**, introduzca la dirección sustituta.
4. Copie o anote la dirección en el campo **ID de usuario**.
5. En el **centro de administración de Exchange**, busque el buzón de correo que desea utilizar como dirección sustituta y, a continuación, introduzca la dirección del campo **ID de usuario** en el campo **Enviar como**. Para más información, ver [Use el EAC para asignar permisos a buzones individuales](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Para utilizar la dirección sustituta en los flujos de trabajo de aprobación
1. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
2. Copie o anote la dirección en el campo **ID de usuario**.
3. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.
4. En el **centro de administración de Exchange**, busque los buzones de correo de cada usuario que aparece en la página **Configuración de usuario de aprobación** y, en el campo **Enviar como**, introduzca la dirección del campo **ID de usuario** de la página **Configuración de correo electrónico SMTP** en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, vea [Administrar permisos para destinatarios](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
6. Para habilitar la sustitución, active **Permitir sustitución del remitente**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] determinará qué dirección se mostrará en el siguiente orden: <br><br> 1. La dirección especificada en el campo **Correo electrónico** de la página **Configuración de usuario de aprobación** para los mensajes en un flujo de trabajo. <br> 2. La dirección especificada en el campo **Enviar como** de la página **Configuración de correo electrónico SMTP**. <br> 3. La dirección especificada en el campo **ID de usuario** de la página **Configuración de correo electrónico SMTP**.

## <a name="set-up-document-sending-profiles"></a>Configurar perfiles de envío de documentos
Puede configurar un método preferido de envío de documentos de ventas para cada uno de sus clientes, de modo que no tenga que seleccionar una opción de envío, como enviar el documento por correo electrónico o como documento electrónico, cada vez que envía un documento. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurar carpetas públicas y reglas para iniciar sesión por correo electrónico en Exchange Online
Aproveche al máximo las comunicaciones entre los vendedores y sus clientes actuales o potenciales mediante el seguimiento de los intercambios de correos electrónicos y, a continuación, conviértalos en oportunidades procesables. Para obtener más información, vea [Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Luego, te conectas [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online. Para obtener más información, vea [Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Configuración del correo electrónico para Business Central en las instalaciones 
[!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones se puede integrar con servicios que se basan en Microsoft Azure. Por ejemplo, puede utilizar Cortana Intelligence para previsiones de flujo de caja más inteligentes, Power BI para visualizar su negocio y Exchange Online para enviar correo electrónico. La integración con estos servicios se basa en el registro de una aplicación en Azure Active Directory. El registro de la aplicación proporciona servicios de autenticación y autorización para las comunicaciones. Para utilizar las capacidades de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones, debe registrar [!INCLUDE[prod_short](includes/prod_short.md)] como una aplicación en el portal de Azure y luego conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de la aplicación. En el siguiente apartado se explica cómo.

### <a name="create-an-app-registration-for-prod_short-in-azure-portal"></a>Crear un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Azure Portal
Los pasos para registrar [!INCLUDE[prod_short](includes/prod_short.md)] en Azure Portal se describen en [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Las configuraciones que son específicas de las capacidades de correo electrónico son los permisos delegados que otorga al registro de su aplicación. La siguiente tabla enumera los permisos mínimos.

|API / Nombre de permiso  |Escriba  |Descripción  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegado|Iniciar sesión y leer el perfil de usuario.         |
|Microsoft Graph / Mail.ReadWrite |Delegado|Redactar mensajes de correo electrónico.         |
|Microsoft Graph / Mail.Send|Delegado|Enviar mensajes de correo electrónico.         |
|Microsoft Graph / offline_access|Delegado|Consentimiento de acceso para mantener los datos. <!--need to verify this-->|

> [!TIP]
> Cuando crea el registro de la aplicación , tenga en cuenta la siguiente información. La necesitará para conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de la aplicación.
> 
> * ID de la aplicación (cliente) 
> * Redirigir URI (opcional)
> * Secreto del cliente

Para obtener directrices generales sobre cómo registrar una aplicación, vea [Inicio rápido: Registrar una aplicación con la plataforma de identidad de Microsoft.](/azure/active-directory/develop/quickstart-register-app.md). 

### <a name="connect-prod_short-to-your-app-registration"></a>Conectar [!INCLUDE[prod_short](includes/prod_short.md)] al registro de la aplicación
Después de registrar su aplicación en Azure Portal, en [!INCLUDE[prod_short](includes/prod_short.md)], utilice la guía de configuración asistida **Registro de AAD para aplicaciones de correo electrónico** para conectar [!INCLUDE[prod_short](includes/prod_short.md)].

1. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de AAD para aplicaciones de correo electrónico** y luego elija el enlace relacionado.
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

## <a name="see-also"></a>Consulte también
[Buzones compartidos en Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como su bandeja de entrada de empresa en Outlook](admin-outlook.md)  
[Obtener [!INCLUDE[prod_short](includes/prod_short.md)] en el dispositivo móvil](install-mobile-app.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]