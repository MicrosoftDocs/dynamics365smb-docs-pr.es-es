---
title: Descripción general de la arquitectura y el componente de integración de Power BI para Business Central | Documentos de Microsoft
description: Conozca los diferentes aspectos de la integración de Power BI con Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="power-bi-integration-component-and-architecture-overview-for-"></a><a name="power-bi-integration-component-and-architecture-overview-for-"></a>Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]

En este artículo, aprenderá sobre los diferentes aspectos de la integración de Power BI con [!INCLUDE[prod_short](includes/prod_short.md)] para ayudarle a comprender su implementación y uso.

## <a name="components"></a><a name="components"></a>Componentes

La siguiente tabla describe los componentes principales relacionados con la integración de Power BI.

|Componente|Descripción|
|---------|-----------|
|Power BI|Un servicio de administración y alojamiento de informes basado en la nube.|
|Power BI Desktop|Una herramienta de creación para crear informes y paneles, y le permite ejecutar informes. Está disponible como descarga gratuita en Microsoft Store y se instala localmente.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Solución en línea o local con conectores expuestos a Power BI y la capacidad de incrustar una parte de Power BI.|

## <a name="whats-available-from-the-start"></a><a name="whats-available-from-the-start"></a>Que hay disponible desde el principio

La siguiente tabla describe las características disponibles.

|Característica|Soporte de [!INCLUDE[prod_short](includes/prod_short.md)] online o local|
|-------|---------------------|
|Conectores de Power BI|Ambos. Diferentes conectores para online y local. Mismo conector usado para Power BI Desktop y el servicio Power BI |
|Experiencia integrada para ver un informe determinado dentro de un FactBox en [!INCLUDE[prod_short](includes/prod_short.md)]|Ambos. Requiere configuración para mostrar informes de forma local.|
|Gestión de informes de Power BI desde [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Los informes predeterminados de Power BI sobre centros de roles desplegados en Power BI|Online|
|Aplicaciones de Power BI en Microsoft AppSource|Online|

## <a name="architecture"></a><a name="architecture"></a>Arquitectura

[!INCLUDE[prod_short](includes/prod_short.md)] se integra con Power BI a través de un conector que utiliza OData. La fuente de datos para los informes de Power BI se exponen como páginas API y servicios web de OData.

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Texto alternativo de la imagen." lightbox="./media/power-bi-architecture.png":::

A partir de febrero de 2022, los informes de Power BI para [!INCLUDE[prod_short](includes/prod_short.md)] en línea provienen de una réplica secundaria de la base de datos de solo lectura. La réplica de la base de datos es parte de la capacidad de [escalado de lectura](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) de [!INCLUDE[prod_short](includes/prod_short.md)] en línea. Esta configuración libera la base de datos principal para transacciones, lo que mejora el rendimiento del sistema. La conexión a la réplica de la base de datos de solo lectura es una parte integral del conector Business Central Online y no requiere ninguna configuración adicional de su parte. Todos los informes nuevos se conectarán a la réplica de la base de datos de solo lectura de forma predeterminada. Los informes antiguos seguirán utilizando la base de datos principal. Para más información, consulte [Plan del segundo lanzamiento de versiones de Business Central 2021](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow"></a><a name="general-flow"></a>Flujo general

El siguiente diagrama ilustra el flujo de trabajo básico para los usuarios al conectar [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI.

![Flujo de trabajo de Power BI para la integración con Business Central.](./media/power-bi-flow.png)

1. El usuario se registra para una cuenta de Power BI.
2. El usuario se conecta a Power BI desde [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] verifica la licencia.
4. [!INCLUDE[prod_short](includes/prod_short.md)] despliega informes predeterminados en el servicio de Power BI. Este paso solo ocurre para [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] hace que los informes en Power BI estén disponibles para la selección en [!INCLUDE[prod_short](includes/prod_short.md)]. Los informes predeterminados se muestran automáticamente en partes de Power BI.
6. El usuario crea un informe en Power BI Desktop.
7. El usuario publica el informe en el servicio Power BI. Los informes están disponibles para su selección en [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
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
