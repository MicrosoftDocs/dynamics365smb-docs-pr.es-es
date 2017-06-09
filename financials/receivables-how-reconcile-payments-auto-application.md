---
title: "Conciliar pagos usando la liquidación automática | Documentos de Microsoft"
description: "Conciliar pagos con liquidación automática"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 423b141969c131688542cc10bb5361085f247a68
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-payments-using-automatic-application"></a>Conciliar pagos con liquidación automática
La ventana **Diario de conciliación de pagos** especifica pagos, bien entrantes de clientes o salientes a proveedores, que se han registrado como transacciones en la cuenta bancaria en línea y que puede liquidar a sus clientes, vendedores y movimientos de la cuenta pendientes. Las líneas del diario se rellenan importando un extracto bancario como una fuente o un archivo de banco.

Un diario de conciliación de pago está relacionado con una cuenta bancaria en [!INCLUDE[d365fin](includes/d365fin_md.md)] que refleja la cuenta bancaria en línea donde se registran las transacciones de pago. Todas las cuenta abiertas relacionada con los movimientos de los clientes o los proveedores se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Si desea importar tanto extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio de fuentes de banco de Envestnet Yodlee y, a continuación, vincular la cuenta bancaria a la cuentas bancaria en línea relacionada. El diario de conciliación de pagos detectará automáticamente las fuentes de banco cuando seleccione la acción **Importar transacciones de banco**. Además, puede configurar una cuenta bancaria para que importe nuevas fuentes de extractos bancarios cada hora. No se importarán las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados. Para obtener más información, vea [Procedimiento: Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Con la acción **Asignar texto a cuenta** puede configurar asignaciones entre el texto de los pagos y la cuentas de débito, crédito y saldo específicas para que los pagos se contabilicen en las cuentas específicas cuando contabilices el diario de conciliación de pagos. Consulte el paso 8. Para más información, consulte [Procedimiento: Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

La funcionalidad similar existe para conciliar el exceso de importes en las líneas del diario de conciliación de pagos sobre una base ad hoc. Para obtener más información, vea [Procedimiento: Conciliar pagos que no pueden liquidarse](receivables-how-reconcile-payments-cannot-apply-auto.md)

La función **Liquidar automáticamente** se usa automáticamente cuando se importa una fuente o un archivo bancario con transacciones de pago, o cuando se activa para liquidar pagos en sus movimientos pendientes relacionados basándose en una correspondencia de datos en una línea de diario con datos en uno o varios movimientos pendientes.

En las líneas de diario donde un pago se ha liquidado automáticamente a un movimiento pendiente o varios, el campo **Confianza de la correspondencia** tiene un valor entre Baja y Alta para indicar la calidad de la correspondencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Tipo cta.** y **N.º cuenta** se rellenan con información sobre el cliente o el proveedor para el que se liquidó el pago. Si ha configurado una asignación de texto a cuenta, la liquidación automática puede dar como resultado un valor de confianza de correspondencia **Alta: asignación de texto a cuenta**.

Para cada línea de diario en la ventana **Diario de conciliación de pagos** podrá abrir la ventana **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la correspondencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se aplicaron automáticamente en un movimiento incorrecto. Para obtener más información, vea [Procedimiento: Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

**Nota**: Puede iniciar la importación de las transacciones bancarias al mismo tiempo que abre la ventana **Conciliación de pagos** para un diario de conciliación de pagos existente en la ventana **Diarios de conciliación de pago**. El procedimiento siguiente describe cómo importar transacciones bancarias a la ventana **Diario de conciliación de pagos** una vez creado un nuevo diario.

## <a name="to-reconcile-payments-using-automatic-application"></a>Para conciliar los pagos con liquidación automática
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Diarios de conciliación de pagos** y elija el vínculo relacionado.
2. Para trabajar en un nuevo diario de conciliación de pago, seleccione la acción **Nuevo diario**.
3. En la ventana **Lista cuentas bancarias pago**, seleccione la cuenta bancaria que desee conciliar los pagos y, a continuación, haga clic en **Aceptar**.
   La ventana **Diario de conciliación de pagos** abre una ventana preparada para la cuenta bancaria seleccionada.
4. Seleccione la acción **Importar transacciones bancarias**.
   Si la cuenta bancaria del diario seleccionado no está configurada para el importe de transacciones bancarias, se abrirá un cuadro de diálogo para ayudarle a rellenar los campos pertinentes.
5. En la ventana **Seleccionar un archivo para importarlo**, seleccione el archivo que contiene las transacciones bancarias para los pagos que desee conciliar y, a continuación, haga clic en **Abrir**.  
6. Si se ha habilitado el servicio Extracto bancario, en la ventana **Filtro de extracto bancario** que se abre automáticamente, especifique el intervalo de fechas para que se importen los extractos bancarios.

    La ventana **Diario de conciliación de pagos** se rellena con líneas para pagos que representan transacciones bancarias en el extracto bancario importado.

    En las líneas de los pagos que se han liquidado automáticamente en sus movimientos pendientes relacionados, el campo **Confianza de la correspondencia** tiene un valor entre **Bajo** y **Alto** para indicar la calidad de la correspondencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Tipo cta.** y **N.º cuenta** se rellenan con información sobre el cliente o el proveedor para el que se liquidó el pago.
7. Seleccione una línea de diario y, a continuación, seleccione la acción **Liquidar manualmente** para revisar, volver a liquidar o liquidar el pago manualmente en la ventana **Liquidación de pago**. Para obtener más información, vea [Procedimiento: Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

    Cuando termine la liquidación manual, el campo **Confianza de la correspondencia** en la línea de diario que ha procesado manualmente contendrá la palabra **Aceptado**.
8. Seleccione una línea de diario desliquidado para un recibo de gasto o cobro periódico, como el de repostar gasolina y, a continuación, elija la acción **Asignar texto a cuenta**. Para más información, consulte [Procedimiento: Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Cuando haya terminado con la asignación de texto de pago a las cuentas, seleccione la acción **Liquidar manualmente**.
10. Si está seguro de que todos los pagos en las líneas de diario se han liquidado correctamente, o se han establecido para un registro directo, seleccione la acción **Registrar**.

Cuando se registra el diario de conciliación de pago, los abonos de movimientos pendientes liquidados se cierran y las cuentas de cliente, de proveedor o de contabilidad relacionadas se actualizan. En el caso de los pagos en las líneas de diario basados en la asignación de texto a cuenta, se actualizan las cuentas de cliente, proveedor y contabilidad especificadas. Para todas las líneas de diario, se crean movimientos de banco. Si selecciona la acción **Registrar pagos y conciliar banco**, todas las cuenta abiertas relacionadas con los movimientos de los clientes o los proveedores se cerrarán. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Puede comparar el valor del campo **Saldo en cuenta bancaria después del registro** con el valor del campo **Saldo final extracto** para hacer un seguimiento cuando la cuenta bancaria se concilie según los pagos registrados.

**Nota**: Si no desea conciliar la cuenta bancaria de la ventana **Diario de conciliación de pagos**, debe usar la ventana **Conciliación banco**. Para obtener más información, vea [Conciliar cuentas bancarias por separado](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

