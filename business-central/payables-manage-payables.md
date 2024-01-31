---
title: Resumen de tareas para administrar los pagos
description: 'Describe las tareas para administrar los pagos, por ejemplo, los pagos a acreedores o la liquidación de pagos salientes en movimientos para cerrar facturas o abonos.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '161, 254, 256, 347, 574, 599, 9002'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Administración de pagos

Una gran parte de la gestión de cuentas por pagar es pagar a sus proveedores, o reembolsar los gastos a sus empleados. Puede usar funciones para agregar líneas de pagos de facturas de compra pendientes en la página **Diario de pagos**. Para enviar transacciones a su banco, puede exportar varias líneas de diario de pagos a un archivo y, a continuación, cargar el archivo a su banco. También puede efectuar pagos por cheque, incluida la transmisión de cheques como pagos electrónicos.

Otra tarea típica es liquidar pagos salientes a sus movimientos de proveedor o empleado relacionados para cerrar las facturas de compra o los abonos de compra o las cuentas de empleado como pagados. Puede realizar esta acción en la página **Diario de conciliación de pagos** importando un archivo de extracto bancario para registrar los pagos. Los pagos se liquidan en los movimientos de proveedor, cliente o empleado pendiente mediante coincidencias entre el texto de pago y la información de movimiento. Existen varias formas de revisar y modificar las coincidencias antes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

De forma alternativa, puede liquidar los pagos salientes manualmente en la página **Diario de pagos** o desde los movimientos de proveedor o empleado relacionados.

En la tabla siguiente se muestra una secuencia de tareas de cuentas por pagar, con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Generar pagos de proveedores o reembolsos a empleados, preparar pagos con cheques y exportar pagos a un archivo bancario al registrarlos. |[Creación de pagos](payables-make-payments.md) |
| Liquide pagos de proveedores automáticamente con facturas de compra sin abonar importando un archivo de extracto bancario. |[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide pagos de proveedor con facturas de compra sin abonar manualmente. |[Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md) |
|Asegúrese de la valoración de inventario correcta mediante la asignación de costes de producto, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar.|[Usar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)|
|Reembolse a los empleados por gastos personales durante las actividades comerciales mediante el pago a su cuenta bancaria.|[Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md)|

## Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Usar los cargos de productos a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
