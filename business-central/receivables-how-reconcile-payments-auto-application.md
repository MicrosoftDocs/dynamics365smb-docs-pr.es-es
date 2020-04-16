---
title: Usar la liquidación automática para conciliar pagos | Documentos de Microsoft
description: Describe cómo usar la función de liquidación automática para liquidar pagos o recibos de efectivo en sus movimientos pendientes relacionados y conciliar pagos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c0acef518c6333061aa9c321b91c47aa1da8df2c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191992"
---
# <a name="reconcile-payments-using-automatic-application"></a>Conciliar los pagos con liquidación automática
La página **Diario de conciliación de pagos** especifica pagos, bien entrantes de clientes o salientes a proveedores, que se han registrado como transacciones en la cuenta bancaria en línea y que puede liquidar a sus clientes, vendedores y movimientos de la cuenta pendientes. Las líneas del diario se rellenan importando un extracto bancario como una fuente o un archivo de banco.

> [!NOTE]
> La página ofrece una funcionalidad de coincidencia automática que liquida pagos a sus movimientos abiertos relacionados basados en una coincidencia de texto en una línea de estado bancario (línea de diario) con texto en uno o más movimientos abiertos. Tenga en cuenta que puede sobrescribir las aplicaciones automáticas sugeridas y puede optar por no utilizar la aplicación automática. Para obtener más información, vea el paso 7 .

Un diario de conciliación de pago está relacionado con una cuenta bancaria en [!INCLUDE[d365fin](includes/d365fin_md.md)] que refleja la cuenta bancaria en línea donde se registran las transacciones de pago. Todas las cuenta abiertas relacionada con los movimientos de los clientes o los proveedores se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Si desea importar tanto extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio Envestnet Yodlee Bank Feeds y, a continuación, vincular la cuenta bancaria a la cuentas bancaria en línea relacionada. El diario de conciliación de pagos detectará automáticamente las fuentes de banco cuando seleccione la acción **Importar transacciones de banco**. Además, puede configurar una cuenta bancaria para que importe nuevas fuentes de extractos bancarios cada hora. No se importarán las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Con la acción **Asignar texto a cuenta** puede configurar asignaciones entre el texto de los pagos y la cuentas de débito, crédito y saldo específicas para que los pagos se contabilicen en las cuentas específicas cuando contabilices el diario de conciliación de pagos. Consulte el paso 8. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

La funcionalidad similar existe para conciliar el exceso de importes en las líneas del diario de conciliación de pagos sobre una base ad hoc. Para obtener más información, vea [Conciliar pagos que no pueden liquidarse](receivables-how-reconcile-payments-cannot-apply-auto.md)

La función **Liquidar automáticamente** se usa automáticamente cuando se importa una fuente o un archivo bancario con transacciones de pago, o cuando se activa para liquidar pagos en sus movimientos pendientes relacionados basándose en una coincidencia de texto en una línea de extracto bancario (línea de diario) con texto en una o más entradas abiertas. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

En las líneas de diario donde un pago se ha liquidado automáticamente a un movimiento pendiente o varios, el campo **Confianza de la correspondencia** tiene un valor entre Baja y Alta para indicar la calidad de la correspondencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Tipo de cuenta** y **N.º de cuenta** se rellenan con información sobre el cliente o el proveedor en el que se ha liquidado el pago. Si ha configurado una asignación de texto a cuenta, la liquidación automática puede dar como resultado un valor de confianza de correspondencia **Alta: asignación de texto a cuenta**.

