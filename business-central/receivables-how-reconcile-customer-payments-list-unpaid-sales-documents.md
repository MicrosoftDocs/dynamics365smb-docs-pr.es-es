---
title: Liquidar pagos para los documentos de venta no pagados
description: 'Los importes pagados por clientes se liquidan en los documentos de venta relacionados y se registra el pago para actualizar los movimientos de cliente, contabilidad y banco.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Conciliar los pagos de clientes desde una lista de documentos de venta impagados

Después de que los clientes realicen pagos electrónicos a su cuenta bancaria, debe realizar las siguientes acciones:

* Aplicar cada importe pagado al documento de venta relacionado.
* Registrar el pago para actualizar los movimientos de cliente, cuenta contable y cuenta bancaria.

En función de sus necesidades comerciales, puede registrar pagos de forma manual, automática y mediante servicios de pago.  

> [!NOTE]  
> Puede realizar las mismas tareas, incluidos los pagos a proveedores, en la página **Diario de conciliación de pagos**. Por ejemplo, puede importar extractos bancarios, utilizar aplicaciones automáticas y conciliar cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Utilice la página **Registrar pagos de cliente** para equilibrar las cuentas internas utilizando las cifras reales de efectivo para garantizar el cobro de los pagos. Puede verificar y registrar rápidamente pagos individuales o de suma global, procesar pagos con descuento y encontrar los documentos no pagados.

Debe registrar pagos para los diferentes clientes que tienen distintas fechas de pago como pagos individuales. Los pagos para el mismo cliente con la misma fecha de pago se pueden registrar como pago de suma total. Los pagos de suma global pueden ser útiles, por ejemplo, cuando un cliente ha realizado un pago único que cubre varias facturas de venta.

## <a name="to-set-up-the-payment-registration-journal"></a>Configurar el diario de registros de pago

Dado que puede registrar distintos tipos de pago en diferentes cuentas de saldo, debe seleccionar una cuenta de saldo en la página **Configuración de registro de pago** antes de empezar a procesar los pagos de cliente. Si siempre registra en la misma cuenta de saldo, puede definir esa cuenta como la predeterminada y evitar este paso cada vez que abra la página **Registrar pagos de cliente**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración del registro de pago** y luego elija el enlace relacionado. Alternativamente, puede elegir la acción **Configurar** en la página **Registrar pagos de cliente**.
2. Rellene los campos de la página **Configuración del registro de pago**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Para facilitar la identificación posterior de los movimientos que se registraron a través del diario, puede asignar una serie numérica específica al diario de pagos. La serie de números es útil si utiliza diarios de conciliación de pagos para registrar y liquidar pagos.

## <a name="to-register-customer-payments-individually"></a>Para registrar los pagos del cliente por separado

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  

    La página **Registrar pagos de cliente** muestra todos los documentos registrados para los que puede registrarse un pago. También puede abrir la página desde las páginas **Clientes** y **Ficha de cliente**, filtrada automáticamente para el cliente especificado.  
2. Seleccione la casilla **Pago realizado** en la línea que representa el documento registrado para el que se ha realizado un pago.
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  

   Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, el campo **Fecha de recepción** contiene la fecha de trabajo.  
4. En el campo **Importe recibido**, especifique el importe que se ha pagado.

    Para los pagos completos, este importe es el mismo que el importe en el campo **Importe pendiente** en la línea. Para los pagos parciales, este importe es inferior al importe del campo **Importe pendiente** en la línea.
5. Repita los pasos 2 a 4 para las demás líneas para documentos registrados para los que se realicen pagos.  
6. Seleccione la acción **Registrar pagos**.  

La información de pagos se registra para los documentos en las líneas donde la casilla de verificación **Pago realizado** está seleccionada. Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente.

## <a name="to-reconcile-lump-sum-payments"></a>Conciliar los pagos de suma totales

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.
2. Seleccione la casilla de verificación **Pago realizado** en las líneas para documentos registrados para el mismo cliente para el que se ha realizado un pago de suma total.  

    > [!NOTE]  
    > El cliente en el campo **Nombre** debe ser igual en todas las líneas que se incluirán en el pago de suma total.  

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, el campo **Fecha de recepción** contiene la fecha de trabajo.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  

    > [!NOTE]  
    > Esta fecha debe ser igual en todas las líneas que se registrarán como pago de suma total.  
4. En el campo **Importe recibido**, especifique los importes en varias líneas que suman el importe del pago total.  

    > [!TIP]  
    > Intente registrar el mayor número posible de pagos completos con el importe de suma total. Introduzca los importes cuya cantidad coincida con el importe en el campo **Importe pendiente** en tantas líneas como sea posible.  
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para el mismo cliente para los que se ha realizado un pago de suma total.  
6. Seleccione la acción **Registrar como pago total**.

   La información de pagos se registra para los documentos en las líneas donde la casilla de verificación **Pago realizado** está seleccionada. Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

