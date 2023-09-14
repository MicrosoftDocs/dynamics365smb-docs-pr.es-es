---
title: Procesamiento de devoluciones o cancelaciones
description: Explica cómo crear y registrar un abono de compra cuando se desean devolver productos a un proveedor o cancelar servicios comprados.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cancel, undo, correct'
ms.search.form: '6640, 6643, 9307, 9309, 9308, 6652, 145, 147'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Procesamiento de devoluciones de compra o cancelaciones

Si desea devolver productos al proveedor o cancelar servicios comprados, puede crear y registrar un abono de compra que especifique el cambio solicitado en relación a la factura de compra original. Para incluir la información correcta de la factura de compras, puede crear el abono de compra directamente de la factura de compra contabilizada o puede crear un nuevo abono de compra con información de factura copiada.

Si necesita más control del proceso de devolución de compras, como documentos de almacén para el manejo de artículos o una mejor descripción al devolver productos de varios documentos de compras con una sola devolución de compra, puede crear órdenes de devolución de compras. Un pedido de devolución de compra emite automáticamente un abono de compra relacionado. Para obtener más información, consulte [Crear un pedido de devolución de compra basado en uno o más documentos de compra registrados](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Si una factura de compra registrada aún no se ha pagado, puede utilizar las funciones **Corregir** o **Cancelar** en la factura de compra registrada para revertir automáticamente las transacciones correspondientes. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Tampoco puede corregir o cancelar las facturas de compra que se registraron con recibos de más de una orden de compra. Para obtener más información, vea [Corregir o cancelar las facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)

Normalmente, se crea un abono de compra o un pedido de devolución de compra como resultado de un abono enviado por un proveedor. El pedido de abono de compra o de devolución de compra funciona como la documentación interna del proceso de abono para fines de estadísticas o control de envíos de los productos relacionados.

El cambio puede relacionarse con todos los productos en la factura de compra original o solo algunos de los productos. Por consiguiente, puede devolver productos parcialmente recibidos o exigir un reembolso parcial de los servicios recibidos. En ese caso, debe editar la información de las líneas del abono de compra o en el pedido de devolución de compras.

Además de la original factura de compra registrada, puede liquidar el abono de compra o el pedido de devolución de compra a otros documentos de compra, por ejemplo otra factura de compra registrada, porque usted también devuelve los productos entregados con dicha factura.

El registro del abono también revertirá cualquier coste de producto que se hubiera asignado al documento registrado, de forma que los movimientos de valor del producto son los mismos de antes que se asignara el cargo de producto.

## Inventario y valoración
Para conservar la valoración correcta del inventario, normalmente desea tomar los artículos devueltos del inventario al costo unitario en el que fueron comprados, no al costo unitario actual. Esto se denomina reversión de coste exacto.

Existen dos funciones para asignar la reversión de coste exacta automáticamente.  

|Función|Description|  
|------------------|---------------------------------------|  
|Función **Revertir líneas documentos registrados** en la página **Pedido dev. compra**|Copia una o varias líneas de documentos registrados para revertirlas en el pedido de devolución de compra. Para obtener más información, consulte [Crear un pedido de devolución de compra basado en uno o más documentos de compra registrados](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|Función **Copiar de documento** en las páginas **Abono compra** y **Pedido dev. compra**|Copia la cabecera y las líneas de un documento registrado que se revertirá.<br /><br /> Requiere que se active la casilla de verificación **Coste exacto devol. obligatorio** en la página **Configuración compras y pagos**.|

Para asignar manualmente la reversión del coste exacto, debe elegir el campo **Liquid.-de mov. pdto** en cualquier tipo de línea de documento, y seleccionar el número del movimiento de compra original. De este modo el pedido de abono de compra o de devolución de compra se vincula al movimiento de compra original y se asegura que el producto se valore con el coste unitario original.

Para obtener más información, consulte [Detalles de diseño: valoración de inventario](design-details-inventory-costing.md).

## Para crear un nuevo abono de compra desde una factura de compra registrada.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas compra** y, a continuación, elija el vínculo relacionado.  
2. En la página **Facturas de compra registradas**, seleccione la factura de compra que desea revertir y, a continuación, seleccione la acción **Crear abono correctivo**.

    La mayoría de los campos de la cabecera de abono de compra se rellenan con la información de la factura de compra registrada. Puede modificar todos los campos, por ejemplo, mediante la nueva información que indica el contrato de devolución.
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Liquidar movs.**.
5. En la página **Liquidar movimientos proveedor**, seleccione la línea con el documento de compra registrado al que desee liquidar el abono de compras y, a continuación, seleccione laacción **Liq. por id.**. El número del abono de compras se inserta en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.

    En la parte inferior de la página **Liq. movs. proveedor**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra el abono de compra, este se aplicará a los documentos de compra registrados especificados.

    Cuando ha creado o editado las líneas de abono de compra necesarias y se han especificado una o varias aplicaciones, puede empezar a registrar el abono de compra.
8. Seleccione la acción **Registrar**.

Las facturas de compra registradas a las que se aplica el abono ahora están revertidas. Si ya ha pagado la factura original, el proveedor ahora deberá reembolsarle el pago a usted. Si el abono es solo para parte del producto en la factura original, puede pagar solo el importe pendiente en la factura de compra original para cerrarla.

El abono de compra se ha eliminado y remplazado por un nuevo documento de la lista de abonos de compra registrados.

## Crear un nuevo abono de compra copiando una factura de compra registrada.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de compra** y, a continuación, elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de compras vacío.
3. En el campo **Proveedor**, escriba el nombre de un proveedor existente.
4. Elija la acción **Copiar de documento**.
5. En la página **Copiar doc. compra**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Elija el campo **Nº documento** para abrir la página **Histórico facturas compra** y seleccione la factura de compra registrada que contiene las líneas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de compra registradas copiadas se actualicen con los cambios en el precio y el coste unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en el abono de compra.
9. Complete el abono de compra como se explica en [Para crear un abono de compra de una factura de compras registrada](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## Crear un pedido de devolución de compras basado en uno o más documentos de compras registrados

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Devolución de pedidos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellen los campos de la ficha desplegable **General**.
4. En la ficha desplegable **Líneas**, rellene las líneas manualmente o copie la información de otros documentos para rellenar las líneas automáticamente:

    - Utilice la función **Revertir líneas documentos registrados:** para copiar una o más líneas de documentos registrados de uno o varios documentos registrados. Esta función revierte siempre exactamente los costes a partir de la línea de documento registrada. Esta función se describe en los pasos siguientes.    
    - Utilice la función **Copiar de documento** para copiar un documento existente al pedido de devolución. Utilice esta función para copiar el documento completo. Puede ser un documento registrado o un documento que todavía no se registró. Esta función sólo permite invertir el coste exacto cuando está seleccionada la casilla **Coste exacto devol. obligatorio** en la página **Configuración ventas y cobros**.  

5. Elija la acción **Revertir líneas documentos registrados**.
6. En la parte superior de la página **Histórico líneas doc. compras**, seleccione el campo **Mostrar sólo líneas reversibles** si solo desea ver las líneas con cantidades que aún no se han devuelto. Por ejemplo, si la cantidad de una factura de compra registrada ya se ha devuelto, puede que no desee incluir esa cantidad en un nuevo documento de devolución de compra.

    > [!NOTE]  
    >  Este campo sólo funciona para líneas de facturas, envíos y recepciones registradas, no para líneas de abonos o devoluciones registradas.  

    En la parte izquierda de la página, se listan los diferentes tipos de documento y el número que aparece entre corchetes muestra el número de documentos que hay disponible del tipo en concreto.

7. En el campo **Filtro de tipo de documento**, seleccione el tipo de líneas de documento registrado que desea utilizar.  
8. Seleccione las líneas que desea copiar en el nuevo documento.  

    > [!NOTE]  
    >  Si utiliza <kbd>Ctrl</kbd>+<kbd>A</kbd> para seleccionar todas las líneas, se copiarán todas las líneas incluidas en el filtro definido, pero se ignorará el filtro **Mostrar solo líneas reversibles**. Por ejemplo, imagine que ha filtrado las líneas en un número de documento determinado con dos líneas, una de las cuales ya se ha devuelto. Aunque el campo **Mostrar solo líneas reversibles** esté seleccionado, si seleccione <kbd>Ctrl</kbd>+<kbd>A</kbd> para copiar todas las líneas, se copiarán las dos líneas, en lugar de copiar solamente aquella que aún no se ha revertido.  

9. Seleccione **Aceptar** para copiar las líneas en el documento nuevo.  

    Tendrán lugar los siguientes procesos:  

    - Para las líneas de documentos registrados del tipo **Producto**, se crea una nueva línea de documento que es una copia de la línea del documento registrado, con la cantidad que aún no se ha revertido. El campo **Liquid. por nº orden producto** se rellena según corresponda con el número de movimiento de producto correspondiente a la línea del documento registrado.  

    - Para las líneas de documentos registrados que no sean del tipo **Producto**, como los cargos de producto, se crea una nueva línea de documento que es una copia de la línea del documento registrado original.  

    - Calcula el campo **Coste unitario (DL)** de la nueva línea a partir de los costes de los movimientos de producto correspondientes.  

    - Si el documento copiado es un envío, una recepción, una recepción de devolución o un envío de devolución registrados, el precio de venta se calcula automáticamente a partir de la ficha del producto.  

    - Si el documento copiado es una factura o un abono registrado, se copian el precio de venta, los descuentos de factura y los descuentos de línea de la línea del documento registrado.  

    - Si la línea del documento registrado contiene líneas de seguimiento de productos, el programa rellena el campo **Liq. por nº orden producto** de dichas líneas de seguimiento con los números de movimiento de producto correspondientes de las líneas de seguimiento de productos registradas.  

     Cuando se copia desde una factura o abono registrados, la aplicación copia los descuentos de factura y de línea válidos en el momento de registrar ese documento desde la línea del documento registrado a la nueva línea de documento. Sin embargo, tenga en cuenta que si se activa la opción **Calc. dto. factura** en la página **Configuración compras y pagos**, el descuento en factura se volverá a calcular cuando registre una línea de documento nueva. Por lo tanto, el importe de la nueva línea puede ser distinto del importe de la línea del documento registrado, dependiendo del nuevo cálculo de descuento de factura.  

    > [!NOTE]  
    >  Si ya se ha revertido, vendido o consumido parte de la cantidad de la línea del documento registrado, se crea una línea sólo para la cantidad que queda en inventario o que no se ha devuelto. Si ya se ha revertido toda la cantidad de la línea del documento registrado, no se crea una nueva línea de documento.  
    >
    >  Si el flujo de los artículos en el documento registrado coincide con el del nuevo documento, se crea una copia de la línea del documento registrado original en el nuevo documento. El campo **Liquid.-de mov. pdto** se ha rellenado porque, en este caso, la reversión de coste exacto no es posible. Por ejemplo, si utiliza la función **Revertir líneas documentos registrados** para obtener una línea de un abono de compras registrado para un nuevo abono de compras, sólo se copia la línea del abono registrado original en el nuevo abono.  

10. En la página **Pedido dev. compra**, en el campo **Cód. auditoría dev.** de cada línea, seleccione el motivo de la devolución.
11. Seleccione la acción **Registrar**.

## Para crear un pedido de sustitución a partir de un pedido de devolución de compra

Puede estar de acuerdo con el proveedor en que compense un producto comprado, sustituyendo el producto. El producto de sustitución puede ser el mismo u otro distinto. Esta situación se puede dar si el proveedor le envió por error un producto equivocado.  

1.  En la página **Pedido dev. compra** para un proceso de devolución activo, en una línea vacía, haga un movimiento negativo para el producto de reposición insertando un importe negativo en el campo **Cantidad** .  
2. Seleccione la acción **Mover líneas negativas**.  
3. En la página **Mover líneas compra negativas**, rellene los campos en una línea según sea necesario.
4. Elija el botón **Aceptar**. La línea negativa se elimina del pedido de devolución de compra y se crea un nuevo pedido de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).  

## Para crear una deducción de compra

Si los productos que recibe del proveedor no son satisfactorios, como cuando están dañados o son del color o tamaño incorrecto, es posible que el proveedor le ofrezca una deducción de compra.  

Puede registrar este coste reducido de compra como un cargo de producto en un abono o pedido de devolución, y vincularlo al albarán registrado. A continuación se describe esto para un pedido de devolución de compra, pero los mismos pasos se aplican a un abono de copra.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de compra** y, a continuación, elija el enlace relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de compras vacío.  
3. Rellene la cabecera de abono con información acerca del proveedor que le envió la deducción de compra.  
4. Seleccione **Cargo (prod.)** en el campo **Tipo** de la ficha desplegable **Líneas**.  
5. En el campo **N.º**, seleccione el valor de cargo apropiado de producto.  

    Puede que desee crear un número de coste de producto especial para cubrir las deducciones de compra.  
6. En el campo **Cantidad**, introduzca **1**.  
7. En el campo **Precio compra**, introduzca el importe de la deducción de compra.  
8. Asigne la deducción de compra como un cargo de producto a los productos del albarán registrado. Para obtener más información, consulte [Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md). Una vez asignada la deducción, vuelva a la página **Abono de compra**.

Cuando registre el pedido de devolución de compra, la deducción de compra se añadirá al importe del movimiento de compra correspondiente. De este modo podrá mantener la precisión de la valoración del inventario.  

## Para combinar envíos devueltos

Si desea devolver los productos cubiertos por distintos pedidos de devolución de compra al mismo vendedor, entonces puede utilizar la función **Combinar envíos devueltos**.  

Cuando envíe los productos, registre los pedidos de devolución de compras relacionados como enviados para crear albaranes de devolución de compra registrados.  

Cuando vaya a facturar estos productos, en lugar de facturar cada pedido de devolución de compra por separado, cree un abono de compra y copie automáticamente las líneas de envío de devolución de compra registradas en este documento. Luego registre el abono de compra y facture con comodidad todos los pedidos de devolución de compra pendientes al mismo tiempo.  

Cuando se combinan envíos devueltos en un abono y se registran, se crea un abono de compra registrado para las líneas facturadas. El campo **Cantidad facturada** del pedido de devolución de compra de origen se actualiza en función de la cantidad facturada. Sin embargo, este pedido de devolución de compra original no se elimina, aunque se haya recibido y facturado por completo, por lo que debe eliminar el pedido de devolución de compra manualmente.

> [!NOTE]  
> El procedimiento siguiente supone que hay varios pedidos de devolución de compra para el proveedor y que están registrados como enviados.     

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de compra** y, a continuación, elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene los campos como sea necesario.  
4. Elija la acción **Traer líns. envío dev.**.  
5. Seleccione las diversas líneas de envío de devolución que desee incluir en la factura.  

    Si ha seleccionado una línea de envío de devolución incorrecta o desea comenzar desde el principio, solo elimine las líneas del abono de compra y vuelva a usar la función **Traer líns. envío devol.**  
6. Seleccione la acción **Registrar**.  

### Para eliminar pedidos de devolución de compra abiertos después del registro del envío de devolución  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Eliminar pedidos de devolución de compra facturados** y, a continuación, elija el enlace relacionado.  
2. Rellene los campos según sea necesario y, a continuación, haga clic en el botón **Aceptar**.  
3. También puede eliminar los pedidos de devolución de compra individuales manualmente.

## Consultar la [formación de Microsoft](/training/paths/return-items-dynamics-365-business-central/) relacionada

## Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Corregir o cancelar facturas de compra sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procesamiento de devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
