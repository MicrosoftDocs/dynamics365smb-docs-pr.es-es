---
title: "Usar la extensión de importación del archivo de nóminas de Quickbooks | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para importar transacciones de salario y nóminas desde el servicio Quickbooks Payroll."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b719a7d2b6b5590ae63920b63aaba8c2313a8661
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-for-financials"></a><span data-ttu-id="8594f-103">La extensión de importación del archivo de nóminas de QuickBooks a Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="8594f-103">The Quickbooks Payroll File Import Extension to Dynamics 365 for Financials</span></span>
<span data-ttu-id="8594f-104">Para contabilizar los pagos de salario y transacciones relacionadas, deberá importar y registrar las transacciones financieras de salario creadas para el proveedor de nóminas al libro mayor.</span><span class="sxs-lookup"><span data-stu-id="8594f-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="8594f-105">Para hacer esto, primero importe un archivo que recibirá del proveedor de nóminas en la ventana **Diario general**.</span><span class="sxs-lookup"><span data-stu-id="8594f-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="8594f-106">A continuación asigne las cuentas externas del archivo de nóminas a las cuentas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8594f-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="8594f-107">Por último, registre operaciones de nóminas según la asignación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="8594f-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="8594f-108">Para obtener más información, vea [Procedimiento: Importar transacciones de nómina](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8594f-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="8594f-109">La extensión de importación del archivo de nóminas de Quickbooks le permite importar la transacción del servicio de nóminas de Quickbooks.</span><span class="sxs-lookup"><span data-stu-id="8594f-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="8594f-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8594f-110">See Also</span></span>
<span data-ttu-id="8594f-111">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="8594f-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="8594f-112">[Finanzas](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="8594f-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="8594f-113">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8594f-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

