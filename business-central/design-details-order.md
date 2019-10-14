---
title: 'Detalles de diseño: Pedido | Documentos de Microsoft'
description: Este tema proporciona información acerca de vínculos de pedido a pedido en un entorno de fabricación contra pedido.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 09ef0ab320b2f7c19c0484f05efe7b3ae1fa41f7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303121"
---
# <a name="design-details-order"></a>Detalles de diseño: Pedidos
En un entorno de fabricación contra pedido, el producto se compra o se produce para cubrir exclusivamente una demanda concreta. Normalmente, se relaciona con productos A y el motivo para elegir la política de reaprovisionamiento de pedido puede ser que la demanda se produce con poca frecuencia, el plazo es insignificante o varían los atributos requeridos.  

La aplicación crea un vínculo de pedido contra pedido, que actúa de conexión preliminar entre el suministro, un pedido de suministro o inventario, y la demanda que se va a cumplir.  

Aparte de utilizar la directiva de pedido, el vínculo de pedido a pedido se puede aplicar de las siguientes formas durante la planificación:  

* Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes necesarios en la misma orden de producción).  
* Al usar la característica de planificación de pedido de venta para crear una orden de producción a partir de un pedido de venta.  

Aunque una empresa de fabricación se considere a sí misma como entorno de fabricación contra pedido, puede ser preferible utilizar una directiva de lote por lote si los productos son puramente estándar sin variación en los atributos. Como resultado, el programa utilizará un inventario no planificado y solo acumulará los pedidos de venta con la misma fecha de envío o dentro de un ciclo definido.  

## <a name="order-to-order-links-and-past-due-dates"></a>Conexiones de pedido contra pedido y fechas vencidas  
A diferencia de la mayoría de conjuntos de suministro-demanda, el sistema ha planificado completamente los pedidos vinculados con fechas de vencimiento anteriores a la fecha inicial de planificación. El motivo empresarial de esta excepción es que los conjuntos de demanda-suministro específicos se deben sincronizar mediante la ejecución. Para obtener más información acerca de la zona congelada aplicable a la mayoría de los tipos de aprovisionamiento-demanda, consulte [Detalles de diseño: Gestión de pedidos antes de la fecha de inicio de planificación](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
