---
title: "Programar un informe para ejecutarlo en una fecha y hora específicos | Documentos de Microsoft"
description: "Obtenga información sobre cómo introducir un informe en una cola de proyectos y programarlo para que se procesa en una fecha y hora específicas."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: badcdee3dfa5bec3c2462149989cf9d4fb5af2a0
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-reports"></a>Trabajar con informes
Un informe recoge la información basada en un conjunto determinado de criterios, y organiza y muestra la información en un formato fácil de leer, imprimible. Existen numerosos informes a la que se accede en la aplicación. Los informes proporcionan normalmente la información en relación con el contexto de la página que va a usar. Por ejemplo, la página **Cliente** incluye los informes para los 10 clientes principales y sus estadísticas de ventas, entre otros datos.

Puede buscar informes en la ficha **Informes** de las páginas seleccionadas, o utilizar búsquedas para buscar informes por nombre. Cuando se abre un informe, se le presenta con una página en la que puede especificar información (opciones y filtros) que determine lo que desea incluir en el informe. Por ejemplo, según del informe, puede especificar un intervalo de fechas, un registro específico como un cliente, o un orden de clasificación.

## <a name="previewing-a-report"></a>Vista preliminar de un informe
Seleccione **Vista previa** para ver el informe en el explorador de Internet. Señale una zona del informe para mostrar la barra de menús.  

![Barra de herramientas Vista preliminar del informe](media/report_viewer.png "barra de herramientas Vista preliminar del informe").

Utilice la barra de menús para:

-   Desplazarse a través de las páginas
-   Acercar y alejar la imagen
-   Cambiar el tamaño para que encaje en la ventana
-   Seleccionar texto

    Puede copiar el texto de un informe y, a continuación pegarlo en algún otro lugar, como una página de [!INCLUDE[d365fin](includes/d365fin_md.md)] o en Microsoft Word.  Con un ratón, por ejemplo, presione y mantenga pulsado donde desee empezar y, a continuación, mueve el ratón para seleccionar una o más palabras, frases o párrafos. A continuación, puede pulsar el botón derecho del ratón y seleccionar **Copiar**. Puede pegar el texto seleccionado donde quiera.
-   Desplazar lateralmente el documento

    Puede mover el área visible del informe en cualquier dirección para ver otras áreas o el informe. Esto es útil cuando se ha ampliado para ver detalles.  Con el ratón, por ejemplo, mantenga pulsado el botón en cualquier parte de la vista previa del informe y, a continuación, mueva el ratón.

-   Descargue a un archivo PDF en su ordenador o su red.


## <a name="saving-a-report"></a>Cómo guardar un informe
Puede guardar un informe en un documento PDF, un documento de Microsoft Word o un documento de Microsoft Excel seleccionando **Enviar a** y luego hacer su selección. 

## <a name="ScheduleReport"></a> Programar un informe para que se ejecute
Puede programar un informe para ejecutarlo en una fecha y hora específicos. Los informes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Puede elegir guardar el informe procesado en un archivo, como archivo Excel, Word o PDF, imprimirlo en una impresora seleccionada o solo procesarlo. Si elige guardar el informe en un archivo, el informe procesado se envía al área **Bandeja de entrada de informes** en la página Inicio, donde puede verlo.

Puede programar un informe cuando abra un informe. Puede elegir la acción **Programar** y, a continuación, introducir información como la impresora, la hora y la fecha. A continuación, el informe se agrega a la cola de proyectos y se ejecutará en el momento especificado. Cuando se procese el informe, el elemento se eliminará de la cola de proyectos. Si guardó el informe procesado en un archivo, estará disponible en el área **Bandeja de entrada de informes**.

## <a name="PrintReport"></a>Imprimir un informe
Si desea imprimir un informe tiene que descargarlo como documento PDF, Word o Excel, elija primero el botón **Enviar a**. Ahora puede abrir el documento del informe inmediatamente e imprimirlo, o guardarlo e imprimirlo más adelante.

## <a name="using-saved-settings"></a>Uso de la configuración guardada
Un informe puede incluir uno o más movimientos en la casilla **Configuración guardada** . *Configuración guardada* es básicamente un grupo predefinido de opciones y filtros que puede aplicar al informe antes de previsualizar o enviar el informe a un archivo. El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos.

La configuración guardada que se denomina **Filtros y opciones usados por última vez** está siempre disponible. Este movimiento establece el informe debe utilizar opciones y filtros que se utilizaron la última vez que se vio.

>[!NOTE]
>Como administrador, puede crear y administrar la configuración guardada para informes de todos los usuarios. Para obtener más información, consulte [Administrar configuración guardada en los informes](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Cambiar el diseño y el aspecto de un informe
El diseño de informe controla lo que se muestra en un informe, cómo se organiza y cómo está diseñado. Si desea cambiar a otro diseño distinto, consulte [Procedimiento: Cambiar el diseño que se utiliza actualmente en un informe](ui-how-change-layout-currently-used-report.md). Pero, si desea personalizar su propio diseño del informe, vea [Procedimiento: Crear y editar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Consulte también
[Especificar selección de impresora para informes](ui-specify-printer-selection-reports.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

