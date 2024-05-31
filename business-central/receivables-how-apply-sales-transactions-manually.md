---
title: Conciliar los pagos de los clientes con el diario de recibos de efectivo o con los asientos del libro mayor de los clientes.
description: Aplique recibos de efectivo o reembolsos de clientes a uno o más asientos abiertos del libro mayor de clientes.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Concilie los pagos de los clientes con un diario de recibos de efectivo o con asientos del libro mayor de clientes

Cuando recibe un pago en efectivo de un cliente o realiza un reembolso en efectivo, puede aplicar el pago o reembolso para cerrar débitos o créditos abiertos. Puede especificar el importe a liquidar. Por ejemplo, puede liquidar pagos parciales en movimientos de cliente. El cierre de movimientos de cliente conserva las estadísticas de cliente, los extractos de cuenta, los intereses, etc. al día.

> [!TIP]  
> En la página **Movs. clientes**, la fuente de color rojo significa que el pago relacionado ha superado su fecha de vencimiento. Si los pagos vencidos se están convirtiendo en un problema, podemos ayudarle a reducir su frecuencia. Puede habilitar la extensión de **Predicciones de pago atrasado**, que usa un modelo predictivo que creamos en Azure Machine Learning para predecir el momento en que se realizan los pagos. Estas predicciones le ayudan a reducir los cobros pendientes y afinar la estrategia de sus colecciones. Por ejemplo, si se predice que un pago se retrasará, puede ajustar los términos de pago o el método de pago para el cliente. Para obtener más información, consulte [Predicciones de pago atrasado](ui-extensions-late-payment-prediction.md).  

Puede liquidar movimientos de cliente de varias formas:

