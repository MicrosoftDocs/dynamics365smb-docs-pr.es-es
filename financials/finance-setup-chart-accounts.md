---
title: Configurar el plan de cuentas | Documentos de Microsoft
description: "Describe cómo puede modificar el plan de cuentas."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configurar o cambiar el plan de cuentas
El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.
Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.  

## <a name="adding-or-changing-accounts"></a>Agregar o cambiar cuentas
Desde el plan de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración.

**Nota**: Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  

* El saldo de la cuenta debe ser cero.  
* El campo **Permite borrar ctas. anteriores a** se debe configurar en la ventana **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
* Si se selecciona el campo **Chequear uso ctas. cont.** en la ventana **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.  

## <a name="see-also"></a>Consulte también
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Dimensiones](finance-dimensions.md)  
[Importar desde otros sistemas financieros](upload-data.md)  
[Trabajar con los códigos GIFI en Canadá](ca-finance-work-gifi-codes.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
