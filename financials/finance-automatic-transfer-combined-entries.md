---
title: "Transferencia automática y movimientos combinados | Documentos de Microsoft"
description: "En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado. Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste. La siguiente tabla describe las distintas opciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="7bd3a-105">Transferencia automática y movimientos combinados</span><span class="sxs-lookup"><span data-stu-id="7bd3a-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="7bd3a-106">En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="7bd3a-107">Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="7bd3a-108">La siguiente tabla describe las distintas opciones.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="7bd3a-109">Combinar movimientos</span><span class="sxs-lookup"><span data-stu-id="7bd3a-109">Combine entries</span></span>|<span data-ttu-id="7bd3a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bd3a-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="7bd3a-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7bd3a-111">None</span></span>|<span data-ttu-id="7bd3a-112">Cada movimiento de contabilidad se transfiere individualmente al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="7bd3a-113">Día</span><span class="sxs-lookup"><span data-stu-id="7bd3a-113">Day</span></span>|<span data-ttu-id="7bd3a-114">Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="7bd3a-115">Mes</span><span class="sxs-lookup"><span data-stu-id="7bd3a-115">Month</span></span>|<span data-ttu-id="7bd3a-116">Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="7bd3a-117">Si ha seleccionado la casilla **Transf. autom. desde C/G** en la ventana **Configuración contabilidad costes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] actualiza la contabilidad de costes después de cada registro en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="7bd3a-118">Ya no se pueden realizar movimientos combinados.</span><span class="sxs-lookup"><span data-stu-id="7bd3a-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7bd3a-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7bd3a-119">See Also</span></span>  
 <span data-ttu-id="7bd3a-120">[Transferir movimientos de contabilidad a movimientos de coste](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7bd3a-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="7bd3a-121">[Criterios para la transferencia de movimientos de contabilidad a movimientos de coste](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7bd3a-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="7bd3a-122">[Resultados de la transferencia](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="7bd3a-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="7bd3a-123">Transferencia y registro de movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="7bd3a-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="7bd3a-124">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7bd3a-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

