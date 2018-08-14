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
# <a name="entering-date-ranges"></a><span data-ttu-id="0488a-103">Introducir rangos de fechas</span><span class="sxs-lookup"><span data-stu-id="0488a-103">Entering Date Ranges</span></span>
<span data-ttu-id="0488a-104">Puede establecer filtros que contienen una fecha de inicio y de finalización para mostrar sólo los datos que se incluyen dentro de dicho rango de fechas o intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0488a-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="0488a-105">Se aplican reglas especiales a la forma de establecer los rangos de fechas.</span><span class="sxs-lookup"><span data-stu-id="0488a-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="0488a-106">Tomemos la lista **Los 10 mejores clientes** como ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0488a-106">Let's take the **Customer Top 10** as an example:</span></span>

![Configurar un rango de fechas en la página de solicitud de la lista de los 10 mejores clientes](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="0488a-108">Aquí puede limitar el informe a un rango de fechas como las últimas 2 semanas, o un total de 6 semanas, o el rango que desee.</span><span class="sxs-lookup"><span data-stu-id="0488a-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="0488a-109">Para establecer los rangos de fechas, introduzca las fechas y utilice **..**</span><span class="sxs-lookup"><span data-stu-id="0488a-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="0488a-110">o **|** para definir el rango.</span><span class="sxs-lookup"><span data-stu-id="0488a-110">or **|** to set the range.</span></span> <span data-ttu-id="0488a-111">En nuestro ejemplo, para mostrar los 10 mejores clientes de las dos primeras semanas de mayo, definiría el filtro de fecha *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="0488a-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="0488a-112">A continuación le mostramos dos ejemplos más:</span><span class="sxs-lookup"><span data-stu-id="0488a-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="0488a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-113">Meaning</span></span> | <span data-ttu-id="0488a-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0488a-114">Example</span></span> | <span data-ttu-id="0488a-115">Movimientos incluidos</span><span class="sxs-lookup"><span data-stu-id="0488a-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="0488a-116">Igual a</span><span class="sxs-lookup"><span data-stu-id="0488a-116">Equal to</span></span>| <span data-ttu-id="0488a-117">15 12 16</span><span class="sxs-lookup"><span data-stu-id="0488a-117">12 15 16</span></span> |<span data-ttu-id="0488a-118">Solo los movimientos registrados el 15 de diciembre de 2016.</span><span class="sxs-lookup"><span data-stu-id="0488a-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="0488a-119">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0488a-119">Interval</span></span>| <span data-ttu-id="0488a-120">15 12 16..15 17 17</span><span class="sxs-lookup"><span data-stu-id="0488a-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="0488a-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="0488a-121">..12 15 16</span></span>|<span data-ttu-id="0488a-122">Registrados entre el 15 de diciembre de 2016 y el 15 de enero de 2017, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="0488a-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="0488a-123">Registrados el 15 de diciembre de 2016 o antes.</span><span class="sxs-lookup"><span data-stu-id="0488a-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="0488a-124">O</span><span class="sxs-lookup"><span data-stu-id="0488a-124">Either/or</span></span>|<span data-ttu-id="0488a-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="0488a-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="0488a-126">Registrados el 15 de diciembre o el 16 de diciembre de 2016.</span><span class="sxs-lookup"><span data-stu-id="0488a-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="0488a-127">Si hay movimientos registrados en los dos días, se mostrarán todos.</span><span class="sxs-lookup"><span data-stu-id="0488a-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="0488a-128">También puede combinar los distintos tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="0488a-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="0488a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0488a-129">Example</span></span> | <span data-ttu-id="0488a-130">Movimientos incluidos</span><span class="sxs-lookup"><span data-stu-id="0488a-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="0488a-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="0488a-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="0488a-132">Movimientos registrados el 15 de diciembre de 2016, o entre el 01 de diciembre de 2016 y el 31 de mayo de 2017, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="0488a-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="0488a-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="0488a-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="0488a-134">Los movimientos registrados el 14 de diciembre o con anterioridad, o bien los movimientos registrados el 30 de diciembre o posteriormente, es decir, todos los movimientos excepto los registrados en las fechas comprendidas entre el 15 y el 29 de diciembre, ambas inclusive.</span><span class="sxs-lookup"><span data-stu-id="0488a-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="0488a-135">Observe que hemos utilizado el formato de fecha MMDDAA de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="0488a-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="0488a-136">A medida que [!INCLUDE[d365fin](includes/d365fin_md.md)] esté disponible en otros mercados, podrá utilizar los formatos a los que está acostumbrado.</span><span class="sxs-lookup"><span data-stu-id="0488a-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="0488a-137">Uso de fórmulas de fecha</span><span class="sxs-lookup"><span data-stu-id="0488a-137">Using Date Formulas</span></span>
<span data-ttu-id="0488a-138">Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas.</span><span class="sxs-lookup"><span data-stu-id="0488a-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="0488a-139">Puede especificar las fórmulas en diversos campos de cálculo de fechas y en campos de frecuencia periódicos y en diarios periódicos.</span><span class="sxs-lookup"><span data-stu-id="0488a-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="0488a-140">En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo.</span><span class="sxs-lookup"><span data-stu-id="0488a-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="0488a-141">Por consiguiente, por ejemplo, si introduce **1W**, el periodo comprende en realidad ocho días porque hoy está incluido.</span><span class="sxs-lookup"><span data-stu-id="0488a-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="0488a-142">Para especificar un periodo de siete días (una semana verdadera) con la fecha inicial del periodo, debe introducir **6D** o **1W\-1D**.</span><span class="sxs-lookup"><span data-stu-id="0488a-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="0488a-143">A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:</span><span class="sxs-lookup"><span data-stu-id="0488a-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="0488a-144">La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="0488a-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="0488a-145">La fórmula de fecha del campo **Periodo gracia** para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento (o desde la fecha de vencimiento del recordatorio anterior), antes de que se cree un recordatorio.</span><span class="sxs-lookup"><span data-stu-id="0488a-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="0488a-146">La fórmula de fechas del campo **Cálculo de fecha de vencimiento** determina cómo calcular la fecha de vencimiento en el recordatorio.</span><span class="sxs-lookup"><span data-stu-id="0488a-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="0488a-147">La fórmula para el cálculo de fechas puede contener un máximo de 20 caracteres, números y letras.</span><span class="sxs-lookup"><span data-stu-id="0488a-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="0488a-148">Puede usar las siguientes letras, que son abreviaturas para especificaciones de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0488a-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="0488a-149">Letra</span><span class="sxs-lookup"><span data-stu-id="0488a-149">Letter</span></span>  |  <span data-ttu-id="0488a-150">Especificación de tiempo</span><span class="sxs-lookup"><span data-stu-id="0488a-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="0488a-151">U</span><span class="sxs-lookup"><span data-stu-id="0488a-151">C</span></span>|<span data-ttu-id="0488a-152">Actual</span><span class="sxs-lookup"><span data-stu-id="0488a-152">Current</span></span>|
|<span data-ttu-id="0488a-153">D</span><span class="sxs-lookup"><span data-stu-id="0488a-153">D</span></span>|<span data-ttu-id="0488a-154">Día\(s\)</span><span class="sxs-lookup"><span data-stu-id="0488a-154">Day\(s\)</span></span>|
|<span data-ttu-id="0488a-155">O</span><span class="sxs-lookup"><span data-stu-id="0488a-155">W</span></span>|<span data-ttu-id="0488a-156">Semana\(s\)</span><span class="sxs-lookup"><span data-stu-id="0488a-156">Week\(s\)</span></span>|
|<span data-ttu-id="0488a-157">C</span><span class="sxs-lookup"><span data-stu-id="0488a-157">M</span></span>|<span data-ttu-id="0488a-158">Mes\(es\)</span><span class="sxs-lookup"><span data-stu-id="0488a-158">Month\(s\)</span></span>|
|<span data-ttu-id="0488a-159">Q</span><span class="sxs-lookup"><span data-stu-id="0488a-159">Q</span></span>|<span data-ttu-id="0488a-160">Trimestre\(s\)</span><span class="sxs-lookup"><span data-stu-id="0488a-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="0488a-161">Y</span><span class="sxs-lookup"><span data-stu-id="0488a-161">Y</span></span>|<span data-ttu-id="0488a-162">Año\(s\)</span><span class="sxs-lookup"><span data-stu-id="0488a-162">Year\(s\)</span></span>|

<span data-ttu-id="0488a-163">Puede construir una fórmula de fecha de tres formas.</span><span class="sxs-lookup"><span data-stu-id="0488a-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="0488a-164">El ejemplo siguiente muestra cómo usar **C** para el actual y una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0488a-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="0488a-165">Expresión</span><span class="sxs-lookup"><span data-stu-id="0488a-165">Expression</span></span>  |  <span data-ttu-id="0488a-166">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0488a-167">PS</span><span class="sxs-lookup"><span data-stu-id="0488a-167">CW</span></span>|<span data-ttu-id="0488a-168">Presente semana</span><span class="sxs-lookup"><span data-stu-id="0488a-168">Current week</span></span>|
|<span data-ttu-id="0488a-169">PM</span><span class="sxs-lookup"><span data-stu-id="0488a-169">CM</span></span>|<span data-ttu-id="0488a-170">Presente mes</span><span class="sxs-lookup"><span data-stu-id="0488a-170">Current month</span></span>|

<span data-ttu-id="0488a-171">El ejemplo siguiente muestra cómo usar un número y una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0488a-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="0488a-172">Un número no puede ser superior a 9999.</span><span class="sxs-lookup"><span data-stu-id="0488a-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="0488a-173">Expresión</span><span class="sxs-lookup"><span data-stu-id="0488a-173">Expression</span></span>  |  <span data-ttu-id="0488a-174">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0488a-175">10D</span><span class="sxs-lookup"><span data-stu-id="0488a-175">10D</span></span>|<span data-ttu-id="0488a-176">10 días a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="0488a-176">10 days from today</span></span>|
|<span data-ttu-id="0488a-177">2S</span><span class="sxs-lookup"><span data-stu-id="0488a-177">2W</span></span>|<span data-ttu-id="0488a-178">2 semanas a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="0488a-178">2 weeks from today</span></span>|

<span data-ttu-id="0488a-179">El ejemplo siguiente muestra cómo usar una unidad de tiempo y un número.</span><span class="sxs-lookup"><span data-stu-id="0488a-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="0488a-180">Expresión</span><span class="sxs-lookup"><span data-stu-id="0488a-180">Expression</span></span>  |  <span data-ttu-id="0488a-181">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0488a-182">D10</span><span class="sxs-lookup"><span data-stu-id="0488a-182">D10</span></span>|<span data-ttu-id="0488a-183">El siguiente día 10 de un mes</span><span class="sxs-lookup"><span data-stu-id="0488a-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="0488a-184">SD4</span><span class="sxs-lookup"><span data-stu-id="0488a-184">WD4</span></span>|<span data-ttu-id="0488a-185">El siguiente día 4 de una semana \(jueves\)</span><span class="sxs-lookup"><span data-stu-id="0488a-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="0488a-186">En el ejemplo siguiente se muestra cómo puede combinar estas tres formas, según la necesidad.</span><span class="sxs-lookup"><span data-stu-id="0488a-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="0488a-187">Expresión</span><span class="sxs-lookup"><span data-stu-id="0488a-187">Expression</span></span>  |  <span data-ttu-id="0488a-188">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0488a-189">PM\+10D</span><span class="sxs-lookup"><span data-stu-id="0488a-189">CM\+10D</span></span>|<span data-ttu-id="0488a-190">Presente mes \+ 10 días</span><span class="sxs-lookup"><span data-stu-id="0488a-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="0488a-191">El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.</span><span class="sxs-lookup"><span data-stu-id="0488a-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="0488a-192">Expresión</span><span class="sxs-lookup"><span data-stu-id="0488a-192">Expression</span></span>  |  <span data-ttu-id="0488a-193">Significado</span><span class="sxs-lookup"><span data-stu-id="0488a-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="0488a-194">-1A</span><span class="sxs-lookup"><span data-stu-id="0488a-194">-1Y</span></span>|<span data-ttu-id="0488a-195">Hace un año desde hoy</span><span class="sxs-lookup"><span data-stu-id="0488a-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="0488a-196">Si el almacén utiliza un calendario base, la fórmula de fecha que escriba en este campo, por ejemplo el campo **Tiempo envío**, se interpreta según los días laborables del calendario.</span><span class="sxs-lookup"><span data-stu-id="0488a-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="0488a-197">Por ejemplo, **1W** significa siete días laborables.</span><span class="sxs-lookup"><span data-stu-id="0488a-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="0488a-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0488a-198">See Also</span></span>
<span data-ttu-id="0488a-199">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0488a-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0488a-200">Cálculo de la fecha de compras</span><span class="sxs-lookup"><span data-stu-id="0488a-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="0488a-201">Introducir criterios en los filtros</span><span class="sxs-lookup"><span data-stu-id="0488a-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

