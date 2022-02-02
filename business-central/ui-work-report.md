---
title: Trabajar con informes, trabajos por lotes y XMLports
description: Obtenga información sobre cómo introducir un informe en una cola de proyectos y programarlo para que se procesa en una fecha y hora específicas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: d62c16ef8c511464fde86a1766499e37f8a07b1f
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972205"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Trabajar con informes, trabajos por lotes y XMLports

Un informe recopila información en función de un conjunto específico de criterios. Organiza y presenta la información en un formato fácil de leer que puede imprimir o guardar como un archivo. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente información relada con el contexto de la página en la que está. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales, estadísticas de ventas, etc.

Los trabajos por lotes y XMLports hacen más o menos lo mismo que los informes, pero se usan más para procesar o exportar datos. Por ejemplo, el trabajo por lotes **Crear recordatorios** crear documentos de recordatorio para los clientes que tienen pagos vencidos.  

> [!NOTE]
> Este tema hace referencia principalmente al "informe", pero se aplica información similar a los trabajos por lotes y XMLports.

## <a name="getting-started"></a>Introducción

Puede buscar informes en la pestaña **Informes** de páginas seleccionadas, o utilizar la búsqueda ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") para buscar informes por nombre.

Cuando abre un informe, un trabajo por lotes o XMLport, normalmente se le presenta una página de solicitud donde se establecen varias opciones y filtros que determinan qué se debe incluir en el informe. Las siguientes secciones explican cómo utilizar la página de solicitud para crear, obtener una vista previa e imprimir un informe.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Uso de valores predeterminados: configuración predefinida 

La mayoría de las páginas de solicitud incluyen el campo **Usar valores predeterminados de**. Este campo le permite seleccionar configuraciones predefinidas para el informe, que configuran automáticamente opciones y filtros para el informe. Seleccione una entrada de la lista desplegable y verá que las opciones y los filtros en la página de solicitud cambian en consecuencia.

La entrada denominada **Filtros y opciones usados por última vez** está siempre disponible. Esta entrada establece el informe para usar opciones y filtros que se utilizaron la última vez que se generó el informe.

El campo **Usar valores predeterminados de** proporciona una manera rápida y confiable de generar informes coherentes que contienen los datos correctos. Después de seleccionar una entrada, puede cambiar cualquiera de las opciones y filtros antes de obtener una vista previa o imprimir el informe. Los cambios que realice no se guardarán en la entrada de configuración predefinida que haya seleccionado, sino que se guardarán en la entrada **Últimas opciones y filtros utilizados**.

>[!NOTE]
> La configuración predefinida normalmente la configura y gestiona un administrador. Si desea obtener más información, consulte [Administrar la configuración guardada para informes y trabajos por lotes](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Especificación de los datos que se van a incluir en los informes

Utilice los campos de **Opciones** y **Filtros** para cambiar el límite de la información que desea en el informe. Los filtros se establecen en un informe de la misma manera que en las listas. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La sección **Filtrar lista por** en una página de solicitud proporciona una capacidad de filtrado genérico para los informes. Estos filtros son opcionales.
>
> Algunos informes ignorarán estos filtros, lo que significa que no importa qué filtro se establezca en la sección **Filtrar lista por** puesto que la salida del informe es la misma. No es posible proporcionar una lista de los campos que se ignoran en los informes, por lo que tendrá que experimentar con los filtros cuando los use.
>
> **Ejemplo**: Cuando utilice el trabajo por lotes **Crear recordatorios**, se ignorará un filtro para el campo **Movs. clientes** del **Nivel últim. record. emitid.** porque los filtros están fijos para ese trabajo por lotes.

## <a name="previewing-a-report"></a>Vista preliminar de un informe

La vista previa de un informe le permite ver cómo quedará el informe antes de imprimirlo. La vista previa no se basa en la impresora seleccionada en el campo **Impresora** en la página de solicitud. Está controlado por el navegador. Después de obtener una vista previa, puede volver a la página de solicitud y realizar cambios en las opciones y filtros según sea necesario.

Para obtener una vista previa de un informe, elija el botón **Vista previa** o **Vista previa y cierre** en la página de solicitud de informe. El botón que se muestra depende del informe, por lo que algunos informes tienen el botón **Vista previa**, mientras que otros tienen un botón **Vista previa y cierre**. Ambos botones abrirán una vista previa del informe. La diferencia es que **Vista previa** mantiene abierta la página de solicitud, para que pueda volver a ella, realizar cambios, obtener otra vez una vista previa o imprimir. Con **Vista previa y cierre**, la página de solicitud se cierra, por lo que tendrá que volver a abrir el informe para realizar cambios o imprimirlo.

> [!NOTE]
> Si usa el lanzamiento de versiones 1 de Business Central 2020 o anterior, solo hay un botón **Vista previa** que cierra la página de solicitud en la vista previa, como se describe para **Vista previa y cierre**.

### <a name="working-with-the-preview"></a>Trabajo con la vista previa

En la versión preliminar, use la barra de menú en la versión preliminar para:

- Desplazarse a través de las páginas
- Acercar y alejar la imagen
- Cambiar el tamaño para que encaje en la página
- Seleccionar texto

    Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[prod_short](includes/prod_short.md)] o Microsoft Word.  Con un mouse, por ejemplo, presione y mantenga pulsado donde desee empezar. Luego mueva el mouse para seleccionar una o más palabras, oraciones o párrafos. Pulse el botón derecho del ratón y seleccione **Copiar**. A continuación, puede pegar el texto seleccionado donde quiera.
