---
title: Crear una ficha de proyecto para un proyecto y especificar las tareas
description: Para un proyecto nuevo, cree una ficha de proyecto que contenga tareas y líneas de planificación, como ayuda para administrar el progreso y los presupuestos.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70bfd81f6fd331018fe6cafd6793ae1f1501f159
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519627"
---
# <a name="create-jobs"></a>Crear proyectos
Cuando inicie un proyecto nuevo, debe crear una ficha de proyecto con tareas de proyecto integradas y líneas de planificación de proyecto, estructuradas en dos niveles.  

La primera capa consta de tareas de proyecto. Debe crear al menos una tarea de proyecto por cada proyecto porque todos los registros hacen referencia a una tarea de proyecto. Tener al menos una tarea de proyecto en su proyecto le permite configurar líneas de planificación de proyecto y registrar el consumo en el proyecto.

La segunda capa consta de líneas de planificación de proyecto, que especifican el uso detallado de los recursos, productos y diversos gastos de contabilidad general.

La estructura de capas permite dividir el proyecto en tareas más pequeñas y usar detalles más específicos en el presupuesto, las ofertas y el registro. Además, le ofrece información de cómo está progresando un proyecto. Por ejemplo, puede hacer un seguimiento de si está alcanzando los hitos señalados o si va encaminado a cumplir las expectativas de presupuesto.

> [!TIP]
> Elija la acción **Proyecto nuevo** en el área de trabajo **Administrador del proyecto** para iniciar una guía configuración asistida que le lleva por los pasos para crear un proyecto con tareas integradas y líneas de planificación. El procedimiento siguiente describe cómo realizar los pasos manualmente. Para ver un ejemplo de cómo crear un trabajo manualmente, consulte [Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

A veces, la parte a la que recibe un servicio es diferente de la parte que paga la factura. En la página **Trabajos**, puede especificar el cliente que se beneficiará del proyecto en los campos **Vender a** y la parte a facturar en los campos **Cobrar a**. También puede especificar dónde se llevará a cabo el trabajo seleccionando de una lista de direcciones de envío para el cliente, agregar información sobre referencias externas para simplificar la comunicación sobre el proyecto y sobrescribir los términos financieros estándar del proyecto.

## <a name="to-create-a-job-card"></a>Para crear una ficha de proyecto
Cree una ficha de proyecto y, a continuación, cree las líneas de tarea de proyecto y las líneas de planificación de proyecto para el mismo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para especificar el proyecto con la información sobre otros proyectos, elija la acción **Copiar proyecto**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

> [!NOTE]  
>   Si utiliza las hojas de horas con su proyecto, también debe designar una persona responsable. Esta persona puede aprobar las hojas de horas para las tareas de empleados asociadas con el proyecto. Para obtener más información, consulte [Configurar hojas de horas](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Para crear tareas para un proyecto
Una parte clave de la creación de un proyecto es especificar las diversas tareas que conlleva. Para ello, debe agregar líneas nuevas en la ficha desplegable **Tareas** de la página **Ficha de proyecto**, con una tarea por línea. Cada proyecto debe tener al menos una tarea.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.
2. Abra la ficha de un proyecto relevante.
3. En la ficha desplegable **Tareas**, rellene los campos según sea necesario en una nueva línea.
4. Para indentar las tareas y crear una jerarquía, elija la acción **Tareas** y, a continuación, elija la acción **Indentar tareas proyecto**.
5. Repita los pasos 3 y 4 para todas las tareas que necesite para el proyecto.
6. Para especificar las tareas de proyecto con la información sobre otras tareas de proyecto, elija la acción **Copiar tareas de proyecto desde**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="to-create-planning-lines-for-a-job"></a>Para crear líneas de planificación de un proyecto
Puede redefinir las nuevas tareas de proyecto como líneas de planificación de proyecto. Una línea de planificación puede utilizarse para capturar cualquier información de un proyecto que desee supervisar. Puede utilizar líneas de planificación para agregar información como qué recursos son necesarios o para capturar productos que sean necesarios para realizar el proyecto. Por ejemplo, si tiene una tarea para obtener la aprobación de clientes para un proyecto, puede asociar esa tarea con líneas de planificación para productos como reuniones con clientes y asignar un recurso.  

Una línea de planificación de un proyecto puede ser de uno de los siguientes tipos.  

| Tipo | Descripción |
| --- | --- |
| **Ppto** |Proporciona consumo y costes del proyecto estimados, habitualmente en un contrato de tiempo y tipo de proyecto. Las líneas de planificación de este tipo no pueden facturarse. |
| **Facturable** |Proporciona una facturación estimada al cliente, habitualmente en un proyecto de precio fijo. |
| **Presupuesto y facturable** |Proporciona el uso presupuestado igual a lo que se desea facturar. |

**Nota**. A medida que introduzca información en las líneas de planificación, la información de costes se completará automáticamente. Por ejemplo, el coste, el precio y el descuento de los recursos y productos se basarán inicialmente en la información que se haya definido en las fichas de los recursos y productos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.
2. Abra una ficha de un proyecto relevante.
3. Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.  
4. En la página **Líneas planificación proyecto**, en una línea nueva, rellene los campos según sea necesario.
5. Repita los pasos 3 y 4 para todas líneas de planificación que necesita para la tarea de proyecto.

## <a name="see-also"></a>Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]