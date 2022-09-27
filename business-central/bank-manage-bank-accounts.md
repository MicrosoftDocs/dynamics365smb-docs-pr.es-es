---
title: Administrar cuentas bancarias
description: Debe reconciliar regularmente los movimientos de banco con las transacciones bancarias relacionadas en sus cuentas bancarias.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.search.form: 377, 378, 165, 1284
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 352304983b331d361947d88fdafc134d50fe70a3
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530897"
---
# <a name="manage-and-reconcile-your-bank-accounts"></a>Administre y concilie sus cuentas bancarias

Se debe completar una conciliación de banco a intervalos regulares para todos sus bancos para garantizar que los registros de caja de la empresa sean correctos. Para ello, compare y haga corresponder los movimientos en sus bancos internos con las transacciones bancarias en su banco, y luego registre los saldos en sus bancos internos para que los totales estén disponibles para los directores financieros. La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.

Puede realizar la tarea por separado del proceso de pagos, en la página **Conciliación banco** donde hace corresponder (concilia) líneas del extracto de cuenta en el panel izquierdo con los movimientos de banco interno en el panel derecho. Alternativamente, puede realizar esta tarea en la página **Diario de conciliación de pagos** como parte del procesamiento de pagos que están representados en un extracto de cuenta. En ambas páginas, puede completar la información del extracto de cuenta mediante la importación de un archivo o de una fuente y puede usar sugerencias de coincidencia automática.

> [!NOTE]  
> En las versiones de EE. UU., también puede realizar las conciliaciones bancarias en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario. Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.

Para poder gestionar sus bancos en [!INCLUDE[prod_short](includes/prod_short.md)], debe configurar cada banco como una ficha de banco. Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos. Para obtener más información, consulte [Configurar bancos](bank-setup-banking.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Concilie los bancos como una tarea independiente en la página **Conciliación banco**. |[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md) |
| Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la página **Diario de conciliación de pagos**. |[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Use la conciliación bancaria para ayudar a comprobar que sus libros estén actualizados y no publique la conciliación hasta que esté satisfecho con la conciliación.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/reconcile-bank-accounts-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también

[Configurar banca](bank-setup-banking.md)  
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Transferir fondos bancarios](bank-how-transfer-bank-funds.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
