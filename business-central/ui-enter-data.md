---
title: Cómo introducir datis eb campos | Documentos de Microsoft
description: Obtenga información sobre las características generales que le ayudan a introducir datos en los campos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "929078"
---
# <a name="entering-data"></a>Introducción de datos

Hay muchas características generales que le ayudan a introducir datos de forma más fácil, rápida y precisa. Las características generales para la introducción de datos se describen en este artículo.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Métodos abreviados de teclado

Hay varios métodos abreviados de teclado que le permiten trabajar "sin ratón" y acelerar la entrada de datos, especialmente con movimientos a gran escala y tareas de escritura repetitivas.

Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md). Algunos de los métodos abreviados se explican en este artículo.

## <a name="QuickEntry"></a>Acelerar la entrada de datos con la entrada rápida

La entrada rápida es una característica diseñada para la entrada de datos cuando se utiliza el teclado. La entrada rápida funciona en campos (como en las páginas de fichas) y en listas (filas y columnas). Es beneficiosa cuando se realizan tareas de escritura repetitivas que requieren la creación de varios registros en secuencia, como un lote de pedidos de venta o el registro de nuevos productos.

Es posible que ya esté familiarizado con el uso de la tecla Tab para navegar desde un campo de una página al siguiente campo editable. Una desventaja de usar Tab es que siempre va secuencialmente al siguiente campo. <!-- even if the field is non-editable or seldom filled it in.-->La entrada rápida le permite cambiar esta ruta. Con la entrada rápida, puede utilizar la tecla Entrar para navegar solo por los campos que le interesan, omitiendo los campos no editables y los campos que normalmente no rellena. Es posible que ya haya observado este comportamiento en algunas páginas. Esto se debe a que la aplicación ya designa los campos que se deben incluir al pulsar Entrar y los que se deben omitir. Puede personalizar la entrada rápida si personaliza su espacio de trabajo y optimiza la forma en que introduce los datos en cada página.

### <a name="how-quick-entry-works"></a>Cómo funciona la entrada rápida

Cada campo puede marcarse como *incluido en la entrada rápida* o como *excluido de la entrada rápida*. Los campos que se incluyen en la entrada rápida se incluirán en la ruta cuando pulse Entrar; los campos que se excluyen de la entrada rápida, no.

