---
title: Ejecutar e imprimir informes en Business Central
description: Aprenda a introducir un informe un informe en una cola de proyectos y programarlo para que se procesa en una fecha y hora específicas.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 06/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="run-and-print-reports-in-business-central"></a>Ejecutar e imprimir informes en Business Central

Los informes le ayudan a recopilar y mostrar datos según criterios específicos. Organiza y presenta la información en un formato fácil de leer que puede imprimir o guardar como un archivo. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente información relada con el contexto de la página en la que está. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales, estadísticas de ventas, etc.

> [!NOTE]
> Los trabajos por lotes y XMLports hacen más o menos lo mismo que los informes, pero se usan más para procesar o exportar datos. Por ejemplo, el trabajo por lotes **Crear recordatorios** crear documentos de recordatorio para enviar a los clientes que tienen pagos vencidos. Este artículo hace referencia principalmente a "informes", pero se aplica información similar a los trabajos por lotes y XMLports.

## <a name="get-started"></a>Introducción

Puede encontrar informes en el menú **Informes** menú en páginas, listas y tarjetas seleccionadas. También puede usar la búsqueda ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"). para buscar informes por nombre. Para obtener una descripción general de los informes integrados que puede utilizar en [!INCLUDE[prod_short](includes/prod_short.md)], ordenados por categorías, vea [Informes disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Cuando elija un informe, normalmente verá una página de solicitud, con el título del nombre del informe, donde se establecen varias opciones y filtros que determinan qué datos se deben incluir. Las siguientes secciones explican cómo utilizar la página de solicitud para crear, obtener una vista previa e imprimir un informe.

## <a name="use-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a>Usar valores predeterminados&mdash;configuración predefinida

La mayoría de las páginas de solicitud del informe incluyen el campo **Usar valores predeterminados de**. Con este campo puede seleccionar configuraciones predefinidas para el informe, que configuran automáticamente opciones y filtros. Seleccione una entrada de la lista desplegable y verá que las opciones y los filtros en la página de solicitud del informe cambian en consecuencia.

La entrada denominada **Filtros y opciones usados por última vez** está siempre disponible. Esta entrada establece el informe para las usar opciones y filtros que utilizó la última vez que se generó el informe.

El campo **Usar valores predeterminados de** proporciona una manera rápida y confiable de generar informes coherentes que contienen los datos correctos. Después de seleccionar una entrada, puede cambiar cualquiera de las opciones y filtros antes de obtener una vista previa o imprimir el informe. Los cambios que realice no se guardarán en la entrada de configuración predefinida que haya seleccionado, sino que se guardarán en la entrada **Últimas opciones y filtros utilizados**.

> [!NOTE]
> La configuración predefinida normalmente la configura y gestiona un administrador. Más información en [Administrar configuraciones guardadas para informes y trabajos por lotes](reports-saving-reusing-settings.md).

## <a name="specify-the-data-to-include-in-a-report"></a>Especificar los datos que se van a incluir en un informe

Utilice los campos de **Opciones** y **Filtros** para cambiar o limitar la información que desea en el informe. Los filtros se establecen en un informe de la misma manera que en las listas. Obtenga más información en la sección [Filtrado](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La ficha desplegable **Filtrar** en un informe de solicitud proporciona una capacidad de filtrado genérico para los informes. Estos filtros son opcionales.
>
> Algunos informes ignorarán estos filtros, lo que significa que no importa qué filtro se establezca en la ficha desplegable **Filtro** puesto que la salida del informe es la misma. No es posible proporcionar una lista de los campos que se ignoran en los informes, por lo que tendrá que experimentar con los filtros cuando los use.
>
> **Ejemplo**: Cuando utilice el trabajo por lotes **Crear recordatorios**, se ignorará un filtro para el campo **Movs. clientes** del **Nivel últim. record. emitid.** porque los filtros están fijos para ese trabajo por lotes.

## <a name="preview-a-report"></a>Obtener una vista previa de un informe

Con la vista previa de un informe puede ver cómo quedará el informe antes de imprimirlo. La vista previa no se basa en la impresora seleccionada en el campo **Impresora** en la página de solicitud. Está controlado por el navegador. Después de obtener una vista previa, puede volver a la página de solicitud y realizar cambios en las opciones y filtros según sea necesario.

Las elecciones de vista previa en la página **Solicitud de informe** dependen del informe. Entonces, para algunos informes, puede seleccionar **Vista previa**, mientras que para otros la elección es **Vista previa y cerrar**. Ambas elecciones abrirán una vista previa del informe. La diferencia es que **Vista previa** mantiene abierta la página de solicitud, para que pueda volver a ella, realizar cambios, obtener otra vez una vista previa o imprimir. En comparación, con **Vista previa y cierre**, la página de solicitud se cierra, por lo que tendrá que volver a abrir el informe para realizar cambios o imprimirlo.

> [!NOTE]
> Si usa el lanzamiento de versiones 1 de Business Central 2020 o anterior, la única elección es **Vista previa** que cierra la página de solicitud en la vista previa, como se describe anteriormente para **Vista previa y cierre**.

### <a name="work-with-the-preview"></a>Trabajar con la vista previa

En la versión preliminar, use la barra de menú en la versión preliminar para:

- Desplazarse a través de las páginas
- Acercar y alejar la imagen
- Cambiar el tamaño para que encaje en la página
- Seleccionar texto
  
  Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[prod_short](includes/prod_short.md)] o Microsoft Word. Con un mouse, por ejemplo, seleccione el botón izquierdo del ratón y mantenga pulsado donde desee empezar. Deslice el ratón para seleccionar una o más palabras, oraciones o párrafos. Después seleccione el botón derecho del ratón y seleccione **Copiar**. Ahora puede pegar el texto seleccionado donde quiera.

