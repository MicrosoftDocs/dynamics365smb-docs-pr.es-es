---
title: "Cómo crear pedidos de venta especiales | Documentos de Microsoft"
description: "Se puede crear un pedido especial para un determinado producto sin stock que se vaya a enviar a un cliente en particular. El proveedor envía el producto al almacén de su empresa y de allí se envía a su cliente sólo o con otros productos de otro pedido."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c7e5d7cda12abd94a999031af3bc8d505b7f6c5e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-special-orders"></a>Cómo crear pedidos especiales
Se puede crear un pedido especial para un determinado producto sin stock que se vaya a enviar a un cliente en particular. El proveedor envía el producto al almacén de su empresa y de allí se envía a su cliente sólo o con otros productos de otro pedido.  

Los pedidos especiales implican que el pedido de compra y el pedido de venta están vinculados para garantizar que se pueda realizar el picking y enviar el producto sin stock específico al cliente.  

Para utilizar esta función, primero debe tener configuradas las fichas de cliente, de proveedor y de producto necesarias para el pedido.  

## <a name="to-create-a-special-order"></a>Para crear un pedido especial  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedido de venta** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Cree un  pedido de venta del producto y rellénelo. Para obtener más información, vea [Procedimiento: Vender productos](sales-how-sell-products.md).
3.  En la ficha desplegable **Líneas**, rellene la línea de venta. En el campo **Cód. compra**, seleccione un código de compra que tenga el campo **Pedido especial** seleccionado.

    A continuación, cree un pedido de compra desde una hoja de demanda.  
4. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Hoja de demanda** y elija el vínculo relacionado.  
5. Elija la acción **Pedido especial** y, a continuación, **Traer pedidoS venta**.  
6.  En la ventana **Traer pedidos venta**, se muestran resultados en los que **Nº documento** hace referencia al número del pedido de venta. Elija el botón **Aceptar**. Se crea una línea en la hoja de demanda para el producto.  
7.  En el campo **Mensaje acción** de la línea de la hoja de demanda, seleccione **Nuevo**.  
8.  En la ventana **Hoja demanda**, haga elija la acción **Ejecutar mensajes acción**. La ventana **Ejecutar mensajes acción - Dem** se abrirá. Elija el botón **Aceptar**.  

    Aparece un mensaje para indicarle que se han creado los pedidos de compra. Elija el botón **Aceptar**.  

El sistema de planificación respeta un pedido de compra que se crea como un pedido especial para un pedido de venta a medida que hace un balance de la oferta y la demanda. Es decir, el pedido de compra (suministro) permanece asociado al pedido de venta (demanda), aunque el pedido de compra pueda cubrir otra demanda anterior. Para obtener más información, consulte [Detalles de diseño: Directivas de reaprovisionamiento](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  No puede utilizar la funcionalidad de pedido especial si el artículo ya está reservado. Por lo tanto, para los artículos que se venden en pedidos especiales, asegúrese de que el campo **Reservar** de la ficha de producto no se establezca en **Siempre**.  

## <a name="see-also"></a>Consulte también  
[Procedimiento: Trabajar con productos sin stock](inventory-how-work-nonstock-items.md)  
[Ccial](sales-manage-sales.md)  
[Procedimiento: Realizar envíos directos](sales-how-drop-shipment.md)   
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reservation-order-tracking-and-action-messaging.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

