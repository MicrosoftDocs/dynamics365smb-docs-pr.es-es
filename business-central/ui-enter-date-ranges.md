---
title: Introducción de fechas y horas en Business Central
description: 'Obtener información sobre cómo introducir fechas y horas con distintos consejos de productividad como taquigrafía, expresiones y rangos.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/27/2023
ms.author: bholtorf
---

# Trabajar con fechas y horas del calendario

Puede introducir fechas y horas de varias maneras. [!INCLUDE[prod_short](includes/prod_long.md)] incluye potentes funciones que aceleran la entrada de datos o ayudan a escribir expresiones de calendario complejas. Hay varios lugares en la aplicación donde puede introducir fechas y horas en los campos. Por ejemplo, en un pedido de venta, puede establecer la fecha de envío. Al filtrar listas o datos de informes, puede introducir fechas y horas para señalar solo los datos que le interesan.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Compruebe su región y la configuración de idioma

La página **Mi configuración** especifica los valores de **Región** e **Idioma** que utiliza en la aplicación. Estos ajustes influyen en cómo se introducen las fechas y horas.

- El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.

- Para los patrones de fecha que involucran palabras, el idioma de las palabras que usa debe corresponder a la configuración de **Idioma**.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] utiliza el sistema de calendario gregoriano.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## Introducción de fechas

En un campo de fecha, puede introducir una fecha con el formato estándar para la configuración de su región. Diferentes regiones pueden usar diferentes separadores entre los días, meses y años. Por ejemplo, algunas regiones usan guiones (mm-dd-aaaa) y otras usan barras diagonales (mm/dd/aaaa).  

> [!TIP]
> Puede usar cualquier separador, incluso un espacio y la fecha se cambiará automáticamente para usar separadores que coincidan con su región.

> [!NOTE]
> El formato en el que se muestran las fechas en los informes impresos o en los documentos enviados por correo electrónico no se ve afectado por su elección personal de configuración regional.

Para trabajar de forma más productiva con fechas y horas, puede utilizar cualquiera de los métodos o formatos que se describen en las siguientes secciones.

### Seleccionar fechas del calendario

Cualquier campo que muestre un icono de calendario se puede configurar con el selector de fechas del calendario. Para mostrar el selector de fechas del calendario, active el icono del calendario o seleccione el atajo <kbd>Ctrl</kbd>+<kbd>Inicio</kbd> en el campo.

![Campos de fecha.](media/ui-date-field.png "Ejemplo de campo de fecha")

