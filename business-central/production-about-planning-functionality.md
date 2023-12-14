---
title: Acerca de la funcionalidad de la planificación
description: Aprenda cómo la planificación utiliza datos de oferta y demanda para sugerir cómo equilibrar la oferta para satisfacer la demanda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.form: '5430,'
ms.date: 09/19/2023
ms.custom: bap-template
---
# <a name="about-planning-functionality"></a>Acerca de la funcionalidad de la planificación

El programa de planificación tiene en cuenta todos los datos del aprovisionamiento y la demanda, cuadra el resultado y genera sugerencias para hacer que el aprovisionamiento satisfaga la demanda.  

Para obtener información detallada, consulte [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md).  

> [!NOTE]  
> En todos los campos que se mencionan en este tema, lea la información de herramienta para entender su función. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="supply-and-demand"></a>Oferta y demanda

La planificación tiene dos elementos: demanda y aprovisionamiento. Estos deben equilibrarse para garantizar que se satisfaga la demanda.  

- Demanda es todo tipo de necesidades brutas, como pedido de venta, pedido de servicio, necesidad de componentes de una orden de producción, transferencia de salida, pedido abierto o previsión. Además, hay otros tipos técnicos de demanda, por ejemplo una orden de producción o un pedido de compra negativos, existencias negativas y devoluciones de compras.  
- Aprovisionamiento se refiere a todo tipo de reposición: existencias, pedido de compra, pedido de ensamblado, orden de producción o transferencia de entrada. A la inversa, puede haber un pedido de venta o de servicio negativo, una necesidad de componente negativo o una devolución de ventas que representen también un aprovisionamiento.  

Otro objetivo del sistema de planificación es el de garantizar que las existencias no aumentan innecesariamente. En el caso de un descenso de la demanda, el programa de planificación sugerirá que se pospongan o cancelen algunos de los pedidos de reposición existentes, o que se reduzca sus cantidades.  

## <a name="planning-calculation"></a>Cálculo de la planificación

