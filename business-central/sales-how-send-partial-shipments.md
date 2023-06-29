---
title: Procesar envíos parciales
description: Los envíos de pedidos de venta se pueden procesar en Business Central con envíos parciales utilizando los campos Aviso envío y Cdad. a enviar.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: a-reishima
---
# <a name="process-partial-shipments"></a><a name="process-partial-shipments"></a><a name="process-partial-shipments"></a>Procesar envíos parciales

En un envío parcial, un pedido no se envía todo a la vez. Por ejemplo, en un pedido de 100 unidades, se envían 40 unidades inmediatamente y 60 unidades más adelante. No hay límite en el número de envíos que se pueden utilizar para un pedido.

Sin embargo, antes de poder utilizar envíos parciales en [!INCLUDE [prod_short](includes/prod_short.md)], debe especificar que el cliente acepta envíos parciales configurando el campo **Aviso envío** en la página **Ficha de cliente**. Alternativamente, si el cliente generalmente solo acepta envíos completos pero luego solicita o acepta un envío parcial para un pedido de venta específico, puede cambiar el campo **Aviso envío** antes de registrar.

De forma predeterminada, [!INCLUDE [prod_short](includes/prod_short.md)] establece el campo en la página **Ficha de cliente** como **Parcial**, que permite envíos parciales. Sin embargo, si el campo se ha ajustado para especificar **Completo**, el campo **Cdad. a enviar** está bloqueado en pedidos de venta para ese cliente.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Vender productos con un pedido de venta de cliente](sales-how-sell-products.md)  
[Enviar productos](warehouse-how-ship-items.md)  
[Realizar envíos directos](sales-how-drop-shipment.md)  
[Ccial](sales-manage-sales.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
