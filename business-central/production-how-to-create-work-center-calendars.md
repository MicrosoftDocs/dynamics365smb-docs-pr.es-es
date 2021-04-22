---
title: Cómo configurar calendarios de planta | Documentos de Microsoft
description: Un calendario del centro de trabajo especifica los días y las horas laborables, las vacaciones y las ausencias que determinan la capacidad bruta disponible del centro de trabajo, medida en tiempo, de acuerdo con los valores de eficiencia y de capacidad definidos. La creación y la activación de un calendario de centro de trabajo implica una serie de tareas previas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e542d67f3cd0516cf435b0a7110e50431aab1a1f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781954"
---
# <a name="set-up-shop-calendars"></a>Configurar calendarios de planta
Un calendario del centro de trabajo o de máquina especifica los días y las horas laborables, las vacaciones y las ausencias que determinan la capacidad disponible bruta del centro de trabajo, medida en tiempo, de acuerdo con los valores de eficiencia y capacidad definidos.

Como requisito para calcular el calendario de un centro de trabajo o de máquina específico, deben definirse primero uno o varios calendarios generales de planta. Los calendarios de planta definen la semana de trabajo estándar en términos de horas de inicio y fin de cada día laborable y la relación con los turnos de trabajo. Asimismo, los calendarios de planta definen los días festivos fijos durante el año.  

A continuación se describe cómo configurar calendarios de centro de trabajo. Los pasos son parecidos al configurar los calendarios de centro de máquina.  

## <a name="to-create-work-shifts"></a>Para crear turnos de trabajo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Turnos trabajo** y luego elija el enlace relacionado.  
2.  En una línea en blanco, escriba un número en el campo **Código** que identifique el turno de trabajo, por ejemplo, **1**.  
3.  Describa el turno de trabajo en el campo **Descripción**, por ejemplo, **Primer turno**.  
4.  Opcionalmente, rellene las líneas para un segundo o tercer turno de trabajo.  

Aunque en los centros de trabajo no se trabaje en diferentes turnos, introduzca al menos un código de turno.  

## <a name="to-set-up-a-shop-calendar"></a>Para configurar un calendario de planta  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Calendarios planta** y luego elija el enlace relacionado.  
2.  En una línea en blanco, escriba un número en el campo **Código** que identifique el calendario de planta.  
3.  Describa el calendario de planta en el campo **Descripción**.  
4.  Seleccione la acción **Días laborables**.
5.  En la página **Días laborables de calendario planta**, defina una semana laborable completa, con el comienzo y finalización para cada día.  

    En el campo **Cód. turno trabajo**, seleccione uno de los turnos definidos previamente. Agregue una línea para cada día laborable y cada turno. Por ejemplo:  

    Lunes 07:00 15:00 1   
    Martes 07:00 15:00 1  

    Si necesita crear un calendario de planta con dos turnos de trabajo, debe rellenar los datos de esta manera:  

    Lunes 07:00 15:00 1   
    Lunes 15:00 23:00 2  
    Martes 07:00 15:00 1  
    Martes 15:00 23:00 2  

    Los días de semana que no defina en el calendario de planta, como sábado y domingo, se consideran días no laborables y tendrán una capacidad disponible de cero en el calendario de un centro de trabajo.  

    Una vez definidos todos los días laborables de una semana, puede cerrar la página **Días labor. calendario planta** y empezar a especificar las vacaciones:  

6.  En la página **Calendarios de planta**, seleccione el calendario de planta y, después, seleccione la acción **Vacaciones**.
7. En la página **Calendario de vacaciones de planta**, defina las vacaciones del año, especificando la fecha y la hora inicial, la hora final y una descripción de cada día festivo en distintas líneas. Por ejemplo:  

    04/07/14 0:00:00 23:59:00 Vacaciones de verano  
    05/07/14 0:00:00 23:59:00 Vacaciones de verano  
    06/07/14 0:00:00 23:59:00 Vacaciones de verano  

Las vacaciones definidas tendrán una capacidad disponible de cero en el calendario del centro de trabajo.  

El calendario de planta se puede asignar ahora a un centro de trabajo para calcular el calendario laborable que regirá la programación de todas las operaciones en dicho centro.  

## <a name="to-calculate-a-work-center-calendar"></a>Para calcular un calendario de centro de trabajo  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Centros de trabajo** y luego elija el enlace relacionado.
2. Abra el centro de trabajo que desea actualizar.  
3. En la el campo **Código de calendario de planta**, seleccione qué calendario de planta se va a utilizar como base de un calendario de centro de trabajo.  
4. Elija la acción **Calendario**.  
5. En la página **Calendario de centro de trabajo**, elija la acción **Mostrar matriz**.  

    En el margen izquierdo de la página de matriz se incluyen los centros de trabajo definidos. En el margen derecho, se muestra un calendario en el que se indican los valores de capacidad disponible para cada día laborable en la unidad de medida definida, por ejemplo, **480** minutos. Cada línea representa el calendario de un centro de trabajo.  

    > [!NOTE]  
    >  También puede ver los valores de capacidad de cada semana o mes al cambiar la selección en el campo **Ver por** de la página **Calendario centro trabajo**.  

    Para reflejar el nuevo calendario de planta como una línea en el centro de trabajo seleccionado, primero se debe calcular.  

6.  Elija la acción **Calcular**.  
7.  En la ficha desplegable **Centro trabajo**, puede definir un filtro para realizar los cálculos de un solo centro de trabajo. Si no define un filtro, se calcularán todos los calendarios de los centro de trabajo existentes.  
8.  Defina las fechas de inicio y de finalización del periodo del calendario que debe calcularse, por ejemplo, un año, del 01/01/14 al 31/12/14.
9. Elija el botón **Aceptar** para calcular la capacidad.  

Ahora se crearán o actualizarán los movimientos del calendario para mostrar la capacidad disponible para cada periodo de acuerdo con los tres grupos de datos maestros siguientes:  

- Los días laborables y los turnos definidos en el calendario de planta asignado.  
- El valor del campo **Capacidad** de la ficha centro de trabajo.  
- El valor del campo **Eficiencia** de la ficha de centro de trabajo.  

El calendario calculado del centro de trabajo definirá ahora cuándo y cuánta capacidad hay disponible en este centro de trabajo. Esto controla la programación detallada de las operaciones realizadas en el centro de trabajo.  

## <a name="to-record-work-center-absence"></a>Para registrar las ausencias en el centro de trabajo  
1.  En la página **Calendario de centro de trabajo**, elija la acción **Mostrar matriz**.
2. En la página **Matriz de calendario de centro de trabajo**, seleccione el centro de trabajo y el día de calendario donde debe registrarse el tiempo de ausencia y, a continuación, seleccione la acción **Ausencia**.  
3.  En la página **Ausencia**, defina la hora de inicio, la hora de finalización y la descripción del día de ausencia. Por ejemplo:  

    25/01/01 08:00 10:00 Mantenimiento  

4.  Seleccione la acción **Actualizar** y luego cierre la página **Ausencia**.  

El tiempo de ausencia registrado se reduce de la capacidad del día seleccionado.  

## <a name="see-also"></a>Consulte también  
[Configurar calendarios base](across-how-to-assign-base-calendars.md)  
[Configuración de centros de trabajo y centros de máquinas](production-how-to-set-up-work-and-machine-centers.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]