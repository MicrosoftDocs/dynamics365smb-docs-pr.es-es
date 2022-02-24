---
title: 'Detalles de diseño: Gestión de directivas de reaprovisionamiento | Documentos de Microsoft'
description: Resumen de las tareas de definición de una directiva de reaprovisionamiento de planificación del suministro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f7d207d0f6e4730d900ce4214d7faa8c809ae8bd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185401"
---
# <a name="design-details-handling-reordering-policies"></a>Detalles de diseño: Gestión de directivas de reaprovisionamiento
Para que un producto participe en la planificación de aprovisionamiento es necesario definir una directiva de reaprovisionamiento. Existen las cuatro directivas de reaprovisionamiento siguientes:  

* Cdad. fija reaprov.  
* Cdad. máxima  
* Pedido  
* Lote a lote  

Las directivas Cdad. fija reaprov. y Cdad. máxima están relacionadas con la planificación de inventario. Aunque la planificación del inventario es técnicamente más sencilla que el procedimiento de compensación, estas directivas deben coexistir con el proceso de compensación paso a paso del seguimiento de aprovisionamiento y pedidos. Para controlar la integración entre los dos y proporcionar la información en la lógica de planificación implicada, hay unos principios estrictos que rigen cómo se tratan las directivas de reaprovisionamiento.  

## <a name="the-role-of-the-reorder-point"></a>Función del punto de pedido
Además del equilibrado general de la oferta y la demanda, el sistema de planificación debe supervisar los niveles de inventario para que los productos afectados respeten las directivas de pedido definidas.  

Un punto de pedido representa la demanda durante un plazo de entrega. Cuando el inventario proyectado está por debajo del nivel de inventario definido por el punto de pedido, ha llegado el momento de pedir más cantidad. Mientras tanto, se prevé que el inventario se reduzca gradualmente y posiblemente alcance cero (o el nivel de stock de seguridad), hasta que llegue la reposición.  

Por consiguiente, el sistema de planificación sugerirá un pedido de suministros de programación anticipada en el momento en el que el inventario proyectado quede por debajo del punto de reaprovisionamiento.  

El punto de pedido refleja un determinado nivel de inventario. No obstante, los niveles de inventario pueden variar significativamente durante el ciclo y, por tanto, el sistema de planificación debe supervisar constantemente el inventario disponible proyectado.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Supervisión del nivel de inventario proyectado y el punto de pedido
El inventario es un tipo de aprovisionamiento, pero para planificación del inventario, el sistema de planificación diferencia entre dos niveles de inventario:  

* Inventario proyectado  
* Inventario disponible proyectado  

### <a name="projected-inventory"></a>Inventario proyectado  
Inicialmente, el inventario proyectado es la cantidad de inventario bruto, incluidos aprovisionamientos y demandas en el pasado a pesar de no estar registrados, al iniciar el proceso de planificación. En el futuro, este se convertirá en un nivel inventario proyectado desplazado que se mantiene a través de cantidades en bruto del aprovisionamiento y la demanda futuros, porque se introducen a lo largo de la línea de tiempo (tanto reservados como asignados de otra forma).  

El sistema de planificación usa el inventario proyectado para supervisar el punto de pedido y para determinar la cantidad de pedido al usar la directiva de reaprovisionamiento de cantidad máxima.  

### <a name="projected-available-inventory"></a>Inventario disponible proyectado  
El inventario disponible proyectado es la parte del inventario proyectado que en un momento determinado está disponible para satisfacer la demanda. El motor de planificación usa el inventario disponible proyectado al supervisar el nivel de stock de seguridad.  

El sistema de planificación usa el inventario disponible proyectado para supervisar el nivel del stock de seguridad, ya que el stock de seguridad siempre debe estar disponible para atender la demanda inesperada.  

### <a name="time-buckets"></a>Ciclos  
Tener un estrecho control del inventario proyectado es crucial para detectar cuándo se está alcanzando o cruzando el punto de pedido y calcular la cantidad correcta del pedido cuando se utiliza la directiva de reaprovisionamiento de cantidad máxima.  

