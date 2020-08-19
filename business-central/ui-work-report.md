---
title: Programar un informe para ejecutarlo en una fecha y hora específicos | Documentos de Microsoft
description: Obtenga información sobre cómo introducir un informe en una cola de proyectos y programarlo para que se procesa en una fecha y hora específicas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 11c3fa284a457db1de272a3d92ebc7fc873ad933
ms.sourcegitcommit: 99cecd005f8ede70e9a3d163a457fcb9aadb6843
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2020
ms.locfileid: "3549897"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Trabajar con informes, trabajos por lotes y XMLports

Un informe recoge la información basada en un conjunto determinado de criterios, y organiza y muestra la información en un formato fácil de leer que puede imprimir o guardar como un archivo. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente la información en relación con el contexto de la página que va a usar. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales, estadísticas de ventas, etc.

Los trabajos por lotes y XMLports realizan más o menos lo mismo que los informes pero con el objetivo de realizar un proceso o exportar datos. Por ejemplo, el trabajo por lotes **Crear recordatorios** crear documentos de recordatorio para los clientes que tienen pagos vencidos.  

> [!NOTE]
> Este tema hace referencia principalmente al "informe", pero se aplica información similar a los trabajos por lotes y XMLports.

Puede buscar informes en la ficha **Informes** de las páginas seleccionadas, o utilizar búsquedas ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") para buscar informes por nombre.

## <a name="specifying-the-data-to-include-in-reports"></a>Especificación de los datos que se van a incluir en los informes
Cuando abre un informe, un trabajo por lotes o XMLport, normalmente se le presenta una página de solicitud donde se establecen varias opciones y filtros que determinan qué se debe incluir en el informe.

Los filtros se establecen en un informe de la misma manera que en las listas. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> La sección **Filtrar lista por** en una página de solicitud proporciona una capacidad de filtrado genérico para los informes. Estos filtros son opcionales.
>
> Algunos informes ignorarán estos filtros, lo que significa que no importa qué filtro se establezca en la sección **Filtrar lista por** puesto que la salida del informe es la misma. No es posible proporcionar una lista de los campos que se ignoran en los informes, por lo que tendrá que experimentar con los filtros cuando los use.
>
> **Ejemplo**: Cuando utilice el trabajo por lotes **Crear recordatorios**, se ignorará un filtro para el campo **Movs. clientes** del **Nivel últim. record. emitid.** porque los filtros están fijos para ese trabajo por lotes.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Uso de la configuración guardada
La página de solicitud puede incluir la sección **Configuración guardada** que contiene una o más entradas en el cuadro **Utilizar el valor predeterminado desde**. Una configuración guardada es básicamente un grupo predefinido de opciones y filtros que puede aplicar al informe antes de previsualizar o enviar el informe a un archivo. La configuración guardada que se denomina **Filtros y opciones usados por última vez** está siempre disponible. Esta entrada establece el informe debe utilizar opciones y filtros que se utilizaron la última vez que se usó.

El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos. Después de configurar el cuadro **Utilizar el valor predeterminado desde** como una entrada de configuración guardada, puede cambiar cualquiera de las opciones y filtros antes de obtener una vista previa o guardar el informe. Los cambios que realice no se guardarán en la entrada de configuración guardada que haya seleccionado, sino que se guardarán en la entrada **Últimas opciones y filtros utilizados**.

>[!NOTE]
>Si es administrador, puede crear y administrar la configuración guardada para informes de todos los usuarios. Para obtener más información, consulte [Administrar configuraciones guardadas para informes y trabajos por lotes](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Vista preliminar de un informe

Elija el botón **Vista previa** para ver el informe en la página de solicitud del informe. Use la barra de menú en la vista previa del informe para:

- Desplazarse a través de las páginas
- Acercar y alejar la imagen
- Cambiar el tamaño para que encaje en la página
- Seleccionar texto

    Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[d365fin](includes/d365fin_md.md)] o Microsoft Word.  Con un ratón, por ejemplo, presione y mantenga pulsado donde desee empezar y, a continuación, mueve el ratón para seleccionar una o más palabras, frases o párrafos. A continuación, puede pulsar el botón derecho del ratón y seleccionar **Copiar**. A continuación, puede pegar el texto seleccionado donde quiera.
