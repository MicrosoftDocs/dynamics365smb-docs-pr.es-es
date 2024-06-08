---
title: Análisis financiero
description: 'Business Central le ayuda a recopilar, analizar y compartir la información de su empresa para inteligencia empresarial.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="financial-analytics"></a>Análisis financiero

Las empresas capturan una enorme cantidad de datos durante las actividades diarias que respaldan la valiosa inteligencia empresarial (BI) para los tomadores de decisiones:

- Cifras de ventas
- Compras
- Gastos de explotación
- Salarios de los empleados
- Presupuestos

[!INCLUDE[prod_short](includes/prod_short.md)] contiene muchas características para ayudarle a recopilar, analizar y compartir la información financiera de su organización:

- Informes financieros (para estados financieros y KPI)
- Análisis ad hoc en listas
- Análisis ad-hoc de datos en Excel (usando Abrir en Excel)
- Informes financieros integrados

Cada una de estas características tiene sus propias ventajas y desventajas, según el tipo de análisis de datos y el rol del usuario. Para obtener más información, vaya a [Información general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md).

Este artículo presenta cómo puede utilizar estas características analíticas para proporcionar información financiera.

## <a name="analytics-needs-in-finance"></a>Necesidades de análisis en finanzas

Al pensar en las necesidades de análisis en finanzas, podría resultar útil utilizar un modelo mental basado en personas descritas en un alto nivel y sus diferentes necesidades de análisis.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Las personas que desempeñan diferentes roles tienen diferentes necesidades en lo que respecta a los datos y los utilizan de diferentes maneras. Por ejemplo, las personas en finanzas interactúan con los datos de manera diferente que las personas en ventas.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Agregación de datos  | Formas típicas de consumir datos                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|DIRGEN / DIRFIN          | Datos de rendimiento  | KPI <br> Paneles <br> Informes financieros           |
|Admin. financiera | Tendencias, resúmenes | Informes de gestión integrados <br> Análisis ad hoc      | 
|Contable         | Datos detallados     | Informes operativos integrados <br> Datos de tareas en pantalla |

## <a name="finance-kpis"></a>KPI financieros

Un indicador clave de rendimiento (KPI) es un valor medible que muestra la eficacia con la que está cumpliendo sus objetivos. En finanzas, las personas suelen utilizar los siguientes KPI para monitorear la salud financiera de su organización:

- Marg. benef. bruto
- Margen de beneficio neto
- Capital circulante
- Relación actual/rápida
- Apalancamiento financiero, también conocido como multiplicador del capital propio
- Ratio deuda-capital propio
- Facturación de activos totales
- Rendimiento del capital propio
- Rendimiento de los activos

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## <a name="using-financial-reporting-to-produce-financial-statements-and-kpis"></a>Uso de informes financieros para crear extractos financieros y KPI

La característica **Informes financieros** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos e informes en la página de inicio, como el gráfico de flujo de efectivo y los informes Balance de ingresos y Balance.

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que puede agregar a un movimiento como parámetro. Las dimensiones le permiten agrupar entradas que tienen características similares para que sean más fáciles de analizar. Por ejemplo, clientes, regiones, productos y vendedores. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

> [!TIP]
> Como una forma rápida de analizar datos transaccionales, puede filtrar por dimensiones los totales del plan de cuentas y todos los movimientos en las páginas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.  

En la tabla siguiente se indican una serie de tareas en informes financieros con vínculos a los artículos que las describen.  

