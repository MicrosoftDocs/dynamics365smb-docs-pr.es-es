---
title: Trabajar con diseños de Excel
description: Aprenda a crear y modificar diseños de informes creados con Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 11/10/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Trabajar con diseños de Microsoft Excel

Los diseños de informes de Microsoft Excel se basan en libros de Excel (archivos .xlsx). Con ellos, puede crear informes que incluyen características conocidas de Excel para resumir, analizar y presentar datos como las fórmulas, tablas dinámicas, gráficos dinámicos y más.

![Muestra un ejemplo de un diseño de Excel.](media/excel-layout-2.png)

En este artículo se explican información que es importante que sepa para empezar a usar los diseños de Excel.

## ¿Por qué usar diseños de Excel?

Beneficios de usar diseños de Excel:

- Crear informes interactivos usando visualizaciones como segmentaciones.
- Ver datos sin procesar del conjunto de datos del informe, lo que le ayudará a comprender cómo funciona el informe y de dónde provienen los datos de las imágenes.
- Usar las funciones integradas de Microsoft Office para realizar el posprocesamiento en los informes presentados, como:
  - [Proteger hojas de cálculo](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Aplicar etiquetas de sensibilidad](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Agregar comentarios y notas](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Previsión y análisis](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Use complementos instalados e integraciones de aplicaciones, como flujos de Power Automate o OneDrive.

## Comenzar

La configuración de un diseño de Excel en un informe conlleva básicamente dos tareas:

1. Crear el nuevo archivo de diseño de Excel.
2. Agregar el nuevo diseño al informe.

## Tarea 1: Crear el archivo de diseño de Excel

Estas son las tres maneras de crear un archivo de diseño de Excel para un informe.

### [Desde cualquier informe](#tab/any-report)

Siga estos pasos para crear un diseño de Excel a partir de cualquier informe, independientemente del tipo de diseño actual. El diseño de Excel contendrá la hora de **Datos** necesaria y una tabla, una hoja de **Metadatos de informe** y nada más.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. En la página **Diseños de informe**, elija cualquier diseño para el informe y, a continuación, elija la acción **Ejecutar informe**.
3. En la página de solicitud de informes, seleccione **Enviar a** > **Documento de Microsoft Excel (solo datos)** > **Aceptar**.

   Este paso descarga un libro de Excel que contiene el conjunto de datos del informe.
4. Abra el archivo descargado en Excel, realice los cambios y después guarde el archivo.

### [Desde otro diseño de informe de Excel](#tab/other-layout)

Si ya hay un diseño de Excel para un informe, puede usar el diseño existente como punto de partida. Hay dos enfoques para obtener una copia del diseño. Puede exportar el diseño existente desde la página **Diseños de informe**, o bien descargar el diseño desde la página de solicitud de informes. Ambas formas descargan un archivo de diseño de Excel que incluye todas las hojas del archivo existente. La diferencia radica en que cuando lo descarga desde la página de solicitud, el diseño incluye datos reales. (Los datos no son necesarios, pero ayudan a la hora de diseñar el diseño).

#### Enfoque 1: Exportar el diseño desde la página **Diseños de informe**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño de Excel de la lista y luego elija la acción **Exportar diseño** desde la parte superior de la página.
3. Abra el archivo en Excel, realice los cambios y después guarde el archivo.

#### Enfoque 2: Descargar el diseño de la página de solicitud de informes

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. En la página **Diseños de informe**, elija cualquier diseño para el informe y, a continuación, elija la acción **Ejecutar informe**.
3. En la página de solicitud del informe, seleccione **Descargar**.
4. Abra el archivo en Excel, realice los cambios y después guarde el archivo.

### [Desde el código AL](#tab/from-code)

Este es el método más avanzado de crear un diseño de informe de Excel. Como requiere tener conocimientos de código AL, se dirige a programadores. En este enfoque, los diseños de Excel forman parte de un paquete de extensión que usted instala. Obtenga más información en [Crear un informe de diseños de Excel](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) en la ayuda para desarrolladores y profesionales de TI.

---

## Tarea 2: Agregar el diseño de Excel al informe

Una vez que tenga el archivo de diseño de Excel, la siguiente tarea es agregarlo como un nuevo diseño para el informe.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione **Nuevo diseño**.
3. Establezca el **Id. informe** en *Informe*.
4. Introduzca un nombre en **Nombre del diseño**.
5. Establezca **Opciones de formato** en **Excel**.
6. Seleccione **Aceptar** y luego realice uno de los siguientes pasos para cargar el archivo de diseño del informe:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   El archivo seleccionado se carga en el diseño y la página **Diseños de informes** se abre.
8. Para ver cómo se ve el informe con el nuevo diseño, seleccione el diseño en la lista y luego seleccione **Ejecutar informe**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## Comprender los diseños de Excel

Hay algunas cosas que debe saber o tener en cuenta cuando cree o introduzca cambios en los diseños de Excel. Todo diseño de Excel debe incluir dos elementos: una hoja de **Datos** y una tabla de **Datos**. Estos elementos forman la base del diseño al definir los datos empresariales de Business Central con los que se puede trabajar. Puede considerar la hoja de **Datos** como un tipo de contrato entre el diseño y los datos empresariales. Usará estos datos como origen de cálculos y visualizaciones que desea presentar en otras hojas.

Hay algunos requisitos específicos para la estructura del libro de Excel. Si no se cumplen los requisitos, tendrá problemas para usar el diseño. El diagrama y la tabla siguientes describen los elementos de un diseño de Excel y los requisitos.

[![Muestra los diferentes elementos de un diseño de Excel.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|N.º|Elemento|Descripción|Obligatoria|
|---|-------|----|---|
|1|Hoja **Datos**|<ul><li>Debe tener el nombre **Datos**.</li><li>Solo puede incluir una tabla, que debe tener el nombre **Datos**.</li></ul>|![Es obligatorio](media/check.png) | 
|2|Tabla **Datos**|<ul><li>Debe tener el nombre **Datos**.</li><li>Debe tener al menos una columna.</li><li>Solo puede incluir columnas que están en el conjunto de datos del informe.</li><li>Debe comenzar en la primera celda **A1** de la hoja de **Datos**.</li></ul>|![Es obligatorio](media/check.png)|
|3|Hojas de presentación|<ul><li>Se usan para presentar datos.</li><li>Los datos provienen de la hoja **Datos**. </li></ul>||
|4|Hoja **Metadatos de informe**|<ul><li>Se incluye automáticamente si el diseño se creó exportando otro informe de Excel.</li><li>Contiene información general sobre el informe.</li><li>Se puede eliminar.</li></ul>|

En resumen, esto es lo que debe y no debe hacer en la hoja de **Datos**:

- No cambie el nombre de la hoja **Datos**, la tabla **Datos** o las columnas.
- Puede eliminar u ocultar columnas.
- No agregue columnas a menos que estén incluidas en el conjunto de datos del informe.
- Puede colocar las hojas en cualquier orden, con la hoja de **Datos** en primer o último lugar.

## Consulte también .

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Inteligencia empresarial](bi.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Análisis de datos de informes con Excel](report-analyze-excel.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