Como se ha indicado anteriormente, el nivel de inventario proyectado se calcula al principio del periodo de planificación. Es un nivel bruto que no tiene en cuenta las reservas y asignaciones similares. Para supervisar este nivel de inventario durante la secuencia de planificación, el sistema supervisa los cambios agregados durante un periodo de tiempo, un ciclo. El programa garantiza que el ciclo sea al menos de un día, ya que es la unidad de tiempo más precisa para un evento de demanda o de suministro.  

### <a name="determining-the-projected-inventory-level"></a>Determinación del nivel de inventario proyectado  
En la secuencia siguiente se describe cómo se determina el nivel de inventario proyectado:  

* Cuando un evento de suministro, como, por ejemplo, un pedido de compra, se ha planificado totalmente, aumentará el inventario proyectado en su fecha de vencimiento.  
* Cuando se ha satisfecho completamente un evento de demanda, el inventario proyectado no se reducirá inmediatamente. En su lugar, registra un aviso de disminución, que es un registro interno que lleva la fecha y la cantidad de la contribución al inventario proyectado.  
* Cunando un evento de suministro posterior se planifica y se coloca en la línea temporal, los avisos de disminución registrados se investigan uno a uno hasta la fecha planificada del suministro mientras se actualiza el inventario proyectado. Durante este proceso, se puede alcanzar o pasar el nivel del punto de pedido del aviso de aumento interno.  
* Si se introduce un nuevo pedido de aprovisionamiento, el sistema comprueba si se hace antes del aprovisionamiento actual. Si lo es, el nuevo aprovisionamiento se convierte en el aprovisionamiento actual y el procedimiento de contrapartida comienza de nuevo.  

A continuación se muestra una ilustración gráfica de este principio:  

![Determinación del nivel de inventario proyectado](media/nav_app_supply_planning_2_projected_inventory.png "Determinación del nivel de inventario proyectado")  

1. El suministro **Sa** de 4 (fijos) cierra la demanda **Da** de 3.  
2. CloseDemand: crear un aviso de disminución de -3 (no se mostrará).  
3. El suministro **Sa** está cerrado con un exceso de 1 (no hay más demanda).  

     Esto aumenta el nivel de inventario proyectado en +4, mientras que el inventario **disponible** proyectado es -1.  

4. El siguiente suministro **Sb** de 2 (otro pedido) ya se ha colocado en la escala de tiempo.  
5. El sistema comprueba si hay un aviso de disminución que preceda a **Sb** (no lo hay, por lo que no se realiza ninguna acción).  
6. El sistema cierra el suministro **Sb** (no hay más demanda); A: mediante la reducción a 0 (cancelar) o B: dejándolo como está.  

     Esto aumenta el nivel de inventario proyectado (A: +0 => +4 o B: +2 = +6).  

7. El sistema realiza una comprobación final: ¿hay un aviso de disminución? Sí, hay uno con fecha de **Da**.  
8. El programa agrega el aviso de disminución del aviso -3 en el nivel de inventario proyectado, A: +4 -3 = 1 o B: +6 -3 = +3.  
9. En el caso de A, el sistema crea un pedido con programación anticipada en la fecha **Da**.  

     En caso de B, el punto de pedido se alcanza y no se crea ningún pedido nuevo.

## <a name="the-role-of-the-time-bucket"></a>El rol del ciclo
El propósito del ciclo es recopilar los eventos de demanda dentro del intervalo de tiempo para crear un pedido de suministro conjunto.  

En el caso de directivas de reaprovisionamiento que utilizan un punto de pedido se puede definir un ciclo. De este modo se garantiza que se acumula la demanda en el mismo periodo de tiempo antes de comprobar el impacto en el inventario proyectado y si se ha superado el último punto de pedido. Si se sobrepasa el punto de pedido, se programa de forma anticipada un nuevo pedido de aprovisionamiento desde el final del periodo definido por el ciclo. Los ciclos comienzan en la fecha inicial de planificación.  

