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
ms.openlocfilehash: 6996c82ee184db980879ea98a6f2cbdca1b10852
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557198"
---
# <a name="create-jobs"></a>Crear proyectos
Cuando inicie un proyecto nuevo, debe crear una ficha de proyecto con tareas de proyecto integradas y líneas de planificación de proyecto, estructuradas en dos niveles.  

La primera capa consta de tareas de proyecto. Debe crear al menos una tarea de proyecto por cada proyecto porque todos los registros hacen referencia a una tarea de proyecto. Tener al menos una tarea de proyecto en su proyecto le permite configurar líneas de planificación de proyecto y registrar el consumo en el proyecto.

La segunda capa consta de líneas de planificación de proyecto, que especifican el uso detallado de los recursos, productos y diversos gastos de contabilidad general.

La estructura de capas permite dividir el proyecto en tareas más pequeñas y usar detalles más específicos en el presupuesto, las ofertas y el registro. Además, le ofrece información de cómo está progresando un proyecto. Por ejemplo, puede hacer un seguimiento de si está alcanzando los hitos señalados o si va encaminado a cumplir las expectativas de presupuesto.

> [!TIP]
> Elija la acción **Proyecto nuevo** en el área de trabajo **Administrador del proyecto** para iniciar una guía configuración asistida que le lleva por los pasos para crear un proyecto con tareas integradas y líneas de planificación. El procedimiento siguiente describe cómo realizar los pasos manualmente. Para ver un ejemplo de cómo crear un trabajo manualmente, consulte [Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

A veces, la parte a la que recibe un servicio es diferente de la parte que paga la factura. En la página **Trabajos**, puede especificar el cliente que se beneficiará del proyecto en los campos **Vender a** y la parte a facturar en los campos **Cobrar a**. También puede proporcionar la siguiente información: 

* Dónde se llevará a cabo el trabajo seleccionando en una lista de direcciones de envío para el cliente.
* Agregue información sobre referencias externas para simplificar la comunicación sobre el proyecto.
* Sobrescriba los términos financieros estándar del proyecto.

## <a name="to-create-a-job-card"></a>Para crear una ficha de proyecto
Cree una ficha de proyecto y, a continuación, cree las líneas de tarea de proyecto y las líneas de planificación de proyecto para el mismo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para especificar el proyecto con la información sobre otros proyectos, elija la acción **Copiar proyecto**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

> [!NOTE]  
>   Si utiliza las hojas de horas con su proyecto, también debe designar una persona responsable. Esta persona puede aprobar las hojas de horas para las tareas de empleados asociadas con el proyecto. Para obtener más información, consulte [Configurar hojas de horas](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Para crear tareas para un proyecto
Una parte clave de la creación de un proyecto es especificar las diversas tareas que conlleva. Para especificar tareas, debe crear una línea por tarea en la ficha desplegable **Tareas** de la página **Ficha de proyecto**. Cada proyecto debe tener al menos una tarea.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.
2. Abra la ficha de un proyecto relevante.
3. En la ficha desplegable **Tareas**, rellene los campos según sea necesario en una nueva línea.
4. Para indentar las tareas y crear una jerarquía, elija la acción **Tareas** y, a continuación, elija la acción **Indentar tareas proyecto**.
5. Repita los pasos 3 y 4 para todas las tareas que necesite para el proyecto.
6. Para especificar las tareas de proyecto con la información sobre otras tareas de proyecto, elija la acción **Copiar tareas de proyecto desde**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="to-create-planning-lines-for-a-job"></a>Para crear líneas de planificación de un proyecto
Puede redefinir las nuevas tareas de proyecto como líneas de planificación de proyecto. Una línea de planificación puede capturar la información de un proyecto que desee supervisar. Por ejemplo, puede realizar un seguimiento de los recursos que requiere el proyecto o los productos que se necesitan. Por ejemplo, tiene una tarea para lograr que un cliente apruebe un proyecto. Puede asociar esa tarea con líneas de planificación para productos como reuniones con clientes y asignar un recurso.  

Una línea de planificación de un proyecto puede ser de uno de los siguientes tipos.  

| Tipo | Descripción |
| --- | --- |
| **Ppto** |Proporciona consumo y costes del proyecto estimados, habitualmente en un contrato de tiempo y tipo de proyecto. Las líneas de planificación de este tipo no pueden facturarse. |
| **Facturable** |Proporciona una facturación estimada al cliente, habitualmente en un proyecto de precio fijo. |
| **Presupuesto y facturable** |Proporciona el uso presupuestado igual a lo que se desea facturar. |

> [!NOTE]
> A medida que introduzca información en las líneas de planificación, la información de costes se completará automáticamente. Por ejemplo, el coste, el precio y el descuento de los recursos y productos se basarán en la información de los recursos y productos. 

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.
2. Abra una ficha de un proyecto relevante.
3. Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.  
4. En la página **Líneas planificación proyecto**, en una línea nueva, rellene los campos según sea necesario.
5. Repita los pasos 3 y 4 para todas líneas de planificación que necesita para la tarea de proyecto.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Crear documentos de picking de almacén e inventario para un proyecto
Para crear documentos de picking de almacén de inventario para proyectos, su administrador debe habilitar **Actualización de característica: habilitar el picking de almacén e inventario de los proyectos** en la página **Administración de características**.

La función agrega las acciones **Crear picking inventario** y **Crear picking almacén** en **Ficha de proyecto**. Para crear o registrar un documento de selección, utilice las acciones **Líns. almac./picking/Líneas movimiento** o **Líneas de picking registradas**.

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

## <a name="see-also"></a>Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]