- Desplazar lateralmente el documento

    Puede mover el área visible del informe en cualquier dirección para ver otras áreas o el informe. La panorámica es útil cuando se ha ampliado para ver detalles.  Con el ratón, por ejemplo, mantenga pulsado el botón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón.

- Descargue a un archivo PDF en su ordenador o su red.
- Imprimir

## <a name="saving-a-report-to-a-file"></a>Guardar un informe en un archivo

Puede guardar un informe en un documento PDF, un documento de Microsoft Word o una hoja de cálculo de Microsoft Excel seleccionando el botón **Enviar a** y luego hacer su selección.

### <a name="send-to-excel"></a>Enviar a Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Hay dos opciones para guardar los resultados del informe como hoja de trabajo en un libro de Excel: **Documento de Microsoft Excel (datos y diseño)** y **Documento de Microsoft Excel (solo datos)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Documento de Microsoft Excel (datos y diseño)](#tab/data-and-layout)

Esta opción solo está disponible para informes que utilizan un diseño RDLC. Exporta los resultados del informe con el diseño RDLC aplicado. Utilice esta opción si desea exportar los datos una vez y solo desea realizar cambios menores en su apariencia, como la fuente y el esquema de color.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Documento de Microsoft Excel (solo datos)](#tab/data-only)

La opción **Documento de Microsoft Excel (solo datos)** exporta los resultados del informe y los criterios que se utilizaron para generarlos &mdash;pero no incluye el diseño del informe. El archivo de Excel incluirá el conjunto de datos completo, como datos sin procesar, organizados en filas y columnas. Se incluyen todas las columnas de datos del conjunto de datos del informe, independientemente de si se utilizan en el diseño del informe.  Utilice esta opción cuando desee:

- Realizar un análisis ad hoc de los datos. Por ejemplo, puede filtrar los datos y utilizar Power Pivot para mostrarlo.

  Cada vez que exporta resultados, se crea una nueva hoja de trabajo. Utilizando la opción **Documento de Microsoft Excel (solo datos)**, puede ejecutar el mismo informe y reutilizar los cambios de formato. Por ejemplo, para Power Pivot puede ejecutar el informe nuevamente por otro período de tiempo, copiar los resultados en la hoja de trabajo y luego actualizar la hoja de trabajo. También puede buscar una aplicación de generación de informes en [AppSource](https://appsource.microsoft.com/).
- Inspeccione el conjunto de datos del informe cuando cree o modifique diseños de informes personalizados.

  Para obtener información sobre cómo crear diseños de informes personalizados, consulte [Creación o modificación de diseños de informes personalizados](ui-how-create-custom-report-layout.md)
- Diagnostique problemas de datos en informes.

##### <a name="for-administrators"></a>Para administradores

- **Documento de Microsoft Excel (solo datos)** se introdujo como característica opcional en 2021 lanzamiento de versiones 1, actualización 18.3. Para dar acceso a los usuarios a esta función, habilite la acutalización de características **Guardar el conjunto de datos del informe en documento de Microsoft Excel** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management). En 2021 lanzamiento de versiones 2, esta característica se hace permanente, por lo que no tendrá que habilitarla.

- Las cuentas de usuario necesitarán el permiso **<!--Export Report Dataset To Excel-->Permitir que la acción exporte el conjunto de datos de informe a Excel**, que puede solicitar mediante el conjunto de permisos **Herramientas de resolución de problemas** o **Exportar informe a Excel**.  

- No puede exportar un informe que tenga más de 1 048 576 filas o 16 384 columnas.

    > [!NOTE]
    > Con Business Central local, el número máximo de filas exportadas puede ser incluso menor. Business Central Server incluye una opción de configuración, denominada **Filas de datos máximas permitidas para enviar a Excel**, para disminuir el límite del valor máximo. Para más información, vea [Configuración de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) o comuníquese con su administrador.

##### <a name="for-developers-and-advanced-users"></a>Para desarrolladores y usuarios avanzados

La opción **Documento de Microsoft Excel (solo datos)** exporta todas las columnas, incluidas las que contienen filtros e instrucciones de formato para otros valores. A continuación se muestran algunos puntos de interés:

- Los datos binarios de un campo, como una imagen, no se exportan.

  En las columnas que contienen datos binarios, los campos incluirán el texto **Datos binarios ({0} bytes)**, donde **{0}** indica el número de bytes.
- A partir de Business Central 2021 lanzamiento de versiones 2, el archivo de Excel también incluye el hoja de cálculo **Metadatos de informe**.

  Esta hoja de cálculo muestra los filtros aplicados al informe y las propiedades generales del informe, como el nombre, el ID y los detalles de la extensión. Los filtros se muestran en la columna **Filtro (DataItem::Table::FilterGroupNo::FieldName)**. Los filtros de esta columna incluyen filtros establecidos en la página de solicitud del informe. También incluye filtros definidos en código AL, por ejemplo, por la [propiedad DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) y la [propiedad DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Para obtener más información sobre el diseño de informes, consulte [Resumen del informe](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Algunos informes exportan números como texto, lo que le impide realizar cálculos o utilizar Power Pivot en las celdas de la hoja de cálculo de Excel. Después de exportar, es una buena idea verificar los números en la hoja de cálculo. Si desea hacer análisis y gráficos con los números, cambie el formato de las celdas relevantes de **Texto** a **Número**. Para obtener más información sobre cómo formatear números en celdas, vea este vídeo [Dar formato a números en celdas en Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

### <a name="microsoft-word-document"></a>Microsoft Word Documento
Use la opción **Documento de Microsoft Word** para generar un informe como un documento de Word.  

> [!NOTE]
> Puede especificar el diseño que se utilizará para cada informe en la página **Selección de informe** en el campo **Diseño seleccionado**. La configuración predeterminada para los informes es **RDLC (incorporado)**, que produce informes en el mismo diseño, o uno similar, que el diseño **Documento de Microsoft Word**. Sin embargo, la diferencia clave es si desea generar uno o varios documentos de informe. Para documentos individuales, puede utilizar la opción RDLC (integrada). Para varios documentos, configure el **Documento de Microsoft Word** como diseño predeterminado para el informe. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Programar un informe para que se ejecute

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir el botón **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha. A continuación, el informe se agrega a la cola de proyectos y se ejecutará en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

Cuando programe la ejecución de un informe, puede especificar que debe ejecutarse todos los jueves configurando el campo **Fórmula de fecha de la próxima ejecución** en *D4*, por ejemplo. Para obtener más información, vea [Uso de fórmulas de fecha](ui-enter-date-ranges.md#using-date-formulas).  

Puede elegir guardar el informe en un archivo (como Excel, Word o PDF), imprimirlo o solo generar el informe. Si elige guardar el informe en un archivo, el informe procesado se envía al área **Bandeja de entrada de informes** en el área de trabajo, donde puede verlo.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Imprimir un informe

Para imprimir un informe, elija el botón **Imprimir** en la página de solicitud o en la barra de menú de la página **Vista previa**.

### <a name="printer"></a><a name="Printer"></a>Impresora

El campo **Impresora** de la página de solicitud muestra el nombre de la impresora a la que se enviará el informe. Para cambiar una impresora, simplemente seleccione la impresora de la lista.

> [!NOTE]
> **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará una experiencia estándar, donde puede elegir una impresora local conectada a su dispositivo. **(Manejado por el navegador)** no está disponible en la aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)] o la aplicación para Microsoft Teams.

> [!TIP]
> La impresora que se ha seleccionado para usted de forma predeterminada está configurada en la página **Selecciones de impresora**. Para obtener información sobre cómo cambiar la impresora predeterminada, consulte [Para seleccionar qué impresoras imprimen qué informes](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Impresión de informes en tailandés

Específicamente para la versión tailandesa de [!INCLUDE[prod_short](includes/prod_short.md)], el botón **Imprimir** no puede imprimir correctamente los informes como sonsecuencia de las limitaciones del servicio que genera el archivo PDF imprimible. En su lugar, puede abrir el informe en Word y luego guardarlo como un PDF imprimible.  

También puede pedir a su administrador que cree un diseño de informe de Word para los informes más utilizados. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Cambio de diseños de informe

El diseño de informe controla lo que se muestra en un informe, cómo se organiza y cómo está diseñado. Si desea cambiar a otro diseño distinto, consulte [Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md). Pero, si desea personalizar su propio diseño del informe, vea [Crear y editar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Opciones avanzadas

Los campos de **Avanzado** establecen limitaciones en el informe generado para controlar los recursos de la impresora. Por lo general, no tendrá que cambiar esta configuración, a menos que tenga un informe grande. Si un informe supera estas limitaciones cuando intenta obtener una vista previa o imprimir, aparece un mensaje que le indica qué limitación se superó. A continuación, puede cambiar la configuración para adaptarla a su informe. Sin embargo, cada campo tiene un valor máximo que debe conocer:

|Campo|Valor máximo|
|-----|-------------|
|Tiempo de representación máximo|12:00:00|
|Número máximo de filas|1000000|
|Número máximo de documentos|500|

> [!NOTE]
> Los valores máximos pueden ser diferentes para [!INCLUDE[prod_short](includes/prod_short.md)] local y un administrador puede cambiarlos. Para obtener más información, consulte [Configuración de Business Central Server: informes](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Para obtener una descripción general de las limitaciones de los informes [!INCLUDE[prod_short](includes/prod_short.md)] en línea, consulte [Límites operativos](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Consulte también

[Configuración de impresoras](ui-specify-printer-selection-reports.md)  
[Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]