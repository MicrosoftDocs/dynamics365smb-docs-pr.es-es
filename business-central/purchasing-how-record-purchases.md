---
title: Registrar compras con facturas de compra (contiene vídeo)
description: 'Describe cómo comprar productos de inventario, no de inventario o recursos creando y registrando facturas o pedidos de compra.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 09/01/2022
ms.author: bholtorf
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Registrar compras con facturas de compra y pedidos

Cree una factura o un pedido de compra para registrar el coste de las compras y para realizar el seguimiento de los pagos. Las facturas y los pedidos de compra también se utilizan para actualizar dinámicamente los niveles de inventario, lo que significa que puede minimizar costes de inventario y proporcionar un mejor servicio al cliente. Los costes de compra, incluidos los gastos del servicio, y los valores de inventario resultantes del registro de las facturas de compra o pedidos contribuyen a las cifras de ganancias y otros indicadores clave de rendimeinto (KPI) financieros en el Área de trabajo.

## <a name="record-purchases-with-purchase-invoices"></a>Registrar compras con facturas de compra

Cuando se reciben los productos de inventario o cuando se completa el servicio comprado, se registra la factura o el pedido de compra para actualizar el inventario y los registros financieros, y para activar el pago al proveedor según los términos de pago. [Creación de pagos](payables-make-payments.md).

> [!CAUTION]  
> No registre una factura de compra para productos físicos hasta que reciba los productos y conozca el coste final de la compra, incluidos gastos adicionales. De lo contrario, las cifras de valor de inventario y de ganancias pueden estar sesgadas.

### <a name="create-a-and-post-purchase-invoice"></a>Crear y registrar una factura de venta

A continuación se describe cómo crear una factura de compra. Los pasos son parecidos para un pedido de compra. La principal diferencia es que los pedidos de compra tienen campos y acciones adicionales para la gestión física de los artículos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.  
2. En el campo **Proveedor**, escriba el nombre de un proveedor existente.

    Otros campos de la página **Factura de compra** se rellenarán con información estándar del proveedor seleccionado. Si el proveedor no está registrado, realice estos pasos:

    1. En el campo **Proveedor**, especifique el nombre del proveedor nuevo.
    2. En el cuadro de diálogo que registra al nuevo proveedor, seleccione **Sí**.
    3. Para obtener más información sobre cómo completar la tarjeta de proveedor, vaya a [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).  
    4. Cuando haya finalizado la ficha de proveedor, seleccione **Aceptar** para devolver a la página **Factura de compra**.

3. Rellene los campos en la página **Factura de compra** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ya puede empezar a rellenar las líneas de la factura de compra con los productos o recursos que ha comprado del proveedor.

    > [!NOTE]  
    > Si ha configurado líneas de compra periódicas para el proveedor, como un pedido de reabastecimiento mensual, puede insertarlas en la factura eligiendo el botón **Obtener líneas de compra periódicas**.
4. En la ficha desplegable **Líneas**, en el campo **Nº producto**, especifique el número de un producto o un servicio de inventario.
5. En el campo **Cantidad**, introduzca el número de productos que se van a comprar.

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Coste unit. directo** multiplicado por el valor del campo **Cantidad**.

    El precio y el importe de las líneas se muestran con o sin IVA dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del proveedor.

    Los campos de totales debajo de las líneas se actualizan automáticamente a medida que se crean o modifican líneas para visualizar los importes que se registrarán en los extractos.

6. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total IVA incl.** en la parte inferior de la factura.

    > [!NOTE]  
    > Si ha configurado descuentos en factura para el proveedor, el valor porcentual especificado se inserta automáticamente en el campo **% descuento factura proveedor** si se cumplen los criterios. El importe relacionado se inserta en el campo **Importe descuento factura**.
7. Cuando reciba los productos o servicios comprados, seleccione **Registrar**.

