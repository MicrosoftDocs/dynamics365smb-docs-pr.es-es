---
title: Liquidar pagos a documentos relacionados y publicarlos | Documentos de Microsoft
description: Describe cómo registrar los pagos que realiza a los proveedores y los reembolsos que realiza a los clientes.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: a35dc8fb1bd6725d4c1f62d387408234f7419b74
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076978"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrar pagos y reembolsos en el diario de pagos

En la página **Diario de pagos**, registre los pagos que realiza a los proveedores y los reembolsos que realiza a los clientes. Cuando publica una línea de diario de pagos, el importe pagado se registra en la cuenta bancaria del sistema especificada. A continuación, debe tomar medidas para realizar la transferencia de dinero real desde la cuenta bancaria relacionada.  

El diario de pagos es un diario general que se optimiza para crear pagos. Puede agregar líneas rápidamente de forma manual, puede permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] sugiera pagos a proveedores y puede aplicar el pago a los documentos publicados. A pesar de que está haciendo pagos, debe introducir una cantidad positiva en el campo **Importe del documento**. Dependiendo del tipo de documento para la línea de diario, este importe se convierte a un importe negativo en las transacciones subyacentes. De esta manera, es más rápido agregar líneas de diario manualmente. Si prefiere introducir importes negativos, puede personalizar el diario de pagos para que muestre el campo **Importe** en su lugar.  

- Aplicación de pagos a facturas o abonos

    Si completa el campo **Liq. por n.º documento** con la factura o nota de crédito que debe pagarse o reembolsarse, entonces el documento en cuestión se configura como pagado cuando publica el diario. Esto se conoce como entrega "liquidada". Como alternativa a la aplicación durante la publicación de pagos, puede usar la página **Aplicar movs. proveedor** y **Aplicar movs. cliente** después de realizar la publicación de los pagos. Para obtener más información, consulte por ejemplo, [Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md).  

- Obtener pagos sugeridos a proveedores o empleados

    Las funciones **Proponer pagos a proveedores** y **Proponer pagos a empleados** pueden ayudarle a completar líneas de diario de pagos automáticamente de acuerdo con la priorización del proveedor y las fechas de vencimiento. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md). Con esta función, se rellena siempre el campo **Liq. por nº documento**.  

- Imprimir cheques y enviar pagos electrónicamente a su banco

    Además de registrar que se realiza el pago, también puede usar la página **Diario de pagos** para generar el pago y procesarlo en su banco. Para obtener más información, consulte [Realizar pagos de cheques](payables-how-work-checks.md) y [Realizar pagos electrónicos](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Realizar pagos en el diario de pagos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Abra la sección de diario dedicada a los pagos.
3. Si sabe a quién pagar o reembolsar, complete los campos manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para aplicar también el pago a la factura o abono relacionado, seleccione el campo **Liq. por n.º documento**, en la página **Aplicar movs. proveedor**, seleccione la factura o abono relevante, y luego elija el botón **Aceptar**.

    Muchos de los campos, como **Importe del documento** y **Fecha vencimiento**, ahora se rellenan con información del documento seleccionado.
5. También puede usar la función **Proponer pagos a proveedores**. Toda la información aplicable y los importes también se ingresan en las líneas del diario. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

    Los mensajes le guiarán para completar correctamente los campos obligatorios.
6.  Cuando se completen todas las líneas del diario de pagos, seleccione la acción **Registrar**.

## <a name="see-also"></a>Consulte también
[Realizar pagos por cheque](payables-how-work-checks.md)  
[Realizar pagos electrónicos](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Personalizar el área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
