---
title: Definición de centros de coste y de objetos de coste para el plan de cuentas | Documentos de Microsoft
description: Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costes para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, el sistema transfiere sólo los movimientos ya vinculados a un centro o un objeto de coste. Para establecer una transferencia significativa, debe asegurarse de que los centros de coste y los objetos de coste están definidos correctamente.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242059"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="54cb3-105">Definición de centros de coste y de objetos de coste para el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="54cb3-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="54cb3-106">Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costes para cada registro de contabilidad o con un trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="54cb3-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="54cb3-107">Cuando lleva a cabo la transferencia, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere sólo los movimientos ya vinculados a un centro o un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="54cb3-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="54cb3-108">Para establecer una transferencia significativa, debe asegurarse de que los centros de coste y los objetos de coste están definidos correctamente.</span><span class="sxs-lookup"><span data-stu-id="54cb3-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="54cb3-109">Definición de los valores de dimensión predeterminados para cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="54cb3-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="54cb3-110">Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="54cb3-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="54cb3-111">El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de coste de DEPARTAMENTO, pero nunca un objeto de coste de PROYECTO al registrar en una cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="54cb3-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="54cb3-112">**Cód. dimensión**</span><span class="sxs-lookup"><span data-stu-id="54cb3-112">**Dimension Code**</span></span>|<span data-ttu-id="54cb3-113">**Registro valor**</span><span class="sxs-lookup"><span data-stu-id="54cb3-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="54cb3-114">Departamento</span><span class="sxs-lookup"><span data-stu-id="54cb3-114">Department</span></span>|<span data-ttu-id="54cb3-115">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="54cb3-115">Code Mandatory</span></span>|  
|<span data-ttu-id="54cb3-116">Programa</span><span class="sxs-lookup"><span data-stu-id="54cb3-116">Project</span></span>|<span data-ttu-id="54cb3-117">Sin código</span><span class="sxs-lookup"><span data-stu-id="54cb3-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="54cb3-118">Definición de valores de dimensión para costes generales y costes directos</span><span class="sxs-lookup"><span data-stu-id="54cb3-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="54cb3-119">Puede transferir costes generales a un centro de coste y costes directos a un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="54cb3-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="54cb3-120">La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.</span><span class="sxs-lookup"><span data-stu-id="54cb3-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="54cb3-121">Transferir a</span><span class="sxs-lookup"><span data-stu-id="54cb3-121">Transfer To</span></span>|<span data-ttu-id="54cb3-122">Registro del centro de coste</span><span class="sxs-lookup"><span data-stu-id="54cb3-122">Cost Center Posting</span></span>|<span data-ttu-id="54cb3-123">Registro del objeto de coste</span><span class="sxs-lookup"><span data-stu-id="54cb3-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="54cb3-124">Centro coste</span><span class="sxs-lookup"><span data-stu-id="54cb3-124">Cost Center</span></span>|<span data-ttu-id="54cb3-125">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="54cb3-125">Code Mandatory</span></span>|<span data-ttu-id="54cb3-126">Sin código</span><span class="sxs-lookup"><span data-stu-id="54cb3-126">No Code</span></span>|  
|<span data-ttu-id="54cb3-127">Objeto coste</span><span class="sxs-lookup"><span data-stu-id="54cb3-127">Cost Object</span></span>|<span data-ttu-id="54cb3-128">Sin código</span><span class="sxs-lookup"><span data-stu-id="54cb3-128">No Code</span></span>|<span data-ttu-id="54cb3-129">Código obligatorio</span><span class="sxs-lookup"><span data-stu-id="54cb3-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="54cb3-130">Para garantizar que el centro de coste y el objeto de coste predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costes, seleccione la casilla **Comprobar registros C/G** en la página Configuración contabilidad costes.</span><span class="sxs-lookup"><span data-stu-id="54cb3-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54cb3-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54cb3-131">See Also</span></span>  
[<span data-ttu-id="54cb3-132">Contabilidad para costes</span><span class="sxs-lookup"><span data-stu-id="54cb3-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="54cb3-133">Configuración de contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="54cb3-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="54cb3-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54cb3-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
