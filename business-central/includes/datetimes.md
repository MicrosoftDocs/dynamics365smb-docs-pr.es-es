---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
---
Cuando introduce fechas y horas, que son una fecha y una hora combinadas en un campo, debe introducir un espacio entre la fecha y la hora. La parte de la fecha solo puede contener espacios en la forma del separador de fecha oficial de la configuración de su región. El tiempo puede contener espacios alrededor del indicador AM/PM en la configuración regional correspondiente.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

En la tabla siguiente se muestran varias formas de introducir fechas y horas y cómo se interpretan.  

|Movimiento|Interpretación|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11/mes actual/año actual 12:00:00|
|1112 12|11/12/año actual 12:00:00|
|h u hoy|fecha de hoy 00:00:00|
|h hora|fecha de hoy hora real|
|h 10:30|fecha de hoy 10:30:00|
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
|m23 h|Martes de la semana 23 del año de la fecha de trabajo, hora del día actual|
|m23|Martes de la semana 23 del año de la fecha de trabajo|
|m 23|Hoy 23:00:00|
|m-1|Martes de la semana 1 del año de la fecha de trabajo|


