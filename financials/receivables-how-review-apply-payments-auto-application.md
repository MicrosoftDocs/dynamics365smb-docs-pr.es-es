---
title: "Comprobar automáticamente los pagos liquidados y liquidar de nuevo los pagos manualmente | Documentos de Microsoft"
description: "Una vez que los pagos se liquiden automáticamente, puede revisar todos los movimientos de un pago y volver a liquidar manualmente los que se han aplicado incorrectamente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2998cd0841452813cb86ee3859804de93cb9bde9
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-review-or-apply-payments-manually-after-automatic-application"></a>Procedimiento: Revisar o liquidar pagos manualmente después de una liquidación automática
Para cada línea de diario que representa un pago en la ventana **Diario de conciliación de pagos** podrá abrir la ventana **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la correspondencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se aplicaron automáticamente en un movimiento incorrecto. Para obtener más información acerca de la liquidación automática, vea [Procedimiento: Conciliar pagos usando la liquidación automática](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Cuando la cuenta bancaria para la que se están conciliando pagos está configurada para la divisa local, la ventana **Liquidación de pago** mostrará todos los movimientos pendientes en la divisa local, incluidos los movimientos pendientes para documentos facturados originalmente en divisas extranjeras. Los pagos liquidados en movimientos con divisas convertidas se pueden por tanto registrar con importes distintos al del documento original, ya que puede que el banco y [!INCLUDE[d365fin](includes/d365fin_md.md)] usen tipos de cambio potencialmente distintos.

Por tanto, es recomendable buscar los códigos de divisas extranjeras en el campo **Código de divisa** de la ventana **Liquidación de pago** para comprobar si las liquidaciones se basan en divisas convertidas. Para revisar el importe del documento original en la divisa extranjera y ver el tipo de cambio utilizado, elija el campo **Liq. por nº mov.** y, a continuación, en el menú contextual, seleccione el botón desplegable para abrir la ventana **Movimientos de clientes** o la ventana **Movimientos de proveedores**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] no gestiona automáticamente los ajustes de ganancia y pérdida necesarios debido a conversiones de divisa.

> [!NOTE]  
>   No puede liquidar movimientos con signo diferente al signo en el pago. Por ejemplo, para cerrar un abono negativo y su factura positiva, primero deberá liquidar el abono para la factura y, a continuación, liquidar el pago para la factura con el importe pendiente reducido.

> [!WARNING]  
>   Si usa descuentos de pago, y si la fecha de pago es anterior a la fecha de vencimiento del pago, el campo **Importe pendiente incl. descuento** en la ventana **Liquidación de pagos** se usará en la correspondencia. En caso contrario, se usará el valor del campo **Importe pendiente**. Si el pago se realizó con un importe de descuento después de la fecha de vencimiento del pago, o se pagó el importe completo pero se concedió un descuento, entonces el importe no coincidirá.

> [!NOTE]  
>   Puede liquidar solo un pago en una cuenta. Si desea dividir la liquidación en varios movimientos pendientes, por ejemplo para liquidar un pago de suma total, los movimientos pendientes deben serlo para la misma cuenta. Para obtener más información, consulte los pasos 7 y 8 del procedimiento de este tema.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Para revisar o aplicar pagos después de una liquidación automática
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de conciliación de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Abra el diario de conciliación de pagos de un banco para el que desee conciliar los pagos. Para obtener más información, vea [Procedimiento: Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).
3. En la ventana **Diario de conciliación de pagos**, seleccione un pago que desee revisar o liquidar manualmente a uno o varios movimientos pendientes y, a continuación, seleccione la acción **Liquidación manual**.
4. Seleccione la casilla **Liquidado** en la línea correspondiente al movimiento pendiente al que desee liquidar el pago.
5. El importe de pago, que también se mostrará en el campo **Importe de la transacción** en la ventana **Liquidación de pagos**, se inserta en el campo **Importe liquidado**, no obstante puede modificar el campo, por ejemplo si desea liquidar el importe a varios movimientos pendientes.
6. Para liquidar una parte del importe abonado a otro movimiento pendiente para la cuenta, por ejemplo para liquidar un pago de suma total, seleccione la casilla **Liquidado** de la línea. El importe liquidado se deduce automáticamente del importe de las transacciones para reflejar la distribución en los dos movimientos pendientes.
7. Para liquidar una parte de un pago a uno o varios movimientos pendientes que no existe en la base de datos, cree una línea nueva debajo de la línea para la misma cuenta. En el campo **Importe liquidado**, introduzca el importe pendiente de liquidar en la nueva línea y, a continuación, ajuste el campo **Importe liquidado** en la línea existente.
8. Repita el paso 5, 6 o 7 para otros movimientos pendientes en los que desee liquidar el importe de pago completa o parcialmente.
9. Cuando haya revisado una liquidación de pago o la haya liquidado manualmente en uno o varios movimientos pendientes, seleccione la acción **Aceptar liquidación**.

Se cierra la ventana **Liquidación de pagos** y, en la ventana de **Diario de conciliación de pagos** el valor del campo **Confianza de la correspondencia** cambia a **Aceptado** para indicarle que ha revisado o ha liquidado manualmente el pago.

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