Cuando haya finalizado de rellenar un campo, pulse Entrar para confirmar los cambios e ir al siguiente campo. Si desea invertir la dirección y pasar al campo anterior, pulse Mayús+Entrar. Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de teclado de entrada rápida](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Sugerencias y trucos
A continuación se ofrece información útil sobre el uso de la entrada rápida.

- Está disponible para cualquier campo editable.
- También funciona en columnas y filas.
- No impide el acceso a otros elementos de una página, como las acciones. Se puede seguir accediendo a ellos utilizando Tab y Mayús+Tab.  
- Las fichas desplegables no tienen que expandir para que funcione la entrada rápida. Si el siguiente campo de entrada rápida se encuentra en una ficha desplegable contraída, esa ficha desplegable se expandirá automáticamente y el enfoque estará en el campo designado.
- La entrada rápida funciona independientemente de si los campos son obligatorios. Por lo tanto, es buena idea asegurarse de que los campos obligatorios se incluyan en la entrada rápida.
- De forma predeterminada, la mayoría de los campos se incluyen automáticamente en la entrada rápida. Por lo tanto, al principio, lo más probable es que su tarea sea excluir campos de la entrada rápida.

### <a name="how-to-change-quick-entry-fields"></a>Cómo modificar los campos de entrada rápida

Para cambiar los campos que se incluyen o se excluyen de la entrada rápida de una página, se utiliza la personalización.

1. Comience la personalización seleccionando el icono ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y **Personalizar**.
2. Seleccione un campo que desee modificar o, en las listas, seleccione la cabecera de columna correspondiente y, a continuación, seleccione **Incluir en entrada rápida** o **Excluir de entrada rápida**.

Para obtener más información sobre la personalización, consulte [Personalización del área de trabajo](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Campos obligatorios

Cuando se introducen datos en páginas, determinados campos aparecen marcados con un asterisco de color rojo. El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.  

Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página. El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.  

## <a name="finding-data-as-you-type"></a>Buscar datos al escribir

 Cuando comience a escribir caracteres en un campo, aparecerá una lista desplegable que muestra los posibles valores de campo. Esta lista cambia a medida que escriba caracteres adicionales y puede seleccionar el valor correcto cuando aparezca.  

 Muchos campos tienen un botón de flecha hacia abajo que puede elegir. Seleccione la flecha para desplegar una lista de datos que están disponibles para su introducción en el campo. El botón tiene dos funciones, según el tipo de campo:  

-   Búsqueda: muestra información de otra tabla, que puede introducir en el campo. Puede seleccionar un elemento de datos a la vez.  

-   Desplegable: muestra el conjunto de opciones que existe para el campo. Sólo puede seleccionar una de las opciones.  

## <a name="copying-and-pasting-fields-and-lines"></a>Copia y pegado de campos y líneas

Puede copiar una o más filas de una lista o un solo campo en una página y luego pegar lo que ha copiado en la misma página, otra página o un documento externo (como Microsoft Excel y el correo electrónico de Outlook). En resumen, para copiar, presione CTRL+C (cmd+C en macOS) en su teclado. Para pegar, presione CTRL+V (cmd+V en macOS).

En una lista, para copiar el campo en la misma columna de la fila anterior y pegarlo en la fila actual, pulse F8.

Para obtener más información, consulte [Copiar y pegar en Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Enfoque en los productos de línea

Al trabajar en documentos que incluyen una parte de productos de línea, como una página de pedido de venta o de factura, puede cambiar su vista para centrarse solo en los productos de línea, ampliando esencialmente la parte de productos de línea para que ocupe prácticamente todo el espacio de trabajo y ocultando otras partes de la página excepto el área de acciones en la parte superior. Esto le proporciona una mejor visión general de los productos de línea y más espacio para trabajar en ellos. Esto es muy beneficioso cuando se trabaja con grandes listas de productos de línea y se desea una entrada rápida de los datos.

Otra ventaja es que también proporciona capacidad de filtrado avanzado, como en otras listas, de modo que la navegación y la búsqueda a través de los productos de línea resulta aún más fácil.

### <a name="switch-the-focus-on-and-off"></a>Activar y desactivar el enfoque

Para el enfoque en los productos de línea, seleccione cualquier lugar de la parte de producto de línea y, a continuación, seleccione ![icono Modo de enfoque](media/focus-mode.png "Icono Modo de enfoque") en la esquina superior derecha o pulse Ctrl+Mayús+F12.

Para volver a la vista normal, seleccione ![Icono Modo de enfoque](media/focus-mode.png "Icono Modo de enfoque") o pulse Ctrl+Mayús+F12 de nuevo.

### <a name="filtering-the-line-items"></a>Filtrado de los productos de línea

Para iniciar el filtrado, seleccione ![Icono Panel de filtros](media/open-filter-pane-icon.png "Icono Panel de filtros") en la parte superior de la lista o pulse **Mayús+F3** para abrir el panel de filtros. Con el panel de filtros se trabaja como en cualquier otra lista. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#Filtering).

El filtrado es especialmente útil cuando se ven y analizan documentos largos. Por ejemplo, imagine que abre una factura de ventas registrada y filtra los productos de línea para visualizar todos los productos de línea que tienen un descuento individual superior al 5 %, o bien establece un filtro para visualizar solo los accesorios de bicicleta con "pro" en el nombre.

## <a name="entering-quantities-by-calculation"></a>Introducir cantidades por cálculo

Al introducir números en campos de cantidad, como el campo **Cantidad** de una línea de diario de producto, puede introducir la fórmula en lugar de la cantidad de la suma.  

### <a name="examples"></a>Ejemplos  

-   Si introduce 19+19, el campo se calcula para obtener el valor 38.  

-   Si introduce 41-9, el campo se calcula para obtener el valor 32.  

-   Si introduce 12*4, el campo se calcula para obtener el valor 48.  

-   Si introduce 12/4, el campo se calcula para obtener el valor 3.  

## <a name="entering-negative-numbers"></a>Especificación de números negativos

Puede especificar números negativos de dos formas. El número -20,5 se puede especificar como:  

-   -20,5  

    O
-   20,5-  

 En ambos casos, el importe se registrará como -20,5.  

 Si el último carácter de la expresión es **+** o **-**, la expresión completa se registrará con ese signo. Ejemplo, **10-20+** dará como resultado 10 y no -10.  

## <a name="entering-dates-and-times"></a>Introducir fechas y horas

Puede especificar fechas y horas en todos los campos diseñados específicamente para las fechas (campos de fecha). Las fechas pueden escribirse con o sin separadores.

> [!NOTE]  
> La forma de especificar las fechas y horas depende de los valores **Región**. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Introducción de fechas

Para los campos de fecha, puede utilizar el selector de datos, que le permite seleccionar una fecha de un calendario o puede introducir fechas manualmente. Esta sección proporciona un breve resumen de cómo introducir fechas. Para obtener más detalles, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

Para la entrada de fecha manual, puede introducir dos, cuatro, seis u ocho dígitos:  

-   Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.  

-   Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo.  

-   Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1930 y el 31/12/2029, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.  

También es posible introducir una fecha como un día de la semana, seguido de un número de la semana y, opcionalmente, un año (por ejemplo, Lun25 o lun25 significa lunes de la semana 25).  

En lugar de introducir una fecha específica, puede introducir uno de estos códigos.  

|Code|Resultado|  
|--------------|----------------|  
|h|Esto especifica la fecha de hoy (la fecha de sistema del equipo).|  
|p|Esto especifica un "período contable, donde `p` significa el primer período contable, `p2` significa el segundo período contable, y así sucesivamente. |
|t|Esto especifica la fecha de trabajo que está configurada en la aplicación. Para cambiar la fecha de trabajo, vea [Cambiar la configuración básica](ui-change-basic-settings.md). Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.|
|c|Esto especifica que la fecha después de `c` es una fecha de cierre, por ejemplo, `C123101`.|  

## <a name="entering-times"></a>Introducción de horas

Cuando introduzca horas, puede insertar cualquier signo separador entre las unidades, aunque no es necesario. No necesita escribir los minutos, los segundo ni AM/PM.  

En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan.  

|Movimiento|Interpretación|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05,5|  
|053005050|05:30:05.05|  

 Debe introducir dos dígitos para cada unidad de tiempo si no escribe ningún separador.  

## <a name="entering-datetimes"></a>Introducción de fechas/horas

Cuando introduzca fechas y horas, debe introducir un espacio en blanco entre la fecha y la hora.  

En la tabla siguiente se muestran varias formas de introducir fechas y horas y cómo se interpretan.  

|Movimiento|Interpretación|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-mes actual-año actual 12:00:00|  
|1112 12|11-12-año actual 12:00:00|  
|h u hoy|fecha de hoy 00:00:00|  
|h hora|fecha de hoy hora real|  
|t 10:30|fecha de hoy 10:30:00|  
|h 3:3:3|fecha de hoy 03:03:03|  
|l o fecha de trabajo|la fecha de trabajo 00:00:00|  
|l o lunes|Lunes de la semana actual 00:00:00|  
|ma o martes|Martes de la semana actual 00:00:00|  
|mi o miércoles|Miércoles de la semana actual 00:00:00|  
|ju o jueves|Jueves de la semana actual 00:00:00|  
|v o viernes|Viernes de la semana actual 00:00:00|  
|s o sábado|Sábado de la semana actual 00:00:00|  
|do o domingo|Domingo de la semana actual 00:00:00|  
|ma 10:30|Martes de la semana actual 10:30:00|  
|ma 3:3:3|Martes de la semana actual 03:03:03|  

## <a name="entering-duration"></a>Introducción de duración

Introduzca un periodo de tiempo como un número seguido de su unidad de medida.  

A continuación se muestran algunos ejemplos.  

|Duración|Unidad de medida**|  
|------------------|-------------------------|  
|2h|2 hrs|  
|6h 30 m|6 hrs 30 mins|  
|6,5h|6 h 30 min|  
|90m|1 hr 30 mins|  
|2d 6h 30m|2 días 6 hrs 30 mins|  
|2d 6h 30m 56s 600ms|2 días 6 hrs 30 mins 56 segs 600 msegs|  

 También puede introducir un número y se convertirá automáticamente en un periodo de tiempo. El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.  

 Para ver la unidad de medida que se va a usar en un campo Duración, introduzca un número y observe a qué unidad de medida se convierte.  

 El número 5 se convierte a 5 hrs, si la unidad de medida es horas.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Consulte también  
 [Ordenar, buscar y filtrar listas](ui-enter-criteria-filters.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
