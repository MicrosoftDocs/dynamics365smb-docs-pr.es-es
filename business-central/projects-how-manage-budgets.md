---
title: Configurar y administrar un presupuesto para un proyecto
description: Describe cómo planificar los recursos y prever y controlar los costes de un proyecto mediante la configuración de un presupuesto para cada proyecto.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-budgets"></a>Gestionar presupuestos de programa

Se puede configurar un presupuesto para cada proyecto. El presupuesto se utiliza para planificar los recursos que asigna a un proyecto. Puede ser genérico, con pocos movimientos, o bien puede contar con más movimientos divididos en niveles de actividad. Puede comparar los importes presupuestados con el uso real registrado en el diario de proyectos. Si supervisa las diferencias entre el uso real y el uso presupuestado, puede controlar un proyecto en curso y mejorar la calidad de futuros proyectos reduciendo el riesgo de subestimar los costes.

El procedimiento siguiente describe cómo calcular los costes presupuestados durante la planificación. Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-project"></a><a name="JobBudgetCosts"></a>Para estimar los costes presupuestados de un proyecto

Si un cliente desea saber el precio de un proyecto que se facturará en función del uso, se deben determinar los costes presupuestados del proyecto. Use la página **Líneas tarea proyecto** para hacerlo.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Abra un proyecto relevante.
3. Seleccione una línea de tarea del tipo Registro y, a continuación, elija la acción **Líneas planificación proyecto**.
4. En una línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

En el campo **Tipo de línea**, escriba la siguiente información.  

| Tipo línea | Descripción |
| --- | --- |
| **Presupuesto y facturable** |Los importes de coste y precio introducidos en la línea de planificación son los costes presupuestados para la línea de planificación concreta. El importe del precio se facturará. |
| **Presupuesto** |Al cliente no se le cobra por el uso. El uso no se transfiere a una factura, pero se utiliza para calcular el WIP. |
| **Facturable** |El cliente sí paga por el uso. La utilización se transfiere a la factura, en función de la cantidad especificada en el campo **Cdad. a transferir a factura**. |

> [!NOTE]  
> El campo **Fecha entrega planificada** de la línea de planificación contiene la fecha en la que se espera que se complete el uso relacionado con la línea de planificación. También es la fecha en la que la línea de planificación se puede transferir a una factura de venta y registrarla. <br /><br /> En la tarea de proyecto subyacente de la página **Ficha proyecto**, los campos **Fecha de inicio** y **Fecha de finalización** respectivamente contienen el valor del campo **Fecha entrega planificada** en las primeras y últimas líneas de planificación de proyecto de la página **Líneas planificación proyecto** relacionada.

> [!NOTE]  
> Cuando rellena el campo **Cantidad**, se calculará el coste y el precio total y se rellenará la línea de planificación. Puede modificarlos en cualquier momento.

En la página **Ficha proyecto**, puede ver un resumen del total de costes presupuestados, precio presupuestado, coste facturado y el precio facturado para cada tarea.

Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).

## <a name="see-also"></a>Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
