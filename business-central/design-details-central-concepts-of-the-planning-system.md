---
title: Detalles de diseño - Conceptos centrales del sistema de planificación | Documentos de Microsoft
description: Las funciones de planificación se incluyen en un proceso que primero selecciona los productos relevantes y el periodo de planificación y, a continuación, propone acciones posibles para que las realice el usuario en función de la situación de demanda/oferta y los parámetros de planificación de los productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6cfe028d21086269f1492aefde31fe6b659d06b4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788126"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Detalles de diseño: Conceptos centrales del sistema de planificación
Las funciones de planificación se incluyen en un proceso que primero selecciona los productos correspondientes y el periodo que se planificará. A continuación, según el código de nivel inferior de cada producto (posición de la L.M.), el proceso llama a una codeunit que calcula un plan de suministro equilibrando los conjuntos de suministro y demanda, y sugiriendo acciones posibles que puede realizar el usuario. Las acciones sugeridas aparecen como líneas en la hoja de planificación o la hoja de demanda.  

![Contenido de la página Hoja de planificación](media/NAV_APP_supply_planning_1_planning_worksheet.png "Contenido de la página Hoja de planificación")  

Se supone que el planificador de una empresa, como un comprador o un planificador de producción, es el usuario del sistema de planificación. El sistema de planificación ayuda al usuario a realizar los cálculos completos pero bastante sencillos de un plan. El usuario podrá concentrarse en resolver problemas más difíciles, como, por ejemplo, cuando las cosas son distintas de las normales.  

El sistema de planificación se basa en la demanda de cliente anticipada y real, como los pedidos previstos y de venta. Si se ejecuta el cálculo de la planificación, la aplicación sugerirá acciones concretas al usuario en relación con un posible aprovisionamiento desde los proveedores, departamentos de producción o de ensamblado o transferencias desde otros almacenes. Estas acciones sugeridas podrían ser crear nuevos pedidos de suministro, como pedidos de compra u órdenes de producción. Si ya hay pedidos de aprovisionamiento, las acciones sugeridas pueden ser aumentar o acelerar los pedidos para satisfacer los cambios de la demanda.  

Otro objetivo del sistema de planificación es el de garantizar que las existencias no aumentan innecesariamente. En el caso de un descenso de la demanda, el programa de planificación sugerirá al usuario que se pospongan o cancelen algunos de los pedidos de aprovisionamiento existentes, o que se reduzcan sus cantidades.  

MRP y MPS, Calc. plan. saldo periodo y Calc. planif. regenerativa son funciones dentro de una codeunit que contiene la lógica de planificación. No obstante, el cálculo del plan de aprovisionamiento implica a distintos subsistemas.  

Observe que el sistema de planificación no incluye ninguna lógica dedicada para la nivelación de capacidad o para la programación precisa. Por lo tanto, dicha trabajo de programación se realiza como una disciplina aparte. La falta de integración directa entre las dos áreas también significa que los cambios importantes de capacidad o de programación requerirán que se vuelva a ejecutar la planificación.  

## <a name="planning-parameters"></a>Parámetros de la planificación  
Los parámetros de planificación que el usuario establece para un producto o un grupo de productos controlan qué acciones sugerirá el sistema de planificación en las distintas situaciones. Los parámetros de planificación se definen en cada ficha de producto para comprobar el momento, la cantidad y el modo de reposición.  

Los parámetros de planificación también se pueden definir para cualquier combinación de producto, variante y ubicación mediante la configuración de una unidad de almacenamiento (UA) para cada combinación necesaria y, a continuación, mediante la especificación de los parámetros individuales.  