El concepto por ciclos refleja el proceso manual de comprobación del nivel de inventario de un modo frecuente en vez de hacerlo por cada transacción. El usuario debe definir la frecuencia (el ciclo). Por ejemplo, el usuario recopila todas las exigencias de producto de un proveedor para hacer un pedido semanal.  

![Ejemplo de ciclo en la planificación](media/nav_app_supply_planning_2_reorder_cycle.png "Ejemplo de ciclo en la planificación")  

Por lo general, el ciclo se usa para evitar un efecto de cascada. Por ejemplo, una fila equilibrada de demanda y aprovisionamiento donde se cancela una demanda temprana, o se crea una nueva. El resultado podría ser que se programe cada pedido de suministro (sin incluir el último).

## <a name="staying-under-the-overflow-level"></a>Mantenimiento por debajo de los niveles de desbordamiento
Cuando se usan políticas de cantidad máxima y cantidad fija, el sistema de planificación se centra en el inventario proyectado únicamente en el ciclo indicado. Esto significa que el sistema de planificación puede sugerir un suministro superfluo cuando se producen cambios de demanda negativa o de suministro positivo fuera del ciclo determinado. Si, por esta razón, se sugiere un aprovisionamiento superfluo, el sistema de planificación calcula qué cantidad de aprovisionamiento debe disminuirse (o eliminarse) para evitar un aprovisionamiento superfluo. Esta cantidad se denomina “nivel de desbordamiento.” El desbordamiento se comunica como una línea de planificación con una acción de **Cambiar cantidad. (salida)** o **Cancelar** y el mensaje de advertencia siguiente:  

*Atención: El inventario proyectado [xx] es superior al nivel de desbordamiento [xx] en la fecha de vencimiento [xx].*  

![Nivel de desbordamiento de inventario](media/supplyplanning_2_overflow1_new.png "Nivel de desbordamiento de inventario")  

###  <a name="calculating-the-overflow-level"></a>Cálculo del nivel de desbordamiento  
El nivel de desbordamiento se calcula de diferentes modos según la configuración de planificación.  

#### <a name="maximum-qty-reordering-policy"></a>Directiva de reaprovisionamiento de cantidad máxima  
Nivel de desbordamiento = stock máximo  

> [!NOTE]  
>  Si existe una cantidad mínima pedido, se agregará de la siguiente forma: nivel de desbordamiento = inventario máximo + cantidad mínima pedido.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Directiva de reaprovisionamiento Cdad. fija reaprov.  
Nivel de desbordamiento = cantidad a pedir + punto de pedido  

> [!NOTE]  
>  Si la cantidad mínima de pedido es más alta que el punto de pedido, se reemplazará de la siguiente forma: nivel de desbordamiento = cantidad a pedir + cantidad mínima de pedido.  

#### <a name="order-multiple"></a>Múltiplo de pedido  
Si existe un múltiplo de pedido, se ajustará el nivel de desbordamiento para las directivas de reaprovisionamiento de cantidad máxima y cantidad fija de reaprovisionamiento.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Crear la línea de planificación con advertencia de desbordamiento  
Cuando un suministro existente provoca que el inventario proyectado sea superior al nivel de desbordamiento al final de un ciclo, se crea una línea de planificación. Para advertir del posible suministro superfluo, la línea de planificación tiene un mensaje de advertencia, el campo **Aceptar mensaje acción** no está seleccionado y el mensaje de acción es Cancelar o Cambiar cdad.  

#### <a name="calculating-the-planning-line-quantity"></a>Cálculo de la cantidad en la línea de planificación  
Cantidad de planificación de línea = cantidad de suministro actual – (inventario proyectado – nivel de desbordamiento)  

> [!NOTE]  
>  Como con todas las líneas de advertencia, se omitirá cualquier cantidad de pedido máximo y mínimo o múltiplo de pedido.  

#### <a name="defining-the-action-message-type"></a>Definir el tipo de mensaje de acción  

