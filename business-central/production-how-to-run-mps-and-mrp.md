---
title: Cómo ejecutar la planificación completa, MPS y MRP | Documentos de Microsoft
description: Los términos "ejecutar la hoja de planificación" o "ejecutar MRP" hacen referencia al cálculo del programa de producción principal y a las necesidades de material, en función de la demanda real y prevista. El programa de planificación puede calcular tanto el Programa de planificación principal (MPS) como la Planificación de necesidades de material (MRP) cuando se solicite, o calcular ambas cosas a la vez.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: bf64955898ddbdce539a2e68c2db07c2c6b8c575
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "934657"
---
# <a name="run-full-planning-mps-or-mrp"></a>Ejecutar la planificación completa, MPS o MRP
Los términos "ejecutar la hoja de planificación" o "ejecutar MRP" hacen referencia al cálculo del programa de producción principal y a las necesidades de material, en función de la demanda real y prevista. El programa de planificación puede calcular tanto el Programa de planificación principal (MPS) como la Planificación de necesidades de material (MRP) cuando se solicite, o calcular ambas cosas a la vez.  

-   MPS se refiere al cálculo de un programa de producción principal basado en la demanda real y en la previsión de demanda. El cálculo de MPS se utiliza para productos finales que tengan una previsión o una línea de pedido de venta. Estos productos se denominan "productos de MPS" y se identifican dinámicamente al iniciarse el cálculo.  
-   MRP se refiere al cálculo de las necesidades de material basado en la demanda real de componentes y en la previsión de demanda de componentes. Sólo se calcula para los productos que no son productos de MPS. La finalidad de MRP es ofrecer planes formales con fases temporales, por producto, para suministrar el producto adecuado, en el momento correcto, en el lugar convenido y en la cantidad justa.  

