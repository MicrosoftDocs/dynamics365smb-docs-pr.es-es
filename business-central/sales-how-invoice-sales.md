---
title: Facturar ventas
description: 'Describe cómo crear un recibo, o una factura o un pedido de venta, para registrar el acuerdo con un cliente para vender productos con condiciones específicas.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="invoice-sales" />Facturar ventas

Normalmente puede crear un pedido o una factura de venta para registrar el contrato con un cliente para vender determinados productos según los términos de entrega y pago establecidos.  

Sin embargo, debe utilizar un pedido de ventas en lugar de una factura de ventas si:  

* Necesita enviar solo parte de una cantidad del pedido, por ejemplo, porque no esté disponible toda la cantidad.  
* Envía productos después de contabilizar las facturas de venta correspondientes.
* Vende productos que el proveedor entrega directamente al cliente, lo que se denomina envío directo. Obtenga más información en [Realizar envíos directos](sales-how-drop-shipment.md).  

En todas las demás situaciones, los pedidos de venta y las facturas de venta funcionan de la misma forma. Obtenga más información sobre cómo usar pedidos de ventas en [Vender productos](sales-how-sell-products.md).

Puede negociar con el cliente creando primero creando una oferta de venta, que puede convertir en una factura de venta cuando acuerde la venta. Obtenga más información en [Crear ofertas de ventas](sales-how-make-offers.md).

## <a name="create-sales-invoices" />Crear factura de venta

