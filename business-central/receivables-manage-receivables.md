---
title: Resumen de tareas para administrar los cobros | Documentos de Microsoft
description: Describe tareas para administrar los cobros y liquidar los pagos en los movimientos de cliente o proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 01a195130a6834256b30efea8c06841c88af354d
ms.contentlocale: es-es
ms.lasthandoff: 05/15/2018

---
# <a name="managing-receivables"></a>Administrar cobros
Un paso normal en el ritmo financiero es conciliar las cuentas bancarias, lo que requiere liquidar pagos entrantes en las movimientos de cliente o propiedad para cerrar las facturas de venta y los abonos de compra como pagados.

Si bien la mayoría de los clientes en entornos B2B pagan después de la entrega y dejan las facturas de ventas publicadas abiertas para que el departamento de Cobros las cierre (aplique) cuando se recibe el pago, algunas facturas de ventas se pueden pagar de inmediato, por ejemplo con PayPal. Dichas facturas se liquidan inmediatamente como pagadas cuando se contabilizan y, por lo tanto, no aparecen como pagos en procesos en AR. Para obtener más información, vea, por ejemplo [Facturar ventas](sales-how-invoice-sales.md).  

En [!INCLUDE[d365fin](includes/d365fin_md.md)], una de las formas más rápidas de registrar pagos desde la ventana **Diario de conciliación de pagos** mediante la importación de un archivo de extracto bancario o una fuente. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias de datos entre el texto de pago y la información de movimiento. Puede revisar y modificar las coincidencias antes de registrar el diario, y cerrar los movimientos de banco para los movimientos al registrar el diario. La cuenta bancaria se concilia cuando se liquidan todos los pagos.

Existen otras ventanas donde puede liquidar pagos o conciliar cuentas bancarias:

* La ventana **Conciliación banco**, donde concilia las cuentas bancarias haciendo coincidir las líneas de extracto bancario importado con los movimientos de cuenta bancaria del sistema. Aquí, también puede conciliar pagos por cheque. Para obtener más información, vea [Conciliar cuentas bancarias por separado](bank-how-reconcile-bank-accounts-separately.md). Aquí, no puede liquidar los pagos.
* La ventana **Registro de pagos**, donde puede liquidar manualmente los pagos recibidos como efectivo, cheque o transacción bancaria frente a una lista de documentos de ventas sin pagar. Tenga en cuenta que esta funcionalidad solo está disponible para documentos de ventas. Aquí, no puede liquidar pagos salientes, y no puede conciliar cuentas bancarias.
* La ventana **Diario de recibos de efectivo**, donde puede registrar manualmente los albaranes en el libro mayor, cliente u otra cuenta pertinente introduciendo una línea de pago. Puede liquidar el albarán o el reembolso a uno o varios movimientos abiertos antes de registrar el diario de cobros o desde movimientos de cliente. Aquí, no puede conciliar cuentas bancarias.  

Otra parte de la gestión de cobros es recopilar saldos pendientes, incluidos intereses, y emitir recordatorios. [!INCLUDE[d365fin](includes/d365fin_md.md)] también ofrece formas de realizar estas acciones. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir los movimientos de clientes o proveedores basados en un archivo o fuente de extracto bancario importado y concilie la cuenta bancaria cuando se apliquen todos los pagos. |[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide pagos para abrir movimientos de cliente basados en una introducción manual de datos en una lista de documentos de ventas sin pagar. |[Conciliar pagos manualmente de una lista de documentos de venta sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Registre reembolsos o recibos de efectivo de clientes en el diario de cobros y aplíquelos a movimientos de cliente, ya sea desde el diario o desde movimientos registrados. |[Conciliar pagos de cliente manualmente](receivables-how-apply-sales-transactions-manually.md) |
| Recordar a los clientes los importes vencidos, calcular intereses y administrar los cobros. |[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md) |
|Asegúrese de que conoce el coste de los productos enviados mediante la asignación de costes de producto, tales como fletes, manipulación física, seguros y transporte en los que incurra después de la venta.|[Usar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)|
|Configure una tolerancia por la que el sistema cierre una factura aunque el pago, incluido el descuento, no cubra totalmente el importe de la factura.|[Trabajar con tolerancias de pago y tolerancias de descuento de pago](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Consulte también
[Ccial](sales-manage-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