* Ingrese información en las siguientes páginas:
   * La página **Diario de conciliación de pagos**. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).
   * La página **Registro de pago**. Para obtener más información, consulte [Conciliar pagos de cliente desde una lista de documentos de ventas sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
   * La página **Diario de recibos de efectivo** . Para obtener más información, consulte [Para completar y publicar un diario de recibos de efectivo](#to-fill-and-post-a-cash-receipt-journal).
* Rellenando el campo **Liq. por nº documento** en documentos de abono de venta. Para obtener más información, consulte [Para aplicar una nota de crédito a un solo movimiento contable de cliente](#to-apply-a-credit-memo-to-a-single-customer-ledger-entry).
* Mediante la acción **Marcar id. de liquidación** en un movimiento de cliente. Para obtener más información, consulte [Para aplicar un pago a un único movimiento contable de cliente](#to-apply-a-payment-to-a-single-customer-ledger-entry).
* Al usar la acción **Aplicar entradas** en la página **Deposito bancario** y luego ingresando el número de factura en el campo **Se aplica a la identificación**. Para obtener más información, consulte [Crear depositarios bancarios](bank-create-bank-deposits.md).

> [!NOTE]  
> Si el campo **Método liquidación** de la ficha del cliente contiene **Liq. por antigüedad**, los pagos se liquidan en el movimiento de crédito pendiente más antiguo, a menos que especifique manualmente un movimiento. Si el método de liquidación es **Manual**, siempre debe liquidar los movimientos manualmente.

## Para rellenar y registrar un diario de recibos de efectivo

Un diario de recibos de caja es un tipo de diario general. Puede usarlo para registrar transacciones en cuentas de contabilidad, bancos, clientes, proveedores y activos fijos. Puede liquidar el pago a una o más entradas del debe cuando registra el pago. También puede aplicar desde las entradas publicadas más tarde.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de recibos de efectivo**, y luego elija el enlace relacionado.
2. Seleccione la acción **Editar diario**.
3. Seleccione la sección de diario que le interese en el campo **Nombre sección**.
4. Rellene el campo **Fecha registro**.  
5. En el campo **Tipo documento**, seleccione **Pago**.

    El campo **Nº documento** se rellena con los números de serie asignados a la sección.  
6. Utilice el campo **Nº documento externo** para almacenar un identificador como el número de comprobación del cliente.

   > [!NOTE]
   > De forma predeterminada, el campo Número de documento externo está oculto. Si es así y desea utilizarlo, puede utilizar la personalización para agregarlo. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

7. En el campo **Tipo mov.**, seleccione **Cliente**.
8. En el campo **Número de cuenta**, seleccione el cliente.
9. Para publicar la solicitud al mismo tiempo que publica la revista, complete los siguientes campos:
   1. En el campo **Tipo contrapartida**, seleccione **Cuenta** para los pagos en efectivo y **Banco** para otros pagos.
   2. En el campo **Cta. contrapartida**, seleccione la cuenta de efectivo para los pagos en efectivo, o la cuenta del banco correspondiente para otros pagos.
10. Registre el diario.

## Para liquidar un pago a un solo movimiento de cliente

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , ingrese **Diario de recibos de efectivo** y elija el enlace relacionado.
2. Seleccione la acción **Editar diario**.
3. En la primera línea de diario, escriba la información correspondiente sobre el movimiento que se va a liquidar.
4. En el campo **Tipo documento**, introduzca **Pago**.
5. En el campo **Tipo mov.**, introduzca **Cliente**.
6. En el campo **Tipo contrapartida**, introduzca **Banco**.
7. En el campo **Liq. por n.º documento**, elija el campo para abrir la página **Aplicar movs. cliente**.
8. En la página **Movs. pendientes cliente**, seleccione el movimiento al que quiere liquidar el pago.
9. En el campo **Importe a liquidar**, introduzca el importe con el que desea liquidar el movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.

    Al final de la página **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
10. Elija el botón **Aceptar**. La página **Diario de recibos de efectivo** ahora muestra el movimiento en los campos **Liq. por tipo documento** y **Liq. por n.º documento**.
11. Registro el diario de cobros.

## Para liquidar un pago a varios movimientos de cliente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de recibos de efectivo**, y luego elija el enlace relacionado.
2. Seleccione la acción **Editar diario**.
3. En la primera línea de diario, escriba la información correspondiente sobre el movimiento que se va a liquidar.
4. En el campo **Tipo documento**, introduzca **Pago**.
5. En el campo **Tipo mov.**, introduzca **Cliente**.
6. En el campo **Tipo contrapartida**, introduzca **Banco**.
7. En el campo **Importe**, introduzca el pago completo como un importe negativo.
8. Para liquidar los pagos de varios movimientos de cliente cuando registre, seleccione la acción **Liquidar movs.**  
9. Seleccione las líneas que incluyen los movimientos a los que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación**.  
10. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.

    Al final de la página **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
11. Elija el botón **Aceptar**.
12. Registro el diario de cobros.

## Para liquidar un abono a un único movimiento de cliente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra el abono de venta correspondiente.
3. Para liquidar el abono a un solo movimiento de cliente al registrar, en la ficha desplegable **Liq. por n.º documento**, seleccione el movimiento que desea liquidar con el pago.
4. En la línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar el movimiento.  

    Si no especifica ninguna cantidad, la aplicación utilizará automáticamente el importe máximo. Al final de la página **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
5. Elija el botón **Aceptar**. La página **Memoria de crédito de ventas** ahora muestra la entrada que seleccionó en **Se aplica al documento. Escriba** y **Se aplica al doc. Nº** campos. Asimismo, muestra el importe del abono que se va a registrar, ajustado con los posibles descuentos por pronto pago.
6. Registre el abono.

## Para liquidar un abono a varios movimientos de cliente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra el abono de venta correspondiente.
3. Para liquidar el abono en varios movimientos del cliente cuando registre, seleccione la acción **Liquidar movs.**
4. Seleccione las líneas que incluyen los movimientos a los que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación**.
5. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.  

    Al final de la página **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
6. Elija el botón **Aceptar**. La página **Abono de venta** mostrará el importe del abono para registrar, ajustado para los posibles descuentos de pago.
7. Registre el abono.

## Para liquidar movimientos de clientes registrados

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de cliente para el cliente con los movimientos que desea liquidar.
3. Elija la acción **Movimiento de libro mayor** y luego seleccione la línea con el asiento que es el asiento de aplicación.
4. Seleccione la acción **Liquidar movs.**. La página **Liquidar movs. cliente** se abre y muestra los movimientos pendientes del cliente.
5. Seleccione las líneas con los movimientos que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación** .
6. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.  

    En la parte inferior de la página **Liquidar movs. cliente**, puede ver el importe específico en el campo **Importe liquidado**.  
7. Seleccione la acción **Registrar liquidación marcada**. La página **Registrar liquidación** aparece con el número de documento del movimiento de liquidación y la fecha de registro del movimiento con la fecha más reciente.  
8. Para registrar la liquidación, elija el botón **Aceptar**.

    Si la aplicación publicada resultó en asientos contables de clientes cerrados, el campo **Abrir** se borra para estos asientos contables.  
9. Para ver los movimientos de proveedores, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado. Busque la ficha del cliente correspondiente para ver los movimientos.  

En la lista de movimientos, en la línea que contiene el movimiento que se liquidó completamente, puede ver que la casilla **Pendiente** no está marcada.  

> [!NOTE]  
> Después de seleccionar un movimiento en la página **Liquidar movs. cliente** o varios movimientos estableciendo **Liq. por id.**, el campo **Importe liquidado** de la línea de diario contendrá la suma de los importes restantes de los movimientos registrados que haya seleccionado, a menos que el campo ya contenga algún valor. Si selecciona **Liq. por antigüedad** en el campo **Método de liquidación** de la ficha de cliente, la liquidación se realizará automáticamente.

## Para liquidar movimientos de cliente en divisas diferentes

Si vende a un cliente en una divisa y cobra en otra, aún puede liquidar la factura con el pago.  

A continuación, tiene un ejemplo. Usted aplica la Entrada A en una moneda a la Entrada B en otra moneda. La fecha de publicación en la Entrada A se utiliza para encontrar el tipo de cambio que se utilizará para convertir montos en la Entrada B. El tipo de cambio se encuentra en la página  **Tipos de cambio de moneda** .  

Se debe habilitar la liquidación de movimientos de cliente en divisas diferentes. Para obtener más información, vea [Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de recibos de efectivo**, y luego elija el enlace relacionado.
2. Abra el diario que desea y rellene la primera línea de diario vacía utilizando un código de divisa.
3. Seleccione la acción **Liquidar movs.**.
4. Seleccione la línea que contiene el movimiento con el que desea liquidar el movimiento del diario de recibos de efectivo, seleccione la acción **Marcar id. de liquidación** y, a continuación, seleccione el movimiento que desea liquidar.
5. Seleccione el botón **Aceptar** para volver al diario de recibos de efectivo.
6. Registre el diario de ventas.  

> [!IMPORTANT]  
>   Si liquida movimientos en distintas divisas, los movimientos se convierten a divisa local. Aunque los tipos de cambio de las dos divisas son fijos, como entre USD y EUR, es posible que exista un pequeño importe residual al convertir los importes a USD. Estos importes residuales mínimos se registran como ganancias y pérdidas en la cuenta especificada en los campos **Cta. dif. pos. realizadas** o **Cta. dif. neg. realizadas** de la página **Divisas**. El campo **Importe (USD)** también se ajusta para los movimientos de proveedor.  

## Para corregir una liquidación de movimientos de clientes
Cuando corrige una aplicación, se crean y registran entradas de corrección para todas las entradas. Las entradas de corrección son las mismas que las originales pero tienen un registro opuesto en el campo **Cantidad**. Las entradas de corrección incluyen todas las entradas del libro mayor derivadas de la aplicación. Por ejemplo, el descuento de pago y las ganancias/pérdidas de divisas. Se vuelven a abrir las entradas que cerró la aplicación.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abrir la ficha de cliente correspondiente.
3. Seleccione la acción **Movimientos**.
4. Seleccione el movimiento relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
5. De forma alternativa, seleccione la acción **Movimiento detallado**.
6. Seleccione el movimiento de liquidación relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
7. Rellene los campos de la cabecera y, a continuación, seleccione la acción **Desliquidar**.  

> [!IMPORTANT]  
>   Si se ha liquidado un movimiento con más de un movimiento de liquidación, primero deberá deshacer la liquidación más reciente.  

## Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]