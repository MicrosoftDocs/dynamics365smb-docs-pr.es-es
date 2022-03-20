---
title: Registrar pagos y reembolsos en diario de pagos
description: Obtenga más información sobre cómo registrar pagos que realiza a los proveedores y reembolsos que realiza a los clientes en la página Diario de pagos.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP
ms.search.form: 256, 233, 624, 1228
ms.date: 07/09/2021
ms.author: edupont
ms.openlocfilehash: fa43027481ba7b9eb970182eb62b5e2aa728fb06
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367260"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrar pagos y reembolsos en el diario de pagos

En la página **Diario de pagos**, registre los pagos que realiza a los proveedores y los reembolsos que realiza a los clientes. Cuando publica una línea de diario de pagos, el importe pagado se registra en la cuenta bancaria del sistema especificada. A continuación, debe tomar medidas para realizar la transferencia de dinero real desde la cuenta bancaria relacionada.  

El diario de pagos es un diario general que se optimiza para crear pagos. Puede agregar líneas rápidamente de forma manual, puede permitir que [!INCLUDE[prod_short](includes/prod_short.md)] sugiera pagos a proveedores y puede aplicar el pago a los documentos publicados. A pesar de que está haciendo pagos, debe introducir una cantidad positiva en el campo **Importe del documento**. Dependiendo del tipo de documento para la línea de diario, este importe se convierte a un importe negativo en las transacciones subyacentes. De esta manera, es más rápido agregar líneas de diario manualmente. Si prefiere introducir importes negativos, puede personalizar el diario de pagos para que muestre el campo **Importe** en su lugar.  

- Aplicación de pagos a facturas o abonos

    Si completa el campo **Liq. por n.º documento** con la factura o nota de crédito que debe pagarse o reembolsarse, entonces el documento en cuestión se configura como pagado cuando publica el diario. Esto se conoce como entrega "liquidada". Como alternativa a la aplicación durante la publicación de pagos, puede usar la página **Aplicar movs. proveedor** y **Aplicar movs. cliente** después de realizar la publicación de los pagos. Para obtener más información, consulte por ejemplo, [Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md).  

- Obtener pagos sugeridos a proveedores o empleados

    Las funciones **Proponer pagos a proveedores** y **Proponer pagos a empleados** pueden ayudarle a completar líneas de diario de pagos automáticamente de acuerdo con la priorización del proveedor y las fechas de vencimiento. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md). Con esta función, se rellena siempre el campo **Liq. por nº documento**.  

- Imprimir cheques y enviar pagos electrónicamente a su banco

    Además de registrar que se realiza el pago, también puede usar la página **Diario de pagos** para generar el pago y procesarlo en su banco. Para obtener más información, consulte [Realizar pagos de cheques](payables-how-work-checks.md) y [Realizar pagos electrónicos](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Realizar pagos en el diario de pagos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Abra la sección de diario dedicada a los pagos.
3. Si sabe a quién pagar, complete los campos manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para aplicar también el pago a la factura o abono relacionado, seleccione el campo **Liq. por n.º documento**, en la página **Aplicar movs. proveedor**, seleccione la factura o abono relevante, y luego elija el botón **Aceptar**.

    Muchos de los campos, como **Importe del documento** y **Fecha vencimiento**, ahora se rellenan con información del documento seleccionado.
5. También puede usar la función **Proponer pagos a proveedores**. Toda la información aplicable y los importes también se ingresan en las líneas del diario. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

    Los mensajes le guiarán para completar correctamente los campos obligatorios.
6. Cuando se completen todas las líneas del diario de pagos, seleccione la acción **Registrar**.


## <a name="to-issue-a-refund-check"></a>Para emitir un cheque de reembolso

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. En el campo **Tipo documento**, seleccione **Reembolso**.  
3. En el campo **Número de documento externo**, utilice esto como referencia para el cheque de reembolso (por ejemplo, número de orden de devolución).  
4. En el campo **Tipo mov.**, seleccione **Cliente**.  
5. En el campo **Nº cuenta**, seleccione el número de cuenta del cliente al que se emitirá el cheque de reembolso.  
6. En el campo **Importe**, introduzca el importe que quiere reembolsar.  
7. En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.  
8. En el campo **Bal. Nº cuenta**, seleccione la cuenta bancaria de la que saldrá el cheque.  
9. En el campo **Liq. por n.º documento** , seleccione los documentos que requieren un reembolso.  
10. Cuando se completen todas las líneas del diario de pagos, elija la acción **Publicar / Imprimir**, luego elija la acción **Publicar e imprimir** y seleccione **Sí**.  
  

## <a name="see-also"></a>Consulte también
[Realizar pagos por cheque](payables-how-work-checks.md)  
[Realizar pagos electrónicos](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
