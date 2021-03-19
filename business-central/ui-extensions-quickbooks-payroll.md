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
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="cb0f8-103">Extensión de importación del archivo de nóminas de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="cb0f8-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="cb0f8-104">Use la extensión de Importación del archivo de nómina de QuickBooks para importar transacciones de nómina de QuickBooks a cuentas de contabilidad en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cb0f8-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cb0f8-105">Por ejemplo, esto es útil cuando está haciendo la transición de QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)], o si subcontrata su nómina pero también desea realizar un seguimiento de ella en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cb0f8-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="cb0f8-106">Pasos para importar datos de nómina</span><span class="sxs-lookup"><span data-stu-id="cb0f8-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="cb0f8-107">El primer paso es que usted, o su contable, utilice las funciones de exportación en QuickBooks para exportar los datos de la nómina a un archivo .IIF.</span><span class="sxs-lookup"><span data-stu-id="cb0f8-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="cb0f8-108">El segundo paso es abrir la página **Diarios generales** en [!INCLUDE[prod_short](includes/prod_short.md)] y usar la acción **Importar transacciones de nómina** para importar el archivo.</span><span class="sxs-lookup"><span data-stu-id="cb0f8-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="cb0f8-109">Durante el proceso de importación debe asignar las cuentas de contabilidad de QuickBooks a las cuentas correspondientes en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cb0f8-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cb0f8-110">Por último, registre operaciones de nóminas en [!INCLUDE[prod_short](includes/prod_short.md)] según la asignación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="cb0f8-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="cb0f8-111">Para obtener más información, vea [Importar transacciones de nómina](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="cb0f8-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cb0f8-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cb0f8-112">See Also</span></span>
<span data-ttu-id="cb0f8-113">[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="cb0f8-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="cb0f8-114">[Finanzas](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="cb0f8-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="cb0f8-115">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb0f8-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]