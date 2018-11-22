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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 0e844d56e973a8e94254212daed32dea2d2263ae
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---

# <a name="entering-data"></a><span data-ttu-id="361a9-104">Introducción de datos</span><span class="sxs-lookup"><span data-stu-id="361a9-104">Entering Data</span></span>
<span data-ttu-id="361a9-105">Hay varias funciones generales que le pueden ayudar a introducir datos de manera rápida y fácil.</span><span class="sxs-lookup"><span data-stu-id="361a9-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="361a9-106">Las funciones generales para la introducción de datos se describen en este artículo.</span><span class="sxs-lookup"><span data-stu-id="361a9-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="361a9-107">Los ejemplos de este producto utilizan los datos de demostración.</span><span class="sxs-lookup"><span data-stu-id="361a9-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="361a9-108">Campos obligatorios</span><span class="sxs-lookup"><span data-stu-id="361a9-108">Mandatory Fields</span></span>
<span data-ttu-id="361a9-109">Cuando se introducen datos en páginas, determinados campos aparecen marcados con un asterisco de color rojo.</span><span class="sxs-lookup"><span data-stu-id="361a9-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="361a9-110">El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.</span><span class="sxs-lookup"><span data-stu-id="361a9-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="361a9-111">Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página.</span><span class="sxs-lookup"><span data-stu-id="361a9-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="361a9-112">El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.</span><span class="sxs-lookup"><span data-stu-id="361a9-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="361a9-113">Buscar datos al escribir</span><span class="sxs-lookup"><span data-stu-id="361a9-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="361a9-114">Cuando comience a escribir caracteres en un campo, aparecerá una lista desplegable que muestra los posibles valores de campo.</span><span class="sxs-lookup"><span data-stu-id="361a9-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="361a9-115">Esta lista cambia a medida que escriba caracteres adicionales y puede seleccionar el valor correcto cuando aparezca.</span><span class="sxs-lookup"><span data-stu-id="361a9-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="361a9-116">Muchos campos tienen un botón de flecha hacia abajo que puede elegir.</span><span class="sxs-lookup"><span data-stu-id="361a9-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="361a9-117">Seleccione la flecha para desplegar una lista de datos que están disponibles para su introducción en el campo.</span><span class="sxs-lookup"><span data-stu-id="361a9-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="361a9-118">El botón tiene dos funciones, según el tipo de campo:</span><span class="sxs-lookup"><span data-stu-id="361a9-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="361a9-119">Búsqueda: muestra información de otra tabla, que puede introducir en el campo.</span><span class="sxs-lookup"><span data-stu-id="361a9-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="361a9-120">Puede seleccionar un elemento de datos a la vez.</span><span class="sxs-lookup"><span data-stu-id="361a9-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="361a9-121">Desplegable: muestra el conjunto de opciones que existe para el campo.</span><span class="sxs-lookup"><span data-stu-id="361a9-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="361a9-122">Sólo puede seleccionar una de las opciones.</span><span class="sxs-lookup"><span data-stu-id="361a9-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="361a9-123">Introducir cantidades por cálculo</span><span class="sxs-lookup"><span data-stu-id="361a9-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="361a9-124">Al introducir números en campos de cantidad, como el campo **Cantidad** de una línea de diario de producto, puede introducir la fórmula en lugar de la cantidad de la suma.</span><span class="sxs-lookup"><span data-stu-id="361a9-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="361a9-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="361a9-125">Examples</span></span>  

-   <span data-ttu-id="361a9-126">Si introduce 19+19, el campo se calcula para obtener el valor 38.</span><span class="sxs-lookup"><span data-stu-id="361a9-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="361a9-127">Si introduce 41-9, el campo se calcula para obtener el valor 32.</span><span class="sxs-lookup"><span data-stu-id="361a9-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="361a9-128">Si introduce 12\*4, el campo se calcula para obtener el valor 48.</span><span class="sxs-lookup"><span data-stu-id="361a9-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="361a9-129">Si introduce 12/4, el campo se calcula para obtener el valor 3.</span><span class="sxs-lookup"><span data-stu-id="361a9-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="361a9-130">Especificación de números negativos</span><span class="sxs-lookup"><span data-stu-id="361a9-130">Entering Negative Numbers</span></span>
<span data-ttu-id="361a9-131">Puede especificar números negativos de dos formas.</span><span class="sxs-lookup"><span data-stu-id="361a9-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="361a9-132">El número -20,5 se puede especificar como:</span><span class="sxs-lookup"><span data-stu-id="361a9-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="361a9-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="361a9-133">-20.5</span></span>  

    <span data-ttu-id="361a9-134">O</span><span class="sxs-lookup"><span data-stu-id="361a9-134">or</span></span>
