---
title: Usar la extensión de importación del archivo de nóminas de QuickBooks | Documentos de Microsoft
description: En este tema se describe cómo utilizar la extensión para importar transacciones de salario y nóminas desde QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 42514576f7fb9542bbecfbbe8e9ff7996040da9b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311121"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Extensión de importación del archivo de nóminas de QuickBooks
Use la extensión de Importación del archivo de nómina de QuickBooks para importar transacciones de nómina de QuickBooks a cuentas de contabilidad en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, esto es útil cuando está haciendo la transición de QuickBooks a [!INCLUDE[d365fin](includes/d365fin_md.md)], o si subcontrata su nómina pero también desea realizar un seguimiento de ella en [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Pasos para importar datos de nómina
El primer paso es que usted, o su contable, utilice las funciones de exportación en QuickBooks para exportar los datos de la nómina a un archivo .IIF. El segundo paso es abrir la página **Diarios generales** en [!INCLUDE[d365fin](includes/d365fin_md.md)] y usar la acción **Importar transacciones de nómina** para importar el archivo. Durante el proceso de importación debe asignar las cuentas de contabilidad de QuickBooks a las cuentas correspondientes en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por último, registre operaciones de nóminas en [!INCLUDE[d365fin](includes/d365fin_md.md)] según la asignación de cuentas. 

Para obtener más información, vea [Importar transacciones de nómina](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Consulte también
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)    
[Finanzas](finance.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
