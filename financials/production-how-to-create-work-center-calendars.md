---
title: "Cómo configurar calendarios de planta | Documentos de Microsoft"
description: "Un calendario del centro de trabajo especifica los días y las horas laborables, las vacaciones y las ausencias que determinan la capacidad bruta disponible del centro de trabajo, medida en tiempo, de acuerdo con los valores de eficiencia y de capacidad definidos. La creación y la activación de un calendario de centro de trabajo implica una serie de tareas previas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cf54f63e94ab3249f30d2fcdbef2c35e323e4cd8
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="2c9bb-104">Configurar calendarios de planta</span><span class="sxs-lookup"><span data-stu-id="2c9bb-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="2c9bb-105">Un calendario del centro de trabajo o de máquina especifica los días y las horas laborables, las vacaciones y las ausencias que determinan la capacidad disponible bruta del centro de trabajo, medida en tiempo, de acuerdo con los valores de eficiencia y capacidad definidos.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="2c9bb-106">Como requisito para calcular el calendario de un centro de trabajo o de máquina específico, deben definirse primero uno o varios calendarios generales de planta.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="2c9bb-107">Los calendarios de planta definen la semana de trabajo estándar en términos de horas de inicio y fin de cada día laborable y la relación con los turnos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="2c9bb-108">Asimismo, los calendarios de planta definen los días festivos fijos durante el año.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="2c9bb-109">A continuación se describe cómo configurar calendarios de centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="2c9bb-110">Los pasos son parecidos al configurar los calendarios de centro de máquina.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="2c9bb-111">Para crear turnos de trabajo</span><span class="sxs-lookup"><span data-stu-id="2c9bb-111">To create work shifts</span></span>  
1.  <span data-ttu-id="2c9bb-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Turnos de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2c9bb-113">En una línea en blanco, escriba un número en el campo **Código** que identifique el turno de trabajo, por ejemplo, **1**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="2c9bb-114">Describa el turno de trabajo en el campo **Descripción**, por ejemplo, **Primer turno**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="2c9bb-115">Opcionalmente, rellene las líneas para un segundo o tercer turno de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="2c9bb-116">Aunque en los centros de trabajo no se trabaje en diferentes turnos, introduzca al menos un código de turno.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="2c9bb-117">Para configurar un calendario de planta</span><span class="sxs-lookup"><span data-stu-id="2c9bb-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="2c9bb-118">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Calendarios de planta** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2c9bb-119">En una línea en blanco, escriba un número en el campo **Código** que identifique el calendario de planta.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="2c9bb-120">Describa el calendario de planta en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="2c9bb-121">Seleccione la acción **Días laborables**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="2c9bb-122">En la ventana **Días laborables de calendario planta**, defina una semana laborable completa, con el comienzo y finalización para cada día.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-122">In the **Shop Calendar Working Days** window, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="2c9bb-123">En el campo **Cód. turno trabajo**, seleccione uno de los turnos definidos previamente.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="2c9bb-124">Agregue una línea para cada día laborable y cada turno.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="2c9bb-125">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2c9bb-125">For example:</span></span>  

    <span data-ttu-id="2c9bb-126">Lunes 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="2c9bb-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="2c9bb-127">Martes 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="2c9bb-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="2c9bb-128">Si necesita crear un calendario de planta con dos turnos de trabajo, debe rellenar los datos de esta manera:</span><span class="sxs-lookup"><span data-stu-id="2c9bb-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="2c9bb-129">Lunes 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="2c9bb-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="2c9bb-130">Lunes 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="2c9bb-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="2c9bb-131">Martes 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="2c9bb-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="2c9bb-132">Martes 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="2c9bb-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="2c9bb-133">Los días de semana que no defina en el calendario de planta, como sábado y domingo, se consideran días no laborables y tendrán una capacidad disponible de cero en el calendario de un centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="2c9bb-134">Una vez definidos todos los días laborables de una semana, puede cerrar la ventana **Días labor. calendario planta** y empezar a especificar las vacaciones.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** window and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="2c9bb-135">En la ventana **Calendarios de planta**, seleccione el calendario de planta y, después, seleccione la acción **Vacaciones**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-135">In the **Shop Calendars** window, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="2c9bb-136">En la ventana **Calendario de vacaciones de planta**, defina las vacaciones del año, especificando la fecha y la hora inicial, la hora final y una descripción de cada día festivo en distintas líneas.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-136">In the **Shop Calendar Holidays** window, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="2c9bb-137">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2c9bb-137">For example:</span></span>  

    <span data-ttu-id="2c9bb-138">04/07/14 0:00:00 23:59:00 Vacaciones de verano</span><span class="sxs-lookup"><span data-stu-id="2c9bb-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="2c9bb-139">05/07/14 0:00:00 23:59:00 Vacaciones de verano</span><span class="sxs-lookup"><span data-stu-id="2c9bb-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="2c9bb-140">06/07/14 0:00:00 23:59:00 Vacaciones de verano</span><span class="sxs-lookup"><span data-stu-id="2c9bb-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="2c9bb-141">Las vacaciones definidas tendrán una capacidad disponible de cero en el calendario del centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="2c9bb-142">El calendario de planta se puede asignar ahora a un centro de trabajo para calcular el calendario laborable que regirá la programación de todas las operaciones en dicho centro.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="2c9bb-143">Para calcular un calendario de centro de trabajo</span><span class="sxs-lookup"><span data-stu-id="2c9bb-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="2c9bb-144">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Centros de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="2c9bb-145">Abra el centro de trabajo que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="2c9bb-146">En la el campo **Código de calendario de planta**, seleccione qué calendario de planta se va a utilizar como base de un calendario de centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="2c9bb-147">Elija la acción **Calendario**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="2c9bb-148">En la ventana **Calendario de centro de trabajo**, elija la acción **Mostrar matriz**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-148">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="2c9bb-149">En el margen izquierdo de la ventana de matriz se incluyen los centros de trabajo definidos.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-149">The left side of the matrix window lists the work centers that are set up.</span></span> <span data-ttu-id="2c9bb-150">En el margen derecho, se muestra un calendario en el que se indican los valores de capacidad disponible para cada día laborable en la unidad de medida definida, por ejemplo, **480** minutos.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="2c9bb-151">Cada línea representa el calendario de un centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2c9bb-152">También puede ver los valores de capacidad de cada semana o mes al cambiar la selección en el campo **Ver por** de la ventana **Calendario centro trabajo**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field in the **Work Center Calendar** window.</span></span>  

    <span data-ttu-id="2c9bb-153">Para reflejar el nuevo calendario de planta como una línea en el centro de trabajo seleccionado, primero se debe calcular.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="2c9bb-154">Elija la acción **Calcular**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="2c9bb-155">En la ficha desplegable **Centro trabajo**, puede definir un filtro para realizar los cálculos de un solo centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="2c9bb-156">Si no define un filtro, se calcularán todos los calendarios de los centro de trabajo existentes.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="2c9bb-157">Defina las fechas de inicio y de finalización del periodo del calendario que debe calcularse, por ejemplo, un año, del 01/01/14 al 31/12/14.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="2c9bb-158">Elija el botón **Aceptar** para calcular la capacidad.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="2c9bb-159">Ahora se crearán o actualizarán los movimientos del calendario para mostrar la capacidad disponible para cada periodo de acuerdo con los tres grupos de datos maestros siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c9bb-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="2c9bb-160">Los días laborables y los turnos definidos en el calendario de planta asignado.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="2c9bb-161">El valor del campo **Capacidad** de la ficha centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="2c9bb-162">El valor del campo **Eficiencia** de la ficha de centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="2c9bb-163">El calendario calculado del centro de trabajo definirá ahora cuándo y cuánta capacidad hay disponible en este centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="2c9bb-164">Esto controla la programación detallada de las operaciones realizadas en el centro de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="2c9bb-165">Para registrar las ausencias en el centro de trabajo</span><span class="sxs-lookup"><span data-stu-id="2c9bb-165">To record work center absence</span></span>  
