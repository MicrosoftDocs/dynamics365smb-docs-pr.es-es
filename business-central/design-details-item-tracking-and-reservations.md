---
title: 'Detalles de diseño: Seguimiento de productos y reservas'
description: Este tema habla del seguimiento y reservas de producto y describe los conceptos detrás de las dos opciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: d2c5032983bd20fc1e8fa902bd6ed522506fc5b3
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "6320893"
---
# <a name="design-details-item-tracking-and-reservations"></a>Detalles de diseño: Seguimiento de productos y reservas

No es habitual el uso simultáneo de la reserva y del seguimiento de producto específico porque ambos crean un acoplamiento entre el suministro y la demanda. Salvo en situaciones en las que un cliente o un planificador de producción solicita un lote específico, casi nunca tiene sentido reservar productos de inventario que ya llevan números de seguimiento de producto para una liquidación específica. Aunque es posible reservar los productos que requieren seguimiento específico, se necesita una funcionalidad especial para evitar conflictos entre los procesadores de pedidos que solicitan los mismos productos a los que se hace un seguimiento.  
  
El concepto de enlace posterior garantiza que una reserva no específica de un número de serie o de lote permanece acoplado dinámicamente hasta que se registra. En el momento de efectuarse el registro, el programa de reservas puede reorganizar reservas no específicas para garantizar que sea posible aplicar una liquidación fija con respecto al número de serie o de lote que se seleccione. Mientras tanto, el número de serie o de lote está disponible para la reserva específica en otros documentos que solicitan dicho número de serie o de lote.  
  
Una reserva no específica es una en la que al usuario no le importa qué producto específico se selecciona, y una reserva específica es una en la que al usuario le importa.  
  
> [!NOTE]  
> La funcionalidad de enlace posterior se relaciona solo con los productos que están configurados con el seguimiento de productos específicos y se aplica únicamente a las reservas sobre el inventario, no sobre los pedidos de suministro entrantes.  
  
La reserva de números de seguimiento de productos se divide en dos categorías, como se muestra en la tabla siguiente.  
  
|Reservas|Description|  
|-----------------|---------------------------------------|  
|Específico|Seleccione un determinado número de serie o de lote cuando reserve el producto de inventario de una demanda, como, por ejemplo, un pedido de venta.<br /><br /> Esta es una reserva habitual. Es un vínculo rígido entre aprovisionamiento y demanda, en el que ambos incluyen números de serie o de lote. **Nota:** La demanda incluye números de serie o de lote. <br /><br /> Por ejemplo, desea reservar una lata de pintura azul del lote A, porque el cliente así lo quiere. Se envía al cliente una lata de pintura azul del lote A.|  
|No específico|No seleccione un determinado número de serie o de lote cuando reserve el producto de inventario de una demanda, como, por ejemplo, un pedido de venta.<br /><br /> Es un estado que se impone en un movimiento de reserva para los números de serie o de lote que no se han seleccionado específicamente. **Nota**: La demanda no incluye números de serie o de lote. <br /><br /> Por ejemplo, desea reservar una lata de pintura azul de cualquier lote para su pedido de venta. Se envía al cliente una lata de pintura azul de un número de serie o de lote aleatorio.|  
  
La diferencia principal entre reserva específica y no específica se define por la existencia de números de serie o de lote en la demanda, tal como se muestra en la tabla siguiente.  

| Escriba            | Aprovisionamiento                | Demanda                   |
|-----------------|-----------------------|--------------------------|
| **Específico**    | Número de serie o de lote. | Número de serie o de lote.    |
| **No específico** | Número de serie o de lote. | Sin número de serie o de lote. |
  
Cuando se reservan cantidades de inventario de una línea de documento de salida para un producto que tenga asignados números de seguimiento de producto y se haya configurado para el seguimiento de producto específico, la página **Reservas** le guiará por distintos flujos de trabajo según la necesidad de números de serie o de lote.  
  
## <a name="specific-reservation"></a>Reserva específica  
Cuando elige **Reservar** en la línea de documento de salida, aparece un cuadro de diálogo en el que se le pregunta si desea reservar determinados números de serie o de lote. Si elige **Sí**, se muestra una lista con todos los números de serie o de lote asignados a la línea del documento. La página **Reservas** se abre después de seleccionar uno de los números de serie o de lote, y, a continuación, puede efectuar la reserva en los números de serie o de lote de la forma habitual.  
  
Si algunos de los números específicos de seguimiento de productos que intenta reservar están en reservas no específicas, un mensaje en la parte inferior de la página **Reservas** le indicará qué parte de la cantidad reservada total está en reservas no específicas y si aún están disponibles.  
  
