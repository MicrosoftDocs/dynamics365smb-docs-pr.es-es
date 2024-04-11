---
title: 'Descripción general de análisis, inteligencia empresarial e informes'
description: 'Proporciona una descripción general de todas las características de inteligencia empresarial, análisis e informes con soporte de Business Central.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# <a name="analytics-business-intelligence-and-reporting-overview"></a>Descripción general de análisis, inteligencia empresarial e informes

Las pequeñas y medianas empresas se basan en capacidades de análisis e informes integrados que pueden usar de inmediato como ayuda para realizar un seguimiento de su negocio. [!INCLUDE[prod_short](includes/prod_short.md)] proporciona informes y herramientas de análisis que cubren procesos comerciales básicos y complejos para dichas organizaciones. También puede realizar análisis ad-hoc directamente desde su página principal.  

## <a name="analytics-needs-in-organizations"></a>Necesidades de análisis en organizaciones

Al pensar en las necesidades de análisis en organizaciones, podría resultar útil utilizar un modelo mental basado en personas descritas en un alto nivel y sus diferentes necesidades de análisis.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

El modelo se basa en el hecho de que diferentes roles en una organización tienen diferentes necesidades en lo que respecta a los datos. Cuanto más alto esté ubicado un rol en el organigrama, más datos agregados necesitará alguien en el rol para hacer su trabajo.

Los roles a menudo prefieren formas de consumir y analizar datos, formas que reflejan el nivel de agregación de datos que necesitan.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Utilice las siguientes secciones para obtener más información sobre las formas de consumir datos de [!INCLUDE[prod_short](includes/prod_short.md)]:

- Informes financieros
- KPI y paneles de control
- Análisis ad hoc
- Informes

## <a name="using-financial-reports-to-produce-financial-statements-and-kpis"></a>Uso de informes financieros para crear extractos financieros y KPI

La función de informes financieros le permite obtener información sobre los datos financieros almacenados en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Captura de pantalla de un informe financiero." lightbox="media/acc_schedule_13_columns.jpg":::

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que puede agregar a un movimiento como parámetro. las dimensiones, la permiten agrupar movimientos que tienen características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Para obtener más información sobre los estados financieros y los KPI, vaya a [Uso de informes financieros para producir estados financieros y KPI](bi.md).

## <a name="using-key-performance-indicators-to-meet-your-business-goals"></a>Utilización de indicadores clave de rendimiento (KPI) para alcanzar sus objetivos empresariales

Un indicador clave de rendimiento (KPI) es un valor medible que muestra la eficacia con la que está cumpliendo sus objetivos. Piense en los KPI como el cuadro de mandos de su empresa, una forma de medir si está cumpliendo o no sus objetivos.

La identificación y el seguimiento de los KPI le permiten saber si su empresa va por el camino correcto o si debe cambiar de rumbo. Cuando se utilizan correctamente, los KPI son herramientas poderosas que le ayudan a:

- Supervisar la salud financiera de la empresa.
- Medir el progreso en comparación con los objetivos estratégicos.
- Detecte los problemas desde el principio.
- Haga ajustes oportunos a las tácticas.
- Motivar a los miembros del equipo.
- Tomar decisiones mejores más rápido.

Para obtener más información sobre KPI, consulte [Utilización de indicadores clave de rendimiento para alcanzar sus objetivos empresariales](./analytics-about-kpis.md)

## <a name="ad-hoc-data-analysis"></a>Análisis de datos ad hoc

A veces, es posible que simplemente quiera comprobar si los números cuadran correctamente, confirmar o desacreditar rápidamente una hipótesis sobre el negocio o tal vez buscar anomalías en tus datos financieros. Para los análisis ad hoc, es posible que no tenga un informe integrado que ayude a responder sus preguntas. Para análisis ad hoc, utilice estas dos funciones:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La función de análisis de datos le permite abrir casi una página de lista, como movimientos de contabilidad o entradas de diario de cliente, entrar en el modo de análisis y luego agrupar, filtrar y pivotar los datos como mejor le parezca. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página de movimientos de contabilidad" lightbox="media/data-analysis-gl-entries.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista, opcionalmente filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en los datos de movimientos de contabilidad usando Excel" lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador con Excel para la web.

