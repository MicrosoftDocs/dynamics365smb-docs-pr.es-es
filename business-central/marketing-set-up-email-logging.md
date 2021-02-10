---
title: Configurar el registro de correo electrónico | Documentos de Microsoft
description: Aprenda a convertir las interacciones de correo electrónico entre vendedores y clientes en oportunidades de venta reales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f099072561e5a35f893a42edbbe6f27a5b4722ed
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749810"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos

Aproveche al máximo las comunicaciones entre los vendedores y sus clientes actuales o potenciales mediante el seguimiento de los intercambios de correos electrónicos y, a continuación, conviértalos en oportunidades procesables. [!INCLUDE[prod_short](includes/prod_short.md)] puede funcionar con Exchange Online para mantener un registro de los mensajes entrantes y salientes. Puede ver y analizar el contenido de cada mensaje en la página **Movimientos del log de interacción**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Configurar carpetas públicas y reglas para iniciar sesión por correo electrónico en Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Luego, te conectas [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Configuración de [!INCLUDE[prod_short](includes/prod_short.md)] para registrar los mensajes de correo electrónico

Comience con el registro de correo electrónico en dos sencillos pasos:

1. Conecte [!INCLUDE[prod_short](includes/prod_short.md)] con Exchange Online para su suscripción de Microsoft 365. Exchange Online gestiona sus mensajes de correo electrónico. Hemos facilitado este paso al proporcionar una guía de configuración asistida. Solo necesita sus credenciales de administrador para su cuenta de administrador en Microsoft 365. Para comenzar la guía, vaya a **Configuración asistida** y, a continuación, elija **Configurar registro de correo electrónico**.  

2. Asegúrese de que se han introducido direcciones de correo electrónico válidas en [!INCLUDE[prod_short](includes/prod_short.md)] para sus vendedores y contactos, dependiendo de si son clientes potenciales o existentes. Para ello, para cada cliente o vendedor, abra la ficha **Contacto** o **Vendedor/Comprador** y consulte el campo **Correo electrónico**.

> [!Tip]
> Después de completar los pasos de la guía, puede comprobar si la conexión se ha realizado correctamente. Busque **Configuración de marketing**, seleccione **Proceso**, **Funciones** y, a continuación, **Validar configuración de registro de correo electrónico**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visualización de los intercambios de mensajes de correo electrónico en el registro de interacciones
[!INCLUDE[prod_short](includes/prod_short.md)] crea una entrada en la página **Log de interacción** cada vez que un vendedor y un contacto intercambian un mensaje de correo electrónico. Para ver el registro de interacción, abra la tarjeta **Contacto** o **Vendedor/Comprador** correspondiente a la persona y, a continuación, elija **Historial** y luego **Mov. log interacción**. Hay algunas cosas que podemos hacer con cada entrada del registro, por ejemplo:

- Ver el contenido del mensaje de correo electrónico que se ha intercambiado haciendo clic en la acción **Mostrar datos adjuntos**.
- Convertir un intercambio de correos electrónicos en una oportunidad de ventas. Si una entrada parece prometedora, puede convertirla en una oportunidad y luego administrar su progreso hasta una venta. Para hacerlo, seleccione la entrada y, a continuación, seleccione la acción **Crear oportunidad**. Para obtener más información, consulte [Administrar oportunidades de venta](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Conexión de versiones locales a Microsoft Exchange
Puedes conectar [!INCLUDE[prod_short](includes/prod_short.md)] local a Exchange local o Exchange Online para el registro de correo electrónico. Para ambas versiones de Exchange, la configuración de la conexión está disponible en la página **Configuración de marketing**. Para Exchange Online, también puede utilizar una guía de configuración asistida. 

### <a name="connecting-to-exchange-on-premises"></a>Conexión a Exchange local.
Para conectar [!INCLUDE[prod_short](includes/prod_short.md)] local a Exchange local, en la página **Configuración de marketing**, puede usar **Básico** como **tipo de autenticación**  y luego ingrese las credenciales para la cuenta de usuario de Exchange local. Entonces active el control de alternancia **Habilitado** para comenzar a registrar el correo electrónico. 

### <a name="connecting-to-exchange-online"></a>Conectar con Exchange Online
Para conectar con Exchange Online, debe usar **OAuth2** como **tipo de autenticación**. También debe registrar una aplicación en Azure Active Directory y proporcionar el identificador de la aplicación, el secreto de Key Vault y la URL de redireccionamiento que se va a utilizar. La URL de redireccionamiento se rellena previamente y debería funcionar para la mayoría de las instalaciones. Para más información, vea [Para registrar una aplicación en Azure AD para conectarse desde Business Central a Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Debe configurar su instalación para usar HTTPS. Para más información, vea [Configuración SSL para proteger la conexión del cliente web de Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Si está configurando su servidor para tener una página de inicio diferente, puede cambiar la dirección URL. El secreto del cliente se guardará como una cadena encriptada en su base de datos.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Para registrar una solicitud en Azure AD para conectarse desde Business Central a Exchange Online
Se parte de la base que para los siguientes pasos está usando Azure Active Directory para gestionar identidades y accesos. Para obtener más información, consulte [Inicio rápido: registrar una aplicación con la plataforma de identidad de Microsoft](/azure/active-directory/develop/quickstart-register-app). Si no usa Azure Active Directory, vea [Usar otro servicio de administración de identidades y accesos](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. En el Portal de Azure, en **Administrar** elija **Autenticación**.
2. En **Redirigir URL**, agregue la URL de redireccionamiento que se sugiere en la página **Configuración de marketing** en [!INCLUDE[prod_short](includes/prod_short.md)]. Si la URL de redireccionamiento en la página Configuración de marketing está vacía, busque la URL de redireccionamiento sugerida en la página **Configuración asistida de registro de correo electrónico**.

    > [!NOTE]
    > Si no especifica la URL de redireccionamiento, puede hacerlo más tarde eligiendo **Agregar una plataforma** y luego elegir **Web** para agregar la aplicación web y la URL de redireccionamiento. 

3. En **Administrar**, elija **Manifiesto**.
4. Busque la propiedad **requiredResourceAccess** en el manifiesto y agregue el siguiente código entre corchetes ([]) para agregar los permisos necesarios. Para obtener más información, consulte [Registrar la aplicación](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth.md#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Elija **Guardar**.
6. Debajo de **Gestionar**, escoja **Permisos de API** y luego confirme que se enumeran los siguientes permisos:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. En **Administrar**, elija **Certificados y secretos** y, luego, cree un nuevo secreto para la aplicación. Usará el secreto en [!INCLUDE[prod_short](includes/prod_short.md)], en el campo **Secreto del cliente** en la página **Configuración de marketing** o lo almacenará en un almacenamiento seguro y lo proporcionará en un suscriptor de eventos.
8. Elija **Panorama** y luego encuentre el valor **Id. de la aplicación (cliente)**. Este es el identificador de cliente de su aplicación. Debe especificarlo en la página **Configuración de marketing** en el campo **Id. del cliente** o almacenarlo en un almacenamiento seguro y proporcionarlo en un suscriptor de eventos.
9. En [!INCLUDE[prod_short](includes/prod_short.md)], configure el registro de correo electrónico en la página **Configuración de marketing** o utilice la guía **Configuración asistida de registro de correo electrónico** para obtener ayuda con el proceso.
    * Proporcione la cuenta de correo electrónico del usuario en nombre del cual el proyecto programado se conectará a Exchange Online y procesará correos electrónicos. El usuario debe tener una licencia válida para Exchange Online.
    * Proporcione la URL de Exchange Online. Por lo general, este es el dominio que especificó en la dirección de correo electrónico del usuario.
    * Proporcionar la **Ruta de la carpeta de cola** y la **Ruta de la carpeta de almacenamiento**.
10. Para empezar a registrar el el correo electrónico, active el control de alternancia **Habilitado**.
11. Inicie sesión con su cuenta de administrador para Azure Active Directory (esta cuenta debe tener una licencia válida para Microsoft Exchange y ser administrador en su entorno de Exchange Online). Después de iniciar sesión, se le pedirá que permita que su aplicación registrada inicie sesión en Exchange Online en nombre de la organización. Debe dar su consentimiento para completar la configuración.

   > [!NOTE]
   > Si no se le solicita que inicie sesión con su cuenta de administrador, podría deberse a que las ventanas emergentes están bloqueadas. Para iniciar sesión, permita las ventanas emergentes de https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Usar otro servicio de administración de identidades y accesos
Si no estas usando Azure Active Directory para administrar las identidades y el acceso, necesitará ayuda de un desarrollador. Si prefiere almacenar el identificador y el secreto de la aplicación en una ubicación diferente, puede dejar en blanco los campos Id . del cliente y Secreto del cliente y escribir una extensión para obtener el identificador y el secreto de la ubicación. Puede proporcionar el secreto en tiempo de ejecución suscribiéndose a los eventos OnGetEmailLoggingClientId y OnGetEmailLoggingClientSecret en la codeunit 1641 "Impl. de CDS Integration".

### <a name="to-stop-logging-email"></a>Para dejar de registrar correo electrónico
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de marketing** y luego elija el enlace relacionado.
2. Desactive el botón de alternancia **Habilitado**.

## <a name="see-also"></a>Consulte también
[Gestionar las relaciones](marketing-relationship-management.md)

