---
title: Experiencias contables en Business Central
description: Obtenga más información sobre el Área de trabajo contable y el hub de empresas que admite contables internos y externos en la empresa cliente.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 06/12/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="accountant-experiences-in-"></a>Experiencias contables en [!INCLUDE[prod_long](includes/prod_long.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Independientemente del tipo de contable que sea, puede utilizar el Área de trabajo **Contable** como su página de inicio en [!INCLUDE[prod_short](includes/prod_short.md)]. Desde aquí, puede acceder a todas las páginas que necesita en su trabajo.  

## <a name="accountant-role-center"></a>Área de trabajo Contable

El Área de trabajo es un tablero de mandos con cuadros de actividad que le muestran cifras clave en tiempo real y le proporcionan un acceso rápido a los datos. La cinta de la parte superior de la página le da acceso a más acciones. Por ejemplo, para abrir informes y estados financieros en Excel. En la barra de navegación superior, puede cambiar rápidamente entre las listas que utiliza con mayor frecuencia. Aquí verá otras áreas como **Docs. registrados** con varios tipos de documentos que la empresa ha registrado.  

Si es nuevo en [!INCLUDE[prod_short](includes/prod_short.md)], puede iniciar una lista de videos directamente desde su área de trabajo. También puede abrir el paseo **Introducción** que se centra en las áreas clave.  

## <a name="company-hub"></a>Hub de empresas

Si trabaja en varias empresas [!INCLUDE [prod_short](includes/prod_short.md)], puede resultarle útil utilizar la página **Hub de empresas** para realizar un seguimiento del trabajo. Para más información, consulte [Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Invitación del contable externo a [!INCLUDE[prod_short](includes/prod_short.md)]

Si utiliza un contable externo para administrar los libros y los informes financieros, su administrador puede invitarle a su [!INCLUDE[prod_short](includes/prod_short.md)] para que pueda trabajar con usted en los datos fiscales. [!INCLUDE[prod_short](includes/prod_short.md)] incluye tres licencias de tipo Contable externo. Para obtener información detallada acerca de las licencias, descargue la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=866544).

Una vez que el contable ha tenido acceso a su [!INCLUDE[prod_short](includes/prod_short.md)], puede utilizar el área de trabajo **Contable** para un acceso fácil a las páginas para el trabajo. También pueden utilizar el hub de empresas en su propio [!INCLUDE [prod_short](includes/prod_short.md)] para gestionar su trabajo. Para más información, consulte [Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Es fácil invitar a su contable externo. Abra la página **Usuarios**, y seleccione la acción **Invitar a contable externo** en la cinta de opciones. Se le crea un correo electrónico, ahora simplemente agregue el correo electrónico de trabajo de su contable y envíe la invitación.  

> [!Note]  
> Para ello es necesario que haya configurado el correo electrónico SMTP. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> La dirección de correo electrónico del contable debe ser una dirección de trabajo basada en Microsoft Entra ID. Si el contable utiliza otro tipo de correo electrónico, la invitación no se podrá enviar.
>
> Esta tarea requiere acceso para administrar usuarios y licencias en Microsoft Entra ID. El usuario que envía esta invitación debe tener asignado al menos el rol de  [Administrador de usuarios](/entra/identity/role-based-access-control/permissions-reference#user-administrator)  en el Microsoft 365 Centro de administración. Para obtener más información, consulte [Acerca de los roles de administrador](/microsoft-365/admin/add-users/about-admin-roles) en el contenido de administración de Microsoft 365.  

### <a name="add-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Agregar su contable a su Microsoft 365 en Azure Portal

Si su administrador o distribuidor no desea utilizar la guía **Invitar a un contable externo**, pueden añadir un usuario externo en Azure Portal y asignar a este usuario la licencia *Contable externo*. Para más información, consulte [Inicio rápido: añada usuarios invitados a su directorio en Azure Portal](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Para añadir a su contable como usuario invitado

1. Abrir el [Portal de Azure](https://portal.azure.com/).
2. En el panel izquierdo, seleccione **Microsoft Entra ID**.
3. Bajo **Gestionar**, seleccione **Los usuarios**.
4. Seleccione **Nuevo usuario invitado**.
5. Sobre la página **Nuevo Usuario**, seleccione **Invitar usuario** y luego añada información sobre su contable externo.  

   De manera opcional, incluya un mensaje de bienvenida personal al contable para informarle de que los está agregando a su [!INCLUDE[prod_short](includes/prod_short.md)].

6. Seleccione **Invitación** para enviar automáticamente la invitación. Aparece una notificación en la esquina superior derecha con el mensaje **Usuario invitado exitosamente**. 
7. Después de enviar la invitación, la cuenta de usuario se añade automáticamente al directorio como invitado.

A continuación, debe asignar al nuevo usuario invitado una licencia para [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-"></a>Para darle acceso a su contable a su [!INCLUDE[prod_short](includes/prod_short.md)]

1. En Azure Portal, en el usuario recién agregado, elija **Perfil** y luego elija **Editar**
2. Actualizar el campo **Lugar de uso** al país o región relevante y luego elija **Guardar**.
3. Escoger **Licencias**y luego abrir **Asignaciones**.
4. Elegir la licencia del **Dynamics 365 Business Central Contable Externo**.  
    
    Si esta licencia no está disponible, comuníquese con su socio revendedor para agregar la licencia a su suscripción.

    Específicamente para propósitos de evaluación en un inquilino de prueba, puede usar una licencia disponible de **Dynamics 365 Business Central para IW** en su lugar. Sin embargo, no puede utilizar este tipo de licencia si ya ha adquirido [!INCLUDE[prod_short](includes/prod_short.md)]. 
5. Guarda la tarea.

Si tiene éxito, la licencia se asigna al usuario invitado y se crea la cuenta de invitado.

### <a name="import-the-new-user-into-"></a>Importar el nuevo usuario a [!INCLUDE[prod_short](includes/prod_short.md)]

El contador recibe un correo electrónico que le notifica que se le ha dado acceso a su Microsoft Entra ID. A continuación, debe darles acceso a la compañía correcta en [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Para añadir el contable a la empresa correcta

1. Abra la [!INCLUDE[prod_short](includes/prod_short.md)] empresa a la que desea dar acceso al contable en [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios** y luego elija el enlace relacionado.  
3. Elija la acción **Obtener nuevos usuarios de Microsoft 365**.

Esta acción importa la cuenta de usuario que creó en Azure Portal a la empresa. Para obtener más información, consulte [Para añadir un usuario en Business Central](ui-how-users-permissions.md#adduser).  

Si desea dar acceso a varias empresas, debe iniciar sesión en cada compañía y repetir este proceso. Alternativamente, puede actualizar los grupos de permisos para el perfil de usuario del contador en [!INCLUDE[prod_short](includes/prod_short.md)], como asignarles el *grupo de usuario* D365 Bus Premium. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Análisis de estados financieros en Excel](finance-analyze-excel.md)  
[Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
