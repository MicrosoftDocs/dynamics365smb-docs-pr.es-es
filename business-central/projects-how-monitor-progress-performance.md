---
title: "Definir un método WIP y supervisar el progreso del proyecto | Documentos de Microsoft"
description: "Describe cómo puede crear un método de trabajo en curso (WIP) y calcular el WIP para estimar el valor financiero de los trabajos mientras están en progreso."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 07/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 95a14b122c5e6b878ec8d7f8314c81de957853b7
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="monitor-job-progress-and-performance"></a>Supervisar el progreso y el rendimiento del trabajo
A medida que progresa un proyecto, se van consumiendo materiales, recursos y otros gastos, que se deben registrar en el proyecto. Trabajo en curso (WIP) es una función que permite estimar el valor financiero de los proyectos en la contabilidad mientras progresa el proyecto. En muchos casos, puede registrar gastos para un proyecto antes de facturarlo. Si solamente se registran gastos, el resultado financiero no será exacto. Para obtener más información, consulte [Comprensión de los métodos WIP](projects-understanding-wip.md).

Para supervisar el valor en la contabilidad, puede calcular WIP y registrar el valor en la contabilidad.

Puede calcular WIP basándose en lo siguiente:

* Valor coste
* Valor venta
* Coste reconocible
* Porcentaje completado
* Contrato consumado

Si desea ver el resultado usando un método diferente, puede cambiar el método y calcular WIP de nuevo. No hay ningún límite en cuanto al número de veces que puede calcular WIP. WIP sólo se calcula, no se registra en la contabilidad. Una vez calculado WIP, ya puede registrar en la contabilidad.

## <a name="to-create-a-job-wip-method"></a>Para crear un método de proyecto WIP
Puede crear un método de proyecto WIP que refleje las necesidades de su organización. Una vez lo haya creado, puede establecerlo como el método de cálculo de proyecto WIP predeterminado que se utilizará en su organización.  

> [!NOTE]
> Tras haber usado el nuevo método para crear los movimientos del WIP, no puede eliminar el método ni modificarlo.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Métodos WIP de proyecto** y, a continuación, seleccione el vínculo relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Cierre la ventana.   
4. Para convertir este nuevo método en el predeterminado, en la esquina superior derecha, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de proyectos** y, a continuación, seleccione el vínculo relacionado.  
5. En el campo **Método WIP predet.**, seleccione el método de la lista.

## <a name="to-define-a-wip-method-for-a-job"></a>Para definir un método de WIP para un proyecto
Al crear un proyecto nuevo, debe especificar el método WIP que se aplica. En algunos casos, el método de WIP de proyecto que puede utilizar se ha configurado como valor predeterminado.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**. Para obtener más información, vea [Crear proyectos](projects-how-create-jobs.md).  
3. En la ventana **Ficha de proyecto**, en el campo **Método WIP**, seleccione un método WIP de la lista. Si se ha definido un método predeterminado, puede seleccionar otra opción si es necesario.  

## <a name="to-calculate-wip"></a>Para calcular WIP
Puede determinar el importe WIP que se debe registrar en cuentas de balance para informes del final de periodo. Para hacerlo, debe usar el proceso **Calcular WIP proyecto**.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Calcular WIP proyecto** y, a continuación, seleccione el vínculo relacionado.  
2. Elija la acción **Calcular WIP**.
3. En la ventana **Calcular WIP proyecto**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.  

> [!NOTE]  
>   El proceso solo calcula el WIP. No se registra en contabilidad. Para hacerlo, debe ejecutar el proceso **Registrar WIP en C/G** una vez que haya calculado el WIP. Para obtener más información, consulte el procedimiento siguiente.

## <a name="to-post-wip"></a>Para registrar WIP
Cuando ha calculado WIP, puede registrarlo en las cuentas de balance de los informes de fin de periodo. Para ello, debe usar el proceso **Registrar WIP en C/G proyecto**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registrar WIP en C/G proyecto** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Registrar WIP en C/G proyecto**, rellene los campos según sea necesario.  
3. Elija el botón **Aceptar**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Para ver el uso estimado del proyecto y registrar las actualizaciones
Puede ver el consumo del proyecto hasta que se termine en un paso. Para ello, utilice el proceso **Cálc. uso restante proyecto** para todas las tareas hasta la terminación del proyecto.  

Esto le permite supervisar y comparar los cálculos originales con los resultados reales, y realizar modificaciones o movimientos nuevos según sea necesario. Por ejemplo, puede haber estimado que un proyecto exigía 10 horas y, hasta el momento, ha llevado 15 horas. Puede agregar las cinco horas adicionales a la línea del diario existente o crear una línea de diario nueva que presente estas cinco horas como horas extra, que es otro tipo de trabajo. Se calcula el coste y el precio apropiado, y se puede registrar en el diario.  

> [!NOTE]  
>   Los movimientos de producto crean movimientos contables y reducen la cantidad de inventario. El proceso **Regis. variación existencias** transfiere el coste del inventario a la contabilidad. Los movimientos de recursos crean movimientos correspondientes.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione un diario de trabajo relevante y, a continuación, seleccione la acción **Cálc. uso restante**.  
3. En la ventana **Cálc. uso restante proyecto** especifique el número del documento y la fecha de registro que se va a insertar en el diario y, a continuación, elija **Aceptar**.  
4. Puede ser necesario actualizar el diario con algunos cambios.  
5. Seleccione **Registrar**.

## <a name="to-view-job-ledger-entries"></a>Para ver los movimientos del proyecto
Los movimientos relativos a proyectos se guardan en los registros de movimientos de proyectos y se numeran de forma secuencial, empezando por 1. Desde el registro de movimientos de proyecto, se puede obtener un resumen de todos los movimientos de proyecto.    

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro movs. proyectos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione un registro correspondiente y, a continuación, elija la acción **Movs. proyectos**.

En la ventana **Movimientos de proyecto** puede revisar los movimientos que está asociado con algún proyecto.  

## <a name="see-also"></a>Consulte también
[Administración de programas](projects-manage-projects.md)
[Gestión de costes de inventario](finance-manage-inventory-costs.md)   
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ccial](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

