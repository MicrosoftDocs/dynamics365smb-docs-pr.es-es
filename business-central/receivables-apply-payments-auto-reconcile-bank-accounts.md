---
title: Conciliar cuentas bancarias y liquidar pagos | Documentos de Microsoft
description: Describe las tareas para conciliar las cuentas de banco, cobros y pagos, registrar recibos de efectivo o gastos, y liquidar los pagos automáticamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 124b3e82a38af375128353d977cc250aa9f94cf8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "921660"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Liquidación de pagos automáticamente y conciliación de cuentas bancarias
Debe conciliar con frecuencia las cuentas bancarias, las de cobros y las de pagos liquidando pagos registrados en el banco en sus facturas sin abonar relacionadas, abonos y otros movimientos pendientes en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Puede realizar esta tarea en la página **Diario de conciliación de pagos** importando una fuente o archivo de extracto bancario para registrar rápidamente los pagos. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias entre el texto de pago y la información de movimiento. Puede revisar y cambiar las liquidaciones automáticas entes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

También puede conciliar cuentas bancarias sin liquidar pagos simultáneamente. Este trabajo se realiza en la página **Conciliación banco**. Para obtener más información, vea [Conciliar cuenta bancaria por separado](bank-how-reconcile-bank-accounts-separately.md).   

Para importar extractos bancarios como fuente de banco, primero debe configurar y habilitar el servicio de fuente de banco de Envestnet Yodlee y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  

De forma alternativa, puede usar el servicio de conversión de datos de banco para convertir un archivo de extracto de banco, en cualquier formato, a una secuencia de datos que pueda importar en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configuración del servicio de conversión de datos bancarios](bank-how-setup-bank-data-conversion-service.md).  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir movimientos de clientes o proveedores importando un extracto bancario y concilie la cuenta bancaria cuando se liquiden todos los pagos. |[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md) |
| Liquide manualmente pagos viendo información detallada sobre datos coincidentes y sugerencias para movimientos pendientes candidatos en los que liquidar pagos. |[Revisar o aplicar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md) |
| Resuelva los pagos que no se pueden liquidar automáticamente a sus movimientos pendientes relacionados. Por ejemplo, porque los importes son distintos o porque no existe ningún movimiento relacionado. |[Conciliar pagos que no se pueden liquidar automáticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Vincule el texto sobre pagos con cuentas concretas de cliente, de proveedor o de contabilidad para que siempre se registren recibos de cobro o gastos periódicos en dichas cuentas cuando no haya documentos a los que aplicarlos. |[Asignar texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
