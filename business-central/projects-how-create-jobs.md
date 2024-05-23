---
title: Crear una ficha de proyecto para un proyecto y especificar las tareas
description: 'Para un proyecto nuevo, cree una ficha de proyecto que contenga tareas y líneas de planificación, como ayuda para administrar el progreso y los presupuestos.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Crear proyectos

Cuando inicie un proyecto nuevo, debe crear una ficha de proyecto con tareas de proyecto integradas y líneas de planificación de proyecto, estructuradas en dos niveles.  

La primera capa consta de tareas de proyecto. Debe crear al menos una tarea de proyecto por cada proyecto porque todos los registros hacen referencia a una tarea de proyecto. Tener al menos una tarea de proyecto en su proyecto le permite configurar líneas de planificación de proyecto y registrar el consumo en el proyecto.

La segunda capa consta de líneas de planificación de proyecto, que especifican el uso detallado de los recursos, productos y diversos gastos de contabilidad general.

La estructura de capas permite dividir el proyecto en tareas más pequeñas y usar detalles más específicos en el presupuesto, las ofertas y el registro. Además, le ofrece información de cómo está progresando un proyecto. Por ejemplo, puede hacer un seguimiento de si está alcanzando los hitos señalados o si va encaminado a cumplir las expectativas de presupuesto.

> [!TIP]
> Elija la acción **Proyecto nuevo** en el área de trabajo **Administrador del proyecto** para iniciar una guía configuración asistida que le lleva por los pasos para crear un proyecto con tareas integradas y líneas de planificación. El procedimiento siguiente describe cómo realizar los pasos manualmente. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Facturar a uno o más clientes por tareas del proyecto

A veces, la parte a la que recibe un servicio es diferente de la parte que paga la factura. Además, en ocasiones es posible que necesites facturar a varios clientes por las tareas del proyecto. En la página **Tarjeta de proyecto**, use el campo **Método de facturación de tareas** para especificar si está facturando a un cliente, o múltiples clientes.

Si el cliente que está recibiendo el servicio también pagará la factura, en los campos **Facturar a** y **Enviar a** campos, elija **Predeterminado (Cliente)** y **Predeterminado (Dirección de venta)**.

Si factura a varios clientes, puede especificar el cliente que recibirá el servicio y el cliente al que facturar por cada tarea del proyecto. También puede proporcionar la siguiente información:

* Dónde se llevará a cabo el trabajo seleccionando en una lista de direcciones de envío para el cliente.
* Agregue información sobre referencias externas para simplificar la comunicación sobre el proyecto.
* Sobrescriba los términos financieros estándar del proyecto.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Facturar a un cliente por varias tareas del proyecto

Puede simplificar su proceso de facturación enviando una factura a un cliente para varios proyectos. Agregue líneas de planificación de proyectos de varios proyectos a una factura de ventas de una sola vez. Este proceso es similar a crear una factura de ventas a partir de una línea de planificación de proyecto e ingresar un valor en el campo **Agregar al número de factura de ventas**.

Visión general del proceso de integración

1. Cree una factura de ventas nueva y rellene el **N.º vender a cliente** . Si es necesario, complete también el **N.º de cliente de facturación.** y los campos **Código de divisa**.
2. En la ficha desplegable **Líneas**, elija la acción **Obtener líneas de planificación de proyecto**. La página **Obtener líneas de planificación de proyectos** muestra líneas de planificación de proyectos facturables de proyectos para el cliente vendedor, el cliente facturado y la moneda de facturación donde la cantidad a facturar es superior a cero. 
3. Elija las líneas que quiera agregar a al factura y después elija **Aceptar**.

Repita estos pasos si desea agregar otro conjunto de líneas de planificación de proyectos. También puede eliminar la factura o sus líneas y empezar de nuevo.

> [!NOTE]
> Hay un par de limitaciones:
>
> * La acción **Obtener líneas de planificación de proyectos** no está disponible en pedidos de venta o cotizaciones de venta.
> * No puede filtrar por el **Código de envío** o **Número de contacto.** .

