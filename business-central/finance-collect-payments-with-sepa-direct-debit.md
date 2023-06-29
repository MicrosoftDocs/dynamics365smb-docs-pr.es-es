---
title: Adeudo directo SEPA en Business Central
description: 'Con el consentimiento de sus clientes, puede cobrar los pagos directamente al banco del cliente según el formato SEPA.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="collect-payments-with-sepa-direct-debit"></a><a name="collect-payments-with-sepa-direct-debit"></a><a name="collect-payments-with-sepa-direct-debit"></a>Cobrar pagos mediante adeudo directo SEPA

Con el consentimiento de sus clientes, puede cobrar los pagos directamente al banco del cliente según el formato SEPA.  

En primer lugar, configure el formato de exportación del archivo de banco que indica a su banco que debe realizar un adeudo directo. A continuación, configure la forma de pago del cliente. Por último, establezca la orden de domiciliación de adeudo directo que refleja el acuerdo con el cliente para cobrar sus pagos en un período de acuerdo determinado.  

Para indicar al banco que transfiera el importe de pago desde el banco del cliente al banco de su empresa, debe crear un movimiento de cobro por adeudo directo que contiene información acerca de los bancos, las facturas de venta afectadas y la orden de domiciliación de adeudo directo. Luego exporta un archivo XML que se basa en el movimiento de cobro y que se envía al banco para su procesamiento. Los pagos que el banco no pudo procesar los comunicará el usuario al banco y el usuario deberá rechazar manualmente los movimientos de pago por adeudo directo en cuestión.  

Puede establecer códigos de venta estándar del cliente con la información de forma de pago y orden de domiciliación de adeudo directo. Puede utilizar el trabajo por lotes **Crear facturas clientes estándar** para generar varias facturas de venta con la información de domiciliación rellenada previamente. Esto puede realizarse manual o automáticamente, según la fecha de vencimiento del pago.  

Cuando los pagos se procesan correctamente, según lo ha comunicado el banco, puede registrar los recibos de pago directamente desde la página **Movimientos de cobros por adeudo directo** o mover las líneas de pago en el diario en el que contabiliza los recibos de pago, como la página **Diario de recibos de efectivo**. Como alternativa, en función del proceso de administración de efectivo, puede esperar y simplemente aplicar los pagos como parte de la conciliación bancaria.  

> [!NOTE]  
> Para cobrar los pagos mediante adeudo directo SEPA, la divisa de la factura de venta debe ser EURO.  

## <a name="setting-up-sepa-direct-debit"></a><a name="setting-up-sepa-direct-debit"></a><a name="setting-up-sepa-direct-debit"></a>Configuración de domiciliaciones de adeudo directo SEPA

Desde la página **Cobros por adeudo directo** puede exportar instrucciones al banco electrónico para realizar recaudar un adeudo directo desde el banco del cliente a su cuenta bancaria, según el formato de débito directo de SEPA.

> [!NOTE]
> La versión global de [!INCLUDE[prod_short](includes/prod_short.md)] solo admite el formato de débito directo de SEPA. La versión de su país o región puede admitir otros formatos para pago electrónico. Consulte **Funcionalidad local** en el contenido.  

Para habilitar la exportación de formatos de archivos bancarios no compatibles originales en [!INCLUDE[prod_short](includes/prod_short.md)], puede configurar una definición de intercambio de datos mediante el marco de intercambio de datos. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

Para poder procesar pagos de clientes electrónicamente exportando instrucciones de adeudo directo en formato de adeudo directo SEPA, debe realizar los pasos de configuración siguientes:  

* Configure el formato de exportación del archivo bancario que indica a su banco que debe recaudar un adeudo directo desde el banco del cliente a cuenta bancaria.  
* Configure la forma de pago del cliente.  
* Establezca la orden de adeudo directo que refleja el acuerdo con el cliente para cobrar sus pagos en un período de acuerdo determinado.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a><a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Configuración del banco para adeudo directo SEPA

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.  
2. Abra el banco que desea utilizar para el adeudo directo.  
3. En la ficha desplegable **Transferencia**, en el campo **Formato exportación de adeudo directo SEPA**, elija la opción para adeudo directo SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a><a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Configuración de la forma de pago del cliente para adeudo directo SEPA

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de pago** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Configure una forma de pago. Rellene los campos específicos del adeudo directo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Adeudo directo**|Especifique si la forma de pago es para el cobro por adeudo directo SEPA.|  
    |**Código términos pago adeudo directo**|Especifique los términos de pago, tal como NO PAGAR, que se muestran en las facturas de venta que paguen mediante adeudo directo SEPA para indicar al cliente que el pago se cobrará automáticamente. Como alternativa, deje el campo en blanco.|  

    > [!NOTE]  
    >  No especifique ningún valor en el campo **Bal. Nº cuenta**.  

