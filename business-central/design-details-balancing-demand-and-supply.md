---
title: 'Detalles de diseño: Equilibrio de oferta y demanda'
description: Este artículo describe cómo priorizar objetivos equilibrando la oferta con la demanda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand" />Detalles de diseño: Equilibrio de oferta y demanda

Para comprender cómo funciona el sistema de planificación, es importante comprender sus objetivos prioritarios:  

* La demanda se satisfará con suficiente aprovisionamiento.  
* Los aprovisionamientos sirven todos a un fin.  

En general, estos objetivos se logran equilibrando el aprovisionamiento con la demanda.  

## <a name="supply-and-demand" />Oferta y demanda

El término *oferta* se refiere a cualquier tipo de cantidad positiva o entrante, como:

* Inventario
* Compras
* Ensamblado
* Producción
* Transferencias de entrada
* Devoluciones de ventas  

El término *demanda* se refiere a cualquier tipo de demanda bruta, como por ejemplo:

* Un artículo de un pedido de ventas
* Un componente para una orden de producción

[!INCLUDE [prod_short](includes/prod_short.md)] también permite usar tipos de demanda más técnicos, como inventario negativo y devoluciones de compra.

Para organizar los orígenes de oferta y demanda, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario. Un perfil es para eventos de demanda y el otro para los eventos de oferta correspondientes. Cada evento de suministro representa una entidad en un pedido, como por ejemplo:

* Una línea de pedido de venta
* Un movimiento contable de producto
* Una línea de pedido de producción

Cuando se cargan los perfiles de inventario, se equilibran los conjuntos de demanda-suministro para generar un plan de suministro que cumpla los objetivos enumerados.

