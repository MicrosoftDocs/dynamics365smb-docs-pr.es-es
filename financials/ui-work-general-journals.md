---
title: Trabajar con diarios generales | Documentos de Microsoft
description: "Obtenga información sobre cómo funcionan los diarios generales."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Trabajar con diarios generales
Puede usar diarios generales para registrar transacciones financieras en cuentas generales y otras cuentas, como cuentas bancarias, de cliente y de proveedor. Registrar con un diario general siempre crea movimientos en cuentas contables. Esto es así incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro.

[!INCLUDE[d365fin](includes/d365fin_md.md)] también tiene diarios no financieros, como el diario de productos o el diario de inventario físico, pero estos diarios no están visibles en la interfaz de usuario.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en el diario. Al registrar el diario, la información se transfiere a movimientos en cuentas individuales, donde no se puede modificar. Sin embargo, puede desliquidar los movimientos registrados y puede registrar movimientos de inversión o correctores.

## <a name="journal-templates-and-batches"></a>Secciones y plantillas del diario
Existen varias plantillas de diario general. Cada plantilla de diario se representa mediante una ventana específica con funciones particulares y los campos que se requieren para admitir estas funciones, como la ventana **Diario de conciliación de pagos** para procesar pagos bancarios y la ventana **Diario de pagos** para pagar a sus proveedores.

**Nota**: Si exporta los archivos de pagos al banco desde el diario de pagos, debe activar la casilla **Permitir exportación de pagos** para el proceso de diario en cuestión en la ventana **Secciones diario general**. Para obtener más información, vea [Procedimiento: Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md).

Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Por ejemplo, puede definir su propia sección de diario del diario de pagos que tiene su diseño y configuración personal.

Un ejemplo de una configuración personal que puede definir en su sección de diario general es tener la ayuda del sistema para rellenar los campos de importes. Si marca la casilla **Proponer importe de compensación** en la línea de su sección en la ventana **Secciones diario general**, a continuación, el campo **Importe**, por ejemplo, las líneas de diario general del mismo número de documento se rellena automáticamente con el valor necesario para incluir el saldo del documento. Para obtener más información, vea [Permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] proponga valores](ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Cuentas principales y cuentas de contrapartida
Si ha configurado cuentas de contrapartida predeterminadas para las secciones del diario, la cuenta de contrapartida se rellenará automáticamente cuando rellene el campo **N.º cuenta**. . Si no, rellene los campos **N.º de cuenta** y **N.º cuenta contrapartida** manualmente. Un importe positivo en el campo **Importe** se adeuda en la cuenta principal y se carga en la cuenta de contrapartida. Un importe negativo se carga en la cuenta principal y se adeuda en la cuenta de contrapartida.

**Nota**: El IVA se calcula de manera independiente para la cuenta principal y la cuenta de contrapartida, para que puedan usar diferentes tipos porcentuales de IVA.

## <a name="recurring-journals"></a>Diarios periódicos
Un diario periódico es un diario general con campos especiales para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Al usar estos campos para las transacciones periódicas, puede registrar importes tanto fijos como variables. También puede especificar la movimientos de reversión automática al día siguiente a la fecha de registro y usar claves de asignación con los movimientos periódicos.

## <a name="see-also"></a>Consulte también
[Utilizar claves de asignación en diarios generales](ui-how-use-allocation-keys-general-journals.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

