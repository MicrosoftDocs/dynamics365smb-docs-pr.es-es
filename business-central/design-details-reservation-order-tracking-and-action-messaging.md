---
title: 'Detalles de diseño: reserva, seguimiento de pedidos y mensajes de acciones | Documentos de Microsoft'
description: El sistema de reservas es completo e incluye las características correlacionadas y paralelas de seguimiento de pedidos y mensajes de acción.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones

El sistema de reservas es completo e incluye las características correlacionadas y paralelas de seguimiento de pedidos y mensajes de acción.  

En el centro del programa de reservas se encuentra la vinculación entre un movimiento de demanda y su correspondiente movimiento de aprovisionamiento, bien mediante reserva o mediante seguimiento de pedidos. Una reserva es un vínculo generado por el usuario, y un registro de seguimiento de pedido es un vínculo generado por el sistema. Las cantidades de un producto que se introduce en el programa de reservas aparece como reservado o como con seguimiento de pedido, pero no ambos al mismo tiempo. La manera en que los sistemas gestionan un producto depende de cómo se haya configurado el producto.  

El sistema de reserva interactúa con el sistema de planificación creando mensajes de acción en las líneas de planificación durante los procesos de planificación. Un mensaje de acción se puede considerar un accesorio a un registro de seguimiento de pedido. Los mensajes de acción, tanto creados dinámicamente para hacer un seguimiento del pedido o durante la ejecución de la planificación, son una herramienta adecuada para planificar el aprovisionamiento de forma eficaz.  

