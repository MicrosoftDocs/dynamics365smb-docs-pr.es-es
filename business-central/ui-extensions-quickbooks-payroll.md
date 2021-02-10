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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757097"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="f499b-103">Extensión de importación del archivo de nóminas de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="f499b-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="f499b-104">Use la extensión de Importación del archivo de nómina de QuickBooks para importar transacciones de nómina de QuickBooks a cuentas de contabilidad en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f499b-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f499b-105">Por ejemplo, esto es útil cuando está haciendo la transición de QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)], o si subcontrata su nómina pero también desea realizar un seguimiento de ella en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f499b-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="f499b-106">Pasos para importar datos de nómina</span><span class="sxs-lookup"><span data-stu-id="f499b-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="f499b-107">El primer paso es que usted, o su contable, utilice las funciones de exportación en QuickBooks para exportar los datos de la nómina a un archivo .IIF.</span><span class="sxs-lookup"><span data-stu-id="f499b-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="f499b-108">El segundo paso es abrir la página **Diarios generales** en [!INCLUDE[prod_short](includes/prod_short.md)] y usar la acción **Importar transacciones de nómina** para importar el archivo.</span><span class="sxs-lookup"><span data-stu-id="f499b-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="f499b-109">Durante el proceso de importación debe asignar las cuentas de contabilidad de QuickBooks a las cuentas correspondientes en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f499b-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f499b-110">Por último, registre operaciones de nóminas en [!INCLUDE[prod_short](includes/prod_short.md)] según la asignación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="f499b-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="f499b-111">Para obtener más información, vea [Importar transacciones de nómina](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="f499b-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f499b-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f499b-112">See Also</span></span>
<span data-ttu-id="f499b-113">[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="f499b-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="f499b-114">[Finanzas](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="f499b-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="f499b-115">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f499b-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
