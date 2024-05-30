---
title: Introducción a Business Central y Power BI
description: Obtener una introducción al uso de Power BI para conseguir información y KPI desde los datos de Business Central.
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-business-central-and-power-bi"></a>Introducción a Business Central y Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Es fácil obtener información sobre los datos de [!INCLUDE[prod_short](includes/prod_short.md)] con [Power BI](https://powerbi.microsoft.com), un sistema de visualización de datos de Microsoft. Power BI recupera datos de [!INCLUDE[prod_short](includes/prod_short.md)] para que pueda crear paneles e informes basados en esos datos. Power BI proporciona una alternativa flexible a los informes integrados en [!INCLUDE[prod_short](includes/prod_short.md)], lo que le permite desglosar y personalizar la visualización, e incluso fusionar datos de diferentes empresas en [!INCLUDE[prod_short](includes/prod_short.md)]. Algunos informes de Power BI también pueden integrarse en Business Central y visualizarse sin salir del sistema. Los paneles de control más complejos se experimentan mejor desde el sitio web de Power BI.

![Power BI y Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-business-central"></a>Qué puede hacer con Power BI y Business Central

Hay varias funciones para trabajar con [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. Algunas cosas se pueden hacer desde Power BI, mientras que otras cosas se hacen desde [!INCLUDE[prod_short](includes/prod_short.md)]. Además, algunas funciones solo están disponibles con [!INCLUDE[prod_short](includes/prod_short.md)] online, no local. La siguiente tabla le ofrece una descripción general.

|Característica|Descripción|Online|Local|Más información|
|-------|-----------|--------------|-----------|----------------|
|Ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI|Puede ver sus datos desde [!INCLUDE[prod_short](includes/prod_short.md)] en informes en Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online incluye algunos informes de Power BI predefinidos. O su organización puede tener algunos informes personalizados.|![Trabaja en línea.](media/check.png)|![Trabaja localmente](media/check.png)|[Aquí...](across-working-with-powerbi.md)|
|Ver informes de Power BI en el cliente de [!INCLUDE[prod_short](includes/prod_short.md)].| Los informes de Power BI que muestran datos de [!INCLUDE[prod_short](includes/prod_short.md)] se pueden incrustar directamente en las páginas de partes de [!INCLUDE[prod_short](includes/prod_short.md)]. Puede cambiar la parte para mostrar cualquier informe que esté disponible para usted. |![trabaja en línea.](media/check.png)|![Trabaja localmente](media/check.png)<sup>[*](#onprem)</sup>|[Aquí...](across-working-with-powerbi.md).|
|Cree informes y paneles en Power BI que muestren datos de [!INCLUDE[prod_short](includes/prod_short.md)].|Utilice Power BI Desktop para crear sus propios informes y paneles. Puede publicar los informes en su propio servicio de Power BI o compartirlos con otros en su organización.|![Trabaja en línea.](media/check.png)|![trabaja localmente](media/check.png)|[Aquí...](across-how-use-financials-data-source-powerbi.md)|
|Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publica tres aplicaciones para Power BI en Microsoft AppSource. Estas aplicaciones crean informes y paneles detallados en su servicio de Power BI para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Las aplicaciones disponibles incluyen: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Trabaja en línea.](media/check.png)||[Aquí...](across-powerbi-business-central-apps.md)|
|Trabajar con datos de [!INCLUDE [prod_short](includes/prod_short.md)] en datamarts y flujos de datos|A partir de julio de 2022, puede utilizar el conector [!INCLUDE [prod_short](includes/prod_short.md)] en Power Query Online con flujos de datos que comparte en diferentes informes y paneles.|![trabaja en línea.](media/check.png)||[Aquí...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Esta función requiere una aplicación registrada para Business Central en Microsoft Azure. Para más información, ver [Registro de Business Central local en Microsoft Entra ID para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="get-ready-to-use-power-bi"></a>Prepararse para usar Power BI

Hay algunas tareas que deben realizarse antes de que pueda comenzar a usar Power BI con [!INCLUDE[prod_short](includes/prod_short.md)].<!-- Some of the tasks are typically only done by administrators or super users.--> Las tareas dependen de su rol en su organización y de lo que quiera hacer con Power BI:

- Como *usuario comercial* usted quiere ver informes de Power BI, ya sea en el Servicio de Power BI o en Business Central
- Como *administrador*, usted es responsable de la administración de la configuración de toda la organización que controla cómo funcionan Business Central y Power BI.
- Como *creador del informe*, usted quiere crear informes de Power BI personalizados que puede compartir con otros usuarios.

|Tarea|Usuario empresarial|Administrador|Creador de informe|Más información|
|----|-------------|-------------|-----------------------|----------------|
|Obtener una cuenta de Power BI.|![otra marca de verificación más.](media/check.png)|![es una marca de verificación](media/check.png)|![otra nueva marca de verificación](media/check.png)|Vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Para registrarse para una cuenta, use su dirección de correo electrónico y contraseña del trabajo. <br /><br/>El registro requiere que tenga una licencia, pero en la mayoría de los casos ya debería tener una licencia gratuita. Para más información, vea [Licencias de Power BI](admin-powerbi-setup.md#license).|
|Obtenga Power BI Desktop|||![otra nueva marca de verificación.](media/check.png)|Para descargar, vaya a [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Para obtener más información, consulte [Obtener Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Exponer datos de Business Central a Power BI||![es una marca de verificación.](media/check.png)|![otra nueva marca de verificación](media/check.png)|[Exponer datos a través de páginas API o servicios web OData](admin-powerbi-setup.md#exposedata)
|Habilitar la integración de Power BI<br />(solo local)||![es una marca de verificación.](media/check.png)||[Configuración Business Central local para la integración de Power BI](across-working-with-business-central-in-powerbi.md#setup)|


## <a name="next-steps"></a>Pasos siguientes

- Si usted es un administrador que necesita configurar Power BI en [!INCLUDE[prod_short](includes/prod_short.md)], vaya a [Habilitar integración de Power BI](admin-powerbi-setup.md).
- Si Power BI ya está configurado y desea probar las funciones, vaya a [Trabajar con informes de Power BI en Business Central](across-working-with-powerbi.md).

## <a name="see-also"></a>Consulte también

[Información general sobre el análisis](reports-bi-reporting.md)   
[Realizar un seguimiento de KPI con métricas de Power BI](track-kpis-with-power-bi-metrics.md)   
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  
[Documentación de Power BI](/power-bi/)  
[¿Qué es Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introducción a los datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introducción a los flujos de datos y preparación de datos de autoservicio](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
