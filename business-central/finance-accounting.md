---
title: Experiencia contable de Business Central | Documentos de Microsoft
description: Obtenga más información sobre el portal contable de Business Central y el Área de trabajo Contable que admite a los contadores interno y externo en la empresa cliente.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/11/2020
ms.author: edupont
ms.openlocfilehash: eae48b25446e4c81d1b8eae86fd2d0d7d0126df6
ms.sourcegitcommit: b9264b4ed650feca18776892ec23f2aa7ec43e20
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372621"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Experiencias contables en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Independientemente del tipo de contable que sea, puede utilizar el Área de trabajo **Contable** como su página de inicio en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Desde aquí, puede acceder a todas las páginas que necesita en su trabajo.  

## <a name="accountant-role-center"></a>Área de trabajo Contable
El Área de trabajo es un tablero de mandos con cuadros de actividad que le muestran cifras clave en tiempo real y le proporcionan un acceso rápido a los datos. En la cinta en la parte superior de la página tiene acceso a más acciones, como abrir los informes financieros y las declaraciones más utilizados en Excel. En la barra de navegación superior, puede cambiar rápidamente entre las listas que utiliza con mayor frecuencia. Aquí verá otras áreas como **Docs. registrados** con varios tipos de documentos que la empresa ha registrado.  

Si es nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede iniciar una lista de videos directamente desde su área de trabajo. También puede abrir el paseo **Introducción** que se centra en las áreas clave.  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Invitación del contable externo a [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si utiliza un contable externo para administrar los libros y los informes financieros, su administrador puede invitarle a su [!INCLUDE[d365fin](includes/d365fin_md.md)] para que pueda trabajar con usted en los datos fiscales. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye tres licencias de tipo Contable externo. Para obtener información detallada acerca de las licencias, consulte la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Una vez que el contable ha accedido a su [!INCLUDE[d365fin](includes/d365fin_md.md)], puede utilizar el área de trabajo **Contable** que da acceso fácil a las páginas más relevantes para el trabajo.  

Hemos facilitado la invitación a su contable externo. Abra simplemente la página **Usuarios**, y seleccione la acción **Invitar a contable externo** en la cinta de opciones. Se le crea un correo electrónico, ahora simplemente agregue el correo electrónico de trabajo de su contable y envíe la invitación.  

> [!Note]  
> Para ello es necesario que haya configurado el correo electrónico SMTP. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> La dirección de correo electrónico del contable debe ser una dirección de trabajo basada en Azure Active Directory. Si el contable utiliza otro tipo de correo electrónico, la invitación no se podrá enviar. 
> 
> Esta tarea requiere acceso para administrar usuarios y licencias en Azure Active Directory, el usuario que envía esta invitación debe tener asignado el rol **Administrador global** o **Administrador de usuarios** en el centro de administración de Microsoft 365. Para obtener más información, consulte [Acerca de los roles de administrador](/microsoft-365/admin/add-users/about-admin-roles) en el contenido de administración de Microsoft 365.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Añadir su contable a su Office 365 a través de Azure Portal

Si su administrador o distribuidor no desea utilizar la guía **Invitar a un contador externo**, pueden añadir un usuario externo en el Portal de Azure y asignar a este usuario la licencia de Contable externo. Para más información, consulte [Inicio rápido: añada usuarios invitados a su directorio en Azure Portal](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Para añadir a su contable como usuario invitado

1. Abrir el [Portal de Azure](https://portal.azure.com/).
2. En el panel izquierdo, seleccione **Azure Active Directory**.
3. Bajo **Gestionar**, seleccione **Los usuarios**.
4. Seleccione **Nuevo usuario invitado**.
5. Sobre la página **Nuevo Usuario**, seleccione **Invitar usuario** y luego añada información sobre su contable externo.  

   De manera opcional, incluya un mensaje de bienvenida personal al contable para informarle de que los está agregando a su [!INCLUDE [prodshort](includes/prodshort.md)].

6. Seleccione **Invitación** para enviar automáticamente la invitación. Aparece una notificación en la esquina superior derecha con el mensaje **Usuario invitado exitosamente**. 
7. Después de enviar la invitación, la cuenta de usuario se añade automáticamente al directorio como invitado.

A continuación, debe asignar al nuevo usuario invitado una licencia para [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Para darle acceso a su contable a su [!INCLUDE [prodshort](includes/prodshort.md)]

1. En Azure Portal, en el usuario recién agregado, elija **Perfil** y luego elija **Editar**
2. Actualizar el campo **Lugar de uso** al país relevante y luego elija **Guardar**.
3. Escoger **Licencias**y luego abrir **Asignaciones**.
4. Elegir la licencia del **Dynamics 365 Business Central Contable Externo**.  

    Si esta licencia no está disponible, debe usar una licencia disponible **Dynamics 365 Business Central para IWs** en su lugar.
5. Guarda la tarea.

Si tiene éxito, la licencia se asigna al usuario invitado y se crea la cuenta de invitado.

### <a name="importing-the-new-user-into-prodshort"></a>Importar al nuevo usuario a [!INCLUDE [prodshort](includes/prodshort.md)]

El contador recibirá un correo electrónico que le notifica que se le ha dado acceso a su Active Directory. A continuación, debe darles acceso a la compañía correcta en [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Para añadir el contable a la empresa correcta

1. Abra la [!INCLUDE [prodshort](includes/prodshort.md)] empresa a la que desea dar acceso al contable en [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Usuarios** y luego elija el enlace relacionado.  
3. Elija la acción **Obtener nuevos usuarios de Office 365**.

Esto importa la cuenta de usuario que creó en Azure Portal a la empresa. Para obtener más información, consulte [Para añadir un usuario en Business Central](ui-how-users-permissions.md#adduser).  

Si desea dar acceso a varias empresas, debe iniciar sesión en cada compañía y repetir este proceso. Alternativamente, puede actualizar los grupos de permisos para el perfil de usuario del contador en [!INCLUDE [prodshort](includes/prodshort.md)], como asignarles el *grupo de usuario* D365 Bus Premium. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).  

## <a name="accountant-hub"></a>Accountant Hub

Si es un contable con varios clientes, puede utilizar [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] para obtener una mejor visión general de sus clientes. Desde allí, puede acceder al suscriptor de cada cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)] y utilizar el Área de trabajo Contable como se describe anteriormente. Para obtener más información, vea [[!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] se encuentra actualmente en vista previa pública en un número reducido de mercados.

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Análisis de estados financieros en Excel](finance-analyze-excel.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md)  
[[!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub en Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