| Para | Vea |
| --- | --- |
| Crear nuevos informes financieros para definir los balances financieros para elaborar informes o para mostrar como gráficos.| [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)|
| Utilice cuentas estadísticas para complementar la información de los informes financieros. Las cuentas estadísticas le permiten agregar métricas que se basan en datos no transaccionales. Puede agregar los datos no transaccionales como unidades basadas en números, tales como el número de empleados, los pies cuadrados o el número de clientes con cuentas vencidas. | [Analizar datos con cuentas estadísticas](bi-use-statistical-accounts.md) |
| Aprenda cómo configurar un nuevo informe financiero a través de ejemplos. | [Tutorial: Usar informes financieros para elaborar previsiones del flujo de efectivo](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analice el rendimiento financiero configurando indicadores clave de rendimiento (KPI) basados en informes financieros, que después publica como servicios web. Los KPI de informes financieros publicados se pueden ver en un sitio Web o importar a Microsoft Excel usando los servicios Web de OData. |[Configurar y publicar un servicio web KPI que se basa en informes financieros](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Configurar vistas para analizar datos usando dimensiones.|[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)|
| Crear nuevos informes de análisis para ventas, compras y existencias, así como configurar plantillas de análisis. |[Crear informes de análisis](bi-how-create-analysis-views-reports.md)|

## <a name="finance-reporting-across-business-units-or-legal-entities"></a>Informes financieros entre unidades de negocio o entidades jurídicas

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones matrices. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada.  

Para obtener más información, vaya a [Consolidación de empresa](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-finance-data"></a>Análisis ad-hoc de datos financieros

A veces, solo es necesario comprobar si los números cuadran correctamente o confirmar rápidamente una cifra. Las siguientes características son excelentes para análisis ad hoc:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La función de análisis de datos le permite abrir casi una página de lista, como movimientos de contabilidad, movimientos de activos fijos, movimientos de cheques o movimientos de cuentas bancarias, entrar en el modo de análisis y luego agrupar, filtrar y pivotar los datos como mejor le parezca.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página de movimientos de contabilidad" lightbox="media/data-analysis-gl-entries.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista para movimientos, opcionalmente filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en los datos de movimientos de contabilidad usando Excel" lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador con Excel para la web. 


Para obtener más información sobre cómo realizar análisis ad hoc en libros de contabilidad, consulte [Análisis ad hoc de datos financieros](ad-hoc-analysis-finance.md). 

## <a name="built-in-reports-for-finance"></a>Informes financieros integrados

[!INCLUDE [prod_short](includes/prod_short.md)] incluye diversos informes integrados, funciones de seguimiento y herramientas para ayudar a los auditores o controladores que son responsables de informar al departamento de finanzas.

Para obtener una descripción general de los informes disponibles, puede elegir **Todos los informes** en el panel superior de su página de inicio. Esta acción abre el explorador de roles, que se filtra según las funciones en la opción **Informe y análisis**. Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Ejemplo de informes sobre el centro de roles financieros" lightbox="media/report-explorer-finance.png":::

Los informes integrados vienen en dos versiones:

- Diseñado para imprimir (pdf).
- Diseñado para análisis en Excel.

Para obtener más información, consulte estos resúmenes de informes relevantes para las finanzas.

- [Informes financieros de Excel integrados](finance-analyze-excel.md)
- [Informes financieros clave integrados](finance-reports.md)
- [Informes de activos fijos integrados](fa-reports.md)
- [Informes de cobros integrados](receivables-reports.md)
- [Informes de pagos integrados](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## <a name="on-screen-finance-task-pages"></a>Páginas de tareas financieras en pantalla

[!INCLUDE [prod_short](includes/prod_short.md)] tiene varias páginas que le brindan resúmenes financieros y tareas por realizar.

### <a name="show-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Mostrar movimientos de contabilidad general y saldos del libro mayor desde la página Plan de cuentas

La página Plan de cuentas muestra todas las cuentas de contabilidad general con números agregados registrados en la contabilidad general. Desde esta página, puede hacer cosas como:  

- Ver informes que muestran movimientos de contabilidad y saldos.  
- Revisar una lista de grupos contables para dicha cuenta.
- Para ver los saldos del Debe y el Haber de una sola cuenta.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Ejemplo de cómo la página del Plan de cuentas muestra información financiera" lightbox="media/chart-of-accounts-page.png":::

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts).

### <a name="view-actual-amounts-compared-to-budgeted-amounts-for-all-accounts-and-for-several-periods"></a>Ver importes reales comparados con importes presupuestados para todas las cuentas y durante varios periodos

Como parte de la recopilación, el análisis y el uso compartido de los datos de la empresa, puede querer ver importes reales comparados con los importes presupuestados para todas las cuentas y durante varios periodos. Puede realizar la comparación desde la página **Plan de cuentas**, seleccionando la acción **Saldo/Ppto. cuenta**.

Para obtener más información, vaya a [Analizar importes reales frente a importes presupuestados](bi-how-analyze-actual-versus-budget.md).

### <a name="analyze-data-by-dimensions"></a>Analizar datos por dimensiones

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Así pues, en lugar de configurar cuentas de libro mayor separadas para cada departamento y proyecto, puede utilizar las dimensiones como base para el análisis y evitar tener que crear una estructura de plan de cuentas complicada.

En análisis financiero, una dimensión son datos que agrega a un movimiento de contabilidad general como una especie de marcador. Estos datos se utilizan para agrupar movimientos de contabilidad general de características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Puede usar dimensiones en movimientos de diarios, documentos y presupuestos. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)

### <a name="analyzing-cash-flow"></a>Análisis el flujo de efectivo

En la página de inicio Contable, en **Rendimiento finanzas**, los gráficos Ciclo de efectivo, Flujo de efectivo e Ingresos y gastos proporcionan formas de analizar el flujo de efectivo:

- Revise las cifras de un periodo mediante el control deslizante de la escala de tiempo.
- Filtre el gráfico seleccionando el origen en la leyenda.
- Cambiar la duración del periodo, o vaya al periodo anterior o próximo, eligiendo opciones en menú desplegable Rendimiento finanzas.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Ejemplo de cómo se ven las imágenes del flujo de efectivo en el centro de funciones del contable" lightbox="media/cashflow-accountant-rolecentre.png":::

Para examinar la previsión, además de los movimientos de previsión, también puede ver la hoja de flujo de efectivo. Por ejemplo, puede ver cómo la previsión:

- Controla las ventas y las compras confirmadas.
- Resta los pagos y suma los cobros.
- Omite los pedidos de venta y de compra duplicados.

Para obtener más información, vaya a [Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md).

## <a name="see-also"></a>Consulte también

[Manejar informes financieros entre unidades de negocio o entidades jurídicas](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Análisis ad-hoc de datos financieros](ad-hoc-analysis-finance.md)   
[Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts)  
[Informes financieros de Excel integrados](finance-analyze-excel.md)  
[Informes financieros clave integrados](finance-reports.md)  
[Informes de activos fijos integrados](fa-reports.md)  
[Informes de cobros integrados](receivables-reports.md)  
[Informes de pagos integrados](payables-reports.md)  
[Información general sobre finanzas](finance.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
