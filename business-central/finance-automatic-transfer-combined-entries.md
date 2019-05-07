---
title: Transferencia automática y movimientos combinados | Documentos de Microsoft
description: En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado. Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste. La siguiente tabla describe las distintas opciones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "941159"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="d344e-105">Transferencia automática y movimientos combinados</span><span class="sxs-lookup"><span data-stu-id="d344e-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="d344e-106">En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado.</span><span class="sxs-lookup"><span data-stu-id="d344e-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="d344e-107">Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="d344e-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="d344e-108">La siguiente tabla describe las distintas opciones.</span><span class="sxs-lookup"><span data-stu-id="d344e-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="d344e-109">Combinar movimientos</span><span class="sxs-lookup"><span data-stu-id="d344e-109">Combine entries</span></span>|<span data-ttu-id="d344e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d344e-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="d344e-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d344e-111">None</span></span>|<span data-ttu-id="d344e-112">Cada movimiento de contabilidad se transfiere individualmente al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d344e-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="d344e-113">Día</span><span class="sxs-lookup"><span data-stu-id="d344e-113">Day</span></span>|<span data-ttu-id="d344e-114">Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d344e-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="d344e-115">Mes</span><span class="sxs-lookup"><span data-stu-id="d344e-115">Month</span></span>|<span data-ttu-id="d344e-116">Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de coste correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d344e-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="d344e-117">Si ha seleccionado la casilla **Transf. autom. desde C/G** en la página **Configuración contabilidad costes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] actualiza la contabilidad de costes después de cada registro en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d344e-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="d344e-118">Ya no se pueden realizar movimientos combinados.</span><span class="sxs-lookup"><span data-stu-id="d344e-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d344e-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d344e-119">See Also</span></span>  
 <span data-ttu-id="d344e-120">[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="d344e-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="d344e-121">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d344e-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
