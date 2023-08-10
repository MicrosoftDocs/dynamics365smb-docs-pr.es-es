---
title: 'Tutorial: planificación automática de suministros'
description: 'En este tutorial, se demuestra el modo de utilizar el sistema de planificación del suministro para planificar automáticamente los pedidos de compra y órdenes de producción en diferentes pedidos de venta.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-planning-supplies-automatically"></a>Tutorial: planificación automática de suministros

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Las frases "ejecutar planificación" y "ejecutar MRP" hacen referencia al cálculo del programa maestro de producción (MPS) y del plan de necesidades de material (MRP) basándose en la demanda real y prevista.  

-   MPS se refiere al cálculo de un programa de producción principal basado en la demanda real y en la previsión de demanda. El cálculo de MPS se utiliza para productos finales que tengan una previsión o una línea de pedido de venta. Estos productos se denominan "productos de MPS" y se identifican dinámicamente al iniciarse el cálculo.  
-   MRP se refiere al cálculo de las necesidades de material basado en la demanda real de componentes y en la previsión de demanda de componentes. Sólo se calcula para los productos que no son productos de MPS. La finalidad global de MRP es la de proporcionar planes con fases temporales, por producto, para suministrar el producto correcto en el momento correcto, en el lugar correcto y en la cantidad correcta.  

 Los algoritmos de planificación usados tanto para MPS como para MRP son idénticos. Los algoritmos de planificación utilizan saldos netos, reutilizan pedidos de suministro existentes y mensajes de acción. El proceso del sistema de planificación examina lo que se necesita o se va a necesitar (la demanda) y lo que hay disponible o se espera que haya (el suministro). Cuando estas cantidades se comparan, se muestran mensajes de acción en la hoja de planificación. Los mensajes de acción son sugerencias para crear un nuevo pedido de suministro, cambiar un pedido de suministro (la cantidad o la fecha) o cancelar un pedido de suministro existente. Los pedidos de suministro pueden ser órdenes de producción, pedidos de compra y pedidos de transferencia. Para obtener información detallada, consulte [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md).  

 El resultado de planificación se calcula en parte con los conjuntos demanda-suministro de la base de datos y en parte con la configuración de fichas ud. almacenamiento o fichas producto, L.M. producción y rutas.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial
 En este tutorial, se demuestra el modo de utilizar el sistema de planificación del suministro para planificar automáticamente todos los pedidos de compra y órdenes de producción necesarias para producir 15 bicicletas de ruta demandadas en diferentes pedidos de venta. Para ofrecer un tutorial claro y realista, se ha delimitado el número de líneas de planificación eliminando todos los demás conjuntos de demanda-suministro en la empresa de demostración CRONUS, salvo la demanda de ventas en el almacén EAST.  

 En este tutorial se ilustran las siguientes tareas:  

-   Creación del pedido de venta y cálculo de un plan de suministro completo.  
-   Visualización de los parámetros de planificación y los movimientos de seguimiento de pedidos detrás de las líneas de planificación.  
-   Creación automática de los pedidos de suministros sugeridos.  
-   Creación de nueva demanda de ventas y replanificar consiguientemente.  

## <a name="roles"></a>Funciones

-   Planificador de producción  
-   Agente de compras  

## <a name="prerequisites"></a>Requisitos previos
 Para completar este tutorial, necesitará:  

-   La empresa de demostración CRONUS España S.A.  
-   Cambiar varios valores de configuración del producto como se indica en los pasos de la sección "Preparación de datos de ejemplo", más adelante en este tutorial.  

## <a name="story"></a>Historia
 El cliente, Cannon Group PLC, hace un pedido de cinco bicicletas de ruta para su entrega el 05-02-2021 (5 de febrero).  

 Eduardo, el planificador de producción, realiza la planificación de suministros de rutina para la primera semana de febrero de 2021. Eduardo realiza el filtrado en su propio almacén, ESTE, y especifica el intervalo de planificación de la fecha de trabajo 23-01-2021 a 07-02-2021 antes de calcular un plan de suministro inicial.  

 La única demanda de dicha semana es para el pedido de venta de GDE Distribución S.A.. Eduardo ve que ninguna de las líneas de planificación tiene advertencias y crea pedidos de suministro sin cambios para las líneas de planificación sugeridas.  

 Al día siguiente, antes de que se inicie o registre ninguno de los pedidos de suministro iniciales, notifican a Eduardo que otro cliente ha realizado un pedido de diez bicicletas de ruta para su envío el 12-02-2021. Eduardo vuelve a calcular para ajustar el plan de suministro según el cambio de la demanda. El nuevo cálculo arroja un plan de saldo periodo que sugiere cambios tanto en el tiempo como en la cantidad de algunos de los pedidos de suministro creados la primera vez.  

 Durante los diversos pasos de planificación, Eduardo consulta los pedidos implicados y utiliza la función Seguimiento pedido para ver qué demanda es cubierta con qué suministro.  

