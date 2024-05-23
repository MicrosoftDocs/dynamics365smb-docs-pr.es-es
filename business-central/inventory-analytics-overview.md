---
title: Análisis de inventario
description: 'Business Central contiene muchas funciones que le ayudan a recopilar, analizar y compartir datos valiosos sobre su inventario para la inteligencia empresarial y la toma de decisiones en su organización.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis de inventario

Las empresas capturan muchos datos durante las actividades diarias que sirven de apoyo a la inteligencia empresarial (BI) para los responsables de inventarios:

- Envío de bienes cuando se cumplan los pedidos de venta.
- Recibos de artículos cuando se cumplen los pedidos de compra.
- Movimientos de productos entre almacenes:

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona características para ayudarle a recopilar, analizar y compartir la información de inventario de su organización:

- Análisis ad hoc en listas
- Análisis ad-hoc de datos en Excel (usando Abrir en Excel)
- Herramientas de análisis de inventario integradas
- Informes de inventario integrados

Cada una de estas características tiene sus ventajas y desventajas, según el tipo de análisis de datos y el rol del usuario. Para obtener más información, vaya a [Información general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md).

Este artículo presenta cómo puede utilizar estas características analíticas para obtener información sobre su inventario.

## Necesidades de análisis en inventario

Cuando piense en las necesidades analíticas en la administración de inventario, puede que le ayude utilizar un modelo basado en personas que describa las diferentes necesidades analíticas a alto nivel.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Las personas que desempeñan diferentes roles tienen diferentes necesidades en lo que respecta a los datos y los utilizan de diferentes maneras. Por ejemplo, las personas en administración de activos y finanzas interactúan con los datos de manera diferente que las personas en ventas.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Agregación de datos  | Formas típicas de consumir datos                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CFO / CEO    | Datos de rendimiento  | KPI, paneles de control, informes financieros           |
|Administrador de inventario  | Tendencias, resúmenes | Informes de administración integrados, análisis ad hoc      | 
|Trabajador de almacén   | Datos detallados     | Informes operativos integrados, datos de tareas en pantalla |

<!-- 
## Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Usar los informes financieros para elaborar estados financieros y KPI relacionados con el inventario

La característica **Financial Reporting** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Específicamente para la administración de inventarios, puede configurar informes financieros en las cuentas de contabilidad general que utiliza para realizar un seguimiento de los registros de inventarios.

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que agrega a un movimiento como parámetro. las dimensiones, la permiten agrupar movimientos que tienen características similares, como clientes, regiones, productos y vendedor. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Para más información sobre los informes financieros, vaya a [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md).

## Informes financieros entre unidades de negocio o entidades jurídicas (relacionadas con el inventario)

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones primarias. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada. Específicamente para la administración de inventarios, es posible que desee consolidar las entradas de contabilidad general de sus cuentas de inventarios para realizar un seguimiento de los KPI de ventas en todas las unidades de negocios o entidades jurídicas.

Para obtener más información, vaya a [Consolidación de empresa](finance-consolidated-company-reporting.md).

## Análisis ad-hoc de datos de inventario

A veces, solo es necesario comprobar si los números cuadran correctamente o confirmar rápidamente una cifra. Las siguientes características son excelentes para análisis ad hoc:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La función de análisis de datos le permite abrir casi una página de lista, como **Movs. productos**, entrar en el modo de análisis y luego agrupar, filtrar y pivotar los datos como mejor le parezca.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Ejemplo de cómo realizar análisis de datos de stock antiguos en la página Movimientos de productos" lightbox="media/data-analysis-inventory-dead-stock.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista, opcionalmente filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador.

Para obtener más información sobre cómo realizar análisis ad hoc de datos de inventarios, vaya a [Análisis ad hoc de datos de inventario](ad-hoc-analysis-inventory.md).

## Informes integrados para inventario

[!INCLUDE [prod_short](includes/prod_short.md)] incluye varios informes integrados, funciones de seguimiento y herramientas para ayudar a las organizaciones de inventario a generar informes sobre sus datos.

Para obtener una descripción general de los informes disponibles, elija **Todos los informes** en su página de inicio. Esta acción abre el explorador de informes, que se filtra según las funciones en la opción **Informe y análisis**. En el encabezado **Ventas y marketing**, elija **Explorar**. Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Ejemplo de informes sobre el centro de roles de ventas" lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Para obtener más información sobre los informes relevantes para el inventario, vaya a [Informes de inventario y almacén integrados](inventory-WMS-reports.md).

## Análisis de inventarios en pantalla

[!INCLUDE [prod_short](includes/prod_short.md)] tiene varias páginas que le brindan resúmenes de inventario y tareas por realizar. Aquí mostramos algunos ejemplos para empezar:

- [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)
- [Seguir productos con números de serie, de lote y de paquete](inventory-how-work-item-tracking.md)
- [Seguir producto - Productos seguidos](inventory-how-to-trace-item-tracked-items.md)
- [Auditar la conciliación entre la contabilidad de inventario y la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Ver productos de tránsito directo en un envío o en la hoja de trabajo de picking](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

El módulo de ventas también incluye páginas de análisis relacionadas con el inventario:

- [Calcular fechas de compromiso de pedido](sales-how-to-calculate-order-promising-dates.md)
- [Calcular fechas de entrega para pedidos de venta](sales-date-calculation-for-sales.md)
- [Seguir paquetes](sales-how-track-packages.md)

### Mostrar los movimientos y balances de contabilidad general relacionados con el inventario desde la página del plan de cuentas

La página **Plan de cuentas** muestra todas las cuentas de contabilidad general con números agregados registrados en la contabilidad general. Desde esta página, puede hacer cosas como:  

- Ver informes que muestran movimientos de contabilidad y saldos.  
- Revisar una lista de grupos contables para dicha cuenta.
- Para ver los saldos del Debe y el Haber de una sola cuenta.

Específicamente para administración de inventario, puede crear una vista en la página Plan de cuentas que solo muestre las cuentas que utiliza para registrar entradas de inventario.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Ejemplo de cómo la página del Plan de cuentas muestra información financiera" lightbox="media/chart-of-accounts-page.png":::

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts).

### Analizar datos de inventario por dimensiones

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Así pues, en lugar de configurar cuentas de libro mayor separadas para cada departamento o ubicación, puede utilizar las dimensiones como base para el análisis y evitar tener que crear una estructura de plan de cuentas complicada.

Para obtener más información, vaya a [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## Consulte también

[Consolidación de empresa](finance-consolidated-company-reporting.md)   
[Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Gestionar los informes financieros de todas las unidades de negocio o entidades jurídicas](finance-consolidated-company-reporting.md)  
[Análisis ad-hoc de datos de inventario](ad-hoc-analysis-inventory.md)  
[Informes integrados de inventario y almacén](inventory-WMS-reports.md)  
[Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
