---
title: "Cómo hacer un seguimiento de las relaciones entre demanda y suministro | Documentos de Microsoft"
description: "Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1de7b6679b6b2494145654f712c3ddb3e760271e
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="track-relations-between-demand-and-supply"></a>Realizar un seguimiento de las relaciones entre demanda y suministro
Desde cualquier documento de suministro o demanda de la llamada red de pedidos, puede efectuar el seguimiento de la demanda de pedido (cantidad seguida), previsión, pedido de ventas abierto o parámetro de planificación (cantidad no seguida) que ha dado lugar a la línea de planificación en cuestión.

Las hojas de planificación también presentan información de planificación complementaria, acerca de entidades sin pedidos para ayudar al planificador a elaborar un plan de suministro óptimo. Para obtener más información, consulte la sección "Elementos de planificación sin seguimiento".

## <a name="to-track-linked-items"></a>Para seguir productos relacionados
El seguimiento de pedidos muestra cómo se relacionan los pedidos de venta, las órdenes de producción y los pedidos de compra con las órdenes de fabricación en los sistemas de planificación y reservas.

A continuación se describe cómo seguir productos asociados en una orden de producción planificada en firme. Los pasos son parecidos a los de todos los tipos de pedidos y planificación de las líneas de hoja de trabajo.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer") escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.
2. Abra la orden de producción planificada en firme pertinente de la lista.
3. En la ficha desplegable **Líneas**, elija la acción **Funciones** y, a continuación, seleccione la acción **Seguimiento de pedido**.

Las líneas de **Seguimiento de pedido** muestran los documentos que están relacionados con la línea de pedido de producción actual.

## <a name="untracked-planning-elements"></a>Elementos planificación sin seguimiento
Se abre la página **Elementos de planificación sin seguimiento** cuando elige el campo **Cantidad sin seguimiento** en la página **Planificación de pedidos**. Responde a dos propósitos:

1. Albergar información sobre cantidades sin seguimiento que se muestran cuando el usuario busca desde la página Seguimiento pedido las cantidades sin seguimiento.
2. Albergar los mensajes de advertencia que se muestran cuando el usuario selecciona el icono de **Advertencia** en la página **Hoja de planificación**.

La página contiene entradas que contabilizan la cantidad de excedentes sin seguimiento con el objeto de realizar un seguimiento de la red. Estas entradas se generan durante la ejecución de la planificación y explican la procedencia de dicha cantidad en las líneas de seguimiento de pedido. La procedencia de este excedente sin seguimiento puede ser:

- Previsión de producción
- Pedidos abiertos
- Stock de seguridad
- Punto de pedido
- Stock máximo
- Cantidad a solicitar
- Cantidad máxima pedido
- Cantidad mínima pedido
- Múltiplos de pedido
- Amort. (% tamaño lote)

## <a name="see-also"></a>Consulte también  
[Planificación](production-planning.md)   
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: Reserva, seguimiento y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

