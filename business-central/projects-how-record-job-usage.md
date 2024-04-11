---
title: Registrar el consumo o uso de recursos y artículos de proyectos
description: 'En este artículo, se describe cómo registrar el consumo o el uso de productos o recursos para proyectos en la administración de proyectos.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-projects"></a>Registrar el consumo o uso para proyectos

Desde la página **Ficha de proyecto**, puede abrir la página **Líneas planificación proyecto** para revisar y registrar el uso en varias partes del proyecto. Esta información se actualiza automáticamente cuando modifica y transfiere información entre proyectos y diarios de proyecto o facturas de proyecto. Para ello es necesario que active el conmutador **Aplicar vínculo uso de forma pred.** en la página **Config. proyecto**. Obtenga más información en [Configurar proyectos](projects-how-setup-jobs.md).  

Por ejemplo, para las líneas de planificación del tipo **Presupuesto**, puede especificar la cantidad de un recurso y luego especificar la cantidad a transferir al diario de proyectos. Si el tipo de la línea de planificación es **Facturable**, puede especificar la cantidad del recurso y luego especificar la cantidad a transferir a una factura. Para obtener más información sobre cómo facturar al cliente, consulte [Proyectos de factura](projects-how-invoice-jobs.md). Al comparar la cantidad original, la cantidad restante o la cantidad registrada, puede revisar rápidamente la información de uso. Para obtener más información acerca de cómo estimar los valores presupuestados durante la planificación, vaya a [Administración de presupuestos de proyecto](projects-how-manage-budgets.md).  

En los procedimientos siguientes se describe cómo registrar cantidades y costes reales (presupuestados) con un diario de proyectos. Alternativamente, puede utilizar los documentos de compra para registrar las compras de un proyecto. Obtenga más información en [Administración de suministros de proyecto](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-project-planning-line-of-type-budget"></a>Para registrar la utilización de una línea de planificación de proyecto de tipo Presupuesto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione el proyecto y, a continuación, elija la acción **Líneas de planificación de proyecto**. 
3. Seleccione una línea planificación de proyecto del tipo **Presupuesto** o **Presupuesto y Facturable** para la que desea registrar la utilización.   

    > [!NOTE]
    > También puede registrar el uso para una línea de planificación de proyecto de tipo **Facturable**. Normalmente, usa estas líneas para crear facturas, pero también puede transferir la información a un diario. Obtenga más información en [Facturar proyectos](projects-how-invoice-jobs.md) 

4. En el campo **Cdad. a transferir al diario**, introduzca la cantidad que desea transferir. La cantidad predeterminada es el valor que introduzca en el campo **Cantidad**.

    El campo **Cantidad pendiente** muestra la cantidad que queda para completar el proyecto y transferir al diario.
5. Elija la acción **Crear líneas de diario de proyectos**.

    > [!TIP]
    > Si va a agregar más líneas de planificación de proyecto para este proyecto, espere en este paso hasta que haya agregado todas las líneas de planificación de proyecto.
6. En la página **Línea planificación proyecto transf. proy.**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Seleccione la acción **Diario de proyectos pendientes**.  
8. En la página **Diario de proyectos**, seleccione la línea relevante y, a continuación, elija la acción **Registrar**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. En la página **Líneas planificación proyecto**, revise el uso registrado mediante la consulta de los campos **Cantidad**, **Cantidad pendiente** y **Cdad. a transferir al diario**.  
10. Repita los pasos del 3 al 8 para registrar la utilización adicional.  

## <a name="to-create-project-journal-lines-manually"></a>Para crear manualmente líneas de diario de proyectos

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. En el campo **Nombre sección**, seleccione una sección de diario de proyectos relevante.  
3. En una nueva línea, introduzca el número de documento, el número de proyecto, el número de la tarea del proyecto, el tipo y la cantidad del tipo que se consume.  
4. Cuando las líneas del diario de proyectos están completas, seleccione la acción **Registrar**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-project-usage-estimates-and-post-updates"></a>Para ver el uso estimado del proyecto y registrar las actualizaciones

Puede ver el consumo del proyecto hasta que se termine en un paso. Para ello, utilice el proceso **Cálc. uso restante proyecto** para todas las tareas hasta la terminación del proyecto.  

Esto le permite supervisar y comparar los cálculos originales con los resultados reales, y realizar modificaciones o movimientos nuevos según sea necesario. Por ejemplo, puede haber estimado que un proyecto exigía 10 horas y, hasta el momento, ha llevado 15 horas. Puede agregar las cinco horas adicionales a la línea del diario existente o crear una línea de diario nueva que presente estas cinco horas como horas extra, que es otro tipo de trabajo. Se calcula el coste y el precio apropiado, y se puede registrar en el diario.  

> [!NOTE]  
> Los movimientos de producto crean movimientos contables y reducen la cantidad de inventario. El proceso **Regis. variación existencias** transfiere el coste del inventario a la contabilidad. Los movimientos de recursos crean movimientos correspondientes.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. Seleccione un diario de proyecto relevante y, a continuación, seleccione la acción **Cálc. uso restante**.  
3. En la página **Cálc. uso restante proyecto** especifique el número del documento y la fecha de registro que se va a insertar en el diario y, a continuación, elija **Aceptar**.  
4. Puede ser necesario actualizar el diario con algunos cambios.  
5. Seleccione **Registrar**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-project"></a>Crear documentos de picking de almacén e inventario para un proyecto

Use las acciones **Crear picking inventario** y **Crear picking almacén** en la página **Ficha de proyecto**. Para crear o registrar un documento de selección, utilice las acciones **Líns. almac./picking/Líneas movimiento** o **Líneas de picking registradas**. Obtenga más información en [Flujos para producción, ensamblaje y proyectos](design-details-internal-warehouse-flows.md).

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

## <a name="to-review-planning-lines-for-a-project-ledger-entry"></a>Para revisar las líneas de planificación de un movimiento de proyecto

Después de haber registrado las líneas de diario de proyectos, puede ver las líneas de planificación que están asociadas a los movimientos del diario de proyectos que se han registrado.

> [!NOTE]  
> Esto requiere que la casilla **Aplicar enlace de uso** se haya seleccionado para el proyecto. Para obtener más información, consulte [Configurar proyectos](projects-how-setup-jobs.md).  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. Seleccione un diario de proyecto relevante y, a continuación, seleccione la acción **Movimientos**.  
3. En la página **Movs. proyectos**, elija la acción **Mostrar líneas planificación proyecto vinculadas**.

## <a name="see-also"></a>Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
