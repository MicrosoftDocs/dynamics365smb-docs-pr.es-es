---
title: Usar la extensión de importación del archivo de nóminas de QuickBooks | Documentos de Microsoft
description: En este tema se describe cómo utilizar la extensión para importar transacciones de salario y nóminas desde QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fc8767f1e6a33f957b33f9076a8cee485b2f1412
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386379"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Extensión de importación del archivo de nóminas de QuickBooks
Use la extensión de Importación del archivo de nómina de QuickBooks para importar transacciones de nómina de QuickBooks a cuentas de contabilidad en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, esto es útil cuando está haciendo la transición de QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)], o si subcontrata su nómina pero también desea realizar un seguimiento de ella en [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="steps-to-import-payroll-data"></a>Pasos para importar datos de nómina
El primer paso es que usted, o su contable, utilice las funciones de exportación en QuickBooks para exportar los datos de la nómina a un archivo .IIF. El segundo paso es abrir la página **Diarios generales** en [!INCLUDE[prod_short](includes/prod_short.md)] y usar la acción **Importar transacciones de nómina** para importar el archivo. Durante el proceso de importación debe asignar las cuentas de contabilidad de QuickBooks a las cuentas correspondientes en [!INCLUDE[prod_short](includes/prod_short.md)]. Por último, registre operaciones de nóminas en [!INCLUDE[prod_short](includes/prod_short.md)] según la asignación de cuentas. 

Para obtener más información, vea [Importar transacciones de nómina](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Consulte también
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones ](ui-extensions.md)    
[Finanzas](finance.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]