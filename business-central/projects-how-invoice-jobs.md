---
title: Crear una factura de venta para facturar un proyecto | Documentos de Microsoft
description: Describe cómo facturar a clientes por los costes del proyecto a medida que progresa un proyecto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 368b0b1edf1105045a365d8d5ac523c88955ad8a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758747"
---
# <a name="invoice-jobs"></a>Facturar proyectos
Durante el proyecto, pueden acumularse los costes del proyecto por el uso de recursos, materiales y compras relacionadas con el proyecto. Según progresa el proyecto, estas transacciones se registran en el diario del proyecto. Es importante que se registren todos los costes en el diario del proyecto antes de facturar al cliente.

> [!NOTE]
> Puede comprar recursos externos no relacionados con un proyecto, por ejemplo, para facturar a un proveedor por el trabajo entregado. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).

Puede facturar el proyecto completo desde la página **Líneas tareas proyecto** o facturar solo las líneas de la factura seleccionada desde la página **Líneas de planificación**. La facturación se puede realizar una vez finalizado el proyecto o a ciertos intervalos durante el progreso del proyecto, basándose en un programa de facturación.

> [!NOTE]  
> Si selecciona **Facturable** en el campo **Tipo línea proyecto** en los documentos de compra de las compras relacionadas con el proyecto, se crearán las líneas de planificación de proyecto que estén listas para facturarse al cliente. Para obtener más información, vea [Administrar suministros de proyecto](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Para crear varias facturas de venta de proyecto
Puede crear la factura de un proyecto o de una o varias tareas del proyecto para un cliente cuando se haya terminado el trabajo que se va a facturar o cuando se llegue a la fecha de facturación en función de un programa de facturación.

El siguiente procedimiento muestra cómo utilizar un proceso para facturar varios proyectos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Crear factura venta proyecto** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione filtros si desea limitar los proyectos que el proceso va a procesar.
4. Elija el botón **Aceptar** para crear las facturas.  

Puede revisar y registrar facturas creadas en la ventana **Facturas de venta**.

> [!NOTE]
> También puede facturar a un cliente seleccionando el proyecto y eligiendo la acción **Crear factura venta proyecto**. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Para crear y registrar facturas de venta de proyecto desde líneas de planificación de proyecto
Puede crear una factura a partir de las líneas de planificación de proyecto e indicar en ese momento la cantidad del producto, recurso o cuenta que desea facturar.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.
2. Abra un proyecto relevante.
3. Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.  
4. En una línea de planificación de proyecto, en el campo **Cdad. para transferir a factura**, introduzca la cantidad del producto, recurso y el tipo de la cuenta de contabilidad que desee facturar.  
5. Elija la acción **Crear factura venta**.
6. En la página **Crear factura venta proyecto**, escriba la fecha de registro y decida si desea crear una nueva factura o anexar esta factura a una existente.
7. Elija el botón **Aceptar**.  
8. En la página **Líneas planificación proyecto**, elija la acción **Facturas venta/Abonos venta**.

    Se abre la página **Factura venta** que muestra la cantidad que ha transferido a la factura.
9. Realice cualquier cambio adicional y, a continuación, elija la acción **Registrar**.

> [!NOTE]  
>   El procedimiento anterior es similar para crear, revisar y registrar un abono de venta relacionado con el proyecto.

## <a name="to-calculate-and-post-job-completion-entries"></a>Para calcular y registrar los movimientos de finalización de proyecto
Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**. Después, debe revertir cualquier WIP que haya registrado en contabilidad.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.
3. En el campo **Estado**, seleccione **Completado**.
4. Siga los pasos de la ayuda para calcular y registrar WIP. También puede seguir los pasos 5 y 6 para hacerlo manualmente.  
5. Elija la acción **Calcular WIP**.
6. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.  

     Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.  
7. Elija la acción **Registrar WIP en C/G proyecto**.
8. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  

     Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.

## <a name="see-also"></a>Consulte también
[Administrar proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]