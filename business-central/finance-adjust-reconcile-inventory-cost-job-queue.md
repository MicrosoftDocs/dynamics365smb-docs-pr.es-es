---
title: Programar trabajos para ajustar y conciliar el coste de inventario
description: 'Obtenga información sobre cómo puede usar la cola de proyectos para mover las tareas para ajustar el coste de inventario o conciliarlo con la contabilidad a un segundo plano. Por ejemplo, si su empresa ejecuta muchas tareas o procesa muchas transacciones.'
author: AndreiPanko
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: 461
ms.date: 09/23/2021
ms.author: andreipa
---
# <a name="schedule-jobs-for-adjusting-and-reconciling-inventory-cost-with-the-general-ledger"></a>Programar trabajos para ajustar y conciliar el coste de inventario con la contabilidad

Para optimizar la experiencia, el ajuste automático de costes y el registro en la contabilidad están activados de forma predeterminada. Sin embargo, a medida que los datos se acumulan con el tiempo, eso podría afectar el rendimiento. Para reducir la carga en la aplicación, a menudo es útil usar entradas de la cola de proyectos para mover las tareas y ejecutarlas en segundo plano.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Mueva la tarea de ajustar los costes de los productos a un segundo plano con la ayuda de la configuración asistida

Crear las entradas de la cola de proyectos puede ser complicado, incluso para un consultor experimentado, por lo que contamos con una guía de configuración asistida para facilitar el proceso de ajuste de los costes de los productos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. existencias** y luego elija el enlace relacionado.  
2. En la página **Configuración del inventario**, alterne el campo **Contabilización automática de costes** o especifique **NUnca** en el campo **Ajuste automático de costes**.  
3. En la notificación que ahora se muestra en la parte superior de la página, elija el enlace **Programar movimiento en cola de proyectos**. Esto abre la guía de configuración asistida **Ajuste de coste de previsión y registro**.  
4. Especifique la tarea que desea programar.  

  > [!NOTE]
  > No puede crear un nuevo movimiento de cola de proyectos si ya existe un movimiento de cola de proyectos para la tarea especificada.

5. Seleccione el campo **Ver los movimiento de la cola de proyectos al finalizar** para revisar y ajustar la configuración. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Para crear un movimiento en la cola de proyectos para ajustar y conciliar el coste de inventario manualmente

Alternativamente, puede crear movimientos de cola de proyectos manualmente. El siguiente procedimiento muestra cómo configurar el trabajo por lotes **Ajustar coste: movimientos de productos** para que se ejecute automáticamente a diario, pero los mismos pasos se aplican al trabajo por lotes **Contabilizar el coste de inventario en la contabilidad**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Movs. cola proyecto** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, elija *Informe*.  
4. En el campo **ID de objeto para ejecutar**, elija *795*, **Ajustar coste: movimiento de productos**.  
5. En el campo **Fórmula de fecha de ejecución siguiente**, introduzca *1D*.
6. En el campo **Hora inicial**, introduzca *2 AM*.
7. Elija la acción **Establecer estado en Preparado**.

Ahora, el coste del inventario se actualizará todas las noches.  

Para programar una tarea para conciliar el inventario con la contabilidad, seleccione codeunit 2846 **Contabilizar el costo de inventario en la contabilidad**.

> [!TIP]
> Para evitar el bloqueo, no programe tareas para el trabajo por lotes **Ajustar coste: movimientos de productos**, la codeunit **Contabilizar el costo de inventario en la contabilidad** ni las tareas para contabilizar transacciones de venta o compra al mismo tiempo. Además, asegúrese de que utilicen la misma categoría de cola de trabajos.

## <a name="see-also"></a>Consulte también

[Modificar costes de productos](inventory-how-adjust-item-costs.md)  
[Conciliar costes de inventario con la contabilidad](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
