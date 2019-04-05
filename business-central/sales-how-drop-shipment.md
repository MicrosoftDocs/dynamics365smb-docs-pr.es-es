---
title: Asociar un pedido de venta a un pedido de compra para un envío directo | Documentos de Microsoft
description: Describe cómo crear un pedido de venta vinculado a un pedido de compra para habilitar el envío directo del proveedor al cliente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 77bed1563a5c0187e78f7e7013dfed4a723d7702
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806139"
---
# <a name="make-drop-shipments"></a>Realizar envíos directos
Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.

Cuando marca un pedido de venta con el envío directo y crea un pedido especificando el cliente en el campo **Venta a-N.º cliente** puede vincular los dos documentos y así asignar instrucciones al proveedor para que envíe el producto directamente al cliente.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Para crear un pedido de venta de envío directo
Para preparar un envío directo cree un pedido de venta como si fuese normal, pero indique en la línea de ventas que dicha venta requiere un envío directo.

1. Cree un pedido de ventas para un artículo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
2. En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**. Use la función **Elegir columnas** si el campo no está visible. Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Para crear pedidos de compra para envíos directos
Para preparar un envío directo de un producto que se va a vender, cree un pedido de compra como si fuese normal, pero indique en el pedido que el producto debe enviarse directamente al cliente no a usted.

1. Cree un pedido de compra. No rellene ningún campo en las líneas. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
2. En el campo **Venta a-N.º cliente**, seleccione el cliente al que le está vendiendo.
3. Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.
4. En la página **Lista ventas**, seleccione el pedido de ventas que ha preparado en [Para crear un pedido de venta de envío directo](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Elija el botón **Aceptar**.

La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.

Ahora puede asignar instrucciones al proveedor para que envíe los productos al cliente, por ejemplo, enviando el pedido de compra por correo electrónico en formato PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Para ver el pedido de compra vinculado al pedido de venta.
* Seleccione la línea del envío directo del pedido de compra, elija las acciones **Pedido**, **Envío directo** y, a continuación, **Pedido de compra**.

## <a name="to-post-a-drop-shipment"></a>Para registrar un envío directo
Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados. También puede registrar el pedido de compra, pero solo con la opción **Recibir** hasta que se haya facturado el pedido de ventas.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.
2. Abra el pedido de venta que ha creado en [Para crear un pedido de venta de envío directo]().
3. En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.
4. Seleccione la acción **Registrar** o **Registrar y enviar**.
5. Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.

## <a name="see-also"></a>Consulte también
[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Vender productos](sales-how-sell-products.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Ventas](sales-manage-sales.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
