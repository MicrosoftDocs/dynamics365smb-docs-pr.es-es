---
title: Análisis de ventas
description: 'Business Central contiene muchas funciones que le ayudan a recopilar, analizar y compartir datos de venta valiosos para la inteligencia empresarial y la toma de decisiones en la organización de ventas.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="sales-analytics"></a>Análisis de ventas

Las empresas capturan muchos datos durante las actividades diarias que sirven de apoyo a la inteligencia empresarial (BI) para los responsables de ventas:

- Oportunidades
- Ofertas de venta
- Pedidos de venta
- Facturas de venta

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona características para ayudarle a recopilar, analizar y compartir la información de ventas de su organización:

- Análisis ad hoc en listas
- Análisis ad-hoc de datos en Excel (usando Abrir en Excel)
- Herramientas de análisis de ventas integradas
- Informes de ventas integrados

Cada una de estas características tiene sus ventajas y desventajas, según el tipo de análisis de datos y el rol del usuario. Para obtener más información, vaya a [Información general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md).

Este artículo presenta cómo puede utilizar estas características analíticas para proporcionar información de ventas.

## <a name="analytics-needs-in-sales"></a>Necesidades de análisis en ventas

Cuando piense en las necesidades analíticas en la administración de ventas, puede que le ayude utilizar un modelo basado en personas que describa las diferentes necesidades analíticas a alto nivel.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Ilustración de diferentes personajes para análisis" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Las personas que desempeñan diferentes roles tienen diferentes necesidades en lo que respecta a los datos y los utilizan de diferentes maneras. Por ejemplo, las personas en administración de activos y finanzas interactúan con los datos de manera diferente que las personas en ventas.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Ilustración de cómo diferentes personas tienen diferentes necesidades analíticas" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Agregación de datos  | Formas típicas de consumir datos                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / CFO / CEO    | Datos de rendimiento  | KPI <br> Paneles <br> Informes financieros           |
|Dtor. ventas      | Tendencias, resúmenes | Informes de gestión integrados <br> Análisis ad hoc      | 
|Director de cuentas / Vendedor | Datos detallados     | Informes operativos integrados <br> Datos de tareas en pantalla |

<!-- 
## <a name="sales-kpis"></a>Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-sales"></a>Usar los informes financieros para elaborar estados financieros y KPI (relacionados con las ventas)

La característica **Financial Reporting** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Específicamente para la administración de ventas, puede configurar informes financieros en las cuentas de contabilidad general que utiliza para realizar un seguimiento de los registros de ventas.