Para obtener más información sobre los análisis de anuncios, vaya a [Análisis de datos ad-hoc](reports-adhoc-analysis.md).

## <a name="reports"></a>Informes

Un informe de [!INCLUDE[prod_short](includes/prod_short.md)] recopila información en función de un conjunto específico de criterios. Los informes organizan y presentan la información en un formato de fácil lectura que puede usar en Excel, imprimir o guardar como un archivo.  

Como ejemplo de un informe interactivo en Excel, el informe ***Cuentas por cobrar vencidas** le permite analizar lo que sus clientes le deben y cuándo vencen los pagos.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Ejemplo del informe interactivo de cuentas por cobrar antiguas en Excel." lightbox="media/aged-accounts-receivables-excel.png":::

Para cuentas por cobrar antiguas, [!INCLUDE[prod_short](includes/prod_short.md)] también incluye un informe diseñado para imprimir. La posibilidad de imprimir es útil si prefiere tener los datos en un archivo .pdf.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Ejemplo del informe de cuentas por cobrar antiguas en pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] viene con más de 300 informes integrados que puede utilizar para respaldar sus procesos comerciales con información basada en datos. Para obtener una descripción general rápida de todos los informes que están disponibles para su función, puede abrir el explorador de informes desde el centro de funciones y todas las páginas de lista y desde **Cuéntame**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Ejemplo de cómo el explorador de informes muestra todos los informes de un rol." lightbox="media/report-explorer-finance.png":::

Para obtener más información sobre cómo usar el explorador de informes para ver todos los informes integrados, vaya a [Explorar informes por función](ui-role-explorer.md).

La siguiente tabla enumera artículos sobre cómo utilizar los informes integrados en [!INCLUDE[prod_short](includes/prod_short.md)].

| Para  | Vea |
| --- | --- |
| Aprenda a usar informes (marcar, ejecutar, imprimir, programar y cambiar el diseño). | [Usar informes en el trabajo diario](reports-use-reports.md) |
| Obtenga más información sobre los informes integrados disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]. |[Descripción general de los informes](reports-available-reports.md)| 
| Utilice el Explorador de informes para ver todos los informes integrados. | [Exploración de informes por rol](ui-role-explorer.md) |

## <a name="external-business-intelligence-and-reporting-tools"></a>Inteligencia empresarial externa y herramientas de informes

Si prefiere utilizar herramientas de inteligencia empresarial que no están integradas en [!INCLUDE[prod_short](includes/prod_short.md)], la siguiente tabla proporciona enlaces a orientación sobre herramientas y formas de utilizar herramientas externas.

| Para  | Vea |
| --- | --- |
| Usar Power BI con datos de Business Central | [Usar Power BI con Business Central](admin-powerbi.md) |
| Integre herramientas de inteligencia de negocios externas con [!INCLUDE[prod_short](includes/prod_short.md)].| [Herramientas de inteligencia empresarial externas](reports-external-analysis.md) |
| Extraer datos a almacenes de datos o lagos de datos| [Cómo extraer datos a almacenes de datos o lagos de datos](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Analizar datos de Business Central con Microsoft Fabric| [Introducción a Microsoft Fabric y Business Central](admin-fabric.md) |
| Lea datos desde Business Central usando API | [API Business Central v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## <a name="see-also"></a>Consulte también

[Uso de informes financieros para crear extractos financieros y KPI](bi.md)  
[Utilización de indicadores clave de rendimiento (KPI) para alcanzar sus objetivos empresariales](analytics-about-kpis.md)  
[Realizar análisis de datos ad hoc](reports-adhoc-analysis.md)  
[Use informes en su trabajo diario](reports-use-reports.md)  
[Descripción general de los informes integrados](reports-available-reports.md)  
[Exploración de informes por rol](ui-role-explorer.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
