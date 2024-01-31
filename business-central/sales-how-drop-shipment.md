---
title: Hacer envíos directos (contiene vídeo)
description: Describe cómo crear un pedido de venta vinculado a un pedido de compra para habilitar el envío directo del proveedor al cliente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Realizar envíos directos

Un envío directo es el envío de los productos de uno de sus proveedores directamente a uno de sus clientes.

Cuando se marca un pedido de venta para envío directo y se crea un pedido de compra especificando el cliente en el campo **Dirección de envío**, **Dirección del cliente**, se pueden enlazar los dos documentos para indicar al proveedor que realice el envío directamente al cliente.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## Para crear un pedido de venta de envío directo

Para preparar un envío directo cree un pedido de venta para un producto e indique en la línea de ventas que dicha venta requiere un envío directo.

1. Cree un pedido de ventas para un artículo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
2. En la línea del pedido de venta del envío directo, seleccione la casilla **Envío directo**. 

> [!TIP]
> De forma predeterminada, la casilla Envío directo no está disponible en las líneas. Si no es así, puede agregarla personalizando la sección de la página que contiene las líneas. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## Para crear pedidos de compra para envíos directos

Para preparar un envío directo, debe indicar en el pedido de compra que debe enviarse a su cliente, no a usted mismo.

1. Cree un pedido de compra. No rellene ningún campo en las líneas. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
2. En el campo **Dirección de envío**, seleccione **Dirección del cliente**.
3. En el campo **Cliente**, seleccione el cliente al que está realizando la venta.
4. Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.
5. En la página **Lista ventas**, seleccione el pedido de ventas que ha preparado en [Para crear un pedido de venta de envío directo](#to-create-a-sales-order-for-drop-shipment).
6. Elija el botón **Aceptar**.

La información de la línea del pedido de venta se inserta en las líneas del pedido de compra.

Ahora puede decirle a su proveedor que envíe los artículos directamente al cliente. Por ejemplo, puede enviarles el pedido por correo electrónico. 

Si su proveedor proporciona un número de seguimiento o información similar, puede añadir esa información en una línea de orden de compra del tipo *Comentario*.  

## Para crear varios pedidos de compra para envíos directos

También puede utilizar la hoja de demanda para crear el pedido de compra para el proveedor. 

La ventaja de utilizar la hoja de demanda es que puede crear órdenes de compra para todos los envíos directos pendientes. Eso significa que no tendrá que crear cada uno individualmente.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de demanda** y luego elija el vínculo relacionado.
2. Elija la acción **Envíos directos** y, a continuación, **Traer pedido venta**.
3. Elija el botón **Aceptar**.
4. Revise las líneas del pedido de compra y, en el campo **Nº proveedor**, seleccione el proveedor que suministra los bienes necesarios. 
5. Elija la acción **Ejecutar mensajes de acción** para convertir líneas revisadas en un pedido de compra.

## Para ver el pedido de compra vinculado al pedido de venta.

* Seleccione la línea del envío directo del pedido de compra, elija las acciones **Pedido**, **Envío directo** y, a continuación, **Pedido de compra**.

## Para registrar un envío directo

Después de que el proveedor envíe los productos, puede establecer los pedidos de venta como enviados. También puede registrar el pedido de compra, pero solo con la opción **Recibir** hasta que se haya facturado el pedido de ventas.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra el pedido de venta que ha creado en [Para crear un pedido de venta de envío directo](#to-create-a-sales-order-for-drop-shipment).
3. En el campo **Cantidad a enviar**, especifiqué qué cantidad del pedido debe enviarse, todo o solo una parte.
4. Seleccione la acción **Registrar** o **Registrar y enviar**.
5. Elija la opción **Enviar** para facturar más adelante o la opción **Enviar y facturar** para facturar ahora.

## Consulte también .

[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Vender productos](sales-how-sell-products.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Ccial](sales-manage-sales.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