-   Si la cantidad de la línea de planificación es superior a 0, el mensaje de acción es Cambiar cdad.  
-   Si la cantidad de la línea de planificación es igual o menor a 0, el mensaje de acción es Cancelar.  

#### <a name="composing-the-warning-message"></a>Composición del mensaje de advertencia  
En el caso de desbordamiento, la página **Elementos planificación sin seguimiento** muestra un mensaje de advertencia con la siguiente información:  

-   Nivel de inventario proyectado que ha activado la advertencia  
-   Nivel de desbordamiento calculado  
-   Fecha de vencimiento del evento de suministro.  

Ejemplo: "El inventario proyectado 120 es superior al nivel de desbordamiento 60 el 28-01-11".  

### <a name="scenario"></a>Caso  
En este ejemplo, un cliente cambia un pedido de venta de 70 a 40 piezas entre dos ejecuciones de planificación. La característica de desbordamiento empieza a reducir la compra que se ha sugerido para la cantidad de venta inicial.  

#### <a name="item-setup"></a>Configuración producto  

|Directiva reaprov.|Cdad. máxima|  
|-----------------------|------------------|  
|Cantidad máxima pedido|100|  
|Punto pedido|50|  
|Grupos contables inventario|80|  

#### <a name="situation-before-sales-decrease"></a>Situación antes de la disminución de venta  

|Evento|Cambiar cdad.|Inventario proyectado|  
|-----------|-----------------|-------------------------|  
|Día uno|Ninguno|80|  
|Venta|-70|10|  
|Final del ciclo|Ninguno|10|  
|Sugerir nuevo pedido de compra|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situación después de la disminución de venta  

|Cambiar|Cambiar cdad.|Inventario proyectado|  
|------------|-----------------|-------------------------|  
|Día uno|Ninguno|80|  
|Venta|-40|nº 40|  
|Compra|+90|130|  
|Final del ciclo|Ninguno|130|  
|Sugerir disminución de compra<br /><br /> pedido a partir de 90 a 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Líneas de planificación resultantes  
 Se crea una línea de planificación (advertencia) para reducir la compra con 30 de 90 a 60 para mantener el inventario proyectado en 100 según el nivel de desbordamiento.  

![Planificar de acuerdo con el nivel de desbordamiento](media/nav_app_supply_planning_2_overflow2.png "Planificar de acuerdo con el nivel de desbordamiento")  

> [!NOTE]  
>  Sin la característica de desbordamiento, no se crea ninguna advertencia si el nivel de inventario proyectado está por encima del inventario máximo. Esto podría provocar un suministro superfluo de 30.

## <a name="handling-projected-negative-inventory"></a>Gestión de inventario negativo proyectado
El punto de pedido expresa la demanda prevista durante el plazo del producto. Cuando se supera el punto de pedido, ha llegado el momento de pedir más. Pero el inventario proyectado debe ser lo suficientemente grande como para satisfacer la demanda hasta que se reciba el nuevo pedido. Mientras tanto, el stock de seguridad debe satisfacer las fluctuaciones en la demanda hasta un nivel de servicio objetivo.  

 Por tanto, el sistema de planificación considera una emergencia el que una demanda futura no se pueda atender desde el inventario proyectado, o dicho de otro modo, que el inventario proyectado quede en negativo. El sistema se ocupa de dicha excepción mediante la sugerencia de un nuevo pedido de suministro para satisfacer la parte de la demanda que no se puede satisfacer mediante las existencias u otro suministro. El tamaño de pedido del nuevo pedido de suministro no tendrá en cuenta el inventario máximo o la cantidad del nuevo pedido. Tampoco tendrá en cuenta los modificadores Cantidad máxima pedido, Cantidad mínima pedido y Múltiplos de pedido. En su lugar, reflejará la deficiencia exacta.  

 La línea de planificación para este tipo pedido de suministro mostrará un icono de advertencia de emergencia y, tras la búsqueda, se proporcionará información adicional para comunicar al usuario la situación.  

 En la ilustración siguiente, el aprovisionamiento D representa un pedido de emergencia que ajustar para inventario negativo.  

 ![Sugerencia de planificación de emergencia para evitar existencias negativas](media/nav_app_supply_planning_2_negative_inventory.png "Sugerencia de planificación de emergencia para evitar existencias negativas")  