## <a name="preparing-sample-data"></a>Preparación de datos de ejemplo
 Cree ud. almacenamiento (UA) para la bicicleta de ruta y una selección de todos sus componentes, números de producto 1001 a 1300. (Algunos componentes se excluyen para simplificar los procedimientos.) Ajuste los parámetros de planificación de los componentes seleccionados para proporcionar un resultado de planificación más transparente.  

### <a name="to-create-stockkeeping-units"></a>Para crear unidades de almacenamiento

1.  Abra la ficha de producto correspondiente a 1001, bicicleta de ruta.  
2.  Seleccione la acción **Crear unidad de almacenamiento**.  
3.  En la página **Crear ud. de almacenam.**, deje todas las opciones y filtros sin cambiar y, a continuación, haga clic en **Aceptar**.  
4.  Repita los pasos 1 a 3 para todos los productos en el intervalo numérico entre 1100 y 1300.  

### <a name="to-change-selected-planning-parameters"></a>Para cambiar los parámetros de planificación seleccionados

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de almacenamiento**, y luego elija el enlace relacionado.  
2.  Abra la ficha de unidad de almacenamiento EAST para el producto 1100, rueda delantera.  
3.  En la ficha desplegable **Planificación**, rellene los campos tal como se describe en la tabla siguiente.  

    |Directiva reaprov.|Stock de seguridad|Periodo de acumulación de lotes|Periodo de reprogramación|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lote a lote|En blanco|2S|2S|  

4.  Repita los pasos 2 y 3 para todas las UA en el intervalo numérico entre 1100 y 1300.  

 De este modo finaliza la preparación de datos de ejemplo para el tutorial.  

## <a name="creating-a-regenerative-supply-plan"></a>Creación de un plan de suministro regenerativo
 En reacción a un nuevo pedido de venta de cinco bicicletas de ruta, Ricardo comienza el proceso de planificación configurando las opciones, los filtros y el intervalo de planificación para excluir el resto de la demanda, salvo la de la primera semana de febrero en el almacén EAST. Ricardo comienza por calcular un programa maestro de producción (MPS) y luego calcula un plan de suministro completo para toda la demanda de nivel inferior (MRP).  

### <a name="to-create-the-sales-order"></a>Para crear el pedido de venta

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En la página **Pedido de venta**, rellene los campos tal como se describe en la tabla siguiente.  

    |Nombre cliente de venta|Fecha envío|Nº producto|Ubicación|Cantidad|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Cannon Group|05-02-2014|1001|EAST|5|  

4.  Acepte el aviso de disponibilidad y elija el botón **Sí** para registrar la cantidad de demanda nueva.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>Crear un plan regenerativo para satisfacer la demanda en el almacén EAST.

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja planificación** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Calcular planificación regenerativa**.  
3.  En la página **Calcular plan - Hoja planif.** rellene los campos tal como se describe en la tabla siguiente.  

    |Calcular plan|Fecha inicial|Fecha final|Mostrar resultados:|Totales límite para|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Sí<br /><br /> **MRP** = No|01-23-2021<br /><br /> (fecha de trabajo)|02-07-2021|1001..1300|Filtro almacén = EAST|  

4.  Elija el botón **Aceptar** para comenzar la ejecución de la planificación.  

     Se crea una línea de planificación que sugiere que se emita una orden de producción planificada para producir las diez bicicletas de ruta, producto 1001, para el 05-02-2021, la fecha de envío del pedido de venta.  

     A continuación, compruebe que esta línea de planificación está relacionada con el pedido de venta de GDE Distribución con la función **Seguimiento pedido**, que vincula dinámicamente la demanda con el suministro planificado.  

5.  Seleccione la nueva línea de planificación y haga clic en **Seguimiento pedido**.  
6.  En la página **Seguimiento de pedido**, elija la acción **Mostrar**.  

     Se muestra el pedido de venta de las cinco bicicletas de ruta que se envía al cliente número 10000 el 05-02-2021.  

