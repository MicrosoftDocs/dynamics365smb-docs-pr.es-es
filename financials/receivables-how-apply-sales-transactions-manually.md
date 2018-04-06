---
title: Liquidar movimientos de cliente en pagos de cliente conciliados manualmente | Documentos de Microsoft
description: "Describe cómo liquidar los recibos de efectivo o los reembolsos a uno o varios movimientos de clientes pendientes y conciliar pagos del cliente."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6e00e9cbc1b1dc8674ccf83876809496a563b0be
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-customer-payments-manually"></a>Conciliar pagos de cliente manualmente
Cuando recibe un cobro de un cliente o efectúa un reembolso, debe decidir si va a liquidar el pago o reembolsarlo para cerrar uno o varios movimientos pendientes del debe o el haber. Puede especificar el importe que desea liquidar. Por ejemplo, puede liquidar pagos parciales en movimientos de cliente. El cierre de movimientos de cliente garantiza que la información, como las estadísticas de cliente, los extractos de cuenta y los intereses, sean correctos.

> [!NOTE]  
>   En la ventana **Movs. clientes**, la fuente de color rojo significa que el pago relacionado ha superado su fecha de vencimiento.

Puede liquidar movimientos de cliente de varias formas:

* Introduciendo información en ventanas específicas, como **Diario de recibos de efectivo** y **Diario de conciliación de pagos**.
* Desde documentos de ventas.
* Desde movimientos de cliente después de que los documentos de ventas se hayan registrado pero no liquidado.

> [!NOTE]  
>   Si el campo **Método liquidación** de la ficha del cliente contiene **Liq. por antigüedad**, los pagos se liquidan en el movimiento de crédito pendiente más antiguo, a menos que especifique manualmente un movimiento. Si el método de liquidación es **Manual**, siempre debe liquidar los movimientos manualmente.

Puede liquidar pagos de cliente manualmente en la ventana **Diario de recibos de efectivo**. Un diario de cobros es un tipo de diario general, por lo que puede usarlo para registrar transacciones en cuentas contables, de banco, de cliente, de proveedor y de activos fijos. Puede liquidar el pago de uno o más movimientos de débito cuando registra el pago o puede liquidarlos desde movimientos registrados posteriormente.

