---
title: 'Ejecutar la planificación completa, MPS o MRP'
description: 'El programa de planificación puede calcular tanto el Programa de producción principal (MPS) como la Planificación de necesidades de material (MRP) cuando se solicite, o ambas cosas a la vez.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: andreipa
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="run-full-planning-mps-or-mrp"></a>Ejecutar la planificación completa, MPS o MRP

Los términos "ejecutar la hoja de planificación" o "ejecutar MRP" hacen referencia al cálculo del programa de producción principal y a las necesidades de material. El cálculo se basa en la demanda real y prevista. El programa de planificación puede calcular tanto el Programa de producción principal (MPS) como la Planificación de necesidades de material (MRP) cuando se solicite, o ambas cosas a la vez.  

- MPS se refiere al cálculo de un programa de producción principal basado en la demanda real y en la previsión de demanda. El cálculo de MPS se utiliza para productos finales que tengan una previsión o una línea de pedido de venta. Estos productos se denominan "productos de MPS" y se identifican dinámicamente al iniciarse el cálculo.  
- MRP se refiere al cálculo de las necesidades de material basado en la demanda real de componentes y en la previsión de demanda de componentes. Sólo se calcula para los productos que no son productos de MPS. La finalidad de MRP es ofrecer planes formales con fases temporales, por producto, para suministrar el producto adecuado, en el momento correcto, en el lugar convenido y en la cantidad justa.  

Los algoritmos de planificación para MPS como para MRP son los mismos. Los algoritmos relativos a saldos netos reutilizan órdenes de reposición existentes y mensajes de acción. El proceso del sistema de planificación examina lo que se necesita o se va a necesitar (la demanda) y lo que hay físicamente o se espera que haya (el suministro). Cuando estas cantidades se comparan, [!INCLUDE[prod_short](includes/prod_short.md)] proporciona mensajes de acción. Los mensajes de acción son sugerencias para crear un pedido nuevo, para cambiar un pedido (la cantidad o la fecha) o para cancelar un pedido. El término "pedido" incluye pedidos de compra, pedido de ensamblado, pedidos de producción y pedidos de transferencia.

Puede seguir los vínculos creados por la planificación entre la demanda y el abastecimiento correspondiente en la página **Seguimiento pedido**. Para obtener más información, vea [Seguimiento de relaciones entre demanda y suministro](production-how-track-demand-supply.md).

Para obtener buenos resultados en la planificación, se deben haber configurado correctamente las siguientes opciones: fichas de producto, L.M. de ensamblado. L.M. de producción y rutas.  

## <a name="methods-for-generating-a-plan"></a>Métodos para generar un plan

- **Calc. planif. regenerativa** procesa o vuelve a generar el plan de materiales. El proceso comienza con la eliminación de todos los pedidos de aprovisionamiento cargados actualmente. Se vuelven a planificar todos los productos de la base de datos.  
- **Calc. plan. cambio periodo**: procesa un plan de cambio neto. Los productos se tienen en cuenta en una planificación de cambio neto de dos tipos de cambios:  
   - **Cambios de demanda y suministro:** son las modificaciones de las cantidades en los pedidos de venta, las previsiones de demanda, los pedidos de ensamblado, las órdenes de producción o los pedidos de compra. También se considera como cambio de cantidad un cambio en el nivel de existencias no planificado.  
   - **Cambios de parámetros de planificación:** son cambios en el stock de seguridad, el punto de pedido, la ruta, la lista de materiales, y cambios en el cálculo de ciclo o plazo de entrega.  
- **Traer mensajes acción:** irve como herramienta de planificación a corto plazo, ya que emite mensajes de acción para alertar al usuario sobre las modificaciones realizadas desde la última vez que se calculó el plan regenerativo o de cambio neto.  

Con cada método previsto, [!INCLUDE[prod_short](includes/prod_short.md)] genera las entradas en la hoja de trabajo asumiendo que la capacidad es infinita. El centro de trabajo y de maquinaria no se tiene en cuenta cuando se desarrollan esquemas.  

> [!IMPORTANT]  
> Calc. planif. regenerativa es el proceso más común. Sin embargo, Calcular plan y Ejecutar mensajes acción se pueden usar para ejecutar el proceso Calc. plan. saldo periodo.  
>
> Puede ejecutar el plan Obtener mensajes de acción entre ejecuciones de planificación de cambios netos y regenerativos para obtener una vista inmediata del efecto de los cambios de programación. Sin embargo, no pretende reemplazar los procesos completos de planificación de cambios netos o regenerativos.  

## <a name="to-calculate-the-planning-worksheet"></a>Para calcular la hoja de planificación
  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de planificación** y luego elija el enlace relacionado.  
