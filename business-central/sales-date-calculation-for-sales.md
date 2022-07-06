---
title: Cálculo de fecha de ventas
description: La aplicación calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada y disponible para picking.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 401deb016122100f86142cb2314c18e3b481bccd
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077871"
---
# <a name="date-calculation-for-sales"></a>Cálculo de fecha de ventas

[!INCLUDE[prod_short](includes/prod_short.md)] calcula automáticamente la fecha más próxima posible en la que se puede enviar un producto incluido en una línea de pedido de venta.

Si el cliente solicita una fecha de entrega concreta, se calcula la fecha en que los productos deberán estar disponibles para el picking y poder realizar su entrega en dicha fecha.

Si el cliente no solicita una fecha de entrega concreta, se calcula la fecha en que los productos se podrán entregar, a partir de la fecha en que estén disponibles para el picking.

## <a name="calculating-a-requested-delivery-date"></a>Realizar cálculos de una Fecha de entrega requerida

Si escribe una fecha de entrega requerida en la línea de pedido de venta, dicha fecha se convertirá en el punto inicial para los cálculos siguientes.

- Fecha entrega requerida - Hora envío = Fecha envío planeada
- Fecha envío planeada - Tiempo manip. alm. salida = Fecha envío

Si los productos están disponibles para el picking en la fecha de envío, el proceso de venta puede continuar. De lo contrario, se muestra una advertencia de falta de stock.

> [!Note]
> Si su proceso se basa en el cálculo hacia atrás, por ejemplo, si utiliza la fecha de entrega solicitada para obtener la fecha de envío planificada, le recomendamos que utilice fórmulas de fecha que tengan duraciones fijas, como "5D" para cinco días o "1S" para una semana. Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos. Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Cálculo de fecha de entrega más próxima posible

Si no especifica una fecha de entrega requerida en la línea de pedido de venta, o si la fecha de entrega requerida no se puede cumplir, se calculará la fecha más próxima en la que estarán disponibles los productos. A continuación se insertará dicha fecha en la línea del campo Fecha envío y utiliza las siguientes formulas para calcular la fecha prevista para el envío de los productos y la fecha de su entrega al cliente:

- Fecha envío + Tiempo manip. alm. salida = Fecha envío planeada
- Fecha envío planeada + Hora envío = Fecha entrega planeada

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

 [Cálculo de la fecha de las compras](purchasing-date-calculation-for-purchases.md)  
 [Calcular fechas de compromiso de pedidos](sales-how-to-calculate-order-promising-dates.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]