- Desplazar lateralmente el documento
  
  Puede mover el área visible del informe en cualquier dirección para ver otras áreas del informe. La panorámica es útil cuando se ha ampliado para ver detalles. Con el ratón, por ejemplo, mantenga seleccionado el botón izquierdo del ratón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón para seleccionar una sección del informe.

- Descargue a un archivo PDF en su ordenador o su red.
- Imprimir

## <a name="save-a-report-to-a-file"></a>Guardar un informe en un archivo

Puede guardar un informe en un documento PDF, un documento de Microsoft Word, hoja de Microsoft Excel o documento XML seleccionando **Enviar a** y luego hacer su selección. Un archivo de diseño se descarga en su equipo.

Si su organización ha configurado OneDrive para las funciones del sistema, en lugar de descargarse, los libros de trabajo de Excel y los documentos de Word se abren en su navegador usando Excel o Word para la web.

> [!TIP]
> Las opciones **Documento de Microsoft Excel (solo datos)** y **Documento XML** son principalmente para propósitos avanzados. Normalmente usará estas opciones para realizar un análisis detallado de los datos. Para más información, consulte [Analizar datos de informes con Excel y XML](report-analyze-excel.md).
>
> También puede usar **Documento de Microsoft Excel (solo datos)** para crear nuevos diseños de Excel para un informe determinado. Más información en [Trabajar con diseños de Excel](ui-excel-report-layouts.md).  

## <a name="schedule-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a>Programar un informe para que se ejecute más tarde o periódicamente

Puede programar un informe único o periódico para ejecutarlo en una fecha y hora específicos. Los informes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Seleccione la opción **Programa** tras seleccionar **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha. El informe se agrega a la cola de proyectos y se ejecuta en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Obtenga más información en [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

Cuando programe la ejecución de un informe, puede especificar, por ejemplo, que debe ejecutarse todos los jueves configurando el campo **Fórmula de fecha de la próxima ejecución** en *D4*. Para obtener más información, vea la sección [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).  

Puede guardar el informe en un archivo (como Excel, Word o PDF), imprimirlo o solo generar el informe. Si guarda el informe en un archivo, el informe procesado se envía a la página **Bandeja de entrada de informes** en el área de trabajo, donde puede verlo. Más información en [Compartir y exportar informes con la bandeja de entrada de informes](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a>Administrar informes recurrentes programados

Los trabajos por lotes generan informes programados que se administran en la página **Entradas de la cola de trabajos**. Puede ver el estado y otra información de cada informe en la página, pausar/reanudar el trabajo por lotes del informe y generar el informe a pedido.

Desde la página **Entradas de la cola de trabajos**, también puede cambiar algunos parámetros del informe, como el tipo de archivo de salida, la recurrencia, la fecha de ejecución y las horas de inicio y finalización. Sin embargo, antes de editar un informe programado existente, es necesario poner en espera la cola de trabajo del informe:

1. Seleccione el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de cola de proyectos** y luego seleccione el vínculo relacionado.  
2. En la página **Movs. cola proyecto**, seleccione el informe deseado.
3. Seleccione la acción **Establecer en espera**.
4. Abra y edite el informe programado seleccionando su estado (*En espera*).

Después de editar las opciones del informe, repita los primeros dos pasos y luego seleccione la acción **Establecer estado en Listo** para reanudar la generación del informe.

Obtenga más información sobre la gestión de colas de trabajos en [Utilice las colas de trabajos para programar tareas](admin-job-queues-schedule-tasks.md).  

## <a name="print-a-report"></a><a name="PrintReport"></a>Imprimir un informe

Para imprimir un informe, seleccione **Imprimir** en el informe de solicitud o en la barra de menú de la página **Vista previa**.

Cuando un informe use un diseño de Excel, no verá el campo **Impresora**, o los botones **Imprimir** o **Vista previa**. En su lugar, hay una opción de **Descargar**. Para imprimir, seleccione **Descargar** y, a continuación, abra el archivo descargado en Excel e imprima desde allí.

### <a name="printer"></a><a name="Printer"></a>Impresora

El campo **Impresora** de la página de solicitud muestra el nombre de la impresora a la que se enviará el informe. Para cambiar una impresora, simplemente seleccione la impresora de la lista.

> [!NOTE]
> La opción **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará unos pasos de impresión estándar, donde puede elegir una impresora local conectada a su equipo. La opción **(Manejado por el navegador)** no está disponible en la aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)] o la aplicación para Microsoft Teams.

