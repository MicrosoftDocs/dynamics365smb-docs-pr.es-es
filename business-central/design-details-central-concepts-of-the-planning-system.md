---
title: 'Detalles de diseño: Conceptos centrales del sistema de planificación'
description: La planificación sugiere acciones para que el usuario las realice en función de la situación de demanda/oferta y los parámetros de planificación de los productos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Detalles de diseño: conceptos centrales del sistema de planificación

Las funciones de planificación se incluyen en un proyecto por lotes que primero selecciona los productos correspondientes y el periodo que se planificará. Luego, de acuerdo con el código de nivel inferior de cada artículo (posición de la lista de materiales), el trabajo por lotes llama a una unidad de código que calcula un plan de suministro. La unidad de código equilibra los conjuntos de oferta y demanda y sugiere acciones que debe realizar el usuario. Las acciones sugeridas aparecen como líneas en la hoja de planificación o la hoja de demanda.  

![Contenido de la página Hojas de planificación.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Contenido de la página Hojas de planificación")  

Se supone que el planificador de una empresa, como un comprador o un planificador de producción, es el usuario del sistema de planificación. El sistema de planificación ayuda al usuario a realizar los cálculos completos pero bastante sencillos de un plan. El usuario podrá concentrarse en resolver problemas más difíciles, como, por ejemplo, cuando las cosas son distintas de las normales.  

El sistema de planificación se basa en la demanda de cliente anticipada y real, como los pedidos previstos y de venta. Los cálculos de planificación sugieren acciones que puede realizar con respecto al suministro de los proveedores, el ensamblaje o la producción, o las transferencias desde otros almacenes. Un ejemplo de acción sugerida podría ser crear nuevos pedidos de suministro, como pedidos de compra u órdenes de producción. Si ya hay pedidos de aprovisionamiento, las acciones sugeridas pueden ser aumentar o acelerar los pedidos para satisfacer los cambios de la demanda.  

Otro objetivo del sistema de planificación es el de garantizar que las existencias no aumentan innecesariamente. En el caso de un descenso de la demanda, el programa de planificación sugerirá al usuario que posponga, reduzca la cantidad o cancele los pedidos de aprovisionamiento existentes.  

Una unidad de código contiene la lógica de planificación y las siguientes funciones:

* MRP y MPS
* Calc. plan. saldo periodo
* Calc. planif. regenerativa

No obstante, el cálculo del plan de aprovisionamiento implica a distintos subsistemas.  

El sistema de planificación no incluye ninguna lógica dedicada para la nivelación de capacidad o para la programación precisa. Esos tipos de trabajo de programación se realizan por separado. La falta de integración directa entre las dos áreas también significa que los cambios importantes de capacidad o de programación requerirán que vuelva a ejecutar la planificación.  

## Parámetros de la planificación

Los parámetros de planificación que establece para un producto o un grupo de productos controlan qué acciones sugerirá el sistema de planificación en las distintas situaciones. Defina parámetros de planificación para cada producto para comprobar el momento, la cantidad y el modo de reposición.  

También puede definir parámetros de planificación para cualquier combinación de producto, variante y ubicación mediante la configuración de una unidad de almacenamiento (UA) para cada combinación y, a continuación, mediante la especificación de los parámetros individuales. Obtenga más información en [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) y [Detalles de diseño: Parámetros de planificación](design-details-planning-parameters.md).  

## Fecha inicial de la planificación

El sistema de planificación lo ayuda a evitar tener pedidos abiertos en el pasado y acciones sugeridas que no son posibles. Planificación trata todas las fechas anteriores a la fecha de inicio como una zona congelada. La regla siguiente se aplica a la zona congelada:  

* Toda la demanda y aprovisionamiento antes de la fecha de inicio del periodo de planificación se tiene como parte del inventario o enviado. Es decir, se asume que el plan para el pasado se ejecuta según el plan proporcionado. Obtenga más información en [Procesar pedidos antes de la fecha de inicio de la planificación](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Seguimiento dinámico de pedidos (fijación)

El seguimiento dinámico de pedidos y su creación simultánea de mensajes de acción en la hoja de trabajo de planificación, no forma parte del sistema de planificación de suministro. Cuando se crea o se cambia una nueva demanda o suministro, el seguimiento dinámico de pedidos vincula, en tiempo real, la demanda y las cantidades que podrían cubrirla,  

Por ejemplo, si introduce o modifica un pedido de venta, el sistema de seguimiento dinámico de pedidos busca inmediatamente el aprovisionamiento para cubrir la demanda. El suministro podría ser del inventario o de un pedido de suministro previsto (como un pedido de compra o una orden de producción). Cuando encuentra una fuente de suministro, [!INCLUDE [prod_short](includes/prod_short.md)] vincula la oferta y la demanda. Accede al enlace en páginas de solo lectura desde las líneas del documento. Cuando no se encuentra un suministro adecuado, el sistema de seguimiento de pedidos dinámico crea mensajes de acción en la hoja de planificación con sugerencias de plan de suministro.  

El seguimiento dinámico de pedidos lo ayuda a evaluar si acepta sugerencias de pedidos de suministro. Desde el lado de la oferta, muestra la demanda que creó la oferta. Desde el lado de la demanda, idenetifica la oferta que debe cubrir la demanda.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Ejemplo de seguimiento dinámico de pedidos.":::

Obtenga más información en [Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).  

En empresas con un flujo de productos bajo y menos estructuras de producto avanzadas, podría ser suficiente utilizar el seguimiento dinámico de pedidos para la planificación de aprovisionamiento. No obstante, en entornos más ocupados, el sistema de planificación se debe utilizar para garantizar un plan de aprovisionamiento correctamente equilibrado.  

### Seguimiento dinámico de pedidos frente al sistema de planificación

Poddría ser complicado diferenciar entre el sistema de planificación y el seguimiento dinámico de pedidos. Ambas funciones muestran la salida en la hoja de trabajo de la planificación mediante la sugerencia de acciones que el planificador debe realizar. No obstante, la forma en la que se produce esta salida es diferente.  

El sistema de planificación se ocupa de todo el patrón de oferta y demanda de un artículo. Considera todos los niveles de la jerarquía de BOM a lo largo de la línea de tiempo. El seguimiento dinámico de pedidos solo aborda la situación del pedido que lo activó. Al equilibrar la oferta y la demanda, el sistema de planificación crea vínculos en un modo por lotes activado por el usuario. El seguimiento dinámico de pedidos crea los enlaces automáticamente cuando ingresa una demanda o un suministro. Por ejemplo, cuando crea una orden de compra o venta.  

El seguimiento dinámico de pedidos vincula el aprovisionamiento y la demanda cuando se introducen los datos según orden de entrada. Esto puede provocar un desorden en las prioridades. Por ejemplo, una orden de venta ingresada primero con una fecha de vencimiento el próximo mes podría estar vinculada al suministro en el inventario. El próximo pedido de venta que vence mañana puede generar un mensaje de acción para crear un nuevo pedido de compra para cubrirlo. La siguiente imagen muestra este escenario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Ejemplo de seguimiento de pedidos en la planificación de suministros 1.":::

El sistema de planificación se ocupa de la oferta y la demanda de artículos en un orden de prioridad. El pedido se prioriza según las fechas de vencimiento y los tipos de pedido. Es decir, sobre la base de que primero se necesita, primero se atiende. Elimina todos los vínculos de seguimiento de pedidos creados dinámicamente y los restablece según prioridad de fecha de vencimiento. Cuando se ha ejecutado el sistema de planificación, se han solucionado todos los desequilibrios entre demanda y suministro, tal como se ilustra a continuación para los mismos datos.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Ejemplo de seguimiento de pedidos en la planificación de suministros 2.":::  

Después de ejecutar la planificación, la tabla Entrada de mensaje de acción no contiene ningún mensaje de acción. Esos mensajes son reemplazados por las acciones sugeridas en la hoja de trabajo de planificación. Obtenga más información en [Conexiones de seguimiento de pedidos durante la planificación](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## Secuencia y prioridad en la planificación

La a secuencia de los cálculos en el plan es importante para que el proyecto se realice en un intervalo de tiempo razonable. La priorización de los requisitos y los recursos también desempeña una importante función a la hora de obtener los mejores resultados.  

El sistema de planificación se basa en la demanda. Los productos de primer nivel se deben planificar antes que los productos de nivel inferior, ya que pueden generar una demanda adicional para los productos de nivel inferior. Por ejemplo, las ubicaciones minoristas deben planificarse antes de que se planifiquen los centros de distribución, porque la ubicación minorista podría incluir demanda adicional del centro de distribución. En un nivel de contrapartida detallado, si un pedido de suministro lanzado puede cubrir el pedido de venta, el sistema no debe crear una nueva orden de suministro. No se debe asignar un suministro con un número de lote específico para cubrir una demanda genérica si otra demanda requiere este lote concreto.  

### Prioridad de producto / Cód. nivel más bajo

En un entorno de fabricación, la demanda para un producto terminado y sellable dará como resultado una demanda derivada para los componentes que forman parte del producto terminado. La estructura de lista de materiales controla la estructura de componentes y puede abarcar varios niveles de productos semiterminados. La planificación de un producto en un nivel provocará demanda derivada para los componentes en el siguiente nivel. Esta jerarquía dará como resultado finalmente una demanda derivada de los productos comprados. El sistema de planificación planifica artículos en orden de clasificación en la jerarquía total de la lista de materiales. El sistema comienza con artículos vendibles terminados en el nivel superior y continúa hacia abajo en la estructura del producto hasta los artículos de nivel inferior (según el código de nivel inferior).  

La siguiente imagen muestra la secuencia en la que [!INCLUDE [prod_short](includes/prod_short.md)] sugiere órdenes de suministro en el nivel superior. Asume que las sugerencias fueron aceptadas y también muestra elementos de nivel inferior.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planificación de las listas de materiales.":::

Para obtener más información acerca de las consideraciones de fabricación, vaya a [Cargar perfiles de inventario](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Optimización del rendimiento para cálculos de bajo nivel

Los cálculos de código de bajo nivel pueden afectar al rendimiento del sistema. Para reducir el efecto, puede desactivar el control de alternancia **Cálculo dinámico de códigos de bajo nivel** en la página **Configuración fabricación**. Cuando lo haga, [!INCLUDE[prod_short](includes/prod_short.md)] le sugiere que cree una entrada de cola de trabajos recurrente para actualizar diariamente los códigos de bajo nivel. Puede asegurarse de que el trabajo se ejecutará fuera del horario laboral especificando una hora de inicio en el campo **Primera fecha/hora de inicio**.

También puede agilizar los cálculos de códigos de bajo nivel seleccionando el control de alternancia **Optimizar el cálculo de códigos de bajo nivel** en la página **Configuración fabricación**.

> [!IMPORTANT]
> Si elige optimizar el rendimiento, [!INCLUDE[prod_short](includes/prod_short.md)] utilizará nuevos métodos de cálculo para determinar los códigos de bajo nivel. Si tiene una extensión que se basa en los eventos utilizados por los cálculos anteriores, la extensión podría dejar de funcionar.

### Prioridad de ubicaciones o de nivel de transferencia

Las empresas con más de un almacén podrían tener que planificar para cada almacén por individual. Por ejemplo, el nivel de existencias de seguridad de un producto y su directiva de reaprovisionamiento podrían diferir de un almacén a otro. Debe especificar los parámetros de planificación por artículo y ubicación.  

Puede usar SKU para especificar parámetros de planificación individuales. Las UA se pueden considerar como productos en un almacén específico. Si no ha definido un SKU para esa ubicación, [!INCLUDE [prod_short](includes/prod_short.md)] utilizará los parámetros establecidos en la ficha del producto. [!INCLUDE [prod_short](includes/prod_short.md)] calcula un plan para las ubicaciones activas únicamente, que es donde hay demanda o suministro para un producto indicado.  

Cualquier producto puede gestionarse en cualquier almacén, pero [!INCLUDE [prod_short](includes/prod_short.md)] tiene un enfoque estricto en cuanto al concepto de almacén. Por ejemplo, un pedido de venta para un artículo en un almacén no se puede satisfacer con stock de otro almacén. La cantidad de existencias primero se debe transferir a la ubicación especificada en el pedido de venta.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planificación de unidades de almacenamiento.":::

Obtenga más información en [Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md).  

### Prioridad pedido

En una UA concreta, la fecha solicitada o disponible representa la máxima prioridad; la demanda de hoy se debe tratar antes que la de los próximos días. Pero aparte de esta clase de prioridad, los distintos tipos de demanda y aprovisionamiento se ordenan según su relevancia empresarial para decidir qué demanda se debe satisfacer primero. Por el lado de la oferta, la prioridad de la orden determina la fuente de suministro a aplicar primero. Obtenga más información en [Priorizar pedidos](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Previsiones de demanda y pedidos abiertos

Las previsiones y los pedidos abiertos representan ambos la demanda prevista. El pedido abierto, que abarca las compras previstas de un cliente durante un determinado periodo de tiempo, sirve para reducir la incertidumbre de una previsión global. El pedido abierto es una previsión específica del cliente por encima de la previsión sin especificar, como se ilustra en la imagen isguiente.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planificación con previsiones.":::

Obtenga más información en [Los pedidos de ventas reducen la demanda de previsión](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Asignar planificación

Todos los artículos deben volver a planificarse para cuando el patrón de oferta o demanda haya cambiado desde la última vez que se calculó un plan. Por ejemplo, si introduce un nuevo pedido de venta o cambia uno existente, vuelva a calcular el plan. Entre otros motivos del nuevo cálculo del plan se incluye un cambio en la previsión o en el stock de seguridad. Un cambio en una lista de materiales mediante la adición o eliminación de un componente también indicaría probablemente un cambio, pero para el producto componente solo.  

El sistema de planificación supervisa dichos eventos y asigna los productos adecuados para realizar la planificación.  

En el caso de ubicaciones múltiples, la asignación sucede en el nivel de producto por combinación de almacén. Si se ha creado un pedido de venta en solo una ubicación, [!INCLUDE [prod_short](includes/prod_short.md)] asigna el producto a esa ubicación específica para planificar.  

El motivo para seleccionar productos para la planificación es cuestión de rendimiento del sistema. Si no ha cambiado el patrón de demanda-aprovisionamiento de un producto, el sistema de planificación no sugerirá ninguna acción. Sin la asignación de planificación, el sistema tendría que realizar cálculos para todos los productos a fin de averiguar para qué debe planificar. Para obtener más información sobre las razones para asignar elementos para la planificación, vaya a [Detalles de diseño: tabla de asignación de planificación](design-details-planning-assignment-table.md).  

Las siguientes son las opciones de planificación disponibles:  

* **Calc. planif. regenerativa** calcula todos los productos seleccionados, tanto si es necesario como si no.  
* **Calc. plan. saldo periodo** calcula únicamente aquellos productos seleccionados que tengan algún cambio en su modelo de demanda y aprovisionamiento y, por tanto, se hayan asignado para planificarse.  

Algunas personas creen que la planificación de cambio neto se debe realizar de forma dinámica, por ejemplo, cuando se registran los pedidos de venta. No obstante, la planificación sobre la marcha podría resultar confusa, ya que los mensajes de las acciones y el seguimiento de pedidos dinámico también se calculan sobre la marcha. [!INCLUDE[prod_short](includes/prod_short.md)] ofrece control disponible para promesa en tiempo real. Proporciona advertencias emergentes cuando ingresa órdenes de venta y el plan de suministro actual no puede satisfacer la demanda.  

El sistema de planificación planifica solo los productos que ha preparado con los parámetros apropiados de planificación. De lo contrario, se supone que planeará los productos de un modo manual o semiautomático con la característica Planificación de pedidos. Para obtener más información sobre los procedimientos de planificación automática, vaya a [Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md).  

## Dimensiones de producto

La demanda y el aprovisionamiento pueden llevar códigos de variante y códigos de almacén que se deben respetar cuando el sistema de planificación salde la demanda y el aprovisionamiento.  

[!INCLUDE [prod_short](includes/prod_short.md)] trata los códigos de variante y de ubicación como dimensiones de producto en una línea de pedido de venta, un movimiento de contabilidad, etc. Por consiguiente, se calcula un plan para cada combinación de variante y almacén, como si la combinación fuera un número de producto aparte.  

En lugar de calcular cualquier combinación teórica de variante y ubicación, [!INCLUDE [prod_short](includes/prod_short.md)] solo calcula las combinaciones que existen realmente en la base de datos. Para obtener más información sobre cómo el sistema de planificación gestiona los códigos de almacén en demandas, vaya a [Detalles de diseño: Demanda en almacén vacío](design-details-balancing-demand-and-supply.md).  

## Atributos de artículo

Los artículos suelen tener atributos generales, como el número de artículo am, el código de variante, el código de ubicación y el tipo de pedido. Sin embargo, cada evento de demanda y suministro puede tener otras especificaciones, como números de serie o de lote. El sistema de planificación planea estos atributos de determinadas formas según su nivel de especificación.  

Un vínculo de pedido a pedido entre demanda y aprovisionamiento es otro tipo de atributo que afecta al sistema de planificación. Obtenga más información en [Enlaces de pedido a pedido](#order-to-order-links).

### Atributos específicos

Algunos atributos de la demanda son específicos y la oferta debe coincidir exactamente con ellos.

* Números de serie o de lote que necesitan aplicación específica (estos atributos son necesarios si activa el control de alternancia **Seguim. NS específ.** o **Seguim. lote específ.** en la página **Ficha cód. seguim. prod.** para el código de seguimiento de producto que usa el producto).  
* Conexiones a pedidos de suministro creados manual o automáticamente para una demanda determinada (conexiones de pedido contra pedido).  

El sistema de planificación aplica las reglas siguientes a estos atributos:  

* La demanda con atributos específicos se puede cubrir únicamente con atributos coincidentes.  
* El suministro con atributos específicos también puede satisfacer la demanda que no requiera estos atributos específicamente.  

Si el inventario o los suministros proyectados no cumplen una demanda de atributos específicos, el sistema de planificación sugiere un nuevo pedido de aprovisionamiento sin sin tener en cuenta los parámetros de planificación.  

### Atributos no específicos

Los artículos con números de serie o de lote sin una configuración específica de seguimiento de artículos pueden tener números de serie o de lote no específicos. Estos tipos de números se pueden aplicar a cualquier número de serie o de lote. El sistema de planificación tiene más libertad, por ejemplo, para hacer corresponder una demanda serializada con un suministro serializado, normalmente en inventario.  

Los suministros a demanda con números de serie o de lote, específicos o no específicos, son de alta prioridad y están exentos de la zona congelada. Serán parte de la planificación incluso si vencen antes de la fecha de inicio de la planificación. Obtenga más información en [Carga de números de serie y de lote por nivel de especificación](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Para obtener más información sobre cómo el sistema de planificación equilibra los atributos, vaya a [Exención de números de serie y de lote y de vínculos de pedido a pedido del periodo anterior](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Vínculos de pedido a pedido

Pedido a pedido significa que usted compra, ensambla o produce un artículo para una demanda específica. Hay varias razones para elegir esta póliza:

* La demanda es poco frecuente.
* El tiempo de entrega es insignificante.
* Los atributos obligatorios varían.  

Otro caso que utiliza vínculos de pedido a pedido es cuando un pedido de ensamblado se vincula a un pedido de venta en una situación de ensamblado para pedido.  

Las conexiones de pedido contra pedido se aplican entre la demanda y el suministro de cuatro maneras:  

* Cuando el producto planificado usa la directiva de reaprovisionamiento **Pedido**  
* Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes en la misma orden de producción)  
* Al crear las órdenes de producción para los pedidos de venta con la característica de planificación de pedido de venta  
* Cuando ensambla un artículo en un pedido de ventas (**Política de ensamblaje** está establecida en **Ensamblar para pedido**)  

El sistema de planificación sugiere que solo solicite la cantidad requerida. El pedido de compra, la orden de producción o el pedido de ensamblado sigue correspondiéndose con la demanda correspondiente. Por ejemplo, si un pedido de venta se modifica en tiempo o en cantidad, el sistema de planificación sugiere que cambie el pedido de aprovisionamiento según corresponda.  

Cuando existen vínculos de pedido contra pedido, el sistema de planificación no incluye el suministro o inventario vinculado en el procedimiento de contrapartida. Los planificadores pueden decidir si utilizar la oferta vinculada o una nueva demanda. En este último caso, pueden eliminar la orden de suministro o reservar manualmente el suministro vinculado.  

Los enlaces de reservas y seguimiento de pedidos se rompen si una situación se vuelve imposible. Por ejemplo, al mover la demanda a una fecha anterior a la oferta. Los enlaces de pedido a pedido se adaptan a los cambios en la oferta o la demanda y nunca se rompen.  

## Reservas

El sistema de planificación no incluye ninguna cantidad reservada en los cálculos. Por ejemplo, si una cantidad para un pedido de ventas está total o parcialmente reservada, no puede usar la cantidad para cubrir otra demanda.

El sistema de planificación no incluye ninguna cantidad reservada en el perfil de inventario proyectado. Debe considerar todas las cantidades para determinar cuándo ha pasado el punto de reorden y cuántos reordenar para alcanzar el nivel máximo de inventario. Las reservas innecesarias pueden aumentar el riesgo de que los niveles de inventario bajen demasiado, ya que la lógica de planificación no detecta las cantidades reservadas.  

La siguiente imagen muestra cómo las reservas pueden dificultar la planificación.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planificación con reservas.":::

Obtenga más información en [Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).  

## Advertencias

La primera columna de la hoja de planificación corresponde a los campos de advertencia. Aparece un icono de advertencia cuando crea una línea de planificación para una situación inusual.  

El suministro de las líneas de planificación con advertencias no se modifica normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere un suministro para satisfacer la cantidad exacta de la demanda. Sin embargo, el sistema se puede configurar para respetar parámetros de planificación para las líneas de planificación con determinadas advertencias. La información de advertencia se muestra en la página **Elementos planificación sin seguimiento**, que también muestra vínculos del seguimiento de pedidos a las entidades de red que no realizan pedidos. Existen tres tipos de advertencias:  

* Emergencia  
* Excepción  
* Atención  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Advertencias en la hoja de planificación.":::

### Emergencia

La advertencia de emergencia se muestra en dos situaciones:  

* Cuando el inventario es negativo en la fecha de inicio de la planificación  
* Cuando existen eventos de demanda o aprovisionamiento atrasados  

Si el inventario de un producto es negativo en la fecha de inicio de la planificación, el sistema de planificación le sugiere un aprovisionamiento de emergencia para la cantidad negativa que llegue en la fecha de inicio de la planificación. El texto de advertencia informa de tal fecha y de la cantidad del pedido de emergencia. Obtenga más información en [Gestión de inventario negativo proyectado](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Las líneas de documento con fecha de vencimiento antes de la fecha de inicio de la planificación se consolidan en un pedido de demanda de emergencia. El pedido se planifica para llegar en la fecha de inicio de la planificación.  

### Excepción

Se mostrará la advertencia de excepción si el inventario disponible previsto cae por debajo de la cantidad de existencias de seguridad. El programa de planificación sugerirá un pedido de suministros para cubrir la demanda en la fecha de vencimiento. El texto de advertencia informa de la cantidad de existencias de seguridad del producto y de la fecha en la que se infringe.  

La violación del nivel de existencias de seguridad es una excepción. No debería suceder si el punto de reorden está configurado correctamente. Obtenga más información en [Función del punto de pedido](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Las propuestas de pedido excepcionales ayudan a garantizar que el inventario disponible proyectado nunca será menor que el nivel de existencias de seguridad. La cantidad propuesta cubre las existencias de seguridad, sin tener en cuenta los parámetros de planificación. Sin embargo, en algunos ejemplos, se considerarán modificadores de pedido.  

> [!NOTE]  
> El sistema de planificación puede haber consumido el stock de seguridad intencionadamente y, a continuación, lo repondrá de forma inmediata. Obtenga más información en [Consumir existencias de seguridad](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Atención

La advertencia de atención se muestra en tres situaciones:  

* La fecha de inicio de la planificación es anterior a la fecha de trabajo.  
* La línea de planificación sugiere cambiar una compra realizada o una orden de producción.  
* El inventario proyectado supera el nivel de desbordamiento en la fecha de vencimiento. Obtenga más información en [Manténgase por debajo del nivel de desbordamiento](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> En las líneas de planificación con advertencias, el campo **Aceptar mensaje acción** está desactivado, ya que se espera que el planificador investigue estás líneas antes de llevar a cabo el plan.  

## Registros de errores

En la página de la solicitud **Calcular plan**, puede seleccionar el campo **Parar y mostrar primer error** para incluir una parada en la ejecución de la planificación cuando se encuentre el primer error. Se muestra un mensaje con información sobre el error. Si hay algún error, la hoja de cálculo de planificación solo mostrará las líneas de planificación correctas realizadas antes de que se produjera el error.  

Si el campo no está seleccionado, el trabajo por lotes **Calcular plan** continuará hasta que se haya completado. Los errores no interrumpirán el trabajo por lotes. Si hay errores, un mensaje indica cuántos elementos se vieron afectados. A continuación, la página **Registro error planificación** proporciona más información sobre el error y vínculos a los documentos o configuraciones afectados.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Mensajes de error en la hoja de planificación.":::

## Flexib. planificación

No siempre es práctico planificar un pedido de suministro existente. Por ejemplo, cuando la producción ha comenzado o contratas personas adicionales en un día específico para hacer el proyecto. Para indicar si el sistema de planificación puede cambiar un pedido, todas las líneas de pedido de suministro tienen el campo **Flexib. planificación** con dos opciones: **Ilimitada** o **Ninguna**. Si el campo está establecido en **Ninguno**, el sistema de planificación no intentará modificar la línea del pedido de aprovisionamiento.  

Puede elegir manualmente una opción del campo, pero, en algunos casos [!INCLUDE [prod_short](includes/prod_short.md)] lo configurará automáticamente. Es importante el hecho de que pueda configurar manualmente la flexibilidad de planificación, ya que facilita la adaptación del uso de la característica a diferentes flujos de trabajo y casos empresariales. Para obtener más información acerca de cómo se utiliza este campo, vaya a [Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md).  

## Planificación de pedidos

La herramienta de planificación de suministro básica representada por la página **Planificación de pedidos** se ha diseñado para la toma de decisiones manual. No tiene en cuenta ningún parámetro de planificación, por lo que no se contempla más adelante en este artículo. Obtenga más información en [Planificación de nuevos pedidos a pedido por pedido](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Recomendamos que no use la planificación de pedidos si su empresa ya utiliza las hojas de trabajo de planificación o solicitud. Los pedidos de aprovisionamientos creados a través de la página **Programación de pedidos** se pueden modificar o eliminar durante las ejecuciones de planificaciones automatizadas. Estos cambios suceden porque los procesos de planificación automatizados utilizan parámetros de planificación que podría no haber tenido en cuenta al realizar el plan manualmente en la página Programación de pedidos.  

## Carga limitada

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona un cronograma aproximado para planificar el uso razonable de los recursos. No crea ni mantiene automáticamente programaciones detalladas basadas en prioridades o reglas de optimización.  

El uso previsto de la característica de recursos con capacidad limitada es el siguiente:

* Para no sobrecargar los recursos
* Para garantizar que la capacidad no se quede sin asignar si pudiera disminuir el tiempo de respuesta de una orden de producción

Al planificar con recursos de capacidad limitada, [!INCLUDE [prod_short](includes/prod_short.md)] se asegura de que no se carguen recursos por encima de su capacidad (carga crítica). Asigna cada operación a la franja temporal disponible más próxima. Si la franja temporal no es lo suficientemente amplia para completar toda la operación, divide la operación en dos o más partes que se colocarán en las franjas temporales más próximas disponibles.  

> [!NOTE]  
> En el caso de división de la operación, el tiempo de configuración se asigna solo una vez, pues se presupone que se realiza algún ajuste manual para optimizar la programación.  

Puede agreagar tiempo de amortiguación a recursos para minimizar la división de operaciones. Esta vez vamos a permitir que [!INCLUDE [prod_short](includes/prod_short.md)] programe la carga para el último día posible superando ligeramente el porcentaje de carga crítica.  

## Consulte también .

[Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md)  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)  
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)  
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