Para obtener más información, consulte [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) y [Detalles de diseño: Parámetros de planificación](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Fecha inicial de la planificación  
Para evitar un plan de suministro que incorpore pedidos abiertos en el pasado y sugiera acciones potencialmente imposibles, el sistema de planificación trata todas las fechas de la fecha inicial de la planificación como una zona congelada donde se aplican la siguiente regla especial:  

Toda la demanda y aprovisionamiento antes de la fecha de inicio del periodo de planificación se tendrá como parte del inventario o enviado.  

Es decir, se asume que el plan para el pasado se ejecuta según el plan proporcionado.  

Para obtener más información, consulte [Gestión de pedidos antes de la fecha de inicio de planificación](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Seguimiento dinámico de pedidos (fijación)  
El seguimiento dinámico de pedidos, con creación simultánea de mensajes de acción en la hoja de trabajo de planificación, no forma parte del sistema de planificación de suministro en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esta característica vincula, en tiempo real, la demanda y las cantidades que podrían cubrirla, siempre que se crea o se cambia una nueva demanda o suministro.  

Por ejemplo, si el usuario introduce o modifica un pedido de venta, el sistema de seguimiento dinámico de pedidos buscará inmediatamente un aprovisionamiento adecuado para cubrir la demanda. Podría ser del inventario o de un pedido de suministro previsto (como un pedido de compra o una orden de producción). Cuando se encuentra un origen de suministro, el programa crea un vínculo entre la demanda y el suministro, y lo muestra en las páginas de solo visualización a las que se tiene acceso desde las líneas de documento correspondientes. Si no se encuentra un suministro adecuado, el sistema de seguimiento de pedidos dinámico crea mensajes de acción en la hoja de planificación con sugerencias de plan de suministro que refleje el equilibrio dinámico. Por consiguiente, el sistema de seguimiento dinámico de pedidos ofrece un sistema de planificación muy básico que puede ser de ayuda para el planificador y otras funciones en la cadena de aprovisionamiento interna.  

Igualmente, el seguimiento dinámico del pedido se pueden considerar una herramienta que ayuda al usuario en evaluar si aceptar o no las sugerencias de pedidos de aprovisionamiento. Desde el lado del aprovisionamiento, un usuario puede ver qué demanda ha creado el aprovisionamiento y, desde el lado de la demanda, qué aprovisionamiento debe satisfacer la demanda.  

![Ejemplo de seguimiento dinámico de pedidos](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Ejemplo de seguimiento dinámico de pedidos")  

Para obtener más información, consulte [Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).  

En empresas con un flujo de productos bajo y menos estructuras de producto avanzadas, puede ser apropiado utilizar el seguimiento dinámico de pedidos como modo principal de planificación de aprovisionamiento. No obstante, en entornos más ocupados, el sistema de planificación se debe utilizar para garantizar un plan de aprovisionamiento correctamente equilibrado siempre.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Seguimiento dinámico de pedidos frente al sistema de planificación  
Con un vistazo rápido puede ser complicado diferenciar entre el sistema de planificación y el seguimiento dinámico de pedidos. Ambas funciones muestran la salida en la hoja de trabajo de la planificación mediante la sugerencia de acciones que el planificador debe realizar. No obstante, la forma en la que se produce esta salida es diferente.  

El sistema de planificación se ocupa de todo el patrón de suministro-demanda de un producto a través de todos los niveles de la jerarquía de la L.M. a lo largo de la escala temporal, mientras que el seguimiento dinámico de pedidos solo se ocupa de la situación del pedido que lo ha activado. Al equilibrar la demanda y el suministro, el sistema de planificación crea vínculos en un modo por lotes activado por el usuario, mientras que el seguimiento dinámico de pedidos crea los vínculos de forma automática y dinámica, siempre que el usuario introduce una demanda o un suministro en la aplicación, por ejemplo, un pedido de venta o un pedido de compra.  

El seguimiento dinámico de pedidos establece vínculos entre aprovisionamiento y demanda cuando se introducen datos según orden de entrada. Esto puede provocar un desorden en las prioridades. Por ejemplo, un pedido de venta que se ha registrado primero, con una fecha de vencimiento en el siguiente mes, se puede vincular al aprovisionamiento en inventario, mientras que el siguiente pedido de venta con vencimiento al día siguiente puede hacer que un mensaje de acción cree un nuevo pedido de compra para cubrirlo, tal como se ilustra a continuación.  

![Ejemplo de seguimiento de pedidos en la planificación de suministros 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Ejemplo de seguimiento de pedidos en la planificación de suministros 1")  

En cambio, el sistema de planificación trata con toda la demanda y el aprovisionamiento para un producto determinado, en orden de prioridad y según las fechas de vencimiento y los tipos de pedidos, es decir, que primero se atiende al primero en necesitar ser atendido. Elimina todos los vínculos de seguimiento de pedidos creados dinámicamente y los restablece según prioridad de fecha de vencimiento. Cuando se ha ejecutado el sistema de planificación, se han solucionado todos los desequilibrios entre demanda y suministro, tal como se ilustra a continuación para los mismos datos.  

![Ejemplo de seguimiento de pedidos en la planificación de suministros 2](media/NAV_APP_supply_planning_1_planning_graph.png "Ejemplo de seguimiento de pedidos en la planificación de suministros 2")  

Después la ejecución de la planificación, no quedan mensajes de acción en la tabla Mov. mensaje acción, ya que han sido reemplazados por las acciones sugeridas en la hoja de trabajo de planificación.  

Para obtener más información, consulte Conexiones de seguimiento de pedidos durante la planificación en [Equilibrio de aprovisionamiento con demanda](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand).  

## <a name="sequence-and-priority-in-planning"></a>Secuencia y prioridad en la planificación  
Al establecer un plan, es importante la secuencia de los cálculos para que el trabajo se realice en un intervalo de tiempo razonable. Además, la priorización de los requisitos y los recursos desempeña una importante función a la hora de obtener los mejores resultados.  

El sistema de planificación en [!INCLUDE[d365fin](includes/d365fin_md.md)] se basa en la demanda. Los productos de primer nivel se deben planificar antes que los productos de nivel inferior, ya que el plan para productos de primer nivel puede generar una demanda adicional para los productos de nivel inferior. Esto significa, por ejemplo, que las ubicaciones minoristas deben planificarse antes de que se planifiquen los centros de distribución, porque el plan de una ubicación minorista puede incluir demanda adicional del centro de distribución. En un nivel de contrapartida detallado, también significa que un pedido de venta no debe desencadenar un nuevo pedido de suministro si un pedido de suministro ya lanzado puede cubrir el pedido de venta. Del mismo modo, no se debe asignar un suministro que incluya un número de lote específico para cubrir una demanda genérica si otra demanda requiere este lote concreto.  

### <a name="item-priority--low-level-code"></a>Prioridad de producto / Cód. nivel más bajo  
En un entorno de fabricación, la demanda para un producto terminado y sellable dará como resultado una demanda derivada para los componentes que forman parte del producto terminado. La estructura de lista de materiales controla la estructura de componentes y puede abarcar varios niveles de productos semiterminados. La planificación de un producto en un nivel provocará demanda derivada para los componentes en el siguiente nivel, y así sucesivamente. Finalmente, esto dará como resultado una demanda derivada de los productos comprados. Por tanto, el sistema de planificación planifica productos en orden de clasificación en la jerarquía de la L.M. total, empezando por los productos vendibles terminados del nivel superior y siguiendo hacia abajo por la estructura de productos hasta los productos de nivel inferior (según el código más bajo).  

![Planificación de las listas de materiales](media/NAV_APP_supply_planning_1_BOM_planning.png "Planificación de las listas de materiales")  

En la figura se ilustra la secuencia en el que el sistema realiza las sugerencias de los pedidos de suministro en el nivel superior y, si se supone que el usuario va a aceptar estas sugerencias, también para productos de nivel inferior.  

Para obtener más información acerca de las consideraciones de fabricación, consulte [Carga de los perfiles de inventario](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

### <a name="locations--transfer-level-priority"></a>Prioridad de ubicaciones o de nivel de transferencia  
Las empresas que trabajan con más de un almacén pueden tener que planificar para cada almacén por individual. Por ejemplo, el nivel de existencias de seguridad de un producto y su directiva de reaprovisionamiento pueden diferir de un almacén a otro. En este caso, los parámetros de planificación deben especificarse por producto y también por almacén.  

Se admite con el uso de UA, donde los parámetros individuales de planificación se pueden especificar en el nivel de UA. Las UA se pueden considerar como productos en un almacén específico. Si el usuario no ha definido una UA para ese almacén, la aplicación establecerá los parámetros en su valor establecido en la ficha del producto. La aplicación calcula un plan para las ubicaciones activas únicamente, que es donde hay demanda o suministro existente para el producto indicado.  

En principio, cualquier producto puede gestionarse en cualquier almacén, pero el enfoque del programa en cuanto al concepto de almacén es muy estricto. Por ejemplo, un pedido de venta en un almacén no se puede satisfacer con una cantidad en existencias en otro almacén. La cantidad de existencias primero se debe transferir a la ubicación especificada en el pedido de venta.  

![Planificación de unidades de almacenamiento](media/NAV_APP_supply_planning_1_SKU_planning.png "Planificación de unidades de almacenamiento")  

Para obtener más información, consulte [Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Prioridad pedido  
En una UA concreta, la fecha solicitada o disponible representa la máxima prioridad; la demanda de hoy se debe tratar antes que la de los próximos días. Pero aparte de esta clase de prioridad, los distintos tipos de demanda y aprovisionamiento se ordenan según su relevancia empresarial para decidir qué demanda se debe satisfacer antes de cubrir otra demanda. En el suministro, la prioridad de pedido indica qué origen de suministro se debe aplicar antes de que se apliquen otros orígenes de suministro.  

Para obtener más información, consulte [Priorizar pedidos](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Previsiones de demanda y pedidos abiertos  
Las previsiones y los pedidos abiertos representan ambos la demanda prevista. El pedido abierto, que abarca las compras previstas de un cliente durante un determinado periodo de tiempo, sirve para reducir la incertidumbre de una previsión global. El pedido abierto es una previsión específica del cliente por encima de la previsión sin especificar, tal como se ilustra a continuación.  

![Planificación con previsiones](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planificación con previsiones")  

Para obtener más información, consulte la sección “Los pedidos de ventas reducen la demanda de previsión” en [Carga de los perfiles de inventario](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Asignar planificación  
Todos los productos se deben planificar; no obstante, no hay razón para calcular un plan para un producto a menos que haya habido un cambio en el patrón de demanda o de aprovisionamiento desde la última vez que se calculó un plan.  

Si el usuario ha introducido un nuevo pedido de venta o ha cambiado uno existente, existen motivos para volver a calcular el plan. Entre otros motivos se incluye un cambio en la previsión o en el stock de seguridad deseado. Un cambio en una lista de materiales mediante la adición o eliminación de un componente indicaría probablemente un cambio, pero para el producto componente solo.  

El sistema de planificación supervisa dichos eventos y asigna los productos adecuados para realizar la planificación.  

En el caso de ubicaciones múltiples, la asignación se realiza en el nivel de producto por combinación de almacén. Si, por ejemplo, se ha creado un pedido de venta en solo una ubicación, la aplicación asignará el producto a esa ubicación específica para planificar.  

El motivo para seleccionar productos para la planificación es cuestión de rendimiento del sistema. Si no se ha producido ningún cambio en el patrón de demanda-aprovisionamiento de un producto, el sistema de planificación no sugerirá ninguna acción. Sin la asignación de planificación, el sistema tendría que realizar cálculos para todos los productos a fin de averiguar para qué debe planificar y lo que agotaría los recursos del sistema.  

La lista completa de los motivos para asignar un producto para planificación se proporciona en [Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md).  

Las opciones de planificación en [!INCLUDE[d365fin](includes/d365fin_md.md)] son:  

-   Calc. planif. regenerativa: calcula todos los productos seleccionados, tanto si es necesario como si no.  
-   Calc. plan. saldo periodo: calcula únicamente aquellos productos seleccionados que tengan algún cambio en su modelo de demanda y aprovisionamiento y, por tanto, se hayan asignado para planificarse.  

Algunos usuarios creen que la planificación de cambio neto se debe realizar de forma dinámica, por ejemplo, cuando se registran los pedidos de venta. No obstante, esto podría resultar confuso, ya que los mensajes de las acciones y el seguimiento de pedidos dinámico también se calculan sobre la marcha. Además, [!INCLUDE[d365fin](includes/d365fin_md.md)] ofrece control en tiempo real neto no comprometido, el cual emite advertencias emergentes cuando se introducen pedidos de venta si la demanda no se puede satisfacer bajo el plan actual de suministro.  

Además de estas consideraciones, el sistema de planificación planifica solo aquellos productos que el usuario ha preparado con los parámetros apropiados de planificación. De lo contrario, se supone que el usuario planeará los productos de un modo manual o semiautomático con la característica Planificación de pedidos.  

Para obtener más información sobre los procedimientos de planificación automática, consulte [Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Dimensiones de producto  
La demanda y el aprovisionamiento pueden llevar códigos de variante y códigos de almacén que se deben respetar cuando el sistema de planificación salde la demanda y el aprovisionamiento.  

El sistema trata los códigos de variante y de ubicación como dimensiones de producto en una línea de pedido de venta, un movimiento de contabilidad, etc. Por consiguiente, se calcula un plan para cada combinación de variante y almacén, como si la combinación fuera un número de producto aparte.  

En lugar de calcular cualquier combinación teórica de variante y ubicación, la aplicación solo calcula las combinaciones que existen realmente en la base de datos.  

Para obtener más información sobre cómo el sistema de planificación gestiona los códigos de almacén en demandas, consulte [Detalles de diseño: Demanda en almacén vacío](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Atributos de producto  
Aparte de las dimensiones de productos generales, como número de producto, código de variante, código de almacén y tipo de pedido, cada evento de demanda y de aprovisionamiento puede llevar especificaciones adicionales en forma de números de serie y de lote. El sistema de planificación planea estos atributos de determinadas formas según su nivel de especificación.  

Un vínculo de pedido a pedido entre demanda y aprovisionamiento es otro tipo de atributo que afecta al sistema de planificación.  

### <a name="specific-attributes"></a>Atributos específicos  
Determinados atributos en demanda son específicos y deben coincidir exactamente con un aprovisionamiento correspondiente. Existen los dos atributos específicos siguientes:  

-   Números de serie o de lote requeridos que necesitan aplicación específica (la casilla **Seguim. NS específ.** o **Seguim. lote específ.** se ha seleccionado en la página **Ficha cód. seguim. prod.** para el código de seguimiento de producto que usa el producto).  
-   Conexiones a pedidos de suministro creados manual o automáticamente para una demanda determinada (conexiones de pedido contra pedido).  

En estos atributos, el sistema de planificación aplica las reglas siguientes:  

-   La demanda con atributos específicos se puede cubrir únicamente con atributos coincidentes.  
-   El suministro con atributos específicos también puede satisfacer la demanda que no solicite estos atributos específicamente.  

Por consiguiente, si una demanda de atributos específicos no se puede cubrir a través del inventario o los aprovisionamientos proyectados, el sistema de planificación sugerirá nuevos pedidos de aprovisionamiento para cubrir esta demanda determinada sin tener en cuenta los parámetros de planificación.  

### <a name="non-specific-attributes"></a>Atributos no específicos  
Los productos con número de serie o de lote sin una configuración específica del seguimiento de productos pueden tener números de serie o de lote que no se deban aplicar al mismo número de serie o de lote exacto, sino que se puedan aplicar a cualquier número de serie o de lote. De este modo el sistema de planificación dispone de más libertad, por ejemplo, para hacer corresponder una demanda serializada con un suministro serializado, normalmente en inventario.  

La demanda y el aprovisionamiento con números de serie y de lote, específicos o no, se consideran prioritarios y están por tanto exentos de la zona congelada, lo que significa que formarán parte de la planificación incluso si vencen antes de la fecha de inicio de la planificación.  

Para obtener más información, consulte la sección sobre la carga de números de serie y de lote por nivel de especificación” en [Carga de los perfiles de inventario](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Para obtener más información sobre cómo el sistema de planificación equilibra los atributos, consulte [Exención de números de serie y de lote y de vínculos de pedido a pedido de la zona congelada](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Vínculos de pedido a pedido  
Las compras de pedido contra pedido implican que un producto se compra, se ensambla o se produce para cubrir exclusivamente una demanda concreta. Normalmente, se relaciona con productos A, y el motivo para elegir esta política de reaprovisionamiento puede ser que la demanda se produce con poca frecuencia, el plazo es insignificante o varían los atributos requeridos.  

Otro caso especial que utiliza vínculos de pedido a pedido es cuando un pedido de ensamblado se vincula a un pedido de venta en una situación de ensamblado para pedido.  

Las conexiones de pedido contra pedido se aplican entre la demanda y el suministro de cuatro maneras:  

-   Cuando el producto planificado usa la directiva de reaprovisionamiento Pedido.  
-   Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes necesarios en la misma orden de producción).  
-   Al crear las órdenes de producción para los pedidos de venta con la característica de planificación de pedido de venta.  
-   Al ensamblar un producto en un pedido de venta. (La directiva de ensamblado se establece en Ensamblar para pedido.  

En estos casos, el sistema de planificación sugerirá solo solicitar la cantidad requerida. Una vez creado, el pedido de compra, la orden de producción o el pedido de ensamblado seguirá correspondiéndose con la demanda correspondiente. Por ejemplo, si un pedido de venta se modifica en tiempo o en cantidad, el sistema de planificación sugerirá que el pedido de aprovisionamiento correspondiente se modifique según corresponda.  

Cuando existen vínculos de pedido contra pedido, el sistema de planificación no incluye el suministro o inventario vinculado en el procedimiento de contrapartida. Depende del usuario evaluar si el suministro vinculado se usa para cubrir otra demanda o una nueva y, en ese caso, eliminar el pedido de suministro o reservar el suministro vinculado manualmente.  

Las reservas y las conexiones de seguimiento de pedidos se interrumpirán si una situación resulta imposible, como desplazar la demanda a una fecha anterior al suministro. No obstante, el vínculo de pedido a pedido se adapta a cualquier cambio en la demanda o el aprovisionamiento correspondiente, por lo que el vínculo nunca se rompe.  

## <a name="reservations"></a>Reservas  
El sistema de planificación no incluye ninguna cantidad reservada en el cálculo. Por ejemplo, si un pedido de venta se ha liquidado o reservado parcialmente con respecto a la cantidad en el inventario, la cantidad reservada en el inventario no se puede utilizar para cubrir otra demanda. El sistema de planificación no incluye este conjunto de demanda-suministro en su cálculo.  

No obstante, el sistema de planificación seguirá incluyendo las cantidades reservadas del perfil de inventario proyectado, ya que todas las cantidades deben tenerse en cuenta a la hora de determinar tanto cuándo se ha pasado el punto de pedido como cuántos hay que volver a pedir para alcanzar y no superar el nivel de inventario máximo. Por tanto, las reservas innecesarias llevarán a un mayor riesgo de que los niveles de inventario bajen demasiado, ya que la lógica de planificación no detecta las cantidades reservadas.  

En la ilustración siguiente se muestra cómo las reservas pueden impedir el plan más factible.  

![Planificación con reservas](media/NAV_APP_supply_planning_1_reservations.png "Planificación con reservas")  

Para obtener más información, consulte [Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Advertencias  
La primera columna de la hoja de planificación corresponde a los campos de advertencia. Cualquier línea de planificación creada para una situación inusual mostrará un icono de advertencia en este campo, en el que el usuario puede hacer clic para obtener información adicional.  

El aprovisionamiento de las líneas de planificación con advertencias no se modificará normalmente según los parámetros de planificación. En su lugar, el sistema de planificación sugiere solo un suministro para satisfacer la cantidad exacta de demanda. Sin embargo, el sistema se puede configurar para respetar ciertos parámetros de planificación para las líneas de planificación con determinadas advertencias. Para obtener más información, consulte la descripción de estas opciones para el proceso **Calcular plan - Hoja planif.** y el proceso **Calcular plan - Hoja demanda** respectivamente.  

La información de advertencia se muestra en la página **Elementos planificación sin seguimiento**, que también se usa para presentar vínculos del seguimiento de pedidos a las entidades de red que no realizan pedidos. Existen los siguientes tipos de advertencia:  

-   Emergencia  
-   Excepción  
-   Atención  

![Advertencias en la hoja de planificación](media/NAV_APP_supply_planning_1_warnings.png "Advertencias en la hoja de planificación")  

### <a name="emergency"></a>Emergencia  
La advertencia de emergencia se muestra en dos situaciones:  

-   Cuando el inventario es negativo en la fecha de inicio de la planificación.  
-   Cuando existen eventos de demanda o aprovisionamiento atrasados.  

Si el inventario de un producto es negativo en la fecha de inicio de la planificación, el sistema de planificación le sugiere un aprovisionamiento de emergencia para la cantidad negativa que llegue en la fecha de inicio de la planificación. El texto de advertencia informa de tal fecha y de la cantidad del pedido de emergencia. Para obtener más información, consulte [Gestión de inventario negativo proyectado](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Todas las líneas de documento con fecha de vencimiento antes de la fecha de inicio de la planificación se consolidan en un pedido de demanda de emergencia para que el elemento llegue en la fecha de inicio de la planificación.  

### <a name="exception"></a>Excepción  
Se mostrará la advertencia de excepción si el inventario disponible previsto cae por debajo de la cantidad de existencias de seguridad. El programa de planificación sugerirá un pedido de suministros para cubrir la demanda en la fecha de vencimiento. El texto de advertencia informa de la cantidad de existencias de seguridad del producto y de la fecha en la que se infringe.  

Infringir el nivel de existencias de seguridad está considerado una excepción debido a que no debería ocurrir si se configura correctamente el punto de nuevo pedido. Para obtener más información, consulte [Función del punto de pedido](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

En general, las propuestas de pedido excepcionales garantizan que el inventario disponible proyectado nunca será menor que el nivel de existencias de seguridad. Esto significa que la cantidad propuesta es justo suficiente como para cubrir las existencias de seguridad, sin tener en cuenta los parámetros de planificación. Sin embargo, en algunos ejemplos, se considerarán modificadores de pedido.  

> [!NOTE]  
>  El sistema de planificación puede haber consumido el stock de seguridad intencionadamente y, a continuación, lo repondrá de forma inmediata. Para obtener más información, consulte [El stock de seguridad se puede consumir](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Atención  
La advertencia de atención se muestra en tres situaciones:  

-   La fecha de inicio de la planificación es anterior a la fecha de trabajo.  
-   La línea de planificación sugiere cambiar una compra realizada o una orden de producción.  
-   El inventario proyectado supera el nivel de desbordamiento en la fecha de vencimiento. Para obtener más información, consulte [Mantenimiento por debajo de los niveles de desbordamiento](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  En las líneas de planificación con advertencias, el campo **Aceptar mensaje acción** está desactivado, ya que se espera que el planificador investigue estás líneas más detalladamente antes de llevar a cabo el plan.  

## <a name="error-logs"></a>Registros de errores  
En la página de la solicitud Calcular plan, el usuario puede seleccionar el campo **Parar y mostrar primer error** para incluir una parada en la ejecución de la planificación cuando se encuentre el primer error. Además, mostrará un mensaje con información sobre el error. Si hay algún error, solo se mostrarán en la hoja de planificación las líneas de planificación correctas realizadas antes de que se produjera el error.  

Si el campo no está seleccionado, el trabajo por lotes Calcular plan continuará hasta que se haya completado. Los errores no interrumpirán el trabajo por lotes. Si hay errores, la aplicación mostrará un mensaje al final, para indicar cuántos productos se ven afectados por los errores. A continuación, se abrirá la página **Registro error planificación**, con más información sobre el error y vínculos a los documentos afectados o las fichas de configuración.  

![Mensajes de error en la hoja de planificación](media/NAV_APP_supply_planning_1_error_log.png "Mensajes de error en la hoja de planificación")  

## <a name="planning-flexibility"></a>Flexib. planificación  
No siempre resulta práctico planificar los pedidos de suministro existentes, por ejemplo cuando se ha iniciado la producción o se ha contratado a personas adicionales un día específico para realizar el trabajo. Para indicar si el sistema de planificación puede cambiar un pedido existente, todas las líneas de pedido de suministro tienen el campo Flexib. planificación con dos opciones: Ilimitada o Ninguna. Si el campo está establecido en Ninguno, el sistema de planificación no intentará modificar la línea del pedido de aprovisionamiento.  

El usuario puede configurar manualmente el campo, pero, en algunos casos el sistema lo configurará automáticamente. Es importante el hecho de que el usuario pueda configurar manualmente la flexibilidad de planificación, ya que facilita la adaptación del uso de la característica a diferentes flujos de trabajo y casos empresariales.  

Para obtener más información acerca de cómo se utiliza este campo, consulte [Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Planificación de pedidos  
La herramienta de planificación de suministro básica representada por la página **Planificación de pedidos** se ha diseñado para la toma de decisiones manual. No tiene en cuenta ningún parámetro de planificación, por lo que no se contempla más adelante en este documento. Para obtener más información acerca de la función de planificación de pedidos, consulte la Ayuda de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  No es recomendable utilizar la planificación de pedidos si la empresa ya utiliza las hojas de trabajo de planificación o solicitud. Los pedidos de aprovisionamientos creados a través de la página **Programación de pedidos** se pueden modificar o eliminar durante las ejecuciones de planificaciones automatizadas. Esto se debe a que los procesos de planificación automatizados utilizan parámetros de planificación que es posible que el usuario que realiza el plan manual en la página Programación de pedidos no tenga en cuenta.  

##  <a name="finite-loading"></a>Carga limitada  
[!INCLUDE[d365fin](includes/d365fin_md.md)] es un sistema ERP estándar, no un sistema de control de envíos o de planta. Planea una utilización factible de los recursos al proporcionar una programación preliminar, pero no crea ni mantiene automáticamente las programaciones detalladas basadas en prioridades o reglas de optimización.  

El uso previsto de la característica Recurso capacidad limitada es 1) evitar la sobrecarga de los recursos específicos y 2) garantizar que no se deje ninguna capacidad sin asignar si pudiera aumentar el plazo de producción de una orden de producción. La característica no incluye ninguna función u opción para priorizar u optimizar las operaciones como sería de prever en un sistema de distribución. No obstante, puede proporcionar información aproximada sobre la capacidad útil para identificar cuellos de botella y evitar sobrecargar los recursos.  

Al planificar con recursos de capacidad limitada, el sistema se asegura de que no se cargue ningún recurso por encima de su capacidad definida (carga crítica). Esto se realiza mediante la asignación de cada operación a la franja temporal disponible más próxima. Si la franja temporal no es lo suficientemente amplia para completar toda la operación, la operación se dividirá en dos o más partes que se colocarán en las franjas temporales más próximas disponibles.  

> [!NOTE]  
>  En el caso de división de la operación, el tiempo de configuración se asigna solo una vez, pues se presupone que se realiza algún ajuste manual para optimizar la programación.  

El tiempo de amortiguación puede agregarse a recursos para minimizar la división de operaciones. De este modo, el sistema puede programar la carga en el último día posible superando el porcentaje de carga crítica ligeramente si esto puede reducir el número de operaciones divididas.  

Esto completa el resumen de los conceptos básicos relacionados con la planificación del suministro en [!INCLUDE[d365fin](includes/d365fin_md.md)]. En las secciones siguientes se investigan estos conceptos con más profundidad y se presentan en el contexto de los procedimientos de planificación básicos, el equilibrado de la demanda y el suministro, así como el uso de las directivas de reaprovisionamiento.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Tabla de asignación de planificación](design-details-planning-assignment-table.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)
