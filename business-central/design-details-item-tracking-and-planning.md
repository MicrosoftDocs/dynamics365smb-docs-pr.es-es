---
title: 'Detalles de diseño: Seguimiento de productos y planificación | Documentos de Microsoft'
description: 'Dado que se almacenan en el programa de reservas, los números de seguimiento de producto se coordinan completamente con los registros de seguimiento de pedidos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-and-planning"></a><a name="design-details-item-tracking-and-planning"></a><a name="design-details-item-tracking-and-planning"></a><a name="design-details-item-tracking-and-planning"></a>Detalles de diseño: Seguimiento de productos y planificación
Dado que se almacenan en el programa de reservas, los números de seguimiento de producto se coordinan completamente con los registros de seguimiento de pedidos. Esto significa que a los productos con registros de seguimiento de pedido se les pueden asignar números de seguimiento de producto. Por el contrario, los productos que tienen número de seguimiento de producto pueden convertirse en registros de seguimiento de pedido. Para obtener más información, consulte [Detalles de diseño: Diseño de seguimiento de producto](design-details-item-tracking-design.md).

Para obtener más información acerca de los sistemas integrados, consulte [Detalles de diseño: Reserva, seguimiento de pedido y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).

Dado que el seguimiento de pedidos hace referencia únicamente a la aplicación específica de un producto, la coordinación con los números de seguimiento de producto solo se aplica a los productos configurados para hacer seguimiento de productos específicos. Esto lo establecen los campos **Seguimiento específico de SN** y **Seguimiento de lote específico** en la ficha de producto, que especifican lo siguiente:

- Cuando se registre, el producto debe llevar un número de serie o de lote.
- Cuando se registre como salida, el producto se debe aplicar al mismo número de serie o de lote.

En consonancia con los principios de equilibrado de aprovisionamiento/demanda estándar, el sistema de planificación y la función de seguimiento de pedidos relacionada solo emparejan aprovisionamientos y demandas con números de seguimiento de productos si el producto en cuestión utiliza el seguimiento de productos específico. En todos los demás casos, los sistemas de planificación y seguimiento de pedidos ignoran los números de seguimiento de productos al aplicar aprovisionamientos para satisfacer la demanda o aplicar la demanda al aprovisionamiento. Para obtener más información, consulte [Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md).

Por ejemplo, cuando hay un seguimiento de pedido para un producto determinado, esto implica que los registros para el producto ya están en la tabla **Mov. reserva**, que es el núcleo del programa de reservas, antes de que se definan los números de seguimiento de productos. Por lo tanto, se aplican las siguientes restricciones de acoplamiento a los números de seguimiento de producto de los que se realiza el seguimiento de pedido:

- La demanda con un número de serie o un número de lote puede cubrir solo el aprovisionamiento con el mismo número de serie o número de lote.
- La demanda sin un número de serie o un número de lote puede cubrir cualquier aprovisionamiento, con o sin número de serie o de lote.

Aparte de sus consecuencias en el seguimiento dinámico de pedidos, las restricciones al acoplamiento del seguimiento de productos no afectan significativamente al sistema de planificación.

En el suministro, por lo general, no se especifica un número de serie o de lote hasta inmediatamente antes de que se registre el pedido, como, por ejemplo, un albarán de compra en el almacén. Al especificar un número de serie o de lote en el lado de demanda, como, por ejemplo, en un pedido de venta, dicho número de serie o de lote ya está en inventario. Por consiguiente, los números de seguimiento de productos no se suelen un problema en la planificación de aprovisionamientos.

En el caso de productos que utilizan seguimiento de productos específico, todas las demandas que lleven números de serie o de lote deben coincidir con el aprovisionamiento correspondiente. En la mayoría de los casos, no tiene sentido reaprovisionar un número de serie o de lote específico, de modo que los aprovisionamientos de compra o de producción probablemente no se verán afectados. No obstante, al transferir productos desde un almacén a otro, es probable que la transferencia se produzca para un lote específico, por lo que la planificación de los aprovisionamientos de transferencia puede verse afectada por la restricción específica de emparejamiento.

Para obtener más información, consulte [Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a><a name="balancing-demand-and-supply"></a><a name="balancing-demand-and-supply"></a><a name="balancing-demand-and-supply"></a>Equilibrado de aprovisionamiento y demanda
Si un producto requiere un seguimiento específico, se crea un vínculo de seguimiento de pedido desde toda la demanda de seguimiento del producto a cualquier aprovisionamiento del mismo que corresponda, con la única limitación de que el aprovisionamiento deberá ir antes de la demanda. Si, en estas circunstancias, no se encuentra ningún aprovisionamiento de seguimiento de productos correspondiente a la demanda con seguimiento específico de productos, se crea un nuevo aprovisionamiento de seguimiento de productos inmediatamente sin tener cuenta el tamaño de pedido, los parámetros de planificación o la reprogramación del aprovisionamiento existente con el mismo número de serie o de lote.

Si los números de seguimiento de productos se asignan en el lado de la demanda o en el lado del aprovisionamiento sin requerir seguimiento de productos específico, se crea un vínculo de seguimiento de pedidos desde la demanda con ese aprovisionamiento y en función de la sincronización y la cantidad más convenientes, tal y como ocurre con el procedimiento de contrapartida normal. El número de seguimiento de producto especificado se incorpora al registro de seguimiento de pedidos de la misma forma que cualquier cantidad de seguimiento de producto especificada define un extremo de la conexión de seguimiento de pedidos. Esto significa que se mantiene el número de seguimiento de producto que se ha introducido, a la vez que también forma parte del registro de seguimiento de pedidos.

Si los números de seguimiento de productos se asignan en el lado del aprovisionamiento sin requerir seguimiento de productos específico, el sistema de planificación considera fijo este aprovisionamiento. No se sugiere ningún cambio de tamaño o de programación para este suministro, pero se tiene en cuenta cuando el sistema de planificación intenta cumplir las necesidades brutas.

Para obtener información detallada, consulte [Detalles de diseño: Equilibrado de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Detalles de diseño: Diseño de seguimiento de productos](design-details-item-tracking-design.md)  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)  
[Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
