---
title: Cálculo de la fecha de entrega de las ventas
description: La aplicación calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada y disponible para picking.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: edupont
---
# Cálculo de la fecha de entrega de las ventas

[!INCLUDE[prod_short](includes/prod_short.md)] calcula automáticamente la fecha más próxima posible en la que se puede enviar un producto incluido en una línea de pedido de venta.

* Si el cliente solicita una fecha de entrega concreta, se calcula la fecha en que los productos deberán estar disponibles para el picking y poder realizar su entrega en dicha fecha.
* Si el cliente no solicita una fecha de entrega concreta, se calcula la fecha en que los productos se pueden entregar. El cálculo comienza a partir de la fecha en que los productos se pueden seleccionar.

## Calcular una fecha de entrega requerida

Si escribe una fecha de entrega requerida en la línea de pedido de venta, dicha fecha se convertirá en el punto inicial para los cálculos siguientes.

- *fecha entrega requerida - hora envío = fecha envío planeada*
- *fecha envío planeada - tiempo manip. alm. salida = fecha envío*

Si los productos están disponibles para el picking en la fecha de envío, el proceso de venta puede continuar. De lo contrario, se muestra una advertencia de falta de stock.

> [!NOTE]
> Si su proceso se basa en el cálculo hacia atrás; por ejemplo, si utiliza la fecha de entrega requerida para obtener la fecha de envío planificada, le recomendamos que utilice fórmulas de fecha con duraciones fijas, como "5D" para cinco días o "1S" para una semana. Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos. Obtenga más información sobre las fórmulas de fecha, en [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

## Calcular la fecha de entrega más próxima posible

Si no especifica una fecha de entrega requerida en la línea del pedido de venta, o si la fecha de entrega requerida no se puede cumplir, se calculará la fecha de disponibilidad de los productos más cercana. A continuación, se insertará dicha fecha en la línea del campo **Fecha envío** y con las siguientes fórmulas calculará la fecha prevista para el envío de los productos y la fecha de su entrega al cliente:

- *fecha envío + tiempo manip. alm. salida = fecha envío planeada*
- *fecha envío planeada + hora envío = fecha entrega planeada*

## Consulte la [formación de Microsoft](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/) relacionada.

## Consulte también .

[Cálculo de la fecha de las compras](purchasing-date-calculation-for-purchases.md)  
[Calcular fechas de compromiso de pedidos](sales-how-to-calculate-order-promising-dates.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
