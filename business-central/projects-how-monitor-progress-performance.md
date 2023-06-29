---
title: Supervisar el progreso y el rendimiento del trabajo
description: Describe cómo puede crear un método de trabajo en curso (WIP) y calcular el WIP para estimar el valor financiero de los trabajos mientras están en progreso.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# <a name="monitor-job-progress-and-performance"></a><a name="monitor-job-progress-and-performance"></a><a name="monitor-job-progress-and-performance"></a>Supervisar el progreso y el rendimiento del trabajo

Con la función Trabajo en curso (WIP) puede estimar el valor financiero de los proyectos en curso en el libro mayor.

A medida que progresa un proyecto, se van consumiendo materiales y recursos y se producen gastos, que se deben registrar en el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Pero si solamente se registran gastos, el resultado financiero no será exacto. Para realizar un seguimiento del valor real del proyecto, calcule el WIP y publíquelo en el libro mayor. Obtenga más información en [Comprensión de los métodos WIP](projects-understanding-wip.md).

Puede calcular WIP basándose en lo siguiente:

* Valor del coste
* Valor de ventas
* Coste reconocible
* Porcentaje de finalización
* Contrato completado

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method"></a><a name="create-a-job-wip-method"></a><a name="create-a-job-wip-method"></a>Crear un método de proyecto WIP

Cree un método de proyecto WIP que satisfaga las necesidades de su organización y establézcalo como predeterminado.  

> [!NOTE]
> Tras haber usado el nuevo método para crear los movimientos del WIP, no podrá modificar o eliminar ese método.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **métodos wip de proyecto** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cierre la página.   
4. Para convertir en predeterminado este nuevo método, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **configuración de proyectos** y luego elija el enlace relacionado.  
5. En el campo **Método WIP predet.**, seleccione el método de la lista.

## <a name="define-a-wip-method-for-a-job"></a><a name="define-a-wip-method-for-a-job"></a><a name="define-a-wip-method-for-a-job"></a>Definir un método de WIP para un proyecto

Al crear un proyecto nuevo, debe especificar el método WIP que se aplica. En algunos casos, el método de proyecto WIP que utiliza ya está configurado como predeterminado.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **proyectos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**. Obtenga más información en [Crear trabajos](projects-how-create-jobs.md).  
3. En la página **Ficha de proyecto**, en el campo **Método WIP**, seleccione un método WIP de la lista. Si se ha definido un método predeterminado, puede seleccionar otra opción si es necesario.  

### <a name="define-a-wip-method-for-a-job-task"></a><a name="define-a-wip-method-for-a-job-task"></a><a name="define-a-wip-method-for-a-job-task"></a>Definir un método de WIP para una tarea de proyecto

Puede definir un método WIP para una tarea de proyecto, excluir algunas tareas de proyecto del cálculo del WIP o agrupar tareas para que se calculen juntas. 

Si desea calcular WIP para cada tarea de proyecto individualmente, la publicación de WIP proporciona dimensiones definidas para las tareas específicas.

**WIP-Total** especifica las tareas de proyecto que desea agrupar al calcular los valores de trabajo en curso (WIP) y reconocimiento. En cualquier grupo de tareas, es necesario que haya una tarea que satisfaga dos condiciones:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Tiene **WIP-Total** ajustado a *Total*. (Si no hay tareas del proyecto con un **WIP-Total** definido en *Total*, *Total* se definirá automáticamente en la última línea de tarea del proyecto cuando el WIP se calcula por primera vez.)

* Tener un número **N.º tarea de proyecto** que sea el final del grupo o rango de las tareas de proyecto.

La siguiente tabla describe las tres opciones:

| Campo | Descripción |
|--|--|
| **\<blank\>** | Deje el campo en blanco si la tarea del proyecto es parte de un grupo de tareas. |
| **Total** | Define el rango o grupo de tareas que se incluyen en el cálculo del WIP y del reconocimiento. En el grupo, cualquier tarea de proyecto con **Tipo tarea proyecto** definido como **Registro** se incluirá en el total WIP, a menos que el campo **Total WIP** de la tarea se defina como **Excluido**. |
| **Excluido** | Solo se aplica a una tarea con **Tipo de tarea de trabajo** de **Registro**, en cuyo caso la tarea no se incluye cuando se calcula el WIP y el reconocimiento. |

En el siguiente ejemplo, las tareas del trabajo se dividen en dos agrupaciones de total WIP, lo que demuestra cómo funciona el campo **WIP-Total**:

