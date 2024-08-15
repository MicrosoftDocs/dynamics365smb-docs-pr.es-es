---
title: Conciliar los recibos o reembolsos de pagos de proveedores en el diario de pagos
description: 'Para procesar, hacer coincidir o conciliar pagos o reembolsos de proveedor manualmente, liquide el importe con uno o varios movimientos de proveedores abiertos.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment application, payment processing, match payments'
ms.search.form: '62, 233, 522, 623'
ms.date: 07/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Conciliar los pagos a proveedores con el diario de pagos o desde las entradas del libro mayor de proveedores
Cuando envía un pago o recibe un reembolso de un proveedor, debe decidir si va a liquidar uno o varios movimientos pendientes con el pago o el reembolso. Puede especificar el importe exacto que desea liquidar con el albarán de pago o el reembolso, y liquidar sólo parcialmente movimientos del proveedor. Debe liquidar todos los movimientos de proveedores para obtener estadísticas e informes correctos de los extractos de cuentas y los intereses.

> [!NOTE]  
>   A veces los proveedores pueden ofrecer reembolsos en lugar de abonos para compensar futuras facturas, especialmente en los casos en que devuelven productos por los que ya ha pagado o si ha pagado de más en una factura.

Puede liquidar los movimientos de proveedor de tres formas distintas:

* Ingresando información en páginas dedicadas, como la página  **Diarios de pagos**  y la página  **Diarios de conciliación de pagos** .
* Desde documentos de abono de compras.
* Desde movimientos de proveedor después de que se registren los documentos de compras, pero no se liquiden.

> [!NOTE]  
>   Si el campo **Método liquidación** de la ficha del proveedor contiene **Liq. por antigüedad**, los pagos se liquidarán manualmente en el movimiento más antiguo si no especifica manualmente qué movimiento quiere liquidar. Si el método de liquidación para un cliente es **Manual**, entonces deberá liquidar los movimientos manualmente.

Puede aplicar pagos a proveedores manualmente a sus documentos de compra relacionados cuando registra los pagos en la página  **Diarios de pagos** . Para obtener más información acerca de cómo rellenar el diario de pagos, consulte [Efectuar pagos](payables-make-payments.md).

También puede liquidar los pagos a proveedores y los pagos a clientes, después los pagos aparecen como transacciones negativas en su banco. En la página  **Diarios de conciliación de pagos**, puede utilizar funciones para la importación de extractos bancarios, la aplicación automática y la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

## Para liquidar uno o varios movimientos del proveedor con un pago:
1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. En la página  **Diarios de pago**, en la primera línea del diario, ingrese la información relevante sobre la entrada de pago.
3. Para liquidar un solo movimiento de proveedor:
   1. En el campo **Liq. por n.º documento**, elija el campo para abrir la página **Aplicar movs. proveedor**.
   2. En la página **Movs. pendientes proveedor**, seleccione el movimiento al que quiere liquidar el pago.
   3. En la línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar el movimiento.
4. O para liquidar múltiples movimientos de proveedor:

   1. Seleccione la acción **Liquidar movs.**.
   2. En la página **Movs. pendientes proveedor**, seleccione las líneas con los movimientos para liquidar con el pago.
   3. Seleccione la acción **Marcar id. de liquidación**.  
   4. En cada línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar cada movimiento.

      Si no ingresa un monto, se aplicará automáticamente el monto máximo. Al final de la página **Movs. pendientes proveedor**, podrá ver el importe específico incluido en el campo Importe liquidado y también si la liquidación está cuadrada.
5. Elija el botón **Aceptar**.
6. Seleccione la acción **Registrar**, para registrar el diario de pagos.

## Para liquidar un abono con uno o varios movimientos de proveedor
1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos de compra** y, a continuación, elija el enlace relacionado.
2. Abra el abono que desea liquidar.
3. Escriba la información relevante en la cabecera.
4. Para liquidar un solo movimiento de proveedor, en la ficha desplegable **Liquidación**, campo **Liq. por n.º documento**, seleccione el movimiento para liquidar el abono y, a continuación, en el campo **Importe a liquidar**, introduzca el importe para liquidar el movimiento.
5. O para liquidar múltiples movimientos de proveedor:

   1. Seleccione la acción **Liquidar movs.**.
   2. Seleccione las líneas que contienen los movimientos para liquidar el abono.
   3. Seleccione la acción **Marcar id. de liquidación**.  
   4. En cada línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar cada movimiento.

       Si no ingresa un monto, se aplicará automáticamente el monto máximo. Al final de la página **Movs. pendientes proveedor**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.