2. Seleccione la acción **Calcular planificación regenerativa** para abrir la página **Calcular plan**.  
3. En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Calcular un programa maestro de producción. En la ejecución se tienen en cuenta los productos con pedidos de venta abiertos o previsiones de demanda. <br/>Si también existen otras demandas para dichos artículos, por ejemplo, stock de seguridad, punto de reorden o líneas de componentes de producción abiertas, estas demandas se incluyen en el cálculo de MPS para garantizar que el sistema de planificación aborde el perfil de inventario completo.  |  
    |**MRP**|Calcular planificación de requisitos de material. En esta ejecución se tienen en cuenta los productos con necesidades dependientes. Normalmente, MPS y MRP se ejecutan al mismo tiempo. Para ejecutar MPS y MRP al mismo tiempo, en la página **Configuración fabricación**, en la ficha desplegable **Planificación**, seleccione el campo **Cálculo agrupado MPS/MRP**.|  
    |**Fecha inicial**|Evaluar disponibilidad del inventario. Si la cantidad física de un producto está por debajo del punto de pedido, el programa crea un pedido de reposición en el futuro, a partir de esta fecha. Si un producto está por debajo del stock de seguridad (a la fecha inicial), el sistema programa un pedido de reposición para la fecha inicial de planificación.|  
    |**Fecha final**|La fecha final del horizonte de la planificación. Con posterioridad a esta fecha no se tienen en cuenta ni la demanda ni el aprovisionamiento. Si el ciclo de reaprovisionamiento de un producto va más allá de la fecha final, el horizonte de planificación efectivo equivale a fecha pedido más el ciclo reaprovisionamiento.<br/><br/> El horizonte de planificación se refiere a la duración del plan. Si el horizonte es demasiado breve, los productos con un plazo más largo no se piden a tiempo. Si es demasiado largo, se invierte demasiado tiempo en revisar y procesar la información y es probable que cambie antes de lo necesario. Puede definir un horizonte de planificación para la producción y otro más largo para las compras, pero no es obligatorio. Se debe definir un horizonte de planificación para compras y producción que cubra el plazo total de los componentes.|  
    |**Parar y mostrar primer error**|Seleccione esta opción si desea que se detenga la ejecución de la planificación tan pronto como encuentre un error. Se muestra un mensaje con información sobre el error. Si hay algún error, sólo se mostrarán en la hoja de planificación las líneas de planificación correctas realizadas antes de que se produjera el error. Si no selecciona este campo, el trabajo por lotes **Calcular plan** continuará hasta que se haya completado. Los errores no interrumpirán el trabajo por lotes. Si hay uno o más errores, se mostrará un mensaje al finalizar el proceso donde se informa el número de productos afectados. A continuación, se abrirá la página **Registro error planificación**, con más información sobre el error y vínculos a las fichas de los productos afectados.|  
    |**Previsión de uso**|Seleccione la previsión que se debe incluir como demanda cuando ejecute el trabajo por lotes de planificación. La previsión predeterminada se configura en la ficha desplegable **Planificación** de la página **Configuración fabricación**.|  
    |**No incluir en la previsión fechas anteriores al**|defina qué parte de la previsión seleccionada desea incluir en la planificación introduciendo una fecha anterior a la cual no se incluirá demanda de previsión alguna.|  
    |**Respetar parámetros de planificación para las advertencias de excepción**|Este campo se encuentra seleccionado de forma predeterminada.<br/><br/> El suministro de las líneas de planificación con advertencias no se modifica normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere solo un suministro para satisfacer la cantidad exacta de demanda. Sin embargo, puede definir ciertos parámetros de planificación para que se respeten las líneas de planificación con determinadas advertencias.<br/><br/>|  

4. En la ficha desplegable **Producto**, defina los filtros para ejecutar la planificación por producto, descripción de producto o almacén.  
5. Elija el botón **Aceptar**. El proceso se ejecuta y las líneas de planificación se agregan a la hoja de planificación.  

## <a name="to-perform-action-messages"></a>Para ejecutar los mensajes de acción
  
1. En la página **Hoja de planificación**, elija la acción **Ejecutar mensajes de acción**.  
2. En la ficha desplegable **Opciones**, especifique cómo crear suministros. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Orden producción**|Especifica cómo crear pedidos de producción. Puede hacerlo directamente desde las propuestas de líneas de planificación. Puede crear órdenes de producción planificadas o planificadas en firme.|  
    |**Pedido de ensamblado**|Especifique cómo crear órdenes de ensamblado. Puede hacerlo directamente desde las propuestas de líneas de planificación.|  
    |**Pedido compra**|Especifique cómo crear órdenes de compra. Puede hacerlo directamente desde las propuestas de líneas de planificación.<br/><br/> Si elige copiar las propuestas de la línea de planificación para los pedidos de compra en una hoja de demanda, seleccione la plantilla y el nombre de la hoja.|  
    |**Pedido de transferencia**|Especifique cómo crear órdenes de transferencia. Puede hacerlo directamente desde las propuestas de líneas de planificación.<br/><br/> Si elige copiar las propuestas de la línea de planificación de los pedidos de transferencia en una hoja de demanda, seleccione la plantilla y el nombre de la hoja.|  
    |**Combinar pedidos de transferencia**|Seleccione si agrupar pedidos de transferencia.|  
    |**Parar y mostrar primer error**|Seleccione esta opción si desea que el proceso de trabajo por lotes **Ejecutar mensajes acción. Plan -.** se detenga al encontrar un error. Se muestra un mensaje con información sobre el error. Si hay errores, solo generarán pedidos de suministro las líneas de planificación procesadas antes de producirse el error.|  

