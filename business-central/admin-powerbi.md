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
ms.openlocfilehash: 3c8ad52667ad8ff0a2cb399ac6354012d7ef9275
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437917"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] y Power BI

Obtener información sobre los datos de [!INCLUDE[prod_short](includes/prod_short.md)] es fácil con [Power BI](https://powerbi.microsoft.com), un sistema de visualización de datos de Microsoft. Power BI recupera datos de [!INCLUDE[prod_short](includes/prod_short.md)] que le permiten crear paneles e informes basados en esos datos. Power BI proporciona una alternativa flexible a los informes integrados en [!INCLUDE[prod_short](includes/prod_short.md)], lo que le permite desglosar y personalizar la visualización, e incluso fusionar datos de diferentes empresas en [!INCLUDE[prod_short](includes/prod_short.md)]. Algunos informes de Power BI también pueden integrarse en Business Central y visualizarse sin salir del sistema. Los paneles de control más complejos se experimentan mejor desde el sitio web de Power BI.

![Power BI y Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>¿Qué puede hacer con Power BI y [!INCLUDE[prod_short](includes/prod_short.md)]?

Hay varias funciones para trabajar con [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. Algunas cosas se pueden hacer desde Power BI, mientras que otras cosas se hacen desde [!INCLUDE[prod_short](includes/prod_short.md)]. Además, algunas funciones solo están disponibles con [!INCLUDE[prod_short](includes/prod_short.md)] online, no local. La siguiente tabla le ofrece una descripción general.

|Característica|Descripción|Online|Local|Más información|
|-------|-----------|--------------|-----------|----------------|
|Ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI|Puede ver sus datos desde [!INCLUDE[prod_short](includes/prod_short.md)] en informes en Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online incluye algunos informes de Power BI predefinidos. O su organización puede haber puesto a su disposición algunos informes personalizados.|![Trabaja en línea.](media/check.png)|![Trabaja localmente](media/check.png)|[Vea...](across-working-with-business-central-in-powerbi.md)|
|Ver informes de Power BI en el cliente de [!INCLUDE[prod_short](includes/prod_short.md)].| Los informes de Power BI que muestran datos de [!INCLUDE[prod_short](includes/prod_short.md)] se pueden incrustar directamente en las páginas de partes de [!INCLUDE[prod_short](includes/prod_short.md)]. Puede cambiar la parte para mostrar cualquier informe que esté disponible para usted. |![trabaja en línea.](media/check.png)|![Trabaja localmente](media/check.png)<sup>[*](#onprem)</sup>|[Vea...](across-working-with-powerbi.md).|
|Cree informes y paneles en Power BI que muestren datos de [!INCLUDE[prod_short](includes/prod_short.md)].|Utilice Power BI Desktop para crear sus propios informes y paneles. Puede publicar los informes en su propio servicio de Power BI o compartirlos con otros en su organización.|![Trabaja en línea.](media/check.png)|![trabaja localmente](media/check.png)|[Vea...](across-how-use-financials-data-source-powerbi.md)
|Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publica tres aplicaciones para Power BI en Microsoft AppSource. Estas aplicaciones crean informes y paneles detallados en su servicio de Power BI para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Las aplicaciones disponibles incluyen: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Trabaja en línea.](media/check.png)||[Vea...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Esta función requiere una aplicación registrada para Business Central en Microsoft Azure. Para más información, ver [Registro de Business Central en las instalaciones en Azure AD para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Preparándose para usar Power BI

Hay algunas tareas que deben realizarse antes de que pueda comenzar a usar Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Las tareas dependerán de su rol en su organización y de lo que quiera hacer con Power BI:

- Como *usuario comercial* usted quiere ver informes de Power BI, ya sea en el Servicio de Power BI o en Business Central
- Como *administrador*, usted es responsable de la administración de la configuración de toda la organización que controla cómo funcionan Business Central y Power BI.
- Como *creador del informe*, usted quiere crear informes de Power BI personalizados que puede compartir con otros usuarios.

|Tarea|Usuario empresarial|Administrador|Creador de informe|Más información|
|----|-------------|-------------|-----------------------|----------------|
|Obtener una cuenta de Power BI.|![otra marca de verificación más.](media/check.png)|![es una marca de verificación](media/check.png)|![otra nueva marca de verificación](media/check.png)|Vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Para registrarse para una cuenta, use su dirección de correo electrónico y contraseña del trabajo. <br /><br/>El registro requiere que tenga una licencia, pero en la mayoría de los casos ya debería tener una licencia gratuita. Para más información, vea [Licencias de Power BI](admin-powerbi-setup.md#license).|
|Obtenga Power BI Desktop|||![otra nueva marca de verificación.](media/check.png)|Para descargar, vaya a [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Para obtener más información, consulte [Obtener Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Exponer datos de Business Central a Power BI||![es una marca de verificación.](media/check.png)|![otra nueva marca de verificación](media/check.png)|[Exponer datos a través de páginas API o servicios web OData](admin-powerbi-setup.md#exposedata)
|Habilitar la integración de Power BI<br />(solo local)||![es una marca de verificación.](media/check.png)||[Configuración Business Central local para la integración de Power BI](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

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