Si el cliente decide comprar, registre la factura de venta para crear los movimientos de cantidad y valor relacionados. Cuando registre la factura de venta, también puede enviarla como PDF anexo. Puede rellenar previamente el cuerpo de correo electrónico con un resumen de la factura y la información de pagos, por ejemplo, proporcionando un vínculo a PayPal. Obtenga más información en [Enviar documentos por correo electrónico](ui-how-send-documents-email.md). Cuando el cliente paga la factura, puede registrar ese pago de diferentes maneras, según el tamaño y los flujos de trabajo preferidos de su organización. Obtenga más información en la sección [Registrar pagos](#registering-payments).  

Las ficha de producto puede ser del tipo **Inventario**, **Servicio** o **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra o una unidad física no guardada en el inventario, respectivamente. Obtenga más información en [Registrar nuevos productos](inventory-how-register-new-items.md). El proceso de la factura de venta es el mismo para los tres tipos de producto.

Puede rellenar los campos de clientes en la factura de venta de dos formas en función de si el cliente ya está registrado. Consulte el paso 2 del siguiente procedimiento.

### <a name="to-create-a-sales-invoice" />Para crear una factura de venta

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
2. En el campo **Cliente**, escriba el nombre de un cliente existente. Sin embargo, si el cliente es nuevo y, por tanto, no está registrado, siga estos pasos para completar la información estándar del cliente en la página **Factura de venta**:

    1. En el campo **Nombre del cliente**, escriba el nombre del cliente nuevo.
    2. En el cuadro de diálogo de registro de nuevos clientes, haga clic en **Sí**.
    3. En la página **Seleccionar una plantilla para un cliente nuevo**, seleccione una plantilla en la que se basará la nueva ficha de cliente y, a continuación, elija **Aceptar**.
    4. Una nueva ficha de cliente muestra la información sobre la plantilla de cliente seleccionada. Rellene el resto de campos. Obtenga más información en [Registrar nuevos clientes](sales-how-register-new-customers.md).  
    5. Cuando haya finalizado la ficha de cliente, elija **Cerrar** para volver a la página **Factura de venta**.

   Muchos campos de la factura de venta se rellenan con la información especificada en la nueva ficha de cliente.  
3. Rellene los campos en la página **Factura venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Si permite que el cliente pague inmediatamente, por ejemplo, en efectivo o mediante PayPal, complete el campo **Cód. forma pago**. El pago se registra cuando se contabiliza la factura de venta. Si selecciona *Efectivo*, el pago se registra en una cuenta de contrapartida especificada.

    Ahora podrá rellenar la ficha desplegable **Líneas** con productos que vende al cliente o para cualquier transacción con el cliente que desee registrar en una cuenta de contabilidad.

4. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.
   * Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede reflejar eso en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.
5. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes:

    * Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    * Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Obtenga más información en [Trabajar con artículos de catálogo](inventory-how-work-nonstock-items.md).

6. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción deberá registrar la línea para el cliente.  

    > [!NOTE]  
    > Si el producto es de tipo **Servicio** o el campo **Tipo** contiene **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Obtenga más información en [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md)

    El valor del campo **Importe línea** se calculará como *Precio venta* × *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
7. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Obtenga más información en [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Repita los pasos 4 a 7 para cada producto o cargo que desee facturar al cliente.

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

    > [!NOTE]
    > En casos muy raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el IVA o el impuesto de venta.<br /><br />Para verificar los importes que se registrarán realmente, puede utilizar la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.
9. En el campo **Descuento en factura excluyendo impuesto**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.**.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios de descuento, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Obtenga más información en [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

10. Cuando las líneas de la factura de venta ya estén completas, seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo **Registrar y enviar confirmación** muestra el método preferido del cliente para recibir documentos. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Obtenga más información en [Configurar perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).

El producto relacionado y los movimientos de cliente se han creado ahora en su sistema y la factura de venta se genera como un documento PDF. La factura de venta se elimina de la lista de facturas de venta y se reemplaza con un nuevo documento de la lista de facturas de venta registradas.  

### <a name="calculating-invoice-discounts-on-sales" />Calcular descuentos en factura para ventas

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices" />Facturas registradas

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Puede corregir o cancelar fácilmente una factura de venta registrada antes de que se pague. Esto es útil si se desea corregir un error de escritura o si el cliente solicita un cambio temprano en el proceso de pedido. Obtenga más información en [Corregir o cancelar facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md). Si la factura de venta registrada se ha pagado, deberá crear un abono de venta para revertir la venta. Obtenga más información en [Procesamiento de devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md).  

[Abra la lista **Histórico facturas venta**](https://businesscentral.dynamics.com/?page=143) en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="registering-payments" />Registro de pagos

En función de sus necesidades comerciales, puede recibir un pago y registrarlo de diferentes maneras: de forma manual, automática y mediante servicios de pago.  

Puede procesar los pagos directamente desde la ficha de cliente. Utilice la acción **Registrar pagos de cliente** para obtener un resumen de las facturas sin abonar de dicho cliente. A continuación, marque la factura como pagada de forma parcial o total. Esta conciliación de pagos permite procesar los pagos de sus clientes al conciliar los importes recibidos en la cuenta bancaria con las facturas de venta relacionadas no pagadas y luego registrar los pagos. Obtenga más información en la sección [Conciliar pagos individualmente](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

En los entornos comerciales donde el cliente paga después de la entrega, de acuerdo con los plazos de pago, una factura de ventas publicada permanece abierta (sin pagar) hasta que el departamento de Cobros verifique que se haya recibido el pago y lo liquide a la factura de ventas publicada. Esto se puede realizar manual o automáticamente. Obtenga más información en [Conciliar los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente](receivables-how-apply-sales-transactions-manually.md) y [Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).  

En los entornos comerciales en los que el cliente paga de forma inmediata, por ejemplo, mediante PayPal o en efectivo, el pago se registra inmediatamente al contabilizar la factura de venta, es decir, la factura de venta publicada se cierra como totalmente liquidada. Seleccione el método relevante en el campo **Cód. forma pago** del pedido. Para pagos electrónicos, como PayPal, también debe completar el campo **Servicio de pago**. Obtenga más información en [Permitir los pagos de clientes mediante servicios de pago](sales-how-enable-payment-service-extensions.md).

Incluso puede crear facturas pagadas directamente para clientes no registrados configurando una tarjeta de "cliente de efectivo" para ellas que señale en la factura de venta. Obtenga más información en [Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Si desea enviar a sus clientes recordatorios de pagos vencidos, debe configurar primero niveles y términos de recordatorio. Obtenga más información en [Configurar términos y niveles de recordatorios](finance-setup-reminders.md).  

## <a name="external-document-numbers" />Números de documento externo

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/modules/invoicing-customers-dynamics-365-business-central/index) relacionada.

## <a name="see-also" />Consulte también .

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Imprimir la lista de picking](sales-how-print-picking-list.md)  
[Inventario](inventory-manage-inventory.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Facturación masiva desde Microsoft Bookings en Business Central ](finance-bookings.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
