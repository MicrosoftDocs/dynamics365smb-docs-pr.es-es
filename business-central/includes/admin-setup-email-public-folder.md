---
author: brentholtorf
ms.topic: include
ms.date: 02/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!NOTE]
> Las siguientes secciones asumen que tiene acceso de administrador para Exchange Online.

Antes de poder configurar el registro de correo electrónico, debe preparar las [carpetas públicas](/exchange/collaboration-exo/public-folders/public-folders) de Office 365. Puede hacer esto en el [Centro de administración de Exchange](/exchange/exchange-admin-center?preserve-view=true) o puede usar el [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Si quiere usar el [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true), puede encontrar ideas sobre cómo configurar su script en un script de muestra que publicamos para el [repositorio de BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Siga los pasos a continuación para configurar Exchange Online, con enlaces a donde puede obtener más información.

### Crear un grupo de roles de administrador

Cree un grupo de funciones de administrador para las carpetas públicas basada en la información de la siguiente tabla:

|Propiedad        |Valor                     |
|----------------|--------------------------|
|Name            |Administración de carpetas públicas |
|Roles seleccionados  |Carpetas públicas            |
|Usuarios seleccionados  |El correo electrónico de la cuenta de usuario que Business Central usará para ejecutar el trabajo de registro de correo electrónico|

Para obtener más información, vea [Administrar grupos de roles en Exchange Online](/exchange/permissions-exo/role-groups).

### Crear un nuevo buzón de carpeta pública

Cree un buzón nuevo de carpetas públicas basado en la información de la siguiente tabla:

|Propiedad        |Valor                     |
|----------------|--------------------------|
|Name            |Buzón público            |

Para obtener más información, vea [Crear un buzón de carpeta pública](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### Crear carpetas públicas nuevas

1. Cree una nueva carpeta pública con el nombre **Registro de correo electrónico** en la raíz para que la ruta completa a la carpeta pase a ser `\Email Logging\`.
2. Cree dos subcarpetas para que el resultado sea la siguiente ruta completa a las carpetas:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Para obtener más información, vea [Crear una carpeta pública](/exchange/collaboration-exo/public-folders/create-public-folder).

### Establecer la propiedad de la carpeta pública

Configure el usuario de registro de correo electrónico como propietario de ambas carpetas públicas, *Cola* y *Almacenamiento*.

Para obtener más información, vea [Asignar permisos a la carpeta pública](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### Habilitar la carpeta pública *Cola* para el correo electrónico

  Para más información, consulte [Habilitar o deshabilitar una carpeta pública para el correo electrónico](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### Habilitar el envío de correos electrónicos para la carpeta pública *Cola*

Habilitar el envío de correos electrónicos para la carpeta pública *Cola* con Outlook o el Shell de administración de Exchange.

Para más información, vea [Permitir a los usuarios anónimos enviar correos electrónicos a una carpeta pública habilitada para correo](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### Crear reglas de flujo de correo

Cree dos reglas de flujo de correo basadas en la información de la siguiente tabla:

|Propósito  |Name |Aplique esta regla si...             |Haga lo siguiente...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Una regla para el correo electrónico entrante |Registrar el correo electrónico enviado a esta organización|*El remitente* se encuentra *Fuera de la organización* y *el destinatario* se encuentra *Dentro de la organización*|Incluya en CCO la cuenta de correo electrónico que se especifica para la carpeta pública *Cola*|
|Una regla para el correo electrónico saliente | Registrar el correo electrónico enviado desde esta organización |*El remitente* se encuentra *Dentro de la organización* y *el destinatario* se encuentra *Fuera de la organización*|Incluya en CCO la cuenta de correo electrónico que se especifica para la carpeta pública *Cola*|

Para obtener más información, consulte [Administrar reglas de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) y [Acciones de regla de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Si realiza cambios en el Shell de administración de Exchange, los cambios se hacen visibles en el centro de administración de Exchange después de un tiempo. Además, los cambios realizados en Exchange estarán disponibles en [!INCLUDE[prod_short](prod_short.md)] después de un tiempo. El retraso puede ser de varias horas.
