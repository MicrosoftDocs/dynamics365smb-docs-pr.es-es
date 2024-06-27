---
title: Configurar prepagos
description: Aprenda a configurar Business Central para utilizar prepagos para facturar y cobrar depósitos de los clientes y remitir depósitos a los proveedores.
author: brentholtorf
ms.reviewer: bholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: '314, 459, 460, 664'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-prepayments"></a>Configurar prepagos

Utiliza prepagos cuando:

* Usted requiere que sus clientes envíen el pago antes de enviarles un pedido.
* Su proveedor le exige que realice el pago antes de enviarle un pedido.

Los prepagos le permiten facturar y cobrar depósitos de los clientes o remitir depósitos a proveedores y asegurarse de que todos los pagos parciales se contabilicen con una factura. Para obtener más información, consulte [Crear una factura de prepago](finance-how-to-create-prepayment-invoices.md).

Para poder registrar facturas de prepago, debe configurar las cuentas auxiliares en la contabilidad y configurar series numéricas para documentos de prepago. Debe especificar una cuenta para los prepagos relacionados con las ventas y otra cuenta para los prepagos relacionados con las compras. Puede especificar las mismas cuentas de contabilización para todos los pagos anticipados relacionados con todos los grupos generales de contabilización de empresas o grupos generales de contabilización de productos. También puede especificar cuentas específicas para grupos contables específicos para ventas y compras, respectivamente. El mejor método a utilizar depende de los requisitos de su empresa para el seguimiento de los prepagos.  

Puede definir el porcentaje del importe de línea que se va a facturar para el prepago, para un cliente o proveedor, para todos los productos o para algunos. Una vez que finalice la configuración, puede generar facturas de prepago a partir de pedidos de compra y venta. Puede usar los porcentajes predeterminados para cada línea de compra o venta o cambiar los importes en la factura según sea necesario. Por ejemplo, puede especificar un importe total para todo el pedido.  

> [!NOTE]
> Recomendamos no utilizar un porcentaje de prepago de 100 en los siguientes casos:
>
> * Si se encuentra en América del Norte. Debido a cómo se calculan los impuestos, un porcentaje de prepago de 100 puede generar problemas con las facturas de prepago.
> * En todas las regiones, si deduce manualmente un descuento por pago de la factura. Un porcentaje de prepago de 100 no dejará automáticamente un importe del que deducir el descuento.
>
> Además, cuando utiliza un porcentaje de prepago de 100, [!INCLUDE[prod_short](includes/prod_short.md)] podría necesitar crear entradas de redondeo de compensación. Cuando eso suceda, deberá elegir una cuenta de en el campo **Cuenta de redondeo de facturas** en la página **Grupos contables de clientes**. Esto es cierto incluso si no ha activado el conmutador **Redondeo de facturas** en la página **Configuración de ventas y clientes**. Si no especifica una cuenta, no podrá contabilizar facturas de prepago.

El importe prepagado pertenece al comprador hasta que reciba los bienes o servicios. Debe configurar cuentas del libro mayor para retener los importes de los pagos anticipados hasta que contabilice la factura final. Los pagos anticipados de ventas deben registrarse en una cuenta de pasivo hasta que se envíen los artículos. Los prepagos de compras deben registrarse en una cuenta de activos hasta que se reciban los productos. Además, debe configurar distintas cuentas contables generales para cada identificador del IVA.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Para agregar cuentas de prepago a la configuración de grupos contables

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración grupos contables** y luego elija el enlace relacionado.
2. En la página **Configuración grupos contables**, rellene los campos siguientes para las líneas relevantes:  

    * **Cuenta prepago ventas**  
    * **Cuenta prepagos compras**  

Si todavía no ha configurado cuentas de contabilidad para prepagos, puede abrir la página **Lista de cuentas** desde el campo de cuenta relevante.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Configurar números de serie para documentos de prepago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Configuración de ventas y cobros**, en la ficha desplegable **Serie numérica**, complete los siguientes campos:  

   * **Nº fact. prepago registrada**
   * **Nº abono prepago registrado**

3. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de compras y pagos** y luego elija el enlace relacionado.
4. En la página **Configuración de compras y pagos**, en la ficha desplegable **Serie numérica**, complete los siguientes campos:

    * **Nº fact. prepago registrada**
    * **Nº abono prepago registrado**

