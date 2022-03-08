---
title: Crear una oferta de compra para solicitar una oferta | Documentos de Microsoft
description: Describe cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 01f0f607faab45b07a85fe4cd13327b02ae14f1e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387754"
---
# <a name="request-quotes"></a>Solicitar presupuestos
Las ofertas de compra pueden utilizarse como borradores de pedidos de compra, que luego se pueden convertir en facturas de compra o en pedidos.


## <a name="to-create-a-purchase-quote"></a>Para crear una oferta de compra
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ofertas compra** y luego elija el enlace relacionado.
2. Crear un documento nuevo, de la misma forma que hace un pedido de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Para convertir una oferta de compra en un pedido de compra
Cuando haya aceptado la oferta del proveedor, puede convertirla en una factura o una orden de compra para procesar la compra.

1. Abra una oferta de compra que esté lista para convertir, y haga clic en **Convertir en pedido**.

La oferta de compra se quita de la base de datos. Se crea una factura o un pedido de compra a partir de la información en la oferta de compra en la que puede procesar la venta. En el campo **Nº oferta** de la factura de compra se muestra o pedido de compra, el número de la oferta de compra a partir de la que se creó.

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]