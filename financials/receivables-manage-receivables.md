---
title: Administrar cobros | Documentos de Microsoft
description: Administrar cobros
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 62d59546331a5faa5ecb7aea0f9bb8dedea719f9
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="managing-receivables"></a>Administrar cobros
Un paso normal en el ritmo financiero es conciliar las cuentas bancarias, lo que requiere liquidar pagos en las movimientos de cliente o propiedad para cerrar las facturas de venta y los abonos de compra.  

En [!INCLUDE[d365fin](includes/d365fin_md.md)], una de las formas más rápidas de registrar pagos desde la ventana **Diario de conciliación de pagos** mediante la importación de un archivo de extracto bancario o una fuente. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias de datos entre el texto de pago y la información de movimiento. Puede revisar y modificar las coincidencias antes de registrar el diario, y cerrar los movimientos de banco para los movimientos al registrar el diario. La cuenta bancaria se concilia cuando se liquidan todos los pagos.

No obstante, existen otros lugares prácticos para liquidar los pagos y para conciliar las cuentas bancarias:  

* La ventana **Conciliación banco**, que también le permite comprobar los movimientos contables. Para obtener más información, vea [Procedimiento: Conciliar cuentas bancarias por separado](bank-how-reconcile-bank-accounts-separately.md).  
* La ventana **Registro de pagos**, donde puede liquidar y comprobar manualmente los pagos recibidos como efectivo, cheque o transacción bancaria frente a una lista de documentos de ventas sin pagar. Tenga en cuenta que esta funcionalidad solo está disponible para documentos de ventas.  
* La ventana **Diario de recibos de efectivo**, donde puede registrar manualmente los albaranes en el libro mayor, cliente u otra cuenta pertinente introduciendo una línea de pago. Puede liquidar el albarán o el reembolso a uno o varios movimientos abiertos antes de registrar el diario de cobros o desde movimientos de cliente.  

Otra parte de la gestión de cobros es recopilar saldos pendientes, incluidos intereses, y emitir recordatorios. [!INCLUDE[d365fin](includes/d365fin_md.md)] también ofrece formas de realizar estas acciones. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir los movimientos de clientes o proveedores basados en un archivo o fuente de extracto bancario importado y concilie la cuenta bancaria cuando se apliquen todos los pagos. |[Liquidar pagos automáticamente y conciliar cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Liquide pagos para abrir movimientos de cliente basados en una introducción manual de datos en una lista de documentos de ventas sin pagar. |[Conciliar pagos manualmente de una lista de documentos de venta sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Registre reembolsos o recibos de efectivo de clientes en el diario de cobros y aplíquelos a movimientos de cliente, ya sea desde el diario o desde movimientos registrados. |[Conciliar pagos de cliente manualmente](receivables-how-apply-sales-transactions-manually.md) |
| Recordar a los clientes los importes vencidos, calcular intereses y administrar los cobros. |[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md) |

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