7.  Cierre las páginas **Pedido venta** y **Seguimiento pedido**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Para calcular MRP para incluir las necesidades subyacentes del componente

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja planificación** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Calcular planificación regenerativa**.  
3.  En la página **Calcular plan - Hoja planif.** rellene los campos tal como se describe en la tabla siguiente.  

    |Calcular|Fecha inicial|Fecha final|Mostrar resultados:|Totales límite para:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Sí<br /><br /> **MRP** = Sí|01-23-2021|02-07-2021|1001..1300|Filtro almacén = EAST|  

4.  Elija el botón **Aceptar** para comenzar la ejecución de la planificación.  

     Se crea un total de 14 líneas de planificación que sugieren pedidos de suministro para toda la demanda que representa el pedido de venta de bicicletas de ruta del almacén EAST.  

## <a name="analyzing-the-planning-result"></a>Análisis del resultado de planificación
 Para estudiar las cantidades sugeridas, Eduardo analiza según líneas de planificación seleccionadas para ver movimientos de seguimiento y parámetros de planificación de pedido.  

 En la página **Hoja de planificación**, observe en la columna **Fecha vencimiento** que los pedidos de suministro sugeridos se programan hacia atrás desde la fecha de vencimiento del pedido de venta, 05-02-2021. La escala de tiempo empieza en la línea de planificación superior con la orden de producción para producir las bicicletas de ruta terminadas. La escala de tiempo finaliza en la línea de planificación inferior con el pedido de compra de productos de nivel inferior, 1255, Arandela trasera, que vence el 01-30-2021. Como la línea de planificación para el producto 1251, eje de rueda posterior, esta línea representa un pedido de compra para los componentes que vencen en la fecha inicial de su producto principal fabricado, el producto de subensamblado 1250 que, a su vez, vence el 03-02-2014. En toda la hoja de cálculo, puede ver que todos los productos subyacentes vencen en la fecha inicial de sus productos principales.  

 La línea de planificación para el producto 1300, Mtje. cadena, sugiere diez piezas. Esto se desvía de las cinco piezas que esperamos que necesite para cubrir el pedido de venta. Empiece a visualizar los movimientos de seguimiento del pedido.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Ver los movimientos de seguimiento del pedido para el producto 1300

1.  Seleccione la línea de planificación del producto 1300 y seleccione la acción **Seguimiento de pedido**.  

     Las dos líneas de la página **Seguimiento pedido** muestran que se hace un seguimiento de cinco piezas desde la línea de planificación (primera línea de seguimiento de pedido) al pedido de venta 1001 (segunda línea de seguimiento de pedido). Las cinco últimas piezas sugeridas en la línea de planificación no están relacionadas con ninguna línea documentada, sino con un parámetro de planificación, movimiento de previsión o movimiento de pedido abierto. Estas cantidades no seguidas se suman en el campo **Cantidad no seguida** en la cabecera de la página **Seguimiento pedido**.  

2.  Elija el campo **Cantidad no seguida**.  

     La página **Elementos planificación sin seguimiento** muestra que el producto 1300 utiliza un parámetro de planificación, Cantidad mínima pedido, de 10,00. Por lo tanto, la línea de planificación es para diez piezas en total, de las cuales se puede realizar un seguimiento de cinco a una demanda. Las cinco últimas piezas son una cantidad no seguida para satisfacer el parámetro de planificación. Empiece a revisar el parámetro de la planificación.  

### <a name="to-check-the-planning-parameter"></a>Para comprobar el parámetro de planificación

1.  En la página **Elementos planificación sin seguimiento**, seleccione la línea de seguimiento de pedido para el producto 1300.  
2.  Elija el campo **Nº de producto** y, a continuación, elija la acción **Avanzado**.  
3.  En la página **Lista de producto**, seleccione la acción **Unidades de almacenamiento**.  
4.  En la página **Lista ud. de almacenam.**, abra la ficha de la unidad de almacenamiento EAST.  
5.  En la ficha desplegable **Planificación**, tenga en cuenta que el campo **Cantidad mínima pedido** contiene 10.  
6.  Cierre todas las páginas salvo **Hoja planificación**.  

### <a name="to-view-more-order-tracking-entries"></a>Para ver más movimientos de seguimiento de pedidos

1.  Seleccione la línea de planificación del producto 1110, Llanta y seleccione la acción **Seguimiento de pedido**.  

     La página **Seguimiento pedido** muestra que se necesitan cinco llantas para cada orden de producción para las ruedas frontales y traseras, respectivamente.  

     Mismo seguimiento de pedidos se aplica a las líneas de planificación de los productos 1120, 1160, y 1170. Para el producto 1120, el campo **Cantidad por** en la L.M. de producción de cada producto de la rueda es 50 UDS, que dan como resultado una necesidad total de 100.  

     La línea de planificación para el producto 1150 para seis piezas tiene un aspecto irregular. Empiece a analizar.  

