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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896138"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Experiencias contables en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Independientemente del tipo de contable que sea, puede utilizar el Área de trabajo **Contable** como su página de inicio en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Desde aquí, puede acceder a todas las páginas que necesita en su trabajo.  

## <a name="accountant-role-center"></a>Área de trabajo Contable
El Área de trabajo es un tablero de mandos con cuadros de actividad que le muestran cifras clave en tiempo real y le proporcionan un acceso rápido a los datos. En la cinta en la parte superior de la página tiene acceso a más acciones, como abrir los informes financieros y las declaraciones más utilizados en Excel. En la barra de navegación superior, puede cambiar rápidamente entre las listas que utiliza con mayor frecuencia. Aquí verá otras áreas como **Docs. registrados** con varios tipos de documentos que la empresa ha registrado.  

Si es nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede iniciar una lista de videos directamente desde su área de trabajo. También puede abrir el paseo **Introducción** que se centra en las áreas clave.  

## <a name="inviteaccountant"></a>Invitación del contable externo a [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[d365fin](includes/d365fin_md.md)] para que pueda trabajar con usted en los datos fiscales.

Una vez que el contable ha accedido a su [!INCLUDE[d365fin](includes/d365fin_md.md)], puede utilizar el área de trabajo **Contable** que da acceso fácil a las páginas más relevantes para el trabajo.  

Hemos facilitado la invitación a su contable externo. Abra simplemente la página **Usuarios**, y seleccione la acción **Invitar a contable externo** en la cinta de opciones. Se le crea un correo electrónico, ahora simplemente agregue el correo electrónico de trabajo de su contable y envíe la invitación.  
> [!Note]  
> Para ello es necesario que haya configurado el correo electrónico SMTP. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).   

![Invitar al contable](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> La dirección de correo electrónico del contable debe ser una dirección de trabajo basada en Azure Active Directory. Si el contable utiliza otro tipo de correo electrónico, la invitación no se podrá enviar.  

### <a name="behind-the-scenes"></a>En segundo plano
[!INCLUDE[d365fin](includes/d365fin_md.md)] incluye tres licencias de tipo Contable externo. Si su empresa utiliza un contable externo, puede dar acceso a su [!INCLUDE[d365fin](includes/d365fin_md.md)] al asignarle una licencia de ese tipo. Para obtener más información sobre las licencias, consulte la [Guía de licencias de Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590). 

Si su suscripción aún tiene una licencia disponible, su administrador o socio distribuidor puede agregar un usuario externo a través de Azure Portal y asignarle a este usuario la licencia Contable externo. Para obtener más información, vea [Agregar usuarios de colaboración B2B de Azure Active Directory en el portal de Azure](/azure/active-directory/b2b/add-users-administrator).

Luego puede invitar al contable desde [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante el uso de la guía de configuración asistida **Invitar a contable externo**. Sin embargo, debido a que esta tarea requiere acceso para administrar usuarios y licencias en Azure Active Directory, el usuario que envía esta invitación debe tener asignado el rol **Administrador global** o **Administrador de usuarios** en el centro de administración de Office 365. Para obtener más información, consulte [Acerca de los roles de administrador](/office365/admin/add-users/about-admin-roles) en el contenido de administración de Office 365. 

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
