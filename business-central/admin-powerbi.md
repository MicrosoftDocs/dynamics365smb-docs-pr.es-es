---
title: Introducción a Business Central y Power BI | Documentos de Microsoft
description: Obtener uan introducción al uso de Power BI para conseguir información, inteligencia empresarial y KPI desde los datos de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 38d7cc9bf45c3bef239a68cd0e4865ef2833776e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935141"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] y Power BI

Obtener información sobre los datos de [!INCLUDE[prod_short](includes/prod_short.md)] es fácil con [Power BI](https://powerbi.microsoft.com), un sistema de visualización de datos de Microsoft. Power BI recupera datos de [!INCLUDE[prod_short](includes/prod_short.md)] que le permiten crear paneles e informes basados en esos datos. Power BI proporciona una alternativa flexible a los informes integrados en [!INCLUDE[prod_short](includes/prod_short.md)], lo que le permite desglosar y personalizar la visualización, e incluso fusionar datos de diferentes empresas en [!INCLUDE[prod_short](includes/prod_short.md)]. Algunos informes de Power BI también pueden integrarse en Business Central y visualizarse sin salir del sistema. Los paneles de control más complejos se experimentan mejor desde el sitio web de Power BI.

![Power BI y Business Central](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>¿Qué puede hacer con Power BI y [!INCLUDE[prod_short](includes/prod_short.md)]?

Hay varias funciones para trabajar con [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. Algunas cosas se pueden hacer desde Power BI, mientras que otras cosas se hacen desde [!INCLUDE[prod_short](includes/prod_short.md)]. Además, algunas funciones solo están disponibles con [!INCLUDE[prod_short](includes/prod_short.md)] online, no local. La siguiente tabla le ofrece una descripción general.

|Característica|Descripción|Online|Local|Más información|
|-------|-----------|--------------|-----------|----------------|
|Ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI|Puede ver sus datos desde [!INCLUDE[prod_short](includes/prod_short.md)] en informes en Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online incluye algunos informes de Power BI predefinidos. O su organización puede haber puesto a su disposición algunos informes personalizados.|![Trabaja en línea](media/check.png)|![Trabaja localmente](media/check.png)|[Vea...](across-working-with-business-central-in-powerbi.md)|
|Ver informes de Power BI en el cliente de [!INCLUDE[prod_short](includes/prod_short.md)].| Los informes de Power BI que muestran datos de [!INCLUDE[prod_short](includes/prod_short.md)] se pueden incrustar directamente en las páginas de partes de [!INCLUDE[prod_short](includes/prod_short.md)]. Puede cambiar la parte para mostrar cualquier informe que esté disponible para usted. |![trabaja en línea](media/check.png)|![Trabaja localmente](media/check.png)<sup>[*](#onprem)</sup>|[Vea...](across-working-with-powerbi.md).|
|Cree informes y paneles en Power BI que muestren datos de [!INCLUDE[prod_short](includes/prod_short.md)].|Utilice Power BI Desktop para crear sus propios informes y paneles. Puede publicar los informes en su propio servicio de Power BI o compartirlos con otros en su organización.|![Trabaja en línea](media/check.png)|![trabaja localmente](media/check.png)|[Vea...](across-how-use-financials-data-source-powerbi.md)
|Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publica tres aplicaciones para Power BI en Microsoft AppSource. Estas aplicaciones crean informes y paneles detallados en su servicio de Power BI para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Las aplicaciones disponibles incluyen: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Trabaja en línea](media/check.png)||[Vea...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Esta función requiere una aplicación registrada para Business Central en Microsoft Azure. Para más información, ver [Registro de Business Central en las instalaciones en Azure AD para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Preparándose para usar Power BI

Hay algunas tareas que deben realizarse antes de que pueda comenzar a usar Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]. Algunas de las tareas generalmente solo las realizan administradores o superusuarios.

1. Si estas usando [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones, asegúrese de que su implementación cumpla con los requisitos descritos en [Preparar[!INCLUDE[prod_short](includes/prod_short.md)] local para la integración de Power BI](admin-powerbi-setup.md#setup). Esta tarea normalmente es administrativa.

2. Publicar datos como servicios web.

    Las unidades de código, páginas y consultas que desea utilizar como fuente de datos en informes de Power BI deben publicarse como servicios web. Hay muchos servicios web publicados de forma predeterminada. Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)].

    Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

3. Obtener una cuenta de Power BI.

    Para hacer cualquier cosa con Power BI y [!INCLUDE[prod_short](includes/prod_short.md)], ya sea administrador o simplemente consumidor, necesitará una cuenta de servicio de Power BI. Para obtener una cuenta, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Para registrarse para una cuenta, use su dirección de correo electrónico y contraseña del trabajo. El registro requiere que tenga una licencia, pero en la mayoría de los casos ya debería tener una licencia gratuita. Para obtener más información, consulte [Licencias de Power BI](admin-powerbi-setup.md#license).

4. Si quiere crear sus propios informes de Power BI, obtenga Power BI Desktop.

    Puede descargar [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Para obtener más información, consulte [Obtener Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Power BI para consumidores](/power-bi/consumer/end-user-consumer)  
[El nuevo aspecto del servicio Power BI](/power-bi/service-new-look)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentación de Power BI](/power-bi/)  
[Inteligencia empresarial](bi.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]