2.  Seleccione la línea de planificación del producto 1150, Llanta y seleccione la acción **Seguimiento de pedido**.  

     La página **Seguimiento pedido** muestra que se hace el seguimiento de cinco unidades para la rueda delantera y que no se hace el seguimiento de una unidad. Empiece a visualizar la cantidad sin seguimiento.  

3.  Elija el campo **Cantidad no seguida**.  

     La página **Elementos planificación sin seguimiento** muestra que el producto 1150 utiliza un parámetro de planificación, Múltiplos de pedido, de 2,00, que especifica que cuando se solicita el producto, debe ser en una cantidad múltiplo de 2. El número más próximo a 5 divisible por 2 es 6.  

     El mismo seguimiento de pedido se aplica a las líneas de planificación de los componentes de concentrador anterior, los productos 1151 y 1155, excepto que cada necesidad se multiplica por el orcentaje de rechazo el definido para el producto 1150 en el campo **Porcentaje de rechazo** de la ficha de producto.  

 De este modo finaliza el análisis del plan de suministro inicial. Observe que la casilla **Aceptar mensaje acción** está seleccionada en todas las líneas de planificación, lo que indica que están listas para convertirse en pedidos de suministro.  

## <a name="carrying-out-action-messages"></a>Realización de mensajes de acción
 A continuación, Eduardo convierte las líneas de planificación sugeridas en pedidos de suministro con la función **Ejecutar mensajes acción**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Para crear automáticamente los pedidos de suministros sugeridos

1.  Seleccione la casilla **Aceptar mensaje acción** en todas las líneas de planificación con una advertencia de tipo Excepción.  
2.  Seleccione la acción **Ejecutar mensajes de acción**.  
3.  En la página **Ejecutar mensajes acción-Plan.**, rellene los campos descritos en la tabla siguiente.  

    |Orden producción|Pedido compra|Ped. transfer.|  
    |----------------------|--------------------|--------------------|  
    |Planif. en firme|Crear ped. compra|Crear ped. transf.|  

4.  Elija el botón **Aceptar** para crear automáticamente todos los pedidos de suministro sugeridos.  
5.  Cierre la página **Hoja planificación** vacía.  

 De este modo finaliza el cálculo inicial, análisis y creación de un plan de suministro para la demanda en el almacén EAST para la primera semana de febrero. En la siguiente sección, otro cliente realiza un pedido de diez bicicletas de ruta, por lo que Eduardo deberá replanificar.  

## <a name="creating-a-net-change-plan"></a>Creación de un plan de saldo periodo
 Al día siguiente, antes de que se inicie o registre ninguno de los pedidos de suministro iniciales, llega un nuevo pedido de venta de Libros S.A. de diez bicicletas de ruta para enviarse el 12-02-2021. A Eduardo le notifican la nueva demanda y pasa a replanificar para ajustar el plan de suministro actual. Eduardo utiliza la función Planif. saldo periodo para calcular únicamente los cambios que se realizan a la demanda o al suministro desde la última ejecución de la planificación. Además, Eduardo expande el periodo de planificación al 14-02-2021, para incluir la nueva demanda de venta el 12-02-2014.  

 El sistema de planificación calcula el mejor modo de cubrir la demanda para estos dos productos idénticos, como consolidar algunos pedidos de compra y órdenes de producción, reprogramar otros pedidos y crear nuevos pedidos donde se requiera.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Para crear la demanda de ventas nueva y replanificar

1.  Seleccione la acción **Nuevo**.  
2.  En la página **Pedido de venta**, rellene los campos tal como se describe en la tabla siguiente.  

    |Nombre cliente de venta|Fecha envío|Nº producto|Ubicación|Cantidad|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A.|02-12-2021|1001|EAST|10|  

3.  Acepte el aviso de disponibilidad y elija el botón **Sí** para registrar la cantidad de demanda.  
4.  Replanifique para ajustar el plan de suministro actual.  
5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja planificación** y luego elija el enlace relacionado.  
6.  Seleccione la acción **Calcular planificación de saldo neto**.  
7.  En la página **Calcular plan - Hoja planif.** rellene los campos tal como se describe en la tabla siguiente.  

    |Calcular plan|Fecha inicial|Fecha final|Mostrar resultados:|Totales límite para|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Sí<br /><br /> **MRP** = Sí|01-23-2021|02-14-2021|1001..1300|Filtro almacén = EAST|  

