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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 79ed5e1b7200a668be2aa078531fd68e0131b6ff
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302601"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Experiencias contables en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Los negocios deben crear sus libros y firmas de contabilidad. Algunas empresas emplean un contable externo, y otras lo tienen en plantilla. Independientemente del tipo de contable que sea, puede utilizar el Área de trabajo **Contable** como su página de inicio en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Desde aquí, puede acceder a todas las páginas que necesita en su trabajo.  

## <a name="accountant-role-center"></a>Área de trabajo Contable
El Área de trabajo es un tablero de mandos con cuadros de actividad que le muestran cifras clave en tiempo real y le proporcionan un acceso rápido a los datos. En la cinta en la parte superior de la página tiene acceso a más acciones, como abrir los informes financieros y las declaraciones más utilizados en Excel. En la barra de navegación superior, puede cambiar rápidamente entre las listas que utiliza con mayor frecuencia. Aquí verá otras áreas como **Docs. registrados** con varios tipos de documentos que la empresa ha registrado.  

Si es nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede iniciar una lista de videos directamente desde su área de trabajo. También puede abrir el paseo **Introducción** que se centra en las áreas clave.  

## <a name="accountant-hub"></a>Accountant Hub
Si es un contable con varios clientes, puede utilizar [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] para obtener una mejor visión general de sus clientes. Desde allí, puede acceder al suscriptor de cada cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)] y utilizar el Área de trabajo Contable como se describe anteriormente. Para obtener más información, vea [[!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] se encuentra actualmente en vista previa pública en un número reducido de mercados.

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365fin_mdmd"></a>Invitación del contable externo a [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[d365fin](includes/d365fin_md.md)] para que pueda trabajar con usted en los datos fiscales.

Una vez que el contable ha accedido a su [!INCLUDE[d365fin](includes/d365fin_md.md)], puede utilizar el área de trabajo **Contable** que da acceso fácil a las páginas más relevantes para el trabajo.  

Hemos facilitado la invitación a su contable externo. Abra simplemente la página **Usuarios**, y seleccione la acción **Invitar a contable externo** en la cinta de opciones. Se le crea un correo electrónico, ahora simplemente agregue el correo electrónico de trabajo de su contable y envíe la invitación.  

![Invitar al contable](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
> Para ello es necesario que haya configurado el correo electrónico SMTP. Puede hacerlo usted mismo o preguntarle a su socio de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Además, debe iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como administrador y no como propietario u otros usuarios. Finalmente, debe haber abandonado la empresa de prueba para tener un administrador de Azure Active Directory.  

> [!IMPORTANT]  
> La dirección de correo electrónico del contable debe ser una dirección de trabajo basada en Azure Active Directory. Si el contable utiliza otro tipo de correo electrónico, la invitación no se podrá enviar.  

### <a name="separate-license"></a>Licencia independiente
En segundo plano, el contable se agrega a su suscriptor de Active Directory. Su administrador puede verificar que el contable acepta la invitación y se le asigna la licencia correcta. Los pasos para hacerlo dependen del tipo de cuenta que utilizó al registrarse en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este tema se basa en el uso de una cuenta de Office 365, que usa Microsoft Azure Active Directory.  

Si ha activado su suscripción de [!INCLUDE[d365fin](includes/d365fin_md.md)] y ya no utiliza la empresa de valoración, dispone de un suscriptor de Azure Active Directory. El administrador o el socio de [!INCLUDE[d365fin](includes/d365fin_md.md)] administra este suscriptor en el [portal de Azure](https://portal.azure.com). Aquí es donde se agregan nuevos usuarios y se aplican y se eliminan las licencias. Para obtener más información, consulte el [resumen del portal de Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Uno de los tipos de licencia para [!INCLUDE[d365fin](includes/d365fin_md.md)] es la licencia *Contable externo*. Este tipo de salida está pensado para que lo utilicen usuarios como, por ejemplo, contables externos. Esto significa que no tiene que comprar un puesto adicional en su Active Directory actual ni usar una de las cuentas de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] existentes en el contable externo. Por ejemplo, si su suscripción de Office 365 actual incluye 10 usuarios para [!INCLUDE[d365fin](includes/d365fin_md.md)] y actualmente usa 10 licencias *Usuario completo*, el administrador puede agregar su contable externo como usuario invitado en el portal de Azure y asignarle la licencia *Contable externo* sin coste adicional. No obstante, solo puede tener un usuario con la licencia *Contable externo*. Si desea añadir más usuarios, debe actualizar su suscripción de Office 365 en consecuencia.

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
[Dynamics 365 - Accountant Hub en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