La compra ahora se refleja en el inventario, en los movimientos de recursos y en los registros financieros, y se activa el pago al proveedor. La factura de compra se elimina de la lista de facturas de compra y se reemplaza con un nuevo documento de la lista de facturas de compra registradas.  Para obtener más información sobre lo que sucede cuando se contabilizan documentos de compra, consulte [Registrar compras](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> En casos raros, los importes registrados pueden desviarse de lo que se muestra en los campos de totales. Esto se debe normalmente a los cálculos de redondeo en relación con el impuesto sobre el valor añadido (IVA) o el impuesto de venta.
>
> Para verificar los importes que se registrarán realmente, vaya a la página **Estadísticas**, que tiene en cuenta los cálculos de redondeo. Además, si selecciona la acción **Liberar**, los campos de totales se actualizarán para incluir los cálculos de redondeo.

## <a name="posted-invoices"></a>Facturas registradas

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Puede corregir o cancelar fácilmente una factura de compra registrada antes de pagar al proveedor. Esto es útil si se desea corregir un error de escritura o cambiar la compra de forma anticipada en el proceso de pedido. Obtenga más información en [Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Si ya ha pagado productos o servicios en la factura de compra registrada, deberá crear un abono de compra para revertir la compra. Obtenga más información en [Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).

[Abra la lista **Histórico facturas compra**](https://businesscentral.dynamics.com/?page=146) en [!INCLUDE [prod_short](includes/prod_short.md)].


## <a name="purchasing-non-inventory-items"></a>Comprar artículos que no pertenecen al inventario

Las líneas de una factura de compra pueden ser del tipo **Recurso** o **Artículo**. Las fichas de producto se pueden clasificar adicionalmente como de tipo **Inventario**, **Servicio** o **No inventario**, lo que especifica si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra (también aplicable para recursos) o una unidad física sin seguimiento en el inventario. Obtenga más información en [Registrar nuevos productos](inventory-how-register-new-items.md). El proceso de la factura de compra es el mismo para todos los tipos mencionados.

> [!NOTE]
> Con el tipo de línea de compra **Recurso**, también puede comprar recursos externos, por ejemplo, para facturar a un proveedor por el trabajo entregado. Obtenga más información en [Configurar recursos](projects-how-setup-resources.md).
>
> Para usar un recurso comprado, es posible que deba establecer la capacidad del recurso y asignarlo manualmente a un trabajo. La compra de un recurso crea un movimiento de recursos; sin embargo, los movimientos de recursos no se rastrean por cantidad y valor como, por ejemplo, los productos. Si se requiere el seguimiento de la cantidad y el valor, considere usar otros tipos de líneas de pedido.

## <a name="when-to-use-purchase-orders"></a>Cuándo usar pedidos de compra

Debe usar pedidos de compra si el proceso de compra requiere que registre recibos parciales de una cantidad del pedido, por ejemplo, porque el proveedor no dispone de la cantidad total. Si entrega productos venedidos directamente desde el proveedor al cliente como envío directo, deberá usar también pedidos de compras. Obtenga más información en [Realizar envíos directos](sales-how-drop-shipment.md).

En todos los demás aspectos, los pedidos de compra funcionan de la misma forma que las facturas de compra. El procedimiento siguiente se basa en una factura de compra. Los pasos son parecidos para un pedido de compra.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Recibir productos con un pedido de compra

A continuación se describe cómo recibir productos con un pedido de compra. 

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Abra un pedido de compra existente o cree uno nuevo.
3. Escriba la cantidad recibida en el campo **Cantidad a recibir**.

   > [!NOTE]
   > Si la cantidad recibida es superior a la ordenada del pedido de compra, y el proveedor se ha configurado para permitir recepciones en exceso, entonces use el campo **En exceso** para administrar la cantidad en exceso. Obtenga más información en la sección [Para recibir más artículos de los solicitados](purchasing-how-record-purchases.md#receive-more-items-than-ordered).
4. Seleccione la acción **Registrar**.

  El valor del campo **Cdad. recibida** se actualiza según corresponde. Si se trata de un recibo parcial, el valor es inferior al valor del campo **Cantidad**.

> [!NOTE]
> Si usa una manipulación de almacén, no puede usar la acción **Registrar** en el pedido de compra para registrar el recibo. Esto se debe a que el empleado del almacén ya ha registrado como recibida la cantidad del pedido de compra. Obtenga más información en [Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-ordered"></a>Recibir más artículos de los solicitados

Cuando lleguen más productos de los que ha pedido, es posible que desee recibirlos en lugar de cancelar el recibo. Por ejemplo, puede ser más barato mantener el exceso de productos en el inventario que devolverlos o su proveedor puede ofrecerle un descuento por conservarlos.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Configurar recibos en exceso

Cree códigos de exceso de recepción para definir un porcentaje por el cual una cantidad recibida puede exceder la cantidad pedida. Especifique el porcentaje en el campo **Porcentaje de tolerancia de recepción en exceso**. Luego asigna el código en las páginas Ficha producto o Ficha proveedor para productos y proveedores.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códigos de recepción en exceso** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Asignar el código de recepción en exceso a un producto

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la página **Ficha producto** del producto.
3. En el campo **Código de recepción en exceso**, elija el código que contiene el porcentaje que desea permitir en los excesos de recepción.

El código de recepción en exceso se asigna al artículo. Los pedidos de compra o los recibos de almacén del producto ahora permiten recibir más que la cantidad solicitada dentro del porcentaje de tolerancia de recepción en exceso.

> [!NOTE]
> Puede configurar un flujo de trabajo de aprobación que requiera que se aprueben las recepciones en exceso antes de que se puedan administrar. Seleccione la casilla **Aprobación requerida** en la página **Códigos de recepción en exceso**. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Recibir un pedido en exceso

En las líneas de compra y las líneas de recepción de almacén, el campo **Cantidad de recepción en exceso** se utiliza para registrar las cantidades recibidas en exceso, esto es, cantidades que exceden el valor de la cantidad pedida del campo **Cantidad**.

Cuando administra una recepción en exceso, puede aumentar el valor del campo **Cant. para recibir** con la cantidad realmente recibida. El campo **Cantidad de recepción en exceso** se actualiza para mostrar la cantidad en exceso. Alternativamente, puede introducir la cantidad en exceso en el campo **Cantidad de recepción en exceso**. El campo **Cantidad para recibir** se actualiza para mostrar la cantidad solicitada más la cantidad en exceso. El siguiente procedimiento describe cómo completar el campo **Cantidad para recibir**.  

1. En un pedido de compra o un documento de recibo de almacén donde la cantidad recibida sea mayor que la ordenada, introduzca la cantidad realmente recibida en el campo **Cantidad para recibir**.

    Si el aumento está dentro de la tolerancia especificada por un código de recepción en exceso asignado, el campo **Cantidad de recepción en exceso** se actualiza para mostrar la cantidad en la que se excede el valor del campo **Cantidad**.

    Si el aumento está por encima de la tolerancia, no se permite la recepción en exceso. Investigue si otro código de recepción en exceso lo permitirá. De lo contrario, solo se puede recibir la cantidad pedida y la cantidad excedente se debe administrar de otra manera, por ejemplo, devolviéndola al proveedor.

2. Publique la recepción como lo haría con cualquier otra.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] no maneja automáticamente los aspectos financieros de las recepciones en exceso. Debe administrar manualmente esto de acuerdo con el proveedor, por ejemplo, enviando una factura nueva o actualizada.

## <a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Registrar compras

En un documento de compra, puede elegir entre las acciones de registro siguientes:

* **Registrar**
* **Vista previa de registro**
* **Registrar e imprimir**
<!--* **Test Report**-->
* **Registrar por lotes**

Cuando se registra un documento de compra, se actualiza la cuenta del proveedor, la contabilidad, los movimientos de producto y los movimientos de recursos.

Por cada documento de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro de la compra puede dar como resultado un movimiento del impuesto sobre el valor añadido (IVA) y uno de contabilidad para el importe de descuento. El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. compras y pagos**.

Para cada línea de compra, en su caso, se crearán entradas en:

* Tabla **Mov. producto** si la línea de compra es de tipo **Producto**.
* Tabla **Mov. contabilidad** si la línea de compra es de tipo **Cuenta**.
* Tabla **Movimiento de recurso** si la línea de compra es de tipo **Recurso**.

Además, los documentos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.

Siempre puede revisar varios movimientos del libro mayor que se crearán como resultado de las publicaciones. Elija **Vista previa de registro** para validar el documento e inspeccionar los movimientos esperados del libro mayor.


> [!IMPORTANT]  
> Cuando registre un pedido de compra para productos, podrá crear tanto un albarán de compra como una factura. Esto se puede hacer simultánea o independientemente. También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales del pedido de compra antes de registrar. Tenga en cuenta que no puede crear una factura de compra a partir de un pedido de compra de productos o servicios que no se han recibido. Es decir, antes de poder facturar debe haber registrado un albarán de compra o haber elegido recibir y facturar al mismo tiempo.

Puede registrar o registrar e imprimir. Si elije registrar e imprimir, un informe se imprime cuando se registre el pedido. También puede elegir la acción **Registrar por lotes** para registrar varios pedidos a la vez. Obtenga más información en [Registrar varios documentos al mismo tiempo](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Ver movimientos

Una vez finalizado el registro, las líneas de compra registradas se quitan del pedido. Al terminar el registro aparece un mensaje de aviso. Después de esto, podrá ver los movimientos registrados en las diferentes páginas, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Movimientos de recursos**, **Albaranes compra** e **Histórico facturas compra**.

En la mayoría de los casos, puede abrir movimientos desde la tarjeta o documento afectado. Por ejemplo, en la página **Ficha proveedor**, seleccione la acción **Entradas**.

## <a name="editing-ledger-entries"></a>Editar movimientos

Puede editar determinados campos en documentos de compra registrados, como el campo **Referencia pago**. Obtenga más información en [Editar documentos registrados](across-edit-posted-document.md). Para campos más críticos que afectan el registro de auditoría, debe revertir o deshacer la publicación. Obtenga más información en [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Consulte también .

[Solicitar presupuestos](purchasing-how-request-quotes.md)  
[Comprar productos para una venta](purchasing-how-purchase-products-sale.md)  
[Preparar envíos directos](sales-how-drop-shipment.md)  
[Compras](purchasing-manage-purchasing.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Configurar recursos](projects-how-setup-resources.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Editar documentos registrados](across-edit-posted-document.md)  
[Registrar varios documentos al mismo tiempo](ui-batch-posting.md)  
[Compras](purchasing-manage-purchasing.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
