---
title: Trabajar con diseños de Excel
description: Aprenda a crear y modificar diseños de informes creados con Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: c0800642804b8e8c9e1dc629224bfac77b174500
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075738"
---
# <a name="working-with-excel-layouts"></a>Trabajar con diseños de Excel

Los diseños de informes de Excel se basan en libros de Microsoft Excel (archivos .xlsx). Le permiten crear informes utilizando las características conocidas de Excel para resumir, analizar y presentar datos, como las fórmulas, PivotTables y PivotCharts.

![Muestra el ejemplo de un diseño de Excel.](media/excel-layout-2.png)

En este artículo se explican algunas de las cosas más importantes que debe saber para empezar a usar los diseños de Excel.

## <a name="why-use-excel-layouts"></a>¿Por qué usar diseños de Excel?

He aquí algunas otras ventajas de usar los diseños de Excel:

- Crear informes interactivos usando visualizaciones como segmentaciones
- Ver datos sin procesar del conjunto de datos del informe para ayudar a comprender cómo funciona el informe y de dónde provienen los datos de las imágenes
- Usar las funciones integradas de Office para realizar el posprocesamiento en los informes presentados, como:
  - [Proteger las hojas de cálculo](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Aplicar etiquetas de sensibilidad](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Agregar comentarios y notas](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Previsión y análisis](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Use complementos instalados e integraciones de aplicaciones, como flujos de Power Automate o OneDrive.

## <a name="get-started"></a>Introducción

La configuración de un diseño de Excel en un informe conlleva básicamente dos tareas:

1. Crear el nuevo archivo de diseño de Excel.
2. Agregar el nuevo diseño al informe.

## <a name="task-1-create-the-excel-layout-file"></a>Tarea 1: Crear el archivo de diseño de Excel

Hay tres maneras de crear un archivo de diseño de Excel para un informe, como se explica en esta sección

### <a name="from-any-report"></a>[Desde cualquier informe](#tab/any-report)

Puede usar los siguientes pasos para crear un diseño de Excel a partir de cualquier informe, independientemente del tipo de diseño actual. El diseño de Excel contendrá la hora de **Datos** necesaria y una tabla, una hoja de **Metadatos de informe** y nada más.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. En la lista **Diseños de informe**, seleccione cualquier diseño para el informe y, a continuación, elija la acción **Ejecutar informe**.
3. En la página de solicitud de informes, seleccione **Enviar a** > **Documento de Microsoft Excel (solo datos)** > **Aceptar**.

   Este paso descarga un libro de Excel que contiene el conjunto de datos del informe.
4. Abra el archivo descargado en Excel, realice los cambios y después guarde el archivo.

### <a name="from-another-excel-layout-on-a-report"></a>[Desde otro diseño de Excel en un informe](#tab/other-layout)

Si ya hay un diseño de Excel para un informe, use el diseño existente como punto de partida. Hay dos enfoques para obtener una copia del diseño. Puede exportar el diseño existente desde la página **Diseños de informe** o descargar el diseño desde la página de solicitud de informes. Ambas formas descargan un archivo de diseño de Excel que incluye todas las hojas del archivo existente. La diferencia es que a partir de la página de solicitud, el diseño incluirá datos reales. Los datos no son necesarios, pero ayudan a la hora de diseñar el diseño.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Enfoque 1: Exportar el diseño desde la página **Diseños de informe**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño de Excel de la lista y luego elija la acción **Exportar diseño** desde la parte superior de la página.
3. Abra el archivo en Excel, realice los cambios y después guarde el archivo.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Enfoque 2: Descargar el diseño de la página de solicitud de informes

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. En la lista **Diseños de informe**, seleccione cualquier diseño para el informe y, a continuación, elija la acción **Ejecutar informe**.
3. En la página de solicitud de informes, seleccione **Descargar**.
4. Abra el archivo en Excel, realice los cambios y después guarde el archivo.

### <a name="from-al-code"></a>[Desde el código AL](#tab/from-code)

Esta forma es la más avanzada. Requiere conocimientos de código AL, por lo que se dirige a los programadores. Los diseños de Excel, en este caso, forman parte de un paquete de extensión que usted instala. Para obtener más información, consulte [Crear un informe de diseños de Excel](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) en la ayuda para desarrolladores y profesionales de TI.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Tarea 2: Agregar el diseño de Excel al informe

Una vez que tenga el archivo de diseño de Excel, la siguiente tarea es agregarlo como un nuevo diseño para el informe.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione **Nuevo diseño**.
3. Establezca el **Id. informe** para informes.
4. Introduzca un nombre en **Nombre del diseño**.
5. Establezca **Opciones de formato** en **Excel**.
6. Seleccione **Aceptar** > **Elegir** para abrir el explorador de archivos en el dispositivo. 
7. Busque y seleccione el archivo de Excel y, a continuación, seleccione **Abrir**.

   El archivo seleccionado se carga en el diseño y vuelve a la página **Diseños de informes**.
8. Si desea ver cómo se ve el informe con el nuevo diseño, seleccione el diseño en la lista y luego seleccione **Ejecutar informe**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Comprender los diseños de Excel

Hay algunas cosas que debe saber o tener en cuenta cuando comience a crear o realizar cambios en los diseños de Excel. Todo diseño de Excel debe incluir dos elementos: una hoja **Datos** y una tabla **Datos**. Estos elementos forman la base del diseño al definir los datos empresariales de Business Central con los que se puede trabajar. Puede pensar en la hoja **Datos** como un tipo de contrato entre el diseño de los datos comerciales. Usará estos datos como origen de cálculos y visualizaciones que desea presentar en otras hojas.

Hay algunos requisitos específicos para la estructura del libro de Excel. Si no se cumplen los requisitos, tendrá problemas para usar el diseño. El diagrama y la tabla siguientes describen los elementos de un diseño de Excel y los requisitos.

[![Muestra los diferentes elementos de un diseño de Excel.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nº|Elemento|Descripción|Obligatoria|
|---|-------|----|---|
|1|Hoja **Datos**|<ul><li>Debe tener el nombre **Datos**</li><li>Solo puede incluir una tabla, y la tabla debe tener el nombre **Datos**</li></ul>|![Es obligatorio](media/check.png) | 
|2|Tabla **Datos**|<ul><li>Debe tener el nombre **Datos**</li><li>Debe tener al menos una columna.</li><li>Solo puede incluir columnas que están en el conjunto de datos del informe.</li><li>Debe comenzar en la primera celda **A1** de la hoja **Datos**</li></ul>|![Es obligatorio](media/check.png)|
|3|Hojas de presentación|<ul><li>Se usan para presentar datos.</li><li>Los datos provienen de la hoja **Datos**. </li></ul>||
|4|Hoja **Metadatos de informe**|<ul><li>Se incluye automáticamente si el diseño se creó exportando otro informe como Excel</li><li>Contiene información general sobre el informe</li><li>Se puede eliminar</li></ul>|

Para resumir lo que puede y no puede hacer en la hoja **Datos**:

- No cambie el nombre de la hoja **Datos**, la tabla **Datos** o las columnas.
- Puede eliminar u ocultar columnas.
- No agregue columnas a menos que estén incluidas en el conjunto de datos del informe.
- Puede colocar las hojas en cualquier orden. Por ejemplo, la hoja **Datos** puede ser la primera o la última.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Preparar Financial Reporting con esquemas de cuentas y categorías de cuentas](bi-how-work-account-schedule.md)  
[Inteligencia empresarial](bi.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Análisis de datos de informes con Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]