- Desplazar lateralmente el documento

    Puede mover el área visible del informe en cualquier dirección para ver otras áreas o el informe. Esto es útil cuando se ha ampliado para ver detalles.  Con el ratón, por ejemplo, mantenga pulsado el botón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón.

- Descargue a un archivo PDF en su ordenador o su red.
- Imprimir

## <a name="saving-a-report"></a>Cómo guardar un informe
Puede guardar un informe en un documento PDF, un documento de Microsoft Word o un documento de Microsoft Excel seleccionando el botón **Enviar a** y luego hacer su selección.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Programar un informe para que se ejecute

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir el botón **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha. A continuación, el informe se agrega a la cola de proyectos y se ejecutará en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

Cuando programe la ejecución de un informe, puede especificar que debe ejecutarse todos los jueves configurando el campo **Fórmula de fecha de la próxima ejecución** en *D4*, por ejemplo. Para obtener más información, vea [Uso de fórmulas de fecha](ui-enter-date-ranges.md#using-date-formulas).  

Puede elegir guardar el informe procesado en un archivo, como archivo Excel, Word o PDF, imprimirlo en una impresora seleccionada o solo procesarlo. Si elige guardar el informe en un archivo, el informe procesado se envía al área **Bandeja de entrada de informes** en el área de trabajo, donde puede verlo.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Imprimir un informe

Un informe se imprime eligiendo el botón **Imprimir** en la página de solicitud de informe o en la barra de menú en la página **Vista previa**.

### <a name="printer-selection"></a>Selección de impresora

El informe se imprime en la impresora que se muestra en el campo **Impresora seleccionada** en la página de solicitud de informe. No puede cambiar la impresora desde esta página.

La impresora seleccionada se configura en la página **Selecciones de impresora** o es la impresora predeterminada configurada en la página **Gestión de impresoras**. Si desea utilizar otra impresora, consulte [Configurar impresoras](ui-specify-printer-selection-reports.md).

Si no se especifica ninguna impresora en la página **Selecciones de impresora** ni se establece como predeterminada en la página **Gestión de impresoras**, se utiliza la función de impresión del navegador. En este caso, **Navegador** aparece en el campo **Impresora seleccionada** en la página de solicitud de informe. 

### <a name="browser-printing"></a>Impresión en el navegador

Como [!INCLUDE[prodshort](includes/prodshort.md)] es un servicio en la nube, no puede llegar a las impresoras locales conectadas al equipo. Sin embargo, puede conectarse a impresoras habilitadas para la nube. En la versión genérica de [!INCLUDE[prodshort](includes/prodshort.md)], una impresora en la nube llamada **Impresora de correo electrónico** se instala como extensión y está lista para usar después de la configuración inicial.

Si no se instala y configura una impresora en la nube o si falla una impresora instalada, la impresión tendrá las opciones de impresión predeterminadas para el navegador.

> [!NOTE]
> Las opciones de impresión del navegador funcionan independientemente de [!INCLUDE[prodshort](includes/prodshort.md)]. Por lo tanto, cualquier configuración de impresora que pueda haberse configurado desde impresoras en [!INCLUDE[prodshort](includes/prodshort.md)] no se transfieren a las opciones de impresión del navegador.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Impresión de informes en tailandés
Específicamente para la versión tailandesa de [!INCLUDE[prodshort](includes/prodshort.md)], el botón **Imprimir** no puede imprimir correctamente los informes debido a las limitaciones del servicio que genera el archivo PDF imprimible. En su lugar, puede abrir el informe en Word y luego guardarlo como un PDF imprimible.  

Alternativamente, puede pedir a su administrador que cree un diseño de informe de Word para los informes más utilizados. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Cambio de diseños de informe
El diseño de informe controla lo que se muestra en un informe, cómo se organiza y cómo está diseñado. Si desea cambiar a otro diseño distinto, consulte [Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md). Pero, si desea personalizar su propio diseño del informe, vea [Crear y editar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Consulte también

[Configuración de impresoras](ui-specify-printer-selection-reports.md)  
[Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