1.  El suministro **A**, inventario proyectado inicial, está por debajo del punto de pedido.  
2.  Se ha creado un nuevo aprovisionamiento programación de forma anticipada (**C**).  

     (Cantidad = Inventario máximo – Nivel de inventario proyectado)  
3.  El suministro **A** está cerrado por la demanda **B**, que no se cubre por completo.  

     (La demanda **B** podría intentar programar el aprovisionamiento C, pero esto no sucederá según el concepto de ciclo).  
4.  Se crea un nuevo suministro (**D**) para cubrir la cantidad restante de la demanda **B**.  
5.  La demanda **B** está cerrada (creando un aviso al inventario proyectado).  
6.  Se cierra el nuevo suministro **D**.  
7.  Se ha comprobado el inventario proyectado; no se ha superado el punto de pedido.  
8.  El suministro **C** está cerrado (no hay más demanda).  
9. Comprobación final: que no queden avisos pendientes en el nivel de inventario.  

> [!NOTE]  
>  El paso 4 refleja cómo reacciona el sistema en versiones anteriores a Microsoft Dynamics NAV 2009 SP1.  

De este modo concluye la descripción de los principios básicos relacionados con la planificación de inventario basada en directivas de reorganización. En la sección siguiente se describen las características de las cuatro directivas de reaprovisionamiento admitidas.

## <a name="reordering-policies"></a>Directivas de reaprovisionamiento
Las directivas de reaprovisionamiento definen cuánto se debe pedir cuando se debe reponer el producto. Hay cuatro directivas de reaprovisionamiento.  

### <a name="fixed-reorder-qty"></a>Cdad. fija reaprov.
La directiva Cdad. fija reaprov. está relacionada con la planificación de inventario de los productos C típicos (coste de inventario bajo, poco riesgo de obsolescencia o muchos productos). Normalmente, esta directiva se usa con relación a un punto de pedido que refleja la demanda anticipada durante el plazo del producto.  

#### <a name="calculated-per-time-bucket"></a>Calculado por ciclo  
Si el sistema de planificación detecta que se ha alcanzado o superado el punto de pedido en un ciclo determinado (ciclo de reaprovisionamiento), por encima del punto de pedido al inicio del periodo o en ese mismo punto, o por debajo al final del periodo o en ese mismo punto, sugerirá crear un nuevo pedido de aprovisionamiento con la cantidad de reaprovisionamiento especificada y anticipará su programación a partir de la primera fecha después de final del ciclo.  

El concepto de punto de pedido por ciclos reduce el número de sugerencias de suministro. Esto refleja el proceso manual de recorrer con frecuencia el almacén para comprobar el contenido real de varias ubicaciones.  

#### <a name="creates-only-necessary-supply"></a>Crea solo el aprovisionamiento necesario  
Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el aprovisionamiento se ha pedido ya para ser recibido en el plazo de entrega del producto. Si un pedido de aprovisionamiento existente puede solucionar el problema llevando el inventario proyectado hasta el punto de pedido o por encima dentro del plazo de entrega, el sistema no sugerirá un nuevo pedido de aprovisionamiento.  

Los pedidos de suministro que se crean específicamente para satisfacer un punto de pedido se excluyen del equilibrado de suministro normal y no cambiarán posteriormente. Por tanto, si un producto con punto de pedido debe retirarse (no reponerse), es recomendable revisar los pedidos de aprovisionamiento pendientes manualmente o cambiar la directiva de reaprovisionamiento a lote por lote, de modo que el sistema reduzca o cancele los aprovisionamientos superfluos.  