-   <span data-ttu-id="361a9-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="361a9-135">20.5-</span></span>  

 <span data-ttu-id="361a9-136">En ambos casos, el importe se registrará como -20,5.</span><span class="sxs-lookup"><span data-stu-id="361a9-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="361a9-137">Si el último carácter de la expresión es **+** o **-**, la expresión completa se registrará con ese signo.</span><span class="sxs-lookup"><span data-stu-id="361a9-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="361a9-138">Ejemplo, **10-20+** dará como resultado 10 y no -10.</span><span class="sxs-lookup"><span data-stu-id="361a9-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="361a9-139">Introducir fechas y horas</span><span class="sxs-lookup"><span data-stu-id="361a9-139">Entering Dates and Times</span></span>
<span data-ttu-id="361a9-140">Puede especificar fechas y horas en todos los campos diseñados específicamente para las fechas (campos de fecha).</span><span class="sxs-lookup"><span data-stu-id="361a9-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="361a9-141">Las fechas pueden escribirse con o sin separadores.</span><span class="sxs-lookup"><span data-stu-id="361a9-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="361a9-142">La forma de especificar las fechas y horas depende de los valores **Región**.</span><span class="sxs-lookup"><span data-stu-id="361a9-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="361a9-143">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="361a9-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="361a9-144">Introducción de fechas</span><span class="sxs-lookup"><span data-stu-id="361a9-144">Entering Dates</span></span>  
 <span data-ttu-id="361a9-145">En un campo de fecha, puede introducir dos, cuatro, seis u ocho dígitos:</span><span class="sxs-lookup"><span data-stu-id="361a9-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="361a9-146">Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="361a9-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="361a9-147">Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="361a9-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="361a9-148">Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1930 y el 31/12/2029, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="361a9-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="361a9-149">También es posible introducir una fecha como un día de la semana, seguido de un número de la semana y, opcionalmente, un año (por ejemplo, Lun25 o lun25 significa lunes de la semana 25).</span><span class="sxs-lookup"><span data-stu-id="361a9-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="361a9-150">En lugar de introducir una fecha específica, puede introducir uno de dos códigos.</span><span class="sxs-lookup"><span data-stu-id="361a9-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="361a9-151">Código</span><span class="sxs-lookup"><span data-stu-id="361a9-151">Code</span></span>|<span data-ttu-id="361a9-152">Resultado</span><span class="sxs-lookup"><span data-stu-id="361a9-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="361a9-153">h</span><span class="sxs-lookup"><span data-stu-id="361a9-153">t</span></span>|<span data-ttu-id="361a9-154">Esto es la fecha de hoy (la fecha de sistema del equipo).</span><span class="sxs-lookup"><span data-stu-id="361a9-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="361a9-155">t</span><span class="sxs-lookup"><span data-stu-id="361a9-155">w</span></span>|<span data-ttu-id="361a9-156">Esta es la fecha de trabajo que está configurada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="361a9-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="361a9-157">Para cambiar la fecha de trabajo, vea [Cambiar la configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="361a9-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="361a9-158">Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.</span><span class="sxs-lookup"><span data-stu-id="361a9-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="361a9-159">Introducción de horas</span><span class="sxs-lookup"><span data-stu-id="361a9-159">Entering Times</span></span>  
 <span data-ttu-id="361a9-160">Cuando introduzca horas, puede insertar cualquier signo separador entre las unidades, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="361a9-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="361a9-161">No necesita escribir los minutos, los segundo ni AM/PM.</span><span class="sxs-lookup"><span data-stu-id="361a9-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="361a9-162">En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="361a9-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="361a9-163">Movimiento</span><span class="sxs-lookup"><span data-stu-id="361a9-163">Entry</span></span>|<span data-ttu-id="361a9-164">Interpretación</span><span class="sxs-lookup"><span data-stu-id="361a9-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="361a9-165">5</span><span class="sxs-lookup"><span data-stu-id="361a9-165">5</span></span>|<span data-ttu-id="361a9-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-166">05:00:00</span></span>|  