> [!NOTE]  
> El sistema de planificación ignora las cantidades reservadas, es decir, el vínculo fuerte que se establece entre el suministro y la demanda no se puede cambiar mediante la planificación.  

 El sistema de reservas también constituye la base estructural del sistema de seguimiento de productos. Para obtener más información, consulte [Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="reservation"></a>Reserva

 Una reserva es un vínculo firme que conecta una demanda determinada con un aprovisionamiento específico. Este vínculo afecta directamente a la transacción de inventario posterior y garantiza la liquidación correcta de los movimientos de producto para fines de valoración de costes. Una reserva reemplaza el método de coste predeterminado de un producto. Para obtener más información, consulte [Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md).  

 La página **Reservas** está accesible desde todas las líneas de pedido del tipo de demanda y de suministro. En esta página, el usuario puede especificar a qué movimiento de demanda o aprovisionamiento crear un enlace de reserva. La reserva consta de un par de registros que comparten el mismo número de movimiento. Un registro tiene un signo negativo y apunta a la demanda. El otro registro tiene un signo positivo y apunta al suministro. Estos registros se almacenan en la tabla **Mov. reserva** con el valor de estado **Reservas**. El usuario puede ver todas las reservas en la página **Movs. reserva**.  

### <a name="offsetting-in-reservations"></a>Compensación en reservas

 Las reservas se realizan según las cantidades de producto disponibles. La disponibilidad de producto se calcula en términos básicos de la siguiente forma:  

 cantidad disponible = inventario + recepciones programadas - requerimientos brutos  

 En la tabla siguiente se muestran los detalles de las entidades de la red de pedidos que forman parte del cálculo de disponibilidad.  

||Campo en T27|Tabla de origen|Filtro de tabla|Campo de origen|  
|-|------------------|------------------|------------------|------------------|  
|**Existencias**|Existencias|Mov. producto|N/D|Cantidad|  
|**Recep. previstas**|Recep. (cdad.) O.P. p.f.|Lín. orden prod.|= Planif. en firme|Cdad. pendiente (base)|  
|**Recep. previstas**|Recep. (cdad.) O.P. lanz.|Lín. orden prod.|= Lanzados|Cdad. pendiente (base)|  
|**Recep. previstas**|Cdad. en pedido de ensamblado|Encabezado de ensamblado|= Pedido|Cdad. pendiente (base)|  
|**Recep. previstas**|Cdad. en pedidos compra|Lín. compra|= Pedido|Cdad. pendiente (base)|  
|**Recep. previstas**|Recep. ped. transfer. (cdad.)|Lín. transferencia|N/D|Cantidad pendiente|  
|**Necesidades brutas**|Cdad. en pedidos venta|Lín. venta|= Pedido|Cdad. pendiente (base)|  
|**Necesidades brutas**|Necesidad programada (cdad.)|Componente orden producción|<>Simulada|Cdad. pendiente (base)|  
|**Necesidades brutas**|Cdad. componentes|Línea de ensamblado|= Pedido|Cdad. pendiente (base)|  
|**Necesidades brutas**|Envío ped. transfer. (cdad.)|Lín. transferencia|N/D|Cantidad pendiente|  

 Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a>Reserva manual

Cuando un usuario crea intencionadamente una reserva, obtiene la propiedad completa de estos productos, además de su responsabilidad. Esto significa que el usuario también debe modificar o cancelar manualmente una reserva. Dichos cambios manuales pueden provocar la modificación automática de las reservas implicadas.  

En la tabla siguiente se muestra cuándo se pueden producir las modificaciones y cuáles son:  

|Acción del usuario|Reacción del sistema|  
|-----------------|---------------------|  
|Reducción de la cantidad reservada|Los campos de cantidad relacionados se actualizan según corresponda.|  
|Cambio de campos de fecha|Los campos de fecha relacionados se actualizan según corresponda.<br /><br /> **Nota:** Si la fecha de vencimiento en una demanda se modifica para que preceda a la fecha de envío o la fecha de vencimiento del aprovisionamiento, la reserva se cancela.|  
|Supresión del pedido|Se cancela la reserva.|  
|Cambio de almacén, ubicación, variante, número de serie o un número de lote|Se cancela la reserva.|  

> [!NOTE]  
> La funcionalidad de enlace posterior también puede cambiar las reservas sin informar al usuario, mediante la reorganización de las reservas no específicas de números de serie o de lote. Para obtener más información, consulte [Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md).  

### <a name="automatic-reservations"></a>Reservas automáticas

 La ficha de producto se puede configurar para que siempre se reserve automáticamente en la demanda, como los pedidos de venta. En este caso, se hace la reserva con respecto al inventario, pedidos de compra, pedidos de ensamblado y órdenes de producción. Si el aprovisionamiento es insuficiente se emite una advertencia.  

 Además, los productos se reservan automáticamente a través de diversas funciones de planificación para mantener una demanda vinculada a un aprovisionamiento concreto. Los movimientos de seguimiento de pedidos para dichos vínculos de planificación contienen **Reservas** en el campo **Estado reserva** en la tabla **Mov. reserva**. En las siguientes situaciones se crean reservas automáticas:  

- Un pedido de producción de varios niveles cuyo campo **Directiva fabricación** del principal involucrado y los productos secundarios se establece en **Fab-contra-pedido**. El sistema de planificación crea reservas entre la orden de producción principal y las órdenes de producción subyacentes para garantizar que se procesan juntas. Dicho enlace de reserva reemplaza la valoración de existencias y el método de liquidación predeterminados del producto.  

- Una orden de producción, de ensamblado o de compra cuyo campo **Directiva reaprov.** del producto implicado está establecido en **Pedido**. El sistema de planificación crea reservas entre la demanda y el suministro planeado para garantizar que se crea el suministro específico. Para obtener más información, consulte [Pedido](design-details-handling-reordering-policies.md#order).  

- Una orden de producción creada de un pedido de venta con la función de **Planificación pedido venta** va vinculada al pedido de venta a una reserva automática.  

- Un pedido de ensamblado creado automáticamente para una línea de pedido de venta para satisfacer la cantidad en el campo **($ T_37_900 Qty. to Assemble to Order $)**. Esta reserva automática vincula la demanda de venta y el suministro de ensamblado de manera que los procesadores de pedidos de venta pueden personalizar y prometer el elemento de ensamblado al cliente directamente. Además, la reserva vincula la salida de ensamblado con la línea de pedido de venta hasta la actividad de envío que satisfaga el pedido del cliente.  

En el caso de aprovisionamiento o demanda no asignadas, el sistema de planificación asigna automáticamente un estado de reserva de tipo **Excedente**. Podría ser resultado de la demanda que se debe a las cantidades previstas o a los parámetros de planificación introducidos por el usuario. Es un excedente legítimo, que el sistema reconoce, y no genera mensajes de acción. El excedente también podría ser un exceso de suministro auténtico o una demanda que permanece sin seguimiento. Se trata de una indicación de un desequilibrio de la red de pedidos, lo que provoca que el sistema emita mensajes de acción. Observe que un mensaje de acción que sugiere un cambio en la cantidad siempre hace referencia al tipo **Excedente**. Para obtener más información, consulte "Ejemplo: Seguimiento de pedidos en ventas, producción y transferencias" en este tema.  

Las reservas automáticas que se crean durante la ejecución de la planificación se gestionan de las siguientes formas:  

- Se aplican en las cantidades de producto que forman parte del cálculo de disponibilidad, como reservas manuales. Para obtener más información, consulte la sección "Compensación en reservas" en este tema.  

- Se incluyen y se pueden modificar en procesos de planificación posteriores, a diferencia de los productos reservados manualmente.  

## <a name="order-tracking"></a>Seguimiento de pedidos

El seguimiento de pedidos ayuda al planificador a mantener un plan de suministro válido al ofrecer información general del desplazamiento entre la demanda y el suministro en la red de pedidos. Los registros de seguimiento de pedidos sirven de base para crear mensajes de acción dinámicos y planificar sugerencias de línea durante los procesos de planificación.  

> [!NOTE]  
> El sistema de seguimiento de pedidos compensa las existencias disponibles a medida que los pedidos entran en la red de pedidos. Esto implica que el sistema no priorice dé prioridad a los pedidos que puedan ser más urgentes en cuanto a la fecha de vencimiento. Por lo tanto, depende de la lógica del sistema de planificación o del conocimiento del planificador cambiar dichas prioridades de una forma significativa.  

> [!NOTE]  
> La directiva de seguimiento de pedidos y la función Traer mensajes acción no están integradas con los trabajos. Esto significa que no se hace seguimiento automático de la demanda relacionada con un proyecto. Al no hacerse un seguimiento, podría hacer que se hiciera un seguimiento de un reabastecimiento existente con información de proyecto hacia otra demanda, por ejemplo, un pedido de venta. Por tanto, puede darse el caso de que haya información sobre el inventario disponible no sincronizada.  

### <a name="the-order-network"></a>Red de pedidos

El sistema de seguimiento de pedidos se basa en el principio de que la red de pedidos debe estar siempre en un estado de equilibrio, en el que cada demanda que entre en el sistema se compense con un suministro correspondiente y viceversa. El programa lo proporciona mediante la identificación de los vínculos lógicos entre todos los movimientos de demanda y de suministro en la red de pedidos.  

Este principio implica que un cambio en la demanda genera un desequilibrio en el lado de suministro de la red de pedidos. Inversamente, un cambio en el aprovisionamiento genera un desequilibrio en la demanda del lado de la red de pedidos. En realidad, la red de pedidos está en un estado de flujo constante con usuarios que entran, hacen modificaciones y eliminan pedidos. El seguimiento de pedidos procesa los pedidos dinámicamente, reacciona a cada cambio en el momento que entra en el sistema y forma parte de la red de pedidos. En cuanto se creen nuevos registros de seguimiento de pedidos, la red de pedidos pasa a tener saldo, pero solo hasta que se produzca el siguiente cambio.  

Para aumentar la transparencia de los cálculos en el sistema de planificación, la página **Elementos planificación sin seguimiento** muestra las cantidades de las que no se realiza el seguimiento, que representan la diferencia de categoría entre la demanda conocida y el suministro sugerido. Cada línea en la página hace referencia a la causa de excedente, como **Pedido abierto**, **Nivel de existencias de seguridad**, **Cdad. fija reaprov**, **Cantidad mínima de pedido**, **Redondeo** o **Amortiguador**.  

### <a name="offsetting-in-order-tracking"></a>Compensación en el seguimiento de pedidos

A diferencia que con las reservas, que se pueden crear solo con cantidades disponibles de productos, el seguimiento de pedidos se puede aplicar a todas las entidades de la red de pedidos que formen parte del cálculo de requisitos netos del sistema de planificación. La demanda neta se calcula de la siguiente forma:  

*demanda neta = necesidades brutas + punto de pedido - recepciones programadas - recepciones planificadas - saldo disponible estimado  

> [!NOTE]  
> En las demandas relacionadas con previsiones o parámetros de planificación no se hacen seguimientos de pedidos.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Ejemplo: Seguimiento de pedidos en ventas, producción y transferencias

En el escenario siguiente se muestra el orden en el que se crean los movimientos de seguimiento de pedidos en la tabla **Mov. reserva** como resultado de varios cambios de la red de pedidos.  

Supongamos que los siguientes son los datos para dos productos configurados para seguimiento de pedidos.  

|Producto 1|Name|"Componente"|
|-|-|-|
||Disponibilidad|100 unidades en el almacén WEST<br /><br />- 30 unidades de LOTA<br />- 70 unidades de LOTB|  
|Producto 2|Name|"Producto fabricado"|
||L. MAT de producción|1 cdad. por "Componente"|  
||Demanda|Venta de 100 unidades en la ubicación EAST|  
||Aprovisionamiento|Orden de producción lanzada (generada con la función **Planificación pedido venta** para la venta de 100 unidades)|  

En la página **Configuración fabricación**, el campo **Componentes en alm.** se establece en **ROJO**.

Los siguientes movimientos de seguimiento de pedidos están en la tabla **Mov. reserva** según los datos de la tabla.  

 ![Primer ejemplo de entradas de seguimiento de pedidos en la tabla Mov. reserva.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### <a name="entry-numbers-8-and-9"></a>Números de movimiento 8 y 9

En el caso de necesidad componentes para LOTA y de LOTB respectivamente, se crean enlaces de seguimiento desde la demanda en la tabla 5407, **Componente orden producción**, al aprovisionamiento en la tabla 32, **Mov. producto**. El campo **Estado reserva** contiene **Seguimiento** para indicar que estos movimientos son vínculos de seguimiento de pedidos dinámico entre suministro y demanda.  

> [!NOTE]  
> El campo **Nº lote** está vacío en las líneas de demanda porque los números de lote no están especificado en las líneas de componente de la orden de producción lanzada.  

### <a name="entry-number-10"></a>Número de movimiento 10

Desde la demanda de venta en la tabla 37, **Lín. venta**, se crea un vínculo de seguimiento de pedidos hacia el aprovisionamiento en la tabla 5406, **Lín. orden prod.**. El campo **Estado reserva** contiene **Reservas**, y el campo **Atado** contiene **Pedido contra pedido**. Se debe a que la orden de producción lanzada se ha generado específicamente para el pedido de venta y debe permanecer vinculada, a diferencia de las conexiones de seguimiento de pedidos con un estado de reserva de **Seguimiento**, que se crean y cambian dinámicamente. Para obtener más información, consulte la sección "Reservas automáticas" en este tema.  

 En este punto del ejemplo, las 100 unidades de LOTA y LOTB se transferirán al almacén EAST por medio de un pedido de transferencia.  

> [!NOTE]  
> En este punto, solo se registra el envío del pedido de transferencia, no la recepción.  

 Ahora, los siguientes movimientos de seguimiento de pedidos están en la tabla **Mov. reserva**.  

 ![Segundo ejemplo de entradas de seguimiento de pedidos en la tabla Mov. reserva.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### <a name="entry-numbers-8-and-9-1"></a>Números de movimiento 8 y 9

Los movimientos de seguimiento de pedidos para los dos lotes del componente que refleja la demanda de la tabla 5407 cambian el estado de reserva de **Seguimiento** a **Excedente**. El motivo es que los suministros a los que estaban vinculados antes, en la tabla 32, se han usado mediante el envío del pedido de transferencia.  

Los excedentes verdaderos, como en este caso, reflejan un exceso de aprovisionamiento que permanece sin seguimiento. Es una indicación de desequilibrio en la red de pedidos que generará un mensaje de acción por parte del sistema de planificación, a menos que se resuelva dinámicamente.  

### <a name="entry-numbers-12-to-16"></a>Números de movimiento de 12 a 16

Dado que se registran dos lotes del componente en el pedido de transferencia como enviados pero no recibidos, todos los registros positivos de seguimiento del pedido relacionados son del tipo de reserva **Excedente**, lo que indica que no están asignados a ninguna demanda. Para cada número de lote, un movimiento se relaciona con la tabla 5741, **Lín. transferencia**, y un movimiento se relaciona con el movimiento de producto en la ubicación en tránsito donde ahora están los productos.  

En este punto del ejemplo, el pedido de transferencia de los componentes del almacén EAST a WEST se registran como recibido.  

Ahora, los siguientes movimientos de seguimiento de pedidos están en la tabla **Mov. reserva**.  

 ![Tercer ejemplo de entradas de seguimiento de pedidos en la tabla Mov. reserva.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

Los movimientos de seguimiento de pedidos ahora son similares al primer punto del escenario, antes de que el pedido de transferencia se registrara como enviado únicamente, con la excepción de que los movimientos del componente ahora tienen el estado de reserva **Excedente**. Se debe a que la necesidad de componentes aún está en la ubicación WEST, lo que refleja que el campo **Cód. almacén** de la línea de componentes de la orden de producción contiene **WEST**, tal como se ha configurado en el campo **Componentes en alm.** El suministro que antes se ha asignado a esta demanda se ha transferido a la ubicación EAST y ahora no se puede realizar el seguimiento completo a menos que la necesidad de componentes de la línea de la orden de producción se cambie a la ubicación EAST.  

En este punto del ejemplo, **Cód. almacén** en la línea del orden de producción está establecido en **EAST**. Además, en la página **Líns. seguim. prod.**, las 30 unidades de LOTA y las 70 unidades de LOTB se asignan a la línea de orden de producción.  

Ahora, los siguientes movimientos de seguimiento de pedidos están en la tabla **Mov. reserva**.  

 ![Cuarto ejemplo de entradas de seguimiento de pedidos en la tabla Mov. reserva.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### <a name="entry-numbers-21-and-22"></a>Números de movimiento 21 y 22

Como la necesidad de componentes se ha cambiado a la ubicación EAST y el suministro está disponible como movimientos de producto en la ubicación EAST, ahora se realiza un seguimiento completo de todos los movimientos de seguimiento de pedidos de los dos números de lote, tal como indica el estado de reserva de **Seguimiento**.  

El campo **Nº lote** ahora está rellenado en el movimiento de seguimiento de pedidos para la tabla 5407 porque los números de lote se han asignado a las líneas de componente de la orden de producción.  

## <a name="action-messaging"></a>Mensajes de acción

Cuando el sistema de seguimiento de pedidos detecta un desequilibrio en la red de pedidos, crea automáticamente un mensaje de acción para notificar al usuario. Los mensajes de acción son llamadas generadas por el sistema para que el usuario realice una acción que especifican los detalles de desequilibrio y sugerencias sobre cómo restaurar los saldos a la red de pedidos. Se muestran como líneas de planificación en la página **Hoja planificación** cuando se elige **Traer mensajes acción**. Además, los mensajes de acción se muestran en líneas de planificación generadas por la ejecución de la planificación para reflejar las sugerencias del sistema de planificación sobre cómo restaurar los saldos en la red de pedidos. En ambos casos, se ejecutan propuestas en la red de pedidos al elegir **Ejecutar mensajes de acción**.  

Un mensaje de acción trata un nivel L.M. cada vez. Si el usuario acepta el mensaje de acción, puede generar mensajes de acción adicionales en el nivel de L.M. siguiente.  

En la tabla siguiente se muestran los mensajes de acción existentes.  

|Mensaje acción|Description|  
|--------------------|---------------------------------------|  
|**Cambiar cdad.**|Cambia la cantidad en un pedido de aprovisionamiento existente para cubrir una demanda modificada o nueva.|  
|**Reprogramar**|Vuelve a programar la fecha de vencimiento en un pedido existente.|  
|**Volver a programar & camb. cdad.**|Vuelve a programar la fecha de vencimiento y cambia la cantidad en un pedido existente.|  
|**Nuevo**|Crea un pedido nuevo si la demanda no se puede satisfacer mediante ninguno de los mensajes de acción anteriores.|  
|**Cancelar**|Cancela un pedido existente.|  

El sistema de seguimiento de pedidos siempre intenta resolver un desequilibrio en la red de pedidos existente. Si esto no es posible, emite un mensaje de acción para crear un pedido nuevo. A continuación se incluye la lista prioritaria que usa el sistema de seguimiento de pedidos para determinar cómo restaurar el saldo. Si se ha introducido una demanda adicional en la red de pedidos, el sistema busca hacer un seguimiento de los pedidos a través de las siguientes comprobaciones:  

1. Comprobar cualquier exceso de aprovisionamiento en el registro del seguimiento de pedido existente para esta demanda.  
2. Comprobar recepciones planeadas y programadas en pedido con fecha de recepción. Se selecciona la última fecha posible.  
3. Comprobar existencias disponibles.  
4. Comprobar si un pedido de aprovisionamiento existe en el registro actual de seguimiento de pedido. Si es así, el programa emite un mensaje de acción de tipo **Cambiar** para incrementar el pedido.  
5. Comprobar que no exista un pedido de aprovisionamiento en el registro actual de seguimiento de pedido. Si es así, el programa emite un mensaje de acción de tipo **Nuevo** para crear un pedido nuevo.  

Las demandas abiertas pasan por la lista y desplazan el aprovisionamiento disponible en cada momento. La demanda restante se cubre siempre mediante el cheque 4 o el cheque 5.  

Cuando se produce una disminución en la cantidad de demanda, el sistema de seguimiento de pedidos intenta resolver el desequilibrio realizando las comprobaciones anteriores en orden inverso. Esto significa que los mensajes de acción existentes podrían modificarse o, incluso, modificarse, si es necesario. El sistema de seguimiento de pedidos siempre presenta el beneficio neto de los cálculos al usuario.  

## <a name="order-tracking-and-planning"></a>Seguimiento y planificación de pedidos

Cuando se ejecuta el sistema de planificación, elimina todos los registros de seguimiento de pedidos y los movimientos de mensajes de acción, y vuelve a crearlos como sugerencias de línea de planificación según los pares y las prioridades suministro/demanda. Cuando ha finalizado el proceso de planificación, la red de pedidos está equilibrada.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a>Sistema de planificación con respecto al seguimiento de pedidos y los mensajes de acción

 En la comparación siguiente se muestra la diferencia entre los métodos que usa el sistema de planificación para crear sugerencias de línea de planificación y los métodos que usa el sistema de seguimiento de pedidos para crear registros de seguimiento de pedidos y mensajes de acción.  

- El sistema de planificación se ocupa de todo el patrón de suministro y demanda de un determinado producto, mientras que el seguimiento de pedidos se ocupa del pedido que lo ha activado.  

- El sistema de planificación se ocupa de todos los niveles de la L.M., mientras que el seguimiento de pedidos se ocupa de un nivel de L.M. cada vez.  

- El sistema de planificación establece vínculos entre la demanda y el suministro según la fecha de vencimiento con prioridad. El seguimiento de pedidos establece vínculos entre la demanda y el suministro según la secuencia del movimiento de pedido.  

- El sistema de planificación tiene en cuenta los parámetros de planificación, mientras que el seguimiento de pedidos no.  

- El sistema de planificación crea un vínculo en un modo por lotes activado por el usuario cuando equilibra la demanda y el suministro, mientras que el seguimiento de pedidos crea los vínculos automática y dinámica a medida que el usuario introduce pedidos.  

## <a name="see-also"></a>Consulte también

[Detalles de diseño: conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
