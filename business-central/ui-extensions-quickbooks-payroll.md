---
title: "Usar la extensión de importación del archivo de nóminas de Quickbooks | Documentos de Microsoft"
description: "Describe cómo utilizar la extensión para importar transacciones de salario y nóminas desde el servicio Quickbooks Payroll."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ae9331c229c3af644459c31dc154e5eb51eecbbf
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="f50b0-103">Extensión de importación del archivo de nóminas de Quickbooks</span><span class="sxs-lookup"><span data-stu-id="f50b0-103">The Quickbooks Payroll File Import Extension</span></span>
<span data-ttu-id="f50b0-104">Para contabilizar los pagos de salario y transacciones relacionadas, deberá importar y registrar las transacciones financieras de salario creadas para el proveedor de nóminas al libro mayor.</span><span class="sxs-lookup"><span data-stu-id="f50b0-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="f50b0-105">Para hacer esto, primero importe un archivo que recibirá del proveedor de nóminas en la ventana **Diario general**.</span><span class="sxs-lookup"><span data-stu-id="f50b0-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="f50b0-106">A continuación asigne las cuentas externas del archivo de nóminas a las cuentas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f50b0-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="f50b0-107">Por último, registre operaciones de nóminas según la asignación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="f50b0-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="f50b0-108">Para obtener más información, vea [Importar transacciones de nómina](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="f50b0-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="f50b0-109">La extensión de importación del archivo de nóminas de Quickbooks le permite importar la transacción del servicio de nóminas de Quickbooks.</span><span class="sxs-lookup"><span data-stu-id="f50b0-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="f50b0-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f50b0-110">See Also</span></span>
<span data-ttu-id="f50b0-111">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="f50b0-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="f50b0-112">[Finanzas](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="f50b0-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="f50b0-113">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f50b0-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

