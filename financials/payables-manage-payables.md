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
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Administración de pagos
Una importante parte de administrar los pagos es pagar a los proveedores. Puede usar funciones para agregar líneas de pagos de facturas de compra pendientes en la ventana **Diario de pagos**. Para enviar transacciones a su banco, puede exportar varias líneas de diario de pagos a un archivo y, a continuación, cargar el archivo a su banco. También puede efectuar pagos por cheque, incluida la transmisión de cheques como pagos electrónicos.

Otra tarea típica es liquidar pagos salientes a sus movimientos de proveedor relacionados para cerrar las facturas de compra o los abonos de compra como pagados. Puede realizar esta acción en la ventana **Diario de conciliación de pagos** importando un archivo de extracto bancario para registrar los pagos. Los pagos se liquidan en los movimientos de proveedor o cliente pendiente mediante coincidencias entre el texto de pago y la información de movimiento. Existen varias formas de revisar y modificar las coincidencias antes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

De forma alternativa, puede liquidar los pagos salientes manualmente en la ventana **Diario de pagos** o desde los movimientos de proveedor relacionados.

En la tabla siguiente se muestra una secuencia de tareas de cuentas por pagar, con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Genere pagos de proveedor pendientes con prioridad según los descuentos por pronto pago y las penalizaciones por retraso. De forma opcional, exporte los pagos a un archivo bancario al registrarlos. |[Realizar pagos](payables-make-payments.md) |
| Liquide pagos de proveedores automáticamente con facturas de compra sin abonar importando un archivo de extracto bancario. |[Liquidar pagos automáticamente y conciliar cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide pagos de proveedor con facturas de compra sin abonar manualmente. |[Conciliar pagos de proveedor manualmente](payables-how-apply-purchase-transactions-manually.md) |
|Asegúrese de la valoración de inventario correcta mediante la asignación de costes de producto, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar.|[Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

