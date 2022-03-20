---
title: Revisar y aplicar pagos manualmente después de unanaplicación automática
description: Una vez que los pagos se liquiden automáticamente, puede revisar todos los movimientos de un pago y volver a liquidar manualmente los que se han aplicado incorrectamente.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.search.form: 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9a4a25de9d1aab74c0c721fbdbda6704a2ae8666
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383062"
---
# <a name="review-and-apply-payments-manually-after-automatic-application"></a>Revisar y aplicar pagos manualmente después de unanaplicación automática
Para cada línea de diario que representa un pago en la página **Diario de conciliación de pagos** podrá abrir la página **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la correspondencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se aplicaron automáticamente en un movimiento incorrecto. Para obtener más información acerca de la liquidación automática, vea [Conciliar pagos usando la liquidación automática](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Cuando la cuenta bancaria para la que se están conciliando pagos está configurada para la divisa local, la página **Liquidación de pago** mostrará todos los movimientos pendientes en la divisa local, incluidos los movimientos pendientes para documentos facturados originalmente en divisas extranjeras. Los pagos liquidados en movimientos con divisas convertidas se pueden por tanto registrar con importes distintos al del documento original, ya que puede que el banco y [!INCLUDE[prod_short](includes/prod_short.md)] usen tipos de cambio potencialmente distintos.

Por tanto, es recomendable buscar los códigos de divisas extranjeras en el campo **Código de divisa** de la página **Liquidación de pago** para comprobar si las liquidaciones se basan en divisas convertidas. Para revisar el importe del documento original en la divisa extranjera y ver el tipo de cambio utilizado, elija el campo **Liq. por nº mov.** y, a continuación, en el menú contextual, seleccione el botón desplegable para abrir la ventana **Movimientos de clientes** o la página **Movimientos de proveedores**.

[!INCLUDE[prod_short](includes/prod_short.md)] no gestiona automáticamente los ajustes de ganancia y pérdida necesarios debido a conversiones de divisa.

> [!NOTE]  
>   No puede liquidar movimientos con signo diferente al signo en el pago. Por ejemplo, para cerrar un abono negativo y su factura positiva, primero deberá liquidar el abono para la factura y, a continuación, liquidar el pago para la factura con el importe pendiente reducido.

> [!WARNING]  
>   Si usa descuentos de pago, y si la fecha de pago es anterior a la fecha de vencimiento del pago, el campo **Importe pendiente incl. descuento** en la página **Liquidación de pagos** se usará en la correspondencia. En caso contrario, se usará el valor del campo **Importe pendiente**. Si el pago se realizó con un importe de descuento después de la fecha de vencimiento del pago, o se pagó el importe completo pero se concedió un descuento, entonces el importe no coincidirá.

> [!NOTE]  
>   Puede liquidar solo un pago en una cuenta. Si desea dividir la liquidación en varios movimientos pendientes, por ejemplo para liquidar un pago de suma total, los movimientos pendientes deben serlo para la misma cuenta. Para obtener más información, consulte los pasos 7 y 8 del procedimiento de este tema.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Para revisar o aplicar pagos después de una liquidación automática
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de conciliación de pagos** y luego elija el enlace relacionado.
2. Abra el diario de conciliación de pagos de un banco para el que desee conciliar los pagos. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).
3. En la página **Diario de conciliación de pagos**, seleccione un pago que desee revisar o liquidar manualmente a uno o varios movimientos pendientes y, a continuación, seleccione la acción **Liquidación manual**.
4. Seleccione la casilla **Liquidado** en la línea correspondiente al movimiento pendiente al que desee liquidar el pago.
5. El importe de pago, que también se mostrará en el campo **Importe de la transacción** en la página **Liquidación de pagos**, se inserta en el campo **Importe liquidado**, no obstante puede modificar el campo, por ejemplo si desea liquidar el importe a varios movimientos pendientes.
6. Para liquidar una parte del importe abonado a otro movimiento pendiente para la cuenta, por ejemplo para liquidar un pago de suma total, seleccione la casilla **Liquidado** de la línea. El importe liquidado se deduce automáticamente del importe de las transacciones para reflejar la distribución en los dos movimientos pendientes.
7. Para liquidar una parte de un pago a uno o varios movimientos pendientes que no existe en la base de datos, cree una línea nueva debajo de la línea para la misma cuenta. En el campo **Importe liquidado**, introduzca el importe pendiente de liquidar en la nueva línea y, a continuación, ajuste el campo **Importe liquidado** en la línea existente.
8. Repita el paso 5, 6 o 7 para otros movimientos pendientes en los que desee liquidar el importe de pago completa o parcialmente.
9. Cuando haya revisado una liquidación de pago o la haya liquidado manualmente en uno o varios movimientos pendientes, seleccione la acción **Aceptar liquidación**.

Se cierra la página **Liquidación de pagos** y, en la página **Diario de conciliación de pagos** el valor del campo **Confianza de la correspondencia** cambia a **Aceptado** para indicarle que ha revisado o ha liquidado manualmente el pago.

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]