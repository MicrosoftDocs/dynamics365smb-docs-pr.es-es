---
title: Registrar el uso facturable y presupuestado de los recursos de proyecto | Documentos de Microsoft
description: Describe cómo registrar el consumo o el uso de productos o recursos en proyectos para facilitar la administración de proyectos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c723625bc54c7b885268946f0e7afdf54be20a2b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "923226"
---
# <a name="record-usage-for-jobs"></a>Registro del uso para proyectos
En la página **Líneas planificación proyecto**, puede revisar y registrar la utilización en las diferentes partes de su proyecto, que se actualiza automáticamente cuando modifica y transfiere la información entre proyectos y diarios de proyectos o facturas del proyecto. Para ello es necesario que haya configurado un proyecto para que **Aplicar vínculo uso de forma pred.** se active. Para obtener más información, consulte [Configurar trabajos](projects-how-setup-jobs.md).  

Por ejemplo, para las líneas de planificación del tipo **Presupuesto**, puede especificar la cantidad de un recurso, e indicar la cantidad a transferir al diario de proyectos. Si el tipo de la línea de planificación es **Facturable**, puede especificar la cantidad del recurso, e indicar la cantidad a transferir a una factura. Comparando la cantidad que se ha transferido al diario o a la factura con la cantidad pendiente, puede revisar rápidamente la información de utilización.

En los procedimientos siguientes se describe cómo registrar precios y costes de proyecto reales (facturables) o presupuestados. Para obtener información acerca de la estimación de valores presupuestados durante la planificación, vea [Administración de presupuestos de proyecto](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Para registrar la utilización de una línea de planificación de proyecto de tipo Presupuesto
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Líneas planificación proyecto**.
3. Seleccione una línea planificación de proyecto del tipo **Presupuesto** o **Presupuesto y Facturable** para la que desea registrar la utilización.
4. En el campo **Cdad. a transferir al diario**, introduzca el número que desea transferir. La cantidad predeterminada es el valor que introduzca en el campo **Cantidad**.

    El campo **Cantidad pendiente** muestra la cantidad que queda para completar el proyecto y transferirse al diario.  
5. Elija la acción **Crear líneas de diario de proyectos**.
6. En la página **Línea planificación proyecto transf. proy.**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Seleccione la acción **Diario de proyectos pendientes**.  
8. En la página **Diario de proyectos**, seleccione la línea relevante y, a continuación, elija la acción **Registrar**.
9. En la página **Líneas planificación proyecto**, revise el uso registrado mediante la consulta de los campos **Cantidad**, **Cantidad pendiente** y **Cdad. a transferir al diario**.  
10. Repita los pasos del 3 al 8 para registrar la utilización adicional.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Para registrar la utilización de una línea de planificación de proyecto de tipo Facturable
En la siguiente tarea, también se registra la utilización, pero para una línea de planificación de proyecto de tipo **Facturable**. Normalmente, en este caso, se factura la utilización, pero también puede transferirla a un diario. Sin embargo, al hacer esto, se crea una línea de planificación de proyecto de tipo **Presupuesto** para que coincida con la línea facturable. Para obtener más información, vea [Administración de presupuestos de proyecto](projects-how-manage-budgets.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.
2. Seleccione el proyecto correspondiente y, a continuación, elija la acción **Líneas planificación proyecto**.  
3. Seleccione una línea de planificación de proyecto de tipo **Facturable** para la que desee registrar la utilización.
4. En el campo **Cdad. a transferir a factura**, introduzca el número que desea transferir. La cantidad predeterminada es el valor que introduzca en el campo **Cantidad**.

    El campo **Cantidad a facturar** muestra la cantidad que queda para completar el proyecto y facturarse.  
5. Elija la acción **Crear factura venta**.
6. En la página **Transf. proy. a factura ventas**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.
7. En la página **Líneas planificación proyecto**, seleccione la línea relevante y, a continuación, elija la acción **Registrar**.
8. Revise la utilización registrada consultando los campos **Cantidad**, **Cantidad a facturar**, **Cdad. a transferir a factura** y, si la factura de ventas está registrada, el campo **Cdad. facturada**.
9. Repita los pasos del 3 al 8 para registrar la utilización adicional.  
10. Para revisar una factura de ventas registrada relacionada, elija la acción **Facturas venta/Abonos venta**.  
11. En la página **Facturas de proyecto**, seleccione la factura correspondiente y, a continuación, elija la acción **Factura ventas/abono pendiente**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Para crear líneas del diario de proyectos desde líneas de planificación del proyecto
Cuando esté preparado para registrar la información de los proyectos, debe crear líneas del diario de proyectos que pueda registrar.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proyectos** y luego elija el enlace relacionado.  
2. Seleccione el proyecto pendiente correspondiente y, a continuación, elija la acción **Líneas planificación proyecto**.  
3. En la página **Líneas planificación proyecto**, en una línea de planificación de proyecto, en el campo **Cdad. a transferir al diario**, introduzca la cantidad que desee transferir a un diario de proyectos.  
4. Elija la acción **Crear líneas de diario de proyectos**.
5. En la página **Línea planificación proyecto transf. proy.**, rellene los campos según sea necesario.  
6. Elija el botón **Aceptar**. Se crean las líneas de proyectos.
7. Para verificar la transferencia, abra la sección de diario de proyectos pertinente y compruebe los movimientos.  
8. Cuando las líneas del diario de proyectos están completas, seleccione la acción **Registrar**.  

## <a name="to-create-job-journal-lines-manually"></a>Para crear manualmente líneas de diario de proyectos
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios proyecto** y luego elija el enlace relacionado.  
2. En el campo **Nombre sección**, seleccione una sección de diario de proyectos relevante.  
3. En una nueva línea, introduzca el número de documento, el número de proyecto, el número de la tarea del proyecto, el tipo y la cantidad del tipo que se consume.  
4. Cuando las líneas del diario de proyectos están completas, seleccione la acción **Registrar**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Para revisar las líneas de planificación de un movimiento de proyecto
Después de haber registrado las líneas de diario de proyectos, puede ver las líneas de planificación que están asociadas a los movimientos del diario de proyectos que se han registrado.

> [!NOTE]  
>   Para ello es necesario que la casilla de verificación **Aplicar vínculo uso de forma pred.** se haya seleccionado para el proyecto, o sea el valor predeterminado para todos los proyectos de su organización. Para obtener más información, consulte [Configurar trabajos](projects-how-setup-jobs.md).  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios proyecto** y luego elija el enlace relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Movimientos**.  
3. En la página **Movs. proyectos**, elija la acción **Mostrar líneas planificación proyecto vinculadas**.

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
