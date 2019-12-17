---
title: Cálculo de la fecha de compra | Documentos de Microsoft
description: La aplicación calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 27442dc72356570e9e8e2d3030bbb9180fb17e23
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877620"
---
# <a name="date-calculation-for-purchases"></a>Cálculo de la fecha de compras
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.  

Si especifica una fecha de recepción solicitada en la cabecera de un pedido de compra, la fecha de pedido calculada será aquella en la que se debe realizar el pedido para recibir los artículos en la fecha solicitada. A continuación, la fecha en que los artículos estarán disponibles para picking se calcula y se especifica en el campo **Fecha recepción esperada**.  

Si no especifica una fecha de recepción esperada, se utiliza la fecha de pedido de la línea como punto inicial para calcular la fecha en la que se espera recibir los productos y la fecha en la que estarán disponibles para picking.  

## <a name="calculating-with-a-requested-receipt-date"></a>Realizar cálculos con una fecha de recepción solicitada  
Si hay una fecha de recepción solicitada en la línea de pedido de compra, esa fecha se utiliza como punto inicial de los cálculos siguientes.  

- fecha de recepción solicitada – plazo entrega (días) = fecha de pedido  
- fecha recepción solicitada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada  

Si introdujo una fecha de recepción solicitada en la cabecera del pedido de compra, se copia al campo correspondiente en todas las líneas. Puede modificarla o eliminarla en cualquiera de las líneas.  

> [!Note]
> Si su proceso se basa en el cálculo hacia atrás, por ejemplo, si utiliza la fecha de recepción solicitada para obtener la fecha de pedido, le recomendamos que utilice fórmulas de fecha que tengan duraciones fijas, como "5D" para cinco días o "1S" para una semana. Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos. Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Realizar cálculos sin una fecha de entrega requerida  
Si especifica una línea de pedido de compra sin una fecha de entrega solicitada, se rellena el campo **Fecha pedido** de la línea con la fecha del campo **Fecha pedido** de la cabecera del pedido de compra. Se trata de la fecha que especificó o la fecha del trabajo. Se utiliza la fecha del pedido como punto inicial para calcular las fechas siguientes de la línea del pedido de compra.  

- fecha pedido + plazo entrega (días) = fecha recepción planificada.  
- fecha recepción planificada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada  

Si modifica la fecha de pedido de la línea, por ejemplo, cuando el proveedor no va tener los productos disponibles sino para una fecha posterior, se vuelven a calcular automáticamente las fechas correspondientes de la línea.  

Si modifica la fecha de pedido de la cabecera, se copia en el campo **Fecha pedido** de todas las líneas y se vuelven a calcular todos los campos de fecha relacionados.  

## <a name="see-also"></a>Consulte también  
 [Cálculo de fecha de ventas](sales-date-calculation-for-sales.md)   
 [Calcular fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
