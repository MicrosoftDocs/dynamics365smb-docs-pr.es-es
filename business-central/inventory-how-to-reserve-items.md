---
title: Cómo reservar productos | Documentos de Microsoft
description: Puede reservar productos para pedidos de venta, pedidos de compra, y órdenes de producción. Puede reservar productos del inventario o de entrada en líneas de documento abiertas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 531489dddc80530b1d2c33a828388a90784db6c0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806521"
---
# <a name="reserve-items"></a>Reservar artículos
Puede reservar productos para pedidos de venta, pedidos de servicio, pedidos de ensamblado y órdenes de producción. Puede reservar productos del inventario o de entrada en líneas de diario abiertas. El trabajo se realiza en la página **Reservas**.

Cada línea de la página **Reservas**, que se abre para reservar productos, muestra información sobre un tipo de línea (venta, compra, diario) o entrada de inventario. Las líneas describen cuántos productos están disponibles para reservarse desde cada tipo de línea o movimiento.

## <a name="to-reserve-items-for-sales"></a>Para reservar productos para venta
A continuación se describe cómo reservar productos de un pedido de venta. Los pasos son similares para pedidos de compra, de servicio y de ensambado.  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  En la ficha desplegable **Líneas** de un pedido de venta, elija la acción **Reservar**. Se abre la página **Reserva**.  
3. Seleccione la línea de la que desea reservar los productos.  
4. Elija una de las siguientes acciones.  

    |**Acciones**|**Descripción**|
    |------------------|---------------------|  
    |**Reserva automática**|Para reservar productos automáticamente en la página **Reserva**.|  
    |**Reserva desde la línea actual**|Para reservar los productos desde la línea seleccionada del documento.|  
    |**Cancelación de reserva desde la línea actual**|Para anular la reserva de los productos desde la línea seleccionada del documento.|

> [!NOTE]  
>  Si existen líneas de seguimiento de producto para el pedido de venta, el programa de reservas le guiará por los pasos especiales. Para obtener más información, consulte [Para reservar un número de serie o de lote específico](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Para reservar un producto para una línea de orden de producción  
Puede reservar productos para órdenes de producción. Tiene que distinguir entre las líneas de la orden de producción, que implica el producto principal, y los componentes de la misma.

En el siguiente procedimiento, se utiliza una orden de producción planificada en firme.   
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer") escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.  
2. Abra la orden de producción planificada en firme para la que desee reservar productos principales.  
3. Seleccione la línea de la orden de producción pertinente.  
4. En la ficha desplegable **Líneas**, seleccione la acción **Reservar**,
5. En la página **Reserva**, seleccione la línea **Lín. venta, Pedido** y, a continuación, la acción **Reservar desde la línea actual**.  

Ahora se reserva la cantidad introducida en la línea de la orden de producción planificada en firme.

## <a name="to-reserve-items-for-production-order-components"></a>Para reservar productos para los componentes de la orden de producción  
Puede reservar productos para órdenes de producción. Tiene que distinguir entre las líneas de la orden de producción, que implica el producto principal, y los componentes de la misma.

En el siguiente procedimiento, se utiliza una orden de producción planificada en firme.    
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer") escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.  
2. Abra la orden de producción planificada en firme para la que desee reservar componentes.  
3. Seleccione la línea de la orden de producción pertinente.  
4. En la ficha desplegable **Líneas**, elija **Línea** y luego seleccione **Componentes**.  
5. Seleccione la línea de componentes correspondiente.  
6. En la ficha desplegable **Líneas**, seleccione la acción **Reservar**,  
7. En la página **Reserva**, seleccione una línea y, a continuación, la acción **Reservar desde la línea actual**.  

Ahora se reserva la cantidad introducida en la línea de componentes de producción planificada en firme.

## <a name="to-change-a-reservation"></a>Para modificar una reserva  
En ocasiones, quizá le interese modificar la reserva de un producto.   
1. Desde la línea de documento de la que se ha reservado, en la ficha desplegable **Líneas**, seleccione la acción **Reserva**.  
2. En la página **Reservas**, seleccione la acción **Movs. reserva**.
3. La página **Movs. reserva**, actualice el campo **Cantidad** de la línea que vaya a modificar.
4. Confirme el mensaje que aparece, eligiendo el botón **Acep.**.

## <a name="to-cancel-a-reservation"></a>Para cancelar una reserva  
En ocasiones, quizá le interese eliminar la reserva de un producto.   
1. Desde la línea de documento de la que desee cancelar una reserva, en la ficha desplegable **Líneas**, seleccione la acción **Reservar**.  
2. En la página **Reservas**, seleccione la acción **Movs. reserva**.  
3.  En la página **Movs. reserva**, elija la acción **Cancelar reserva**.  
4.  Confirme el mensaje que aparece, eligiendo el botón **Acep.**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Para reservar un número de serie o de lote específico  
De los documentos de salida para los productos marcados para seguimiento, como pedidos de venta o listas de componentes de producción, puede reservar números de serie o de lote específicos. Esto puede resultar útil, por ejemplo, si necesita componentes de producción de un lote específico por coherencia con lotes anteriores de producción, o porque un cliente ha solicitado un número de serie específico. Para obtener más información, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

Esto se denomina reserva específica, porque se reserva de la cantidad de producto X que pertenece al lote X. Si simplemente reserva de las cantidades de producto X, es una reserva normal, no específica. Para obtener más información, consulte [Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md).

El procedimiento siguiente se basa en un pedido de venta.    
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego seleccione el enlace relacionado.  
2. Cree una línea de pedido de venta para un producto marcado para seguimiento.  
3. Asigne números de serie y de lote a la línea de pedido de venta. Para obtener más información, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).
4. En la línea del pedido de ventas, seleccione la acción **Reservar**.  
5. Elija el botón **Sí** para reservar números de serie o lote específicos.  
6. En la página **Lista seguimiento producto**, seleccione la combinación de números de serie y lote que acaba de asignar.  
7. Elija el botón **Aceptar** para abrir la página **Reserva** que muestra solo el suministro con el número de seguimiento del producto especificado. Si existe alguna reserva no específica de cualquiera de los números de seguimiento de producto que ha especificado en esta línea, se le informa de la cantidad que ya se ha reservado.  
8. Elija **Reservar auto.** o **Reservar desde la línea actual** para realizar una reserva sobre los números de seguimiento de productos específicos.

## <a name="see-also"></a>Consulte también
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md)  
[Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md)  
[Trabajar con números de lote y de serie](inventory-how-work-item-tracking.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