8.  Elija el botón **Aceptar** para comenzar la ejecución de la planificación.  

 Se crea un total de 14 líneas de planificación. Observe en la primera línea de planificación que el campo **Mensaje acción** indica **Nuevo**, el campo **Cantidad** muestra 10 y el campo **Fecha vencimiento** señala 12-02-21. Esta nueva línea para el producto principal superior, 1001, Bicicleta ruta, se crea debido a que el producto utiliza la política de reaprovisionamiento de **Pedido**, que indica que debe suministrarse en una relación de uno a uno a la demanda, el pedido de venta de diez piezas.  

 Las dos siguientes líneas de planificación son las órdenes de producción de las ruedas para bicicletas de ruta. Cada pedido existente de cinco, en el campo **Cantidad original**, aumenta hasta 15, en el campo **Cantidad**. Ambas órdenes de producción tienen fechas de vencimiento sin cambiar, como se indica en el campo **Mensaje de acción** que contiene **Cambiar cdad**. Esto ocurre también para la línea de planificación para el producto 1300, excepto su múltiplo de pedido de 10,00 redondea la demanda seguida de 15 piezas hasta 20.  

 Todas las demás líneas de planificación contienen un mensaje de acción **Reprog. y camb. cdad.** Esto indica que, además de aumentarse en cantidad, se trasladan las fechas de vencimiento en relación con el plan de suministro para incluir la cantidad adicional en el tiempo de producción disponible (capacidad). Los componentes comprados se vuelven a programar y se aumentan para suministrar las órdenes de producción. Empiece a analizar el nuevo plan.  

## <a name="analyzing-the-changed-planning-result"></a>Análisis del resultado de planificación modificado
 Dado que todos los productos planificados de lote a lote en el filtro, 1100 a 1300, tienen un periodo de reprogramación de dos semanas, se modifican todos sus pedidos de suministros existentes para cubrir la nueva demanda, que se realiza dentro de las dos semanas especificadas.  

 Varias líneas de planificación se multiplican simplemente por tres para proporcionar 15 bicicletas de ruta en lugar de 5, y las fechas de vencimiento se retroceden para proporcionar las cantidades aumentadas por la fecha de envío del pedido de venta Cannon Group. Para estas líneas de planificación, todas las cantidades pueden ser seguidas. Las líneas de planificación restantes incrementan en diez piezas, además de mover sus fechas de vencimiento. Para estas líneas de planificación, una parte de las cantidades no son seguidas debido a parámetros de planificación diferentes. Empiece a visualizar algunos de estos movimientos de seguimiento del pedido.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Ver los movimientos de seguimiento del pedido para el producto 1250

1.  Seleccione la línea de planificación del producto 1250 y seleccione la acción **Seguimiento de pedido**.  

     Las sietes líneas de la página **Seguimiento pedido** muestran que se hace un seguimiento de cinco y diez piezas desde la rueda trasera hasta las bicicletas de ruta en los dos pedidos de venta, respectivamente.  

     No se hace el seguimiento de las últimas cinco piezas. Empiece a analizar.  

2.  Elija el campo **Cantidad no seguida**.  

     La página **Elementos planificación sin seguimiento** muestra que el producto 1250 utiliza un parámetro de planificación, Múltiplos de pedido, de 10,00. Por lo tanto, la línea de planificación es de 20 piezas en el total para redondear la necesidad real hasta el número más cercano divisible por 10. Las cinco últimas piezas son una cantidad no seguida para satisfacer el parámetro de planificación.  

3.  Cierre todas las páginas salvo **Hoja planificación**.  

### <a name="to-view-an-existing-order"></a>Ver un pedido existente

1.  En la línea de planificación del producto 1250, elija el campo **Nº orden ref.**. .  
2.  En la página **Orden produc. planif. en firme** para el buje trasero. El pedido existente de diez piezas, que se creó en la primera ejecución de la planificación, se abrirá.  
3.  Cierre la orden de producción planificada en firme.  

 De este modo finaliza el tutorial sobre cómo se utiliza el sistema de planificación para detectar automáticamente la demanda, calcular los pedidos de suministro adecuados según los parámetros de demanda y planificación y, finalmente, crear automáticamente diferentes tipos de pedidos de suministro con las fechas y cantidades adecuadas.  

## <a name="see-also"></a>Consulte también
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
