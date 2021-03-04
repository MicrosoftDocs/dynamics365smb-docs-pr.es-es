---
title: Programar un informe para ejecutarlo en una fecha y hora específicos | Documentos de Microsoft
description: Obtenga información sobre cómo introducir un informe en una cola de proyectos y programarlo para que se procesa en una fecha y hora específicas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e4b1615ebf177db94e3dfb372809fa71ed2f1459
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760172"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Trabajar con informes, trabajos por lotes y XMLports

Un informe recoge la información basada en un conjunto determinado de criterios, y organiza y muestra la información en un formato fácil de leer que puede imprimir o guardar como un archivo. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente la información en relación con el contexto de la página que va a usar. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales, estadísticas de ventas, etc.

Los trabajos por lotes y XMLports realizan más o menos lo mismo que los informes pero con el objetivo de realizar un proceso o exportar datos. Por ejemplo, el trabajo por lotes **Crear recordatorios** crear documentos de recordatorio para los clientes que tienen pagos vencidos.  

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
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Especificación de los datos a incluir en los informes

Utilice los campos de **Opciones** y **Filtros** para cambiar el límite de la información que desea en el informe. Los filtros se establecen en un informe de la misma manera que en las listas. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La sección **Filtrar lista por** en una página de solicitud proporciona una capacidad de filtrado genérico para los informes. Estos filtros son opcionales.
>
> Algunos informes ignorarán estos filtros, lo que significa que no importa qué filtro se establezca en la sección **Filtrar lista por** puesto que la salida del informe es la misma. No es posible proporcionar una lista de los campos que se ignoran en los informes, por lo que tendrá que experimentar con los filtros cuando los use.
>
> **Ejemplo**: Cuando utilice el trabajo por lotes **Crear recordatorios**, se ignorará un filtro para el campo **Movs. clientes** del **Nivel últim. record. emitid.** porque los filtros están fijos para ese trabajo por lotes.

## <a name="previewing-a-report"></a>Vista preliminar de un informe

La vista previa de un informe le permite ver cómo quedará el informe antes de imprimirlo. La vista previa presentará el informe basado en la [impresora](#Printer) que se muestra en el campo **Impresora** de la página de solicitud. Después de obtener una vista previa, puede volver a la página de solicitud y realizar cambios en las opciones y filtros según sea necesario.

Para obtener una vista previa de un informe, elija el botón **Vista previa** o **Vista previa y cierre** en la página de solicitud de informe. El botón que se muestra depende del informe, por lo que algunos informes tienen el botón **Vista previa**, mientras que otros tienen un botón **Vista previa y cierre**. Ambos botones abrirán una vista previa del informe. La diferencia es que **Vista previa** mantiene abierta la página de solicitud, para que pueda volver a ella, realizar cambios, obtener otra vez una vista previa o imprimir. Con **Vista previa y cierre**, la página de solicitud se cierra, por lo que tendrá que volver a abrir el informe para realizar cambios o imprimirlo.

> [!NOTE]
> Si usa el lanzamiento de versiones 1 de Business Central 2020 o anterior, solo hay un botón **Vista previa** que cierra la página de solicitud en la vista previa, como se describe para **Vista previa y cierre**.

### <a name="working-with-the-preview"></a>Trabajo con la vista previa

En la versión preliminar, use la barra de menú en la versión preliminar para:

- Desplazarse a través de las páginas
- Acercar y alejar la imagen
- Cambiar el tamaño para que encaje en la página
- Seleccionar texto

    Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[prod_short](includes/prod_short.md)] o Microsoft Word.  Con un ratón, por ejemplo, presione y mantenga pulsado donde desee empezar y, a continuación, mueva el ratón para seleccionar una o más palabras, frases o párrafos. Pulse el botón derecho del ratón y seleccione **Copiar**. A continuación, puede pegar el texto seleccionado donde quiera.
- Desplazar lateralmente el documento

    Puede mover el área visible del informe en cualquier dirección para ver otras áreas o el informe. La panorámica es útil cuando se ha ampliado para ver detalles.  Con el ratón, por ejemplo, mantenga pulsado el botón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón.

- Descargue a un archivo PDF en su ordenador o su red.
- Imprimir

## <a name="saving-a-report"></a>Cómo guardar un informe

Puede guardar un informe en un documento PDF, un documento de Microsoft Word o un documento de Microsoft Excel seleccionando el botón **Enviar a** y luego hacer su selección.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Programar un informe para que se ejecute

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir el botón **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha. A continuación, el informe se agrega a la cola de proyectos y se ejecutará en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

Cuando programe la ejecución de un informe, puede especificar que debe ejecutarse todos los jueves configurando el campo **Fórmula de fecha de la próxima ejecución** en *D4*, por ejemplo. Para obtener más información, vea [Uso de fórmulas de fecha](ui-enter-date-ranges.md#using-date-formulas).  

Puede elegir guardar el informe en un archivo, como un archivo Excel, Word o PDF, imprimirlo en una impresora seleccionada o solo generar el informe. Si elige guardar el informe en un archivo, el informe procesado se envía al área **Bandeja de entrada de informes** en el área de trabajo, donde puede verlo.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Imprimir un informe

Para imprimir un informe, elija el botón **Imprimir** en la página de solicitud o en la barra de menú de la página **Vista previa**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Impresora

El campo **Impresora** de la página de solicitud muestra el nombre de la impresora a la que se enviará el informe. **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará una experiencia estándar, donde puede elegir una impresora local conectada a su dispositivo.

No puede cambiar la impresora mediante el campo **Impresora**. Para cambiar la impresora, tendrás que ir a las páginas **Selecciones de impresora** o **Gestión de impresoras**. La configuración de la impresora suele ser una tarea del administrador. Si desea obtener más información, consulte [Configurar impresoras](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Impresión de informes en tailandés

Específicamente para la versión tailandesa de [!INCLUDE[prod_short](includes/prod_short.md)], el botón **Imprimir** no puede imprimir correctamente los informes como sonsecuencia de las limitaciones del servicio que genera el archivo PDF imprimible. En su lugar, puede abrir el informe en Word y luego guardarlo como un PDF imprimible.  

Alternativamente, puede pedir a su administrador que cree un diseño de informe de Word para los informes más utilizados. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).  

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