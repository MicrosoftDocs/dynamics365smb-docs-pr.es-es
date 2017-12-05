---
title: Registrar y reembolsar gastos empresariales de los empleados | Documentos de Microsoft
description: Registre los gastos de los empleados con el diario general en la cuenta del empleado y luego registre un pago a la cuenta bancaria del empleado para reembolsar el gasto relacionado con el negocio.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: daa014eaa78caa7a317b05ca92ff27c1d1530c06
ms.openlocfilehash: 0e10011c598678134cb7badbd9a3be97751b4424
ms.contentlocale: es-es
ms.lasthandoff: 10/17/2017

---
# <a name="how-to-record-and-reimburse-employees-expenses"></a>Procedimiento: registro y reembolso de los costes de los empleados
[!INCLUDE[d365fin](includes/d365fin_md.md)] soporta transacciones para empleados de una manera similar a los proveedores. En consecuencia, existen grupos de contabilización de empleados para asegurarse de que las entradas del libro mayor de empleados se registran en las cuentas relevantes del libro mayor.

> [!NOTE]  
> Las transacciones de empleado se pueden registrar únicamente en la divisa local. Los pagos de reembolso a los empleados no son compatibles con los descuentos y las tolerancias de pago.

Si los empleados gastan su propio dinero durante las actividades comerciales, puede registrar el gasto en la cuenta del empleado. De este modo, puede reembolsar al empleado mediante un pago a su cuenta bancaria, del mismo modo que paga a los proveedores.

## <a name="to-record-an-employees-expense"></a>Registrar el gasto de un empleado
Puede registrar los costes de los empleados en la ventana **Diario general**.
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios generales** y elija el vínculo relacionado.
2. Abra la sección del diario general correspondiente. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. En una línea nueva de diario, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Repita el paso 3 para todos los gastos que el empleado ha incurrido.

    > [!TIP]  
    > Si desea introducir varias líneas de gastos sobre una línea de cuenta de contrapartida para la cuenta bancaria del empleado, seleccione la casilla de verificación **Sugerir importe de compensación** en la línea de la sección en la ventana **Secciones diario general**. El campo **Importe** de la línea de la cuenta de contrapartida se rellena previamente de forma automática con el valor que se requiere para compensar los gastos.
5. Seleccione la acción **Registrar** para registrar gastos de la cuenta del empleado.

## <a name="to-reimburse-an-employee"></a>Reembolsar al empleado
Reembolse a los empleados mediante pagos a su cuenta bancaria en la ventana **Diario de pagos**.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Abra la sección del diario de pagos correspondiente. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. Rellene los campos según sea necesario. Para obtener más información, consulte [Creación de pagos](payables-make-payments.md).
4. Opcionalmente, elija la acción **Proponer pagos a empleados** para insertar automáticamente las líneas de diario para los reembolsos pendientes del empleado.
5. Seleccione la acción **Registrar** para registrar el reembolso.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Conciliar reembolsos con movimientos de empleado
Aplique los pagos de los empleados a las entradas del libro mayor relacionadas, de la misma manera que lo hace para los pagos a proveedores, por ejemplo, en la ventana **Diario de conciliación de pagos**, en función de las entradas del extracto bancario relacionadas. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md). Opcionalmente, puede liquidar manualmente en la ventana **Movimientos de los empleados**. Para obtener más información, consulte el tema relacionado [Conciliar pagos de proveedor manualmente](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Consulte también
[Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Revertir registros](finance-how-reverse-journal-posting.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

