---
title: Registrar gastos o ingresos directamente en contabilidad
description: Puede crear transacciones en la página del diario general para actividades comerciales que no involucran un documento.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Registrar transacciones directamente en la contabilidad general

Puede usar diarios generales para registrar transacciones financieras directamente en cuentas generales y otras cuentas, como cuentas bancarias, de cliente, proveedor y empleado.  

Un uso típico del diario general es contabilizar los gastos de los empleados durante las actividades empresariales para su reembolso. Para obtener más información, consulte [Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md).

Los diarios generales registran las transacciones financieras directamente en cuentas contables y otras cuentas, como bancarias, de clientes, de proveedores y de empleados. Registrar con un diario general crea movimientos en cuentas contables. Las entradas se crean incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro. Puede personalizar la versión de un diario general configurando una sección o una plantilla de diario. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

Los asientos que publica con documentos requieren un proceso de nota de abono. Sin embargo, puede revertir los asientos que contabiliza en el diario general. Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

## Para registrar una transacción directamente en una cuenta contable

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales**, y luego elija el enlace relacionado.
2. Abra el lote del diario general. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. En una línea nueva de diario, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Repita el paso 3 para todas las transacciones que desee registrar.

    > [!TIP]  
    > Si desea introducir varias líneas de transacción sobre una línea de cuenta de contrapartida, por ejemplo, de una cuenta bancaria, seleccione la casilla de verificación **Sugerir importe de compensación** en la línea de la sección en la página **Secciones diario general**. El campo **Importe** de la línea de la cuenta de contrapartida se rellena previamente de forma automática con el valor que se requiere para compensar las transacciones.
5. Seleccione la acción **Registrar** para registrar las transacciones en las cuentas contables especificadas.

## Consulte también

[Trabajar con diarios generales](ui-work-general-journals.md)  
[Registrar y reembolsar los costes de los empleados](finance-how-record-reimburse-employee-expenses.md)  
[Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]