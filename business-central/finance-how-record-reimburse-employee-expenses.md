---
title: Registrar y reembolsar gastos empresariales de los empleados
description: Registre los gastos de los empleados con el diario general en la cuenta del empleado y luego registre un pago a la cuenta bancaria del empleado para reembolsar el gasto relacionado con el negocio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184404"
---
# <a name="record-and-reimburse-employees-expenses"></a>Registro y reembolso de los costes de los empleados

[!INCLUDE[prod_short](includes/prod_short.md)] soporta transacciones para empleados de una manera similar a los proveedores. En consecuencia, existen grupos de contabilización de empleados para asegurarse de que las entradas del libro mayor de empleados se registran en las cuentas relevantes del libro mayor.

> [!NOTE]  
> Las transacciones de empleado se pueden registrar únicamente en la divisa local. Los pagos de reembolso a los empleados no son compatibles con los descuentos y las tolerancias de pago.

Si los empleados gastan su propio dinero durante las actividades comerciales, puede registrar el gasto en la cuenta del empleado. De este modo, puede reembolsar al empleado mediante un pago a su cuenta bancaria, del mismo modo que paga a los proveedores.  

> [!TIP]
> En este artículo se explica cómo registrar el gasto en los libros y cómo reembolsar al empleado. Su organización puede tener un portal o aplicación donde los empleados pueden enviar sus informes de gastos.

[!INCLUDE [prod_short](includes/prod_short.md)] es lo suficientemente flexible como para adaptarse a muchas prácticas diferentes. Los números de cuenta exactos que se utilizarán dependen de la configuración y los procesos de su organización.  

## <a name="to-record-an-employees-expense"></a>Registrar el gasto de un empleado

Puede registrar los costes de los empleados en la página **Diario general**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diarios generales** y luego elija el enlace relacionado.  
2. Abra la sección del diario general correspondiente. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. En una línea nueva de diario, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Repita el paso 3 para todos los gastos que el empleado ha incurrido.

    > [!TIP]  
    > Si desea introducir varias líneas de gastos sobre una línea de cuenta de contrapartida para la cuenta bancaria del empleado, seleccione la casilla de verificación **Sugerir importe de compensación** en la línea de la sección en la página **Secciones diario general**. El campo **Importe** de la línea de la cuenta de contrapartida se rellena previamente de forma automática con el valor que se requiere para compensar los gastos.
5. Seleccione la acción **Registrar** para registrar gastos de la cuenta del empleado.

## <a name="to-reimburse-an-employee"></a>Reembolsar al empleado

Reembolse a los empleados mediante pagos a su cuenta bancaria en la página **Diario de pagos**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Abra la sección del diario de pagos correspondiente. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. Rellene los campos según sea necesario. Para obtener más información, consulte [Creación de pagos](payables-make-payments.md).
4. Opcionalmente, elija la acción **Proponer pagos a empleados** para insertar automáticamente las líneas de diario para los reembolsos pendientes del empleado.
5. Seleccione la acción **Registrar** para registrar el reembolso.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Conciliar reembolsos con movimientos de empleado

Aplique los pagos de los empleados a las entradas del libro mayor relacionadas, de la misma manera que lo hace para los pagos a proveedores, por ejemplo, en la página **Diario de conciliación de pagos**, en función de las entradas del extracto bancario relacionadas. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md). Opcionalmente, puede liquidar manualmente en la página **Movimientos de los empleados**. Para obtener más información, consulte la sección [Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md) relacionada.  

## <a name="see-also"></a>Consulte también

[Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]