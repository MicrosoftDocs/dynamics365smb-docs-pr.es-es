---
title: Cómo crear pedidos especiales
description: Aprenda a crear un pedido especial para un determinado producto del catálogo que se vaya a enviar a un cliente en particular.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Crear pedidos especiales

Se puede crear un pedido especial para un determinado producto del catálogo que se vaya a enviar a un cliente en particular. El proveedor envía el producto al almacén de su empresa y de allí se envía a su cliente sólo o con otros productos de otro pedido.  

Los pedidos especiales implican que el pedido de compra y el pedido de venta están vinculados para garantizar que se pueda realizar el picking y enviar el producto del catálogo específico al cliente.  

Para utilizar esta función, primero debe tener configuradas las fichas de cliente, de proveedor y de producto necesarias para el pedido.  

## Para crear un pedido especial

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedido venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Cree un  pedido de venta del producto y rellénelo. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
3.  En la ficha desplegable **Líneas**, rellene la línea de venta. En el campo **Cód. compra**, seleccione un código de compra que tenga el campo **Pedido especial** seleccionado.

    A continuación, cree un pedido de compra desde una hoja de demanda.  
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja de demanda** y luego elija el enlace relacionado.  
5. Elija la acción **Pedido especial** y, a continuación, **Traer pedidoS venta**.  
6.  En la página **Traer pedidos venta**, se muestran resultados en los que **Nº documento** hace referencia al número del pedido de venta. Elija el botón **Aceptar**. Se crea una línea en la hoja de demanda para el producto.  
7.  En el campo **Mensaje acción** de la línea de la hoja de demanda, seleccione **Nuevo**.  
8.  En la página **Hoja de demanda**, elija la acción **Ejecutar mensajes de acción**. La página **Ejecutar mensajes acción - Dem.** se abrirá. Elija el botón **Aceptar**.  

    Aparece un mensaje para indicarle que se han creado los pedidos de compra. Elija el botón **Aceptar**.  

El sistema de planificación respeta un pedido de compra que se crea como un pedido especial para un pedido de venta a medida que hace un balance de la oferta y la demanda. Es decir, el pedido de compra (suministro) permanece asociado al pedido de venta (demanda), aunque el pedido de compra pueda cubrir otra demanda anterior. Para obtener más información, consulte [Detalles de diseño: Directivas de reaprovisionamiento](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  No puede utilizar la funcionalidad de pedido especial si el artículo ya está reservado. Por lo tanto, para los artículos que se venden en pedidos especiales, asegúrese de que el campo **Reservar** de la ficha de producto no se establezca en **Siempre**.  

## Consulte también .

[Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md)  
[Ventas](sales-manage-sales.md)  
[Realizar envíos directos](sales-how-drop-shipment.md)   
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reservation-order-tracking-and-action-messaging.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
