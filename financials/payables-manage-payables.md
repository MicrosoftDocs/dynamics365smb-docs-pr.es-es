---
title: Resumen de tareas para administrar las cuentas por pagar | Documentos de Microsoft
description: "Describe las tareas para administrar los pagos, por ejemplo, los pagos a acreedores o la liquidación de pagos salientes en movimientos para cerrar facturas o abonos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d260cf22980d097637e26d97282ad5e4f344120a
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="managing-payables"></a>Administración de pagos
Una gran parte de la gestión de cuentas por pagar es pagar a sus proveedores, o reembolsar los gastos a sus empleados. Puede usar funciones para agregar líneas de pagos de facturas de compra pendientes en la ventana **Diario de pagos**. Para enviar transacciones a su banco, puede exportar varias líneas de diario de pagos a un archivo y, a continuación, cargar el archivo a su banco. También puede efectuar pagos por cheque, incluida la transmisión de cheques como pagos electrónicos.

Otra tarea típica es liquidar pagos salientes a sus movimientos de proveedor o empleado relacionados para cerrar las facturas de compra o los abonos de compra o las cuentas de empleado como pagados. Puede realizar esta acción en la ventana **Diario de conciliación de pagos** importando un archivo de extracto bancario para registrar los pagos. Los pagos se liquidan en los movimientos de proveedor, cliente o empleado pendiente mediante coincidencias entre el texto de pago y la información de movimiento. Existen varias formas de revisar y modificar las coincidencias antes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

De forma alternativa, puede liquidar los pagos salientes manualmente en la ventana **Diario de pagos** o desde los movimientos de proveedor o empleado relacionados.

En la tabla siguiente se muestra una secuencia de tareas de cuentas por pagar, con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Generar pagos de proveedores o reembolsos a empleados, preparar pagos con cheques y exportar pagos a un archivo bancario al registrarlos. |[Creación de pagos](payables-make-payments.md) |
| Liquide pagos de proveedores automáticamente con facturas de compra sin abonar importando un archivo de extracto bancario. |[Liquidar pagos automáticamente y conciliar cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide pagos de proveedor con facturas de compra sin abonar manualmente. |[Conciliar pagos de proveedor manualmente](payables-how-apply-purchase-transactions-manually.md) |
|Asegúrese de la valoración de inventario correcta mediante la asignación de costes de producto, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar.|[Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

