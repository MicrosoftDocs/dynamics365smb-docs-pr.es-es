---
title: Conciliar cuentas bancarias y aplicar pagos
description: 'Describe las tareas para conciliar las cuentas de banco, cobros y pagos, registrar recibos de efectivo o gastos, y liquidar los pagos automáticamente.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a><a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Liquidación de pagos automáticamente y conciliación de cuentas bancarias
Debe conciliar con frecuencia los bancos y las cuentas de cobros y de pagos liquidando pagos registrados en el banco en sus facturas abiertas (sin abonar) relacionadas, abonos y otros movimientos pendientes en [!INCLUDE[prod_short](includes/prod_short.md)].  

Puede realizar esta tarea en la página **Diario de conciliación de pagos**, por ejemplo, importando una fuente o archivo de extracto bancario para registrar rápidamente los pagos. Los pagos se liquidan en los movimientos de cliente o proveedor abiertos en función de las coincidencias entre el texto de pago y la información de movimiento. Puede revisar y cambiar las liquidaciones automáticas entes de registrar el diario. Puede elegir cerrar los movimientos de cuentas bancarias abiertos relacionados con los movimientos liquidados cuando registra el diario. La cuenta bancaria se concilia automáticamente cuando se liquidan todos los pagos.

La lógica que rige cómo se compara automáticamente el texto de pago con la información de movimiento se configura en la página **Reglas de liquidación de pago** como una serie de reglas priorizadas que puede editar.

También puede conciliar cuentas bancarias sin liquidar pagos simultáneamente. Este trabajo se realiza en la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).   

Para importar extractos bancarios como fuente de banco, primero debe configurar y habilitar el servicio Envestnet Yodlee Bank Feeds y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> También puede importar archivos de extractos de cuenta en formato delimitado por coma o punto y coma (.CSV). Use la configuración asistida **Configurar un formato de archivo de extracto de cuenta** para definir formatos de importación de extractos de cuenta y adjuntar el formato a una cuenta bancaria. A continuación, puede usar estos formatos cuando importe extractos de cuenta en la página **Conciliación de cuentas bancarias**.

De forma alternativa, puede usar la extensión AMC Banking 365 Fundamentals para convertir un archivo de extracto de cuenta, en cualquier formato, a una secuencia de datos que pueda importar en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

| Para | Vea |
| --- | --- |
| Liquide pagos para abrir movimientos de clientes o proveedores importando un extracto bancario y concilie la cuenta bancaria cuando se liquiden todos los pagos. |[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md) |
| Liquide manualmente pagos viendo información detallada sobre datos coincidentes y sugerencias para movimientos pendientes candidatos en los que liquidar pagos. |[Revisar o aplicar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md) |
| Resuelva los pagos que no se pueden liquidar automáticamente a sus movimientos pendientes relacionados. Por ejemplo, porque los importes son distintos o porque no existe ningún movimiento relacionado. |[Conciliar pagos que no se pueden liquidar automáticamente](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Vincule el texto sobre pagos con cuentas concretas de cliente, de proveedor o de contabilidad para que siempre se registren recibos de cobro o gastos periódicos en dichas cuentas cuando no haya documentos a los que aplicarlos. |[Asignar texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Establezca reglas para determinar el modo en que los pagos/operaciones bancarias deben liquidarse automáticamente en los movimientos pendientes relacionados cuando se utiliza la función **Liquidar automáticamente** en la página **Diario de conciliación de pagos**.|[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/use-journals-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