4. Elija el botón **Aceptar** para cerrar la página **Métodos pago**.  
5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
6. Abra la ficha del cliente que desee configurar para los cobros por adeudo directo SEPA.  
7. Elija el campo **Código método pago** y seleccione el código de la forma de pago que especificó en el paso 3.  
8. Repita los pasos 6 a 7 para todos los clientes que desea configurar para el cobro por adeudo directo SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a><a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Configuración de la orden de domiciliación de adeudo directo que representa el acuerdo del cliente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Abra la ficha del cliente que desee configurar para adeudos directos SEPA.  
3. Elija la acción **Cuentas bancarias**.  
4. En la página **Lista bancos cliente**, seleccione el banco de cliente que utilizará domiciliaciones y, a continuación, elija la opción **Órdenes de domiciliación de adeudo directo**.  
5. En la página **Órdenes de domiciliación de adeudo directo SEPA**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código banco cliente**|Especifica el banco desde el que se cobran los pagos por domiciliación. Este campo se rellena automáticamente.|  
    |**Válido desde**|Especifique la fecha en que inicia la orden de domiciliación de adeudo directo.|  
    |**Válido hasta**|Especifique la fecha en que finaliza la orden de domiciliación de adeudo directo.|  
    |**Fecha de firma**|Especifique la fecha en que el cliente firmó la orden de domiciliación de adeudo directo.|  
    |**Tipo de pago**|Especifica si el contrato cubre varios (**Pago recurrente**) cobros por adeudo directo o uno solo (**Pago único**).|  
    |**Número de debe esperado**|Especifica el número de cobros por adeudo directo que espera efectuar. Este campo solo es pertinente si ha seleccionado **Pago recurrente** en el campo **Tipo de pago**.|  
    |**Contador debe**|Especifica el número de cobros por adeudo directo que se realizaron con esta orden de domiciliación de adeudo directo. Este campo se actualiza automáticamente.|  
    |**Bloqueado**|Especifique que los cobros por adeudo directo no se pueden realizar con esta orden de domiciliación de adeudo directo.|  

