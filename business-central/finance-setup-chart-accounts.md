---
title: Configurar un plan contable
description: Puede cambiar las cuentas predeterminadas en el plan de cuentas (COA) y puede agregar nuevas cuentas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 901650c2ed61867cdcccd093d54b10fe24ce30a9
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2911076"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configurar o cambiar el plan de cuentas
El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.
Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas. 
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9]


## <a name="adding-or-changing-accounts"></a>Agregar o cambiar cuentas
Desde el plan de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración.

> [!NOTE]  
>   Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  
>  
>   * El saldo de la cuenta debe ser cero.  
>   * El campo **Permite borrar ctas. anteriores a** se debe configurar en la página **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
>   * Si se selecciona el campo **Chequear uso ctas. cont.** en la página **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.  

## <a name="see-also"></a>Consulte también
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