## <a name="nonspecific-reservation"></a>Reserva no específica  
Si elige **Nº** en el cuadro de diálogo que aparece, se abre la página **Reservas**, donde podrá reservar entre todos los números de serie o de lote en el inventario.  
  
Dada la estructura del programa de reservas, cuando se coloca una reserva no específica en un producto con seguimiento, el sistema debe seleccionar movimientos de producto específicos con respecto a los cuales realizar la reserva. Dado que los movimientos de producto incluyen los números de seguimiento de producto, el proceso de reserva indirectamente números de serie o de lote específicos, aunque el usuario no lo quiera así específicamente. Para controlar esta situación, el sistema de reservas intenta reorganizar los movimientos de reserva no específicos antes del registro.  
  
El sistema realmente sigue reservando según los movimientos específicos, pero, después, usa un mecanismo de reorganización siempre que hay una demanda específica del número de lote o de serie en la reserva no específica. Esto puede suceder cuando se registra una transacción de demanda, como un pedido de venta, un diario de consumo o un pedido de transferencia, para el número de serie o de lote, o cuando se intenta reservar específicamente el número de serie o de lote. El programa reorganiza las reservas para que el número de lote o de serie esté disponible para la demanda o para la reserva específica, por lo que se coloca otro número de lote o de serie en la reserva no específica. Si no hay cantidad suficiente en el inventario, el sistema reorganiza lo que puede y se recibe un error de la disponibilidad si sigue habiendo cantidad insuficiente en el momento del registro.  
  
> [!NOTE]  
>  En una reserva no específica, el campo del número de lote o de serie está en blanco en el movimiento de reserva que señala la demanda, como, por ejemplo, la venta.  
  
## <a name="reshuffle"></a>Reorganizar  
Cuando un usuario registra un documento de salida después de realizar el picking con un número de serie o de lote incorrecto, se reorganizan otras reservas no específicas para reflejar el número de serie o de lote real que se ha preparado. Esto satisface el motor de registro con una liquidación fija entre el suministro y la demanda.  
  
En todos los casos empresariales admitidos, solo es posible reorganizar con respecto a movimientos de producto positivos que incluyan números de reserva y de serie o de lote pero no números de serie o de lote definidos en el lado de la demanda.  
  
## <a name="supported-business-scenarios"></a>Escenarios empresariales admitidos  
La funcionalidad de enlace posterior admite los siguientes escenarios empresariales:  
  
* Introducir un número de serie o de lote específico en un documento de salida con reserva no específica de un número de serie o de lote incorrecto.  
* Reserva de un número de serie o de lote específico.  
* Registrar un documento de salida con la reserva no específica de un número de serie o de lote.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation"></a>Registrar números de serie o de lote en un documento de salida con reserva no específica incorrecta.  
Es el más habitual de los tres escenarios admitidos. En este caso, la funcionalidad de enlace posterior garantiza que un usuario pueda introducir un número de serie o de lote, realmente seleccionado, en un documento de salida que tenga ya una reserva no específica de otro número de serie o de lote.  
  
Por ejemplo, la necesidad surge cuando un procesador de pedidos primero ha realizado una reserva no específica de cualquier número de serie o de lote. Posteriormente, cuando se hace realmente el picking del producto del inventario, en el pedido se debe especificar el número de serie o de lote de picking antes de que se registre. La reserva no específica se reorganiza en el momento del registro para garantizar que el número de serie o de lote elegido se puede introducir sin perder la reserva y para garantizar que dicho número se puede aplicar y registrar por completo.  
  
### <a name="reserve-specific-serial-or-lot-numbers"></a>Reservar un número de serie o de lote específico  
En este caso empresarial, la funcionalidad de enlace posterior garantiza que un usuario que intente reservar un número de serie o de lote determinado que no esté específicamente reservado pueda hacerlo. Una reserva no específica se organiza en el momento de reserva para liberar el número de serie o lote para la solicitud específica.  
  
La reorganización se produce automáticamente, pero la ayuda integrada se muestra en la parte inferior de la página **Reservas** y muestra el siguiente texto:  
  
**XX de la cantidad reservada total no es específica y puede estar disponible.**  
  
Además, el campo **Cantidad reservada no específica** muestra cuántos movimientos de reserva no son específicos. Por omisión, este campo no es visible para los usuarios.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers"></a>Registrar un documento de salida con la reserva no específica de los números de serie o de lote.  
Este escenario empresarial está respaldado por la funcionalidad de enlace posterior que permite la liquidación fija y el registro de salida de lo que se ha preparado realmente mediante la reorganización de otra reserva no específica de un número de serie o de lote. Si no es posible reorganizarlo, aparece el mensaje de error estándar siguiente cuando el usuario intenta registrar el envío:  
  
**El producto XX no se puede liquidar por completo.**  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]