Las dimensiones desempeñan un papel importante en la inteligencia empresarial. Una dimensión son datos que agrega a un movimiento como parámetro. las dimensiones, la permiten agrupar movimientos que tienen características similares, como clientes, regiones, productos y vendedor. Entre otros fines, utilice las dimensiones al definir las vistas de análisis y al crear informes financieros. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Para más información sobre los informes financieros, vaya a [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-sales"></a>Informes financieros entre unidades de negocio o entidades jurídicas (relacionadas con las ventas)

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones primarias. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada. Específicamente para la administración de ventas, es posible que desee consolidar las entradas de contabilidad general de sus cuentas de ventas para realizar un seguimiento de los KPI de ventas en todas las unidades de negocios o entidades jurídicas.

Para obtener más información, vaya a [Consolidación de empresa](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-sales-data"></a>Análisis ad-hoc de datos de ventas

A veces, solo es necesario comprobar si los números cuadran correctamente o confirmar rápidamente una cifra. Las siguientes características son excelentes para análisis ad hoc:

- Análisis de datos en las páginas de la lista del libro mayor
- Abrir en Excel

La función de análisis de datos le permite abrir casi una página de lista, como **Movimientos de contabilidad**, **Entradas de diario de cliente**, **Movimientos contables del producto** o **Facturas registradas**, entrar en el modo de análisis y luego agrupar, filtrar y pivotar los datos como mejor le parezca.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página Movimientos de cliente" lightbox="media/data-analysis-customer-ledger-entries.png":::

Del mismo modo, puede utilizar la acción **Abrir en Excel** para abrir una página de lista, opcionalmente filtrar la lista a un subconjunto de datos y luego usar Excel para trabajar con los datos. Por ejemplo, mediante el uso de funciones como Analizar datos, Análisis hipotético u Hoja de previsión.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en los datos de movimientos de cliente usando Excel" lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Si configura OneDrive para funciones del sistema, el libro de trabajo de Excel se abre en su navegador.

Para obtener más información sobre cómo realizar análisis ad hoc de datos de ventas, vaya a [Análisis ad hoc de datos de ventas](ad-hoc-analysis-sales.md). 

## <a name="built-in-reports-for-sales"></a>Informes de ventas integrados

[!INCLUDE [prod_short](includes/prod_short.md)] incluye varios informes integrados, funciones de seguimiento y herramientas para ayudar a las organizaciones de ventas a generar informes sobre sus datos.

Para obtener una descripción general de los informes disponibles, elija **Todos los informes** en el panel superior de su página de inicio. Esta acción abre el explorador de roles, que se filtra según las funciones en la opción **Informe y análisis**. Para obtener más información, vaya a [Búsqueda de informes con el explorador de roles](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Ejemplo de informes sobre el centro de roles financieros" lightbox="media/report-explorer-sales.png":::

Los informes integrados vienen en dos versiones:

- Diseñado para imprimir (pdf).
- Diseñado para análisis en Excel.

Para obtener más información sobre los informes relevantes para las ventas, vaya a [Informes de ventas integrados](sales-reports.md).

## <a name="on-screen-sales-analytics"></a>Análisis de ventas en pantalla

[!INCLUDE [prod_short](includes/prod_short.md)] tiene varias páginas que le brindan resúmenes de ventas y tareas por realizar. Aquí mostramos algunos ejemplos para empezar:

- [Abra la lista **Ofertas de venta**](https://businesscentral.dynamics.com/?page=9300)
- [Abra la lista **Pedidos de venta**](https://businesscentral.dynamics.com/?page=9305)
- [Abra la lista **Histórico facturas venta**](https://businesscentral.dynamics.com/?page=143)
- [Abra la lista **Pedidos de devolución de ventas**](https://businesscentral.dynamics.com/?page=9304)
- [Calcular fechas de compromiso de pedido](sales-how-to-calculate-order-promising-dates.md)
- [Calcular fechas de entrega para pedidos de venta](sales-date-calculation-for-sales.md)
- [Seguir paquetes](sales-how-track-packages.md)

### <a name="show-sales-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Mostrar movimientos de contabilidad general y saldos relacionados con ventas desde la página Plan de cuentas

La página Plan de cuentas muestra todas las cuentas de contabilidad general con números agregados registrados en la contabilidad general. Desde esta página, puede hacer cosas como:  

- Ver informes que muestran movimientos de contabilidad y saldos.  
- Revisar una lista de grupos contables para dicha cuenta.
- Para ver los saldos del Debe y el Haber de una sola cuenta.

Específicamente para ventas, puede crear una vista en la página Plan de cuentas que solo muestre las cuentas que utiliza para registrar entradas de ventas.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Ejemplo de cómo la página del Plan de cuentas muestra información financiera" lightbox="media/chart-of-accounts-page.png":::

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-sales"></a>Analizar datos por dimensiones (relacionadas con las ventas)

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Así pues, en lugar de configurar cuentas de libro mayor separadas para cada departamento o ubicación, puede utilizar las dimensiones como base para el análisis y evitar tener que crear una estructura de plan de cuentas complicada.

Para obtener más información, vaya a [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Consulte también

[Consolidación de empresa](finance-consolidated-company-reporting.md)   
[Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Gestionar los informes financieros de todas las unidades de negocio o entidades jurídicas](finance-consolidated-company-reporting.md)  
[Análisis ad-hoc de datos de ventas](ad-hoc-analysis-sales.md)   
[Informes de ventas integrados](sales-reports.md)   
[Conocer el plan de cuentas](finance-general-ledger.md#the-chart-of-accounts)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