Los algoritmos de planificación usados tanto para MPS como para MRP son idénticos. Los algoritmos de planificación relativos a saldos netos reutilizan órdenes de reposición existentes y mensajes de acción. El proceso del sistema de planificación examina lo que se necesita o se va a necesitar (la demanda) y lo que hay físicamente o se espera que haya (el suministro). Cuando estas cantidades se comparan, [!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona mensajes de acción. Los mensajes de acción son sugerencias para crear un pedido nuevo, para cambiar un pedido (la cantidad o la fecha) o para cancelar un pedido ya solicitado. El término "pedido" incluye pedidos de compra, pedido de ensamblado, pedidos de producción y pedidos de transferencia.

Los vínculos creados por el motor de planificación entre la demanda y el abastecimiento correspondiente se puede seguir en la página **Seguimiento pedido**. Para obtener más información, vea [Seguimiento de relaciones entre demanda y suministro](production-how-track-demand-supply.md).   

Para obtener buenos resultados en la planificación, se deben haber configurado correctamente las siguientes opciones: fichas de producto, L.M. de ensamblado. L.M. de producción y rutas.  

## <a name="methods-for-generating-a-plan"></a>Métodos para generar un plan  

-   **Calc. planif. regenerativa**: esta función procesa o vuelve a generar el plan de materiales. El proceso comienza con la eliminación de todos los pedidos de aprovisionamiento cargados actualmente. Se vuelven a planificar todos los productos de la base de datos.  
-   **Calc. plan. cambio periodo**: esta función procesa un plan de cambio neto. Los productos se tienen en cuenta en una planificación de cambio neto de dos tipos de cambios:  
    - **Cambios de demanda y suministro:** son las modificaciones de las cantidades en los pedidos de venta, las previsiones de demanda, los pedidos de ensamblado, las órdenes de producción o los pedidos de compra. También se considera como cambio de cantidad un cambio en el nivel de existencias no planificado.  
    - **Cambios de parámetros de planificación:** son cambios en el stock de seguridad, el punto de pedido, la ruta, la lista de materiales, y cambios en el cálculo de ciclo o plazo de entrega.  
-   **Traer mensajes acción:** esta función sirve como herramienta de planificación a corto plazo, ya que emite mensajes de acción para alertar al usuario sobre las modificaciones realizadas desde la última vez que se calculó el plan regenerativo o de cambio neto.  

Con cada método previsto, [!INCLUDE[d365fin](includes/d365fin_md.md)] genera las entradas en la hoja de trabajo asumiendo que la capacidad es infinita. El centro de trabajo y de maquinaria no se tiene en cuenta cuando se desarrollan esquemas.  

> [!IMPORTANT]  
>  La función Calc. planif. regenerativa es el proceso más común. Sin embargo, las funciones Calcular plan y Ejecutar mensajes acción se pueden usar para ejecutar el proceso Calc. plan. saldo periodo.  
>   
>  La función Traer mensajes de acción se puede ejecutar entre planes de cambio neto y regenerativos para obtener una vista inmediata del efecto de los cambios en el programa, pero no se debe usar como sustituto de los procesos de los dos planes completos.  

## <a name="to-calculate-the-planning-worksheet"></a>Para calcular la hoja de planificación  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hojas planificación** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Calcular planificación regenerativa** para abrir la página **Calcular plan**.  
3.  En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Seleccione para iniciar el cálculo de un programa de producción maestro. En la ejecución se tienen en cuenta los productos con pedidos de venta abiertos o previsiones de demanda.|  
    |**MRP**|Seleccione para iniciar el cálculo de la planificación de requisitos de material. En esta ejecución se tienen en cuenta los productos con necesidades dependientes. Normalmente, MPS y MRP se ejecutan al mismo tiempo. Para ejecutar MPS y MRP al mismo tiempo, el campo de **Cálculo agrupado MPS/MRP** debe estar seleccionado en la ficha desplegable **Planificación** en la página **Configuración fabricación**.|  
    |**Fecha inicial**|Esta fecha se utiliza para evaluar la disponibilidad de existencias. Si la cantidad física de un producto está por debajo del punto de pedido, el programa crea un pedido de reposición en el futuro, a partir de esta fecha. Si un producto está por debajo del stock de seguridad (a la fecha inicial), el sistema programa un pedido de reposición para la fecha inicial de planificación.|  
    |**Fecha final**|Es la fecha final del horizonte de la planificación. Con posterioridad a esta fecha no se tienen en cuenta ni la demanda ni el aprovisionamiento. Si el ciclo de reaprovisionamiento de un producto va más allá de la fecha final, el horizonte de planificación efectivo equivale a fecha pedido + ciclo reaprovisionamiento.<br /><br /> El horizonte de planificación se refiere a la duración del plan. Si el horizonte es demasiado breve, los productos con un plazo más largo no se piden a tiempo. Si es demasiado largo, se invierte demasiado tiempo en revisar y procesar la información y es probable que cambie antes de lo necesario. Se puede definir un horizonte de planificación para la producción y otro más largo para las compras, pero no es obligatorio. Se debe definir un horizonte de planificación para compras y producción que cubra el plazo acumulado de los componentes.|  
    |**Parar y mostrar primer error**|Seleccione si desea que se detenga la ejecución de la planificación tan pronto como encuentre un error. Además, se mostrará un mensaje con información sobre el primer error. Si hay algún error, sólo se mostrarán en la hoja de planificación las líneas de planificación correctas realizadas antes de que se produjera el error. Si no selecciona este campo, el trabajo por lotes **Calcular plan** continuará hasta finalizar, es decir, los errores no lo detendrán. Si hay uno o más errores, se mostrará un mensaje al finalizar el proceso donde se informa el número de productos afectados. A continuación, se abrirá la página **Registro error planificación**, con más información sobre el error y vínculos a las fichas de los productos afectados.|  
    |**Usar previsión**|Seleccione la previsión que se debe incluir como demanda cuando ejecute el trabajo por lotes de planificación. La previsión predeterminada se configura en la ficha desplegable **Planificación** de la página **Configuración fabricación**.|  
    |**No incluir en la previsión fechas anteriores al**|Defina qué cantidad de la previsión seleccionada se debe incluir en la ejecución de la planificación; para ello, introduzca una fecha antes de la cual no se incluye la demanda prevista, con lo que se excluye la información obsoleta.|  
    |**Respetar parámetros de planificación para las advertencias de excepción**|Este campo se encuentra seleccionado de forma predeterminada.<br /><br /> El suministro de las líneas de planificación con advertencias no se modifica normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere solo un suministro para satisfacer la cantidad exacta de demanda. Sin embargo, puede definir ciertos parámetros de planificación para que se respeten las líneas de planificación con determinadas advertencias.<br /><br />|  

4.  En la ficha desplegable **Producto**, defina los filtros para ejecutar la planificación por producto, descripción de producto o almacén.  
5.  Elija el botón **Aceptar**. El proceso se ejecuta y, a continuación, la hoja de planificación se rellena con las líneas de planificación.  

## <a name="to-perform-action-messages"></a>Para ejecutar los mensajes de acción  
1.  En la página **Hoja de planificación**, elija la acción **Ejecutar mensajes de acción**.  
2.  En la ficha desplegable **Opciones**, especifique cómo crear suministros. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Orden producción**|Especifique cómo desea crear órdenes de producción. Puede hacerlo directamente desde las propuestas de líneas de planificación. Puede crear órdenes de producción planificadas o planificadas en firme.|  
    |**Pedido de ensamblado**|Especifique cómo desea crear órdenes de ensamblado. Puede hacerlo directamente desde las propuestas de líneas de planificación.|  
    |**Pedido compra**|Especifique cómo desea crear órdenes de compra. Puede hacerlo directamente desde las propuestas de líneas de planificación.<br /><br /> Si elige copiar las propuestas de la línea de planificación para los pedidos de compra en una hoja de demanda, seleccione la plantilla y el nombre de la hoja.|  
    |**Ped. transfer.**|Especifique cómo desea crear órdenes de transferencia. Puede hacerlo directamente desde las propuestas de líneas de planificación.<br /><br /> Si elige copiar las propuestas de la línea de planificación de los pedidos de transferencia en una hoja de demanda, seleccione la plantilla y el nombre de la hoja.|  
    |**Combinar pedidos de transferencia**|Seleccione si desea agrupar pedidos de transferencia.|  
    |**Parar y mostrar primer error**|Seleccione si desea que el proceso de trabajo por lotes **Ejecutar mensajes acción. Plan -.** se detenga al encontrar un error. Además, se mostrará un mensaje con información sobre el primer error. Si hay errores, solo generarán pedidos de suministro las líneas de planificación procesadas antes de producirse el error.|  

3.  En la ficha desplegable **Línea planif.**, puede definir filtros para limitar la ejecución de mensajes de acción.  
4.  Elija el botón **Aceptar**.  

El proceso elimina las líneas de la hoja de planificación una vez que ha llevado a cabo el mensaje de acción. Las demás líneas permanecen en la hoja de planificación hasta que se aceptan posteriormente, o se eliminan. Las líneas se pueden eliminar manualmente.  

## <a name="action-messages"></a>Mensajes de acción  
Los mensajes de acción son emitidos por el sistema de seguimiento de pedidos cuando, con los pedidos existentes, no se logra un equilibrio. Se trata de sugerencias para que realice los cambios necesarios para volver a llegar a un equilibrio entre aprovisionamiento y demanda.  

La generación de mensajes de acción tiene lugar en un nivel por vez, por código de nivel inferior de cada producto. Así se garantiza que se consideren todos los productos que tengan o vayan a tener cambios de aprovisionamiento o demanda.  

Para evitar mensajes de acción superfluos o poco importantes, el usuario puede establecer amortiguadores, que sirven para restringirlos exclusivamente a cambios que exceden la cantidad o el número de días definido.  

Después de revisar los mensajes de acción y determinar si acepta todos los cambios sugeridos o sólo algunos, seleccione el campo **Aceptar mensaje acción**, y estará listo para actualizar los programas.  

> [!NOTE]  
>  Un mensaje de acción es una sugerencia para crear o cancelar un pedido, o para cambiar la cantidad o la fecha de un pedido. Puede tratarse de un pedido de compra o de transferencia, o de una orden de producción.  

Como respuesta a los desequilibrios entre aprovisionamiento y demanda, se generan los mensajes de acción siguientes.  

|Mensaje acción|Descripción|  
|--------------------|---------------------------------------|  
|**Nuevo**|Si una demanda no se puede satisfacer con lo que sugieren los mensajes de acción en cuanto a **Cambiar cdad.**, **Reprogramar** o **Reprog. y cambiar cdad.** de los pedidos existentes, se genera el mensaje **Nuevo**, que sugiere crear otro pedido. Además, se emite el mensaje **Nuevo** si no hay pedidos de suministro en el ciclo de reaprovisionamiento del producto en cuestión. Este parámetro determina el número de periodos hacia adelante y hacia atrás del perfil de disponibilidad cuando busca un pedido para reprogramarlo.|  
|**Cambiar cantidad**|Cuando cambia la cantidad de la demanda ligada a un pedido de suministro, se genera un mensaje de acción **Cambiar cdad.**, que indica que se debe cambiar el abastecimiento correspondiente en función del cambio en la demanda. Si se produce una nueva demanda, [!INCLUDE[d365fin](includes/d365fin_md.md)] busca el pedido de suministro sin reservar más próximo en el ciclo de reaprovisionamiento, y emite un mensaje de cambio.|  
|**Reprogramar**|Si en un pedido de demanda o abastecimiento, cambia la fecha y ello crea un desequilibrio en la red de pedidos, se emite un mensaje de acción **Volver a programar**. Si la relación entre abastecimiento y demanda es de uno a uno, se emite un mensaje de acción que sugiere modificar el pedido de suministro en tal sentido. Si el pedido de abastecimiento cubre la demanda de más de un pedido de venta, se reprograma el pedido de abastecimiento, con la misma fecha que la primera demanda.|  
|**Reprogramar y cambiar cantidad**|Si se han modificado las fechas y las cantidades de un pedido, debe cambiar las fechas y las cantidades de los planes. Los mensajes de acción recogen las dos acciones en un mensaje, **Reprog. y cambiar cdad.**, para garantizar que la red de pedidos vuelva a quedar equilibrada.|  
|**Cancelar**|Si se elimina una demanda que se ha cubierto pedido a pedido, se emite un mensaje de acción para cancelar el pedido de suministro relacionado. Si la relación no es pedido a pedido, se genera un mensaje de acción para cambiar y reducir el abastecimiento. Si, por otros factores, como ajustes de inventario, no se requiere un pedido de suministro en el momento en que el usuario genera los mensajes de acción, [!INCLUDE[d365fin](includes/d365fin_md.md)] sugiere el mensaje **Cancelar** en la hoja.|  

## <a name="see-also"></a>Consulte también  
[Planificación](production-planning.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