1.  <span data-ttu-id="2c9bb-166">En la ventana **Calendario de centro de trabajo**, elija la acción **Mostrar matriz**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-166">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="2c9bb-167">En la ventana **Matriz de calendario de centro de trabajo**, seleccione el centro de trabajo y el día de calendario donde debe registrarse el tiempo de ausencia y, a continuación, seleccione la acción **Ausencia**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-167">In the **Work Center Calendar Matrix** window, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="2c9bb-168">En la ventana **Ausencia**, defina la hora de inicio, la hora de finalización y la descripción del día de ausencia.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-168">In the **Absence** window, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="2c9bb-169">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2c9bb-169">For example:</span></span>  

    <span data-ttu-id="2c9bb-170">25/01/01 08:00 10:00 Mantenimiento</span><span class="sxs-lookup"><span data-stu-id="2c9bb-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="2c9bb-171">Seleccione la acción **Actualizar** y luego cierre la ventana **Ausencia**.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-171">Choose the **Update** action, and then close the **Absence** window.</span></span>  

<span data-ttu-id="2c9bb-172">El tiempo de ausencia registrado se reduce de la capacidad del día seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2c9bb-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c9bb-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c9bb-173">See Also</span></span>  
[<span data-ttu-id="2c9bb-174">Configurar calendarios base</span><span class="sxs-lookup"><span data-stu-id="2c9bb-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="2c9bb-175">Configuración de centros de trabajo y centros de máquinas</span><span class="sxs-lookup"><span data-stu-id="2c9bb-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="2c9bb-176">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="2c9bb-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="2c9bb-177">Fabricación</span><span class="sxs-lookup"><span data-stu-id="2c9bb-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="2c9bb-178">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c9bb-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

