---
title: "Detalles de diseño: Lote por lote | Documentos de Microsoft"
description: "Aprender cómo utilizar la directiva de lote por lote para establecer la cantidad del pedido basada en la demanda."
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
ms.openlocfilehash: 2e0d1d18685f3395c31071ca9a2495c0091c564d
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-lot-for-lot"></a>Detalles de diseño: Lote por lote
La directiva de lote por lote es la más flexible porque el sistema solo reacciones ante la demanda real, además de actuar ante la demanda anticipada de los pedidos de previsión y abiertos; a continuación, liquida la cantidad del pedido según la demanda. La directiva de lote por lote está dirigida a los productos A y B, donde el inventario se puede aceptar pero se debe evitar.  
  
De algún modo, la directiva del lote por lote se parece a la directiva de pedido, pero su acercamiento a los productos es genérico; puede aceptar cantidades en el inventario y une demandas con aprovisionamientos correspondientes en ciclos definidos por el usuario.  
  
El ciclo se define en el campo **Ciclo**. El programa trabaja con un ciclo mínimo de un día, ya que es la unidad de medida de tiempo menor en los eventos de demanda y de suministro del sistema (aunque, en la práctica, la unidad de medida de tiempo en las órdenes de producción y las necesidades de componentes puede ser segundos).  
  
El ciclo también establece límites con respecto a cuándo se debe reprogramar un pedido de suministro existente para cubrir una demanda determinada. Si el aprovisionamiento entra dentro del ciclo, se volverá a programar dentro o fuera para cubrir la demanda. De lo contrario, si es anterior, se producirá una acumulación innecesaria del inventario y se debe cancelar. Si es posterior, se creará un nuevo pedido de aprovisionamiento en su lugar.  
  
Con esta directiva, también se puede definir un stock de seguridad para compensar las fluctuaciones posibles en el suministro, o para satisfacer la demanda repentina.  
  
Dado que la cantidad del pedido de aprovisionamiento se basa en la demanda real, puede tener sentido usar los modificadores de pedido: redondear la cantidad del pedido para satisfacer un múltiplo de pedido especificado (o unidad de medida de compra), incrementar el pedido a una cantidad mínima especificada o disminuir la cantidad máxima especificada (y crear así dos aprovisionamientos o más para alcanzar la cantidad total necesaria).  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
