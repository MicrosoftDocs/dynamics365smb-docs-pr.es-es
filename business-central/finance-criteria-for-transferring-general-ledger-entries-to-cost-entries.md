---
title: Criterios para la transferencia de movimientos de contabilidad a movimientos de coste | Documentos de Microsoft
description: Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de coste. Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 62d19b5ff112871f7f44f0945bdcfd38306ed8b3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242818"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="ef1e6-104">Criterios para la transferencia de movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="ef1e6-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="ef1e6-105">Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="ef1e6-106">Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="ef1e6-107">Se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="ef1e6-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="ef1e6-108">Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="ef1e6-109">Los movimientos tienen valores de dimensión que corresponden a un centro de coste y a un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="ef1e6-110">Para estos movimientos, el centro de coste tiene preferencia.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="ef1e6-111">Esto ayuda a evitar una situación en la que un tipo de coste aparece en un objeto de coste y un centro de coste y por lo tanto se cuenta dos veces en estadísticas.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="ef1e6-112">El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="ef1e6-113">Los movimientos se transfieren a un tipo de coste que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="ef1e6-114">No se transfieren los movimientos de contabilidad si:</span><span class="sxs-lookup"><span data-stu-id="ef1e6-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="ef1e6-115">Los movimientos tienen valores de dimensión que no corresponden a un centro de coste ni a un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="ef1e6-116">Los movimientos tienen un importe de cero.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="ef1e6-117">Los movimientos tienen una cuenta de contabilidad que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="ef1e6-118">Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="ef1e6-119">Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de coste asignado.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="ef1e6-120">Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="ef1e6-121">Los movimientos se registraron con una fecha de cierre.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="ef1e6-122">Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.</span><span class="sxs-lookup"><span data-stu-id="ef1e6-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef1e6-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ef1e6-123">See Also</span></span>  
[<span data-ttu-id="ef1e6-124">Contabilidad para costes</span><span class="sxs-lookup"><span data-stu-id="ef1e6-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="ef1e6-125">[Transferir movimientos de contabilidad a movimientos de coste](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ef1e6-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="ef1e6-126">[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ef1e6-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="ef1e6-127">Acerca de la contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="ef1e6-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="ef1e6-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef1e6-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
