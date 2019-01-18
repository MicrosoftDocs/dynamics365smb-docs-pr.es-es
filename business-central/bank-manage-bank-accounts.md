---
title: Administrar cuentas bancarias | Documentos de Microsoft
description: Debe reconciliar regularmente los movimientos de banco con las transacciones bancarias relacionadas en sus cuentas bancarias.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 62b2bf8987146a69d17bd343f88d31d60a205ffb
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="managing-bank-accounts"></a>Administrar cuentas bancarias
A intervalos regulares, debe conciliar sus movimientos bancarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] con las transacciones bancarias relacionadas a cuentas bancarias en su banco y, a continuación, registrar el saldo en su cuenta bancaria. Puede realizar esta tarea, ya sea como parte del procesamiento de los pagos representados en un extracto bancario en el **Diario de conciliación de pagos**. Alternativamente, puede realizar la tarea por separado del proceso de pagos, en la página **Conciliación banco** donde coincide (reconcilia) líneas de extracto bancario en el panel izquierdo con los movimientos de cuenta bancaria internos en el panel derecho. En ambas páginas, puede completar la información del extracto de cuenta mediante la importación de un archivo o de una fuente y puede usar sugerencias de coincidencia automática.

> [!NOTE]  
> En las versiones de EE. UU., también puede realizar las conciliaciones bancarias en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario. Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección "Conciliar cuentas bancarias" en Funcionalidad local para Estados Unidos.

A veces, debe transferir importes entre la cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] para reflejar las transferencias en su cuenta bancaria. Puede realizar esta tarea en la página **Diario general**, de diferentes maneras en función de la divisa de los fondos.

Para poder gestionar las cuentas bancarias, debe configurar cada cuenta bancaria como una ficha de banco. Además, debe configurar los servicios electrónicos que pueda usar para importar extractos bancarios y exportar archivos de pagos. Para obtener más información, consulte [Configurar cuentas bancarias](bank-setup-banking.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Concilie cuentas bancarias relacionadas en relación con el procesamiento de pagos en la página **Diario de conciliación de pagos**. |[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Concilie cuentas bancarias, incluidos los movimientos de cheque, como una tarea independiente en la página **Conciliación de cuentas bancarias**. |[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md) |
| Registre transferencias entre bancos en la misma divisa o en divisas diferentes. |[Transferir fondos bancarios](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Consulte también
[Configurar banca](bank-setup-banking.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Administrar pagos](payables-manage-payables.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

