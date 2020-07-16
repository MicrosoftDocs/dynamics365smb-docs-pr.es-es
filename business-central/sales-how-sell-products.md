---
title: Crear un pedido de venta y vender productos | Documentos de Microsoft
description: Describe cómo crear un pedido de venta para registrar el acuerdo con un cliente para vender o comerciar productos con condiciones específicas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 07/03/2020
ms.author: sgroespe
ms.openlocfilehash: 529985b477da5079beadc5c4014aa9bdfd3ecb6c
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534801"
---
# <a name="sell-products"></a>Vender productos

Puede crear un pedido o una factura de venta para registrar el contrato con un cliente para vender determinados productos según los términos de entrega y pago establecidos.

> [!NOTE]  
> Use pedidos de venta si el proceso de venta requiere que pueda enviar parte de una cantidad del pedido, por ejemplo, porque la cantidad total no está disponible a la vez. Si usa facturas de ventas, [!INCLUDE [prodshort](includes/prodshort.md)] supone que envía la cantidad completa cuando contabiliza la factura. Si vende productos que se entregan directamente desde el proveedor al cliente, como envío directo, deberá usar también pedidos de ventas. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, los pedidos de venta funcionan de la misma forma que las facturas de venta. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).

Puede negociar con el cliente creando primero una oferta que podrá convertir en un pedido cuando acuerde la venta. Para obtener más información, consulte [Crear ofertas de ventas](sales-how-make-offers.md).

Después de que el cliente haya confirmado el contrato, por ejemplo después de un proceso de oferta, puede enviar confirmación de pedido para registrar su obligación de entregar los productos según se ha acordado.

Cuando entregue los productos, ya sea total o parcialmente, registre el pedido de ventas como enviado o como enviado y facturado para crear los movimientos del producto relacionado y del cliente en su sistema. Cuando registre el pedido de venta, también puede enviar por correo electrónico el documento como un archivo PDF adjunto. Puede tener el cuerpo de correo electrónico rellenado previamente con un resumen del pedido y la información de pago, como por ejemplo un vínculo a PayPal. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

En los entornos comerciales donde el cliente paga después de la entrega, de acuerdo con el plazo de pago, una factura de ventas publicada permanece abierta (sin pagar) hasta que el departamento de Cobros verifique que se haya recibido el pago y lo liquide a la factura de ventas publicada. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

En los entornos comerciales en los que el cliente paga de forma inmediata, por ejemplo, mediante PayPal o en efectivo, el pago se registra inmediatamente al contabilizar la factura que no es de venta, es decir, la factura de venta publicada se cierra como totalmente liquidada. Seleccione el método relevante en el campo **Cód. forma pago** del pedido. Consulte debajo del paso 8. Para pagos electrónicos, como PayPal, también debe completar el campo **Servicio de pago**. Para obtener más información, consulte [Permitir pagos de cliente a través de servicios de pago](sales-how-enable-payment-service-extensions.md).

Incluso puede crear pedidos pagados directamente para clientes no registrados configurando primero una tarjeta de "cliente de efectivo" que señale en el pedido de venta. Para obtener más información, consulte [Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md).

Puede corregir o cancelar fácilmente una factura de venta registrada derivada de un pedido de venta antes de que se haya realizado el pago. Esto es útil si se desea corregir un error de escritura o si el cliente solicita un cambio temprano en el proceso de pedido. Para obtener más información, vea [Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md) Si la factura de venta registrada se ha pagado, deberá crear un abono de venta para revertir la venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).

La ficha de producto puede ser del tipo **Inventario**, **Servicio** y **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra o una unidad física no guardada en el inventario. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md). El proceso del pedido de venta es el mismo para los tres tipos de producto.

Puede rellenar los campos de cliente en el pedido de venta de dos formas en función de si el cliente ya está registrado. Consulte los pasos 2 y 3 del siguiente procedimiento.

