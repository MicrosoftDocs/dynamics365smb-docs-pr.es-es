---
title: Análisis de compras
description: 'Business Central contiene muchas funciones que le ayudan a recopilar, analizar y compartir datos de venta valiosos para la inteligencia empresarial y la toma de decisiones en la organización de compra.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis de compras

Las empresas capturan muchos datos durante las actividades diarias que sirven de apoyo a la inteligencia empresarial (BI) para los responsables de compras:

- Ofertas de compra
- Pedidos de compra
- Facturas de compra

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona características para ayudarle a recopilar, analizar y compartir la información de compras de su organización:

- Análisis ad hoc en listas
- Análisis ad-hoc de datos en Excel (usando Abrir en Excel)
- Informes de ventas integrados

Cada una de estas características tiene sus ventajas y desventajas, según el tipo de análisis de datos y el rol del usuario. Para obtener más información, vaya a [Información general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md).

Este artículo presenta cómo puede utilizar estas características analíticas para obtener información de compras.

## Necesidades de análisis en compras

Cuando piense en las necesidades analíticas en las compras, puede que le ayude utilizar un modelo basado en personas que describa las diferentes necesidades analíticas a alto nivel.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Las personas que desempeñan diferentes roles tienen diferentes necesidades en lo que respecta a los datos y los utilizan de diferentes maneras. Por ejemplo, las personas en administración de activos y finanzas interactúan con los datos de manera diferente que las personas en ventas.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Agregación de datos  | Formas típicas de consumir datos                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CSO / CFO / CEO    | Datos de rendimiento  | KPI <br> Paneles <br> Informes financieros           |
|Director de compras      | Tendencias, resúmenes | Informes de gestión integrados <br> Análisis ad hoc      | 
|Director de compras / Agente de compras | Datos detallados     | Informes operativos integrados <br> Datos de tareas en pantalla |

<!-- 
## Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## Usar los informes financieros para elaborar estados financieros y KPI (relacionados con las compras)

La característica **Financial Reporting** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Específicamente para compras, puede configurar informes financieros en las cuentas de contabilidad general que utiliza para realizar un seguimiento de las contabilizaciones de compras.

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que puede agregar a un movimiento como parámetro. las dimensiones, la permiten agrupar movimientos que tienen características similares, como clientes, regiones y productos, y así poder recuperar con facilidad estos grupos para su análisis. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Para más información sobre los informes financieros, vaya a [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md).

## Informes financieros entre unidades de negocio o entidades jurídicas (relacionadas con la compra)

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones primarias. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada. Específicamente para la administración de compras, es posible que desee consolidar las entradas de contabilidad general de sus cuentas de compras para realizar un seguimiento de los KPI de ventas en todas las unidades de negocios o entidades jurídicas.

Para obtener más información, vaya a [Consolidación de empresa](finance-consolidated-company-reporting.md).

## Análisis ad-hoc de datos de compra

A veces, solo es necesario comprobar si los números cuadran correctamente o confirmar rápidamente una cifra. Las siguientes características son excelentes para análisis ad hoc:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La característica **Análisis de datos** le permite abrir casi cualquier página de lista, como **Pedidos de compra**, **Histórico facturas compra**, **Movs. proveedores** o **Entradas de contabilidad general**, entrar en el modo de análisis y, a continuación, agrupar, filtrar y pivotar los datos como mejor le parezca.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página Movimientos de cliente" lightbox="media/data-analysis-vendor-ledger-entries.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista, filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en los datos de movimientos de cliente usando Excel" lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador.

Para obtener más información sobre cómo realizar análisis ad hoc de datos de compras, vaya a [Análisis ad hoc de datos de compras](ad-hoc-analysis-purchasing.md).

## Informes integrados para compras

[!INCLUDE [prod_short](includes/prod_short.md)] incluye varios informes integrados, funciones de seguimiento y herramientas para ayudar a las organizaciones de compras a generar informes sobre sus datos.

Para obtener una descripción general de los informes disponibles, elija **Todos los informes** en la parte superior de su página de inicio. Esta acción abre el explorador de roles, que se filtra según las funciones en la opción **Informe y análisis**. Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Ejemplo de informes sobre el centro de roles financieros XXX" lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Para obtener más información sobre los informes relevantes para las compras, vaya a [Informes de compras integrados](purchase-reports.md).

## Análisis de compras en pantalla

[!INCLUDE [prod_short](includes/prod_short.md)] tiene varias páginas que le brindan resúmenes de compras y tareas por realizar. Aquí mostramos un ejemplo para empezar:

- [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)  
- [Calcular las fechas de compras](purchasing-date-calculation-for-purchases.md)
- [Ver movimientos de compras](purchasing-how-record-purchases.md#viewing-ledger-entries)


### Mostrar los movimientos y balances de contabilidad general relacionados con las compras desde la página del plan de cuentas

La página Plan de cuentas muestra todas las cuentas de contabilidad general con números agregados registrados en la contabilidad general. Desde esta página, puede hacer cosas como:  

- Ver informes que muestran movimientos de contabilidad y saldos.  
- Revisar una lista de grupos contables para dicha cuenta.
- Para ver los saldos del Debe y el Haber de una sola cuenta.

Específicamente para compras, puede crear una vista en la página Plan de cuentas que solo muestre las cuentas que utiliza para registrar entradas de compras.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Ejemplo de cómo la página del Plan de cuentas muestra información financiera" lightbox="media/chart-of-accounts-page.png":::

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts).

### Analizar datos por dimensiones (relacionadas con las compras)

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de compra. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Así pues, en lugar de configurar cuentas de libro mayor separadas para cada departamento o ubicación, puede utilizar las dimensiones como base para el análisis y evitar tener que crear una estructura de plan de cuentas complicada.

Para obtener más información, vaya a [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## Consulte también

[Consolidación de empresa](finance-consolidated-company-reporting.md)  
[Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Manejar informes financieros entre unidades de negocio o entidades jurídicas](finance-consolidated-company-reporting.md)  
[Análisis ad-hoc de datos de compra](ad-hoc-analysis-purchasing.md)  
[Informes integrados para compras](purchase-reports.md)  
[Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]