---
title: Análisis ad-hoc de datos de sostenibilidad
description: Aprenda a usar el modo de análisis de datos para analizar datos de sostenibilidad.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis ad-hoc de datos de sostenibilidad

En este artículo se explica cómo usar la característica de **Análisis de datos** para analizar datos de sostenibilidad directamente de las páginas de lista y consultas. No es necesario ejecutar un informe ni cambiar a otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Información general de emisiones" o "Emisiones por ámbito", o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las siguientes páginas de lista para análisis ad hoc de datos de sostenibilidad:

- [Movimientos del diario de sostenibilidad](https://businesscentral.dynamics.com/?page=6220)

## Escenarios de análisis ad hoc de sostenibilidad

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de sostenibilidad en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Información general de emisiones (suma por categoría)](#example-emission-overview-sum-by-category) | Analice sus emisiones por categoría. | [Movimientos del diario de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) | **Categoría de cuenta**, **Nombre de cuenta**, **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O**.|
| [Emisiones medias por categoría](#example-average-emissions-by-category) | Analice sus emisiones medias por categoría. | [Movimientos del diario de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) | **Categoría de cuenta**, **Nombre de cuenta**, **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O**.|
| [Emisiones por ámbito](#example-emissions-by-scope) | Analice sus emisiones por ámbito. | [Movimientos del diario de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) | **Ámbito de la emisión**, **Categoría de cuenta**, **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O**.|

## Ejemplo: Información general de emisiones (suma por categoría)

Para analizar sus emisiones por categorías, siga estos pasos:

1. Abra la página [Movimientos de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active el modo **Dinámico** (ubicado directamente encima del campo **Buscar**).
1. Arrastre los campos **Categoría de cuenta** y **Nombre de cuenta** al área **Grupos de filas**. Arrastre los campos en ese orden.
1. Arrastre los campos **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O** al área **Valores**.
1. Cambie el nombre de su pestaña de análisis a **Información general de emisiones (sum)** o algo que describa este análisis para usted.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Ejemplo 1 de cómo realizar análisis de datos en la página Movimientos de sostenibilidad" lightbox="media/data-analysis-sustainability-entries.png":::

## Ejemplo: Emisiones medias por categoría

Para analizar sus emisiones medias por categorías, siga estos pasos:

1. Abra la página [Movimientos de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active el modo **Dinámico** (ubicado directamente encima del campo **Buscar**).
1. Arrastre los campos **Categoría de cuenta** y **Nombre de cuenta** al área **Grupos de filas**. Arrastre los campos en ese orden.
1. Arrastre los campos **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O** al área **Valores**.
1. Para cada campo en el área **Valores**, selecciónelo y cambie la función de agregación a `Average`.
1. Cambie el nombre de su pestaña de análisis a **Información general de emisiones (avg)** o algo que describa este análisis para usted.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Ejemplo 2 de cómo realizar análisis de datos en la página Movimientos de sostenibilidad" lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Ejemplo: Emisiones por ámbito

Para analizar sus emisiones por ámbito, siga estos pasos:

1. Abra la página [Movimientos de sostenibilidad](https://businesscentral.dynamics.com/?page=6220) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active el modo **Dinámico** (ubicado directamente encima del campo **Buscar**).
1. Arrastre los campos **Ámbito de la emisión** y **Categoría de cuenta** al área **Grupos de filas**. Arrastre los campos en ese orden.
1. Arrastre los campos **Emisiones de NH4**, **Emisiones de CO2** y **Emisiones de N2O** al área **Valores**.
1. Cambie el nombre de su pestaña de análisis a **Información general de emisiones por ámbito** o algo que describa este análisis para usted.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Ejemplo 3 de cómo realizar análisis de datos en la página Movimientos de sostenibilidad" lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Base de datos para análisis ad hoc de sostenibilidad

La información que introduzca en un diario de sostenibilidad es temporal y puede modificarla mientras esté en el diario. Al contabilizar el diario, la información se transfiere a las entradas del libro mayor de sostenibilidad en las cuentas individuales de sostenibilidad, donde no puede modificarse. Sin embargo, puede publicar entradas revertidas o corregidas. La página de lista [Movimientos sostenibilidad](https://businesscentral.dynamics.com/?page=6220) es el principal origen de datos para el análisis ad hoc de los datos de sostenibilidad.

Para obtener más información sobre cómo publicar entradas de sostenibilidad, vaya a [Registrar entradas de sostenibilidad](finance-sustainability-journal.md).

## Consulte también

[Registrar entradas de sostenibilidad](finance-sustainability-journal.md)  
[Informes de sostenibilidad integrados](sustainability-reports.md)   
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