Consulte también [Métodos abreviados de teclado en el selector de fechas del calendario](keyboard-shortcuts.md#calendarshortcuts).

### Patrón día\-semana\-año

Puede introducir una fecha como día de la semana seguido de un número de semana y, opcionalmente, un año. Por ejemplo, Lun25 o lun25 significa lunes de la semana 25. Si no introduce un año, se utiliza el año de la fecha de trabajo.

En lugar de introducir la palabra completa para el día de la semana, puede introducir parte de la palabra, comenzando desde el principio. En caso de conflictos (como con m que podría ser martes o miércoles), los días se evalúan de acuerdo con la configuración de la región. La entrada se evalúa primero en función de la fecha de trabajo y también hoy, así que tenga esto en cuenta al abreviar. Por ejemplo, _m_ ya significa hoy, por lo que no puede significar martes o miércoles.

El esquema de número de la semana siempre es ISO 8601, donde la semana 1 es la semana con 4 de enero, o la semana con el primer jueves del año.

### Patrones de dígitos

En un campo de fecha, puede introducir dos, cuatro, seis u ocho dígitos:

- Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.

- Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo. El orden del día y mes lo determina la configuración de región. Incluso si la configuración de región tiene el año anterior al día y al mes, cuatro dígitos se interpretan como el día y el mes.

- Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1950 y el 31/12/2049, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.

  > [!NOTE]
  > Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones, el intervalo de años de dos dígitos puede ser diferente. Los administradores pueden cambiar el rango modificando el ajuste **CalendarTwoDigitYearMax** del servidor [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configuración de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).
 
### Hoy

Ingrese la palabra para _hoy_, en el idioma especificado en la página **Mi configuración**, para establecer la fecha de un registro en la fecha de hoy. En lugar de introducir la palabra completa, puede introducir parte de la palabra, comenzando desde el principio. Por ejemplo, en inglés, puede ingresar _t_ o _tod_, siempre que no sea también el comienzo de otra palabra.

### Período

Para filtrar un período contable específico, en un campo de fecha introduzca la letra p, o la palabra periodo, seguida de un número que identifique el período contable, como p2 o periodo4. El período contable es relativo al ejercicio de la fecha de trabajo actual que la establecida en su área de trabajo. Por ejemplo, si la fecha de trabajo es **21/03/22**, con _p1_, o solo _p_, se filtra el primer periodo contable del ejercicio 2022 (por ejemplo, 01/01/22..31/01/22). _p15_ filtra el decimoquinto periodo contable desde el inicio del ejercicio 2022 (por ejemplo, 01/03/23..31/03/23).

Los periodos contables se definen en la página **Periodos contables**. Para ver o cambiar los períodos contables, abra la página [aquí](https://businesscentral.dynamics.com/?page=100).

### Fecha de trabajo

Utilice una fecha de trabajo para especificar una fecha que no sea la de hoy en los registros. Por ejemplo, una fecha de trabajo es útil cuando necesita establecer una fecha particular para varios registros. Usted especifica la fecha de trabajo en la página **Mi configuración**. 

Una forma rápida de ingresar la fecha de trabajo en los registros es ingresar parte o toda la palabra _trabajo_, comenzando desde el principio de la palabra, en el idioma en el que esté usando [!INCLUDE[prod_short](includes/prod_long.md)]. Por ejemplo, en inglés, puede ingresar _w_ o _work_. El idioma también se especifica en la página **Mi configuración**.

Si no ha especificado una fecha de trabajo, se utilizará la fecha de hoy. Para más información, consulte [Cambiar la configuración básica como la fecha de trabajo](ui-change-basic-settings.md#work-date).

### Fecha cierre

Cuando cierra el ejercicio, puede usar fechas U, para indicar que un movimiento es un movimiento de cierre. La fecha de cierre se encuentra técnicamente entre dos fechas, por ejemplo, entre 31 de diciembre y 1 de enero.

Para especificar que es una fecha de cierre, coloque una C delante, como C123101. Use este formato en combinación con todos los patrones de fecha.

### Ejemplos

La siguiente tabla contiene ejemplos de fechas en todos los formatos. Se supone que la configuración regional formatea las fechas de acuerdo con: **año.mes.día.**, una semana a partir del lunes y el idioma inglés.

|**Entrada**      |**Interpretación**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|11/mes de la fecha de trabajo/año de la fecha de trabajo.|
|1112|12/11/año de la fecha de trabajo.|
|h u hoy|fecha de hoy|
|p4|rango de fechas que incluye el cuarto período contable, por ejemplo, 01/04/20..30/04/20|
|l o fecha de trabajo|la fecha de trabajo|
|l o lunes|Lunes de la semana de la fecha de trabajo|
|ma o martes|Martes de la semana de la fecha de trabajo|
|sá o sábado|Sábado de la semana de la fecha de trabajo|
|d o domingo|Domingo de la semana de la fecha de trabajo|
|m23|Martes de la semana 23 del año de la fecha de trabajo|
|m 23|Martes de la semana 23 del año de la fecha de trabajo|
|m-1|Martes de la semana 1 del año de la fecha de trabajo|

##  <a name="BKMK_SettingDateRanges"></a> Configuración de rangos

En listas, totales e informes, puede establecer filtros en fechas, horas y fechas y horas que contienen un valor de inicio y, opcionalmente, un valor final para mostrar solo los datos de ese rango. Se aplican reglas estándar a la forma de establecer los rangos de fechas.

|**Significado**|**Expresión de muestra (Fecha)**|**Datos que se incluyen en el filtro**|
|-----------|---------------------|--------------------|
|Intervalo|15 12 00..15 01 01<br /><br />..15 12 00<br /><br />p1..p4|Registros con fechas entre el 15 12 00 y el 15 01 01 inclusive.<br /><br />Registros con fechas de 12 15 00 o anteriores.<br /><br />Rango de fechas que incluye los períodos contables segundo, tercero y cuarto, por ejemplo, 01/01/20..30/04/20.|
|O|15 12 00\|16 12 00|Registros con datos de 12 15 00 o 12 16 00. Si hay registros con fechas en ambos días, se mostrarán todos.|
|Combinación|15 12 00\|01 12 00..10 12 00  <br /><br />..14 12 00\|30 12 00..|Registros con fechas de 15 12 00 o en fechas entre el 01 12 00 y el 10 12 00, inclusive.  <br /><br />Registros con fechas de 12 14 00 o anteriores, o fechas de 12 30 00 o posteriores, es decir, todos los registros excepto aquellos con fechas comprendidas entre 12 15 00 y 12 29 00 inclusive.|

Puede utilizar cualquiera de los formatos válidos en los filtros de rango de fechas. Por ejemplo, lun14 3..h 4p aplicado en un campo de fecha y hora da como resultado un filtro desde las 3 a.m. del lunes en la semana 14 del año actual de la fecha de trabajo, inclusive, hasta hoy a las 4 p.m., inclusive.

## Usar fórmulas de fecha

Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas. Puede introducir fórmulas de fecha en varios campos o filtros de cálculo de fecha.

> [!NOTE]
> En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo. Por consiguiente, por ejemplo, si introduce 1S, el periodo comprende en realidad ocho días porque hoy está incluido. Para especificar un periodo de siete días \(una semana verdadera\) con la fecha inicial del periodo, debe introducir 6D o 1S-1D.

A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:

- La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.

- La fórmula de fecha del campo **Periodo gracia** para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento \(o desde la fecha del recordatorio anterior\), antes de que se cree un recordatorio.

- La fórmula de fechas del campo **Cálculo de fecha de vencimiento** determina cómo calcular la fecha de vencimiento en el recordatorio.

La fórmula de fechas puede contener un máximo de 20 caracteres, números y letras. Puede usar las siguientes letras, que son abreviaturas para especificaciones unidades de calendario.

|  Letra  |  Significado  |
|----------|----------------------|
|P|Presente|
|D|Día\(s\)|
|S|Semana\(s\)|
|M|Mes\(es\)|
|T|Trimestre\(s\)|
|A|Año\(s\)|

Puede construir una fórmula de fecha de tres formas.

El ejemplo siguiente muestra cómo usar A para el actual y una unidad de tiempo.

|  Expresión  |  Significado  |
|--------------|-----------|
|PS|Presente semana|
|MC|Mes actual (último día del mes)|

El ejemplo siguiente muestra cómo usar un número y una unidad de tiempo. Un número no puede ser superior a 9999.

|  Expresión  |  Significado  |
|--------------|-----------|
|10D|10 días a partir de hoy|
|2S|2 semanas a partir de hoy|

El ejemplo siguiente muestra cómo usar una unidad de tiempo y un número.

|  Expresión  |  Significado  |
|--------------|-----------|
|D10|El siguiente día 10 de un mes|
|SD4|El siguiente día 4 de una semana \(jueves\)|

En el ejemplo siguiente se muestra cómo puede combinar estas tres formas, según la necesidad.

|  Expresión  |  Significado  |
|--------------|-----------|
|PM+10D|Presente mes \+ 10 días|

El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.

|  Expresión  |  Significado  |
|--------------|-----------|
|-1A|Hace un año desde hoy|

> [!IMPORTANT]
> Si el almacén utiliza un calendario base, la fórmula de fecha que escriba en este campo, por ejemplo el campo **Tiempo envío**, se interpreta según los días laborables del calendario. Por ejemplo, 1S significa siete días laborables.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Use Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
> In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

- The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

- The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

- The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
> If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## Introducción de horas

Cuando introduzca horas, puede insertar cualquier signo separador que no sea espacio entre las unidades. Si usa dos dígitos para cada unidad hasta milisegundos, entonces no es necesario.

Solo tiene que escribir las unidades más grandes que requiera; el resto se pondrá a cero. También puede omitir los indicadores de AM/PM.

En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan. Se supone que la configuración regional formatea las horas de acuerdo con: **Horas:Minutos:Segundos.Milisegundos.** y usa los indicadores AM y PM de 'AM' y 'PM', respectivamente.

|**Entrada**      |**Interpretación**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5.50|05:30:05,5|
|053005050|05:30:05.05|

> [!NOTE]
> Los milisegundos se interpretan como notación decimal. Por ejemplo, 3, 30 y 300 significan 300 milisegundos, mientras que 03 significa 30 y 003 significa 3 milisegundos.

> [!IMPORTANT]
> No puede utilizar 24:00 para referirse a la medianoche, ni usar un valor superior a 24:00.

La palabra para "hora" en el idioma utilizado por [!INCLUDE[prod_short](includes/prod_long.md)] se evaluará hasta la hora actual de su ordenador o dispositivo móvil. Puede introducir cualquier parte de la palabra, comenzando desde el principio, como h u HOR.

## Introducir fechas y horas combinadas

[!INCLUDE [datetimes](includes/datetimes.md)]

## Introducción de duración

Algunos campos de la aplicación representan una duración o cantidad de tiempo transcurrido, en lugar de una fecha u hora específicas. Introduzca un periodo de tiempo como un número seguido de su unidad de medida.

A continuación se muestran algunos ejemplos.

|**Duración**|**Unidad de medida**|
|------------|-------------------|
|2h|2 h|
|6 h 30 m|6 h 30 m|
|6,5h|6 h 30 m|
|90m|1 h 30 m|
|2d 6h 30m|2 días 6 hrs 30 mins|
|2d 6h 30m 56s 600ms|2 días 6 h 30 m 56 s 600 ms|

También puede introducir un número que se convertirá automáticamente en un periodo de tiempo. El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.

Para ver qué unidad de medida se está utilizando en un campo de duración, introduzca un número. Luego, puede ver a qué unidad de medida se convierte.

Por ejemplo, si la unidad de medida es horas, el número 5 se convierte a 5 hrs.

## Consulte también .

[Trabajar con [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)  
[Introducir criterios en los filtros](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
