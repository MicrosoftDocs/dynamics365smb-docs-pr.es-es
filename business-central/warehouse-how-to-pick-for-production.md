---
title: 'Realizar picking o mover artículos para producción, ensamblado o proyectos en una configuración básica de almacén'
description: 'Cuando el almacén requiere que procese el picking, pero no los envíos, utilice la página Picking inventario para registrar los componentes que fueron elegidos.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Realizar picking para producción, ensamblado o proyectos en una configuración básica de almacén

La forma de realizar el picking de componentes para fabricación, trabajos u órdenes de ensamblado depende de la configuración del almacén. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

En una configuración de almacén avanzada para el flujo de salida (picking), en la página **Tarjeta de almacén** para el almacén, active el control de alternancia **Picking requerido** y desactive el control de alternancia **Envío requerido**.

Use los siguientes documentos de origen para las operaciones internas:

* Picking inventario
* Movimiento inventario

## <a name="inventory-picks"></a>Picking de inventario

* Cuando registra un picking de inventario para una operación interna, como la producción o un trabajo, el consumo de los componentes seleccionados se registra al mismo tiempo.
* El control de alternancia **Ubicación obligatoria** en la página **Tarjeta del almacén** es opcional.
* Cuando se utiliza el picking de inventario, el campo **Cód. ubicación** de una línea de componente de orden de producción o en líneas de planificación de trabajos define la ubicación *traer*. Los componentes se reducen en la ubicación traer cuando registra el consumo.

## <a name="inventory-movements"></a>Movimientos de inventario

* Los movimientos de inventario requieren que active el control de alternancia **Ubicación obligatoria** en la página **Tarjeta de ubicación** para la ubicación.
* Los movimientos de inventario solo funcionan con líneas de componentes de órdenes de producción y líneas de órdenes de ensamblaje.
* Cuando registra un movimiento de inventario para una operación interna, se registra únicamente el movimiento físico de los componentes en una ubicación del área de operación. No se publica el consumo.
* Al utilizar movimientos de inventario, el campo **Código de ubicación** en las líneas de componente de orden de producción define la ubicación *apartado* en el área de la operación. La ubicación de Colocar es donde los empleados del almacén deben colocar los componentes.
* Registre el consumo de los componentes del picking por separado registrando un diario de consumo o una orden de ensamblaje.

>[!NOTE]
> Incluso si la opción **Picking requerido** está desactivada, puede usar un documento **Picking de almacén**. Los documentos de picking de almacén son similares a los documentos de **Picking de inventario**. Esto es útil si desea usar picking en operaciones y enviar en flujos de almacén de salida.

### <a name="production"></a>Producción

Utilice documentos de **Picking de inventario** para seleccionar componentes de producción en el flujo a producción.

