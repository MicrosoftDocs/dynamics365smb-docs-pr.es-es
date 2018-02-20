---
title: Configurar los valores de campo sugeridos | Documentos de Microsoft
description: "Para evitar cálculos manuales y completar rápidamente y de forma precisa las tareas, puede configurar la entrada de datos automática de forma que Finance and Operations, Business edition rellene los campos seleccionados."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e9134b3d5fc62fb510b27db5fcbaa71e54b2b97a
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="letting-included365finincludesd365finmdmd-suggest-values"></a>Permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] proponga valores
[!INCLUDE[d365fin](includes/d365fin_md.md)]  puede ayudarle a completar las tareas más rápida y correctamente rellenando previamente los campos o las líneas completas con los datos que, de no ser así, debería calcular e introducir usted. Aunque los datos introducidos automáticamente son siempre correctos, puede cambiarlos si lo desea.

La funcionalidad que introduce los valores del campo por usted, normalmente, se ofrece mediante tareas en las que se introducen grandes volúmenes de datos transaccionales y se desea evitar errores y ahorrar tiempo. Este tema contiene una selección de éstas funcionalidades. Se agregarán más secciones en futuras actualizaciones de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Casilla **Sugerir importe de compensación** en la ventana **Secciones diario general**
Cuando, por ejemplo, está introduciendo en el diario general las líneas para los gastos múltiples que deben registrarse en la misma cuenta bancaria y, a continuación, introduce una nueva línea en el diario para un gasto, puede tener el campo **Importe** en la línea de la cuenta bancaria automáticamente actualizado en el importe que balanza los gastos. Para obtener más información sobre trabajar con diarios generales, vea [Trabajar con diarios generales](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Para tener el campo **Importe** en la contrapartida de las líneas del diario general rellenado automáticamente
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios generales** y elija el vínculo relacionado.
2. En la línea que aparece el proceso de su diario general preferido, seleccione la casilla **Sugerir importe de compensación**.
3. Abra el diario general y registre las transacciones usando la funcionalidad descrita para la inserción automática del valor de un campo.       

Para obtener información acerca de cómo configurar un proceso personal del diario general, por ejemplo, para el control de gastos, vea [Trabajar con diarios generales](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Campo **Rellenar fecha de recepción automáticamente** en la ventana **Registro de pago**
La ventana **Registro de pago** muestra los pagos entrantes pendientes como líneas que representan los documentos de venta donde se debe un importe para el pago. Para obtener más información acerca de liquidar los pagos de clientes, consulte [Conciliar manualmente pagos de cliente desde una lista de documentos de ventas sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Sus principales acciones en la ventana son rellenar la casilla de **Pago realizado** y el campo **Fecha recepción**. Puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para que introduzca la fecha del trabajo automáticamente en el campo **Fecha recepción** cuando selecciona la casilla de verificación **Pago realizado**.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Para tener el campo **Fecha recepción** rellenado automáticamente en la ventana **Registro de pago**
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de registro de pago** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la casilla **Rellenar automáticamente fecha recepción**.
3. Abra la ventana **Registro de pago** y procese los pagos de cliente entrantes usando la funcionalidad descrita para introducir un valor de un campo automáticamente.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finanzas](finance.md)