> [!TIP]
> La impresora que se ha seleccionado para usted de forma predeterminada está configurada en la página **Selecciones de impresora**. Obtenga más información sobre cómo puede cambiar la impresora predeterminada en la sección [Configurar impresoras predeterminadas](ui-specify-printer-selection-reports.md#default).

### <a name="print-reports-in-thai"></a>Imprimir informes en tailandés

Específicamente para la versión tailandesa de [!INCLUDE[prod_short](includes/prod_short.md)], el botón **Imprimir** no puede imprimir correctamente los informes como sonsecuencia de las limitaciones del servicio que genera el archivo PDF imprimible. En su lugar, puede abrir el informe en Word y luego guardarlo como un PDF imprimible.  

También puede pedir a su administrador que cree un diseño de informe de Word para los informes más utilizados. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).  

## <a name="switch-the-report-layout"></a>Cambiar el diseño del informe

El diseño de informe controla lo que se muestra en un informe, cómo se organiza y cómo está diseñado. Existen varias formas de cambiar el diseño:

- Cuando esté configurando para ejecutar un informe, verá el diseño actual en el campo **Diseño de informe** en la página de solicitud. Para cambiar temporalmente a un diseño distinto, seleccione el campo **Diseño del informe**, después seleccione en la lista de diseños disponibles para el informe.
- Para cambiar el diseño predeterminado utilizado por un informe, vaya a las páginas **Diseños de informes** o **Selección de diseño de informe**.

Más información en [(Versión heredada) Establecer el diseño utilizado por un informe](ui-set-report-layout.md). Pero, si desea personalizar su propio diseño del informe, vea [Empezar a crear diseños](ui-get-started-layouts.md).

## <a name="change-language-and-format-of-numbers-dates-and-times"></a>Cambiar idioma y formato de números, fechas y horas

De forma predeterminada, el idioma del texto y el formato de los números, las fechas y las horas en un informe se basan en su idioma de trabajo y configuración regional, que se definen en la página **Mi configuración**. Sin embargo, puede cambiar el idioma y la región de formato caso por caso cuando obtenga una vista previa, imprima o envíe un informe. En la página de solicitud, configure las opciones de **Idioma** y **Región de formato** que desee. También puede especificar el formato de idioma y región que se utilizará de forma predeterminada para los clientes y proveedores en sus páginas de tarjetas.

Dependiendo de dónde haya especificado la configuración de idioma y formato, [!INCLUDE [prod_short](includes/prod_short.md)] determina la configuración a utilizar en el siguiente orden:

1. La configuración que especifica cuando genera un informe.
2. La configuración especificada en el documento, que proviene de la configuración del cliente o proveedor.
3. La configuración especificada en el objeto Informe AL.
4. La configuración definida en Mi configuración.

Para obtener más información sobre la página **Mi configuración**, consulte [Cambiar la configuración básica](ui-change-basic-settings.md#region).

## <a name="advanced-options"></a>Opciones avanzadas

Los campos de la ficha desplegable **Avanzado** establecen limitaciones en el informe generado para controlar los recursos de la impresora. Por lo general, no tendrá que cambiar esta configuración, a menos que tenga un informe grande. Si un informe supera estas limitaciones cuando intenta obtener una vista previa o imprimir, un mensaje indica qué limitación se superó. A continuación, puede cambiar la configuración para adaptarla a su informe. Sin embargo, cada campo tiene un valor máximo que debe conocer:

|Campo|Valor máximo|
|-----|-------------|
|Tiempo de representación máximo|12:00:00|
|Número máximo de filas|1000000|
|Número máximo de documentos|500|

> [!NOTE]
> Los valores máximos pueden ser diferentes para [!INCLUDE[prod_short](includes/prod_short.md)] local y un administrador puede cambiarlos. Más información en la sección [Configuración de Business Central Server: informes](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Para obtener una descripción general de las limitaciones de informe en [!INCLUDE[prod_short](includes/prod_short.md)] en línea, consulte [Límites operativos](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Consulte también .

- [Informes disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
- [Usar informes en el trabajo diario](reports-use-reports.md)  
- [Descripción general de Inteligencia empresarial e informes](reports-bi-reporting.md)  
- [Configuración de impresoras](ui-specify-printer-selection-reports.md)  
- [Ejecutar trabajos por lotes y XMLports](ui-how-run-batch-jobs.md)  
- [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md)  
- [Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
- [Inteligencia empresarial financiera](bi.md)  
- [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