Para una ubicación que usa ubicaciones, puede ampliar el flujo a producción usando documentos de **Movimiento de inventario**. Los movimientos de inventario son especialmente útiles para la baja de componentes. Para obtener más información acerca del procedimiento de bajada del consumo de componentes desde las ubicaciones para producción o de aprovisionamiento manual, consulte [Bajada de componentes de producción en una configuración de almacén básica](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Ensamblado

Utilice los documentos **Movimiento de inventario** para mover componentes del ensamblado al área de ensamblado.

> [!NOTE]
> Los documentos **Movimiento de inventario** requieren ubicaciones.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los tipos ensamblar para stock y ensamblar para pedido de los flujos de ensamblado. Para obtener más información sobre el ensamblado para pedido en el flujo de almacén saliente, vaya a [Tratamiento de productos para ensamblar para pedido en los pickings de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Administración de proyectos

Utilice documentos de **Picking de inventario** para seleccionar componentes de proyecto en el flujo a la administración de proyectos.

Para las ubicaciones que usen ubicaciones, puede ampliar el flujo a los trabajos con **Movimiento de inventario**.

> [!NOTE]
> Se agregó la capacidad de seleccionar componentes para las líneas de planificación de trabajos a [!INCLUDE[d365fin](includes/d365fin_md.md)] en el lanzamiento de versiones 2 de 2022. Para empezar a usar la capacidad, un administrador debe activar **Actualización de característica: habilitar el picking de almacén e inventario de los proyectos** en la página **Administración de características**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] utiliza el valor del campo **Cantidad restante** en la línea de planificación del trabajo cuando crea selecciones de inventario. Para usar selecciones de inventario para trabajos, debe activar la opción **Aplicar enlace de uso** en la página **Tarjeta de trabajo** para el trabajo. Esto le permite rastrear el uso contra su plan. Si no activa la opción, la cantidad restante permanecerá en **0** y la selección de inventario no se creará. Para obtener más información, consulte [Configurar seguimiento de uso de trabajo](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-jobs-in-a-basic-warehouse-configuration"></a>Realizar picking o mover a producción, ensamblado y proyectos en una configuración básica de almacén

Puede crear un picking de inventario o movimientos de inventario de tres formas:  

* Desde el propio documento de origen.  
* Para diversos documentos de origen al mismo tiempo utilizando un trabajo por lotes.  
* En dos pasos. Libere el documento de origen para que esté listo para el picking. Cree el movimiento o picking de inventario a partir de los documentos **Picking de inventario** o **Movimiento de inventario**. El picking o movimiento de inventario están basados en el documento de origen.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Para crear un picking de inventario desde el documento de origen

1. En el documento de origen, que puede ser una orden de producción o un trabajo, elija la acción **Crear almacenamiento/picking de inventario**.  
2. Seleccione la casilla **Crear picking de inventario**.
3. Elija el botón **Aceptar**.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Para crear un movimiento de inventario desde el documento de origen

1. En el documento de origen, que puede ser una orden de producción, una orden de ensamblado o un trabajo, elija la acción **Crear almacenamiento/picking de inventario**.  
2. Seleccione la casilla de verificación **Crear movimiento de inventario**.
3. Elija el botón **Aceptar**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Para crear varios picking o movimientos de inventario con un trabajo por lotes

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear almacenamiento/picking/movimiento de inventario** y, a continuación, elija el vínculo relacionado.  
2. En la ficha desplegable **Solicitud almacén**, use los campos **Documento origen** y **Cód. procedencia mov.** para filtrar tipos de documentos o intervalos de números de documento. Por ejemplo, puede crear picking solo de los pedidos de producción.
3. En la ficha desplegable **Opciones**, active los controles deslizantes **Crear picking de inventario** o **Crear movimiento de inventario**.
4. Elija el botón **Aceptar**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Para crear pickings o movimientos de inventario en dos pasos

Para seleccionar o mover componentes para documentos de origen en dos pasos, debe liberar el documento de origen para que esté listo para picking. Lance los documentos de origen para las operaciones internas de las siguientes formas.  

|Documento origen|Método de lanzamiento|  
|---------------------|--------------------|  
|Orden producción|En la página **Orden de producción planificada**, cambie el estado de un pedido a **Liberado** o use la página **Orden de producción liberada** para crear una orden de producción liberada.|  
|Pedido de ensamblado|Cambiar el estado de una orden de ensamblado a **Liberado**.|
|Proyectos | Cambie el estado del trabajo **Abierto** o cree un trabajo con el estado Abierto de inmediato.|  

Un empleado de almacén asignado al picking de artículos puede crear un documento de almacenamiento de inventario para el documento de origen.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking de inventario** o **Movimiento de inventario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Documento origen**, seleccione el tipo de documento de origen para el que es el almacenamiento.

    > [!NOTE]
    > No puede usar documentos de **Picking de inventario** para seleccionar componentes del ensamblado.
4. En el campo **Cód. procedencia mov.**, seleccione el documento de origen.  
5. También puede elegir la acción **Traer documento origen** para seleccionar un documento de una lista de documentos de origen de entrada que están preparados para el picking en el almacén.  
6. Elija el botón **Aceptar** para rellenar las líneas de picking o movimientos según el documento de origen seleccionado.  

## <a name="to-record-the-inventory-pick"></a>Para registrar el picking de inventario

1. En la página **Picking inventario**, abra el documento para el que registrar el picking.  
2. En el campo **Cód. ubicación** en las líneas de picking, la ubicación desde donde se debe realizar el picking de productos donde el producto está disponible. Puede cambiar la ubicación si lo necesita.
3. Realice el picking e introduzca la cantidad de picking en el campo **Cdad. a manipular**.

    Si debe hacer el pikcing de los producto para una línea de más de una ubicación, por ejemplo porque la ubicación no contiene la cantidad total, utilice la acción **Dividir línea** de la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.  
4. Seleccione la acción **Registrar**.  

Lo siguiente sucede durante el proceso de publicación:

* Registre el consumo de las líneas del documento de origen donde se realizó el picking.
* Si el almacén utiliza ubicaciones, el registro también creará movimientos de almacén para registrar los cambios de cantidad de la ubicación.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>Para registrar el movimiento de inventario

1. En la página **Movimiento de inventario**, abra el documento para registrar el movimiento.  
2. En el campo **Cód. ubicación**, en las líneas de movimientos, la ubicación desde la cual se debe realizar el picking se sugiere en función de la ubicación predeterminada del producto y la disponibilidad. Puede cambiar la ubicación si lo necesita.  
3. Realice el movimiento e introduzca la cantidad que se movió en el campo **Cdad. a manipular**. El valor de Toma y las líneas de Plaza deben iguales. Si no, no podrá registrar el movimiento.

    Si debe traer los producto para una línea de más de una ubicación, por ejemplo porque la ubicación no contiene la cantidad total, utilice la acción **Dividir línea** de la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.  
4. Elija la acción **Registro movimiento de inventario**.  

Lo siguiente sucede durante el proceso de publicación:

* Los movimientos de almacén ahora indican que los componentes ahora están en las ubicaciones especificadas en las líneas del pedido de documento de origen. Por ejemplo, la orden de ensamblaje, el componente de producción o la línea de planificación del trabajo.

>[!NOTE]
> A diferencia de cuando se mueven los componentes con pickings de inventario, el consumo no se registra cuando se registra un movimiento de inventario. El consumo se registra como un paso separado al contabilizar el documento de origen.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>La bajada de los componentes para producción en una configuración básica de almacén

Los métodos de baja afectan al flujo de componentes en producción. Obtenga más información en [Bajar componentes según la salida de la operación](production-how-to-flush-components-according-to-operation-output.md). Según el método de bajada seleccionado, puede realizar el picking de componentes para la producción de las siguientes maneras:

* Utilice un documento de **Picking de inventario** para registrar la selección de productos que usan el método de vaciado **Manual**. Cuando registra un picking de inventario, se registra el consumo de los componentes seleccionados. 
* Utilice un documento de **Movimiento de inventario** con una referencia a un documento de origen para registrar los pickings de los componentes que utilizan el método de bajada **Manual**. Deberá registrar el consumo por separado. Obtenga más información en [Registrar consumibles de producción por lotes](production-how-to-post-consumption.md). 
* Utilice un documento de **Movimiento de inventario** con una referencia a un documento de origen para registrar los pickings para los componentes que utilizan el método de bajada **Picking + Adelante**, **Picking + Atrás**. El consumo de los componentes se producirá automáticamente cuando cambie el estado de la orden de fabricación o al iniciar o finalizar una operación. Todos los componentes necesarios deben estar disponibles. De lo contrario, el registro del consumo de baja se detiene para ese componente.
* Use un documento de **Movimiento de inventario** sin una referencia a un documento de origen u otras formas de registrar el movimiento de componentes que usan el método de baja **Adelante** o **Atrás** . El consumo de los componentes se producirá automáticamente cuando cambie el estado de la orden de fabricación o al iniciar o finalizar una operación. Todos los componentes necesarios deben estar disponibles. De lo contrario, el registro del consumo de baja se detiene para ese componente. Obtener más información en [Mover productos internamente en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Ejemplo:

Tiene un pedido de fabricación de 15 unidades del producto SP-SCM1004. Algunos de los productos de la lista de componentes deben darse de baja manualmente en un diario de consumo, y en los demás productos se puede llevar a cabo el picking y la bajada automáticamente mediante el método de baja **Pick + Atrás**.  

En los pasos siguientes se ofrece un ejemplo de las acciones correspondientes para distintas personas y las respuestas relacionadas:  

1. El supervisor de planta lanza la orden de producción. Los productos con el método de baja **Anticipada** y sin conexión de ruta se deducen de la ubicación de aprovisionamiento manual.  
2. El supervisor de planta elige la acción **Crear picking/almacenamiento de inventario** en la orden de producción y activa la acción **Crear picking de inventario** y **Crear movimiento de inventario**. Se crea un documento de selección de almacén para productos con el método de bajada **Manual** y se crea un movimiento de inventario para los productos con los métodos de bajada **Picking + Atraás** y **Picking + Adelante**.
3. El administrador de almacén asigna los picking y los movimientos a un empleado de almacén.
4. El empleado del almacén realiza el picking de los productos desde las ubicaciones apropiadas y los coloca en la ubicación Para producción o en la ubicación especificada en movimiento de inventario. La ubicación puede ser una ubicación de centro de trabajo o de centro de máquina.  
5. El empleado de almacén registra el picking. La cantidad se deduce de las ubicaciones.
6. El empleado de almacén registra el movimiento. La cantidad se deduce de las ubicaciones de picking y se agregan a la ubicación de consumo. Se actualiza el campo **Cdad. preparada pedido** de la lista de componentes para todos los productos preparados.  
7. El operador de máquina notifica al director de producción que se han completado los productos finales.  
8. El supervisor de planta utiliza el diario de salida o el diario de producción para contabilizar la salida. La cantidad de elementos de componentes que utilizan los métodos de baja **Pick + Adelante** o **Pick + Atrás** con vínculos de enrutamiento se deduce de la papelera A producción.
9. El administrador de producción cambia el estado del pedido de producción y modifica el estado a **Terminado**. La cantidad de productos componentes que usan el método de baja **Atrás** se deduce de la ubicación de aprovisionamiento manual y la cantidad de los productos componentes que usan el método de baja **Pick + Atrás** y no se deduce ningún vínculo de enrutamiento de la ubicación para producción.  

 En la ilustración siguiente se muestra cuando se rellena el campo **Cód. ubicación** de la lista de componentes según la configuración de la máquina o del centro de trabajo.  

:::image type="content" source="media/binflow.png" alt-text="Descripción general de cuándo y cómo se rellena el campo Código de ubicación.":::

## <a name="see-also"></a>Consulte también .

[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Administración de ensamblados](assembly-assemble-items.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