## <a name="to-create-a-sales-order"></a>Para crear un pedido de ventas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.
2. En el campo **Cliente**, escriba el nombre de un cliente existente.

    Otros campos de la página **Pedido de venta** se rellenarán con la información estándar del cliente seleccionado. Si el cliente no está registrado, realice los pasos siguientes:
3. En el campo **Cliente**, escriba el nombre del cliente nuevo.
4. En el cuadro de diálogo de registro de nuevos clientes, haga clic en el botón **Sí**.
5. En la página **Seleccionar una plantilla para un cliente nuevo**, seleccione una plantilla en la que se basará la nueva ficha de cliente y, a continuación, haga clic en el botón **Aceptar**.

    Una nueva ficha de cliente se abre, prellenada con información sobre la plantilla de cliente seleccionada. El campo **Nombre** se rellena previamente con el nombre del nuevo cliente que especificó en el pedido de venta.
6. Rellene los campos restantes de la ficha de cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  
7. Cuando haya finalizado la ficha de cliente, haga clic en el botón **Aceptar** para volver a la página **Pedido venta**.

    Muchos campos del pedido de venta se rellenan con la información especificada en la nueva ficha de cliente.
8. Rellene los campos en la página **Pedido venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si permite que el cliente pague inmediatamente, por ejemplo, en tarjeta de crédito o mediante PayPal, complete el campo **Cód. forma pago**. El pago se registra cuando se contabiliza el pedido de venta como facturado. Si selecciona EFECTIVO, el pago se registra en una cuenta de contrapartida especificada.

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
13. Repita los pasos 9 a 12 para cada producto que desee vender al cliente.

    Los totales por debajo de las líneas se calculan automáticamente cuando se crean o modifican las líneas.
14. Una nueva ficha de cliente muestra la información sobre la plantilla de cliente seleccionada. Rellene el resto de campos. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  
15. Cuando haya finalizado la ficha de cliente, haga clic en el botón **Aceptar** para volver a la página **Pedido venta**.

    Muchos campos del pedido de venta se rellenan con la información especificada en la nueva ficha de cliente.
16. Rellene los campos en la página **Pedido venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ahora podrá rellenar las líneas de la factura de pedido de los productos que vende al cliente o para cualquier transacción con el cliente que desee registrar en una cuenta de contabilidad.   

    Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.  
17. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.

18. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes:

    * Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    * Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

19. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.  

    > [!NOTE]  
    > Si el producto es de tipo **Servicio** o el campo **Tipo** contiene **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md).

    El valor del campo **Importe línea** se calculará como *Precio venta* x *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
20. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Repita los pasos 9 a 12 para cada producto o cargo que desee vender al cliente.  

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

    > [!NOTE]
    > En casos muy raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el IVA o el impuesto de venta.<br /><br />Para verificar los importes que se registrarán realmente, puede utilizar la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.  
22. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).
23. Para enviar únicamente una parte de la cantidad del pedido, escriba dicha cantidad en el campo **Cantidad a enviar**. El calor se copia en el campo **Cantidad a facturar**.
24. Para facturar únicamente una parte de la cantidad enviada, escriba dicha cantidad en el campo **Cantidad a facturar**. La cantidad debe ser inferior al valor del campo **Cantidad a enviar**.   
25. Cuando las líneas del pedido de venta ya estén completas, seleccione la acción **Registrar y enviar**.

El cuadro de diálogo **Registrar y enviar confirmación** muestra el método preferido del cliente para recibir documentos. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

El producto relacionado y los movimientos de cliente se han creado ahora en su sistema y el pedido de venta se genera automáticamente como un documento PDF. Cuando el pedido de venta se registra por completo, se elimina de la lista de pedidos de venta y se sustituye por nuevos documentos de la lista de facturas de venta registradas y la lista de envíos de venta registrados.

## <a name="see-also"></a>Consulte también
[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Imprimir la lista de picking](sales-how-print-picking-list.md)  
[Inventario](inventory-manage-inventory.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
