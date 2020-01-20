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
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 85f7feccd0eefa7c709ce077a8b01b049fc675c8
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2020
ms.locfileid: "2954061"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Liquidación de pagos automáticamente y conciliación de cuentas bancarias
Debe conciliar con frecuencia los bancos y las cuentas de cobros y de pagos liquidando pagos registrados en el banco en sus facturas abiertas (sin abonar) relacionadas, abonos y otros movimientos pendientes en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Puede realizar esta tarea en la página **Diario de conciliación de pagos**, por ejemplo, importando una fuente o archivo de extracto bancario para registrar rápidamente los pagos. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias entre el texto de pago y la información de movimiento. Puede revisar y cambiar las liquidaciones automáticas entes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

La lógica que rige cómo se compara automáticamente el texto de pago con la información de movimiento se configura en la página **Reglas de liquidación de pago** como una serie de reglas priorizadas que puede editar.

También puede conciliar cuentas bancarias sin liquidar pagos simultáneamente. Este trabajo se realiza en la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).   

Para importar extractos bancarios como fuente de banco, primero debe configurar y habilitar el servicio Envestnet Yodlee Bank Feeds y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

De forma alternativa, puede usar la extensión AMC Banking 365 Fundamentals para convertir un archivo de extracto de cuenta, en cualquier formato, a una secuencia de datos que pueda importar en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir movimientos de clientes o proveedores importando un extracto bancario y concilie la cuenta bancaria cuando se liquiden todos los pagos. |[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md) |
| Liquide manualmente pagos viendo información detallada sobre datos coincidentes y sugerencias para movimientos pendientes candidatos en los que liquidar pagos. |[Revisar o aplicar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md) |
| Resuelva los pagos que no se pueden liquidar automáticamente a sus movimientos pendientes relacionados. Por ejemplo, porque los importes son distintos o porque no existe ningún movimiento relacionado. |[Conciliar pagos que no se pueden liquidar automáticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Vincule el texto sobre pagos con cuentas concretas de cliente, de proveedor o de contabilidad para que siempre se registren recibos de cobro o gastos periódicos en dichas cuentas cuando no haya documentos a los que aplicarlos. |[Asignar texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Establezca reglas para determinar el modo en que los pagos/operaciones bancarias deben liquidarse automáticamente en los movimientos pendientes relacionados cuando se utiliza la función **Liquidar automáticamente** en la página **Diario de conciliación de pagos**.|[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learnlearnmodulesuse-journals-dynamics-365-business-centralindex"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
