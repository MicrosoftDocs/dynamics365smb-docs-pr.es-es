---
title: Análisis de activos fijos
description: 'Aprenda a recopilar, analizar y compartir datos sobre activos fijos para inteligencia empresarial.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis de activos fijos

Las empresas con activos fijos capturan una gran cantidad de datos sobre ellos durante las actividades diarias. Esos datos respaldan una valiosa inteligencia empresarial (BI) para los administradores de activos fijos:

- Adquisiciones de activos
- Depreciación de activos
- Seguro y mantenimiento
- Presupuestos de activos

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona características para ayudarle a recopilar, analizar y compartir datos sobre activos fijos de su organización:

- Informes financieros (para estados financieros y KPI sobre cuentas de activos fijos)
- Análisis ad hoc en listas
- Análisis ad-hoc de datos en Excel (usando Abrir en Excel)
- Herramientas integradas de análisis de activos fijos
- Informes de activos fijos integrados

> [!NOTE]
> El análisis de activos fijos es un poco diferente a otras áreas. Necesita analizar datos que ya están presentes, como adquisiciones de activos, depreciación y seguros, pero también datos sobre datos futuros (proyectados), como depreciación y retiros de activos. Para el último tipo de análisis, [!INCLUDE[prod_short](includes/prod_short.md)] tiene informes integrados que pueden calcular estos números.

Cada característica tiene sus propias ventajas y desventajas, según el tipo de análisis de datos y el rol del usuario. Para obtener más información, vaya a [Información general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md).

Este artículo describe formas de utilizar estas características de análisis para obtener información sobre sus activos fijos.

## Necesidades de análisis en la administración de activos

A la hora de pensar en las necesidades analíticas en la administración de activos, puede ser útil utilizar un modelo basado en personas que describa sus necesidades analíticas a alto nivel.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Cuando se trata de datos, las personas que desempeñan diferentes funciones tienen diferentes necesidades y utilizan los datos de diferentes maneras. Por ejemplo, las personas en administración de activos y finanzas interactúan con los datos de manera diferente que las personas en ventas.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Agregación de datos  | Formas típicas de consumir datos                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO / COO / CEO                 | Datos de rendimiento  | KPI <br> Paneles <br> Informes financieros           |
|Gestión de activos / Controlador   | Tendencias, resúmenes | Informes de gestión integrados <br> Análisis ad hoc      | 
|Contable                      | Datos detallados     | Informes operativos integrados <br> Datos de tareas en pantalla |

## KPI de gestión de activos

Un indicador clave de rendimiento (KPI) es un valor medible que muestra la eficacia con la que está cumpliendo sus objetivos. En la gestión de activos, las personas suelen utilizar los siguientes KPI para monitorear el uso de activos de su organización:

- Facturación de activos totales
- Rendimiento de los activos

## Usar los informes financieros para elaborar estados financieros y KPI relacionados con activos fijos

La característica **Financial Reporting** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Específicamente para la administración de activos, puede configurar informes financieros en las cuentas de contabilidad general que utiliza para realizar un seguimiento de los registros de activos fijos.

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que puede agregar a un movimiento como parámetro. Las dimensiones, la permiten agrupar movimientos que tienen características similares, como clientes, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Para más información sobre los informes financieros, vaya a [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md).

## Informes financieros entre unidades de negocio o entidades jurídicas (relacionadas con activos fijos)

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones primarias. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada. Específicamente para la administración de activos, es posible que desee consolidar las entradas de contabilidad general de sus cuentas de activos fijos para realizar un seguimiento de los KPI de activos fijos en todas las unidades de negocios o entidades jurídicas.

Para obtener más información, vaya a [Consolidación de empresa](finance-consolidated-company-reporting.md).

## Análisis ad-hoc de datos de activos fijos

A veces, solo es necesario comprobar si los números cuadran correctamente o confirmar rápidamente una cifra. Las siguientes características son excelentes para análisis ad hoc:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La función de análisis de datos le permite abrir casi una página de lista, como **Movimientos de contabilidad** o **Entradas de diario de cliente**, entrar en el modo de análisis y luego agrupar, filtrar y pivotar los datos como mejor le parezca.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Movs. Activos para ver el valor de un activo." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista para movimientos, opcionalmente filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador con Excel para la web. 

Para obtener más información sobre cómo realizar análisis ad hoc en movimientos de activos, consulte [Análisis ad hoc de datos de activos fijos](ad-hoc-analysis-fa.md).


## Informes de activos fijos integrados

[!INCLUDE [prod_short](includes/prod_short.md)] incluye diversos informes integrados, funciones de seguimiento y herramientas para ayudar a los auditores o controladores que informan de activos fijos.

Para obtener una descripción general de los informes disponibles, elija **Todos los informes** en la parte superior de su página de inicio. Esta acción abre la página Explorador de roles, que se filtra según las funciones en la opción **Informe y análisis**. Para buscar informes relacionados con activos fijos, en el campo **Buscar**, introduzca **Activos fijos**. Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Ejemplo de informes sobre el centro de roles financieros" lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Para obtener más información sobre los informes que son relevantes para los activos fijos, consulte [Informes integrados de activos fijos](fa-reports.md).

## Análisis de activos fijos en pantalla

[!INCLUDE [prod_short](includes/prod_short.md)] tiene varias páginas que le brindan resúmenes de activos fijos y tareas por realizar. Aquí mostramos algunos ejemplos para empezar:

- [Registrar y calcular la amortización y analizarla](fa-how-depreciate-amortize.md)
- [Supervisar costes de mantenimiento](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Controlar la cobertura de seguros](fa-how-insure.md#to-monitor-insurance-coverage)
- [Ver valores modificados del libro de amortización](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Ver movimientos de venta/baja](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Ver valores venta/baja previstos](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Mostrar movimientos de contabilidad general y saldos del libro mayor de activos fijos desde la página Plan de cuentas

La página Plan de cuentas muestra todas las cuentas de contabilidad general con números agregados en la contabilidad general. Desde esta página, puede hacer cosas como:  

- Ver informes que muestran movimientos de contabilidad y saldos.  
- Revisar una lista de grupos contables para dicha cuenta.
- Para ver los saldos del Debe y el Haber de una sola cuenta.

Específicamente para activos fijos, puede crear una vista en la página Plan de cuentas que solo muestre las cuentas de activos o quizás solo las cuentas de activos que utiliza para registrar entradas de activos fijos.

:::image type="content" source="media/chart-of-accounts-page-fa.png" alt-text="Ejemplo de cómo la página del Plan de cuentas muestra información financiera" lightbox="media/chart-of-accounts-page-fa.png":::

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts).

### Analizar datos por dimensiones (relacionadas con activos fijos)

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como A/F diarios. Por ejemplo, las dimensiones pueden, por ejemplo, indicar de qué departamento o ubicación procede un movimiento.  

Así pues, en lugar de configurar cuentas de libro mayor separadas para cada departamento o ubicación, puede utilizar las dimensiones como base para el análisis y evitar tener que crear una estructura de plan de cuentas complicada.

Para obtener más información, vaya a [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)

## Consulte también

[Manejar informes financieros entre unidades de negocio o entidades jurídicas](finance-consolidated-company-reporting.md)  
[Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts)  
[Análisis ad-hoc de datos de activos fijos](ad-hoc-analysis-fa.md)   
[Informes de activos fijos integrados](fa-reports.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