> [!NOTE]  
> Puede utilizar la misma numeración de serie para las facturas de prepago y las facturas normales, o bien utilizar numeraciones de serie distintas. Si utiliza series distintas, éstas no deben solaparse, ya que no debe haber ningún número que se repita en ambas series.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Definir porcentajes de prepago para productos, clientes y vendedores

Puede definir un porcentaje de prepago predeterminado de un producto para todos los clientes, un cliente determinado o un grupo de precios de cliente. Si no desea aplicar el mismo porcentaje de prepago a todos los clientes, debe especificar a qué clientes o a qué grupos de precios de clientes se aplica el porcentaje de prepago.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione un elemento y, a continuación, elija la acción **Conf. ventas y cobros**.  
3. En la página **Porcentajes prepago ventas**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Puede definir un porcentaje de prepago predeterminado para un cliente o proveedor en relación con todos los productos y todos los tipos de líneas de venta. Introduzca el porcentaje en la tarjeta del cliente o del proveedor. El siguiente procedimiento muestra cómo especificar un porcentaje de pago anticipado para un cliente, pero se aplican pasos similares a los proveedores.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abrir la ficha para un cliente.
3. Rellene el campo **% prepago**.
4. Repita los pasos para otros clientes o proveedores.  

> [!TIP]
> También puede acceder a la página **Porcentajes prepago ventas** desde la tarjeta de cliente o proveedor.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Para determinar qué porcentaje de prepago tiene prioridad

Un pedido podría tener un porcentaje de prepago en la cabecera de venta y otro porcentaje distinto para los productos en las líneas. Para determinar qué porcentaje de prepago se aplica a cada línea de venta, [!INCLUDE [prod_short](includes/prod_short.md)] busca y aplica el primer porcentaje predeterminado en el siguiente orden:  

1. Un porcentaje de prepago para el producto en la línea y el cliente al que se dirige el pedido.  
2. Un porcentaje de prepago para el producto en la línea y el grupo de precios al que pertenece el cliente.  
3. Un porcentaje de prepago para el producto en la línea para todos los clientes.  
4. El porcentaje de prepago en la cabecera de ventas o de compra.  

Dicho de otro modo, el porcentaje de prepago de la ficha del cliente solo se aplica si no hay definido un porcentaje de prepago para el producto. Sin embargo, si modifica el contenido del campo **Porcentaje de prepago** en la cabecera de venta o compra después de crear las líneas, se actualiza el porcentaje de prepago en todas las líneas. La actualización facilita la creación de un pedido con un porcentaje de prepago fijo, independientemente del porcentaje definido para los productos.

## <a name="to-automatically-release-sales-orders-when-prepayments-are-applied"></a>Para liberar automáticamente pedidos de venta cuando se aplican prepagos

Puede ahorrar tiempo configurando una entrada en la cola de trabajos que liberará automáticamente pedidos de venta que requieren prepago después de que la liquidación de pagos. Automatizar el proceso le ahorra el paso de lanzar el pedido de venta.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En el campo **Frecuencia de actualización automática prepago**, especifique con qué frecuencia desea que se ejecute la entrada de la cola de trabajos.

> [!TIP]
> Mientras esté aquí, considere agregar una protección contra el envío o la facturación de pedidos de venta que tengan importes de prepago sin abonar. Si activa el botón de alternancia **Comprobar prepago al registrar**, [!INCLUDE[prod_short](includes/prod_short.md)] evitará que las personas publiquen pedidos con importes de prepago sin abonar.

3. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de cola de proyectos** y luego elija el enlace relacionado.
4. Configure la entrada de la cola de trabajos **Actualización pendiente prepago ventas**, por ejemplo, utilizando la configuración en la ficha desplegable **Periodicidad** para programar la frecuencia con la que desea que se ejecute. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Consulte también .

[Facturar prepagos](finance-invoice-prepayments.md)  
[Tutorial: configuración y facturación de prepagos de ventas](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Calcular el impuesto sobre bienes y servicios sobre los prepagos en Australia](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Calcular el impuesto sobre bienes y servicios sobre los prepagos en Nueva Zelanda](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Descripción de contabilidad y plan de cuentas](finance-general-ledger.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
