---
title: Crear un pedido de venta y vender productos | Documentos de Microsoft
description: "Describe cómo crear un pedido de venta para registrar el acuerdo con un cliente para vender o comerciar productos con condiciones específicas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 01/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6e18df20a5bef5aae44f476755eede73c99668da
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="sell-products"></a>Vender productos
Puede crear un pedido o una factura de venta para registrar el contrato con un cliente para vender determinados productos según los términos de entrega y pago establecidos.

> [!NOTE]  
>   Use pedidos de venta si el proceso de venta requiere que pueda enviar parte de una cantidad del pedido, por ejemplo, porque la cantidad total no está disponible a la vez. Si vende productos que se entregan directamente desde el proveedor al cliente, como envío directo, deberá usar también pedidos de ventas. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, los pedidos de venta funcionan de la misma forma que las facturas de venta. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).

Puede negociar con el cliente creando primero una oferta que podrá convertir en un pedido cuando acuerde la venta. Para obtener más información, consulte [Realización de ofertas](sales-how-make-offers.md).

Después de que el cliente haya confirmado el contrato, por ejemplo después de un proceso de oferta, puede enviar confirmación de pedido para registrar su obligación de entregar los productos según se ha acordado.

Cuando entregue los productos, ya sea total o parcialmente, registre el pedido de ventas como enviado o como enviado y facturado para crear los movimientos del producto relacionado y del cliente en su sistema. Cuando registre el pedido de venta, también puede enviar por correo electrónico el documento como un archivo PDF adjunto. Puede tener el cuerpo de correo electrónico rellenado previamente con un resumen del pedido y la información de pago, como por ejemplo un vínculo a PayPal. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

En entornos de negocio donde el cliente debe pagar antes de que los productos se entreguen, por ejemplo en la venta minorista, debe esperar la recepción del pago antes de entregar los productos. En la mayoría de casos, puede procesar los pagos entrantes algunas semanas después de la salida liquidando los pagos a las facturas relacionadas, registradas como facturas de ventas no pagadas . Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Puede corregir o cancelar fácilmente una factura de venta registrada derivada de un pedido de venta antes de que se haya realizado el pago. Esto es útil si se desea corregir un error de escritura o si el cliente solicita un cambio temprano en el proceso de pedido. Para obtener más información, vea [Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md) Si la factura de venta registrada se ha pagado, deberá crear un abono de venta para revertir la venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).

Los productos pueden ser productos de inventario y servicios, lo que se indica por los tipos **Producto - Inventario** y **Producto - Servicio** en las líneas de venta. El proceso del pedido de venta es el mismo para ambos tipos de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

Puede rellenar los campos de cliente en el pedido de venta de dos formas en función de si el cliente ya está registrado. Consulte los pasos 2 y 3 del siguiente procedimiento.

## <a name="to-create-a-sales-order"></a>Para crear un pedido de ventas
1. En la página principal, seleccione la acción **Pedido de venta**.  
2. En el campo **Cliente**, escriba el nombre de un cliente existente.

    Otros campos de la ventana **Pedido de venta** se rellenarán con la información estándar del cliente seleccionado. Si el cliente no está registrado, realice los pasos siguientes:
3. En el campo **Cliente**, escriba el nombre del cliente nuevo.
4. En el cuadro de diálogo de registro de nuevos clientes, haga clic en el botón **Sí**.
5. En la ventana **Seleccionar una plantilla para un cliente nuevo**, seleccione una plantilla en la que se basará la nueva ficha de cliente y, a continuación, haga clic en el botón **Aceptar**.

    Una nueva ficha de cliente se abre, prellenada con información sobre la plantilla de cliente seleccionada. El campo **Nombre** se rellena previamente con el nombre del nuevo cliente que especificó en el pedido de venta.
6. Rellene los campos restantes de la ficha de cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  
7. Cuando haya finalizado la ficha de cliente, haga clic en el botón **Aceptar** para volver a la ventana **Pedido de venta**.

    Muchos campos del pedido de venta se rellenan con la información especificada en la nueva ficha de cliente.
8. Rellene los campos restantes de la ventana **Pedido de venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ya puede rellenar las líneas del pedido de venta con los productos de inventario o los servicios que quiera vender al cliente.

    Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.
9. En la ficha desplegable **Líneas**, en el campo **Producto**, especifique el número de un producto o un servicio de inventario.  
10. En el campo **Cantidad**, escriba el número de productos que se van a vender.

    > [!NOTE]  
>   Para los producto de tipo Servicio la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea.

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Precio venta** multiplicado por el valor del campo **Cantidad**.

    El precio y el importe de las líneas se muestran con o sin IVA dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.
11. En el campo **% Descuento línea**, especifique un porcentaje si desea conceder al cliente un descuento para el producto. El valor del campo **Importe de línea** se actualiza según corresponde.

    Si ha configurado precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el porcentaje de descuento, el precio y el presupuesto de línea en la línea de la factura se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).
12. Para agregar un comentario acerca de la línea de oferta que el cliente puede ver en la oferta de venta impresa, escriba un texto en el campo **Descripción** en una línea vacía.  
13. Repita los pasos 9 a 12 para cada producto que desee ofertar al cliente.

    Los totales por debajo de las líneas se calculan automáticamente cuando se crean o modifican las líneas.
14. Una nueva ficha de cliente muestra la información sobre la plantilla de cliente seleccionada. Rellene el resto de campos. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  
15. Cuando haya finalizado la ficha de cliente, haga clic en el botón **Aceptar** para volver a la ventana **Pedido de venta**.

   Muchos campos del pedido de venta se rellenan con la información especificada en la nueva ficha de cliente.  
16. Rellene los campos restantes de la ventana **Pedido de venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Ahora podrá rellenar las líneas de la factura de pedido de los productos que vende al cliente o para cualquier transacción con el cliente que desee registrar en una cuenta de contabilidad.   

   Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.  
17. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.
18. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes: - Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    - Si la línea es de un producto sin stock. Elija la acción **Seleccionar artículos sin stock**. Para obtener más información, consulte [Trabajar con productos sin stock](inventory-how-work-nonstock-items.md).

19. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.  

    > [!NOTE]  
>   Si el producto es de tipo **Producto - Servicio** o **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md).

    El valor del campo **Importe línea** se calculará como *Precio venta* x *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
20. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Repita los pasos 9 a 12 para cada producto o cargo que desee vender al cliente.  

    Los totales por debajo de las líneas se calculan automáticamente cuando se crean o modifican las líneas.  
22. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).
23. Para enviar únicamente una parte de la cantidad del pedido, escriba dicha cantidad en el campo **Cantidad a enviar**. El calor se copia en el campo **Cantidad a facturar**.
24. Para facturar únicamente una parte de la cantidad enviada, escriba dicha cantidad en el campo **Cantidad a facturar**. La cantidad debe ser inferior al valor del campo **Cantidad a enviar**.   
25. Cuando las líneas del pedido de venta ya estén completas, seleccione la acción **Registrar y enviar**.

El cuadro de diálogo **Registrar y enviar confirmación** muestra el método preferido del cliente para recibir documentos. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

El producto relacionado y los movimientos de cliente se han creado ahora en su sistema y el pedido de venta se genera automáticamente como un documento PDF. Cuando el pedido de venta se registra por completo, se elimina de la lista de pedidos de venta y se sustituye por nuevos documentos de la lista de facturas de venta registradas y la lista de envíos de venta registrados.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