|<span data-ttu-id="361a9-167">5:30</span><span class="sxs-lookup"><span data-stu-id="361a9-167">5:30</span></span>|<span data-ttu-id="361a9-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="361a9-168">05:30:00</span></span>|  
|<span data-ttu-id="361a9-169">0530</span><span class="sxs-lookup"><span data-stu-id="361a9-169">0530</span></span>|<span data-ttu-id="361a9-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="361a9-170">05:30:00</span></span>|  
|<span data-ttu-id="361a9-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="361a9-171">5:30:5</span></span>|<span data-ttu-id="361a9-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="361a9-172">05:30:05</span></span>|  
|<span data-ttu-id="361a9-173">053005</span><span class="sxs-lookup"><span data-stu-id="361a9-173">053005</span></span>|<span data-ttu-id="361a9-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="361a9-174">05:30:05</span></span>|  
|<span data-ttu-id="361a9-175">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="361a9-175">5:30:5,50</span></span>|<span data-ttu-id="361a9-176">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="361a9-176">05:30:05.5</span></span>|  
|<span data-ttu-id="361a9-177">053005050</span><span class="sxs-lookup"><span data-stu-id="361a9-177">053005050</span></span>|<span data-ttu-id="361a9-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="361a9-178">05:30:05.05</span></span>|  

 <span data-ttu-id="361a9-179">Debe introducir dos dígitos para cada unidad de tiempo si no escribe ningún separador.</span><span class="sxs-lookup"><span data-stu-id="361a9-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="361a9-180">Introducción de fechas/horas</span><span class="sxs-lookup"><span data-stu-id="361a9-180">Entering Datetimes</span></span>  
 <span data-ttu-id="361a9-181">Cuando introduzca fechas y horas, debe introducir un espacio en blanco entre la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="361a9-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="361a9-182">En la tabla siguiente se muestran varias formas de introducir fechas y horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="361a9-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="361a9-183">Movimiento</span><span class="sxs-lookup"><span data-stu-id="361a9-183">Entry</span></span>|<span data-ttu-id="361a9-184">Interpretación</span><span class="sxs-lookup"><span data-stu-id="361a9-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="361a9-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="361a9-185">131202 132455</span></span>|<span data-ttu-id="361a9-186">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="361a9-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="361a9-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="361a9-187">1-12-02 10</span></span>|<span data-ttu-id="361a9-188">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="361a9-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="361a9-189">1.12.02 5</span></span>|<span data-ttu-id="361a9-190">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="361a9-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="361a9-191">1.12.02</span></span>|<span data-ttu-id="361a9-192">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="361a9-193">11 12</span><span class="sxs-lookup"><span data-stu-id="361a9-193">11 12</span></span>|<span data-ttu-id="361a9-194">11-mes actual-año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="361a9-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="361a9-195">1112 12</span></span>|<span data-ttu-id="361a9-196">11-12-año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="361a9-197">h u hoy</span><span class="sxs-lookup"><span data-stu-id="361a9-197">t or today</span></span>|<span data-ttu-id="361a9-198">fecha de hoy 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="361a9-199">h hora</span><span class="sxs-lookup"><span data-stu-id="361a9-199">t time</span></span>|<span data-ttu-id="361a9-200">fecha de hoy hora real</span><span class="sxs-lookup"><span data-stu-id="361a9-200">today's date actual time</span></span>|  
