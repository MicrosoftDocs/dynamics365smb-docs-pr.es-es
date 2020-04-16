---
title: Introducción de fechas y horas en Business Central | Documentos de Microsoft
description: Obtener información sobre cómo introducir fechas y horas con distintos consejos de productividad como taquigrafía, expresiones y rangos. Filtrar listas o informes hasta fechas o períodos de tiempo específicos.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ff34a7a8a1086b41d2df2a75955017fc82866fb6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194408"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="a94f6-104">Trabajar con fechas y horas del calendario</span><span class="sxs-lookup"><span data-stu-id="a94f6-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="a94f6-105">ofrece múltiples formas de introducir fechas y horas, además de potentes funciones que aceleran la entrada de datos o ayudan a escribir expresiones de calendario complejas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="a94f6-106">Hay varios lugares en la aplicación donde puede introducir fechas y horas en los campos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="a94f6-107">Por ejemplo, en un pedido de venta, puede establecer la fecha de envío.</span><span class="sxs-lookup"><span data-stu-id="a94f6-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="a94f6-108">Al filtrar listas o datos de informes, puede introducir fechas y horas para señalar solo los datos que le interesan.</span><span class="sxs-lookup"><span data-stu-id="a94f6-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="a94f6-109">Compruebe su región y la configuración de idioma</span><span class="sxs-lookup"><span data-stu-id="a94f6-109">Check your region and language settings</span></span>
<span data-ttu-id="a94f6-110">La página **Mi configuración** especifica los valores de **Región** e **Idioma** que utiliza en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a94f6-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="a94f6-111">Estos ajustes influyen en cómo se introducen las fechas y horas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="a94f6-112">El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="a94f6-113">Para los patrones de fecha que involucran palabras, el idioma de las palabras que usa debe corresponder a la configuración de **Idioma**.</span><span class="sxs-lookup"><span data-stu-id="a94f6-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="a94f6-114">utiliza el sistema de calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="a94f6-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="a94f6-115">Introducción de fechas</span><span class="sxs-lookup"><span data-stu-id="a94f6-115">Entering Dates</span></span>

<span data-ttu-id="a94f6-116">En un campo de fecha, puede introducir una fecha con el formato estándar para la configuración de su región.</span><span class="sxs-lookup"><span data-stu-id="a94f6-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="a94f6-117">Diferentes regiones pueden usar diferentes separadores entre los días, meses y años.</span><span class="sxs-lookup"><span data-stu-id="a94f6-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="a94f6-118">Por ejemplo, algunas regiones usan guiones (mm-dd-aaaa) y otras usan barras diagonales (mm/dd/aaaa).</span><span class="sxs-lookup"><span data-stu-id="a94f6-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="a94f6-119">No obstante, puede usar cualquier separador, incluso un espacio y la fecha se cambiará automáticamente para usar separadores que coincidan con su región.</span><span class="sxs-lookup"><span data-stu-id="a94f6-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="a94f6-120">Tenga en cuenta que el formato en el que se muestran las fechas en los informes impresos o en los documentos enviados por correo electrónico no se ve afectado por su elección personal de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a94f6-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="a94f6-121">Para trabajar de forma más productiva con fechas y horas, puede utilizar cualquiera de los métodos o formatos que se describen en las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a94f6-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="a94f6-122">Seleccionar fechas del calendario</span><span class="sxs-lookup"><span data-stu-id="a94f6-122">Picking dates from the calendar</span></span>

