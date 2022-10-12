---
author: edupont04
ms.topic: include
ms.date: 09/21/2022
ms.author: edupont
ms.openlocfilehash: 1ed4346dbdcbd6fc4eb5b3cde677498c9f3b5ea6
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608220"
---
Cuando abre la página **Disponibilidad prod. por variante** desde una línea del documento, puede insertar una variante en la línea del documento al seleccionar la línea con la variante que desea insertar y hacer clic en el botón Aceptar. Si solo ha utilizado la página para consultar la disponibilidad y no desea introducir una variante, cierre la página sin hacer clic en el botón Aceptar.

La página muestra una línea por cada periodo. Cada línea muestra las cifras de disponibilidad del producto en los siguientes campos clave:

| Campo | Descripción |
|--|--|
| **Necesidades brutas**| Especifica la suma de la demanda total del producto. La necesidad bruta consiste en la *demanda independiente* y la *demanda dependiente*. La *demanda independiente* incluye los pedidos de venta, pedidos de servicio, pedidos de transferencia y previsiones de producción. La *demanda dependiente* incluye los componentes de orden de producción de las órdenes planificadas, planificadas en firme y lanzadas. También incluye líneas de hojas de planificación y solicitud.|
| **Recepción programada** | Especifica la suma de los productos de las órdenes de reposición. El cálculo incluye órdenes de producción planificadas en firme y lanzadas, pedidos de compra y pedidos de transferencia. |
| **Recep. orden planif.** | Especifica la suma de productos de las órdenes de producción planificadas. |
| **Saldo disponible estimado** | Especifica el inventario disponible calculado. |
| **Planificación liberación órdenes** | Especifica la suma de los productos de las propuestas de pedidos de reposición. El cálculo incluye pedidos de producción planificados. También incluye las líneas de hojas de planificación y de demanda que se calculan según la fecha de inicio de la hoja de planificación y la orden de producción, o la fecha de la orden de la hoja de demanda. Esta suma no se incluye en el inventario disponible proyectado. No obstante, indica qué cantidades deberían convertirse de órdenes planificadas a recepciones programadas. |
