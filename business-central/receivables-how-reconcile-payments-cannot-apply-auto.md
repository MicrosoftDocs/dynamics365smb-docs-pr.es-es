---
title: Usar la característica Transferir diferencia a cuenta para conciliar pagos
description: 'Describe cómo procesar los pagos que no se pueden aplicar a un documento, por ejemplo, cuando un tipo de cambio provoca que los importes sean distintos.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Conciliar pagos que no se pueden liquidar automáticamente
En ocasiones es posible que tenga que gestionar los pagos en su cuenta bancaria que no se pueden liquidar con un cliente, proveedor o movimiento de cuenta bancario abierto relacionado. Los motivos pueden ser que no haya ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)] con el que se pueda liquidar el pago o el documento relacionado en [!INCLUDE[prod_short](includes/prod_short.md)] tiene un importe diferente al de la transacción, por ejemplo, debido al tipo de cambio de divisa. En la página **Diario de conciliación de pagos**, todos los importes de transacciones de pagos que aún no se hayan liquidado aparecen en el campo **Diferencia**, incluidos los importes que no se pueden liquidar debido a los motivos que aparecen anteriormente.

Los métodos para resolver este tipo de pagos no aplicados son los siguientes:
* Aplicar manualmente
* Usar la asignación de texto a cuenta
* Transferir una cantidad en exceso a una línea de diario para crear y registrar la entrada requerida, como un reembolso de un pago en exceso.

Los pagos que no se pueden liquidar pueden aparecer en líneas de diario de conciliación de las distintas formas siguientes:

* El valor del campo **Diferencia** es igual al valor del campo **Importe de transacción**, que indica que no se puede liquidar ninguna parte del pago con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado.
* El valor del campo **Diferencia** es inferior al valor del campo **Importe de transacción**, que indica que no se puede liquidar ninguna parte del pago con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado. La parte del pago restante no se puede liquidar y se debe conciliar manualmente o registrándola directamente en una cuenta.

Para conciliar esos pagos, puede seleccionar la acción **Transferir diferencia a cuenta** y especificar entonces en qué cuenta se registrará el importe del campo **Diferencia** al registrar el diario de conciliación de pagos. Puede hacer esto desde la página **Diario de conciliación de pagos** o desde la página **Revisión de aplicación de pagos** que se abre eligiendo el valor en el campo **Confianza de la correspondencia** o eligiendo el campo **Diferencia**.

> [!TIP]  
>   Existen funciones similares para configurar la conciliación automática de pagos periódicos que no se pueden liquidar con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## Para conciliar pagos que no se pueden liquidar automáticamente
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de conciliación de pagos** y luego elija el enlace relacionado.
2. Abra un diario de conciliación de pagos. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).
3. Seleccione **Transferir diferencia a cuenta**. Se abre la página **Transferir diferencia a cuenta**.
4. En el campo **Tipo de cuenta**, especifique el tipo de cuenta en el que se registrará el importe del pago.
5. En el campo **Nº de cuenta**, especifique la cuenta en la que se registrará el importe del pago.
6. En el campo **Descripción**, especifique el texto que describe este registro de pago directo. Por omisión, se inserta el texto del campo **Texto de la transacción** en la línea de diario de conciliación de pagos.
7. Elija el botón **Aceptar**.

Si el valor del campo **Diferencia** era igual al valor del campo **Importe de la transacción** cuando registró el diario de conciliación de pagos, el pago completo de la línea de diario se registrará directamente en la cuenta de contrapartida especificada.

Si el valor del campo **Diferencia** era inferior al valor del campo **Importe de la transacción**, se creará una línea de diario adicional con el mismo texto y fecha y con la diferencia insertada en el campo **Importe de la transacción**. En la línea del diario original, la diferencia se deducirá del valor del campo **Importe de la transacción** y el pago se liquidará con el cliente, proveedor o movimiento de cuenta bancaria relacionado. Cuando registre el diario de conciliación de pagos, se registrará una parte del pago como un pago liquidado. La otra parte del pago se registrará directamente en la cuenta especificada.

## Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]