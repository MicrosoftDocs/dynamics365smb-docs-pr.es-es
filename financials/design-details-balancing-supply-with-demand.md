---
title: "Detalles de diseño: Equilibrio de aprovisionamiento con demanda | Documentos de Microsoft"
description: "El núcleo del sistema de planificación implica el equilibrio de la demanda y del suministro mediante la sugerencia de acciones de usuario para revisar los pedidos de suministro en caso de que se produzca un desequilibrio. Se produce por la combinación de variante y de ubicación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5020c048373f10e72e40f0c9b1e5a11fc45eedb5
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-balancing-supply-with-demand"></a>Detalles de diseño: Equilibrio de aprovisionamiento con demanda
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
  
## <a name="rules-concerning-actions-for-supply-events"></a>Reglas relativas a las acciones para los eventos de suministro  
Cuando el sistema de planificación realiza un cálculo descendente en el que el suministro debe satisfacer la demanda, esta se toma tal como se indica, es decir, está fuera del control del sistema de planificación. No obstante, el lado de aprovisionamiento sigue pudiéndose gestionar. Por lo tanto, el sistema de planificación sugerirá la creación de nuevos pedidos de suministro, reprogramar los existentes o cambiar la cantidad del pedido. Si un pedido de aprovisionamiento existente pasa a ser superfluo, el sistema de planificación sugiere que el usuario lo cancele.  
  
Si el usuario desea excluir un pedido de aprovisionamiento existente de las sugerencias de planificación, puede indicar que no tiene flexibilidad de planificación (flexibilidad de planificación = ninguna). A continuación, el exceso de suministro del pedido se usará para satisfacer la demanda, pero no se sugerirá ninguna acción.  
  
En general, todo el aprovisionamiento tiene una flexibilidad de planificación limitada por las condiciones de cada una de las acciones sugeridas.  
  
-   **Reprogramar fuera**: fecha de un pedido de suministro existente que se puede excluir de la programación para cumplir la fecha de vencimiento de demanda a menos que:  
  
    -   Representa el inventario (siempre en el día cero).  
    -   Tiene una directiva pedido a pedido vinculada a otra demanda.  
    -   Se encuentra fuera de la ventana de reprogramación definida por el ciclo.  
    -   Hay un suministro más aproximado que se podría usar.  
    -   Por otro lado, el usuario puede decidir no reprogramar porque:  
    -   El pedido de suministro ya se ha vinculado a otra demanda en una fecha anterior.  
    -   La reprogramación necesaria es tan mínima que el usuario la considera insignificante.  
  
-   **Reprogramar dentro**: fecha de un pedido de suministro existente que se puede incluir en la programación, excepto con las condiciones siguientes:  
  
    -   Está vinculada directamente a otra demanda.  
    -   Se encuentra fuera de la ventana de reprogramación definida por el ciclo.  
  
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
  
## <a name="determining-the-supply-quantity"></a>Configuración de la cantidad de aprovisionamiento  
Los parámetros de planificación definidos por el usuario controlan la cantidad sugerida de cada pedido de suministro.  
  
Cuando el sistema de planificación calcula la cantidad de un nuevo pedido de suministro o el cambio de cantidad de uno existente, la cantidad sugerida puede ser distinta de la demanda real.  
  
Si se seleccionan un inventario máximo o una cantidad de pedido fija, la cantidad sugerida se puede aumentar para coincidir con esa cantidad fija o ese inventario máximo. Si una directiva de reaprovisionamiento utiliza una punto de pedido, la cantidad se puede aumentar para llegar al menos al punto de pedido.  
  
 La cantidad sugerida se puede modificar en esta secuencia:  
  
1. Hasta la cantidad de pedido máxima (si la hay).  
2. Hasta la cantidad de pedido mínima.  
3. Hasta cumplir el múltiplo de pedido más próximo. (En caso de configuración errónea, se podría infringir la cantidad máxima de pedido).  
  
## <a name="order-tracking-links-during-planning"></a>Conexiones de seguimiento de pedidos durante la planificación  
En cuanto al seguimiento de pedidos durante la planificación, es importante mencionar que el sistema de planificación reorganiza los vínculos de seguimiento de pedidos dinámicamente creados para las combinaciones de producto, variante o almacén.  
  
Existen dos motivos para esto:  
  
-   El sistema de planificación debe poder justificar las sugerencias, que toda la demanda quede cubierta y que ningún pedido de suministro sea superfluo.  
-   Los vínculos de seguimiento de pedidos creados dinámicamente deben volverse a equilibrar con regularidad.  
  
Con el tiempo, las conexiones de seguimiento de pedidos se descuadran porque la red completa de seguimiento de pedidos no se reorganiza hasta que un evento de demanda o de suministro se cierre realmente.  
  
Antes de cuadrar el aprovisionamiento por la demanda, el programa elimina todos los vínculos de seguimiento de pedidos existentes. A continuación, durante el procedimiento de contrapartida, cuando se cierra un evento demanda o de suministro, establece nuevos vínculos de seguimiento de pedidos entre la demanda y el suministro.  
  
> [!NOTE]  
>  Aunque el producto no se haya configurado para seguimiento dinámico de pedidos, el programa previsto establecerá vínculos de seguimiento de pedidos equilibrados, tal y como se ha explicado anteriormente.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
