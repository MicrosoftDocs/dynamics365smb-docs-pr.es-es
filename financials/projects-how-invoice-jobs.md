---
title: Crear una factura de venta para facturar un proyecto | Documentos de Microsoft
description: "Describe cómo facturar a clientes por los costes del proyecto a medida que progresa un proyecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9367dc5875b687b95076efffb3b0df2019332651
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-invoice-jobs"></a>Facturación de proyectos
Durante el proyecto, pueden acumularse los costes del proyecto por el uso de recursos, materiales y compras relacionadas con el proyecto. Según progresa el proyecto, estas transacciones se registran en el diario del proyecto. Es importante que se registren todos los costes en el diario del proyecto antes de facturar al cliente.

Puede facturar el proyecto completo desde la ventana **Líneas tareas proyecto** o facturar solo las líneas de la factura seleccionada desde la ventana **Líneas de planificación**. La facturación se puede realizar una vez finalizado el proyecto o a ciertos intervalos durante el progreso del proyecto, basándose en un programa de facturación.

> [!NOTE]  
>   Si selecciona **Facturable** en el campo **Tipo línea proyecto** en los documentos de compra de las compras relacionadas con el proyecto, se crearán las líneas de planificación de proyecto que estén listas para facturarse al cliente. Para obtener más información, vea [Administrar suministros de proyecto](projects-how-manage-project-supplies.md).

## <a name="to-create-and-post-a-job-sales-invoice"></a>Para crear y registrar una factura de venta del proyecto
Puede crear la factura de un proyecto o de una o varias tareas del proyecto para un cliente cuando se haya terminado el trabajo que se va a facturar o cuando se llegue a la fecha de facturación en función de un programa de facturación.

En la ventana **Proyectos** puede facturar a un cliente seleccionando el proyecto y eligiendo la acción **Crear factura venta proyecto**. El siguiente procedimiento muestra cómo utilizar un proceso para facturar varios proyectos.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Crear factura venta proyecto** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione filtros si desea limitar los proyectos que el proceso va a procesar.
4. Elija el botón **Aceptar** para crear las facturas.  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a>Para crear varias facturas de venta de proyecto desde líneas de planificación de proyecto
Puede crear una factura a partir de las líneas de planificación de proyecto e indicar en ese momento la cantidad del producto, recurso o cuenta que desea facturar.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Abra un proyecto relevante.
3. Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.  
4. En una línea de planificación de proyecto, en el campo **Cdad. para transferir a factura**, introduzca la cantidad del producto, recurso y el tipo de la cuenta de contabilidad que desee facturar.  
5. Elija la acción **Crear factura venta**.
6. En la ventana **Crear factura venta proyecto**, escriba la fecha de registro y decida si desea crear una nueva factura o anexar esta factura a una existente.
7. Elija el botón **Aceptar**.  

    En la línea de planificación de proyecto, en el campo **Cdad. transferida a factura**, puede ver la cantidad.
8. En la ventana **Líneas planificación proyecto**, elija la acción **Facturas venta/Abonos venta**.

    Se abre la ventana **Factura venta** que muestra la cantidad que ha transferido a la factura.  
9. Realice cualquier cambio adicional y, a continuación, elija la acción **Registrar**.

> [!NOTE]  
>   El procedimiento anterior es similar para crear, revisar y registrar un abono de venta relacionado con el proyecto.

## <a name="to-calculate-and-post-job-completion-entries"></a>Para calcular y registrar los movimientos de finalización de proyecto
Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**. Después, debe revertir cualquier WIP que haya registrado en contabilidad.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.
3. En el campo **Estado**, seleccione **Completado**.
4. Siga los pasos de la ayuda para calcular y registrar WIP. También puede seguir los pasos 5 y 6 para hacerlo manualmente.  
5. Elija la acción **Calcular WIP**.
6. En la ventana **Calcular WIP proyecto**, rellene los campos según sea necesario.  

     Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.  
7. Elija la acción **Registrar WIP en C/G proyecto**.
8. En la ventana **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  

     Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.

## <a name="see-also"></a>Consulte también
[Administrar proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ccial](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

