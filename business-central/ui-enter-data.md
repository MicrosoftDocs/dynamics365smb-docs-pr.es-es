---
title: "Cómo introducir datis eb campos | Documentos de Microsoft"
description: "Hay varias funciones generales que le pueden ayudar a introducir datos de manera rápida y fácil. Las funciones generales para la introducción de datos se describen en este tema."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a>Introducción de datos
Hay varias funciones generales que le pueden ayudar a introducir datos de manera rápida y fácil. Las funciones generales para la introducción de datos se describen en este artículo.  

Los ejemplos de este producto utilizan los datos de demostración.

## <a name="mandatory-fields"></a>Campos obligatorios
Cuando se introducen datos en páginas, determinados campos aparecen marcados con un asterisco de color rojo. El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.  

Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página. El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.  


## <a name="finding-data-as-you-type"></a>Buscar datos al escribir  
 Cuando comience a escribir caracteres en un campo, aparecerá una lista desplegable que muestra los posibles valores de campo. Esta lista cambia a medida que escriba caracteres adicionales y puede seleccionar el valor correcto cuando aparezca.  

 Muchos campos tienen un botón de flecha hacia abajo que puede elegir. Seleccione la flecha para desplegar una lista de datos que están disponibles para su introducción en el campo. El botón tiene dos funciones, según el tipo de campo:  

-   Búsqueda: muestra información de otra tabla, que puede introducir en el campo. Puede seleccionar un elemento de datos a la vez.  

-   Desplegable: muestra el conjunto de opciones que existe para el campo. Sólo puede seleccionar una de las opciones.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Introducir cantidades por cálculo  
 Al introducir números en campos de cantidad, como el campo **Cantidad** de una línea de diario de producto, puede introducir la fórmula en lugar de la cantidad de la suma.  

## <a name="examples"></a>Ejemplos  

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
 En un campo de fecha, puede introducir dos, cuatro, seis u ocho dígitos:  

-   Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.  

-   Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo.  

-   Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1930 y el 31/12/2029, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.  

 También es posible introducir una fecha como un día de la semana, seguido de un número de la semana y, opcionalmente, un año (por ejemplo, Lun25 o lun25 significa lunes de la semana 25).  

 En lugar de introducir una fecha específica, puede introducir uno de dos códigos.  

|Código|Resultado|  
|--------------|----------------|  
|h|Esto es la fecha de hoy (la fecha de sistema del equipo).|  
|t|Esta es la fecha de trabajo que está configurada en la aplicación. Para cambiar la fecha de trabajo, vea [Cambiar la configuración básica](ui-change-basic-settings.md). Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|h 10:30|fecha de hoy 10:30:00|  
|h 3:3:3|fecha de hoy 03:03:03|  
|t o fecha de trabajo|la fecha de trabajo 00:00:00|  
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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Uso de fórmulas de fecha  
 Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas. Puede especificar las fórmulas en diversos campos de cálculo de fechas y en campos de frecuencia periódicos y en diarios periódicos.  

> [!NOTE]  
>  En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo. Por consiguiente, si introduce 1s, por ejemplo, el periodo comprende en realidad ocho días porque hoy está incluido. Para especificar un periodo de siete días (una semana verdadera) con la fecha inicial del periodo, debe introducir 6D o 1W-1D.  

 A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:  

-   La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.  

-   La fórmula de fecha del campo Periodo gracia para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento (o desde la fecha del recordatorio anterior), antes de que se cree un recordatorio.  

-   La fórmula de fechas del campo Cálculo de fecha de vencimiento determina cómo calcular la fecha de vencimiento en el recordatorio.  

 La fórmula para el cálculo de fechas puede contener un máximo de 20 caracteres, números y letras. Puede usar las siguientes letras, que son abreviaturas para especificaciones de tiempo.  

|||  
|-|-|  
|C|Presente|  
|D|Día(s)|  
|S|Semana(s)|  
|M|Mes(es)|  
|T|Trimestre(s)|  
|A|Año(s)|  

 Puede construir una fórmula de fecha de tres formas.  

 El ejemplo siguiente muestra un número actual y más una unidad de tiempo.  

|||  
|-|-|  
|PS|Presente semana|  
|PM|Presente mes|  

 El ejemplo siguiente muestra un número y una unidad de tiempo. Un número no puede ser superior a 9999.  

|||  
|-|-|  
|10D|10 días a partir de hoy|  
|2S|2 semanas a partir de hoy|  

 El ejemplo siguiente muestra una unidad de tiempo y un número.  

|||  
|-|-|  
|D10|El siguiente día 10 de un mes|  
|DS4|El siguiente día 4 de una semana (jueves)|  

 En el ejemplo siguiente se muestra cómo puede combinar estas tres formas, según la necesidad.  

|||  
|-|-|  
|PM+10D|Presente mes + 10 días|  

 El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.  

|||  
|-|-|  
|-1A|Hace un año desde hoy|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Consulte también  
 [Buscar, filtrar y ordenar datos](ui-enter-criteria-filters.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

