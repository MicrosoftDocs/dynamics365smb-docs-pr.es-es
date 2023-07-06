---
title: Resumen de tareas para administrar cobros
description: Este tema resume las tareas para administrar los cobros y liquidar los pagos en los movimientos de cliente o proveedor.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer payment, debtor, balance due, AR'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="managing-receivables"></a><a name="managing-receivables"></a><a name="managing-receivables"></a><a name="managing-receivables"></a>Administrar cobros

Un paso normal en el ritmo financiero es conciliar las cuentas bancarias, lo que requiere liquidar pagos entrantes en las movimientos de cliente o propiedad para cerrar las facturas de venta y los abonos de compra como pagados.

Si bien la mayoría de los clientes en entornos B2B pagan después de la entrega y dejan las facturas de ventas publicadas abiertas para que el departamento de Cobros las cierre (aplique) cuando se recibe el pago, algunas facturas de ventas se pueden pagar de inmediato, por ejemplo con PayPal. Dichas facturas se liquidan inmediatamente como pagadas cuando se contabilizan y, por lo tanto, no aparecen como pagos en procesos en AR. Para obtener más información, vea, por ejemplo [Facturar ventas](sales-how-invoice-sales.md).  

En [!INCLUDE[prod_short](includes/prod_short.md)], una de las formas más rápidas de registrar pagos es con la página **Diario de conciliación de pagos** mediante la importación de un archivo de extracto bancario o una fuente. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias de datos entre el texto de pago y la información de movimiento. Puede revisar y modificar las coincidencias antes de registrar el diario, y cerrar los movimientos de banco para los movimientos al registrar el diario. La cuenta bancaria se concilia cuando se liquidan todos los pagos.

Existen otras páginas donde puede liquidar pagos o conciliar cuentas bancarias:

* La página **Conciliación banco**, donde concilia las cuentas bancarias haciendo coincidir las líneas de extracto bancario importado con los movimientos de cuenta bancaria del sistema. Aquí, también puede conciliar pagos por cheque. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md). Aquí, no puede liquidar los pagos.
* La página **Registro de pagos**, donde puede liquidar manualmente los pagos recibidos como efectivo, cheque o transacción bancaria frente a una lista de documentos de ventas sin pagar. Tenga en cuenta que esta funcionalidad solo está disponible para documentos de ventas. Aquí, no puede liquidar pagos salientes, y no puede conciliar cuentas bancarias.
* La página **Diario de recibos de efectivo**, donde puede registrar manualmente los albaranes en el libro mayor, cliente u otra cuenta pertinente introduciendo una línea de pago. Puede liquidar el albarán o el reembolso a uno o varios movimientos abiertos antes de registrar el diario de cobros o desde movimientos de cliente. Aquí, no puede conciliar cuentas bancarias.

La página **Diario de conciliación de pagos** usa lógica de conciliación automática que puede configurar en la página **Reglas de liquidación de pago**. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).  

Otros aspectos de la gestión de los cobros incluyen el cobro de los saldos pendientes, incluidos los gastos financieros y los recordatorios, así como la apertura de cuentas bancarias para permitir que los pagos de los clientes se retiren automáticamente de su cuenta.

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir los movimientos de clientes o proveedores basados en un archivo o fuente de extracto bancario importado y concilie la cuenta bancaria cuando se apliquen todos los pagos. |[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide los pagos para abrir los movimientos de un cliente según una lista de documentos de ventas pendientes de pago en la página **Registro de pagos**. |[Conciliar pagos de cliente desde una lista de documentos de venta sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Registre reembolsos o recibos de efectivo de clientes en el diario de cobros y aplíquelos a movimientos de cliente, ya sea desde el diario o desde movimientos registrados. |[Concilie los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente.](receivables-how-apply-sales-transactions-manually.md) |
| Recordar a los clientes los importes vencidos, calcular intereses y administrar los cobros. |[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md) |
|Con el consentimiento de sus clientes, los pagos se cobran directamente al banco del cliente, solo en euros.|[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Bloquear a un cliente para que no pueda entrar en documentos o publicaciones, por ejemplo porque es insolvente.|[Bloquear clientes](receivables-how-block-customers.md)|
|Configure una tolerancia por la que el sistema cierre una factura aunque el pago, incluido el descuento, no cubra totalmente el importe de la factura.|[Trabajar con tolerancias de pago y tolerancias de descuento de pago](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Predecir cuando los pagos se realizarán tarde para los documentos de ventas. | [Extensión de predicción de pagos atrasados](ui-extensions-late-payment-prediction.md) |

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Ccial](sales-manage-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