#### <a name="combines-with-order-modifiers"></a>Combina con modificadores de pedido  
Los modificadores de pedido, Cantidad mínima pedido, Cantidad máxima pedido y Múltiplos de pedido, no deben desempeñar un rol amplio cuando se usa la directiva cantidad de pedido fija. No obstante, el sistema de planificación aún tiene en cuenta estos modificadores y disminuye la cantidad a la cantidad de pedido máxima especificada (y crea dos o más aprovisionamientos para alcanzar la cantidad total de pedido), aumenta el pedido a la cantidad de pedido mínima especificada, o la redondea para que llegue al múltiplo del pedido especificado.  

#### <a name="combines-with-calendars"></a>Combina con Calendarios  
Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el pedido está programado para un día no laborable, según los calendarios definidos en el campo **Código calendario base** en las páginas **Información empresa** y **Ficha almacén**.  

Si la fecha programada es un día no laborable, el sistema de planificación mueve el pedido al próximo día laborable. Esto puede dar lugar a un pedido que cumpla con el punto de pedido pero que no cumpla una demanda específica. Para este tipo de demandas sin saldar, el sistema de planificación crea un suministro extra.  

#### <a name="should-not-be-used-with-forecast"></a>No debe usarse con la previsión  
Dado que la demanda prevista aparece expresada ya en el nivel del punto de pedido, no es necesario incluir una previsión en la planificación de un producto mediante un punto de pedido. Si es necesario basar el plan en una previsión, utilice la directiva de lote por lote.  

#### <a name="must-not-be-used-with-reservations"></a>No se debe usar con reservas  
Si el usuario ha reservado una cantidad, por ejemplo una cantidad en inventario, en algunas demandas lejanas se perturbará la base de la planificación. Aunque el nivel de inventario estimado es aceptable en relación con el punto de nuevo pedido, las cantidades pueden no estar disponibles. El programa puede intentar compensarlo mediante la creación de pedidos de excepción; no obstante, se recomienda que el campo Reservar está configurado como Nunca en los productos que están planificados con un punto de pedido.

### <a name="maximum-qty"></a>Cdad. máxima
La directiva de cantidad máxima es una forma de mantener el inventario mediante un punto de pedido.  

También se aplica a esta directiva todo lo relacionado con la directiva de cantidad de reaprovisionamiento fija. La única diferencia es la cantidad del suministro sugerido. Al usar la directiva de cantidad máxima, la cantidad del nuevo pedido se definirá dinámicamente según el nivel de inventario proyectado y, por lo tanto, normalmente será distinta de un pedido a otro.  

#### <a name="calculated-per-time-bucket"></a>Calculado por ciclo  
La cantidad a pedir se actualmente en el momento (el final de un ciclo) en el que el sistema de planificación detecta que se ha superado el punto de pedido. En este punto, el programa mide la diferencia entre el nivel de inventario proyectado actual y el inventario máximo especificado. Esto constituye la cantidad que se debe volver a pedir. A continuación, el sistema comprueba si el suministro ya se ha pedido en otra parte para recibirse en el plazo y, en caso afirmativo, reduce la cantidad del nuevo pedido de suministro en las cantidades ya pedidas.  

El programa garantizará que el inventario proyectado llegue como mínimo al nivel de punto de pedido como mínimo, en el caso de que el usuario haya olvidado especificar una cantidad de inventario máxima.  

#### <a name="combines-with-order-modifiers"></a>Combina con modificadores de pedido  
Dependiendo de la configuración, puede ser mejor agrupar la directiva de cantidad máxima con modificadores de pedido para garantizar una cantidad de pedido mínima o redondearla a un número entero de unidades de medida de compra, o dividirla en más lotes según lo definido en la cantidad de pedido máxima.  

### <a name="combines-with-calendars"></a>Combina con Calendarios  
Antes de proponer nuevos pedidos de aprovisionamiento para satisfacer un punto de pedido, el sistema de planificación comprueba si el pedido está programado para un día no laborable, según los calendarios definidos en el campo **Código calendario base** en las páginas **Información empresa** y **Ficha almacén**.  

