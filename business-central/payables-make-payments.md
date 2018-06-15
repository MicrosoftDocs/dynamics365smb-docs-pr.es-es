---
title: Resumen de tareas para administrar los pagos a proveedores | Documentos de Microsoft
description: "Describe las tareas para administrar los pagos a proveedores o acreedores, incluido el registro de líneas de pago, y obtener un resumen de saldo vencido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 6b912e8f54fd0e3fb4ac4a1eee3c376c209ffe65
ms.contentlocale: es-es
ms.lasthandoff: 04/26/2018

---
# <a name="making-payments"></a>Creación de pagos
Cuando efectúa pagos a proveedores o reembolsos a empleados, las líneas de pago relacionadas se registran en la ventana **Diario de pagos**. Puede usar la función **Proponer pagos a proveedores** para buscar los pagos vencidos del proveedor. También puede usar el informe **Proveedor - Pagos por periodos** para obtener una visión general de los pagos vencidos del proveedor.

Desde el diario de pagos, puede imprimir cheques automáticos o registrar cuándo se escriben los cheques. Si selecciona **Cheque automático** en el campo **Tipo pago por banco**, las líneas que representan cheques se deben imprimir antes de que se pueda registrar el diario de pagos.

Cuando se registran los pagos, puede exportarlos a un archivo de banco que se cargará al sitio de banco electrónico para su procesamiento.

Cuando se hayan efectuado los pagos en su banco, debe liquidarlos a sus movimientos de proveedor o empleado abiertos relacionados. Puede hacerlo manualmente o importando un archivo de extracto bancario y liquidando los pagos automáticamente. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
|Información sobre las funciones básicas de la ventana **Diario de pagos**, basada en el diario general, para prepararse para registrar pagos a proveedores o empleados.|[Trabajar con diarios generales](ui-work-general-journals.md)|
|Publique pagos a proveedores y reembolsos a clientes y, opcionalmente, aplique los pagos a las facturas/abonos sin pagar para cerrarlos como pagados.|[Registre pagos y reembolsos](payables-how-post-payments-refunds.md)|
| Use una función en la ventana **Diario de pagos** para sugerir pagos de proveedores según los criterios seleccionados, como la fecha de vencimiento, la posibilidad de aplicar descuentos o su liquidez. |[Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md) |
| Emita cheques para realizar pagos a proveedor o reembolsos a cliente, ya sean en papel o automáticos. Anule los cheques antes o después del registro. |[Realizar pagos por cheque](payables-how-work-checks.md) |
|Realice pagos electrónicos mediante la exportación de pagos a un archivo de banco que envíe a su banco para su procesamiento, incluido EFT (transferencia electrónica de fondos) en Norteamérica. |[Realizar pagos electrónicos](payables-how-export-payments-bank-file.md)|
|Realizar pagos electrónicos en función del estándar de transferencia de crédito SEPA de la UE.|[Realizar pagos con Servicio de conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Pague al proveedor en efectivo o cheque y registre el pago cuando registre la factura. |[Liquidar facturas de compra inmediatamente](finance-how-to-settle-purchase-invoices-promptly.md) |
|Reembolse a los empleados por gastos personales durante las actividades comerciales mediante el pago a su cuenta bancaria.|[Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md)|
| Asegúrese de que su banco solo compensa cheques e importes validados enviándoles un archivo que contenga la información de proveedor, cheque y pago. |[Exportar un archivo de Positive Pay](finance-how-positive-pay.md) |

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

