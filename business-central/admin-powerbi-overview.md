---
title: Descripción general de la arquitectura y el componente de integración de Power BI para Business Central | Documentos de Microsoft
description: Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con las aplicaciones de Business Central para Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d02740b0f4c73b96be9268cfdf5e4c3de157d5d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924533"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a>Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prodshort](includes/prodshort.md)]

En este artículo, aprenderá sobre los diferentes aspectos de la integración de Power BI con [!INCLUDE[prodshort](includes/prodshort.md)] para ayudarle a comprender su implementación y uso.

## <a name="components"></a>Componentes

La siguiente tabla describe los componentes principales relacionados con la integración de Power BI.

|Componente|Descripción|
|---------|-----------|
|Power BI|Un servicio de administración y alojamiento de informes basado en la nube.|
|Power BI Desktop|Una herramienta de creación para crear informes y paneles, y le permite ejecutar informes. Está disponible como descarga gratuita en Microsoft Store y se instala localmente.|
|[!INCLUDE[prodshort](includes/prodshort.md)]|Solución en línea o local con conectores expuestos a Power BI y la capacidad de incrustar una parte de Power BI.|

## <a name="whats-available-from-the-start"></a>Que hay disponible desde el principio

La siguiente tabla describe las características disponibles.

|Característica|Soporte de [!INCLUDE[prodshort](includes/prodshort.md)] online o local|
|-------|---------------------|
|Conectores de Power BI|Ambos. Diferentes conectores para online y local. Mismo conector usado para Power BI Desktop y el servicio Power BI |
|Experiencia integrada para ver un informe determinado dentro de un FactBox en [!INCLUDE[prodshort](includes/prodshort.md)]|Ambos. Requiere configuración para mostrar informes de forma local.|
|Gestión de informes de Power BI desde [!INCLUDE[prodshort](includes/prodshort.md)]|Online|
|Los informes predeterminados de Power BI sobre centros de roles desplegados en Power BI|Online|
|Aplicaciones de Power BI en Microsoft AppSource|Online.|

## <a name="architecture"></a>Arquitectura

[!INCLUDE[prodshort](includes/prodshort.md)] se integra con Power BI a través de un conector que utiliza OData. La fuente de datos para los informes de Power BI se exponen como servicios web de OData.

![Arquitectura de Power BI para la integración con Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Flujo general

El siguiente diagrama ilustra el flujo de trabajo básico para los usuarios al conectar [!INCLUDE[prodshort](includes/prodshort.md)] a Power BI.

![Flujo de trabajo de Power BI para la integración con Business Central](./media/power-bi-flow.png)

1. El usuario se registra para una cuenta de Power BI.
2. El usuario se conecta a Power BI desde [!INCLUDE[prodshort](includes/prodshort.md)].
3. [!INCLUDE[prodshort](includes/prodshort.md)] verifica la licencia.
4. [!INCLUDE[prodshort](includes/prodshort.md)] despliega informes predeterminados en el servicio de Power BI. Este paso solo ocurre para [!INCLUDE[prodshort](includes/prodshort.md)] online.
5. [!INCLUDE[prodshort](includes/prodshort.md)] hace que los informes en Power BI estén disponibles para la selección en [!INCLUDE[prodshort](includes/prodshort.md)]. Los informes predeterminados se muestran automáticamente en partes de Power BI.
6. El usuario crea un informe en Power BI Desktop.
7. El usuario publica el informe en el servicio Power BI. Los informes están disponibles para su selección en [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Power BI para consumidores](/power-bi/consumer/end-user-consumer)  
[El nuevo aspecto del servicio Power BI](/power-bi/service-new-look)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentación de Power BI](/power-bi/)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
