---
title: Crear facturas de prepagos
description: Gestione situaciones en las que usted o su proveedor requieran prepago. Utilice los porcentajes predeterminados de cada línea de venta o de compra o ajuste el importe según sea necesario.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 10/04/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a>Crear facturas de prepagos

Si requiere que sus clientes paguen antes de enviarles su pedido, puede usar las características de prepago. Lo mismo se aplica si su proveedor requiere que pague antes de enviarle un pedido.  

Puede iniciar el proceso de prepago cuando cree un pedido de venta o de compra. El porcentaje de prepago predeterminado para un producto del pedido o para el cliente o proveedor, se incluirá en la factura de prepago. También puede especificar un porcentaje de prepago para todo el documento.

Después de crear un pedido de venta o de compra, puede crear una factura de prepago para este. Utilice los porcentajes predeterminados de cada línea de venta o de compra o ajuste el importe. Por ejemplo, podría especificar un importe total para todo el pedido.  

El procedimiento siguiente describe cómo facturar un prepago del pedido de venta. Los pasos son parecidos para pedidos de compra.  

## <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de prepago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Cree un pedido de venta nuevo para un cliente relevante. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  

    En la ficha desplegable **Prepago**, el campo **% de prepago** especifica el porcentaje que se utilizará para calcular el importe de prepago. Si existe un porcentaje de prepago predeterminado en la ficha del cliente, el campo se rellenará automáticamente. Puede cambiar el porcentaje. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Elija el campo **Compreión prepago** si desea crear líneas en la factura de prepago que combinen líneas del pedido de cliente si:  

    - Tienen la misma cuenta para los prepagos, tal y como lo haya determinado en la configuración de grupos contables.  
    - Tienen las mismas dimensiones.  

    Si desea especificar una factura de prepago con una línea para cada línea de pedido de venta que tenga un porcentaje de prepago, después, no elija el campo **Compresión prepago**.  

    La fecha de vencimiento del prepago se calcula automáticamente en función del valor de **Código términos prepago**.

    > [!NOTE]
    > Cuando algunas líneas de una factura requieren un prepago del 100 % y otras líneas no, y hay IVA en la cuenta de prepago, el monto redondeado puede generar un error al crear una factura de prepago. El error se produce porque el importe de la factura de prepago es superior a los importes de las líneas del documento. Para solucionar el problema, cambie los montos en una o todas las líneas que requieren el 100% de prepago. El cambio volverá a calcular el redondeo del importe del IVA y utilizará la diferencia de redondeo acumulada en la última línea modificada.
    >
    > Dos formas más de solucionar el problema son:
    >
    > * Cree un grupo contable de productos con IVA independiente y una configuración de tipo de registro de IVA con un identificador de IVA independiente y utilícelos para los productos o líneas que requieran un prepago del 100 %. El redondeo se realiza para cada identificador de IVA, por lo que se realizará un redondeo por separado para los productos que se asignan al grupo contable de productos con IVA.
    > * Use una factura independiente para los productos o líneas que requieren y no requieren pagos anticipados del 100 %.

3. Rellene las líneas de venta.  

    Si ha especificado un porcentaje de prepago predeterminado para el cliente o en la ficha desplegalbe **Prepago** en este documento, este valor se copia en cada línea. Puede cambiar el contenido del campo **% de prepago** en la línea.  

    > [!TIP]
    > Si no ve el campo **% prepago**, puede agregarlo a través de la personalización.  Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

4. Para ver el importe de prepago total, elija la acción **Estadísticas**.

    Si desea ajustar el importe de prepago total para el pedido, puede cambiar los contenidos del campo **Importe prepago** en la página **Estad. pedido ventas**.  

    Si se selecciona el campo **Precios IVA incluido**, el campo **Cantidad prepago incl. IVA** se puede modificar.  

    Si cambia el contenido del campo **Cantidad prepago**, la cantidad se distribuirá proporcionalmente entre todas las líneas, excepto aquellas líneas cuyo valor es **0** en el campo **% de prepago**.  

5. Para imprimir un test antes de registrar la factura de prepago, elija las acciones **Prepago** e **Informe test prepago**.  
6. Para registrar una factura de prepago, elija las acciones **Prepago** y **Registrar factura prepago**.  

    Para registrar e imprimir la factura de prepago, seleccione la acción **Registrar e imprimir factura prepago**.  

Puede emitir otras facturas de prepago adicionales para el pedido. Para emitir otra factura, aumente la cantidad de prepago de una o varias líneas, ajuste la fecha del documento si es necesario y registre la factura de prepago. Se creará una nueva factura con la diferencia entre las cantidades de prepago facturadas hasta el momento y la nueva cantidad de prepago.  

> [!NOTE]  
> Si se encuentra en América del Norte, no puede cambiar el porcentaje de prepago después de que se haya contabilizado la factura de prepago. Esto se evita en la versión americana de [!INCLUDE[prod_short](includes/prod_short.md)] porque el cálculo del impuesto sobre las ventas, de otra manera, sería incorrecto.  

 Cuando esté listo para registrar el resto de la factura, hágalo del mismo modo que lo haría con cualquier otra factura; la cantidad de prepago se descontará automáticamente del importe vencido.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Actualizar el estado de los pedidos y facturas prepago automáticamente

Puede acelerar el procesamiento de pedidos y facturas configurando entradas de cola de trabajos que actualizan automáticamente el estado de esos documentos. Cuando se paga una factura de prepago, las entradas de la cola de trabajos pueden cambiar automáticamente el estado del documento de **Pago anticipado pendiente** a **Liberado**. Cuando configure las entradas de la cola de trabajos, las unidades de código que necesitará usar son **384 actualizado Pendiente Prepago Ventas** y **384 actualizado Pendiente Prepago Compra**. Le recomendamos que programe las entradas para que se ejecuten con frecuencia, por ejemplo, cada minuto. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Consulte también .

[Facturar prepagos](finance-invoice-prepayments.md)  
[Tutorial: configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
