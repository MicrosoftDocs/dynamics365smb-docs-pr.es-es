---
title: Liquidar pagos a documentos relacionados y publicarlos | Documentos de Microsoft
description: "Describe cómo registrar los pagos que realiza a los proveedores y los reembolsos que realiza a los clientes."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: es-es
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Registre pagos y reembolsos
En la ventana **Diario de pagos**, registre los pagos que realiza a los proveedores y los reembolsos que realiza a los clientes. Cuando publica una línea de diario de pagos, el importe pagado se registra en la cuenta bancaria del sistema especificada. A continuación, debe tomar medidas para realizar la transferencia de dinero real desde la cuenta bancaria relacionada.

Si completa el campo **Liq. por n.º documento** con la factura o nota de crédito que debe pagarse o reembolsarse, entonces el documento en cuestión se configura como pagado cuando publica el diario. Esto se conoce como entrega "liquidada". Como alternativa a la aplicación durante la publicación de pagos, puede usar la ventana **Aplicar movs. proveedor** y **Aplicar movs. cliente** después de realizar la publicación de los pagos. Para obtener más información, consulte, por ejemplo [Conciliar pagos de proveedor manualmente](payables-how-apply-purchase-transactions-manually.md).

La función **Proponer pagos a proveedores** puede ayudarle a completar líneas de diario de pagos automáticamente de acuerdo con la priorización del proveedor y las fechas de vencimiento. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md). Con esta función, se rellena siempre el campo **Liq. por nº documento**.

Además de registrar que se realiza el pago, también puede usar la ventana **Diario de pagos** para generar el pago y procesarlo en su banco. Para obtener más información, consulte [Realizar pagos de cheques](payables-how-work-checks.md) y [Realizar pagos electrónicos](payables-how-export-payments-bank-file.md).  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Abra la sección de diario dedicada a los pagos.
3. Si sabe a quién pagar o reembolsar, complete los campos manualmente. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para aplicar también el pago a la factura o abono relacionado, seleccione el campo **Liq. por n.º documento**, en la ventana **Aplicar movs. proveedor**, seleccione la factura o abono relevante, y luego elija el botón **Aceptar**.

    Muchos de los campos, como **Importe** y **Fecha vencimiento**, ahora se rellenan con información del documento seleccionado.
5. También puede usar la función **Proponer pagos a proveedores**. Toda la información aplicable y los importes también se ingresan en las líneas del diario. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

    Los mensajes le guiarán para completar correctamente los campos obligatorios.
6.  Cuando se completen todas las líneas del diario de pagos, seleccione la acción **Registrar**.

## <a name="see-also"></a>Consulte también
[Realizar pagos por cheque](payables-how-work-checks.md)  
[Realizar pagos electrónicos](payables-how-export-payments-bank-file.md)  
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

