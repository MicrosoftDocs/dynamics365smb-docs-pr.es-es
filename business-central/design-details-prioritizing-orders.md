---
title: "Detalles de diseño: Prioridad de pedidos | Documentos de Microsoft"
description: "Leer información sobre cómo dar prioridad para satisfacer los requisitos de demanda y oferta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6e09ad64750493f99210d47516410d8471a83011
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-prioritizing-orders"></a>Detalles de diseño: Prioridad de pedidos
En una UA concreta, la fecha solicitada o disponible representa la máxima prioridad; la demanda de hoy se debe tratar antes que la de la semana que viene. Pero además de esta prioridad general, el sistema de planificación sugerirá también el tipo de demanda que debe ser satisfecho antes de cubrir otra demanda. Del mismo modo, sugerirá el origen de suministro que se debe aplicar antes de aplicar otros orígenes de suministro. Esto se realice según las prioridades de pedido.  
  
La demanda y el suministro cargados contribuyen a un perfil del inventario proyectado según las prioridades siguientes:  
  
## <a name="priorities-on-the-demand-side"></a>Prioridades en la demanda  
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
  
## <a name="priorities-on-the-supply-side"></a>Prioridades en el suministro  
1. Ya en el inventario: movimiento de producto (flexibilidad de planificación = ninguna)  
2. Pedido de devolución de venta (flexibilidad de planificación = ninguna)  
3. Pedido de transferencia de entrada  
4. Orden producción  
5. Pedido de ensamblado  
6. Pedido compra  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioridad relacionada con el estado de la demanda y del suministro  
Aparte de las prioridades dadas por el tipo de demanda y aprovisionamiento, el estado actual de los pedidos en el proceso de ejecución también define una prioridad. Por ejemplo, las actividades de almacén repercuten y se tiene en cuenta el estado de los pedidos de ventas, compra, transferencia, ensamblado y órdenes de producción.  
  
1. Parcialmente controlado (flexibilidad de planificación = ninguna)  
2. Ya en proceso en el almacén (flexibilidad de planificación = ninguna)  
3. Lanzados: todos los tipos de pedido (flexibilidad de planificación = ilimitada)  
4. Orden de producción planificada en firme (flexibilidad de planificación = ilimitada)  
5. Planificado/Abierto: todos los tipos de pedido (flexibilidad de planificación = ilimitada)  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
