---
title: Crear una oferta de compra para solicitar una oferta
description: Describe cómo crear una oferta de venta o un documento de solicitud de oferta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '49, 97, 9306, 9346'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="request-quotes"></a>Solicitar ofertas

Las ofertas de compra pueden utilizarse como borradores de pedidos de compra, que luego se pueden convertir en facturas de compra o en pedidos.

## <a name="create-a-purchase-quote"></a>Crear una oferta de compra

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ofertas de compra** y, a continuación, elija el vínculo relacionado.
2. Crear un documento nuevo, de la misma forma que hace un pedido de compra. Obtenga más información en [Registrar compras](purchasing-how-record-purchases.md).

## <a name="convert-a-purchase-quote-to-a-purchase-order"></a>Convertir una oferta de compra en un pedido de compra

Cuando haya aceptado la oferta del proveedor, puede convertirla en una orden de compra para procesar la compra.

1. Abra la oferta de compra que desea convertir y haga clic en **Convertir en pedido**.

La oferta de compra se quita de la base de datos. Se crea una factura o un pedido de compra a partir de la información en la oferta de compra, que puede utilizar para procesar la compra y, a continuación, registrar una factura de compra. En el campo **Nº oferta** del pedido de compra y la factura de compra se muestra el el número de la oferta de compra a partir de la que se crearon.

> [!NOTE]
> No es posible convertir una oferta de compra en una factura de compra directamente, como es posible con las ofertas de venta. Para obtener detalles sobre cómo crear una factura de compra, lea [Registrar compras con facturas de compra](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
