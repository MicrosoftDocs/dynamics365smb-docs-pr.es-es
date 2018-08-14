---
title: "Configuración de rangos de fechas en Business Central | Documentos de Microsoft"
description: "Obtenga información sobre cómo obtener un informe para mostrar datos de periodos de tiempo específicos mediante rangos de fechas en Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: es-es
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Introducir rangos de fechas
Puede establecer filtros que contienen una fecha de inicio y de finalización para mostrar sólo los datos que se incluyen dentro de dicho rango de fechas o intervalo de tiempo. Se aplican reglas especiales a la forma de establecer los rangos de fechas. Tomemos la lista **Los 10 mejores clientes** como ejemplo:

![Configurar un rango de fechas en la página de solicitud de la lista de los 10 mejores clientes](./media/ui-enter-date-ranges/customer-top10-list.png)

Aquí puede limitar el informe a un rango de fechas como las últimas 2 semanas, o un total de 6 semanas, o el rango que desee. Para establecer los rangos de fechas, introduzca las fechas y utilice **..** o **|** para definir el rango. En nuestro ejemplo, para mostrar los 10 mejores clientes de las dos primeras semanas de mayo, definiría el filtro de fecha *05 01 17..05 14 17*.
A continuación le mostramos dos ejemplos más:

| Significado | Ejemplo | Movimientos incluidos |
|---|---|---|
|Igual a| 15 12 16 |Solo los movimientos registrados el 15 de diciembre de 2016.|
|Intervalo| 15 12 16..15 17 17<br /><br />..12 15 16|Registrados entre el 15 de diciembre de 2016 y el 15 de enero de 2017, ambos incluidos.<br /><br />Registrados el 15 de diciembre de 2016 o antes.|
|O|12 15 16&#124;12 16 16|Registrados el 15 de diciembre o el 16 de diciembre de 2016. Si hay movimientos registrados en los dos días, se mostrarán todos.|

También puede combinar los distintos tipos de formato.

| Ejemplo | Movimientos incluidos |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Movimientos registrados el 15 de diciembre de 2016, o entre el 01 de diciembre de 2016 y el 31 de mayo de 2017, ambos incluidos. |
|..12 14 16&#124;12 30 16.. | Los movimientos registrados el 14 de diciembre o con anterioridad, o bien los movimientos registrados el 30 de diciembre o posteriormente, es decir, todos los movimientos excepto los registrados en las fechas comprendidas entre el 15 y el 29 de diciembre, ambas inclusive. |

Observe que hemos utilizado el formato de fecha MMDDAA de EE. UU. A medida que [!INCLUDE[d365fin](includes/d365fin_md.md)] esté disponible en otros mercados, podrá utilizar los formatos a los que está acostumbrado.

## <a name="using-date-formulas"></a>Uso de fórmulas de fecha
Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas. Puede especificar las fórmulas en diversos campos de cálculo de fechas y en campos de frecuencia periódicos y en diarios periódicos.

> [!NOTE]
>  En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo. Por consiguiente, por ejemplo, si introduce **1W**, el periodo comprende en realidad ocho días porque hoy está incluido. Para especificar un periodo de siete días (una semana verdadera) con la fecha inicial del periodo, debe introducir **6D** o **1W\-1D**.

A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:

-   La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.

-   La fórmula de fecha del campo **Periodo gracia** para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento (o desde la fecha de vencimiento del recordatorio anterior), antes de que se cree un recordatorio.

-   La fórmula de fechas del campo **Cálculo de fecha de vencimiento** determina cómo calcular la fecha de vencimiento en el recordatorio.

La fórmula para el cálculo de fechas puede contener un máximo de 20 caracteres, números y letras. Puede usar las siguientes letras, que son abreviaturas para especificaciones de tiempo.

|  Letra  |  Especificación de tiempo  |
|----------|----------------------|
|U|Actual|
|D|Día\(s\)|
|O|Semana\(s\)|
|C|Mes\(es\)|
|Q|Trimestre\(s\)|
|Y|Año\(s\)|

Puede construir una fórmula de fecha de tres formas.

El ejemplo siguiente muestra cómo usar **C** para el actual y una unidad de tiempo.

|  Expresión  |  Significado  |
|--------------|-----------|
|PS|Presente semana|
|PM|Presente mes|

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
|PM\+10D|Presente mes \+ 10 días|

El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.

|  Expresión  |  Significado  |
|--------------|-----------|
|-1A|Hace un año desde hoy|

> [!IMPORTANT]
>  Si el almacén utiliza un calendario base, la fórmula de fecha que escriba en este campo, por ejemplo el campo **Tiempo envío**, se interpreta según los días laborables del calendario. Por ejemplo, **1W** significa siete días laborables.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)  
[Introducir criterios en los filtros](ui-enter-criteria-filters.md)  