<span data-ttu-id="a94f6-123">Cualquier campo que muestre un icono de calendario se puede configurar con el selector de fechas del calendario.</span><span class="sxs-lookup"><span data-stu-id="a94f6-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="a94f6-124">Para mostrar el selector de fechas del calendario, active el ícono de calendario o presione el atajo de teclado Ctrl + Inicio en el campo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="a94f6-125">![Campos de fecha](media/ui-date-field.png "Ejemplo de campo de fecha")</span><span class="sxs-lookup"><span data-stu-id="a94f6-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="a94f6-126">Consulte también [Métodos abreviados de teclado en el selector de fechas del calendario](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="a94f6-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="a94f6-127">Patrón día\-semana\-año</span><span class="sxs-lookup"><span data-stu-id="a94f6-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="a94f6-128">Puede introducir una fecha como día de la semana seguido de un número de semana y, opcionalmente, un año.</span><span class="sxs-lookup"><span data-stu-id="a94f6-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="a94f6-129">Por ejemplo, Lun25 o lun25 significa lunes de la semana 25.</span><span class="sxs-lookup"><span data-stu-id="a94f6-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="a94f6-130">Si no introduce un año, se utiliza el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="a94f6-131">En lugar de introducir la palabra completa para el día de la semana, puede introducir parte de la palabra, comenzando desde el principio.</span><span class="sxs-lookup"><span data-stu-id="a94f6-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="a94f6-132">En caso de conflictos (como con m que podría ser martes o miércoles), los días se evalúan de acuerdo con la configuración de la región.</span><span class="sxs-lookup"><span data-stu-id="a94f6-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="a94f6-133">La entrada se evalúa primero en función de la fecha de trabajo y también hoy, así que tenga esto en cuenta al abreviar.</span><span class="sxs-lookup"><span data-stu-id="a94f6-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="a94f6-134">Por ejemplo, m ya significa hoy, por lo que no puede significar martes o miércoles.</span><span class="sxs-lookup"><span data-stu-id="a94f6-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="a94f6-135">El esquema de número de la semana siempre es ISO 8601, donde la semana 1 es la semana con 4 de enero, o la semana con el primer jueves del año.</span><span class="sxs-lookup"><span data-stu-id="a94f6-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="a94f6-136">Patrones de dígitos</span><span class="sxs-lookup"><span data-stu-id="a94f6-136">Digit patterns</span></span>

<span data-ttu-id="a94f6-137">En un campo de fecha, puede introducir dos, cuatro, seis u ocho dígitos:</span><span class="sxs-lookup"><span data-stu-id="a94f6-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="a94f6-138">Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="a94f6-139">Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="a94f6-140">El orden del día y mes lo determina la configuración de región.</span><span class="sxs-lookup"><span data-stu-id="a94f6-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="a94f6-141">Incluso si la configuración de región tiene el año anterior al día y al mes, cuatro dígitos se interpretan como el día y el mes.</span><span class="sxs-lookup"><span data-stu-id="a94f6-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="a94f6-142">Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1930 y el 31/12/2029, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="a94f6-143">Hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-143">Today</span></span>

<span data-ttu-id="a94f6-144">Introduzca la palabra para hoy, en el idioma establecido por la configuración de **Idioma**, que establecerá la fecha a la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="a94f6-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="a94f6-145">En lugar de introducir la palabra completa, puede introducir parte de la palabra, comenzando desde el principio, como h u hoy, siempre que no sea también el comienzo de otra palabra.</span><span class="sxs-lookup"><span data-stu-id="a94f6-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="a94f6-146">Periodo</span><span class="sxs-lookup"><span data-stu-id="a94f6-146">Period</span></span>

<span data-ttu-id="a94f6-147">Para filtrar un período contable específico, en un campo de fecha introduzca la letra p, o la palabra periodo, seguida de un número que identifique el período contable, como p2 o periodo4.</span><span class="sxs-lookup"><span data-stu-id="a94f6-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="a94f6-148">El período contable es relativo al ejercicio de la fecha de trabajo actual que la establecida en su área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="a94f6-149">Por ejemplo, si la fecha de trabajo es **21/03/20**, con p1, o solo p, se filtra el primer periodo contable del ejercicio 2020 (por ejemplo, 01/01/20..31/01/20).</span><span class="sxs-lookup"><span data-stu-id="a94f6-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="a94f6-150">p15 filtra el decimoquinto periodo contable desde el inicio del ejercicio 2020 (por ejemplo, 01/03/21..31/03/21).</span><span class="sxs-lookup"><span data-stu-id="a94f6-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="a94f6-151">Los periodos contables se definen en la página **Periodos contables**.</span><span class="sxs-lookup"><span data-stu-id="a94f6-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="a94f6-152">Para ver o cambiar los períodos contables, abra la página [aquí](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="a94f6-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="a94f6-153">Fecha de trabajo actual</span><span class="sxs-lookup"><span data-stu-id="a94f6-153">Current work date</span></span>

<span data-ttu-id="a94f6-154">La función de fecha de trabajo le permite grabar transacciones usando una fecha que es diferente de la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="a94f6-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="a94f6-155">La palabra para 'fecha de trabajo', en el idioma establecido por la configuración **Idioma**, establecerá la fecha en la fecha de trabajo establecida actualmente que se especifica en la página **Mis configuraciones**.</span><span class="sxs-lookup"><span data-stu-id="a94f6-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="a94f6-156">En lugar de introducir la palabra completa, puede introducir parte de la palabra, comenzando desde el principio, como "t" o "trabajo".</span><span class="sxs-lookup"><span data-stu-id="a94f6-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="a94f6-157">Si no ha definido una fecha de trabajo, la fecha actual se usará como la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="a94f6-158">Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.</span><span class="sxs-lookup"><span data-stu-id="a94f6-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="a94f6-159">Consulte también [Cambiar la configuración básica como la fecha de trabajo](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="a94f6-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="a94f6-160">Fecha cierre</span><span class="sxs-lookup"><span data-stu-id="a94f6-160">Closing Date</span></span>

<span data-ttu-id="a94f6-161">Cuando cierra el ejercicio, puede usar fechas U, para indicar que un movimiento es un movimiento de cierre.</span><span class="sxs-lookup"><span data-stu-id="a94f6-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="a94f6-162">La fecha de cierre se encuentra técnicamente entre dos fechas, por ejemplo, entre 31 dic. y 1 ene.</span><span class="sxs-lookup"><span data-stu-id="a94f6-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="a94f6-163">Para especificar que es una fecha de cierre, coloque una C delante, como C123101.</span><span class="sxs-lookup"><span data-stu-id="a94f6-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="a94f6-164">Esto se puede utilizar en combinación con todos los patrones de fecha.</span><span class="sxs-lookup"><span data-stu-id="a94f6-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="a94f6-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a94f6-165">Examples</span></span>

<span data-ttu-id="a94f6-166">La siguiente tabla contiene ejemplos de fechas en todos los formatos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="a94f6-167">Se supone que la configuración regional formatea las fechas de acuerdo con: **año.mes.día.**, una semana a partir del lunes y el idioma inglés.</span><span class="sxs-lookup"><span data-stu-id="a94f6-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="a94f6-168">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="a94f6-168">**Entry**</span></span>      |<span data-ttu-id="a94f6-169">**Interpretación**</span><span class="sxs-lookup"><span data-stu-id="a94f6-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="a94f6-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="a94f6-170">2018.12.31.</span></span>|<span data-ttu-id="a94f6-171">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-171">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-172">181231</span><span class="sxs-lookup"><span data-stu-id="a94f6-172">181231</span></span>|<span data-ttu-id="a94f6-173">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-173">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="a94f6-174">18.12.31.</span></span>|<span data-ttu-id="a94f6-175">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-175">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="a94f6-176">18.12.31.</span></span>|<span data-ttu-id="a94f6-177">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-177">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-178">31122018</span><span class="sxs-lookup"><span data-stu-id="a94f6-178">20181231</span></span>|<span data-ttu-id="a94f6-179">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-179">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="a94f6-180">18/12,31</span></span>|<span data-ttu-id="a94f6-181">31/12/2018.</span><span class="sxs-lookup"><span data-stu-id="a94f6-181">2018.12.31.</span></span>|
|<span data-ttu-id="a94f6-182">11</span><span class="sxs-lookup"><span data-stu-id="a94f6-182">11</span></span>|<span data-ttu-id="a94f6-183">11/mes de la fecha de trabajo/año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="a94f6-184">1112</span><span class="sxs-lookup"><span data-stu-id="a94f6-184">1112</span></span>|<span data-ttu-id="a94f6-185">12/11/año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-185">work date year.11.12.</span></span>|
|<span data-ttu-id="a94f6-186">h u hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-186">t or today</span></span>|<span data-ttu-id="a94f6-187">fecha de hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-187">today's date</span></span>|
|<span data-ttu-id="a94f6-188">p4</span><span class="sxs-lookup"><span data-stu-id="a94f6-188">p4</span></span>|<span data-ttu-id="a94f6-189">rango de fechas que incluye el cuarto período contable, por ejemplo, 01/04/20..30/04/20</span><span class="sxs-lookup"><span data-stu-id="a94f6-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="a94f6-190">l o fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-190">w or workdate</span></span>|<span data-ttu-id="a94f6-191">la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-191">the working date</span></span>|
|<span data-ttu-id="a94f6-192">l o lunes</span><span class="sxs-lookup"><span data-stu-id="a94f6-192">m or Monday</span></span>|<span data-ttu-id="a94f6-193">Lunes de la semana de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-193">Monday of the work date week</span></span>|
|<span data-ttu-id="a94f6-194">ma o martes</span><span class="sxs-lookup"><span data-stu-id="a94f6-194">tu or Tuesday</span></span>|<span data-ttu-id="a94f6-195">Martes de la semana de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="a94f6-196">sá o sábado</span><span class="sxs-lookup"><span data-stu-id="a94f6-196">sa or Saturday</span></span>|<span data-ttu-id="a94f6-197">Sábado de la semana de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="a94f6-198">d o domingo</span><span class="sxs-lookup"><span data-stu-id="a94f6-198">s or Sunday</span></span>|<span data-ttu-id="a94f6-199">Domingo de la semana de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="a94f6-200">m23</span><span class="sxs-lookup"><span data-stu-id="a94f6-200">t23</span></span>|<span data-ttu-id="a94f6-201">Martes de la semana 23 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="a94f6-202">m 23</span><span class="sxs-lookup"><span data-stu-id="a94f6-202">t 23</span></span>|<span data-ttu-id="a94f6-203">Martes de la semana 23 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="a94f6-204">m-1</span><span class="sxs-lookup"><span data-stu-id="a94f6-204">t-1</span></span>|<span data-ttu-id="a94f6-205">Martes de la semana 1 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="a94f6-206">Configuración de rangos</span><span class="sxs-lookup"><span data-stu-id="a94f6-206">Setting Ranges</span></span>

<span data-ttu-id="a94f6-207">En listas, totales e informes, puede establecer filtros en fechas, horas y fechas y horas que contienen un valor de inicio y, opcionalmente, un valor final para mostrar solo los datos de ese rango.</span><span class="sxs-lookup"><span data-stu-id="a94f6-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="a94f6-208">Se aplican reglas estándar a la forma de establecer los rangos de fechas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="a94f6-209">**Significado**</span><span class="sxs-lookup"><span data-stu-id="a94f6-209">**Meaning**</span></span>|<span data-ttu-id="a94f6-210">**Expresión de muestra (Fecha)**</span><span class="sxs-lookup"><span data-stu-id="a94f6-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="a94f6-211">**Datos que se incluyen en el filtro**</span><span class="sxs-lookup"><span data-stu-id="a94f6-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="a94f6-212">Intervalo</span><span class="sxs-lookup"><span data-stu-id="a94f6-212">Interval</span></span>|<span data-ttu-id="a94f6-213">15 12 00..15 01 01</span><span class="sxs-lookup"><span data-stu-id="a94f6-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="a94f6-214">..15 12 00</span><span class="sxs-lookup"><span data-stu-id="a94f6-214">..12 15 00</span></span><br /><br /><span data-ttu-id="a94f6-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="a94f6-215">p1..p4</span></span>|<span data-ttu-id="a94f6-216">Registros con fechas entre el 15 12 00 y el 15 01 01 inclusive.</span><span class="sxs-lookup"><span data-stu-id="a94f6-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="a94f6-217">Registros con fechas de 12 15 00 o anteriores.</span><span class="sxs-lookup"><span data-stu-id="a94f6-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="a94f6-218">Rango de fechas que incluye los períodos contables segundo, tercero y cuarto, por ejemplo, 01/01/20..30/04/20.</span><span class="sxs-lookup"><span data-stu-id="a94f6-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="a94f6-219">O</span><span class="sxs-lookup"><span data-stu-id="a94f6-219">Either/or</span></span>|<span data-ttu-id="a94f6-220">15 12 00\|16 12 00</span><span class="sxs-lookup"><span data-stu-id="a94f6-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="a94f6-221">Registros con datos de 12 15 00 o 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="a94f6-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="a94f6-222">Si hay registros con fechas en ambos días, se mostrarán todos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="a94f6-223">Combinación</span><span class="sxs-lookup"><span data-stu-id="a94f6-223">Combination</span></span>|<span data-ttu-id="a94f6-224">15 12 00\|01 12 00..10 12 00</span><span class="sxs-lookup"><span data-stu-id="a94f6-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="a94f6-225">..14 12 00\|30 12 00..</span><span class="sxs-lookup"><span data-stu-id="a94f6-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="a94f6-226">Registros con fechas de 15 12 00 o en fechas entre el 01 12 00 y el 10 12 00, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a94f6-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="a94f6-227">Registros con fechas de 12 14 00 o anteriores, o fechas de 12 30 00 o posteriores, es decir, todos los registros excepto aquellos con fechas comprendidas entre 12 15 00 y 12 29 00 inclusive.</span><span class="sxs-lookup"><span data-stu-id="a94f6-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="a94f6-228">Puede utilizar cualquiera de los formatos válidos en los filtros de rango de fechas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="a94f6-229">Por ejemplo, lun14 3..h 4p aplicado en un campo de fecha y hora da como resultado un filtro desde las 3 a.m. del lunes en la semana 14 del año actual de la fecha de trabajo, inclusive, hasta hoy a las 4 p.m., inclusive.</span><span class="sxs-lookup"><span data-stu-id="a94f6-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="a94f6-230">Uso de fórmulas de fecha</span><span class="sxs-lookup"><span data-stu-id="a94f6-230">Using Date Formulas</span></span>
<span data-ttu-id="a94f6-231">Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="a94f6-232">Puede introducir fórmulas de fecha en varios campos o filtros de cálculo de fecha.</span><span class="sxs-lookup"><span data-stu-id="a94f6-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="a94f6-233">En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="a94f6-234">Por consiguiente, por ejemplo, si introduce 1S, el periodo comprende en realidad ocho días porque hoy está incluido.</span><span class="sxs-lookup"><span data-stu-id="a94f6-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="a94f6-235">Para especificar un periodo de siete días \(una semana verdadera\) con la fecha inicial del periodo, debe introducir 6D o 1S-1D.</span><span class="sxs-lookup"><span data-stu-id="a94f6-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="a94f6-236">A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:</span><span class="sxs-lookup"><span data-stu-id="a94f6-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="a94f6-237">La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="a94f6-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="a94f6-238">La fórmula de fecha del campo **Periodo gracia** para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento \(o desde la fecha del recordatorio anterior\), antes de que se cree un recordatorio.</span><span class="sxs-lookup"><span data-stu-id="a94f6-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="a94f6-239">La fórmula de fechas del campo **Cálculo de fecha de vencimiento** determina cómo calcular la fecha de vencimiento en el recordatorio.</span><span class="sxs-lookup"><span data-stu-id="a94f6-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="a94f6-240">La fórmula de fechas puede contener un máximo de 20 caracteres, números y letras.</span><span class="sxs-lookup"><span data-stu-id="a94f6-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="a94f6-241">Puede usar las siguientes letras, que son abreviaturas para especificaciones unidades de calendario.</span><span class="sxs-lookup"><span data-stu-id="a94f6-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="a94f6-242">Letra</span><span class="sxs-lookup"><span data-stu-id="a94f6-242">Letter</span></span>  |  <span data-ttu-id="a94f6-243">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="a94f6-244">P</span><span class="sxs-lookup"><span data-stu-id="a94f6-244">C</span></span>|<span data-ttu-id="a94f6-245">Presente</span><span class="sxs-lookup"><span data-stu-id="a94f6-245">Current</span></span>|
|<span data-ttu-id="a94f6-246">D</span><span class="sxs-lookup"><span data-stu-id="a94f6-246">D</span></span>|<span data-ttu-id="a94f6-247">Día\(s\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-247">Day\(s\)</span></span>|
|<span data-ttu-id="a94f6-248">S</span><span class="sxs-lookup"><span data-stu-id="a94f6-248">W</span></span>|<span data-ttu-id="a94f6-249">Semana\(s\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-249">Week\(s\)</span></span>|
|<span data-ttu-id="a94f6-250">M</span><span class="sxs-lookup"><span data-stu-id="a94f6-250">M</span></span>|<span data-ttu-id="a94f6-251">Mes\(es\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-251">Month\(s\)</span></span>|
|<span data-ttu-id="a94f6-252">T</span><span class="sxs-lookup"><span data-stu-id="a94f6-252">Q</span></span>|<span data-ttu-id="a94f6-253">Trimestre\(s\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="a94f6-254">A</span><span class="sxs-lookup"><span data-stu-id="a94f6-254">Y</span></span>|<span data-ttu-id="a94f6-255">Año\(s\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-255">Year\(s\)</span></span>|

<span data-ttu-id="a94f6-256">Puede construir una fórmula de fecha de tres formas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="a94f6-257">El ejemplo siguiente muestra cómo usar A para el actual y una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="a94f6-258">Expresión</span><span class="sxs-lookup"><span data-stu-id="a94f6-258">Expression</span></span>  |  <span data-ttu-id="a94f6-259">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="a94f6-260">PS</span><span class="sxs-lookup"><span data-stu-id="a94f6-260">CW</span></span>|<span data-ttu-id="a94f6-261">Presente semana</span><span class="sxs-lookup"><span data-stu-id="a94f6-261">Current week</span></span>|
|<span data-ttu-id="a94f6-262">PM</span><span class="sxs-lookup"><span data-stu-id="a94f6-262">CM</span></span>|<span data-ttu-id="a94f6-263">Presente mes</span><span class="sxs-lookup"><span data-stu-id="a94f6-263">Current month</span></span>|

<span data-ttu-id="a94f6-264">El ejemplo siguiente muestra cómo usar un número y una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="a94f6-265">Un número no puede ser superior a 9999.</span><span class="sxs-lookup"><span data-stu-id="a94f6-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="a94f6-266">Expresión</span><span class="sxs-lookup"><span data-stu-id="a94f6-266">Expression</span></span>  |  <span data-ttu-id="a94f6-267">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="a94f6-268">10D</span><span class="sxs-lookup"><span data-stu-id="a94f6-268">10D</span></span>|<span data-ttu-id="a94f6-269">10 días a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-269">10 days from today</span></span>|
|<span data-ttu-id="a94f6-270">2S</span><span class="sxs-lookup"><span data-stu-id="a94f6-270">2W</span></span>|<span data-ttu-id="a94f6-271">2 semanas a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-271">2 weeks from today</span></span>|

<span data-ttu-id="a94f6-272">El ejemplo siguiente muestra cómo usar una unidad de tiempo y un número.</span><span class="sxs-lookup"><span data-stu-id="a94f6-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="a94f6-273">Expresión</span><span class="sxs-lookup"><span data-stu-id="a94f6-273">Expression</span></span>  |  <span data-ttu-id="a94f6-274">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="a94f6-275">D10</span><span class="sxs-lookup"><span data-stu-id="a94f6-275">D10</span></span>|<span data-ttu-id="a94f6-276">El siguiente día 10 de un mes</span><span class="sxs-lookup"><span data-stu-id="a94f6-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="a94f6-277">SD4</span><span class="sxs-lookup"><span data-stu-id="a94f6-277">WD4</span></span>|<span data-ttu-id="a94f6-278">El siguiente día 4 de una semana \(jueves\)</span><span class="sxs-lookup"><span data-stu-id="a94f6-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="a94f6-279">En el ejemplo siguiente se muestra cómo puede combinar estas tres formas, según la necesidad.</span><span class="sxs-lookup"><span data-stu-id="a94f6-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="a94f6-280">Expresión</span><span class="sxs-lookup"><span data-stu-id="a94f6-280">Expression</span></span>  |  <span data-ttu-id="a94f6-281">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="a94f6-282">PM+10D</span><span class="sxs-lookup"><span data-stu-id="a94f6-282">CM+10D</span></span>|<span data-ttu-id="a94f6-283">Presente mes \+ 10 días</span><span class="sxs-lookup"><span data-stu-id="a94f6-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="a94f6-284">El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.</span><span class="sxs-lookup"><span data-stu-id="a94f6-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="a94f6-285">Expresión</span><span class="sxs-lookup"><span data-stu-id="a94f6-285">Expression</span></span>  |  <span data-ttu-id="a94f6-286">Significado</span><span class="sxs-lookup"><span data-stu-id="a94f6-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="a94f6-287">-1A</span><span class="sxs-lookup"><span data-stu-id="a94f6-287">-1Y</span></span>|<span data-ttu-id="a94f6-288">Hace un año desde hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="a94f6-289">Si el almacén utiliza un calendario base, la fórmula de fecha que escriba en este campo, por ejemplo el campo **Tiempo envío**, se interpreta según los días laborables del calendario.</span><span class="sxs-lookup"><span data-stu-id="a94f6-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="a94f6-290">Por ejemplo, 1S significa siete días laborables.</span><span class="sxs-lookup"><span data-stu-id="a94f6-290">For example, 1W  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

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
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="a94f6-291">Introducción de horas</span><span class="sxs-lookup"><span data-stu-id="a94f6-291">Entering Times</span></span>
<span data-ttu-id="a94f6-292">Cuando introduzca horas, puede insertar cualquier separador no espacial que desee entre las unidades, pero si usa dígitos dobles para cada unidad hasta milisegundos, no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a94f6-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="a94f6-293">Solo tiene que escribir las unidades más grandes que requiera; el resto se pondrá a cero.</span><span class="sxs-lookup"><span data-stu-id="a94f6-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="a94f6-294">También puede omitir los indicadores de AM/PM.</span><span class="sxs-lookup"><span data-stu-id="a94f6-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="a94f6-295">En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="a94f6-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="a94f6-296">Se supone que la configuración regional formatea las horas de acuerdo con: **Horas:Minutos:Segundos.Milisegundos.**</span><span class="sxs-lookup"><span data-stu-id="a94f6-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="a94f6-297">y usa los indicadores AM y PM de 'AM' y 'PM', respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a94f6-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="a94f6-298">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="a94f6-298">**Entry**</span></span>      |<span data-ttu-id="a94f6-299">**Interpretación**</span><span class="sxs-lookup"><span data-stu-id="a94f6-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="a94f6-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="a94f6-300">05:23:17</span></span>|<span data-ttu-id="a94f6-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="a94f6-301">05:23:17</span></span>|
|<span data-ttu-id="a94f6-302">5</span><span class="sxs-lookup"><span data-stu-id="a94f6-302">5</span></span>|<span data-ttu-id="a94f6-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-303">05:00:00</span></span>|
|<span data-ttu-id="a94f6-304">5AM</span><span class="sxs-lookup"><span data-stu-id="a94f6-304">5AM</span></span>|<span data-ttu-id="a94f6-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-305">05:00:00</span></span>|
|<span data-ttu-id="a94f6-306">5P</span><span class="sxs-lookup"><span data-stu-id="a94f6-306">5P</span></span>|<span data-ttu-id="a94f6-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-307">17:00:00</span></span>|
|<span data-ttu-id="a94f6-308">12</span><span class="sxs-lookup"><span data-stu-id="a94f6-308">12</span></span>|<span data-ttu-id="a94f6-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-309">12:00:00</span></span>|
|<span data-ttu-id="a94f6-310">12A</span><span class="sxs-lookup"><span data-stu-id="a94f6-310">12A</span></span>|<span data-ttu-id="a94f6-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-311">00:00:00</span></span>|
|<span data-ttu-id="a94f6-312">12P</span><span class="sxs-lookup"><span data-stu-id="a94f6-312">12P</span></span>|<span data-ttu-id="a94f6-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-313">12:00:00</span></span>|
|<span data-ttu-id="a94f6-314">17</span><span class="sxs-lookup"><span data-stu-id="a94f6-314">17</span></span>|<span data-ttu-id="a94f6-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-315">17:00:00</span></span>|
|<span data-ttu-id="a94f6-316">5:30</span><span class="sxs-lookup"><span data-stu-id="a94f6-316">5:30</span></span>|<span data-ttu-id="a94f6-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-317">05:30:00</span></span>|
|<span data-ttu-id="a94f6-318">0530</span><span class="sxs-lookup"><span data-stu-id="a94f6-318">0530</span></span>|<span data-ttu-id="a94f6-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-319">05:30:00</span></span>|
|<span data-ttu-id="a94f6-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="a94f6-320">5:30:5</span></span>|<span data-ttu-id="a94f6-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="a94f6-321">05:30:05</span></span>|
|<span data-ttu-id="a94f6-322">053005</span><span class="sxs-lookup"><span data-stu-id="a94f6-322">053005</span></span>|<span data-ttu-id="a94f6-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="a94f6-323">05:30:05</span></span>|
|<span data-ttu-id="a94f6-324">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="a94f6-324">5:30:5,50</span></span>|<span data-ttu-id="a94f6-325">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="a94f6-325">05:30:05.5</span></span>|
|<span data-ttu-id="a94f6-326">053005050</span><span class="sxs-lookup"><span data-stu-id="a94f6-326">053005050</span></span>|<span data-ttu-id="a94f6-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="a94f6-327">05:30:05.05</span></span>|

<span data-ttu-id="a94f6-328">Debe tener en cuenta que los milisegundos se interpretan como notación decimal.</span><span class="sxs-lookup"><span data-stu-id="a94f6-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="a94f6-329">Por ejemplo, 3, 30 y 300 significan 300 milisegundos, mientras que 03 significa 30 y 003 significa 3 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="a94f6-330">No puede utilizar 24:00 para referirse a la medianoche, ni usar un valor superior a 24:00.</span><span class="sxs-lookup"><span data-stu-id="a94f6-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="a94f6-331">La palabra para "hora" en el idioma utilizado por [!INCLUDE[d365fin](includes/d365fin_long_md.md)] se evaluará hasta la hora actual de su ordenador o dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="a94f6-331">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="a94f6-332">Puede introducir cualquier parte de la palabra, comenzando desde el principio, como h u HOR.</span><span class="sxs-lookup"><span data-stu-id="a94f6-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="a94f6-333">Introducir fechas y horas combinadas</span><span class="sxs-lookup"><span data-stu-id="a94f6-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="a94f6-334">Cuando introduce fechas y horas, que son una fecha y una hora combinadas en un campo, debe introducir un espacio entre la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="a94f6-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="a94f6-335">La parte de la fecha solo puede contener espacios en la forma del separador de fecha oficial de la configuración de su región.</span><span class="sxs-lookup"><span data-stu-id="a94f6-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="a94f6-336">El tiempo puede contener espacios alrededor del indicador AM/PM.</span><span class="sxs-lookup"><span data-stu-id="a94f6-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="a94f6-337">También es posible introducir solo una fecha en un campo de fecha y hora, pero no es posible introducir solo una hora.</span><span class="sxs-lookup"><span data-stu-id="a94f6-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="a94f6-338">En la tabla siguiente se enumeran algunos ejemplos de combinaciones de fecha/hora.</span><span class="sxs-lookup"><span data-stu-id="a94f6-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="a94f6-339">La configuración regional en los ejemplos muestra las fechas en el formato día\-mes\-año, utilizando los designadores de AM/PM, el idioma inglés y el domingo como el inicio de la semana.</span><span class="sxs-lookup"><span data-stu-id="a94f6-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="a94f6-340">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="a94f6-340">**Entry**</span></span>      |<span data-ttu-id="a94f6-341">**Interpretación**</span><span class="sxs-lookup"><span data-stu-id="a94f6-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="a94f6-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="a94f6-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="a94f6-343">08/01/2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="a94f6-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="a94f6-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="a94f6-344">131202 132455</span></span>|<span data-ttu-id="a94f6-345">13/12/2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="a94f6-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="a94f6-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="a94f6-346">1-12-02 10</span></span>|<span data-ttu-id="a94f6-347">01/12/2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="a94f6-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="a94f6-348">1.12.02 5</span></span>|<span data-ttu-id="a94f6-349">01/12/2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="a94f6-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="a94f6-350">1.12.02</span></span>|<span data-ttu-id="a94f6-351">01/12/2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="a94f6-352">11 12</span><span class="sxs-lookup"><span data-stu-id="a94f6-352">11 12</span></span>|<span data-ttu-id="a94f6-353">11/mes de la fecha de trabajo/año de la fecha de trabajo 12:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="a94f6-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="a94f6-354">1112 12</span></span>|<span data-ttu-id="a94f6-355">11/12/año de la fecha de trabajo 12:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="a94f6-356">h u hoy</span><span class="sxs-lookup"><span data-stu-id="a94f6-356">t or today</span></span>|<span data-ttu-id="a94f6-357">fecha de hoy 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="a94f6-358">h 10:30</span><span class="sxs-lookup"><span data-stu-id="a94f6-358">t 10:30</span></span>|<span data-ttu-id="a94f6-359">fecha de hoy 10:30:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="a94f6-360">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="a94f6-360">t 3:3:3</span></span>|<span data-ttu-id="a94f6-361">fecha de hoy 03:03:03</span><span class="sxs-lookup"><span data-stu-id="a94f6-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="a94f6-362">l o fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-362">w or workdate</span></span>|<span data-ttu-id="a94f6-363">la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="a94f6-364">l o lunes</span><span class="sxs-lookup"><span data-stu-id="a94f6-364">m or Monday</span></span>|<span data-ttu-id="a94f6-365">Lunes de la semana de la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="a94f6-366">ma o martes</span><span class="sxs-lookup"><span data-stu-id="a94f6-366">tu or Tuesday</span></span>|<span data-ttu-id="a94f6-367">Martes de la semana de la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="a94f6-368">sá o sábado</span><span class="sxs-lookup"><span data-stu-id="a94f6-368">sa or Saturday</span></span>|<span data-ttu-id="a94f6-369">Sábado de la semana de la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="a94f6-370">d o domingo</span><span class="sxs-lookup"><span data-stu-id="a94f6-370">s or Sunday</span></span>|<span data-ttu-id="a94f6-371">Domingo de la semana de la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="a94f6-372">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="a94f6-372">tu 10:30</span></span>|<span data-ttu-id="a94f6-373">Martes de la semana de la fecha de trabajo 10:30:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="a94f6-374">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="a94f6-374">tu 3:3:3</span></span>|<span data-ttu-id="a94f6-375">Martes de la semana de la fecha de trabajo 03:03:03</span><span class="sxs-lookup"><span data-stu-id="a94f6-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="a94f6-376">m23 h</span><span class="sxs-lookup"><span data-stu-id="a94f6-376">t23 t</span></span>|<span data-ttu-id="a94f6-377">Martes de la semana 23 del año de la fecha de trabajo, hora del día actual</span><span class="sxs-lookup"><span data-stu-id="a94f6-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="a94f6-378">m23</span><span class="sxs-lookup"><span data-stu-id="a94f6-378">t23</span></span>|<span data-ttu-id="a94f6-379">Martes de la semana 23 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="a94f6-380">m 23</span><span class="sxs-lookup"><span data-stu-id="a94f6-380">t 23</span></span>|<span data-ttu-id="a94f6-381">Hoy 23:00:00</span><span class="sxs-lookup"><span data-stu-id="a94f6-381">Today 23:00:00</span></span>|
|<span data-ttu-id="a94f6-382">m-1</span><span class="sxs-lookup"><span data-stu-id="a94f6-382">t-1</span></span>|<span data-ttu-id="a94f6-383">Martes de la semana 1 del año de la fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="a94f6-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="a94f6-384">Introducción de duración</span><span class="sxs-lookup"><span data-stu-id="a94f6-384">Entering Duration</span></span>
<span data-ttu-id="a94f6-385">Algunos campos de la aplicación representan una duración o cantidad de tiempo transcurrido, en lugar de una fecha u hora específicas.</span><span class="sxs-lookup"><span data-stu-id="a94f6-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="a94f6-386">Introduzca un periodo de tiempo como un número seguido de su unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="a94f6-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="a94f6-387">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a94f6-387">Here are some examples.</span></span>

|<span data-ttu-id="a94f6-388">**Duración**</span><span class="sxs-lookup"><span data-stu-id="a94f6-388">**Duration**</span></span>|<span data-ttu-id="a94f6-389">**Unidad de medida**</span><span class="sxs-lookup"><span data-stu-id="a94f6-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="a94f6-390">2h</span><span class="sxs-lookup"><span data-stu-id="a94f6-390">2h</span></span>|<span data-ttu-id="a94f6-391">2 h</span><span class="sxs-lookup"><span data-stu-id="a94f6-391">2 hrs</span></span>|
|<span data-ttu-id="a94f6-392">6 h 30 m</span><span class="sxs-lookup"><span data-stu-id="a94f6-392">6h 30 m</span></span>|<span data-ttu-id="a94f6-393">6 h 30 m</span><span class="sxs-lookup"><span data-stu-id="a94f6-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="a94f6-394">6,5h</span><span class="sxs-lookup"><span data-stu-id="a94f6-394">6.5h</span></span>|<span data-ttu-id="a94f6-395">6 h 30 m</span><span class="sxs-lookup"><span data-stu-id="a94f6-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="a94f6-396">90m</span><span class="sxs-lookup"><span data-stu-id="a94f6-396">90m</span></span>|<span data-ttu-id="a94f6-397">1 h 30 m</span><span class="sxs-lookup"><span data-stu-id="a94f6-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="a94f6-398">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="a94f6-398">2d 6h 30m</span></span>|<span data-ttu-id="a94f6-399">2 días 6 h 30 m</span><span class="sxs-lookup"><span data-stu-id="a94f6-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="a94f6-400">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="a94f6-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="a94f6-401">2 días 6 h 30 m 56 s 600 ms</span><span class="sxs-lookup"><span data-stu-id="a94f6-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="a94f6-402">También puede introducir un número que se convertirá automáticamente en un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a94f6-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="a94f6-403">El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.</span><span class="sxs-lookup"><span data-stu-id="a94f6-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="a94f6-404">Para ver la unidad de medida que se va a usar en un campo Duración, introduzca un número y observe a qué unidad de medida se convierte.</span><span class="sxs-lookup"><span data-stu-id="a94f6-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="a94f6-405">Por ejemplo, si la unidad de medida es horas, el número 5 se convierte a 5 hrs.</span><span class="sxs-lookup"><span data-stu-id="a94f6-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="a94f6-406">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a94f6-406">See Also</span></span>
<span data-ttu-id="a94f6-407">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a94f6-407">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a94f6-408">Cálculo de la fecha de compras</span><span class="sxs-lookup"><span data-stu-id="a94f6-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="a94f6-409">Introducir criterios en los filtros</span><span class="sxs-lookup"><span data-stu-id="a94f6-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
