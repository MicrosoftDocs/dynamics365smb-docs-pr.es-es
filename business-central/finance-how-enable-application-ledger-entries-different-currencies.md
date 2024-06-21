---
title: Liquidar movimientos en distintas divisas
description: 'Puede liquidar movimientos en varias divisas, por ejemplo, si vende a un cliente en una divisa y cobra en otra.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, payment, reconcile'
ms.search.form: '148, 460, 25'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Permitir la liquidación de movimientos de cliente en distintas divisas

Si se realiza una compra a un proveedor en una divisa y se emite el pago en otra divisa, es posible liquidar la compra con el pago.

De igual modo, si vende a un cliente en una divisa y cobra en otra, puede liquidar el pago con la factura de venta.

El procedimiento siguiente describe cómo configurarlo para movimientos de proveedor en la página **Configuración de compras y pagos**. La configuración es similar para los movimientos de cliente en la página **Configuración de ventas y cobros**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Para permitir la liquidación de movimientos de proveedor en divisas distintas

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de compras y pagos** y luego elija el enlace relacionado.
2. En el campo **Liquidación entre divisas**, seleccione una de las siguientes opciones.

| Opción | Descripción |
| --- | --- |
| Ninguno |No se permite la liquidación entre divisas. |
| UME |Se permite la liquidación entre divisas de la UME. |
| Todo |Se permite la liquidación entre todas las divisas. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Para configurar cuentas para liquidar diferencias de redondeo en divisa

Si liquida movimientos en varias divisas distintas, debe configurar las cuentas en las que se registrarán las diferencias de redondeo.  

> [!NOTE]  
> Primero debe configurar las cuentas contables antes de completar la tarea. Para obtener más información, consulte [Descripción del libro mayor y plan de cuentas](finance-general-ledger.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro cliente** y luego elija el enlace relacionado.  
2. En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.  
3. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro proveedor**, y luego elija el enlace relacionado.  
4. En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.  

## <a name="see-also"></a>Consulte también .

[Administrar pagos](payables-manage-payables.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