|<span data-ttu-id="361a9-201">h 10:30</span><span class="sxs-lookup"><span data-stu-id="361a9-201">t 10:30</span></span>|<span data-ttu-id="361a9-202">fecha de hoy 10:30:00</span><span class="sxs-lookup"><span data-stu-id="361a9-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="361a9-203">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="361a9-203">t 3:3:3</span></span>|<span data-ttu-id="361a9-204">fecha de hoy 03:03:03</span><span class="sxs-lookup"><span data-stu-id="361a9-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="361a9-205">t o fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="361a9-205">w or workdate</span></span>|<span data-ttu-id="361a9-206">la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="361a9-207">l o lunes</span><span class="sxs-lookup"><span data-stu-id="361a9-207">m or Monday</span></span>|<span data-ttu-id="361a9-208">Lunes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-209">ma o martes</span><span class="sxs-lookup"><span data-stu-id="361a9-209">tu or Tuesday</span></span>|<span data-ttu-id="361a9-210">Martes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-211">mi o miércoles</span><span class="sxs-lookup"><span data-stu-id="361a9-211">we or Wednesday</span></span>|<span data-ttu-id="361a9-212">Miércoles de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-213">ju o jueves</span><span class="sxs-lookup"><span data-stu-id="361a9-213">th or Thursday</span></span>|<span data-ttu-id="361a9-214">Jueves de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-215">v o viernes</span><span class="sxs-lookup"><span data-stu-id="361a9-215">f or Friday</span></span>|<span data-ttu-id="361a9-216">Viernes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-217">s o sábado</span><span class="sxs-lookup"><span data-stu-id="361a9-217">s or Saturday</span></span>|<span data-ttu-id="361a9-218">Sábado de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-219">do o domingo</span><span class="sxs-lookup"><span data-stu-id="361a9-219">su or Sunday</span></span>|<span data-ttu-id="361a9-220">Domingo de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="361a9-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="361a9-221">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="361a9-221">tu 10:30</span></span>|<span data-ttu-id="361a9-222">Martes de la semana actual 10:30:00</span><span class="sxs-lookup"><span data-stu-id="361a9-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="361a9-223">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="361a9-223">tu 3:3:3</span></span>|<span data-ttu-id="361a9-224">Martes de la semana actual 03:03:03</span><span class="sxs-lookup"><span data-stu-id="361a9-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="361a9-225">Introducción de duración</span><span class="sxs-lookup"><span data-stu-id="361a9-225">Entering Duration</span></span>  
 <span data-ttu-id="361a9-226">Introduzca un periodo de tiempo como un número seguido de su unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="361a9-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="361a9-227">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="361a9-227">Here are some examples.</span></span>  

|<span data-ttu-id="361a9-228">Duración</span><span class="sxs-lookup"><span data-stu-id="361a9-228">Duration</span></span>|<span data-ttu-id="361a9-229">Unidad de medida\*\*</span><span class="sxs-lookup"><span data-stu-id="361a9-229">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="361a9-230">2h</span><span class="sxs-lookup"><span data-stu-id="361a9-230">2h</span></span>|<span data-ttu-id="361a9-231">2 hrs</span><span class="sxs-lookup"><span data-stu-id="361a9-231">2 hrs</span></span>|  
|<span data-ttu-id="361a9-232">6h 30 m</span><span class="sxs-lookup"><span data-stu-id="361a9-232">6h 30 m</span></span>|<span data-ttu-id="361a9-233">6 hrs 30 mins</span><span class="sxs-lookup"><span data-stu-id="361a9-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="361a9-234">6,5h</span><span class="sxs-lookup"><span data-stu-id="361a9-234">6.5h</span></span>|<span data-ttu-id="361a9-235">6 h 30 min</span><span class="sxs-lookup"><span data-stu-id="361a9-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="361a9-236">90m</span><span class="sxs-lookup"><span data-stu-id="361a9-236">90m</span></span>|<span data-ttu-id="361a9-237">1 hr 30 mins</span><span class="sxs-lookup"><span data-stu-id="361a9-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="361a9-238">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="361a9-238">2d 6h 30m</span></span>|<span data-ttu-id="361a9-239">2 días 6 hrs 30 mins</span><span class="sxs-lookup"><span data-stu-id="361a9-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="361a9-240">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="361a9-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="361a9-241">2 días 6 hrs 30 mins 56 segs 600 msegs</span><span class="sxs-lookup"><span data-stu-id="361a9-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="361a9-242">También puede introducir un número y se convertirá automáticamente en un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="361a9-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="361a9-243">El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.</span><span class="sxs-lookup"><span data-stu-id="361a9-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="361a9-244">Para ver la unidad de medida que se va a usar en un campo Duración, introduzca un número y observe a qué unidad de medida se convierte.</span><span class="sxs-lookup"><span data-stu-id="361a9-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="361a9-245">El número 5 se convierte a 5 hrs, si la unidad de medida es horas.</span><span class="sxs-lookup"><span data-stu-id="361a9-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

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

