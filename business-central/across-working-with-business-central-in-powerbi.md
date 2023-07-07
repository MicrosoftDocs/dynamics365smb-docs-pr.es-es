---
title: Trabajar con datos de Business Central en Power BI | Documentos de Microsoft
description: 'Obtener información, inteligencia empresarial y KPI de los datos de Business Central utilizando Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2022
ms.author: jswymer
---
# <a name="work-with--data-in-power-bi"></a>Trabajar con datos de [!INCLUDE [prod_short](includes/prod_short.md)] en Power BI

En este artículo, aprenderá algunos de los conceptos básicos sobre cómo trabajar con informes y paneles en Power BI que usan [!INCLUDE [prod_short](includes/prod_short.md)] como fuente de datos. El artículo analiza algunos aspectos que lo ayudarán a comenzar como usuario de [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener pautas generales e instrucciones sobre el uso de Power BI, ver [Documentación de Power BI para consumidores](/power-bi/consumer).

## <a name="get-ready"></a>Prepararse

Regístrese para el servicio de Power BI. Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use una dirección de correo electrónico y contraseña del trabajo.

## <a name="get-started"></a>Introducción

Una vez que tenga una cuenta de Power BI, puede iniciar sesión en [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

El servicio de Power BI aloja todos los informes disponibles. Para ver el informe, seleccione **Mi espacio de trabajo** > **Informes**. Luego, seleccione el informe que desea ver.

Con [!INCLUDE[prod_short](includes/prod_short.md)] Online, automáticamente tendrá un conjunto de informes predeterminados en su espacio de trabajo. Si desea crear sus propios informes, puede utilizar Power BI Desktop para crear informes y luego publicarlos en su espacio de trabajo. Para más información, ver [Introducción a la creación de informes en Power BI Desktop para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] local, tendrá que empezar desde cero utilizando Power BI Desktop. Opcionalmente los informes de Power BI se pueden distribuir como archivos que puede cargar.

## <a name="get-the-latest-data"></a>Obtener los datos más recientes

Cada informa de Power BI se basa en un conjunto de datos que obtiene datos de los orígenes de [!INCLUDE[prod_short](includes/prod_short.md)]. Quiere asegurarse de que los datos de sus informes de  Power BI están actualizados con los datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Este concepto se conoce como *actualización*.  Dependiendo de cómo haya configurado su organización Power BI, es posible que la actualización no se realice automáticamente. Hay dos formas de actualizar los datos: manualmente o programando una actualización. La actualización manual se realiza a pedido, según sea necesario. La actualización programada le permite actualizar automáticamente a intervalos de tiempo definidos.

### <a name="refresh-manually"></a>Actualizar manualmente

En el panel de navegación, debajo **Conjuntos de datos**, seleccione **Mas opciones (...)** junto al conjunto de datos, luego seleccione **Refrescar ahora**.

### <a name="schedule-a-refresh"></a>Programe una actualización

En el panel de navegación, debajo de Conjuntos de datos, seleccione Mas opciones (...) junto al conjunto de datos, luego seleccione **Programar actualización**. Complete la información debajo de la sección **Programar actualización** y seleccione **Aplicar**.

Para obtener más información, vea [Configurar actualización programada](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="upload-reports-from-files"></a><a name="upload"></a>Cargar informes desde archivos

Los informes de Power BI se pueden distribuir entre los usuarios como archivos .pbix. Si tiene un archivo .pbix, puede cargarlo en un espacio de trabajo. Para cargar un informe, siga los siguientes pasos:

1. En su nuevo espacio de trabajo, seleccione **Obtener datos**.

2. En el cuadro Archivos, seleccione **Obtener**.

3. Seleccione **Archivo local**, navegue hasta donde guardó el archivo y seleccione **Abierto**.

Para más información, ver [Sube el informe al servicio](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Cargar un informe requiere que tenga un espacio de trabajo con [capacidad Premium](/power-bi/service-premium-what-is). Para obtener más información, vea [Gestión de capacidades Premium](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] online, también puede cargar un informe desde [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, ver [Trabajar con informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)] - Subir informes](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Compartir informes con otros

Una vez que un informe está en su espacio de trabajo, puede compartirlo con otras personas de su organización.

Para compartir un informe, en una lista de informes o en un informe abierto, seleccione **Compartir**. En el panel **Compartir informe**, ingrese las direcciones de correo electrónico completas de las personas o grupos de distribución con los que desea compartir. Siga las instrucciones en pantalla para completar el intercambio. Para más información, ver [Compartir un panel o informe.](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Debe tener una [Licencia Pro de Power BI](/power-bi/service-features-license-type) y las personas con las que compartes también lo harán. El contenido debe estar en un espacio de trabajo con [capacidad Premium](/power-bi/service-premium-what-is). Para más información, vea [Formas de compartir el trabajo en Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Trabajar con informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-powerbi.md)  
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
