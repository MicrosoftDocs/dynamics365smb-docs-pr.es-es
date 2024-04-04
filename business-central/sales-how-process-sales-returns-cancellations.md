---
title: Procesamiento de devoluciones de ventas o cancelaciones
description: 'Describe cómo crear un abono de venta para procesar una devolución, una cancelación o un reembolso de productos o servicios de los que ha recibido el pago.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procesamiento de devoluciones de ventas o cancelaciones

Si un cliente desea devolver u obtener un reembolso de algún producto o servicio que usted ha vendido y que le han pagado, debe crear y registrar una abono de ventas que especifique el cambio requerido. Para incluir la información correcta de la factura de venta, puede hacer lo siguiente:  

- Crear una nota de abono de venta directamente desde un histórico de facturas de venta.
- Cree una nueva nota de abono de ventas con la información de la factura copiada.

Si necesita más control del proceso de devolución de ventas, como documentos de almacén para el manejo de artículos o una mejor descripción al recibir productos de varios documentos de ventas con una sola devolución de ventas, puede crear órdenes de devolución de ventas. Una orden de devolución de ventas emite automáticamente la nota de crédito de ventas relacionada y otros documentos relacionados con la devolución, como una orden de venta de reemplazo, si es necesario. Para obtener más información, consulte [Procesar pedidos de devolución de ventas](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Si una factura de venta registrada aún no se ha pagado, puede usar las funciones **Corregir** o **Cancelar** en la factura de venta registrada para revertir las transacciones. Estas funciones solo funcionan para las facturas sin pagar y no admiten devoluciones o cancelaciones parciales. Para obtener más información, vea [Corregir o cancelar las facturas de venta sin abonar](sales-how-correct-cancel-sales-invoice.md)

Una devolución o reembolso se puede relacionar con solo algunos de los productos o servicios de la factura de venta original. En ese caso, debe editar la información de las líneas del abono de venta o en el pedido de devolución de ventas. Cuando se registra el abono de venta o el pedido de devolución de ventas, se revierten los documentos de venta que se ven afectados por el cambio y se puede crear un pago de devolución para el cliente. Para obtener más información, consulte [Creación de pagos](payables-make-payments.md).  

El registro del abono también revertirá cualquier coste de producto que se hubiera asignado al documento registrado, de forma que los movimientos de valor del producto son los mismos de antes que se asignara el cargo de producto.

> [!NOTE]
> Los aspectos de contabilidad de las devoluciones de ventas, como los pagos de reembolso a los clientes, se consideran trabajo de contabilidad y no se describen aquí. Para obtener más información, vea [Administración de pagos](payables-manage-payables.md).

## Para crear un nuevo abono de venta desde una factura de venta registrada.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.  
2. En la página **Histórico facturas venta**, seleccione el histórico de facturas de venta que desea revertir, elija la acción **Cancelar** y, a continuación, seleccione la acción **Crear abono correctivo**.

    La cabecera del abono de venta contiene información de la factura de venta registrada. Puede modificarla, por ejemplo, mediante la nueva información que indica el contrato de devolución.  
3. Edite la información de las líneas según el contrato, como por ejemplo el número de productos devueltos o el importe que se reembolsará.
4. Seleccione la acción **Preparar** y, a continuación, seleccione la acción **Liquidar movs**.
5. En la página **Liquidar movimientos cliente**, seleccione la línea con el documento de ventas registrado al que desee liquidar el abono de ventas y, a continuación, seleccione la acción **Liq. por id.**.

    El identificador del abono de ventas se muestra en el campo **Liq. por id**.
6. En la línea del campo **Importe a liquidar**, introduzca el importe que desea liquidar si es menor que el importe original.  

    En la parte inferior de la página **Liq. movs. cliente**, puede observar el importe total a liquidar para revertir todos los movimientos correspondientes, concretamente cuando el valor en el campo **Balanza** es cero.
7. Elija el botón **Aceptar**. Cuando registra el abono de venta, este se aplica a los documentos de venta registrados.

    Después de crear o editar las líneas de abono de venta y especificar una o varias aplicaciones, puede registrar el abono de venta.  
8. Elija la acción **Registro** y, a continuación, seleccione la acción **Registrar y enviar**.  

El cuadro de diálogo de **Registrar y enviar confirmación** se abre para mostrar el método de envío preferido para el cliente. Puede cambiar el método de envío seleccionando el botón de búsqueda en el campo **Enviar documento a**. Para obtener más información, vea [Configurar los perfiles de envío de documentos](sales-how-setup-document-send-profiles.md).  

Los documentos de venta registrados a los que ha aplicado el abono están invertidas y se puede crear un pago del reembolso para el cliente. El abono de venta se ha eliminado y remplazado por un nuevo documento de la lista de abonos de venta registrados.

## Crear un nuevo abono de venta copiándolo desde una factura de venta registrada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de ventas vacío.
3. En el campo **Nombre cliente**, escriba el nombre de un cliente existente.
4. Seleccione la acción **Preparar** y, a continuación, seleccione la acción **Copiar documento**.
5. En la página **Copiar documento de ventas**, en el campo **Tipo de documento**, seleccione el campo **Factura registrada**
6. Elija el campo **N.º documento** para abrir la página **Histórico facturas venta** y seleccione el registro de histórico de facturas de venta que contiene las línas que desea revertir.
7. Seleccione la casilla **Recalcular líneas** si desea que las líneas de factura de venta registradas copiadas se actualicen con los cambios en el precio y el coste unitario del producto desde que la factura fue registrada.
8. Elija el botón **Aceptar**. Las líneas de factura copiadas se insertarán en el abono de venta.
9. Complete el abono de venta como se explica en [Para crear un abono de ventas de una factura de ventas registrada](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## Para crear una deducción de venta
Puede enviar un abono a un cliente con una reducción en el precio si el cliente ha recibido los productos ligeramente dañados o si los ha recibido con retraso.  
Registre este precio reducido como un cargo de producto en un abono o una devolución y asígnelo al envío registrado. A continuación se describe esto para un abono de venta, pero los mismos pasos se aplican a un pedido de devolución.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo** para abrir un abono de ventas vacío.
3. Rellene la cabecera de abono con información acerca del cliente al que desea conceder la deducción de venta.  
4. Seleccione **Cargo (prod.)** en el campo **Tipo** de la ficha desplegable **Líneas**.  
5. En el campo **N.º**, seleccione el valor de cargo apropiado de producto.  
     Puede que desee crear un número de cargo de producto especial para cubrir las deducciones de venta.  
6. En el campo **Cantidad**, introduzca **1**.  
7. En el campo **Precio de venta IVA excl.**, introduzca el importe de la deducción de venta.  
8. Asigne la deducción de venta como un cargo de producto a los productos del albarán registrado. Para obtener más información, consulte [Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md). Una vez asignada la deducción, vuelva a la página **Abono venta**.  

Cuando registre el pedido de devolución de ventas, la deducción de ventas se añadirá al importe del movimiento de ventas correspondiente. De este modo podrá mantener la precisión de la valoración del inventario.

## Agrupar recibos de devolución
Puede agrupar recibos de devolución si su cliente devuelve varios productos incluidos en distintos pedidos de devolución de ventas.  

Cuando reciba los productos en el almacén, registre los pedidos de devolución de ventas correspondientes como recibidos. Esto crea recibos de devolución registrados.  

Cuando vaya a facturar al cliente en cuestión, en lugar de facturar cada pedido de devolución de ventas por separado, cree un abono de venta y copie automáticamente las líneas de recepción de devolución registradas en el documento. Luego registre el abono de venta y facture cómodamente todos los pedidos de devolución de venta pendientes de una sola vez.  

Para agrupar recibos de devolución deberá activar la casilla de verificación **Fact. automática** de la página **Ficha cliente**.  

### Para agrupar recibos de devolución de forma manual  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, rellene los campos como sea necesario.  
4. Elija la acción **Traer líns. recep. dev.**.  
5. Seleccione las líneas de la recepción de devolución que desea incluir en el abono:  

    - Para insertar todas las líneas, selecciónelas y haga clic en **Aceptar**.  

    - Para insertar líneas concretas, selecciónelas y haga clic en **Aceptar**.  
6.  Si se ha seleccionado una línea de envío incorrecta o desea volver a empezar, sólo tiene que eliminar las líneas del abono y volver a ejecutar la función **Traer líns. recep. dev.**  
7.  Registrar la factura.  

### Agrupar automáticamente recepciones de devolución

Puede agrupar recepciones de devolución de forma automática y registrar los abonos automáticamente utilizando la función **Fact. autom. recep. dev.**  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Fact. autom. recep. dev.** y, a continuación, elija el vínculo relacionado.
2. En la página **Fact. autom. recep. dev...** , rellene los campos para seleccionar las recepciones de devolución relevantes.
3. Seleccione la casilla de verificación **Registrar abonos**. De lo contrario, deberá registrar manualmente los abonos resultantes de compra.
4. Elija el botón **Aceptar**.  

### Para eliminar un pedido de devolución recibido y facturado

Al facturar recepciones de devolución de esta forma, los pedidos de devolución a partir de los cuales se registraron las recepciones de devolución siguen existiendo, aunque se hayan recibido y facturado por completo.  

Cuando las recepciones de devolución se agrupan en un abono y se registran, se crea un abono de venta registrado para las líneas abonadas. El campo **Cantidad facturada** de la devolución de venta de origen se actualiza en función de la cantidad facturada.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Eliminar pedidos de devolución de venta facturados** y, a continuación, elija el enlace relacionado.  
2. Especifique en el campo de filtro **Nº.** que pedidos de devolución desea eliminar.  
3. Elija el botón **Aceptar**.  

También puede eliminar los pedidos de devolución de venta individuales manualmente.  

## Inventario y valoración

Para conservar la valoración correcta del inventario, normalmente desea devolver los artículos devueltos al inventario al costo unitario en el que fueron vendidos, no al costo unitario actual. Esto se denomina reversión de coste exacto.

Existen dos funciones para asignar la reversión de coste exacta automáticamente:  

|Función|Descripción|  
|------------------|---------------------------------------|  
|Función **Revertir líneas documentos registrados** en la página **Pedido dev. venta**|Copia una o varias líneas de documentos registrados para revertirlas en el pedido de devolución de ventas. Para obtener más información, consulte [Crear un pedido de devolución de ventas basado en uno o más documentos de ventas publicados](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|Función**Copiar líneas** en las páginas **Abono venta** y **Pedido dev. venta**.|Copia la cabecera y las líneas de un documento registrado que se revertirá.<br /><br /> Requiere que se active la casilla de verificación **Coste exacto devol. obligatorio** en la página **Configuración ventas y cobros**.|

Para asignar manualmente la reversión del coste exacto, debe elegir el campo **Liquid.-de mov. pdto** en cualquier tipo de línea de documento, y seleccionar el número del movimiento de venta original. De este modo el pedido de abono de venta o de devolución de venta se vincula al movimiento de venta original y se asegura que el producto se valore con el coste unitario original.

Para obtener más información, consulte [Detalles de diseño: valoración de inventario](design-details-inventory-costing.md).

## Consulte también

[Ventas](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