Si un pago en el banco no se representa mediante una línea en la página **Registrar pagos de cliente**, puede ser porque el documento relacionado aún no se ha registrado. En ese caso, puede usar una función de búsqueda para buscar rápidamente el documento y registrarlo para procesar el pago. Para obtener más información, consulte [Buscar un documento determinado de ventas que no esté totalmente facturado](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Si un pago en el banco no se representa mediante ningún documento en , puede abrir un diario general previamente rellenado en la página **Registrar pagos de cliente** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto. Para obtener más información, consulte [Registrar pagos sin documento relacionado](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Para procesar pagos de cliente con descuentos manualmente

Si ha acordado un descuento por pronto pago con el cliente, los importes de pago pueden ser inferiores a los importes de factura si el pago se produce antes de la fecha de descuento acordada.  

En los procedimientos siguientes se explican formas para registrar pagos al descuento en la página **Registro de pago**.  

* El importe de pago es igual al importe al descuento restante, y la fecha de pago es antes de la fecha de descuento. Registra el pago tal como está.  
* El importe de pago es igual al importe al descuento restante, pero la fecha de pago es posterior a la fecha de descuento. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente. También puede definir la fecha de descuento posteriormente para permitir el pago total.  
* El importe del pago es menor que el importe al descuento restante. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente.  
* El importe del pago es mayor que el importe al descuento restante. Registra los pagos tal como están. Solo se registra el importe pendiente. El importe adicional se abona al cliente.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Importar un importe de pago igual al descuento y donde la fecha de pago es antes de la fecha de descuento

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe pend. incl. descuento**.

    La casilla de verificación **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Importar un importe de pago igual al descuento ero donde la fecha de pago es posterior a la fecha de descuento

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe pend. incl. descuento**.

    La casilla de verificación **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. En el campo **Fecha de recepción**, especifique una fecha de pago que sea posterior a la fecha del campo **Fecha de descuento del pago**.

   Los campos de fecha cambian a la fuente color rojo, y un mensaje de error se muestra en la parte inferior de la página. Los siguientes dos pasos solucionan eso.
4. Seleccione la acción **Detalles**.  
5. En la página **Detalles del registro de pago**, en el campo **Fecha de descuento del pago**, en la ficha desplegable **Descuento del pago**, especifique una fecha que sea posterior a la fecha del campo **Fecha de recepción**, en la página **Registro de pago**.  

    El mensaje de error y la fuente de color rojo desaparecen, y puede seguir procesando el pago descontado.
6. Compruebe que el campo **Importe pendiente** contenga el importe pendiente para pagar el importe total de la factura.  
7. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Procesar un pago que es menor que el importe al descuento restante

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es inferior al importe del campo **Importe pend. incl. descuento**.

    La casilla de verificación **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.  
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contiene el importe pendiente para pagar el importe al descuento.  
5. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Procesar un pago que es mayor que el importe al descuento restante

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es superior al importe del campo **Importe pend. incl. descuento**.  

    La casilla de verificación **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado está cerrado y al cliente se acredita el importe de pago en exceso.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Buscar un documento de ventas específico que no está facturado totalmente

La página **Registrar pagos de cliente** le facilita las tareas necesarias para calcular el saldo de las cuentas internas con cifras reales de efectivo para garantizar la colección efectiva de los clientes y el pago debido a los proveedores. Muestra los pagos entrantes pendientes como líneas que representen los documentos de venta donde se debe un importe para el pago.  

Normalmente, cuando se realiza un pago, se registra en el banco o de otro modo, el documento de compra o venta se representa como una línea en la página **Registrar pagos de clientes**. El documento está esperando que usted registre el pago del importe pendiente. Sin embargo, a veces un pago que se ha realizado no se representa mediante una línea en la página **Registrar pagos de cliente**, normalmente porque en el documento no está totalmente facturado.

Utilice la acción **Buscar documentos** para buscar entre los documentos que no se han facturado por completo. Puede buscar basado en uno o varios de los siguientes criterios:  

* N.º documento  
* Importe o rango de importes  

En el procedimiento siguiente se explica cómo buscar un documento determinado mediante ambos criterios de búsqueda.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.
2. Con el puntero en cualquier línea, seleccione la acción **Buscar documentos**.
3. En la página **Búsqueda de documentos**, especifique un valor de búsqueda en el campo **Número de documento**.  

    > [!NOTE]  
    > El valor que especifique en este campo se encierra entre los caracteres comodín ocultos. Esto significa que la acción busca todos los números de documento que contengan el valor especificado.
4. En el campo **Importe**, especifique el importe concreto en el documento que desee buscar.  
5. En el campo **% tolerancia de importe**, especifique un valor de porcentaje para definir el rango de importes que desea buscar para encontrar el documento abierto.  

    Si introduzca 10, la acción busca importes en un importe de más o menos el 10 por ciento del valor en el campo **Cantidad**.
6. Seleccione la acción **Buscar**.  

Si hay documentos que coinciden con los criterios de búsqueda, la página **Resultado de la búsqueda de documentos** se abrirá en las líneas de presentación que representan dichos documentos. Cada línea contiene un número de documento, una descripción y un importe.

Si un pago en el banco no se representa mediante ningún documento, puede abrir un diario general previamente rellenado en la página **Registrar pagos de cliente** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Registrar pagos sin documento relacionado

Si un pago en el banco no está representado por un documento, puede utilizar la acción **Diario general** para abrir una línea de diario general precargada desde la página **Registrar pagos de clientes**. Utilice el diario para registrar el pago directamente en la cuenta de contrapartida sin aplicar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.
2. Seleccione la acción **Diario general**.  

    La página **Diario general** se abre con una línea que contiene la cuenta de saldo de la sección de diario configurada en la página **Configuración de registro de pago**.  
3. Rellene el resto de los campos de cada línea del diario general. Por ejemplo, proporcione el importe, el número de cliente o la información del extracto bancario. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Puede registrar la línea del diario para actualizar el total de la cuenta de contrapartida. También puede dejar la línea del diario sin registrar, y quizás agregarla con una nota conforme el pago necesita más análisis.  

Si no publica la línea del diario, su valor se agrega al valor en el campo **Importe pend. incl. descuento** campo en la página **Registro de pago**.  

## <a name="see-also"></a>Consulte también

[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
