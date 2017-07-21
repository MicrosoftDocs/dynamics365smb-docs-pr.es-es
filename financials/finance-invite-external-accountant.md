---
title: Agregar el contable externo a Financials | Documentos de Microsoft
description: "Obtenga información sobre cómo puede invitar a su contable externo a Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitar al contable externo a [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si utiliza un contable externo para administrar los libros y los informes financieros, puede invitarle a su [!INCLUDE[d365fin](includes/d365fin_md.md)] para que pueda trabajar con usted en los datos fiscales.

Una vez que el contable ha accedido a su [!INCLUDE[d365fin](includes/d365fin_md.md)], puede utilizar el área de trabajo **Contable** que da acceso fácil a las ventanas más relevantes para el trabajo.  

> [!NOTE]  
>  Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de Financials](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Invitar al contable a [!INCLUDE[d365fin](includes/d365fin_md.md)]
En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)], la invitación del contable externo requiere que un administrador lo agregue al suscriptor de Active Directory. Los pasos para hacerlo dependen del tipo de cuenta que utilizó al registrarse en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este tema se basa en el uso de una cuenta de Office 365, que usa Microsoft Azure Active Directory.  

> [!TIP]  
>  Es recomendable que se ponga en contacto con su socio de [!INCLUDE[d365fin](includes/d365fin_md.md)] para obtener ayuda.  

Si ha activado su suscripción de [!INCLUDE[d365fin](includes/d365fin_md.md)] y ya no utiliza la empresa de valoración, dispone de un suscriptor de Azure Active Directory. El administrador o el socio de [!INCLUDE[d365fin](includes/d365fin_md.md)] administra este suscriptor en el [portal de Azure](https://portal.azure.com). Aquí es donde se agregan nuevos usuarios y se aplican y se eliminan las licencias. Para obtener más información, vea el [resumen del portal de Microsoft Azure](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Licencia independiente
Uno de los tipos de licencia para [!INCLUDE[d365fin](includes/d365fin_md.md)] es la licencia *Contable externo*. Este tipo de salida está pensado para que lo utilicen usuarios como, por ejemplo, contables externos. Esto significa que no tiene que comprar un puesto adicional en su Active Directory actual ni usar una de las cuentas de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] existentes en el contable externo. Por ejemplo, si su suscripción de Office 365 actual incluye 10 usuarios para [!INCLUDE[d365fin](includes/d365fin_md.md)] y actualmente usa 10 licencias *Usuario completo*, el administrador puede agregar su contable externo como usuario invitado en el portal de Azure y asignarle la licencia *Contable externo* sin coste adicional. No obstante, solo puede tener un usuario con la licencia *Contable externo*. Si desea añadir más usuarios, debe actualizar su suscripción de Office 365 en consecuencia.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Experiencias contables en Dynamics 365 for Financials](finance-accounting.md)  
[Financials para contables en Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

