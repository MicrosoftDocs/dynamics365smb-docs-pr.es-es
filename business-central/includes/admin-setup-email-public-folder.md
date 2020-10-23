---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: a62a1a628f22ff47fa86a64a72f5b1834960dc72
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3931276"
---
Antes de poder configurar el registro de correo electrónico, debe preparar su Exchange Online con [carpetas públicas](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Puede hacer esto en el [Centro de administración de Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) o puede usar el [Shell de administración de Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Si quiere usar el [Shell de administración de Exchange](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), puede encontrar ideas sobre cómo configurar su script en un script de muestra que publicamos para [el repositorio de BCTech](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

La siguiente lista describe los pasos principales con enlaces para obtener más información.  

- Cree una función de administrador para las carpetas públicas basada en la información de la siguiente tabla:

  |Propiedad        |Valor                     |
  |----------------|--------------------------|
  |Name            |Administración de carpetas públicas |
  |Roles seleccionados  |Carpetas públicas            |
  |Miembros seleccionados|El correo electrónico de la cuenta de usuario que Business Central usará para ejecutar el trabajo de registro de correo electrónico|

  Para obtener más información, vea [Administrar grupos de roles](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Cree un buzón nuevo de carpetas públicas basado en la información de la siguiente tabla:

  |Propiedad        |Valor                     |
  |----------------|--------------------------|
  |Name            |Buzón público            |

  Para obtener más información, vea [Crear un buzón de carpetas públicas en Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Crear carpetas públicas nuevas

  - Cree una nueva carpeta pública con el nombre *Registro de correo electrónico* en la raíz para que la ruta completa a la carpeta pase a ser ```\Email Logging\```
  - Cree dos subcarpetas para que el resultado sea la siguiente ruta completa a las carpetas:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Para obtener más información, vea [Crear una carpeta pública](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Habilitar la carpeta pública *Cola* para el correo electrónico

  Para más información, vea [Habilitar o deshabilitar una carpeta pública para el correo electrónico](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Habilitar el envío de correos electrónicos para la carpeta pública *Cola* con Outlook o el Shell de administración de Exchange

  Para más información, vea [Permitir a los usuarios anónimos enviar correos electrónicos a una carpeta pública habilitada para correo](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Establezca el usuario de registro de correo electrónico como propietario de ambas carpetas públicas, *Cola* y *Almacenamiento* con Outlook o el Shell de administración de Exchange según la información de la siguiente tabla:

  |Propiedad        |Valor                     |
  |----------------|--------------------------|
  |Usuario            |El correo electrónico de la cuenta de usuario que Business Central usará para ejecutar el trabajo de registro de correo electrónico|
  |Nivel de permiso|Propietario                     |

  Para obtener más información, vea [Asignar permisos a la carpeta pública](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Crear dos reglas de flujo de correo basadas en la información de la siguiente tabla:

  |Propósito  |Name |Condiciones                        |Acción                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Una regla para el correo electrónico entrante |Registrar el correo electrónico enviado a esta organización|*El remitente* se encuentra *Fuera de la organización* y *el destinatario* se encuentra *Dentro de la organización*|Incluya en CCO la cuenta de correo electrónico que se especifica para la carpeta pública *Cola*|
  |Una regla para el correo electrónico saliente | Registrar el correo electrónico enviado desde esta organización |*El remitente* se encuentra *Dentro de la organización* y *el destinatario* se encuentra *Fuera de la organización*|Incluya en CCO la cuenta de correo electrónico que se especifica para la carpeta pública *Cola*|
  
  Para más información, vea [Administrar reglas de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) y [Acciones de regla de flujo de correo en Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Si realiza cambios en el Shell de administración de Exchange, los cambios se hacen visibles en el centro de administración de Exchange después de un tiempo. Además, los cambios realizados en Exchange estarán disponibles en [!INCLUDE[prodshort](prodshort.md)] después de un tiempo.
