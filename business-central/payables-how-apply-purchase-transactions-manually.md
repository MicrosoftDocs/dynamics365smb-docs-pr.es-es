---
title: Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor | Documentos de Microsoft
description: Para procesar, hacer coincidir o conciliar pagos o reembolsos de proveedor manualmente, liquide el importe con uno o varios movimientos de proveedores abiertos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b981a0062c628f3ffe3b0de8eaf4c811a13632ec
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916831"
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor
Cuando envía un pago o recibe un reembolso de un proveedor, debe decidir si va a liquidar uno o varios movimientos pendientes con el pago o el reembolso. Puede especificar el importe exacto que desea liquidar con el albarán de pago o el reembolso, y liquidar sólo parcialmente movimientos del proveedor. Debe liquidar todos los movimientos de proveedores para obtener estadísticas e informes correctos de los extractos de cuentas y los intereses.

> [!NOTE]  
>   A veces los proveedores pueden ofrecer reembolsos en lugar de abonos para compensar futuras facturas, especialmente en los casos en que devuelven productos por los que ya ha pagado o si ha pagado de más en una factura.

Puede liquidar los movimientos de proveedor de tres formas distintas:

* Introduciendo información en páginas específicas, como **Diario de pagos** y **Diario de conciliación de pagos**.
* Desde documentos de abono de compras.
* Desde movimientos de proveedor después de que se registren los documentos de compras, pero no se liquiden.

> [!NOTE]  
>   Si el campo **Método liquidación** de la ficha del proveedor contiene **Liq. por antigüedad**, los pagos se liquidarán manualmente en el movimiento más antiguo si no especifica manualmente qué movimiento quiere liquidar. Si el método de liquidación para un cliente es **Manual**, entonces deberá liquidar los movimientos manualmente.

Puede liquidar pagos a proveedores manualmente a los documentos de compra relacionados cuando registre pagos en la página **Diario de pagos**. Para obtener más información acerca de cómo rellenar el diario de pagos, consulte [Efectuar pagos](payables-make-payments.md).

También puede liquidar los pagos a proveedores y los pagos a clientes, después los pagos aparecen como transacciones negativas en su banco. En la página **Diario de conciliación de pagos**, puede usar las funciones para importar extractos bancarios, para la liquidación automática y para la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Para liquidar uno o varios movimientos del proveedor con un pago:
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. En la página **Diario de pagos**, en la primera línea del diario, escriba la información correspondiente sobre el movimiento de pago.
3. Para liquidar un solo movimiento de proveedor:
   1. En el campo **Liq. por n.º documento**, elija el campo para abrir la página **Aplicar movs. proveedor**.
   2. En la página **Movs. pendientes proveedor**, seleccione el movimiento al que quiere liquidar el pago.
   3. En la línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar el movimiento.
4. O para liquidar múltiples movimientos de proveedor:

   1. Seleccione la acción **Liquidar movs.**.
   2. En la página **Movs. pendientes proveedor**, seleccione las líneas con los movimientos para liquidar con el pago.
   3. Seleccione la acción **Marcar id. de liquidación**.  
   4. En cada línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar cada movimiento.

      Si no especifica ninguna cantidad, se utiliza automáticamente el importe máximo. Al final de la página **Movs. pendientes proveedor**, podrá ver el importe específico incluido en el campo Importe liquidado y también si la liquidación está cuadrada.
5. Elija el botón **Aceptar**.
6. Seleccione la acción **Registrar**, para registrar el diario de pagos.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Para liquidar un abono con uno o varios movimientos de proveedor
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Abono de compra** y luego elija el enlace relacionado.
2. Abra el abono que desea liquidar.
3. Escriba la información relevante en la cabecera.
4. Para liquidar un solo movimiento de proveedor, en la ficha desplegable **Liquidación**, campo **Liq. por n.º documento**, seleccione el movimiento para liquidar el abono y, a continuación, en el campo **Importe a liquidar**, introduzca el importe para liquidar el movimiento.
5. O para liquidar múltiples movimientos de proveedor:

   1. Seleccione la acción **Liquidar movs.**.
   2. Seleccione las líneas que contienen los movimientos para liquidar el abono.
   3. Seleccione la acción **Marcar id. de liquidación**.  
   4. En cada línea del campo **Importe pendiente de liquidar**, introduzca el importe para liquidar cada movimiento.

       Si no especifica ninguna cantidad, se utiliza automáticamente el importe máximo. Al final de la página **Movs. pendientes proveedor**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.
