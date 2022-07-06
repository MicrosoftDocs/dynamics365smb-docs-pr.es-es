---
title: Crear un pedido de venta de cliente y vender productos
description: Describe cómo crear un pedido de venta para registrar el acuerdo con un cliente para vender o comerciar productos con condiciones específicas.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order
ms.search.form: 42, 48, 9305
ms.date: 01/19/2022
ms.author: edupont
ms.openlocfilehash: 102fa04db203d8b1fe05d63629fbe24f49193112
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077845"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Vender productos con un pedido de venta de cliente  

Este artículo proporciona orientación a los usuarios sobre cuándo utilizar un pedido de venta de cliente en lugar de solo una factura. Si el proceso de venta requiere que pueda enviar solo partes de una cantidad del pedido, por ejemplo, porque la cantidad total no está disponible a la vez, venda esos productos creando un pedido de venta de cliente.  

Si vende productos que se entregan directamente desde el proveedor al cliente, como envío directo, deberá usar también pedidos de ventas. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, los pedidos de venta funcionan de la misma forma que las facturas de venta. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).

Cuando entregue los productos, ya sea total o parcialmente, registre el pedido de ventas como enviado o como enviado y facturado para crear los movimientos del producto relacionado y del cliente en su sistema. Cuando registre el pedido de venta, también puede enviar por correo electrónico el documento como un archivo PDF adjunto. Puede tener el cuerpo de correo electrónico rellenado previamente con un resumen del pedido y la información de pago, como por ejemplo un vínculo a PayPal. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

En los entornos comerciales en los que el cliente paga de forma inmediata, por ejemplo, mediante PayPal o en efectivo, el pago se registra inmediatamente al contabilizar la factura que no es de venta, es decir, la factura de venta publicada se cierra como totalmente liquidada. Seleccione el método relevante en el campo **Cód. forma pago** del pedido. Consulte debajo del paso 8. Para pagos electrónicos, como PayPal, también debe completar el campo **Servicio de pago**. Para obtener más información, consulte [Permitir pagos de cliente a través de servicios de pago](sales-how-enable-payment-service-extensions.md).

Incluso puede crear pedidos pagados directamente para clientes no registrados configurando primero una tarjeta de "cliente de efectivo" que señale en el pedido de venta. Para obtener más información, consulte [Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md).

## <a name="to-create-a-sales-order"></a>Para crear un pedido de ventas

> [!NOTE]  
> El siguiente procedimiento asume que el cliente ya está preparado. Para obtener instrucciones sobre cómo hacer esto, consulte [Registrar nuevos clientes](sales-how-register-new-customers.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Nuevo** para crear una entrada nueva.
3. En el campo **Cliente**, escriba el nombre de un cliente existente.

    Otros campos de la página **Pedido de venta** se rellenarán con la información estándar del cliente seleccionado.  

4. Rellene los campos en la página **Pedido venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si permite que el cliente pague inmediatamente, por ejemplo, en tarjeta de crédito o mediante PayPal, complete el campo **Cód. forma pago**. El pago se registra cuando se contabiliza el pedido de venta como facturado. Si selecciona EFECTIVO, el pago se registra en una cuenta de contrapartida especificada.

    Ya puede rellenar las líneas del pedido de venta con los productos de inventario o los servicios que quiera vender al cliente.

    Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.
5. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.

6. En el campo **N.º**, introduzca el número de un producto de inventario o servicio.

    Deje el campo **N.º** vacío en los casos siguientes:

    * Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    * Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).
7. En el campo **Cantidad**, escriba el número de productos que se van a vender.

    > [!NOTE]  
    > Para los producto de tipo *Recurso* o *Servicio* la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md).

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Precio venta** multiplicado por el valor del campo **Cantidad**.

    El precio y el importe de las líneas se muestran con o sin IVA dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.
8. En el campo **% Descuento línea**, especifique un porcentaje si desea conceder al cliente un descuento para el producto. El valor del campo **Importe de línea** se actualiza según corresponde.

    Si ha configurado precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el porcentaje de descuento, el precio y el presupuesto de línea en la línea de la factura se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).
9. Para agregar un comentario acerca de la línea de pedido que el cliente puede ver en el pedido de venta impreso, escriba un comentario en el campo **Descripción** en una línea vacía.  
10. Repita los pasos 5 a 9 para cada producto que desee vender al cliente.

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

    > [!NOTE]
    > En casos muy raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el IVA o el impuesto de venta.
    >
    > Para verificar los importes que se registrarán realmente, utilice la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.  

11. Opcionalmente, en el campo **Importe de descuento en factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuestos incluidos**.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).
12. Para enviar únicamente una parte de la cantidad del pedido, escriba dicha cantidad en el campo **Cantidad a enviar**. El calor se copia en el campo **Cantidad a facturar**.
13. Para facturar únicamente una parte de la cantidad enviada, escriba dicha cantidad en el campo **Cantidad a facturar**. La cantidad debe ser inferior al valor del campo **Cantidad a enviar**.  
14. Cuando las líneas del pedido de venta ya estén completas, seleccione la acción **Registrar y enviar**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

El cuadro de diálogo **Registrar y enviar confirmación** muestra el método preferido del cliente para recibir documentos. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

El producto relacionado y los movimientos de cliente se han creado ahora en su sistema y el pedido de venta se genera automáticamente como un documento PDF. Cuando el pedido de venta se registra por completo, se elimina de la lista de pedidos de venta y se sustituye por nuevos documentos de la lista de facturas de venta registradas y la lista de envíos de venta registrados.  

## <a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Imprimir la lista de picking](sales-how-print-picking-list.md)  
[Inventario](inventory-manage-inventory.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]