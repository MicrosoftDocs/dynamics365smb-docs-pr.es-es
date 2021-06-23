---
title: 'Detalles de diseño: registros de seguimiento de productos históricos frente a activos | Documentos de Microsoft'
description: Cuando se registran partes de una cantidad de línea de documento, solo dicha cantidad concreta se transfiere a los movimientos de producto y sus números de seguimiento de producto. No obstante, le interesará acceder a toda la información de seguimiento del producto relevante directamente desde la línea activa del documento. Es decir, no solo desea ver los movimientos que están relacionados con la cantidad restantes, sino que también desea información sobre las unidades que se han registrado. Cuando consulte o modifique la página **Líns. seguim. prod.**, el contenido colectivo de las tablas **Especificación seguimiento** (T336) y **Mov. reserva** (T337) se presentan en una versión temporal de T336. De este modo se garantiza que se obtiene acceso a los datos de seguimiento de producto históricos y activos como una sola unidad.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 587c396bece9437e170912dc523bebb04a39e1e4
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216033"
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Detalles de diseño: registros de seguimiento de productos históricos frente a activos
Cuando se registran partes de una cantidad de línea de documento, solo dicha cantidad concreta se transfiere a los movimientos de producto y sus números de seguimiento de producto. No obstante, le interesará acceder a toda la información de seguimiento del producto relevante directamente desde la línea activa del documento. Es decir, no solo desea ver los movimientos que están relacionados con la cantidad restantes, sino que también desea información sobre las unidades que se han registrado. Cuando consulte o modifique la página **Líns. seguim. prod.**, el contenido colectivo de las tablas **Especificación seguimiento** (T336) y **Mov. reserva** (T337) se presentan en una versión temporal de T336. De este modo se garantiza que se obtiene acceso a los datos de seguimiento de producto históricos y activos como una sola unidad.  

 En la tabla siguiente se muestra cómo se usan T336 y T337 en un escenario de compra. Las cifras en negrita representan los valores que el usuario especifica manualmente en la página **Líns. seguim. prod.**  

 Paso 1: cree una línea de pedido de compra de siete piezas con los números de seguimiento de producto.  

||**Cantidad (base)**|**Cdad. a manipular**|**Cdad. a facturar (base)**|**Cdad. manipulada (Base)**|**Cdad. facturada (Base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Paso 2: reciba cuatro piezas.  

||**Cantidad (base)**|**Cdad. a manipular**|**Cdad. a facturar (base)**|**Cdad. manipulada (Base)**|**Cdad. facturada (Base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Página **Líns. seguim. prod. almacén**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Paso 3: reciba dos piezas y facture dos piezas.  

||**Cantidad (base)**|**Cdad. a manipular**|**Cdad. a facturar (base)**|**Cdad. manipulada (Base)**|**Cdad. facturada (Base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Página **Líns. seguim. prod. almacén**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Paso 4: reciba una pieza.  

||**Cantidad (base)**|**Cdad. a manipular**|**Cdad. a facturar (base)**|**Cdad. manipulada (Base)**|**Cdad. facturada (Base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Página **Líns. seguim. prod. almacén**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Facturar 5 piezas.  

||**Cantidad (base)**|**Cdad. a manipular**|**Cdad. a facturar (base)**|**Cdad. manipulada (Base)**|**Cdad. facturada (Base)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Página **Líns. seguim. prod. almacén**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)   
 [Detalles de diseño: página Líns. seguim. prod.](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]