6. Elija el botón **Aceptar**.  
   La página **Abono compra** muestra el movimiento que ha introducido en los campos **Liq. por tipo documento** y **Liq. por n.º documento**. La página también muestra el importe del abono para registrar, ajustado con los descuentos por pronto pago.
7. Seleccione el botón **Registrar** para crear el abono de compra.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Para liquidar movimientos de proveedor registrados
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra el proveedor pertinente con movimientos ya registrados.
3. Seleccione la acción **Movimientos** y, a continuación, seleccione la acción **Liquidar movs**.
4. En la página **Movs. pendientes proveedor** podrá ver los movimientos pendientes del proveedor.
5. Seleccione la línea con el movimiento que se liquidará.
6. Seleccione la acción **Marcar id. de liquidación**.

    El campo **Liq. por id.** muestra tres asteriscos si trabaja con un sistema de usuario único o su identificador de usuario si trabaja con un sistema multiusuario.  
7. Para cada línea del campo **Importe a liquidar** introduzca el importe para liquidar cada movimiento.

    Si no especifica ninguna cantidad, se utiliza automáticamente el importe máximo. Puede ver el importe en el campo **Importe liquidado** en la parte inferior de la página **Liquidar movs. proveedor**.
8. Seleccione la acción **Registrar liquidación marcada**.  

    La página **Registrar liquidación** se abre con el número de documento del movimiento de liquidación y la fecha de registro del movimiento con la fecha más reciente.
9. Para registrar la liquidación, elija el botón **Aceptar**.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Para liquidar movimientos de proveedor entre divisas distintas
Si se realiza una venta a un proveedor en una divisa y se efectúa el pago en otra divisa, todavía se puede solicitar la factura para el pago.

Si con un movimiento (Movimiento 1) en una divisa liquida otro movimiento (Movimiento 2) en otra divisa, se usa la fecha de registro del Movimiento 1 para buscar el tipo de cambio adecuado para convertir los importes del Movimiento 2. El tipo de cambio relevante se encuentra en la página **Tipos cambio divisa**. En ese caso, debe habilitar la liquidación de movimientos de proveedor en divisas distintas. Para obtener más información, vea [Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Abra el diario que desea y rellene la primera línea de diario vacía utilizando un código de divisa.
3. Seleccione la acción **Liquidar movs.**.
4. Seleccione la línea que contiene el movimiento con el que desea liquidar el movimiento del diario de pagos, seleccione la acción **Marcar id. de liquidación** y, a continuación, seleccione el movimiento que desea liquidar.
5. Elija el botón **Aceptar** para volver al diario de pagos.
6. Registre el diario de pagos.

> [!IMPORTANT]  
>   Si liquida movimientos en distintas divisas, los movimientos se convierten a divisa local. Aunque los tipos de cambio de las dos divisas son fijos, como entre USD y EUR, es posible que exista un pequeño importe residual al convertir los importes de divisa extranjera a USD. Estos importes residuales mínimos se registran como ganancias y pérdidas en la cuenta especificada en el campo **Cta. dif. pos. realizadas** o **Cta. dif. neg. realizadas** de la página **Divisas**. El campo **Importe (USD)** también se ajusta para los movimientos de proveedor correspondientes.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Para deshacer un movimiento de liquidación de movimientos de proveedor
Cuando se deshace una liquidación errónea, se crean y registran movimientos de corrección que son idénticos al original, pero de signo opuesto en el campo de importe, para todos los movimientos, incluidos todos los registros de contabilidad derivados de la liquidación, como los descuentos por pronto pago y las pérdidas y ganancias en divisas. Los movimientos que se cerraron con la liquidación se volverán a abrir.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de proveedor correspondiente.
3. Seleccione la acción **Movimientos**.
4. Seleccione el movimiento relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
5. De forma alternativa, seleccione la acción **Movimiento detallado**.
6. Seleccione el movimiento de liquidación relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
7. Rellene los campos de la cabecera y, a continuación, seleccione la acción **Desliquidar**.

> [!IMPORTANT]  
>   Si se ha liquidado un movimiento con más de un movimiento de liquidación, primero deberá deshacer la liquidación más reciente.

## <a name="see-also"></a>Consulte también
[Pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