Para cada línea de diario en la página **Diario de conciliación de pagos** podrá abrir la página **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la correspondencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se aplicaron automáticamente en un movimiento incorrecto. Para obtener más información, vea [Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Puede iniciar la importación de las transacciones bancarias al mismo tiempo que abre la página **Conciliación de pagos** para un diario de conciliación de pagos existente en la página **Diarios de conciliación de pago**. El procedimiento siguiente describe cómo importar transacciones bancarias a la página **Diario de conciliación de pagos** una vez creado un nuevo diario.

## <a name="to-reconcile-payments-using-automatic-application"></a>Para conciliar los pagos con liquidación automática
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario de conciliación de pagos** y luego elija el enlace relacionado.
2. Para trabajar en un nuevo diario de conciliación de pago, seleccione la acción **Nuevo diario**.
3. En la página **Lista cuentas bancarias pago**, seleccione la cuenta bancaria que desee conciliar los pagos y, a continuación, haga clic en **Aceptar**.
   La página **Diario de conciliación de pagos** abre una ventana preparada para la cuenta bancaria seleccionada.
4. Seleccione la acción **Importar transacciones bancarias**.
   Si la cuenta bancaria del diario seleccionado no está configurada para el importe de transacciones bancarias, se abrirá un cuadro de diálogo para ayudarle a rellenar los campos pertinentes.
5. En la página **Seleccionar un archivo para importarlo**, seleccione el archivo que contiene las transacciones bancarias para los pagos que desee conciliar y, a continuación, haga clic en **Abrir**.  
6. Si se ha habilitado el servicio Extracto bancario, en la página **Filtro de extracto bancario** que se abre automáticamente, especifique el intervalo de fechas para que se importen los extractos bancarios.

    La página **Diario de conciliación de pagos** se rellena con líneas para pagos que representan transacciones bancarias en el extracto bancario importado.

    En las líneas de los pagos que se han liquidado automáticamente en sus movimientos pendientes relacionados, el campo **Confianza de la correspondencia** tiene un valor entre **Bajo** y **Alto** para indicar la calidad de la correspondencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Tipo de cuenta** y **N.º de cuenta** se rellenan con información sobre el cliente o el proveedor en el que se ha liquidado el pago.
7. Seleccione una línea de diario y, a continuación, seleccione la acción **Liquidar manualmente** para revisar, volver a liquidar o liquidar el pago manualmente en la página **Liquidación de pago**. Para obtener más información, vea [Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

    Cuando termine la liquidación manual, el campo **Confianza de la correspondencia** en la línea de diario que ha procesado manualmente contendrá la palabra **Aceptado**.
8. Seleccione una línea de diario desliquidado para un recibo de gasto o cobro periódico, como el de repostar gasolina y, a continuación, elija la acción **Asignar texto a cuenta**. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Cuando haya terminado con la asignación de texto de pago a las cuentas, seleccione la acción **Liquidar manualmente**.
10. Si está seguro de que todos los pagos en las líneas de diario se han liquidado correctamente, o se han establecido para un registro directo, seleccione la acción **Registrar** y elija una de las opciones:

    - **Registrar pagos y conciliar bancos**: para registrar los pagos como liquidados y cerrar los movimientos bancarios de la cuenta relacionada como reconciliados.
    - **Registrar solamente pagos**: para publicar solo los pagos como liquidados pero dejar abiertos los movimientos bancarios de cuentas bancarias relacionadas. Se requiere que concilie el banco por separado, por ejemplo: Para obtener más información, consulte [Conciliar el banco](bank-how-reconcile-bank-accounts-separately.md).
    - **Informe de prueba**: para revisar el resultado del registro antes de registrar. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en la parte inferior de la página **Diario de conciliación de pagos**.

Cuando se registra el diario de conciliación de pago, los abonos de movimientos pendientes liquidados se cierran y las cuentas de cliente, de proveedor o de contabilidad relacionadas se actualizan. En el caso de los pagos en las líneas de diario basados en la asignación de texto a cuenta, se actualizan las cuentas de cliente, proveedor y contabilidad especificadas. Para todas las líneas de diario, se crean movimientos de banco. Si selecciona la acción **Registrar pagos y conciliar banco**, todas las cuenta abiertas relacionadas con los movimientos de los clientes o los proveedores se cerrarán. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Puede comparar el valor del campo **Saldo en cuenta bancaria después del registro** con el valor del campo **Saldo final extracto** para hacer un seguimiento cuando la cuenta bancaria se concilie según los pagos registrados.

> [!NOTE]  
>   Si no desea conciliar la cuenta bancaria de la página **Diario de conciliación de pagos**, debe usar la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
