---
title: Facturar ventas
description: Describe cómo crear un recibo, o una factura o un pedido de venta, para registrar el acuerdo con un cliente para vender productos con condiciones específicas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.search.form: 42, 43, 48, 9301, 9305
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 125d28f1621e23f14cda9ce57a935a7da71e43cb
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752473"
---
# <a name="invoice-sales"></a>Facturar ventas

Puede crear una factura o un pedido de ventas para registrar el contrato con un cliente para vender determinados productos según términos de entrega y pago determinados.  

Hay un par de escenarios en los que debe usar un pedido de venta en lugar de una factura de venta:  

* Si necesita enviar solo parte de una cantidad del pedido, por ejemplo, porque no esté disponible toda la cantidad.  
* Si envía productos después de contabilizar las facturas de venta correspondientes.
* Si vende productos que el proveedor entrega directamente al cliente, lo que se denomina envío directo. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md).  

En todos los demás aspectos, los pedidos de venta y las facturas de venta funcionan de la misma forma. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).

Puede negocias con el cliente creando primero creando una oferta de venta, que puede convertir en una factura de venta cuando acuerde la venta. Para obtener más información, consulte [Crear ofertas de ventas](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Crear factura de venta

Si el cliente decide comprar, registre la factura de venta para crear los movimientos de cantidad y valor relacionados. Cuando registre la factura de venta, también puede enviar por correo electrónico el documento como un PDF anexo. Puede tener el cuerpo de correo electrónico rellenado con un resumen de la factura y la información de pagos, como un vínculo a PayPal. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md). Cuando el cliente paga la factura, puede registrar ese pago de diferentes maneras, según el tamaño y los flujos de trabajo preferidos de su organización. Para obtener más información, vea la sección [Registrar pagos](#registering-payments).  

Las fichas de productos pueden ser del tipo **Inventario**, **Servicio** y **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra o una unidad física no guardada en el inventario. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md). El proceso de la factura de venta es el mismo para los tres tipos de producto.

Puede rellenar los campos de clientes en la factura de venta de dos formas en función de si el cliente ya está registrado. Consulte el paso 2 del siguiente procedimiento.

### <a name="to-create-a-sales-invoice"></a>Para crear una factura de venta

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
2. En el campo **Cliente**, escriba el nombre de un cliente existente.

   Otros campos de la página **Factura venta** contienen información estándar sobre el cliente seleccionado. Si el cliente no está registrado, realice los pasos siguientes:

    1. En el campo **Cliente**, escriba el nombre del cliente nuevo.
    2. En el cuadro de diálogo de registro de nuevos clientes, haga clic en el botón **Sí**.
    3. En la página **Seleccionar una plantilla para un cliente nuevo**, seleccione una plantilla en la que se basará la nueva ficha de cliente y, a continuación, haga clic en el botón **Aceptar**.
    4. Una nueva ficha de cliente muestra la información sobre la plantilla de cliente seleccionada. Rellene el resto de campos. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  
    5. Cuando haya finalizado la ficha de cliente, haga clic en el botón **Aceptar** para volver a la página **Factura venta**.

   Muchos campos de la factura de venta se rellenan con la información especificada en la nueva ficha de cliente.  
3. Rellene los campos en la página **Factura venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si permite que el cliente pague inmediatamente, por ejemplo, en efectivo o mediante PayPal, complete el campo **Cód. forma pago**. El pago se registra cuando se contabiliza la factura de venta. Si selecciona EFECTIVO, el pago se registra en una cuenta de contrapartida especificada.

    Ahora podrá rellenar las líneas de la factura de venta de los productos que vende al cliente o para cualquier transacción con el cliente que desee registrar en una cuenta de contabilidad.  

    Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.  
4. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.
5. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes:

    * Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    * Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

6. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.  

    > [!NOTE]  
    > Si el producto es de tipo **Servicio** o el campo **Tipo** contiene **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md)

    El valor del campo **Importe línea** se calculará como *Precio venta* x *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
7. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Repita los pasos 9 a 12 para cada producto o cargo que desee facturar al cliente.  

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

    > [!NOTE]
    > En casos muy raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el IVA o el impuesto de venta.<br /><br />Para verificar los importes que se registrarán realmente, puede utilizar la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.
9. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
10. Cuando las líneas de la factura de venta ya estén completas, seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo **Registrar y enviar confirmación** muestra el método preferido del cliente para recibir documentos. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

El producto relacionado y los movimientos de cliente se han creado ahora en su sistema y la factura de venta se genera como un documento PDF. La factura de venta se elimina de la lista de facturas de venta y se reemplaza con un nuevo documento de la lista de facturas de venta registradas.  

### <a name="calculating-invoice-discounts-on-sales"></a>Calcular descuentos en factura para ventas

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Facturas registradas

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Puede corregir o cancelar fácilmente una factura de venta registrada antes de que se pague. Por ejemplo, esto es útil si se desea corregir un error de escritura o si el cliente solicita un cambio temprano en el proceso de pedido. Para obtener más información, vea [Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md) Si la factura de venta registrada se ha pagado, deberá crear un abono de venta para revertir la venta. Para obtener más información, vea [Procesar devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).  

[Abra la lista **Histórico facturas venta**](https://businesscentral.dynamics.com/?page=143) en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments"></a>Registro de pagos

En función de sus necesidades comerciales, puede recibir el pago y registrarlo de diferentes maneras: de forma manual, automática y mediante servicios de pago.  

Puede procesar los pagos directamente desde la ficha de cliente. Utilice la acción **Registrar pagos de cliente** para obtener un resumen de las facturas sin abonar de dicho cliente. A continuación, marque la factura como pagada de forma parcial o total. Esta conciliación de pagos permite procesar los pagos de sus clientes al conciliar los importes recibidos en la cuenta bancaria con las facturas de venta relacionadas no pagadas y luego registrar los pagos. Para obtener más información, vea [Conciliar pagos individualmente](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

En los entornos comerciales donde el cliente paga después de la entrega, de acuerdo con el plazo de pago, una factura de ventas publicada permanece abierta (sin pagar) hasta que el departamento de Cobros verifique que se haya recibido el pago y lo liquide a la factura de ventas publicada. Esto se puede realizar manual o automáticamente. Para obtener más información, vea [Conciliar los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente](receivables-how-apply-sales-transactions-manually.md) y [Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).  

En los entornos comerciales en los que el cliente paga de forma inmediata, por ejemplo, mediante PayPal o en efectivo, el pago se registra inmediatamente al contabilizar la factura de venta, es decir, la factura de venta publicada se cierra como totalmente liquidada. Seleccione el método relevante en el campo **Cód. forma pago** del pedido. Consulte debajo del paso 8. Para pagos electrónicos, como PayPal, también debe completar el campo **Servicio de pago**. Para obtener más información, consulte [Permitir pagos de cliente a través de servicios de pago](sales-how-enable-payment-service-extensions.md).  

Incluso puede crear facturas pagadas directamente para clientes no registrados configurando primero una tarjeta de "cliente de efectivo" que señale en la factura de venta. Para obtener más información, consulte [Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Si desea enviar a sus clientes recordatorios de pagos vencidos, debe configurar niveles y términos de recordatorio. Para más información, ver [Configurar términos y niveles de recordatorio](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Números de documento externo

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Imprimir la lista de picking](sales-how-print-picking-list.md)  
[Inventario](inventory-manage-inventory.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Facturación masiva desde Microsoft Bookings en Business Central ](finance-bookings.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]