Si la fecha programada es un día no laborable, el sistema de planificación mueve el pedido al próximo día laborable. Esto puede dar lugar a un pedido que cumpla con el punto de pedido pero que no cumpla una demanda específica. Para este tipo de demandas sin saldar, el sistema de planificación crea un suministro extra.

### <a name="order"></a>Sentido
En un entorno de fabricación contra pedido, el producto se compra o se produce para cubrir exclusivamente una demanda concreta. Normalmente, se relaciona con productos A y el motivo para elegir la política de reaprovisionamiento de pedido puede ser que la demanda se produce con poca frecuencia, el plazo es insignificante o varían los atributos requeridos.  

La aplicación crea un vínculo de pedido contra pedido, que actúa de conexión preliminar entre el suministro, un pedido de suministro o inventario, y la demanda que se va a cumplir.  

Aparte de utilizar la directiva de pedido, el vínculo de pedido a pedido se puede aplicar de las siguientes formas durante la planificación:  

* Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes necesarios en la misma orden de producción).  
* Al usar la característica de planificación de pedido de venta para crear una orden de producción a partir de un pedido de venta.  

Aunque una empresa de fabricación se considere a sí misma como entorno de fabricación contra pedido, puede ser preferible utilizar una directiva de lote por lote si los productos son puramente estándar sin variación en los atributos. Como resultado, el programa utilizará un inventario no planificado y solo acumulará los pedidos de venta con la misma fecha de envío o dentro de un ciclo definido.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Conexiones de pedido contra pedido y fechas vencidas  
A diferencia de la mayoría de conjuntos de suministro-demanda, el sistema ha planificado completamente los pedidos vinculados con fechas de vencimiento anteriores a la fecha inicial de planificación. El motivo empresarial de esta excepción es que los conjuntos de demanda-suministro específicos se deben sincronizar mediante la ejecución. Para obtener más información acerca de la zona congelada aplicable a la mayoría de los tipos de aprovisionamiento-demanda, consulte [Gestión de pedidos antes de la fecha de inicio de planificación](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Lote a lote
La directiva de lote por lote es la más flexible porque el sistema solo reacciones ante la demanda real, además de actuar ante la demanda anticipada de los pedidos de previsión y abiertos; a continuación, liquida la cantidad del pedido según la demanda. La directiva de lote por lote está dirigida a los productos A y B, donde el inventario se puede aceptar pero se debe evitar.  

De algún modo, la directiva del lote por lote se parece a la directiva de pedido, pero su acercamiento a los productos es genérico; puede aceptar cantidades en el inventario y une demandas con aprovisionamientos correspondientes en ciclos definidos por el usuario.  

El ciclo se define en el campo **Ciclo**. El programa trabaja con un ciclo mínimo de un día, ya que es la unidad de medida de tiempo menor en los eventos de demanda y de suministro del sistema (aunque, en la práctica, la unidad de medida de tiempo en las órdenes de producción y las necesidades de componentes puede ser segundos).  

El ciclo también establece límites con respecto a cuándo se debe reprogramar un pedido de suministro existente para cubrir una demanda determinada. Si el aprovisionamiento entra dentro del ciclo, se volverá a programar dentro o fuera para cubrir la demanda. De lo contrario, si es anterior, se producirá una acumulación innecesaria del inventario y se debe cancelar. Si es posterior, se creará un nuevo pedido de aprovisionamiento en su lugar.  

Con esta directiva, también se puede definir un stock de seguridad para compensar las fluctuaciones posibles en el suministro, o para satisfacer la demanda repentina.  

Dado que la cantidad del pedido de aprovisionamiento se basa en la demanda real, puede tener sentido usar los modificadores de pedido: redondear la cantidad del pedido para satisfacer un múltiplo de pedido especificado (o unidad de medida de compra), incrementar el pedido a una cantidad mínima especificada o disminuir la cantidad máxima especificada (y crear así dos aprovisionamientos o más para alcanzar la cantidad total necesaria).

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
