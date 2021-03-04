---
title: Configurar reglas para la liquidación automática de los pagos
description: En la página Reglas de liquidación de pago, se establecen reglas para determinar el modo en que los pagos/operaciones bancarias deben liquidarse automáticamente en los movimientos pendientes relacionados cuando se utiliza la función Liquidar automáticamente en la página Diario de conciliación de pagos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6ffd2a12d399f0a05517d9e1031df3227aa7248a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758347"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Configurar reglas para la liquidación automática de los pagos

En la página **Reglas de liquidación de pagos**, se establecen reglas para regular el modo en que el texto de pago (en una operación bancaria) se ajusta automáticamente al texto de los movimientos pendientes en los dos procesos siguientes:

- Liquidar automáticamente los pagos de sus facturas pendientes (no pagadas), abonos u otros movimientos relacionados cuando utilice la función **Liquidar automáticamente** en la página **Diario de conciliación de pagos**. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

- Conciliar automáticamente las transacciones bancarias con sus movimientos internos de banco relacionados cuando se selecciona la acción **Conciliar automáticamente** en la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).

Las reglas de liquidación de pagos nuevas se configuran eligiendo qué tipos de datos en una línea de diario de conciliación de pago deben corresponder con datos en uno o varios movimientos pendientes antes de que el pago relacionado se liquide automáticamente en los movimientos pendientes. La calidad de cada liquidación automática se muestra como un valor de **Bajo** a **Alto** en el campo **Confianza de la correspondencia** en la página **Diario de conciliación de pagos**, según la regla de liquidación de pago que se haya utilizado.

Cada fila de la página **Reglas de liquidación de pagos** representa una regla de liquidación de pagos. Las reglas se aplican en el orden especificado por el campo **Orden clasificación**. Si se emplean varias reglas a la vez, se usa en primer lugar la confianza de correspondencia de la regla.

La función de liquidación automática se basa en criterios de correspondencia prioritarios. La función primero intenta, por orden de prioridad, relacionar el texto de los cinco campos **Parte vinculada** de una línea de diario con el texto de banco, el nombre o la dirección de los clientes o proveedores con documentos sin pagar que representan movimientos pendientes. A continuación, la función intenta hacer coincidir el texto de los campos **Texto de la transacción** e **Información adicional de la transacción** en una línea del diario con el texto de los campos **N.º documento externo** y **N.º documento** en los movimientos pendientes. Por último, la función intenta hacer coincidir la cantidad del campo **Importe extracto** de una línea del diario con la cantidad de los movimientos pendientes.

> [!NOTE]
> La correspondencia de texto solo es posible para el texto de más de cuatro caracteres.

Además de los criterios de correspondencia, lo siguiente se aplica en relación con el signo del importe de pago:

- Para importes negativos, la correspondencia se realiza primero contra movimientos pendientes que representan las facturas de cliente y luego contra los abonos de proveedor.
- Para importes positivos, la correspondencia se realiza primero contra movimientos pendientes que representan las facturas de proveedor y luego contra los abonos de cliente.

## <a name="to-set-up-a-payment-application-rule"></a>Para configurar una regla de liquidación de pago
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Reglas de liquidación de pago** y luego elija el enlace relacionado.
2. Defina una regla de liquidación de pago nueva o modificada; para ello, rellene los campos en una línea, tal como se describe en la tabla siguiente.

|Campo|Descripción|
|-|-|
|**Confianza de la correspondencia**|Especifica la confianza en la regla de liquidación que se define en la línea. <br /></br>Según la calidad de la liquidación de pago automático de la línea del diario, un valor que especifica en este campo se muestra en el campo **Confianza de la correspondencia** de la página **Diario de conciliación de pagos**.|
|**Prioridad**|Especifica la prioridad de la regla de aplicación relativa a otras reglas de aplicación que se definen como líneas en la página **Reglas de liquidación de pago**. 1 representa la prioridad más alta.|
|**Parte relacionada conciliada**|Especifica cuánta información sobre el cliente o el proveedor, como dirección, nombre de ciudad y número de cuenta bancaria, en la línea del diario de conciliación del pago debe coincidir con información en el movimiento pendiente antes de que la regla de liquidación se utilice para liquidar automáticamente el pago en el movimiento pendiente.|
|**N.º doc./N.º doc. ext. conciliado**|Especifica si el texto de la línea del diario de conciliación de pagos debe coincidir con el valor de los campos **N.º documento** o **N.º documento externo** que consta en el movimiento pendiente, antes de que la regla de liquidación se use automáticamente para liquidar el pago en el movimiento pendiente.|
|**Tolerancia importe incl. conciliada**|Especifica cuántos movimientos para un cliente o un proveedor deben coincidir con el importe incluida la tolerancia de pago antes de que la regla de liquidación se use para liquidar automáticamente un pago en el movimiento pendiente.|

La tabla siguiente muestra las reglas de liquidación configuradas en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> Las reglas de liquidación de pagos pueden ser distintas en su implementación de [!INCLUDE[prod_short](includes/prod_short.md)].

| Confianza de la correspondencia | Prioridad | Parte relacionada conciliada | N.º doc./N.º doc. ext. conciliado | Tolerancia importe incl. conciliada |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Alta             | 1        | Completamente                 | Sí: múltiple                 | Una instancia                      |
| Alta             | 2        | Completamente                 | Sí: múltiple                 | Múltiples instancias               |
| Alta             | 3        | Completamente                 | Sí                            | Una instancia                      |
| Alta             | 4        | Completamente                 | Sí                            | Múltiples instancias               |
| Alta             | 5        | Parcialmente             | Sí: múltiple                 | Una instancia                      |
| Alta             | 6        | Parcialmente             | Sí: múltiple                 | Múltiples instancias               |
| Alta             | 7        | Parcialmente             | Sí                            | Una instancia                      |
| Alta             | 8        | Completamente                 | No                             | Una instancia                      |
| Alta             | 9        | No                    | Sí: múltiple                 | Una instancia                      |
| Alta             | 10       | No                    | Sí: múltiple                 | Múltiples instancias               |
| Media           | 1        | Completamente                 | Sí: múltiple                 | No contemplado                 |
| Media           | 2        | Completamente                 | Sí                            | No contemplado                 |
| Media           | 3        | Completamente                 | No                             | Múltiples instancias               |
| Media           | 4        | Parcialmente             | Sí: múltiple                 | No contemplado                 |
| Media           | 5        | Parcialmente             | Sí                            | No contemplado                 |
| Media           | 6        | No                    | Sí                            | Una instancia                      |
| Media           | 7        | No                    | Sí: múltiple                   | No contemplado                 |
| Media           | 8        | Parcialmente             | No                             | Una instancia                      |
| Media           | 9        | No                    | Sí                            | No contemplado                 |
| Baja              | 1        | Completamente                 | No                             | Ninguna instancia                     |
| Baja              | 2        | Parcialmente             | No                             | Múltiples instancias               |
| Baja              | 3        | Parcialmente             | No                             | Ninguna instancia                     |
| Baja              | 4        | No                    | No                             | Una instancia                      |
| Baja              | 5        | No                    | No                             | Múltiples instancias               |

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]