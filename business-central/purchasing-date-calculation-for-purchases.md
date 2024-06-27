---
title: Calcular las fechas de compras
description: Este artículo describe cómo puede calcular las fechas para las compras.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 04/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="calculate-dates-for-purchases"></a>Calcular las fechas de compras

Si quiere tener artículos en el inventario en una fecha determinada, [!INCLUDE[prod_short](includes/prod_short.md)] puede calcular automáticamente la fecha en la que debe pedirlos. 

El resultado es la fecha en la que puede recoger los artículos que ha pedido.  

Si especifica una fecha de recepción solicitada en una línea de pedido de compra, la fecha de pedido calculada es la fecha en la que debe realizar el pedido. La fecha en que los artículos estarán disponibles para su recogida se muestra en el campo **Fecha recepción esperada**.  

Si no especifica una fecha de recepción solicitada, la fecha en que espera recibir los artículos se basa en la fecha del pedido en la línea. 

La fecha de recepción es también la fecha en que los artículos estarán disponibles para su recogida.  

> [!TIP]
> De forma predeterminada, muchos de los campos de fecha que se mencionan en este artículo están ocultos en las líneas del pedido de compra. Si un campo no está disponible, puede agregarlo personalizando la página. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a>Realizar cálculos con una fecha de recepción solicitada

Si hay una fecha de recepción solicitada en la línea de pedido de compra, esa fecha se utiliza como base de los cálculos siguientes:  

- fecha de recepción solicitada – plazo entrega (días) = fecha de pedido  
- fecha recepción solicitada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada  

Si especifica una fecha de recepción solicitada en una línea de pedido de compra, esa fecha se asigna a las nuevas líneas a medida que las crea. Puede cambiar o eliminar las dimensiones en las líneas.  

> [!NOTE]
> Si su proceso se basa en el cálculo hacia atrás, por ejemplo, si utiliza la fecha de recepción solicitada para obtener la fecha de pedido, le recomendamos que utilice fórmulas de fecha que tengan duraciones fijas, como "5D" para cinco días o "1S" para una semana. Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos. Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date"></a>Realizar cálculos sin una fecha de recepción solicitada

Si especifica una línea de pedido de compra sin una fecha de recepción requerida, el campo **Fecha pedido** de la línea muestra la fecha del campo **Fecha pedido** de la cabecera del pedido de compra. Se trata de la fecha que especificó o la fecha del trabajo. Se utiliza la fecha del pedido como punto inicial para calcular las fechas siguientes de la línea del pedido de compra, como sigue.  

- fecha pedido + plazo entrega (días) = fecha recepción planificada.  
- fecha recepción planificada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada  

Si cambia la fecha del pedido en la línea, [!INCLUDE[prod_short](includes/prod_short.md)] vuelve a calcular las otras fechas.  

## <a name="default-values-for-lead-time-calculation"></a>Valores predeterminados para el cálculo del tiempo de entrega

[!INCLUDE[prod_short](includes/prod_short.md)] usa la fórmula de fecha en el campo **Cálculo del plazo de entrega** en la línea del pedido de compra para calcular el pedido y las fechas de recepción esperadas.  

Puede especificar manualmente la fórmula de fecha en las líneas. De lo contrario, [!INCLUDE[prod_short](includes/prod_short.md)] utilizará las fórmulas que se definen en las páginas siguientes en este orden de prioridad:

1. Producto - Lista proveedores
2. Ficha producto
3. Ficha ud. de almacenam.
4. Ficha proveedor

## <a name="see-also"></a>Consulte también .

[Cálculo de fecha de ventas](sales-date-calculation-for-sales.md)  
[Calcular fechas de compromiso de pedido](sales-how-to-calculate-order-promising-dates.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
