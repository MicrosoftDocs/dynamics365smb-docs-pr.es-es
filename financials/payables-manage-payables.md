---
title: Administrar pagos | Documentos de Microsoft
description: "Administración de pagos"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


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

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