## <a name="using-date-formulas"></a><span data-ttu-id="361a9-246">Uso de fórmulas de fecha</span><span class="sxs-lookup"><span data-stu-id="361a9-246">Using Date Formulas</span></span>  
 <span data-ttu-id="361a9-247">Una fórmula de fecha es una breve combinación abreviada de letras y números que especifica cómo calcular fechas.</span><span class="sxs-lookup"><span data-stu-id="361a9-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="361a9-248">Puede especificar las fórmulas en diversos campos de cálculo de fechas y en campos de frecuencia periódicos y en diarios periódicos.</span><span class="sxs-lookup"><span data-stu-id="361a9-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="361a9-249">En todos los campos de fórmulas de datos, un día se incluye automáticamente para cubrir el día de hoy como fecha en que comienza el periodo.</span><span class="sxs-lookup"><span data-stu-id="361a9-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="361a9-250">Por consiguiente, si introduce 1s, por ejemplo, el periodo comprende en realidad ocho días porque hoy está incluido.</span><span class="sxs-lookup"><span data-stu-id="361a9-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="361a9-251">Para especificar un periodo de siete días (una semana verdadera) con la fecha inicial del periodo, debe introducir 6D o 1W-1D.</span><span class="sxs-lookup"><span data-stu-id="361a9-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="361a9-252">A continuación se incluye algunos ejemplos de cómo se pueden usar las fórmulas de fechas:</span><span class="sxs-lookup"><span data-stu-id="361a9-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="361a9-253">La fórmula de fecha del campo de frecuencia periódica en los diarios periódicos determina con qué frecuencia se registrará el movimiento de la línea de diario.</span><span class="sxs-lookup"><span data-stu-id="361a9-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="361a9-254">La fórmula de fecha del campo Periodo gracia para un determinado nivel de recordatorio determina el periodo de tiempo que debe transcurrir, desde la fecha de vencimiento (o desde la fecha del recordatorio anterior), antes de que se cree un recordatorio.</span><span class="sxs-lookup"><span data-stu-id="361a9-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="361a9-255">La fórmula de fechas del campo Cálculo de fecha de vencimiento determina cómo calcular la fecha de vencimiento en el recordatorio.</span><span class="sxs-lookup"><span data-stu-id="361a9-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="361a9-256">La fórmula para el cálculo de fechas puede contener un máximo de 20 caracteres, números y letras.</span><span class="sxs-lookup"><span data-stu-id="361a9-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="361a9-257">Puede usar las siguientes letras, que son abreviaturas para especificaciones de tiempo.</span><span class="sxs-lookup"><span data-stu-id="361a9-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-258">C</span><span class="sxs-lookup"><span data-stu-id="361a9-258">C</span></span>|<span data-ttu-id="361a9-259">Presente</span><span class="sxs-lookup"><span data-stu-id="361a9-259">Current</span></span>|  