## <a name="to-create-a-project-card"></a>Para crear una ficha de proyecto

Cree una ficha de proyecto y, a continuación, cree las líneas de tarea de proyecto y las líneas de planificación de proyecto para el mismo.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para basar el proyecto en información de otro proyecto, elija la acción **Copiar proyecto**, rellene los campos según sea necesario y después elija el botón **Aceptar**.

> [!NOTE]  
> Si utiliza las hojas de horas con su proyecto, también debe designar una persona responsable. Esta persona puede aprobar las hojas de horas para las tareas de empleados asociadas con el proyecto. Para obtener más información, consulte [Configurar partes de horas](projects-how-setup-time-sheets.md).

Opcionalmente, marque las acciones del proyecto como bloqueadas utilizando el campo **Bloqueado**. la siguiente tabla describe el efecto de las opciones de este campo.

|Opción  |Descripción  |
|---------|---------|
|En blanco |Se permiten todas las acciones.|
|Registro    |Podrá trabajar con las líneas de planificación, pero estará bloqueado el registro para el proyecto. Si elige esta opción, no podrá registrar ningún consumo o ventas relacionados con el proyecto.|
|Todo  |Todas las acciones están bloqueadas.|

## <a name="to-create-tasks-for-a-project"></a>Para crear tareas para un proyecto

Una parte clave de la creación de un proyecto es especificar las diversas tareas que conlleva. Para especificar tareas, debe crear una línea por tarea en la ficha desplegable **Tareas** de la página **Ficha de proyecto**. Cada proyecto debe tener al menos una tarea.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.
2. Abra la ficha de proyecto de un proyecto relevante.
3. En la ficha desplegable **Tareas**, rellene los campos según sea necesario en una nueva línea.
4. Para indentar las tareas y crear una jerarquía, elija la acción **Tareas** y, a continuación, elija la acción **Indentar tareas proyecto**.
5. Repita los pasos 3 y 4 para todas las tareas que necesite para el proyecto.
6. Para especificar las tareas de proyecto con la información sobre otras tareas de proyecto, elija la acción **Copiar tareas de proyecto desde**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="to-create-planning-lines-for-a-project"></a>Para crear líneas de planificación de un proyecto

Puede redefinir las nuevas tareas de proyecto como líneas de planificación de proyecto. Una línea de planificación puede capturar la información de un proyecto que desee supervisar. Por ejemplo, puede realizar un seguimiento de los recursos que requiere el proyecto o los productos que se necesitan. Por ejemplo, tiene una tarea para lograr que un cliente apruebe un proyecto. Puede asociar esa tarea con líneas de planificación para productos como reuniones con clientes y asignar un recurso.  

Una línea de planificación de un proyecto puede ser de uno de los siguientes tipos.  

| Tipo | Descripción |
| --- | --- |
| **Presupuesto** |Proporciona consumo y costes del proyecto estimados, habitualmente en un contrato de tiempo y tipo de proyecto. Las líneas de planificación de este tipo no pueden facturarse. |
| **Facturable** |Proporciona una facturación estimada al cliente, habitualmente en un proyecto de precio fijo. |
| **Presupuesto y facturable** |Proporciona el uso presupuestado igual a lo que se desea facturar. |

> [!NOTE]
> A medida que introduzca información en las líneas de planificación del proyecto, la información de costes se completará automáticamente. Por ejemplo, el coste, el precio y el descuento de los recursos y productos se basarán en la información de los recursos y productos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.
2. Abra una ficha de un proyecto relevante.
3. Seleccione una tarea de proyecto cuyos campo **Tipo tarea proyecto** contenga **Registrar** y seleccione la acción **Líneas planificación proyecto**.  
4. En la página **Líneas planificación proyecto**, en una línea nueva, rellene los campos según sea necesario.
5. Repita los pasos 3 y 4 para todas líneas de planificación que necesita para la tarea de proyecto.

## <a name="see-also"></a>Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Vídeo: Cómo crear un proyecto en Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