|N.º tarea de proyecto|Descripción|Tipo de tarea de proyecto|Campo **WIP-Total**|  
|------------------|----------------------|----------------------|----------------------|  
|1000|Preparación|Total inicio|\<blank\>|
|1010|.    Limpieza|Registrar|**Excluido**|
|1099|Preparación total|Total fin|\<blank\>|
|1100|Alfombrado|Total inicio|\<blank\>|
|1110|.    Encolar el suelo|Registrar|**Excluido**|
|1120|.    Colocación de la moqueta|Registrar|\<blank\>|
|1199|Alfombrado total|Total fin|\<blank\>|
|1200|Finalizar|Total inicio|\<blank\>|
|1210|.    Aspirar la moqueta|Registrar|\<blank\>|
|1299|Finalización total|Total fin|**Total**|
|1300|Corrección de errores|Total inicio|\<blank\>|
|1310|.    Corrección de errores|Registrar|\<blank\>|
|1399|Corrección de errores total|Total fin|**Total**|

Notará:

* Del *1000* al *1299*: se calculará el WIP por separado para este grupo de tareas. Sin embargo, tenga en cuenta que dos de las tareas, 1010 y 1110, se excluyen del cálculo de WIP porque su tipo de tarea de proyecto es **Registro**.

* Del *1300* al *1399*: se calculará el WIP por separado para este grupo de tareas.

## <a name="calculate-wip"></a><a name="calculate-wip"></a><a name="calculate-wip"></a>Calcular WIP

Puede determinar el importe WIP que se debe registrar en cuentas de balance para informes del final de periodo. Para hacerlo, debe usar el proyecto por lotes **Calcular WIP proyecto**.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **calcular wip proyecto** y luego elija el enlace relacionado.  
2. Elija la acción **Calcular WIP**.
3. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.  

> [!NOTE]  
>   El proyecto por lotes solo calcula el WIP, es decir, no lo registra en el módulo de contabilidad. Para registrarlo, ejecute proyecto por lotes **Registrar WIP en C/G** una vez que haya calculado el WIP. Obtenga más información en el siguiente procedimiento.

## <a name="post-wip"></a><a name="post-wip"></a><a name="post-wip"></a>Registrar WIP

Cuando ha calculado WIP, puede registrarlo en las cuentas de balance de los informes de fin de periodo. Para ello, debe usar el proceso **Registrar WIP en C/G proyecto**.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **registrar wip en g/l proyecto**, y luego elija el enlace relacionado.  
2. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  
3. Elija el botón **Aceptar**.

## <a name="calculate-and-post-job-completion-entries"></a><a name="calculate-and-post-job-completion-entries"></a><a name="calculate-and-post-job-completion-entries"></a>Calcular y registrar los movimientos de finalización de proyecto

Cuando haya terminado todas las actividades de un proyecto, incluidos los registros de consumo y la facturación, tiene que actualizarlo para que su **Estado** sea **Completado**. Después, debe revertir cualquier WIP que haya registrado en contabilidad.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **proyectos** y luego elija el enlace relacionado.  
2. Seleccione un proyecto pendiente y, a continuación, elija la acción **Editar**.
3. En el campo **Estado**, seleccione **Completado**.
4. Siga los pasos de la ayuda para calcular y registrar WIP. O bien siga los pasos 5 y 6 para hacerlo manualmente.  
5. Elija la acción **Calcular WIP**.
6. En la página **Calcular WIP proyecto**, rellene los campos según sea necesario.  

     Los movimientos de trabajo en curso del proyecto creados al ejecutar el proceso tendrán marcada la casilla **Proyecto completado** para indicar que se trata de movimientos de finalización.  
7. Elija la acción **Registrar WIP en C/G proyecto**.
8. En la página **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  

     Los movimientos de contabilidad del trabajo en curso del proyecto creados al ejecutar el trabajo por lotes tendrán marcada la casilla de verificación **Proyecto completado** para indicar que se trata de movimientos de finalización.

## <a name="view-job-ledger-entries"></a><a name="view-job-ledger-entries"></a><a name="view-job-ledger-entries"></a>Ver los movimientos del proyecto

Los movimientos relativos a proyectos se guardan en los registros de movimientos de proyectos y se numeran de forma secuencial, empezando por 1. Desde el registro de movimientos de proyecto, se puede obtener un resumen de todos los movimientos de proyecto.    

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **registros de proyectos** y luego elija el enlace relacionado.
2. Seleccione un registro correspondiente y, a continuación, elija la acción **Movs. proyectos**.

En la página **Movimientos de proyecto** puede revisar los movimientos que está asociado con algún proyecto.  

## <a name="find-related-microsoft-training"></a><a name="find-related-microsoft-training"></a><a name="find-related-microsoft-training"></a>Encontrar la [formación de Microsoft](/training/paths/calculate-post-job-wip/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Tutorial: cálculo del trabajo en curso para un proyecto](walkthrough-calculating-work-in-process-for-a-job.md)
[Administrar proyectos](projects-manage-projects.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
