---
title: Registrar el consumo o uso de recursos y artículos de proyectos
description: Describe cómo registrar el consumo o el uso de productos o recursos en proyectos para facilitar la administración de proyectos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.search.form: 89, 92, 201, 1007, 1014
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c948845c535474ccd5fb8c3d6e031e5467c9de2f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532085"
---
# <a name="record-consumption-or-usage-for-jobs"></a>Registrar el consumo o uso para proyectos

En la página **Líneas planificación proyecto**, puede revisar y registrar la utilización en las diferentes partes de su proyecto, que se actualiza automáticamente cuando modifica y transfiere la información entre proyectos y diarios de proyectos o facturas del proyecto. Para ello, es necesario que haya configurado un proyecto para que **Aplicar vínculo de uso** se active. Para obtener más información, consulte [Configurar trabajos](projects-how-setup-jobs.md).  

Por ejemplo, para las líneas de planificación del tipo **Presupuesto**, puede especificar la cantidad de un recurso, e indicar la cantidad a transferir al diario de proyectos. Si el tipo de la línea de planificación es **Facturable**, puede especificar la cantidad del recurso, e indicar la cantidad a transferir a una factura. Para obtener más información sobre cómo facturar al cliente, consulte [Proyectos de factura](projects-how-invoice-jobs.md). Al comparar la cantidad original, la cantidad restante o la cantidad registrada, puede revisar rápidamente la información de uso. Para obtener información acerca de la estimación de valores presupuestados durante la planificación, vea [Administración de presupuestos de proyecto](projects-how-manage-budgets.md).  

En los procedimientos siguientes se describe cómo registrar cantidades y costes reales (presupuestados) con el diario de proyectos. Alternativamente, puede utilizar los documentos de compra para registrar la compra de un proyecto. Para obtener más información, vea [Administrar suministros de proyectos](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Para registrar la utilización de una línea de planificación de proyecto de tipo Presupuesto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
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

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
2. En el campo **Nombre sección**, seleccione una sección de diario de proyectos relevante.  
3. En una nueva línea, introduzca el número de documento, el número de proyecto, el número de la tarea del proyecto, el tipo y la cantidad del tipo que se consume.  
4. Cuando las líneas del diario de proyectos están completas, seleccione la acción **Registrar**.  

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Para ver el uso estimado del proyecto y registrar las actualizaciones

Puede ver el consumo del proyecto hasta que se termine en un paso. Para ello, utilice el proceso **Cálc. uso restante proyecto** para todas las tareas hasta la terminación del proyecto.  

Esto le permite supervisar y comparar los cálculos originales con los resultados reales, y realizar modificaciones o movimientos nuevos según sea necesario. Por ejemplo, puede haber estimado que un proyecto exigía 10 horas y, hasta el momento, ha llevado 15 horas. Puede agregar las cinco horas adicionales a la línea del diario existente o crear una línea de diario nueva que presente estas cinco horas como horas extra, que es otro tipo de trabajo. Se calcula el coste y el precio apropiado, y se puede registrar en el diario.  

> [!NOTE]  
>   Los movimientos de producto crean movimientos contables y reducen la cantidad de inventario. El proceso **Regis. variación existencias** transfiere el coste del inventario a la contabilidad. Los movimientos de recursos crean movimientos correspondientes.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Cálc. uso restante**.  
3. En la página **Cálc. uso restante proyecto** especifique el número del documento y la fecha de registro que se va a insertar en el diario y, a continuación, elija **Aceptar**.  
4. Puede ser necesario actualizar el diario con algunos cambios.  
5. Seleccione **Registrar**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Crear documentos de picking de almacén e inventario para un proyecto

Para crear documentos de picking de almacén de inventario para proyectos, su administrador debe habilitar **Actualización de característica: habilitar el picking de almacén e inventario de los proyectos** en la página **Administración de características**.

La función agrega las acciones **Crear picking inventario** y **Crear picking almacén** en **Ficha de proyecto**. Para crear o registrar un documento de selección, utilice las acciones **Líns. almac./picking/Líneas movimiento** o **Líneas de picking registradas**. Para obtener más información sobre picking, consulte [Elegir productos](warehouse-pick-items.md).

Puede usar acciones en las siguientes condiciones:
* El **Estado** del proyecto es **Abierto**.
* El **Tipo de línea** de la línea de planificación del proyecto es **Presupuesto** o **Presupuesto y facturable**.
* El **Tipo** de la línea de planificación del proyecto es **Producto**.
* **Picking requerido** está habilitado para la ubicación relacionada.
* **Ubic. y pick. dirigido** está deshabilitado.

> [!NOTE] 
> Aunque la configuración se llama **Picking requerido**, aún puede registrar el consumo directamente desde la línea del diario de proyecto para la ubicación. Si el almacén está configurado para requerir el proceso de picking, pero no el proceso de envío, utilice la página **Picking inventario** para organizar e imprimir la información de picking. También se usa la página para ingresar y publicar el resultado del picking, lo que, a su vez, registra el consumo de los productos 
> 
> Si su almacén se ha configurado para requerir picking y procesamiento de envío, con lo que ha activado los campos de **Picking requerido** y **Envío requerido** en la **Ficha de almacén**, utilice la página **Picking de almacén** para gestionar el picking. Los picking de almacén son similares a los de inventario. La diferencia es que, en lugar de registrar la información del picking, registra el propio picking. Este registro no contabiliza el consumo, solo hace que los productos estén disponibles para el registro. Como administrador del almacén, puede utilizar la hoja de trabajo de un picking para organizar la información antes de crear las instrucciones individuales de picking de almacén


## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Para revisar las líneas de planificación de un movimiento de proyecto

Después de haber registrado las líneas de diario de proyectos, puede ver las líneas de planificación que están asociadas a los movimientos del diario de proyectos que se han registrado.

> [!NOTE]  
> Esto requiere que la casilla **Aplicar enlace de uso** se haya seleccionado para el proyecto. Para obtener más información, consulte [Configurar proyectos](projects-how-setup-jobs.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Movimientos**.  
3. En la página **Movs. proyectos**, elija la acción **Mostrar líneas planificación proyecto vinculadas**.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/post-job-usage-sales/) relacionada

## <a name="see-also"></a>Consulte también .

[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