También puede liquidar pagos de cliente y de proveedor en la ventana **Diario de conciliación de pagos** mediante funciones para la importación de extractos bancarios, la liquidación automática y la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md). De forma alternativa, puede conciliar los pagos de clientes basados en una lista de documentos de ventas sin abonar en la ventana **Registro de pagos**. Para obtener más información, consulte [Conciliar pagos de cliente desde una lista de documentos de ventas sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Para rellenar y registrar un diario de recibos de efectivo
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de recibos de efectivo** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Editar diario**.
3. Seleccione la sección de diario que le interese en el campo **Nombre sección**.
4. Rellene el campo **Fecha registro**.  
5. En el campo **Tipo documento**, seleccione **Pago**.

    El campo **Nº documento** se rellena con los números de serie asignados a la sección.  
6. Utilice el campo **Nº documento externo** para almacenar un identificador como el número de comprobación del cliente.
7. En el campo **Tipo mov.**, seleccione **Cliente**.
8. En el campo **Cód. cuenta banco**, seleccione la cuenta de contabilidad que desee.
9. Si desea registrar la aplicación al mismo tiempo que el diario, elija una de estas acciones.
10. En el campo **Tipo contrapartida**, seleccione **Cuenta** para los pagos en efectivo y **Banco** para otros pagos.
11. En el campo **Cta. contrapartida**, seleccione la cuenta de efectivo para los pagos en efectivo, o la cuenta del banco correspondiente para otros pagos.
12. Registre el diario.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Para liquidar un pago a un solo movimiento de cliente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de recibos de efectivo** y seleccione el vínculo relacionado.
2. Seleccione la acción **Editar diario**.
3. En la primera línea de diario, escriba la información correspondiente sobre el movimiento que se va a liquidar.
4. En el campo **Tipo documento**, introduzca **Pago**.
5. En el campo **Tipo mov.**, introduzca **Cliente**.
6. En el campo **Tipo contrapartida**, introduzca **Banco**.
7. En el campo **Liq. por n.º documento**, elija el campo para abrir la ventana **Aplicar movs. cliente**.
8. En la ventana **Movs. pendientes cliente**, seleccione el movimiento al que quiere liquidar el pago.
9. En el campo **Importe a liquidar**, introduzca el importe con el que desea liquidar el movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.

    Al final de la ventana **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
10. Elija el botón **Aceptar**. La ventana **Diario de recibos de efectivo** ahora muestra el movimiento que ha introducido en los campos **Liq. por tipo documento** y **Liq. por n.º documento**.
11. Registro el diario de cobros.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Para liquidar un pago a varios movimientos de cliente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de recibos de efectivo** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Editar diario**.
3. En la primera línea de diario, escriba la información correspondiente sobre el movimiento que se va a liquidar.
4. En el campo **Tipo documento**, introduzca **Pago**.
5. En el campo **Tipo mov.**, introduzca **Cliente**.
6. En el campo **Tipo contrapartida**, introduzca **Banco**.
7. En el campo **Importe**, introduzca el pago completo como un importe negativo.
8. Para liquidar los pagos de varios movimientos de cliente cuando registre, seleccione la acción **Liquidar movs.**  
9. Seleccione las líneas que incluyen los movimientos a los que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación**.  
10. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.

    Al final de la ventana **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
11. Elija el botón **Aceptar**.
12. Registro el diario de cobros.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Para liquidar un abono a un único movimiento de cliente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Abonos de venta** y, a continuación, seleccione el vínculo relacionado.
2. Abra el abono de venta correspondiente.
3. Para liquidar el abono a un solo movimiento de cliente al registrar, en la ficha desplegable **Liq. por n.º documento**, seleccione el movimiento que desea liquidar con el pago.
4. En la línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar el movimiento.  

    Si no especifica ninguna cantidad, el programa utilizará automáticamente el importe máximo. Al final de la ventana **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.    
5. Elija el botón **Aceptar**. La ventana **Abono de venta** ahora muestra el movimiento que ha introducido en los campos **Liq. por tipo documento** y **Liq. por n.º documento**. Asimismo, muestra el importe del abono que se va a registrar, ajustado con los posibles descuentos por pronto pago.
6. Registre el abono.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Para liquidar un abono a varios movimientos de cliente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Abonos de venta** y, a continuación, seleccione el vínculo relacionado.
2. Abra el abono de venta correspondiente.
3. Para liquidar el abono en varios movimientos del cliente cuando registre, seleccione la acción **Liquidar movs.**
4. Seleccione las líneas que incluyen los movimientos a los que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación**.
5. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.  

    Al final de la ventana **Movs. pendientes cliente**, podrá ver el importe específico incluido en el campo **Importe liquidado** y también si la liquidación está cuadrada.  
6. Elija el botón **Aceptar**. La ventana **Abono de venta** mostrará el importe del abono para registrar, ajustado para los posibles descuentos de pago.
7. Registre el abono.

## <a name="to-apply-posted-customer-ledger-entries"></a>Para liquidar movimientos de clientes registrados
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.
2. Abra la ficha de cliente para el cliente con los movimientos que desea liquidar.
3. Elija la acción **Movimientos** y, a continuación, seleccione la línea con el movimiento que se liquidará.
4. Seleccione la acción **Liquidar movs.**. La **Liquidar movs. cliente** se abre y muestra los movimientos pendientes del cliente.
5. Seleccione las líneas con los movimientos que desea aplicar el movimiento de liquidación y, a continuación, seleccione la acción **Marcar id. de liquidación** .
6. En cada línea del campo **Importe a liquidar**, introduzca el importe con el que desea liquidar cada movimiento. Si no especifica ninguna cantidad, se usa el importe máximo.  

    En la parte inferior de la ventana **Liquidar movs. cliente**, puede ver el importe específico en el campo **Importe liquidado**.  
7. Seleccione la acción **Registrar liquidación marcada**. La ventana **Registrar liquidación** aparece con el número de documento del movimiento de liquidación y la fecha de registro del movimiento con la fecha más reciente.  
8. Para registrar la liquidación, elija el botón **Aceptar**.

    Si la liquidación registrada obtiene como resultado movimientos cerrados de cliente, se desactivará el campo **Pendiente** para dichos movimientos.    
9. Para consultar los movimientos, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado. Busque la ficha del cliente correspondiente para ver los movimientos.  

En la lista de movimientos, en la línea que contiene el movimiento que se liquidó completamente, puede ver que la casilla **Pendiente** no está marcada.  

> [!NOTE]  
>   Después de seleccionar un movimiento en la ventana **Liquidar movs. cliente** o varios movimientos estableciendo **Liq. por id.**, el campo **Importe liquidado** de la línea de diario contendrá la suma de los importes restantes de los movimientos registrados que haya seleccionado, a menos que el campo ya contenga algún valor. Si selecciona **Liq. por antigüedad** en el campo **Método de liquidación** de la ficha de cliente, la liquidación se realizará automáticamente.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Para liquidar movimientos de cliente en divisas diferentes
Si vende a un cliente en una divisa y cobra en otra, aún puede liquidar la factura con el pago.  

Si con un movimiento (Movimiento 1) en una divisa liquida otro movimiento (Movimiento 2) en otra divisa, se usa la fecha de registro del Movimiento 1 para buscar el tipo de cambio adecuado para convertir los importes del Movimiento 2. El tipo de cambio relevante se encuentra en la ventana **Tipos cambio divisa**.  

Se debe habilitar la liquidación de movimientos de cliente en divisas diferentes. Para obtener más información, vea [Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de recibos de efectivo** y, a continuación, seleccione el vínculo relacionado.
2. Abra el diario que desea y rellene la primera línea de diario vacía utilizando un código de divisa.
3. Seleccione la acción **Liquidar movs.**.
4. Seleccione la línea que contiene el movimiento con el que desea liquidar el movimiento del diario de recibos de efectivo, seleccione la acción **Marcar id. de liquidación** y, a continuación, seleccione el movimiento que desea liquidar.
5. Seleccione el botón **Aceptar** para volver al diario de recibos de efectivo.
6. Registre el diario de ventas.  

> [!IMPORTANT]  
>   Si liquida movimientos en distintas divisas, los movimientos se convierten a divisa local. Aunque los tipos de cambio de las dos divisas son fijos, como entre USD y EUR, es posible que exista un pequeño importe residual al convertir los importes a USD. Estos importes residuales mínimos se registran como ganancias y pérdidas en la cuenta especificada en los campos **Cta. dif. pos. realizadas** o **Cta. dif. neg. realizadas** de la ventana **Divisas**. El campo **Importe (USD)** también se ajusta para los movimientos de proveedor.  

## <a name="to-correct-an-application-of-customer-entries"></a>Para corregir una liquidación de movimientos de clientes
Cuando se corrige una liquidación errónea, se crean y registran movimientos de corrección que son idénticos al original, pero de signo opuesto en el campo de importe, para todos los movimientos, incluidos todos los registros de contabilidad derivados de la liquidación, como los descuentos por pronto pago y las pérdidas y ganancias en divisas. Los movimientos que se cerraron con la liquidación se volverán a abrir.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.
2. Abrir la ficha de cliente correspondiente.
3. Seleccione la acción **Movimientos**.
4. Seleccione el movimiento relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
5. De forma alternativa, seleccione la acción **Movimiento detallado**.
6. Seleccione el movimiento de liquidación relevante y, a continuación, seleccione la acción **Desliquidar entradas**.
7. Rellene los campos de la cabecera y, a continuación, seleccione la acción **Desliquidar**.  

> [!IMPORTANT]  
>   Si se ha liquidado un movimiento con más de un movimiento de liquidación, primero deberá deshacer la liquidación más reciente.  

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

