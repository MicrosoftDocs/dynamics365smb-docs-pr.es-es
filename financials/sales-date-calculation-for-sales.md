---
title: "Cálculo de la fecha de ventas | Documentos de Microsoft"
description: "El programa calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c5cb056c7287f4c12b84dcece595a8e97c0a6214
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-sales"></a>Cálculo de fecha de ventas
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcula automáticamente la fecha más próxima posible en la que se puede enviar un producto incluido en una línea de pedido de venta.

Si el cliente solicita una fecha de entrega concreta, se calcula la fecha en que los productos deberán estar disponibles para el picking y poder realizar su entrega en dicha fecha.

Si el cliente no solicita una fecha de entrega concreta, se calcula la fecha en que los productos se podrán entregar, a partir de la fecha en que estén disponibles para el picking.

## <a name="calculating-a-requested-delivery-date"></a>Realizar cálculos de una Fecha de entrega requerida
Si escribe una fecha de entrega requerida en la línea de pedido de venta, se utilizará dicha fecha como punto inicial para los cálculos siguientes.

- Fecha entrega requerida - Hora envío = Fecha envío planeada
- Fecha envío planeada - Tiempo manip. alm. salida = Fecha envío

Si los productos están disponibles para el picking en la fecha de envío, el proceso de venta puede continuar.

Si no lo están, se mostrará la advertencia de falta de stock.

## <a name="calculating-the-earliest-possible-delivery-date"></a>Cálculo de fecha de entrega más próxima posible
Si no especifica una fecha de entrega requerida en la línea de pedido de venta, o si la fecha de entrega requerida no se puede cumplir, se calculará la fecha más próxima en la que estarán disponibles los productos. A continuación se insertará dicha fecha en la línea del campo Fecha envío y utiliza las siguientes formulas para calcular la fecha prevista para el envío de los productos y la fecha de su entrega al cliente:

- Fecha envío + Tiempo manip. alm. salida = Fecha envío planeada
- Fecha envío planeada + Hora envío = Fecha entrega planeada


## <a name="see-also"></a>Consulte también  
 [Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)   
 [Calcular fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

