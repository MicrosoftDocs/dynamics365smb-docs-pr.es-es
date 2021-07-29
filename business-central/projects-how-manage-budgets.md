---
title: Configurar y administrar un presupuesto para un proyecto | Documentos de Microsoft
description: Describe cómo planificar los recursos y prever y controlar los costes de un proyecto mediante la configuración de un presupuesto para cada proyecto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ceb57fb6425b988920957c3066aa19659d08ae89
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443463"
---
# <a name="manage-job-budgets"></a>Gestionar presupuestos de proyecto
Se puede configurar un presupuesto para cada proyecto. El presupuesto se utiliza para planificar los recursos que asigna a un proyecto. Puede ser genérico, con pocos movimientos, o bien puede contar con más movimientos divididos en niveles de actividad. Puede comparar los importes presupuestados con el uso real registrado en el diario de proyectos. Si supervisa las diferencias entre el uso real y el uso presupuestado, puede controlar un proyecto en curso y mejorar la calidad de futuros proyectos reduciendo el riesgo de subestimar los costes.

El procedimiento siguiente describe cómo calcular los costes presupuestados durante la planificación. Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a> Para estimar los costes presupuestados de un proyecto
Si un cliente desea saber el precio de un proyecto que se facturará en función del uso, se deben determinar los costes presupuestados del proyecto. Para hacerlo, debe usar la página **Líneas tarea proyecto**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2. Abra un proyecto relevante.
3. Seleccione una línea de tarea del tipo Registro y, a continuación, elija la acción **Líneas planificación proyecto**.
4. En una línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

En el campo **Tipo de línea**, escriba la siguiente información.  

| Tipo línea | Descripción |
| --- | --- |
| **Presupuesto y facturable** |Los importes de coste y precio introducidos en la línea de planificación son los costes presupuestados para la línea de planificación concreta. El importe del precio se facturará. |
| **Ppto** |Al cliente no se le cobra por el uso. La utilización no se transfiere a una factura, pero se utilizará en el cálculo del trabajo en curso. |
| **Facturable** |El cliente sí paga por el uso. La utilización se transfiere a la factura, en función de la cantidad especificada en el campo Cdad. a transferir a factura. |

> [!NOTE]  
> El campo **Fecha entrega planificada** de la línea de planificación contiene la fecha en la que se espera que se complete el uso relacionado con la línea de planificación. También es la fecha en la que la línea de planificación se puede transferir a una factura de venta y registrarla. <br /><br /> En la tarea de trabajo subyacente de la página **Ficha trabajo**, los campos **Fecha de inicio** y **Fecha de finalización** respectivamente contienen el valor del campo **Fecha entrega planificada** en las primeras y últimas líneas de planificación de trabajo de la página **Líneas planificación proyecto** relacionada.

> [!NOTE]  
>   Cuando rellena el campo **Cantidad**, se calculará el coste y el precio total y se rellenará la línea de planificación. Puede modificarlos en cualquier momento.

En la página **Ficha proyecto**, puede ver un resumen del total de costes presupuestados, precio presupuestado, coste facturado y el precio facturado para cada tarea.

Para obtener información acerca del registro de precios y costes de proyecto presupuestados y reales, vea [Registro del uso para proyectos](projects-how-record-job-usage.md).

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]