3. En la ficha desplegable **Línea planif.**, puede definir filtros para limitar la ejecución de mensajes de acción.  
4. Elija el botón **Aceptar**.  

El proceso elimina las líneas de la hoja de planificación una vez que ha llevado a cabo el mensaje de acción. Las demás líneas permanecen en la hoja de planificación hasta que se aceptan posteriormente, o se eliminan. Las líneas se pueden eliminar manualmente.  

## <a name="action-messages"></a>Mensajes de acción
  
Los mensajes de acción son emitidos por el sistema de seguimiento de pedidos cuando, con los pedidos existentes, no se logra un equilibrio. Estos mensajes pueden verse como sugerencias para que realice los cambios necesarios para volver a llegar a un equilibrio entre aprovisionamiento y demanda.  

La generación de mensajes de acción tiene lugar en un nivel por vez, por código de nivel inferior de cada producto. Así se garantiza que se consideren todos los productos que tengan o vayan a tener cambios de aprovisionamiento o demanda.  

Para evitar mensajes de acción innecesarios o poco importantes, puede establecer amortiguadores, que sirven para restringirlos exclusivamente a cambios que exceden la cantidad o el número de días definido.  

Después de revisar los mensajes de acción y determinar si acepta todos los cambios sugeridos o sólo algunos, seleccione el campo **Aceptar mensaje acción**. A continuación, actualice los horarios en consecuencia.  

> [!NOTE]  
> Un mensaje de acción es una sugerencia para crear o cancelar un pedido, o para cambiar la cantidad o la fecha de un pedido. Puede tratarse de un pedido de compra o de transferencia, o de una orden de producción.  

Como respuesta a los desequilibrios entre aprovisionamiento y demanda, se generan los mensajes de acción siguientes.  

|Mensaje de acción|Descripción|  
|--------------------|---------------------------------------|  
|**Nuevo**|Si una demanda no se puede satisfacer con lo que sugieren los mensajes de acción en cuanto a **Cambiar cdad.**, **Reprogramar** o **Reprog. y cambiar cdad.** de los pedidos existentes, se genera el mensaje **Nuevo**, que sugiere crear otro pedido. El mensaje **Nuevo** también se genera si no hay pedidos de suministro en el ciclo de reaprovisionamiento del producto en cuestión. Esta opción determina el número de periodos hacia adelante y hacia atrás del perfil de disponibilidad cuando busca un pedido para reprogramarlo.|  
|**Cambiar cantidad**|Cuando la cantidad cambia para una demanda ligada a un pedido de suministro, se genera un mensaje de acción **Cambiar cdad.**, El mensaje indica que se debe cambiar el abastecimiento correspondiente en función del cambio en la demanda. Si se produce una nueva demanda, [!INCLUDE[prod_short](includes/prod_short.md)] busca el pedido de suministro sin reservar más próximo en el ciclo de reaprovisionamiento, y emite un mensaje de cambio.|  
|**Reprogramar**|Si en un pedido de demanda o abastecimiento, cambia la fecha y ello crea un desequilibrio en la red de pedidos, se emite un mensaje de acción **Volver a programar**. Si la relación entre abastecimiento y demanda es de uno a uno, se emite un mensaje de acción que sugiere modificar el pedido de suministro en tal sentido. Si el pedido de abastecimiento cubre la demanda de más de un pedido de venta, se reprograma el pedido de abastecimiento, con la misma fecha que la primera demanda.|  
|**Reprogramar y cambiar cantidad**|Si se han modificado las fechas y las cantidades de un pedido, debe cambiar las fechas y las cantidades de los planes. Los mensajes de acción recogen las dos acciones en un mensaje, **Reprog. y cambiar cdad.**, para garantizar que la red de pedidos vuelva a quedar equilibrada.|  
|**Cancelar**|Si se elimina una demanda que se ha cubierto pedido a pedido, se emite un mensaje de acción para cancelar el pedido de suministro relacionado. Si la relación no es pedido a pedido, se genera un mensaje de acción para cambiar y reducir el abastecimiento. Si, por otros factores, como ajustes de inventario, no se requiere un pedido de suministro en el momento en que genera los mensajes de acción, [!INCLUDE[prod_short](includes/prod_short.md)] sugiere el mensaje **Cancelar** en la hoja.|  

## <a name="see-also"></a>Consulte también

[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
