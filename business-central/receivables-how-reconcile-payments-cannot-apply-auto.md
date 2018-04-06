---
title: "Usar la característica Transferir diferencia a cuenta para conciliar pagos | Documentos de Microsoft"
description: "Describe cómo procesar los pagos que no se pueden aplicar a un documento, por ejemplo, cuando un tipo de cambio provoca que los importes sean distintos."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 10ef6ae09c6c568cc1281b67e915ae80f9d26e8e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a>Conciliar pagos que no se pueden liquidar automáticamente
En ocasiones es posible que tenga que gestionar los pagos en su cuenta bancaria que no se pueden liquidar con un cliente, proveedor o movimiento de cuenta bancario abierto relacionado. Los motivos pueden ser que no haya ningún documento en [!INCLUDE[d365fin](includes/d365fin_md.md)] con el que se pueda liquidar el pago o el documento relacionado en [!INCLUDE[d365fin](includes/d365fin_md.md)] tiene un importe diferente al de la transacción, por ejemplo, debido al tipo de cambio de divisa. En la ventana **Diario de conciliación de pagos**, todos los importes de transacciones de pagos que aún no se hayan liquidado aparecen en el campo **Diferencia**, incluidos los importes que no se pueden liquidar debido a los motivos que aparecen anteriormente.

Los pagos que no se pueden liquidar pueden aparecer en líneas de diario de conciliación de las distintas formas siguientes:

* El valor del campo **Diferencia** es igual al valor del campo **Importe de transacción**, que indica que no se puede liquidar ninguna parte del pago con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado.
* El valor del campo **Diferencia** es inferior al valor del campo **Importe de transacción**, que indica que no se puede liquidar ninguna parte del pago con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado. La parte del pago restante no se puede liquidar y se debe conciliar manualmente o registrándola directamente en una cuenta.

Para conciliar esos pagos, puede seleccionar el botón **Transferir diferencia a cuenta** y especificar en qué cuenta se registrará el importe del campo **Diferencia** al registrar el diario de conciliación de pagos.

> [!TIP]  
>   Existen funciones similares para configurar la conciliación automática de pagos periódicos que no se pueden liquidar con el cliente, proveedor o movimiento de cuenta bancaria abierto relacionado. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Para conciliar pagos que no se pueden liquidar
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de conciliación de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Abra un diario de conciliación de pagos. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).
3. Seleccione **Transferir diferencia a cuenta**. Se abre la ventana **Transferir diferencia a cuenta**.
4. En el campo **Tipo de cuenta**, especifique el tipo de cuenta en el que se registrará el importe del pago.
5. En el campo **Nº de cuenta**, especifique la cuenta en la que se registrará el importe del pago.
6. En el campo **Descripción**, especifique el texto que describe este registro de pago directo. Por omisión, se inserta el texto del campo **Texto de la transacción** en la línea de diario de conciliación de pagos.
7. Elija el botón **Aceptar**.

Si el valor del campo **Diferencia** era igual al valor del campo **Importe de la transacción** cuando registró el diario de conciliación de pagos, el pago completo de la línea de diario se registrará directamente en la cuenta de contrapartida especificada.

Si el valor del campo **Diferencia** era inferior al valor del campo **Importe de la transacción**, se creará una línea de diario adicional con el mismo texto y fecha y con la diferencia insertada en el campo **Importe de la transacción**. En la línea del diario original, la diferencia se deducirá del valor del campo **Importe de la transacción** y el pago se liquidará con el cliente, proveedor o movimiento de cuenta bancaria relacionado. Cuando registre el diario de conciliación de pagos, se registrará una parte del pago como un pago liquidado. La otra parte del pago se registrará directamente en la cuenta especificada.

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

