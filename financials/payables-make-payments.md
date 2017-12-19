---
title: Resumen de tareas para administrar los pagos a proveedores | Documentos de Microsoft
description: "Describe las tareas para administrar los pagos a proveedores o acreedores, incluido el registro de líneas de pago, y obtener un resumen de saldo vencido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 6cd7b9922f047d05a2cc37a9157de47221f67a7f
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="making-payments"></a>Creación de pagos
Cuando efectúa pagos a proveedores o reembolsos a empleados, las líneas de pago relacionadas se registran en la ventana **Diario de pagos**. Puede usar la función **Proponer pagos a proveedores** para buscar los pagos vencidos del proveedor. También puede usar el informe **Proveedor - Pagos por periodos** para obtener una visión general de los pagos vencidos del proveedor.

Desde el diario de pagos, puede imprimir cheques automáticos o registrar cuándo se escriben los cheques. Si selecciona **Cheque automático** en el campo **Tipo pago por banco**, las líneas que representan cheques se deben imprimir antes de que se pueda registrar el diario de pagos.

Cuando se registran los pagos, puede exportarlos a un archivo de banco que se cargará al sitio de banco electrónico para su procesamiento.

Cuando se hayan efectuado los pagos en su banco, debe liquidarlos a sus movimientos de proveedor o empleado abiertos relacionados. Puede hacerlo manualmente o importando un archivo de extracto bancario y liquidando los pagos automáticamente. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
|Utilice la ventana **Diario de pagos**, basada en el diario general, para registrar pagos a proveedores o empleados.|[Trabajar con diarios generales](ui-work-general-journals.md)|
| Use una función para sugerir pagos de proveedores según los criterios seleccionados, como la fecha de vencimiento, la posibilidad de aplicar descuentos o su liquidez. |[Propuesta de pagos a proveedores](payables-how-suggest-vendor-payments.md) |
|Reembolse a los empleados por gastos personales durante las actividades comerciales mediante el pago a su cuenta bancaria.|[Procedimiento: registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md)|
| Emita cheques para realizar pagos a proveedor, ya sean en papel o automáticos. Anule los cheques antes o después del registro. |[Procedimiento: Trabajar con cheques](payables-how-work-checks.md) |
| Pague al proveedor en efectivo o cheque y registre el pago cuando registre la factura. |[Liquidación de facturas de compra inmediatamente](finance-how-to-settle-purchase-invoices-promptly.md) |
| Asegúrese de que su banco solo compensa cheques e importes validados enviándoles un archivo que contenga la información de proveedor, cheque y pago. |[Exportar un archivo de Positive Pay](finance-how-positive-pay.md) |
|Exporte los pagos desde la ventana **Diario de pagos** a un archivo de banco que envíe a su banco para su procesamiento, incluido EFT (transferencia electrónica de fondos) en Norteamérica. |[Exportación de pagos a un archivo de banco](payables-how-export-payments-bank-file.md)|
|Realizar pagos electrónicos en función del estándar de transferencia de crédito SEPA de la UE.|[Realizar pagos con Servicio de conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|    

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

