---
title: Gestionar ausencias del empleado | Documentos de Microsoft
description: "Describe cómo registrar ausencias del empleados y analizar las estadísticas de las ausencias."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 09866f6774af5b2d9644015e986772052146d901
ms.contentlocale: es-es
ms.lasthandoff: 04/18/2018

---
# <a name="manage-employee-absence"></a>Gestionar ausencia empleados
Para administrar la ausencia de un empleado, se debe registrar en la ventana **Registro de ausencias**. Puede posteriormente hacer un seguimiento de distintas maneras para fines de análisis y creación de informes.

Las ausencias de empleado se pueden ver en dos ventanas diferentes:

* En la ventana **Registro de ausencias** se registran todas las ausencias de empleados, con una línea para cada ausencia.
* En la ventana **Ausencias de empleado** se muestran únicamente las ausencias de un empleado. Esta es la información que se ha introducido en la ventana **Registro de ausencias**, filtrada por un empleado específico.

Para obtener unas estadísticas fiables, se debe utilizar siempre la misma unidad de medida (hora o día) al registrar las ausencias.

## <a name="to-register-employee-absence"></a>Para registrar ausencias de empleados
Puede registrar las ausencias de empleados diariamente o a algún otro intervalo que cubra sus necesidades de organización.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Registro de ausencia** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene una línea para cada ausencia de empleado que desee registrar.
4. Cierre la ventana.

    > [!Tip]
    > Para obtener datos estadísticos significativos, utilice siempre la misma unidad de medida, hora o día, al registrar las ausencias.

## <a name="to-view-an-individual-employees-absence"></a>Para ver las ausencias de un empleado en particular
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Empleados** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el empleado correspondiente y, a continuación, elija la acción **Ausencias**.

    La ventana **Ausencias empleado** se abre para mostrar todas las ausencias y la fecha en que comenzaron y finalizaron.

## <a name="to-view-an-employees-absence-by-categories"></a>Para ver las ausencias de un empleado por categorías
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Empleados** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el empleado correspondiente y, a continuación, elija la acción **Ausencias por categorías**.
3. En la ventana **Empl. ausencias por categorías**, rellene los campos de filtro que sean necesarios y después seleccione la acción **Mostrar matriz**.

    La ventana **Emp. matriz ausenc. por catgs.** se abre para mostrar todas las ausencias, desglosadas por causas de ausencia.

## <a name="to-view-all-employee-absences-by-category"></a>Para ver todas las ausencias de empleados por la categoría
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Registro de ausencia** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Registro de ausencias** elija la acción **Panorama por categorías**.
3. En la ventana **Panorama ausencias por categs.**, establezca un filtro en el campo **Filtro nº empleado** para ver las ausencias de un solo empleado o de un grupo de empleados.
4. Elija la acción **Mostrar matriz**.

    La ventana **Panorama ausencias por matriz categs.** muestra las ausencias de todos los empleados, desglosadas por varias causas de ausencia.

## <a name="to-view-all-employee-absences-by-period"></a>Para ver todas las ausencias de empleados por periodo
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Registro de ausencia** y, a continuación, seleccione el vínculo relacionado.
   En la ventana **Registro de ausencias** elija la acción **Panorama por periodos**.
2. En la ventana **Panorama de ausencias por periodos** defina un filtro en el campo **Filtro causa ausencia** para ver las ausencias de empleado por las causas de ausencia específicas.
3. Elija la acción **Mostrar matriz**.

    La ventana **Matriz panorama ausencias en periodos** muestra las ausencias del empleado, desglosadas por periodos.

## <a name="see-also"></a>Consulte también
[Administrar recursos humanos](hr-manage-human-resources.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)