|<span data-ttu-id="361a9-260">D</span><span class="sxs-lookup"><span data-stu-id="361a9-260">D</span></span>|<span data-ttu-id="361a9-261">Día(s)</span><span class="sxs-lookup"><span data-stu-id="361a9-261">Day(s)</span></span>|  
|<span data-ttu-id="361a9-262">S</span><span class="sxs-lookup"><span data-stu-id="361a9-262">W</span></span>|<span data-ttu-id="361a9-263">Semana(s)</span><span class="sxs-lookup"><span data-stu-id="361a9-263">Week(s)</span></span>|  
|<span data-ttu-id="361a9-264">M</span><span class="sxs-lookup"><span data-stu-id="361a9-264">M</span></span>|<span data-ttu-id="361a9-265">Mes(es)</span><span class="sxs-lookup"><span data-stu-id="361a9-265">Month(s)</span></span>|  
|<span data-ttu-id="361a9-266">T</span><span class="sxs-lookup"><span data-stu-id="361a9-266">Q</span></span>|<span data-ttu-id="361a9-267">Trimestre(s)</span><span class="sxs-lookup"><span data-stu-id="361a9-267">Quarter(s)</span></span>|  
|<span data-ttu-id="361a9-268">A</span><span class="sxs-lookup"><span data-stu-id="361a9-268">Y</span></span>|<span data-ttu-id="361a9-269">Año(s)</span><span class="sxs-lookup"><span data-stu-id="361a9-269">Year(s)</span></span>|  

 <span data-ttu-id="361a9-270">Puede construir una fórmula de fecha de tres formas.</span><span class="sxs-lookup"><span data-stu-id="361a9-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="361a9-271">El ejemplo siguiente muestra un número actual y más una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="361a9-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-272">PS</span><span class="sxs-lookup"><span data-stu-id="361a9-272">CW</span></span>|<span data-ttu-id="361a9-273">Presente semana</span><span class="sxs-lookup"><span data-stu-id="361a9-273">Current week</span></span>|  
|<span data-ttu-id="361a9-274">PM</span><span class="sxs-lookup"><span data-stu-id="361a9-274">CM</span></span>|<span data-ttu-id="361a9-275">Presente mes</span><span class="sxs-lookup"><span data-stu-id="361a9-275">Current month</span></span>|  

 <span data-ttu-id="361a9-276">El ejemplo siguiente muestra un número y una unidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="361a9-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="361a9-277">Un número no puede ser superior a 9999.</span><span class="sxs-lookup"><span data-stu-id="361a9-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-278">10D</span><span class="sxs-lookup"><span data-stu-id="361a9-278">10D</span></span>|<span data-ttu-id="361a9-279">10 días a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="361a9-279">10 days from today</span></span>|  
|<span data-ttu-id="361a9-280">2S</span><span class="sxs-lookup"><span data-stu-id="361a9-280">2W</span></span>|<span data-ttu-id="361a9-281">2 semanas a partir de hoy</span><span class="sxs-lookup"><span data-stu-id="361a9-281">2 weeks from today</span></span>|  

 <span data-ttu-id="361a9-282">El ejemplo siguiente muestra una unidad de tiempo y un número.</span><span class="sxs-lookup"><span data-stu-id="361a9-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-283">D10</span><span class="sxs-lookup"><span data-stu-id="361a9-283">D10</span></span>|<span data-ttu-id="361a9-284">El siguiente día 10 de un mes</span><span class="sxs-lookup"><span data-stu-id="361a9-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="361a9-285">DS4</span><span class="sxs-lookup"><span data-stu-id="361a9-285">WD4</span></span>|<span data-ttu-id="361a9-286">El siguiente día 4 de una semana (jueves)</span><span class="sxs-lookup"><span data-stu-id="361a9-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="361a9-287">En el ejemplo siguiente se muestra cómo puede combinar estas tres formas, según la necesidad.</span><span class="sxs-lookup"><span data-stu-id="361a9-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-288">PM+10D</span><span class="sxs-lookup"><span data-stu-id="361a9-288">CM+10D</span></span>|<span data-ttu-id="361a9-289">Presente mes + 10 días</span><span class="sxs-lookup"><span data-stu-id="361a9-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="361a9-290">El ejemplo siguiente muestra cómo utilizar un signo menos para indicar una fecha del pasado.</span><span class="sxs-lookup"><span data-stu-id="361a9-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="361a9-291">-1A</span><span class="sxs-lookup"><span data-stu-id="361a9-291">-1Y</span></span>|<span data-ttu-id="361a9-292">Hace un año desde hoy</span><span class="sxs-lookup"><span data-stu-id="361a9-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="361a9-293">Consulte también</span><span class="sxs-lookup"><span data-stu-id="361a9-293">See Also</span></span>  
 [<span data-ttu-id="361a9-294">Buscar, filtrar y ordenar datos</span><span class="sxs-lookup"><span data-stu-id="361a9-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="361a9-295">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="361a9-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