Los niveles de inventario y los parámetros de planificación son otros tipos de oferta y demanda. Estos tipos se someten a un equilibrio integrado para reponer los artículos en stock. Obtenga más información en [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief" />El concepto del equilibrio en resumen

La demanda proviene de sus clientes. El suministro es lo que crea y elimina para establecer el equilibrio. El sistema de planificación se inicia con la demanda y, a continuación, vuelve hacia el suministro.  

Los perfiles de inventario contienen información acerca de las demandas y suministros, cantidades y plazos. Estos perfiles constituyen los dos lados de la escala de contrapartida.  

El objetivo de la planificación es equilibrar la oferta y demanda de un producto para garantizar que el suministro corresponderá a la demanda, según lo definido por los parámetros y las reglas de planificación.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Resumen del equilibrio entre la oferta y la demanda.":::

## <a name="process-orders-before-the-planning-start-date" />Procesar pedidos antes de la fecha de inicio de la planificación

Para evitar que un plan de suministro muestre sugerencias poco razonables, el sistema de planificación no planificará nada en el período anterior a la fecha de inicio de la planificación. La siguiente regla se aplica a ese período:

* Toda la demanda y aprovisionamiento antes de la fecha de inicio del periodo de planificación se tiene como parte del inventario o enviado.  

Salvo algunas excepciones, el sistema de planificación no sugerirá ningún cambio en los pedidos de suministro en el período ni creará vínculos de seguimiento de pedidos para ese periodo. Las excepciones a esta regla son las siguientes:  

* El inventario que se proyecta para estar disponible, incluida la suma de aprovisionamiento y la demanda en el período, es menor que cero.  
* Los pedidos con fecha anterior requieren números de serie o lote.  
* El conjunto de oferta y demanda se vincula por una directiva de pedido a pedido. 

Si el inventario disponible inicial es menor que cero, el sistema de planificación sugiere un pedido de aprovisionamiento de emergencia el día antes del periodo de planificación para cubrir la cantidad que falta. Por tanto, el inventario proyectado y disponible será siempre al menos cero cuando empiece la planificación para el periodo futuro. La línea de planificación de este pedido de suministro mostrará un icono de advertencia de emergencia con información adicional.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period" />Los números de serie y de lote y las conexiones de pedido contra pedido están exentos del periodo anterior

Si se requieren números de serie o de lote o existe un enlace de pedido a pedido, el sistema de planificación ignora la regla sobre el período anterior. Incluirá cantidades retroactivas desde la fecha de inicio y podría sugerir acciones correctivas si la oferta y la demanda no están sincronizadas. Estos conjuntos de oferta y demanda deben coincidir para garantizar que se satisfaga una demanda específica.

## <a name="load-inventory-profiles" />Cargar los perfiles de inventario

Para organizar los orígenes de oferta y demanda, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario.  

La oferta y la demanda con fechas de vencimiento en la fecha inicial de planificación se cargan en cada perfil de inventario. Cuando se cargan, los tipos de oferta y demanda se ordenan según las prioridades generales, como:

* Fecha de vencimiento
* Códigos de bajo nivel
* Ubicación
* Variante

Se aplican prioridades de pedido a los diversos tipos para satisfacer primero la demanda más importante. Obtenga más información en [Priorización de pedidos](design-details-balancing-demand-and-supply.md#prioritize-orders).  

La demanda también puede ser negativa. Tratar la demanda negativa como oferta. Sin embargo, a diferencia de la oferta típica, la demanda negativa se considera oferta fija. El sistema de planificación puede tenerla en cuenta, pero no sugerirá cambios.  

En general, el sistema de planificación considera todos los pedidos de aprovisionamiento posteriores a la fecha de inicio de la planificación como sujetos a cambios para cubrir la demanda. No obstante, después de que una cantidad se registra a partir de un pedido de aprovisionamiento, no la puede modificar el sistema de planificación. Los siguientes pedidos no se pueden replanificar:  

* Órdenes de producción lanzadas donde se ha registrado la salida o el consumo.  
* Pedidos de ensamblado donde se ha registrado la salida o el consumo.  
* Pedidos de transferencia donde se ha registrado el envío.  
* Pedidos de compra en los que se ha registrado la recepción.  

Aparte de cargar los tipos de oferta y demanda, se cargan determinados tipos respetando reglas especiales y dependencias. Las siguientes secciones de este artículo describen estas reglas y dependencias.  

### <a name="item-dimensions-are-separated" />Las dimensiones de producto están separadas

El plan de suministro se debe calcular para cada combinación de dimensiones de producto, como variante y ubicación. Solo es necesario calcular las combinaciones con una necesidad de demanda o de suministro.  

El sistema de planificación busca combinaciones en el perfil de inventario. Cuando encuentra una nueva combinación, crea un registro de control interno que contiene la información sobre la combinación. El sistema de planificación, a continuación, inserta la UA como el registro de control, o bucle externo. Como resultado, se establecen los parámetros de planificación adecuados según una combinación de variante y almacén, y el sistema puede proceder con el bucle interno. 

> [!NOTE]  
> No tiene que introducir un registro de SKU al introducir la demanda o el suministro de una determinada combinación de variante y ubicación. Por lo tanto, si no existe una SKU para una combinación determinada, [!INCLUDE [prod_short](includes/prod_short.md)] crea un registro de SKU temporal según los datos del producto. Si el control de alternancia **Almacén obligatorio** se establece en Sí en la **página de configuración del inventario**, se debe crear una SKU o bien el control de alternancia de **componentes en el almacén** debe definirse en Sí. Obtenga información en [Planificación con o sin almacenes](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level" />Los números de serie y de lote se cargan por nivel de especificación

Los números de serie o lote se cargan en los perfiles de inventario, junto con la oferta y demanda a los que están asignados.  

Los atributos de oferta y demanda se organizan por prioridad de pedido y por el nivel de especificación. Debido a que las coincidencias de números de serie y de lote reflejan el nivel de especificación, una demanda más específica coincidirá antes que una demanda menos específica. Por ejemplo, una demanda específica podría ser un número de lote especificado para una línea de venta. Una demanda menos específica podría ser una venta de cualquier número de lote.

> [!NOTE]  
> Las únicas reglas de prioridades exclusivas para la oferta y demanda con números de serie y de lote, son el nivel de especificación definido por sus combinaciones y la configuración de seguimiento de producto de los productos.  

Durante el ajuste, el sistema de planificación considera inflexible el suministro que tiene números de serie y de lote. El sistema no aumentará ni reprogramará dichas órdenes de suministro. La única excepción a esto es si se utilizan en una relación de pedido a pedido. Obtenga más información en [Los enlaces de pedido a pedido nunca se rompen](#order-to-order-links-are-never-broken). Esta excepción protege el suministro frente a la recepción varios mensajes de acción, posiblemente en conflicto, cuando tiene atributos variables. Por ejemplo, los atributos variables pueden ser cuando el suministro tiene una colección de números de serie diferentes.  

Otra razón por la que el suministro de números de serie y de lote es inflexible es que los números de serie y de lote a menudo se asignan tarde en el proceso. Podría ser confuso si se sugieren cambios en ese punto.  

El balance de números de serie y de lote no respeta la regla de no planificar nada antes de la fecha de inicio de la planificación. Si la oferta y la demanda no se sincronizan, el sistema de planificación sugerirá cambios o nuevos pedidos, independientemente de la fecha de inicio de la planificación.  

### <a name="order-to-order-links-are-never-broken" />Las conexiones de pedido contra pedido nunca se rompen

Al planificar un producto de pedido contra pedido, el suministro vinculado solo se debe usar para lo que se pensó originalmente. La demanda vinculada no se debe cubrir con otra oferta, incluso si la oferta está disponible en cuanto a tiempo y a cantidad. Por ejemplo, no se puede utilizar para cubrir otra demanda un pedido de ensamblado vinculado a un pedido de venta en un caso de ensamblado para pedido.  

La oferta y demanda de pedido contra pedido se deben equilibrar de forma precisa. El sistema de planificación garantizará el suministro sin tener en cuenta los parámetros de tamaño de pedido, los modificadores y las cantidades en el inventario (aparte de las cantidades relacionadas con los pedidos vinculados). Por el mismo motivo, el sistema sugiere disminuir aprovisionamientos en exceso si se disminuye la demanda vinculada.  

Esta contrapartida también afecta a la temporización. No se considera el horizonte limitado que ofrece el ciclo; el suministro se reprogramará si ha cambiado el plazo de la demanda. No obstante, el tiempo de amortiguación se respetará e impedirá que los aprovisionamientos de pedido a pedido no entren en el programa, excepto en el caso de aprovisionamientos internos de una orden de producción de varios niveles (orden de proyecto).  

> [!NOTE]  
> Los números de serie y de lote también se pueden especificar en la demanda de pedido contra pedido. En ese caso, el aprovisionamiento no es inflexible, como normalmente sucede con números de serie y de lote. En este caso, el programa aumentará o disminuirá según los cambios en la demanda. Además, si una demanda tiene distintos números de serie o de lote, por ejemplo más de un número de lote, se sugerirá un pedido de aprovisionamiento para cada lote.  

> [!NOTE]  
> Las previsiones no deben llevar a crear pedidos de aprovisionamiento limitados por un vínculo de pedido a pedido. Si se usa la previsión, solo debe hacerse como generador de una demanda dependiente en un entorno de fabricación.

### <a name="component-need-is-loaded-according-to-production-order-changes" />La necesidad de componente se carga según los cambios de la orden de producción

Al manipular las órdenes de producción, el sistema de planificación debe supervisar los componentes necesarios antes de cargarlos en el perfil de demanda. Las líneas de componente resultantes de una orden de producción cambiada reemplazarán las líneas del pedido original. El cambio garantiza que el sistema de planificación no duplica las líneas de planificación para una necesidad de componentes.  

### <a name="consume-safety-stock" />Consumir el stock de seguridad

El stock de seguridad es una demanda que se carga en el perfil de inventario en la fecha inicial de la planificación.  

El stock de seguridad es una cantidad de inventario que se aparta para satisfacer las incertidumbres en la demanda durante el plazo de reposición. Sin embargo, se puede consumir para satisfacer una demanda. En ese caso, el sistema de planificación garantizará que el stock de seguridad se reponga rápidamente. El sistema sugiere una orden de suministro para reponer la cantidad de existencias de seguridad en la fecha en que se consume. La línea de planificación mostrará un icono de advertencia de excepción explicando que el stock de seguridad se ha consumido parcialmente o en su totalidad a través de un pedido de excepción para la cantidad que falta.  

### <a name="forecast-demand-is-reduced-by-sales-orders" />Los pedidos de ventas reducen la demanda de previsión

Las previsiones de demanda expresan la demanda futura prevista. Mientras se introduce la demanda real, normalmente como pedidos de venta para productos fabricados, se consume la previsión.

El pronóstico en sí no se reduce por las órdenes de venta. No obstante, las cantidades de previsión que se usan en el cálculo de la planificación se reducen (por las cantidades del pedido de venta) antes de que la cantidad pendiente entre en el perfil de demanda. Para las ventas durante un período, la planificación incluye tanto las órdenes de venta abiertas como los asientos de artículos de las ventas enviadas. La excepción a esta regla es cuando provienen de un pedido general.  

Debe definir un período de pronóstico válido. La fecha de la cantidad prevista define el comienzo del periodo y la fecha de la previsión siguiente define el final del periodo.  

No se usa la previsión para periodos anteriores al periodo de planificación, independientemente de si se ha consumido. La primera cifra de previsión que interesa es la fecha de inicio de la planificación o la fecha más próxima.  

La previsión puede ser para diferentes tipos de demanda:

* Demanda independiente, como pedidos de venta
* Demanda dependiente, como componentes de órdenes de producción.

Un producto puede tener los dos tipos de previsión. Durante la planificación, el consumo se realiza por separado, primero para la demanda independiente y después para la demanda dependiente.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders" />Los pedidos de venta reducen la demanda del pedido abierto

La previsión se complementa con los pedidos de venta abiertos como una forma de especificar la demanda futura de un cliente específico. Como con la previsión (sin especificar), las ventas reales deberán consumir la demanda prevista, y la cantidad pendiente deberá corresponder al perfil de inventario de demanda. El consumo no reduce realmente la cantidad del pedido de venta abierto.

El cálculo de planificación incluye los pedidos de venta abiertos vinculados a la línea de pedido abierto específica, pero no incluye ningún periodo de tiempo válido. Tampoco incluye los pedidos registrados, porque el procedimiento de registro ya ha reducido la cantidad pendiente del pedido abierto.

## <a name="prioritize-orders" />Prioridad de pedidos

Dentro de un SKU dado, la fecha solicitada o disponible representa la prioridad más alta. La demanda de hoy debe ser atendida antes que la demanda de la próxima semana. Pero, además de esta prioridad global, el sistema de planificación hará las siguientes sugerencias según las prioridades de orden:

* Qué tipo de demanda debe cumplir primero.
* El origen de suministro que se debe aplicar antes de aplicar otros orígenes de suministro.  

La oferta y demanda cargadas contribuyen a un perfil del inventario proyectado según las prioridades.  

### <a name="priorities-on-the-demand-side" />Prioridades en la demanda

1. Ya enviado: movimiento de producto  
2. Pedido dev. compra  
3. Pedido de venta  
4. Pedido servicio  
5. Necesidades de componentes de producción  
6. Línea de pedido de ensamblado  
7. Pedido de transferencia de salida  
8. Pedido abierto (que no ha sido consumido todavía por los pedidos de venta relacionados)  
9. Previsión (que no han consumido aún otros pedidos de venta)  

> [!NOTE]  
> Las devoluciones de compras normalmente no intervienen en la planificación de suministros; siempre se deben reservar del lote que se va a devolver. Si no reserva, las devoluciones de compra desempeñan una función en la disponibilidad y se les da una elevada prioridad para evitar que el sistema de planificación sugiera un pedido de aprovisionamiento solo para servir a una devolución de compra.  

### <a name="priorities-on-the-supply-side" />Prioridades en el suministro

1. Ya en el inventario: movimiento de producto (flexibilidad de planificación = ninguna)  
2. Pedido de devolución de venta (flexibilidad de planificación = ninguna)  
3. Pedido de transferencia de entrada  
4. Orden de producción  
5. Pedido de ensamblado  
6. Pedido de compra  

### <a name="priority-related-to-the-state-of-supply-and-demand" />Prioridad relacionada con el estado de la oferfta y la demanda

Además de las prioridades del tipo de oferta y demanda, hay otras cosas que afectan la flexibilidad de planificación. Por ejemplo, las actividades del almacén y el estado de los siguientes pedidos:

* Venta
* Compra
* Transferencia
* Ensamblado
* Producción

El estado de estas órdenes tiene los siguientes efectos: 

1. Parcialmente controlado (flexibilidad de planificación = ninguna)  
2. Ya en proceso en el almacén (flexibilidad de planificación = ninguna)  
3. Lanzados: todos los tipos de pedido (flexibilidad de planificación = ilimitada)  
4. Orden de producción planificada en firme (flexibilidad de planificación = ilimitada)  
5. Planificado/Abierto: todos los tipos de pedido (flexibilidad de planificación = ilimitada)

## <a name="balancing-supply-with-demand" />Equilibrio de oferta y demanda

El sistema de planificación equilibra la oferta y la demanda sugiriendo acciones para revisar las órdenes de suministro que no están equilibradas. Este equilibrio ocurre para cada combinación de variante y ubicación.  

Imagine que cada perfil de inventario contiene dos cadenas:

* Una cadena de eventos de demanda, ordenados por fecha y prioridad
* Una cadena correspondiente de eventos de suministro

Cada evento hace referencia a su tipo e identificación de origen. Las reglas para el equilibrio del producto son sencillas. La coincidencia entre oferta y demanda puede darse en cualquier momento del proceso, como se muestra aquí:  

1. No hay demanda ni aprovisionamiento para el producto => la planificación ha terminado (o no debe iniciarse).  
2. Hay demanda pero no hay aprovisionamiento => el aprovisionamiento debe ser sugerido.  
3. Hay aprovisionamiento pero no hay demanda para él => el aprovisionamiento debe ser cancelado.  
4. Hay tanto demanda como oferta => debe haber preguntas y respuestas para que [!INCLUDE [prod_short](includes/prod_short.md)] pueda garantizar que la oferta puede satisfacer la demanda.

    Si el momento de aprovisionamiento no resulta adecuado, probablemente el aprovisionamiento pueda volver a programarse de la siguiente forma:  

    1. Si el aprovisionamiento es anterior a la demanda, probablemente el aprovisionamiento se puede programar fuera para que el inventario sea lo más bajo posible.  
    2. Si el aprovisionamiento es posterior a la demanda, probablemente el aprovisionamiento se puede volver a programar en el futuro. Si no, el programa sugiere un nuevo aprovisionamiento.  
    3. Si el aprovisionamiento cubre la demanda en la fecha, el sistema de planificación puede investigar si la cantidad de aprovisionamiento puede cubrir la demanda.  

    Cuando se ha aplicado el plan, la cantidad que se suministrará se puede calcular del siguiente modo:  

    1. Si la cantidad de aprovisionamiento es menor que la demanda, la cantidad de aprovisionamiento puede incrementarse (o no, si tiene una directiva de cantidad máxima).  
    2. Si la cantidad de aprovisionamiento es mayor que la demanda, la cantidad de aprovisionamiento puede reducirse (o no, si tiene una directiva de cantidad mínima).  

    En este punto se da una de estas dos situaciones:  

    1. Se puede satisfacer la demanda actual, en cuyo caso se puede cerrar y se puede iniciar la planificación de la demanda siguiente.  
    2. El suministro ha alcanzado el máximo, dejando parte de la cantidad de demanda sin cubrir. En este caso, el sistema de planificación puede cerrar el aprovisionamiento actual y proceder con el siguiente.  

 El procedimiento comienza de nuevo con la demanda siguiente y el suministro actual, o viceversa. El suministro actual también puede cubrir esta demanda siguiente, o la demanda actual no se ha cubierto por completo.  

### <a name="rules-for-actions-for-supply-events" />Reglas de acciones para los eventos de oferta

Para los cálculos de arriba hacia abajo en los que la oferta debe satisfacer la demanda, la demanda se toma como un dato. Está fuera del control del sistema de planificación. Sin embargo, el sistema de planificación puede administrar el lado de la oferta y hará las siguientes sugerencias:

* Crear nuevos pedidos de suministros
* Reprogramar pedidos existentes o cambiar sus cantidades
* Cancelar pedidos de suministros que ya no se necesitan  

Para excluir un pedido de suministro existente de las sugerencias de planificación, puede indicar que no tiene flexibilidad de planificación (flexibilidad de planificación = ninguna). A continuación, el exceso de suministro del pedido se usará para satisfacer la demanda, pero no se sugerirá ninguna acción. 

En general, todo el aprovisionamiento tiene una flexibilidad de planificación limitada por las condiciones de cada una de las acciones sugeridas.  

* **Reprogramar fuera**: fecha de un pedido de suministro existente que se puede excluir de la programación para cumplir la fecha de vencimiento de demanda a menos que:

  * Representa el inventario (siempre en el día cero).  
  * Tiene una directiva pedido a pedido vinculada a otra demanda.  
  * Está fuera de la ventana para reprogramar en el intervalo de tiempo.
  * Hay un suministro más aproximado que se podría usar.  
  * Por otro lado, el usuario puede decidir no reprogramar porque:
  * El pedido de suministro se vincula a otra demanda en una fecha anterior.  
  * La reprogramación necesaria es tan mínima que se considera insignificante.  

* **Reprogramar dentro**: fecha de un pedido de suministro existente que se puede incluir en la programación, excepto en las condiciones siguientes:

  * Está vinculada directamente a otra demanda.  
  * Está fuera de la ventana para reprogramar definida en el intervalo de tiempo.

> [!NOTE]  
> Al planificar un producto con un punto de pedido, puede programar el pedido de suministro si es necesario. Esto a menudo sucede en los pedidos de suministro con programación anticipada que se activan mediante un punto de pedido.

* **Aumentar cantidad**: la cantidad de un pedido de aprovisionamiento existente se puede aumentar para satisfacer la demanda, a menos que los pedidos de aprovisionamiento estén conectados directamente con una demanda por un vínculo de pedido a pedido.  

> [!NOTE]  
> Aunque puede aumentar el pedido de aprovisionamiento, el aumento podría quedar limitado por una cantidad máxima de pedido definida.  

* **Disminución de cantidad**: los pedidos de aprovisionamiento existentes con excedente en comparación con una demanda existente se pueden disminuir para satisfacer la demanda.  

> [!NOTE]  
> Aunque la cantidad se puede disminuir, podrían quedar excedentes en comparación con la demanda porque haya una cantidad mínima de pedido definida o un múltiplo de pedido. 

* **Cancelar**: como incidente especial de la acción de disminución de cantidad, el pedido de aprovisionamiento puede cancelarse si se ha reducido a cero. 
* **Nuevo**: si no hay pedidos de suministro, o no se puede cambiar uno existente para satisfacer la cantidad necesaria en la fecha de vencimiento de la demanda, se sugiere un nuevo pedido de suministro.  

### <a name="determine-the-supply-quantity" />Determinar la cantidad de aprovisionamiento

Usted define los parámetros de planificación que controlan la cantidad sugerida de cada pedido de suministro.  

Cuando el sistema de planificación calcula la cantidad de un nuevo pedido de suministro o la cantidad para cambiar en un pedido existente, la cantidad sugerida podría ser distinta de la demanda real.  

Si se seleccionan un inventario máximo o cantidads de pedido fijas, la cantidad sugerida podría aumentar para coincidir con la cantidad fija o ese inventario máximo. Si una directiva de reaprovisionamiento utiliza una punto de pedido, la cantidad se puede aumentar para llegar al menos al punto de pedido. 

La cantidad sugerida podría modificarse en esta secuencia:  

1. Hasta la cantidad de pedido máxima.  
2. Hasta la cantidad de pedido mínima.  
3. Hasta cumplir el múltiplo de pedido más próximo.

### <a name="order-tracking-links-during-planning" />Conexiones de seguimiento de pedidos durante la planificación

Para el seguimiento de pedidos durante la planificación, el sistema de planificación reorganiza los vínculos de seguimiento de pedidos para las combinaciones de producto, variante o almacén. El sistema reorganiza los enlaces de seguimiento por las siguientes razones:

* Verificar sus sugerencias para cubrir toda la demanda y asegurarse de que se necesitan todas las órdenes de suministro.  
* Los enlaces de seguimiento de pedidos deben reequilibrarse periódicamente.  

Con el tiempo, los enlaces de seguimiento de pedidos se desequilibran. Las conexiones se descuadran porque la red completa de seguimiento de pedidos no se reorganiza hasta que un evento de demanda o de suministro se cierre realmente.

Antes de cuadrar el aprovisionamiento por la demanda, el sistema de planificación elimina todos los vínculos de seguimiento de pedidos existentes. Durante el procedimiento de contrapartida, cuando se cierra un evento demanda o de suministro, crea nuevos vínculos de seguimiento de pedidos entre la demanda y la oferta.  

> [!NOTE]  
> Aunque el producto no se haya configurado para seguimiento dinámico de pedidos, el sistema de planificación establecerá vínculos de seguimiento de pedidos equilibrados.

## <a name="close-balanced-supply-and-demand" />Cerrar la oferta y demanda equilibradas

Equilibrar la oferta tiene tres resultados posibles:

* Se cumplen la cantidad necesaria y la fecha de los eventos de demanda y se puede cerrar la planificación de ellos. El evento de suministro permanece abierto y podría cubrir la próxima demanda. Al mantener el evento de suministro abierto, permite que el procedimiento de equilibrado empiece con el evento de oferta actual y la siguiente demanda.  
* El pedido de suministro no se puede modificar para cubrir toda la demanda. El evento de demanda sigue abierto, con una cantidad sin cubrir que se podría cubrir mediante el evento de suministro siguiente. Por lo tanto, se cierra el evento de suministro y el equilibrado puede empezar con la demanda actual y el siguiente evento de suministro.  
* Se ha cubierto toda la demanda y no hay demanda siguiente (o no ha habido demanda en absoluto). El aprovisionamiento excedente se podría reducir (o cancelar) y después cerrar. Cualquier otro evento de suministro también debe cancelarse.  

Por último, el sistema de planificación creará una conexión de seguimiento de pedidos entre el suministro y la demanda.  

### <a name="create-the-planning-line-suggested-action" />Crear la línea de planificación (acción sugerida)

Si se sugiere alguna acción (**nueva**, **cambiar de cantidad**, **reprogramar**, **reprogramar y cambiar de cantidad** o **cancelar**) para revisar el pedido de aprovisionamiento, el sistema de planificación crea una línea de planificación en la hoja de trabajo de planificación. Para el seguimiento de pedidos, la línea de planificación se crea no solo cuando se cierra el evento de suministro, sino también si se cierra el evento de demanda. Esto es así aunque el evento de suministro aún esté abierto y podría cambiarse cuando se procese el siguiente evento de demanda. La línea de planificación se puede modificar de nuevo cuando se crea.

Para reducir la carga en la base de datos al manejar órdenes de producción, la línea de planificación se puede actualizar en tres niveles:

* Crear solo la línea de planificación con la fecha de vencimiento y la cantidad actuales, pero sin la ruta y los componentes.  
* Incluir ruta: la ruta planificada incluye el cálculo de las fechas y las horas de inicio y fin. Incluir la ruta exige muchos accesos a la base de datos. Para determinar las fechas finales y de vencimiento, podría ser necesario calcular la ruta aunque el evento de suministro no se haya cerrado. Por ejemplo, si está programando hacia adelante.  
* Incluir despliegue de L.M.: puede suceder justo antes de cerrar el evento de aprovisionamiento.

## <a name="see-also" />Consulte también

[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)  
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