6. Repita los pasos 1 a 5 para todos los clientes que desea configurar para adeudos directos SEPA.  

 La orden de domiciliación de adeudo directo se inserta automáticamente en el campo **Id. de orden de domiciliación** de adeudo directo cuando se crea una factura de venta para el cliente que ha seleccionado en el paso 2. Para obtener más información, vea [Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a><a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a><a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario

Para indicar al banco que transfiera el importe de pago desde el banco del cliente al banco de su empresa, debe crear un cobro por adeudo directo que contiene información acerca de los bancos del cliente, las facturas de venta afectadas y la orden de domiciliación de adeudo directo. Desde el movimiento de pago por domiciliación, luego exporta un archivo XML que se envía o carga en el banco electrónico para su procesamiento. Los pagos que el banco no pudo procesar los comunicará el banco al usuario y este último deberá rechazar manualmente los movimientos de pago por adeudo directo en cuestión.  

 > [!NOTE]  
 > Para cobrar los pagos mediante adeudo directo SEPA, la divisa de la factura de venta debe ser EURO.  

### <a name="to-create-a-direct-debit-collection"></a><a name="to-create-a-direct-debit-collection"></a><a name="to-create-a-direct-debit-collection"></a>Creación de un cobro por domiciliación

 1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cobros por adeudo directo** y, a continuación, elija el vínculo relacionado.  
 2. En la página **Cobros por adeudo directo**, elija la acción **Crear cobro por adeudo directo**.  
 3. En la página **Crear cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Fecha vencimiento inicio**|Especifique la primera fecha de vencimiento de pago más temprana de las facturas de venta para las que desee crear un cobro por domiciliación.|  
    |**Fecha de vencimiento final**|Especifique la fecha de vencimiento de pago más tarde de las facturas de venta para las que desee crear un cobro por domiciliación.|  
    |**Tipo socio**|Especifique el cobro por domiciliación se realiza para los clientes de tipo **Empresa** o **Persona**.|  
    |**Solo clientes con orden de domiciliación válida**|Especifique si se crea un cobro por adeudo directo para los clientes que tienen una orden de domiciliación de adeudo directo válida. **Nota**: Se crea un cobro por domiciliación incluso si el campo **Id. de orden de domiciliación de adeudo directo** no se ha rellenado en la factura de venta.|  
    |**Solo facturas con orden de domiciliación válida**|Especifique si se crea un cobro de adeudo directo solo para las facturas de ventas si se selecciona una orden de domiciliación de adeudo directo válida en el campo **Id. de orden de domiciliación de adeudo directo** en la factura de ventas.|  
    |**N.º cuenta bancaria**|Especifique a cuál de los bancos de su empresa se transferirá el pago cobrado desde el banco del cliente.|  
    |**Nombre banco**|Especifica el nombre del banco seleccionado en el campo **Cód. cuenta banco**. Este campo se rellena automáticamente.|  

 4. Elija el botón **Aceptar**.  

Se agrega un cobro por domiciliación a la página **Cobros por adeudo directo** y se crean uno o varios movimientos de cobros por domiciliación.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a><a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a><a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Exportación de movimientos de cobro por domiciliación a un archivo de banco

 1. En la página **Cobros por adeudo directo**, elija la acción **Movimientos de cobros por adeudo directo**.  
 2. En la página **Movimientos de cobros por adeudo directo**, seleccione el movimiento que desee exportar y, a continuación, elija la acción **Crear archivo de cobro por adeudo directo**.  
 3. Guarde el archivo de exportación en la ubicación desde donde envía o carga en el banco electrónico.  

      En la página **Direct Debit Collect. Movimientos**, el campo **Estado cobro por adeudo directo** se cambia el archivo creado. En la página **Órdenes de domiciliación de adeudo directo SEPA**, el campo **Contador debe** se actualiza con un recuento.  

 Si el archivo exportado no se puede procesar, por ejemplo, porque el cliente es insolvente, puede rechazar el movimiento de cobro por domiciliación. Si el banco procesa correctamente el archivo exportado, los pagos por vencimientos de las facturas de venta implicadas se cobran automáticamente de los clientes implicados. En ese caso, puede cerrar el cobro.  

### <a name="to-reject-a-direct-debit-collection-entry"></a><a name="to-reject-a-direct-debit-collection-entry"></a><a name="to-reject-a-direct-debit-collection-entry"></a>Rechazo de un movimiento de cobro por domiciliación

* En la página **Movimientos de cobros por adeudo directo**, seleccione el movimiento que no se procesó correctamente y, a continuación, elija la acción **Rechazar movimiento**.  

    El valor del campo **Estado** de la página **Movimientos de cobros por adeudo directo** se cambia a **Rechazada**.  

### <a name="to-close-a-direct-debit-collection"></a><a name="to-close-a-direct-debit-collection"></a><a name="to-close-a-direct-debit-collection"></a>Cierre de un cobro por domiciliación

* En la página **Movimientos de cobros por adeudo directo**, seleccione el movimiento que se procesó correctamente y, a continuación, elija la acción **Cerrar cobro**.  

    El cobro por domiciliación relacionado está cerrado.  

 Ahora podrá registrar los recibos de pago para las facturas de venta implicadas. Puede hacerlo, ya que normalmente se registran recibos de pago, como en la página **Registro de pago**, o bien puede registrar los recibos de pago relacionados directamente en la página **Movimientos de cobros por adeudo directo**. Para obtener más información, consulte [Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a><a name="posting-sepa-direct-debit-payment-receipts"></a><a name="posting-sepa-direct-debit-payment-receipts"></a>Registro de recibos de pagos de domiciliación de adeudo directo SEPA

Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas. Para obtener más información, consulte [Crear movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Puede registrar el recibo de pago directamente desde la página **Cobros por adeudo directo** o la página **Movimientos de cobros por adeudo directo**. Como alternativa, puede delegar el trabajo a otro usuario mediante la preparación de las líneas de diario relacionadas.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Registro de un recibo de pago de domiciliación desde la página Cobros por adeudo directo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cobros por adeudo directo** y, a continuación, elija el vínculo relacionado.  
2. Seleccione una línea para un cobro por adeudo directo que se ha exportado a un archivo de banco y procesado correctamente por el banco.
3. Seleccione la acción **Registrar recibos de pago**.  
4. En la página **Registrar cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº cobro por adeudo directo**|Especifique el cobro por adeudo directo para el que desea registrar el albarán de pago.|  
    |**Plantilla de libros diario general**|Especifique la plantilla de diario general que se debe usar para registrar el albarán de pago, tal como la plantilla de recibo de cobro.|  
    |**Nombre sección diario general**|Especifique qué sección del diario general se debe usar para registrar el albarán de pago.|  
    |**Crear solo diario**|Seleccione esta casilla si no desea registrar el recibo de pago al seleccionar el botón **Aceptar**. El recibo de pago se preparará en el diario especificado y no se registrará hasta que alguien registre las líneas de diario en cuestión.|  

5. Elija el botón **Aceptar**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Administrar cobros](receivables-manage-receivables.md)  
[Gestión de servicios](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
