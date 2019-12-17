---
title: Configurar el correo electrónico en Business Central | Documentos de Microsoft
description: Describe cómo usar el servidor SMTP de la empresa para enviar y recibir mensajes de correo electrónico en Business Central, así como el modo de usar la configuración del servidor de correo electrónico creada con la suscripción de Office 365.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: e1f24e6da71d32e162b107b0e0b9e01cb68cc302
ms.sourcegitcommit: 23577ae8ecaaf09b58716c2b9f65e39c188e3661
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2019
ms.locfileid: "2810818"
---
# <a name="set-up-email"></a>Configurar correo electrónico
Para enviar y recibir los correos electrónicos desde [!INCLUDE[d365fin](includes/d365fin_md.md)], debe rellenar los campos de la página Configuración correo SMTP.

En lugar de especificar los detalles del servidor SMTP manualmente, puede utilizar la función **Aplicar la configuración del servidor de Office 365** para introducirlos con la información de su suscripción de Office 365.

Puede configurar el correo electrónico manualmente, tal como se describe a continuación, o puede obtener ayuda mediante la guía de configuración asistida **Configuración correo electrónico**. Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Para configurar el correo electrónico
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Si está utilizando una cuenta que requiere autenticación de dos factores, la contraseña que introduzca en el campo **Contraseña** debe ser la misma que la que utiliza para su suscripción de Office 365 y debe ser de tipo **Contraseña de aplicación**. Para obtener más información, consulte [Administrar las contraseñas de aplicación para la verificación en dos pasos](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 
3. Opcionalmente, elija la acción **Aplicar la configuración del servidor de Office 365** para insertar información que ya esté definida para su suscripción de Office 365.
4. Una vez rellenados correctamente todos los campos, elija la acción **Configuración de correo elect. de prueba**.
5. Cuando la prueba se realice correctamente, cierre la página.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Uso de una dirección de remitente sustituta en los mensajes de correo electrónico salientes
Todos los mensajes de correo electrónico salientes desde [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizarán la dirección predeterminada de la cuenta que especificó en la página Configuración de correo electrónico SMTP, como se describe más arriba. Sin embargo, puede utilizar las funciones **Enviar como** o **Enviar en nombre de** en su servidor Exchange para cambiar la dirección del remitente en los mensajes salientes. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizará la cuenta predeterminada para autenticarse en Exchange, pero sustituirá la dirección del remitente por la que especifique o la modificará con "en nombre de".

A continuación se ofrecen ejemplos de cómo se usan Enviar como y Enviar en nombre de en [!INCLUDE[d365fin](includes/d365fin_md.md)]:

 * Al enviar documentos como pedidos de compra o de venta a proveedores y clientes, es posible que desee que parezcan proceder de una dirección _noreply@yourcompanyname.com_.
 * Cuando su flujo de trabajo envía una solicitud de aprobación por correo electrónico utilizando la dirección de correo electrónico del solicitante.

> [!Note]
> Solo puede utilizar una cuenta para sustituir las direcciones de remitente. Es decir, no puede tener una dirección sustituta para los procesos de compra y otra para los procesos de venta.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Para configurar la dirección de remitente sustituta para todos los mensajes de correo electrónico salientes
1. En el **centro de administración de Exchange** de su cuenta de Office 365, busque el buzón de correo para utilizarlo como dirección sustituta y, a continuación, copie o anote la dirección. Si necesita una nueva dirección, vaya a su centro de administración de Microsoft 365 para crear un nuevo usuario y configurar su buzón de correo.
2. En [!INCLUDE[d365fin](includes/d365fin_md.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
3. En el campo **Enviar como**, introduzca la dirección sustituta.
4. Copie o anote la dirección en el campo **ID de usuario**.
5. En el **centro de administración de Exchange**, busque el buzón de correo que desea utilizar como dirección sustituta y, a continuación, introduzca la dirección del campo **ID de usuario** en el campo **Enviar como**. Para obtener más información, vea [Administrar permisos para destinatarios](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Para utilizar la dirección sustituta en los flujos de trabajo de aprobación
1. En [!INCLUDE[d365fin](includes/d365fin_md.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
2. Copie o anote la dirección en el campo **ID de usuario**.
3. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. usuario aprobación** y luego elija el enlace relacionado.
4. En el **centro de administración de Exchange**, busque los buzones de correo de cada usuario que aparece en la página **Configuración de usuario de aprobación** y, en el campo **Enviar como**, introduzca la dirección del campo **ID de usuario** de la página **Configuración de correo electrónico SMTP** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Administrar permisos para destinatarios](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. En [!INCLUDE[d365fin](includes/d365fin_md.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de correo electrónico SMTP** y luego elija el enlace relacionado.
6. Para habilitar la sustitución, active **Permitir sustitución del remitente**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] determinará qué dirección se mostrará en el siguiente orden: <br><br> 1. La dirección especificada en el campo **Correo electrónico** de la página **Configuración de usuario de aprobación** para los mensajes en un flujo de trabajo. <br> 2. La dirección especificada en el campo **Enviar como** de la página **Configuración de correo electrónico SMTP**. <br> 3. La dirección especificada en el campo **ID de usuario** de la página **Configuración de correo electrónico SMTP**.


## <a name="see-also"></a>Consulte también

[Buzones compartidos en Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como su bandeja de entrada de empresa en Outlook](admin-outlook.md)  
[Obtener [!INCLUDE[d365fin](includes/d365fin_md.md)] en el dispositivo móvil](install-mobile-app.md)