6. Elija el botón **Aceptar**.  
   La página  **Notas de crédito de compra** muestra la entrada que ha seleccionado en el campo  **Se aplica a tipo de documento**  y en el campo  **Se aplica a número de documento** . La página también muestra el importe del abono para registrar, ajustado con los descuentos por pronto pago.
7. Seleccione el botón **Registrar** para crear el abono de compra.

## Para liquidar movimientos de proveedor registrados
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra el proveedor pertinente con movimientos ya registrados.
3. Seleccione la acción **Movimientos** y, a continuación, seleccione la acción **Liquidar movs**.
4. En la página **Movs. pendientes proveedor** podrá ver los movimientos pendientes del proveedor.
5. Seleccione la línea con el movimiento que se liquidará.
6. Seleccione la acción **Marcar id. de liquidación**.

    El campo **Liq. por id.** muestra tres asteriscos si trabaja con un sistema de usuario único o su identificador de usuario si trabaja con un sistema multiusuario.  
7. Para cada línea del campo **Importe a liquidar** introduzca el importe para liquidar cada movimiento.

    Si no ingresa un monto, se aplicará automáticamente el monto máximo. Puede ver el importe en el campo **Importe liquidado** en la parte inferior de la página **Liquidar movs. proveedor**.
8. Seleccione la acción **Registrar liquidación marcada**.  

    La página **Registrar liquidación** se abre con el número de documento del movimiento de liquidación y la fecha de registro del movimiento con la fecha más reciente.
9. Para registrar la liquidación, elija el botón **Aceptar**.

## Para liquidar movimientos de proveedor entre divisas distintas
Si se realiza una venta a un proveedor en una divisa y se efectúa el pago en otra divisa, todavía se puede solicitar la factura para el pago.

Si con un movimiento (Movimiento 1) en una divisa liquida otro movimiento (Movimiento 2) en otra divisa, se usa la fecha de registro del Movimiento 1 para buscar el tipo de cambio adecuado para convertir los importes del Movimiento 2. El tipo de cambio relevante se encuentra en la página **Tipos cambio divisa**. En ese caso, debe habilitar la liquidación de movimientos de proveedor en divisas distintas. Para obtener más información, vea [Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Abra el diario que desea y rellene la primera línea de diario vacía utilizando un código de divisa.
3. Seleccione la acción **Liquidar movs.**.
4. Seleccione la línea que contiene el movimiento con el que desea liquidar el movimiento del diario de pagos, seleccione la acción **Marcar id. de liquidación** y, a continuación, seleccione el movimiento que desea liquidar.
5. Elija el botón **Aceptar** para volver al diario de pagos.
6. Registre el diario de pagos.

> [!IMPORTANT]  
>   Si liquida movimientos en distintas divisas, los movimientos se convierten a divisa local. Aunque los tipos de cambio de las dos divisas son fijos, como entre USD y EUR, es posible que exista un pequeño importe residual al convertir los importes de divisa extranjera a USD. Estos importes residuales mínimos se registran como ganancias y pérdidas en la cuenta especificada en el campo **Cta. dif. pos. realizadas** o **Cta. dif. neg. realizadas** de la página **Divisas**. El campo **Importe (USD)** también se ajusta para los movimientos de proveedor correspondientes.

## Para deshacer un movimiento de liquidación de movimientos de proveedor
Cuando se anula la aplicación de una aplicación errónea, se crean entradas correctoras que son idénticas a la entrada original pero con el logaritmo opuesto en el campo de importe y se registran para todas las entradas, incluidas todas las contabilizaciones en el libro mayor derivadas de la aplicación, como descuentos de pago y ganancias/pérdidas cambiarias. Los movimientos que se cerraron con la liquidación se volverán a abrir.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de proveedor correspondiente.
3. Seleccione la acción **Movimientos**.
4. Seleccione el movimiento relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
5. De forma alternativa, seleccione la acción **Movimiento detallado**.
6. Seleccione el movimiento de liquidación relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
7. Rellene los campos de la cabecera y, a continuación, seleccione la acción **Desliquidar**.

> [!IMPORTANT]  
>   Si se ha liquidado un movimiento con más de un movimiento de liquidación, primero deberá deshacer la liquidación más reciente.

## Consulte también
[Pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]