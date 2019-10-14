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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 709e444d185e6950d6367036db622b30c8062f25
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310617"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Trabajar con informes, trabajos por lotes y XMLports
Un informe recoge la información basada en un conjunto determinado de criterios, y organiza y muestra la información en un formato fácil de leer que puede imprimir o guardar como un archivo. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente la información en relación con el contexto de la página que va a usar. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales, estadísticas de ventas, etc.

Los trabajos por lotes y XMLports realizan más o menos lo mismo que los informes pero con el objetivo de realizar un proceso o exportar datos. Por ejemplo, el trabajo por lotes **Crear recordatorios** crear documentos de recordatorio para los clientes que tienen pagos vencidos.  

> [!NOTE]
> Este tema hace referencia principalmente al "informe", pero se aplica información similar a los trabajos por lotes y XMLports.

Puede buscar informes en la ficha **Informes** de las páginas seleccionadas, o utilizar búsquedas ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer") para buscar informes por nombre.

## <a name="specifying-the-data-to-include-in-reports"></a>Especificación de los datos que se van a incluir en los informes
Cuando abre un informe, un trabajo por lotes o XMLport, normalmente se le presenta una página de solicitud donde se establecen varias opciones y filtros que determinan qué se debe incluir en el informe.

Los filtros se establecen en un informe de la misma manera que en las listas. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#-filtering).

> [!Caution]
> La sección **Filtrar lista por** en una página de solicitud proporciona una capacidad de filtrado genérico para los informes. Estos filtros son opcionales.<br /><br /> Algunos informes ignorarán estos filtros, lo que significa que no importa qué filtro se establezca en la sección **Filtrar lista por** puesto que la salida del informe es la misma. No es posible proporcionar una lista de los campos que se ignoran en los informes, por lo que tendrá que experimentar con los filtros cuando los use.<br /><br />
**Ejemplo**: Cuando utilice el trabajo por lotes **Crear recordatorios**, se ignorará un filtro para el campo **Movs. clientes** del **Nivel últim. record. emitid.** porque los filtros están fijos para ese trabajo por lotes.

## <a name="SavedSettings"></a>Uso de la configuración guardada
La página de solicitud puede incluir la sección **Configuración guardada** que contiene una o más entradas en el cuadro **Utilizar el valor predeterminado desde**. Una configuración guardada es básicamente un grupo predefinido de opciones y filtros que puede aplicar al informe antes de previsualizar o enviar el informe a un archivo. La configuración guardada que se denomina **Filtros y opciones usados por última vez** está siempre disponible. Esta entrada establece el informe debe utilizar opciones y filtros que se utilizaron la última vez que se usó.

El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos. Después de configurar el cuadro **Utilizar el valor predeterminado desde** como una entrada de configuración guardada, puede cambiar cualquiera de las opciones y filtros antes de obtener una vista previa o guardar el informe. Los cambios que realice no se guardarán en la entrada de configuración guardada que haya seleccionado, sino que se guardarán en la entrada **Últimas opciones y filtros utilizados**.

>[!NOTE]
>Si es administrador, puede crear y administrar la configuración guardada para informes de todos los usuarios. Para obtener más información, consulte [Administrar configuraciones guardadas para informes y trabajos por lotes](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Vista preliminar de un informe
Elija el botón **Vista previa** para ver el informe. Use la barra de menú en la vista previa del informe para:

-   Desplazarse a través de las páginas
-   Acercar y alejar la imagen
-   Cambiar el tamaño para que encaje en la página
-   Seleccionar texto

    Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[d365fin](includes/d365fin_md.md)] o Microsoft Word.  Con un ratón, por ejemplo, presione y mantenga pulsado donde desee empezar y, a continuación, mueve el ratón para seleccionar una o más palabras, frases o párrafos. A continuación, puede pulsar el botón derecho del ratón y seleccionar **Copiar**. A continuación, puede pegar el texto seleccionado donde quiera.
-   Desplazar lateralmente el documento

    Puede mover el área visible del informe en cualquier dirección para ver otras áreas o el informe. Esto es útil cuando se ha ampliado para ver detalles.  Con el ratón, por ejemplo, mantenga pulsado el botón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón.

-   Descargue a un archivo PDF en su ordenador o su red.
-   Imprimir

## <a name="saving-a-report"></a>Cómo guardar un informe
Puede guardar un informe en un documento PDF, un documento de Microsoft Word o un documento de Microsoft Excel seleccionando el botón **Enviar a** y luego hacer su selección.

## <a name="ScheduleReport"></a> Programar un informe para que se ejecute
Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir el botón **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha. A continuación, el informe se agrega a la cola de proyectos y se ejecutará en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

Puede elegir guardar el informe procesado en un archivo, como archivo Excel, Word o PDF, imprimirlo en una impresora seleccionada o solo procesarlo. Si elige guardar el informe en un archivo, el informe procesado se envía al área **Bandeja de entrada de informes** en el área de trabajo, donde puede verlo.

## <a name="PrintReport"></a>Imprimir un informe
Puede imprimir un informe desde el botón **Imprimir** en la página de opciones que aparece al abrir el informe o desde la barra de menús en Vista previa.  

### <a name="printing-reports-in-thai"></a>Impresión de informes en tailandés
Específicamente para la versión tailandesa de [!INCLUDE[prodshort](includes/prodshort.md)], el botón **Imprimir** no puede imprimir correctamente los informes debido a las limitaciones del servicio que genera el archivo PDF imprimible. En su lugar, puede abrir el informe en Word y luego guardarlo como un PDF imprimible.  

Alternativamente, puede pedir a su administrador que cree un diseño de informe de Word para los informes más utilizados. Para obtener más información, vea [Administrar diseños de informes y documentos](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Cambio de diseños de informe
El diseño de informe controla lo que se muestra en un informe, cómo se organiza y cómo está diseñado. Si desea cambiar a otro diseño distinto, consulte [Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md). Pero, si desea personalizar su propio diseño del informe, vea [Crear y editar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Consulte también
[Especificar selección de impresora para informes](ui-specify-printer-selection-reports.md)  
[Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
