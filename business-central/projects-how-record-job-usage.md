---
title: Registrar el consumo o uso de recursos y artículos de proyectos
description: Describe cómo registrar el consumo o el uso de productos o recursos en proyectos para facilitar la administración de proyectos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 65975621fff862b64333c87e70f34b75f8e2cbdb
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938101"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Registrar el consumo o uso para proyectos

En la página **Líneas planificación proyecto**, puede revisar y registrar la utilización en las diferentes partes de su proyecto, que se actualiza automáticamente cuando modifica y transfiere la información entre proyectos y diarios de proyectos o facturas del proyecto. Para ello, es necesario que haya configurado un proyecto para que **Aplicar vínculo de uso** se active. Para obtener más información, consulte [Configurar trabajos](projects-how-setup-jobs.md).  

Por ejemplo, para las líneas de planificación del tipo **Presupuesto**, puede especificar la cantidad de un recurso, e indicar la cantidad a transferir al diario de proyectos. Si el tipo de la línea de planificación es **Facturable**, puede especificar la cantidad del recurso, e indicar la cantidad a transferir a una factura. Para obtener más información sobre cómo facturar al cliente, consulte [Proyectos de factura](projects-how-invoice-jobs.md). Al comparar la cantidad original, la cantidad restante o la cantidad registrada, puede revisar rápidamente la información de uso. Para obtener información acerca de la estimación de valores presupuestados durante la planificación, vea [Administración de presupuestos de proyecto](projects-how-manage-budgets.md).  

En los procedimientos siguientes se describe cómo registrar cantidades y costes reales (presupuestados) con el diario de proyectos. Alternativamente, puede utilizar los documentos de compra para registrar la compra de un proyecto. Para obtener más información, vea [Administrar suministros de proyectos](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Para registrar la utilización de una línea de planificación de proyecto de tipo Presupuesto

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Líneas planificación proyecto**.
3. Seleccione una línea planificación de proyecto del tipo **Presupuesto** o **Presupuesto y Facturable** para la que desea registrar la utilización.  

    > [!NOTE]
    > También puede registrar el uso para una línea de planificación de proyecto de tipo **Facturable**. Normalmente, usa estas líneas para crear facturas, pero también puede transferirla a un diario. Para obtener más información, vea [Facturar proyectos](projects-how-invoice-jobs.md) <!--However, when you do that, a job planning line of type **Budget** is created to match the billable line. For more information, see [Manage Job Budgets](projects-how-manage-budgets.md).-->

4. En el campo **Cdad. a transferir al diario**, introduzca el número que desea transferir. La cantidad predeterminada es el valor que introduzca en el campo **Cantidad**.

    El campo **Cantidad pendiente** muestra la cantidad que queda para completar el proyecto y transferirse al diario.  
5. Elija la acción **Crear líneas de diario de proyectos**.

    > [!TIP]
    > Si va a agregar más líneas de planificación de proyecto para este proyecto, espere en este paso hasta que haya agregado todas las líneas de planificación de proyecto.
6. En la página **Línea planificación proyecto transf. proy.**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Seleccione la acción **Diario de proyectos pendientes**.  
8. En la página **Diario de proyectos**, seleccione la línea relevante y, a continuación, elija la acción **Registrar**.
9. En la página **Líneas planificación proyecto**, revise el uso registrado mediante la consulta de los campos **Cantidad**, **Cantidad pendiente** y **Cdad. a transferir al diario**.  
10. Repita los pasos del 3 al 8 para registrar la utilización adicional.  

## <a name="to-create-job-journal-lines-manually"></a>Para crear manualmente líneas de diario de proyectos

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. En el campo **Nombre sección**, seleccione una sección de diario de proyectos relevante.  
3. En una nueva línea, introduzca el número de documento, el número de proyecto, el número de la tarea del proyecto, el tipo y la cantidad del tipo que se consume.  
4. Cuando las líneas del diario de proyectos están completas, seleccione la acción **Registrar**.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Para ver el uso estimado del proyecto y registrar las actualizaciones

Puede ver el consumo del proyecto hasta que se termine en un paso. Para ello, utilice el proceso **Cálc. uso restante proyecto** para todas las tareas hasta la terminación del proyecto.  

Esto le permite supervisar y comparar los cálculos originales con los resultados reales, y realizar modificaciones o movimientos nuevos según sea necesario. Por ejemplo, puede haber estimado que un proyecto exigía 10 horas y, hasta el momento, ha llevado 15 horas. Puede agregar las cinco horas adicionales a la línea del diario existente o crear una línea de diario nueva que presente estas cinco horas como horas extra, que es otro tipo de trabajo. Se calcula el coste y el precio apropiado, y se puede registrar en el diario.  

> [!NOTE]  
>   Los movimientos de producto crean movimientos contables y reducen la cantidad de inventario. El proceso **Regis. variación existencias** transfiere el coste del inventario a la contabilidad. Los movimientos de recursos crean movimientos correspondientes.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Cálc. uso restante**.  
3. En la página **Cálc. uso restante proyecto** especifique el número del documento y la fecha de registro que se va a insertar en el diario y, a continuación, elija **Aceptar**.  
4. Puede ser necesario actualizar el diario con algunos cambios.  
5. Seleccione **Registrar**.



## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Para revisar las líneas de planificación de un movimiento de proyecto

Después de haber registrado las líneas de diario de proyectos, puede ver las líneas de planificación que están asociadas a los movimientos del diario de proyectos que se han registrado.

> [!NOTE]  
> Esto requiere que la casilla **Aplicar enlace de uso** se haya seleccionado para el proyecto. Para obtener más información, consulte [Configurar proyectos](projects-how-setup-jobs.md).  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Movimientos**.  
3. En la página **Movs. proyectos**, elija la acción **Mostrar líneas planificación proyecto vinculadas**.

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
