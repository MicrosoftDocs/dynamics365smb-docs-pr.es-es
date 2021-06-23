---
title: 'Detalles de diseño: Equilibrado de aprovisionamiento y demanda | Documentos de Microsoft'
description: Para saber cómo funciona el sistema de planificación, es necesario conocer los objetivos con prioridad del sistema de planificación, los más importantes de los cuales son asegurarse de que las demandas se satisfagan con suficiente suministro y de que los suministros tengan un propósito.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 05e812ab11a831ac1c2d96d506489527f06142a2
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215533"
---
# <a name="design-details-balancing-demand-and-supply"></a>Detalles de diseño: Equilibrio de aprovisionamiento y demanda
Para saber cómo funciona el sistema de planificación, es necesario conocer los objetivos con prioridad del sistema de planificación, los más importantes de los cuales son asegurarse de que:  

- La demanda se satisfará con suficiente aprovisionamiento.  
- Los aprovisionamientos sirven todos a un fin.  

 En general, estos objetivos se logran equilibrando el aprovisionamiento con la demanda.  

## <a name="demand-and-supply"></a>Aprovisionamiento y demanda
 "Demanda" es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción. Además, la aplicación permite tipos de demanda más técnicos, como inventario negativo y devoluciones de compra.  

  Suministro es el término habitual que se usa para cualquier tipo de cantidad positiva o de entrada, como inventario, compras, ensamblado, producción o transferencias de entrada. Además, una devolución de ventas también puede representar un aprovisionamiento.  

  Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario. Un perfil contiene eventos de demanda y el otro incluye los eventos de suministro correspondientes. Cada evento representa una entidad de red de pedidos, como una línea de pedido de venta, un movimiento de producto o una línea de orden de producción.  

  Cuando se cargan los perfiles de inventario, se equilibran los distintos conjuntos de demanda-suministro para generar un plan de suministro que cumpla los objetivos enumerados.  

  Los parámetros de planificación y los niveles de inventario son otros tipos de demanda y suministro respectivamente, en los que se realizará una contrapartida integrada para reponer los productos en existencias. Para obtener más información, consulte [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Concepto de contrapartida en resumen
  La demanda la proporcionan los clientes de una empresa. El suministro es lo que puede crear y eliminar la empresa para establecer el equilibrio. El sistema de planificación se inicia con la demanda independiente y, a continuación, vuelve hacia el suministro.  

   Los perfiles de inventario se usan para incluir información acerca de las demandas y suministros, cantidades y plazos. Esencialmente, estos perfiles constituyen los dos lados de la escala de contrapartida.  

   El objetivo del mecanismo de planificación es contrarrestar la demanda y el suministro de un producto para garantizar que el suministro corresponderá a la demanda de una forma factible, según lo definido por los parámetros y las reglas de planificación.  

   ![Resumen del equilibrio entre la oferta y la demanda](media/nav_app_supply_planning_2_balancing.png "Resumen del equilibrio entre la oferta y la demanda")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Gestión de pedidos antes de la fecha de inicio de planificación
Para evitar que un plan de suministro muestre sugerencias imposibles y, por tanto, de poca utilidad, el sistema de planificación considera el periodo hasta la fecha inicial como una zona congelada donde no hay nada planificado. La regla siguiente se aplica a la zona congelada:  

Toda la demanda y aprovisionamiento antes de la fecha de inicio del periodo de planificación se tendrá como parte del inventario o enviado.  

Por consiguiente, el sistema de planificación, salvo algunas excepciones, no sugerirá ningún cambio en los pedidos de aprovisionamiento en la zona congelada, y no se creará ni se guardará ningún vínculo de seguimiento de pedidos para ese periodo.  

Las excepciones a esta regla son las siguientes:  

   * Si el inventario disponible proyectado, incluida la suma de aprovisionamiento y la demanda en la zona congelada, es menor que cero.  
   * Si hacen falta números de serie o lote en los pedidos con fecha anterior.  
   * Si el conjunto de aprovisionamiento y demanda se vincula por una directiva de pedido a pedido.  

Si el inventario disponible inicial es menor que cero, el sistema de planificación sugiere un pedido de aprovisionamiento de emergencia el día antes del periodo de planificación para cubrir la cantidad que falta. Por tanto, el inventario proyectado y disponible será siempre al menos cero cuando empiece la planificación para el periodo futuro. La línea de planificación de este pedido de suministro mostrará un icono de advertencia de emergencia y, tras la búsqueda, se proporciona información adicional.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Los números de serie y de lote y las conexiones de pedido contra pedido están exentos de la zona congelada  
   Si se requieren números de serie y de lote o si hay un vínculo de pedido a pedido, el sistema de planificación no tendrá en cuenta la zona congelada e incorporará estas cantidades con fecha anterior a partir de la fecha de inicio y potencialmente propondrá acciones correctivas si la demanda y el aprovisionamiento no están sincronizados. El motivo empresarial de este principio es que dichos conjuntos de demanda-suministro específicos deben coincidir para garantizar que se cumple esta demanda específica.

## <a name="loading-the-inventory-profiles"></a>Carga de los perfiles de inventario
Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario.  

Los tipos normales de demanda y suministro con fechas de fecha de vencimiento en la fecha inicial de planificación se cargan en cada perfil de inventario. Cuando se cargan, los distintos tipos de demanda y de suministro se ordenan según las prioridades generales, como la fecha de vencimiento, los códigos de bajo nivel, la ubicación y la variante. Además, se aplican prioridades de pedido a los diversos tipos para garantizar que primero se satisfaga la demanda más importante. Para obtener más información, consulte [Priorizar pedidos](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Como se indicaba anteriormente, la demanda también podría ser negativa. Esto significa que se debe tratar como suministro; no obstante, a diferencia de los tipos de suministro normales, la demanda negativa se considera suministro fijo. El sistema de planificación puede tenerla en cuenta, pero no sugerirá cambios.  

En general, el sistema de planificación considera todos los pedidos de aprovisionamiento posteriores a la fecha de inicio de la planificación como sujetos a cambios para cubrir la demanda. No obstante, en cuanto una cantidad se registra a partir de un pedido de aprovisionamiento, ya no la puede modificar el sistema de planificación. Por consiguiente, los diferentes pedidos siguientes no se pueden replanificar:  

- Órdenes de producción lanzadas donde se ha registrado la salida o el consumo.  
- Pedidos de ensamblado donde se ha registrado la salida o el consumo.  
- Pedidos de transferencia donde se ha registrado el envío.  
- Pedidos de compra en los que se ha registrado la recepción.  

Aparte de cargar los tipos de demanda y aprovisionamiento, se cargan determinados tipos respetando reglas especiales y dependencias, las cuales que se describen a continuación.  

### <a name="item-dimensions-are-separated"></a>Las dimensiones de producto están separadas  
El plan de suministro se debe calcular mediante la combinación de dimensiones de producto, como variante y ubicación. No obstante, no hay razón para calcular ninguna combinación teórica. Solo es necesario calcular las combinaciones con una necesidad de demanda o de suministro.  

El sistema de planificación lo controla mediante la ejecución a través del perfil de inventario. Cuando se encuentra una nueva combinación, la aplicación crea un registro de control interno que contiene la información de combinación real. La aplicación inserta la UA como el registro de control, o bucle externo. Como resultado, se establecerán los parámetros de planificación adecuados según una combinación de variante y almacén, y la aplicación podrá proceder al bucle interno.  

> [!NOTE]  
>  La aplicación no requiere que el usuario introduzca un registro de UA al introducir la demanda o el suministro de una determinada combinación de variante y ubicación. Por lo tanto, si no exista una UA para una combinación determinada, la aplicación crea su propio registro de UA temporal según los datos de la ficha de producto. Si Almacén obligatorio se establece en Sí en la página de configuración del inventario, se debe crear una UA o bien los componentes en el almacén deben definirse en Sí. Para obtener más información, consulte [Detalles de diseño: Demanda en almacén vacío](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Los números de serie y de lote se cargan por nivel de especificación  
Los atributos en forma de números de serie o lote se cargan en los perfiles de inventario, junto con la demanda y el aprovisionamiento a los que están asignados.  

Los atributos de demanda y aprovisionamiento se organizan por prioridad de pedido, así como por el nivel de especificación. Dado que las coincidencias de número de serie o de lote reflejan el nivel de especificación, la demanda más específica, como un número de lote seleccionado específicamente para una línea de venta, buscará una coincidencia antes que una demanda menos específica, por ejemplo una venta de cualquier número de lote seleccionado.  

> [!NOTE]  
>  No existen reglas de prioridades exclusivas para demanda y suministro con números de serie y de lote, aparte del nivel de especificación definido por sus combinaciones de números de serie y de lote, y la configuración de seguimiento de producto de los productos que intervienen.  

Durante el proceso de equilibrado, el sistema de planificación toma los números de serie y de lote inflexibles y no intenta ni aumentar ni reprogramar estos pedidos de aprovisionamiento (a menos que se utilicen en una relación de pedido a pedido). Vea Las conexiones de pedido contra pedido nunca se rompen). De este modo se protege el suministro frente a la recepción varios mensajes de acción, posiblemente en conflicto, cuando un suministro tiene atributos variables, como, por ejemplo, una colección de números de serie distintos.  

Otra razón por la que el aprovisionamiento de números de serie y de lote no es flexible es que los números de serie y de lote generalmente se asignan tan tarde en el proceso que resultaría confuso si se sugirieran cambios.  

La contrapartida de números de serie o de lote no respeta la *zona congelada*. Si la demanda y el aprovisionamiento no se sincroniza, el sistema de planificación sugerirá cambios o sugerirá nuevos pedidos, independientemente de la fecha de inicio de la planificación.  

### <a name="order-to-order-links-are-never-broken"></a>Las conexiones de pedido contra pedido nunca se rompen  
Al planificar un producto de pedido contra pedido, el suministro vinculado no se debe usar para ninguna otra demanda que para la que se ha pensado originalmente. La demanda vinculada no se debe cubrir con otro suministro aleatorio, incluso si, en la situación actual, está disponible en cuanto a tiempo y a cantidad. Por ejemplo, no se podrá utilizar para cubrir otra demanda un pedido de ensamblado vinculado a un pedido de venta en un caso de ensamblado para pedido.  

La demanda y el suministro de pedido contra pedido se deben equilibrar de forma precisa. El sistema de planificación garantizará el suministro en todas las situaciones sin tener en cuenta los parámetros de tamaño de pedido, los modificadores y las cantidades en el inventario (aparte de las cantidades relacionadas con los pedidos vinculados). Por el mismo motivo, el sistema sugiere disminuir aprovisionamientos en exceso si se disminuye la demanda vinculada.  

Esta contrapartida también afecta a la temporización. No se considera el horizonte limitado que ofrece el ciclo; el suministro se reprogramará si ha cambiado el plazo de la demanda. No obstante, el tiempo de amortiguación se respetará e impedirá que los aprovisionamientos de pedido a pedido no entren en el programa, excepto en el caso de aprovisionamientos internos de una orden de producción de varios niveles (orden de proyecto).  

> [!NOTE]  
>  Los números de serie y de lote también se pueden especificar en la demanda de pedido contra pedido. En ese caso, el aprovisionamiento no es inflexible de forma predeterminada, como generalmente sucede con números de serie y de lote. En este caso, el programa aumentará o disminuirá según los cambios en la demanda. Además, si una demanda lleva distintos números de serie o de lote, por ejemplo más de un número de lote, se sugerirá un pedido de aprovisionamiento por lote.  

> [!NOTE]  
>  Las previsiones no deben llevar a crear pedidos de aprovisionamiento limitados por un vínculo de pedido a pedido. Si se usa la previsión, solo debe hacerse como generador de una demanda dependiente en un entorno de fabricación.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>La necesidad de componente se carga según los cambios de la orden de producción  
Al manipular las órdenes de producción, el sistema de planificación debe supervisar los componentes necesarios antes de cargarlos en el perfil de demanda. Las líneas de componente resultantes de una orden de producción modificada reemplazarán las del pedido original. De este modo se garantiza que el sistema de planificación establece que nunca se dupliquen las líneas de planificación de la necesidad de componentes.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> El stock de seguridad se puede consumir  
El stock de seguridad es, principalmente, un tipo de demanda y, por lo tanto, se carga en el perfil de inventario en la fecha inicial de la planificación.  

El stock de seguridad es una cantidad que se aparta para compensar las incertidumbres en la demanda durante el plazo de reposición. No obstante, se pueden consumir si es necesario para cubrir una demanda. En dicho caso, el programa de planificación garantizaría que el stock de seguridad se sustituye rápidamente sugiriendo un pedido de aprovisionamiento para abastecer la cantidad de stock de seguridad en la fecha en la que se consume. Esta línea de planificación mostrará un icono de advertencia de excepción explicando al planificador que el stock de seguridad se ha consumido parcialmente o en su totalidad a través de un pedido de excepción para la cantidad que falta.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Los pedidos de ventas reducen la demanda de previsión  
La previsión de demanda expresa la demanda futura prevista. Mientras se introduce la demanda real, normalmente como pedidos de venta para productos fabricados, se consume la previsión.  

La previsión no se reduce realmente por los pedidos de venta; permanece igual. No obstante, las cantidades de previsión utilizadas en el cálculo de la planificación se reducen (por las cantidades del pedido de venta) antes de que la cantidad pendiente, si la hubiera, entre en el perfil del inventario de demanda. Cuando el sistema de planificación examina las ventas reales durante un periodo, se incluyen los pedidos de venta abiertos y los movimientos de producto de las ventas enviadas, a menos que se deriven de un pedido abierto.  

Un usuario debe definir un periodo válido de previsión. La fecha de la cantidad prevista define el comienzo del periodo y la fecha de la previsión siguiente define el final del periodo.  

No se usa la previsión para periodos anteriores al periodo de planificación, independientemente de si se ha consumido o no. La primera cifra de previsión que interesa es la fecha de inicio de la planificación o la fecha anterior más próxima.  

La previsión puede ser de demanda independiente, como pedidos de venta, o de demanda dependiente, como los componentes de orden de producción (módulo - previsión). Un producto puede tener los dos tipos de previsión. Durante la planificación, el consumo se realiza por separado, primero para la demanda independiente y después para la demanda dependiente.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Los pedidos de venta reducen la demanda del pedido abierto  
La previsión se complementa con el pedido de venta abierto para especificar la demanda futura de un cliente específico. Como con la previsión (sin especificar), las ventas reales deberán consumir la demanda prevista, y la cantidad pendiente deberá corresponder al perfil de inventario de demanda. Una vez, más el consumo no reduce realmente el pedido abierto.  

El cálculo de planificación tiene en cuenta los pedidos de venta abiertos vinculados a la línea de pedido abierto específica, pero no tiene en cuenta ningún periodo de tiempo válido. Ni tiene en cuenta los pedidos registrados, debido a que el procedimiento de registro ya ha reducido la cantidad pendiente del pedido abierto.

## <a name="prioritizing-orders"></a>Prioridad de pedidos
En una UA concreta, la fecha solicitada o disponible representa la máxima prioridad; la demanda de hoy se debe tratar antes que la de la semana que viene. Pero además de esta prioridad general, el sistema de planificación sugerirá también el tipo de demanda que debe ser satisfecho antes de cubrir otra demanda. Del mismo modo, sugerirá el origen de suministro que se debe aplicar antes de aplicar otros orígenes de suministro. Esto se realice según las prioridades de pedido.  

La demanda y el suministro cargados contribuyen a un perfil del inventario proyectado según las prioridades siguientes:  

### <a name="priorities-on-the-demand-side"></a>Prioridades en la demanda  
1. Ya enviado: movimiento de producto  
2. Pedido devolución compra  
3. Pedido venta  
4. Pedido servicio  
5. Necesidad de componentes de producción  
6. Línea de pedido ensamblado  
7. Pedido de transferencia de salida  
8. Pedido abierto (que no ha sido consumido todavía por los pedidos de venta relacionados)  
9. Previsión (que no han consumido aún otros pedidos de venta)  

> [!NOTE]  
>  Las devoluciones de compras normalmente no intervienen en la planificación de suministros; siempre se deben reservar del lote que se va a devolver. Si no reserva, las devoluciones de compra desempeñan una función en la disponibilidad y se les da una elevada prioridad para evitar que el sistema de planificación sugiera un pedido de aprovisionamiento solo para servir a una devolución de compra.  

### <a name="priorities-on-the-supply-side"></a>Prioridades en el suministro  
1. Ya en el inventario: movimiento de producto (flexibilidad de planificación = ninguna)  
2. Pedido de devolución de venta (flexibilidad de planificación = ninguna)  
3. Pedido de transferencia de entrada  
4. Orden producción  
5. Pedido de ensamblado  
6. Pedido compra  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioridad relacionada con el estado de la demanda y del suministro  
Aparte de las prioridades dadas por el tipo de demanda y aprovisionamiento, el estado actual de los pedidos en el proceso de ejecución también define una prioridad. Por ejemplo, las actividades de almacén repercuten y se tiene en cuenta el estado de los pedidos de ventas, compra, transferencia, ensamblado y órdenes de producción.  

1. Parcialmente controlado (flexibilidad de planificación = ninguna)  
2. Ya en proceso en el almacén (flexibilidad de planificación = ninguna)  
3. Lanzados: todos los tipos de pedido (flexibilidad de planificación = ilimitada)  
4. Orden de producción planificada en firme (flexibilidad de planificación = ilimitada)  
5. Planificado/Abierto: todos los tipos de pedido (flexibilidad de planificación = ilimitada)

## <a name="balancing-supply-with-demand"></a>Equilibrio de aprovisionamiento con demanda
El núcleo del sistema de planificación implica el equilibrio de la demanda y del suministro mediante la sugerencia de acciones de usuario para revisar los pedidos de suministro en caso de que se produzca un desequilibrio. Se produce por la combinación de variante y de ubicación.  

Imagínese que cada perfil de inventario contiene una cadena de eventos de demanda (ordenados por fecha y prioridad) y una cadena correspondiente de eventos de aprovisionamiento. Cada evento hace referencia a su tipo e identificación de origen. Las reglas para la contrapartida del producto son sencillas. Se pueden producir cuatro casos de coincidencia entre aprovisionamiento y demanda en cualquier momento del proceso:  

1. No hay demanda ni aprovisionamiento para el producto => la planificación ha terminado (o no debe iniciarse).  
2. Hay demanda pero no hay aprovisionamiento => el aprovisionamiento debe ser sugerido.  
3. Hay aprovisionamiento pero no hay demanda para él => el aprovisionamiento debe ser cancelado.  
4. Hay tanto demanda como aprovisionamiento=> debe haber preguntas y respuestas para que el sistema pueda garantizar que la demanda se satisfará y que el aprovisionamiento es suficiente.  

    Si el momento de aprovisionamiento no resulta adecuado, probablemente el aprovisionamiento pueda volver a programarse de la siguiente forma:  

    1.  Si el aprovisionamiento es anterior a la demanda, probablemente el aprovisionamiento se puede volver a programar fuera para que el inventario sea lo más bajo posible.  
    2.  Si el aprovisionamiento es posterior a la demanda, probablemente el aprovisionamiento se puede volver a programar dentro. Si no, el programa sugiere un nuevo aprovisionamiento.  
    3.  Si el aprovisionamiento cubre la demanda en la fecha, el sistema de planificación puede proceder a investigar si la cantidad de aprovisionamiento puede cubrir la demanda.  

    Una vez aplicado el plan, la cantidad suficiente que se suministrará se puede calcular del siguiente modo:  

    1.  Si la cantidad de aprovisionamiento es menor que la demanda, es posible que la cantidad de aprovisionamiento pueda incrementarse (o no si está limitada por una directiva de cantidad máxima).  
    2.  Si la cantidad de aprovisionamiento es mayor que la demanda, es posible que la cantidad de aprovisionamiento pueda disminuirse (o no si está limitada por una directiva de cantidad mínima).  

    En este punto se da cualquiera de estas dos situaciones:  

    1.  Se puede satisfacer la demanda actual, en cuyo caso se puede cerrar y se puede iniciar la planificación de la demanda siguiente.  
    2.  El suministro ha alcanzado el máximo, dejando parte de la cantidad de demanda sin cubrir. En este caso, el sistema de planificación puede cerrar el aprovisionamiento actual y proceder con el siguiente.  

 El procedimiento comienza de nuevo con la demanda siguiente y el suministro actual, o viceversa. El suministro actual también puede cubrir esta demanda siguiente, o la demanda actual no se ha cubierto por completo.  

### <a name="rules-concerning-actions-for-supply-events"></a>Reglas relativas a las acciones para los eventos de suministro  
Cuando el sistema de planificación realiza un cálculo descendente en el que el suministro debe satisfacer la demanda, esta se toma tal como se indica, es decir, está fuera del control del sistema de planificación. No obstante, el lado de aprovisionamiento sigue pudiéndose gestionar. Por lo tanto, el sistema de planificación sugerirá la creación de nuevos pedidos de suministro, reprogramar los existentes o cambiar la cantidad del pedido. Si un pedido de aprovisionamiento existente pasa a ser superfluo, el sistema de planificación sugiere que el usuario lo cancele.  

Si el usuario desea excluir un pedido de aprovisionamiento existente de las sugerencias de planificación, puede indicar que no tiene flexibilidad de planificación (flexibilidad de planificación = ninguna). A continuación, el exceso de suministro del pedido se usará para satisfacer la demanda, pero no se sugerirá ninguna acción.  

En general, todo el aprovisionamiento tiene una flexibilidad de planificación limitada por las condiciones de cada una de las acciones sugeridas.  

-   **Reprogramar fuera**: fecha de un pedido de suministro existente que se puede excluir de la programación para cumplir la fecha de vencimiento de demanda a menos que:  

    -   Representa el inventario (siempre en el día cero).  
    -   Tiene una directiva pedido a pedido vinculada a otra demanda.  
    -   Se encuentra fuera de la página de reprogramación definida por el ciclo.  
    -   Hay un suministro más aproximado que se podría usar.  
    -   Por otro lado, el usuario puede decidir no reprogramar porque:  
    -   El pedido de suministro ya se ha vinculado a otra demanda en una fecha anterior.  
    -   La reprogramación necesaria es tan mínima que el usuario la considera insignificante.  

-   **Reprogramar dentro**: fecha de un pedido de suministro existente que se puede incluir en la programación, excepto con las condiciones siguientes:  

    -   Está vinculada directamente a otra demanda.  
    -   Se encuentra fuera de la página de reprogramación definida por el ciclo.  

> [!NOTE]  
>  Al planificar un producto con un punto de pedido, siempre se puede programar el pedido de suministro si es necesario. Esto es habitual en los pedidos de suministro con programación anticipada que se activan mediante un punto de pedido.  

-   **Aumentar cantidad**: la cantidad de un pedido de aprovisionamiento existente se puede aumentar para satisfacer la demanda, a menos que los pedidos de aprovisionamiento estén conectados directamente con una demanda por un vínculo de pedido a pedido.  

> [!NOTE]  
>  Aunque es posible aumentar el pedido de aprovisionamiento, puede quedar limitado por una cantidad máxima de pedido definida.  

-   **Disminución de cantidad**: los pedidos de aprovisionamiento existentes con excedente en comparación con una demanda existente se pueden disminuir para satisfacer la demanda.  

> [!NOTE]  
>  Aunque la cantidad se podría disminuir, pueden quedar excedentes en comparación con la demanda porque haya una cantidad mínima de pedido definida o un múltiplo de pedido.  

-   **Cancelar**: como incidente especial de la acción de disminución de cantidad, el pedido de aprovisionamiento podría cancelarse si se ha reducido a cero.  
-   **Nuevo**: si no existe ningún pedido de suministro, o no se puede cambiar uno existente para satisfacer la cantidad necesaria en la fecha de vencimiento solicitada, se sugiere un nuevo pedido de suministro.  

### <a name="determining-the-supply-quantity"></a>Configuración de la cantidad de aprovisionamiento  
Los parámetros de planificación definidos por el usuario controlan la cantidad sugerida de cada pedido de suministro.  

Cuando el sistema de planificación calcula la cantidad de un nuevo pedido de suministro o el cambio de cantidad de uno existente, la cantidad sugerida puede ser distinta de la demanda real.  

Si se seleccionan un inventario máximo o una cantidad de pedido fija, la cantidad sugerida se puede aumentar para coincidir con esa cantidad fija o ese inventario máximo. Si una directiva de reaprovisionamiento utiliza una punto de pedido, la cantidad se puede aumentar para llegar al menos al punto de pedido.  

 La cantidad sugerida se puede modificar en esta secuencia:  

1. Hasta la cantidad de pedido máxima (si la hay).  
2. Hasta la cantidad de pedido mínima.  
3. Hasta cumplir el múltiplo de pedido más próximo. (En caso de configuración errónea, se podría infringir la cantidad máxima de pedido).  

### <a name="order-tracking-links-during-planning"></a>Conexiones de seguimiento de pedidos durante la planificación  
En cuanto al seguimiento de pedidos durante la planificación, es importante mencionar que el sistema de planificación reorganiza los vínculos de seguimiento de pedidos dinámicamente creados para las combinaciones de producto, variante o almacén.  

Existen dos motivos para esto:  

-   El sistema de planificación debe poder justificar las sugerencias, que toda la demanda quede cubierta y que ningún pedido de suministro sea superfluo.  
-   Los vínculos de seguimiento de pedidos creados dinámicamente deben volverse a equilibrar con regularidad.  

Con el tiempo, las conexiones de seguimiento de pedidos se descuadran porque la red completa de seguimiento de pedidos no se reorganiza hasta que un evento de demanda o de suministro se cierre realmente.  

Antes de cuadrar el aprovisionamiento por la demanda, la aplicación elimina todos los vínculos de seguimiento de pedidos existentes. A continuación, durante el procedimiento de contrapartida, cuando se cierra un evento demanda o de suministro, establece nuevos vínculos de seguimiento de pedidos entre la demanda y el suministro.  

> [!NOTE]  
>  Aunque el producto no se haya configurado para seguimiento dinámico de pedidos, el programa previsto establecerá vínculos de seguimiento de pedidos equilibrados, tal y como se ha explicado anteriormente.
## <a name="closing-demand-and-supply"></a>Cierre de aprovisionamiento y demanda
Cuando se han realizado los procedimientos de equilibrado del suministro, existen tres situaciones finales posibles:  

* Se han cumplido la cantidad necesaria y la fecha de los eventos de demanda, y se puede cerrar la planificación de ellos. El evento de suministro aún está abierto y puede cubrir la demanda siguiente, por lo que el procedimiento de contrapartida puede empezar con el evento de suministro actual y la demanda siguiente.  
* El pedido de suministro no se puede modificar para cubrir toda la demanda. El evento de demanda sigue abierto, con una cantidad sin cubrir que se puede cubrir mediante el evento de suministro siguiente. Por lo tanto, se cierra el evento de suministro, por lo que el equilibrado puede empezar con la demanda actual y el siguiente evento de suministro.  
* Se ha cubierto toda la demanda; no hay demanda subsiguiente (o no ha habido demanda en absoluto). Si hay algún aprovisionamiento de excedente, se puede reducir (o cancelarse) y después cerrar. Es posible que existan eventos de suministro adicionales más adelante en la cadena y también se deben cancelar.  

Por último, el sistema de planificación creará una conexión de seguimiento de pedidos entre el suministro y la demanda.  

### <a name="creating-the-planning-line-suggested-action"></a>Crear la línea de planificación (acción sugerida)  
Si se sugiere alguna acción (nueva, cambiar de cantidad, reprogramar, reprogramar y cambiar de cantidad o cancelar) para revisar el pedido de aprovisionamiento, el sistema de planificación crea una línea de planificación en la hoja de trabajo de planificación. El seguimiento de pedidos obliga a la creación de la línea de planificación no solo cuando se cierra el evento de aprovisionamiento, sino también si se cierra el evento de demanda, aunque el evento de aprovisionamiento esté aún abierto y puede estar sujeto a los cambios adicionales cuando se procesa el evento de demanda siguiente. Esto significa que la línea de planificación se puede modificar de nuevo cuando se crea por primera vez.  

Para minimizar el acceso de base de datos al manipular las órdenes de producción, la línea de planificación se puede mantener en tres niveles, a la vez que se intenta realizar el nivel de mantenimiento menos exigente:  

* Crear solo la línea de planificación con la fecha de vencimiento y la cantidad actuales, pero sin la ruta y los componentes.  
* Incluir ruta: la ruta planificada se diseña incluyendo el cálculo de las fechas y las horas de inicio y fin. Esto exige muchos accesos a la base de datos. Para determinar las fechas finales y de vencimiento, es posible que sea necesario calcularlo aunque el evento de suministro no se haya cerrado (en el caso de la programación hacia delante).  
* Incluir despliegue de L.M.: esto puede esperar a justo antes de cerrar el evento de aprovisionamiento.  

De este modo concluyen las descripciones de cómo el sistema de planificación carga, da prioridad y equilibra la demanda y el suministro. En integración con esta actividad de planificación de aprovisionamientos, el programa debe garantizar que el nivel de inventario requerido de cada producto planificado se mantiene según sus directivas de reaprovisionamiento.

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
 [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
 [Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]