El programa de planificación está controlado por la demanda, estimada y real, de los clientes, además de los parámetros de reaprovisionamiento de existencias. Si se ejecuta el cálculo de la planificación, la aplicación sugerirá acciones concretas ([Mensajes de acción](production-how-to-run-mps-and-mrp.md#action-messages)) que se deben emprender en relación con una posible reposición de los proveedores, transferencias entre almacenes, o producción. Si ya hay pedidos de reposición, las acciones sugeridas pueden ser aumentar o acelerar los pedidos para satisfacer los cambios de la demanda.  

La base de la rutina de planificación es el cálculo bruto-neto. Las necesidades netas controlan la emisión de pedidos planificados, que se programan en función de la información sobre rutas (productos fabricados) o el plazo de seguridad de la ficha de producto (productos comprados). Las cantidades de los pedidos planificados se basan en el cálculo de la planificación y se ven afectadas por los parámetros definidos en cada una de las fichas de producto.  

> [!TIP]
> El programa de planificación se basa en cómo su organización utiliza los almacenes. Para obtener más información, consulte [Planificación con o sin almacenes](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a>Planificación con pedidos de transferencia manuales

En el campo **Sistema reposición** de una ficha de unidad de almacenamiento, puede configurar el programa de planificación para que cree pedidos de transferencia que equilibren el suministro y la demanda entre los distintos almacenes.  

Además de dichos pedidos de transferencia automáticos, puede que a veces sea necesario realizar un traslado general de cantidades en existencia a otro almacén, independientemente de la demanda existente. Para ello debería crear manualmente un pedido de transferencia con la cantidad que trasladar. Para garantizar que el sistema de planificación no intenta manipular este pedido de transferencia manual, debe establecer el campo **Flexibilidad de planificación** de las líneas de transferencia en Ninguna.  

Por el contrario, si desea que el sistema de planificación ajuste las cantidades del pedido de transferencia y las fechas para la demanda existente, debe establecer el campo **Flexibilidad de planificación** en el valor predeterminado, Ilimitada.

## <a name="planning-parameters"></a>Parámetros de la planificación

Los parámetros de la planificación controlan cuándo, en qué cantidad y cómo realizar el reaprovisionamiento, en función de diversas opciones de la ficha de producto (o unidad de almacenamiento, SKU) y de la configuración de la fabricación.  

Existen los siguientes parámetros de planificación en la ficha del producto o de la UA:  

- Periodo amortiguador  
- Cantidad amortiguador  
- Directiva reaprov.  
- Punto pedido
- Stock máximo  
- Nivel desbordamiento  
- Ciclo  
- Periodo de acumulación de lotes  
- Periodo de reprogramación  
- Cantidad a pedir  
- Plazo de seguridad  
- Stock de seguridad  
- Directiva de ensamblado  
- Política fabricación  

Existen los modificadores de pedido en la ficha del producto o de la UA:  

- Cantidad mínima pedido  
- Cantidad máxima pedido  
- Múltiplos de pedido  

Los campos de configuración de planificación global de la página **Configuración de fabricación** son:  

- Cód. niv. más bajo dinámico  
- Previsión de la demanda actual  
- Previsiones en almacénes  
- Plazo seguridad genérico  
- Nivel desbordamiento en blanco  
- Combinar cálc. MPS/MRP
- Componentes en alm.  
- Periodo predet. amortiguador  
- Cantidad predet. amortiguador  

Para obtener más información, consulte [Detalles de diseño: parámetros de planificación](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Otros campos importantes de planificación

### <a name="planning-flexibility"></a>Flexib. planificación

En la mayoría de pedidos de suministros, como pedidos de producción, puede seleccionar **Ilimitada** o **Ninguna** en el campo **Flexibilidad de planificación** en las líneas.

Esto especifica si el sistema de planificación tiene en cuenta el suministro representado en la línea del pedido de producción al calcular mensajes de acción.
Si el campo contiene la opción **Ilimitada**, el sistema de planificación incluye la línea cuando calcula mensajes de acción. Si en el campo está especificada la opción **Ninguna**, la línea es firme e invariable, y el sistema de planificación no la incluye al calcular los mensajes de acción.

### <a name="warning"></a>Advertencia

El campo de información **Advertencia**, la página **Hoja de planificación** le indica las líneas de planificación creadas para una situación inusual, con un texto que el usuario puede elegir para leer información adicional. Existen los siguientes tipos de advertencia:

- Emergencia
- Excepción
- Atención
- Emergencia

La advertencia de emergencia se muestra en dos situaciones:

- El inventario es negativo en la fecha de inicio de la planificación.
- Existen eventos de demanda u oferta atrasados.

Si el inventario de un producto es negativo en la fecha de inicio de la planificación, el sistema de planificación le sugiere un pedido de suministro de emergencia para la cantidad negativa que llegue en la fecha de inicio de la planificación. El texto de advertencia informa de tal fecha y de la cantidad del pedido de emergencia.

Todas las líneas de documento con fecha de vencimiento antes de la fecha de inicio de la planificación se consolidan en un pedido de demanda de emergencia para que el elemento llegue en la fecha de inicio de la planificación.

### <a name="exception"></a>Excepción

Se mostrará la advertencia de excepción si el inventario disponible previsto cae por debajo de la cantidad de existencias de seguridad.

El programa de planificación sugerirá un pedido de suministros para cubrir la demanda en la fecha de vencimiento. El texto de advertencia informa de la cantidad de existencias de seguridad del producto y de la fecha en la que se infringe.

Infringir el nivel de existencias de seguridad está considerado una excepción debido a que no debería ocurrir si se configura correctamente el punto de nuevo pedido.

> [!NOTE]
> El suministro de las líneas de planificación con advertencias de excepción no se modifica normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere solo un suministro para satisfacer la cantidad exacta de demanda. Sin embargo, puede configurar la ejecución de la planificación para que respete ciertos parámetros de planificación para las líneas de planificación con determinadas advertencias. Para obtener más información, consulte la descripción del campo **Respetar parámetros de planificación para las advertencias de excepción** en el artículo [Ejecutar la planificación completa, MPS o MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Atención

La advertencia de emergencia se muestra en dos situaciones:

- La fecha de inicio de la planificación es anterior a la fecha de trabajo.
- La línea de planificación sugiere cambiar una compra realizada o una orden de producción.

> [!NOTE]
> En las líneas de planificación con advertencias, el campo **Aceptar mensaje acción** está desactivado, ya que se espera que el planificador investigue estás líneas más detalladamente antes de llevar a cabo el plan.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planificación de hojas de planificación y hojas de demanda

Como se describe en [Planificación](production-planning.md), puede elegir entre dos hojas de trabajo para la mayoría de las actividades de planificación, la hoja de planificación y la hoja de demanda. La mayoría de los procesos se describen en función de la hoja de planificación, pero hay un par de escenarios en los que se prefiere la hoja de demanda.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

### <a name="requisition-worksheet"></a>Hoja de demanda

La página **Hoja demanda** incluye una lista de productos que desea solicitar. Los productos se pueden introducir en la hoja de varias formas:

- Introduzca los productos manualmente en la hoja y rellene los campos pertinentes.

- Use el trabajo por lotes **Calcular plan**. De este modo, se calculará un plan de reposición para los productos y las unidades de almacenamiento que se han configurado con un sistema de reposición de **Compra** o **Transferencia**. Cuando utilice este proceso, el programa rellenará automáticamente el campo **Mensaje acción** con una acción recomendada que puede realizar para reponer el producto. Esta acción podría, por ejemplo, aumentar la cantidad del producto en un pedido existente o crear un nuevo pedido.

- Si ha utilizado el proceso **Calcular plan** desde la página **Hoja planificación** para calcular un plan de reposición, puede aplicar el proceso **Ejecutar mensajes acción** para copiar las propuestas de pedido de compra y transferencia de la hoja de planificación a la hoja de demanda. Esto es práctico si separa los usuarios responsables de la gestión de órdenes de producción de los responsables de pedidos de compra y transferencia.

- Puede utilizar la acción **Envío directo** para rellenar las líneas de la hoja de demanda. Esta acción utiliza el proceso **Traer pedidos venta** para determinar las líneas de pedido de venta que desea asignar a un envío directo.

- Puede utilizar la acción **Pedido especial** para rellenar las líneas de la hoja de demanda. Esta acción utiliza el proceso **Traer pedidos venta** para determinar las líneas de pedido de venta que desea asignar a un envío especial.

Las líneas de la hoja de demanda contienen información detallada sobre los productos que es necesario reaprovisionar. Puede editar y eliminar líneas para ajustar su plan de reposición y, más tarde, procesar las líneas con el proceso **Ejecutar mensajes acción**. 

Para obtener detalles sobre la planificación con ubicaciones y transferencias, consulte [Planificación con o sin ubicaciones](production-planning-with-without-locations.md).

> [!TIP]
> Cuando trabaje en las páginas **Hoja de demanda** u **Hoja de planificación**, puede organizar las líneas ordenándolas por nombre de columna. Esto es especialmente útil en la página Hoja de planificación porque se puede usar para órdenes de producción de varios niveles. De forma predeterminada, las líneas se ordenan por el campo **N.º producto**. Para agrupar líneas de un pedido de varios niveles, ordene según el **Nº orden ref.** . También los campos **Orden MPS** y **Nivel de planificación** pueden ayudar a mostrar la jerarquía de las líneas.

## <a name="see-also"></a>Consulte también .

[Detalles de diseño: planificación de suministro](design-details-supply-planning.md)  
[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
