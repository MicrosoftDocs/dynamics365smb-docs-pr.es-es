---
title: "Cómo actualizar costes estándar | Documentos de Microsoft"
description: "Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 88e715ddd2c60c3eb780ffe71d80676fdea00209
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="update-standard-costs"></a><span data-ttu-id="e711e-103">Actualizar costes estándar</span><span class="sxs-lookup"><span data-stu-id="e711e-103">Update Standard Costs</span></span>
<span data-ttu-id="e711e-104">Debe actualizar periódicamente los costes estándar de los componentes y distribuir los nuevos costes al producto principal.</span><span class="sxs-lookup"><span data-stu-id="e711e-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="e711e-105">El proceso normalmente consiste en los cuatro pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e711e-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="e711e-106">Actualizar los costes en los niveles de componente y de capacidad.</span><span class="sxs-lookup"><span data-stu-id="e711e-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="e711e-107">Para obtener más información, consulte el proceso **Sugerir coste estándar prod.**.</span><span class="sxs-lookup"><span data-stu-id="e711e-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="e711e-108">Consolide y distribuya los costes de componentes y de capacidad para calcular el coste total de fabricación o ensamblado de los productos.</span><span class="sxs-lookup"><span data-stu-id="e711e-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="e711e-109">Implementar los costes estándar que se introducen al ejecutar los trabajos por lotes anteriores.</span><span class="sxs-lookup"><span data-stu-id="e711e-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="e711e-110">Los costes estándar no tienen efecto hasta que se implementan.</span><span class="sxs-lookup"><span data-stu-id="e711e-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="e711e-111">Para obtener más información, consulte Implementar cambios de coste estándar.</span><span class="sxs-lookup"><span data-stu-id="e711e-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="e711e-112">Implementar los cambios para actualizar el campo **Coste unitario** en la ficha del producto y realizar una revalorización de inventario.</span><span class="sxs-lookup"><span data-stu-id="e711e-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="e711e-113">Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="e711e-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="e711e-114">Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="e711e-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="e711e-115">Para actualizar los costes estándar</span><span class="sxs-lookup"><span data-stu-id="e711e-115">To update standard costs</span></span>  
1.  <span data-ttu-id="e711e-116">Ejecute el proceso **Valorar stock - movs. producto**.</span><span class="sxs-lookup"><span data-stu-id="e711e-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="e711e-117">Ejecute el proceso **Regis. variación existencias**.</span><span class="sxs-lookup"><span data-stu-id="e711e-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="e711e-118">Abra la **Hoja trab. coste estándar** y use una o más de las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e711e-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="e711e-119">Ejecute el proceso **Sugerir coste estándar prod.**</span><span class="sxs-lookup"><span data-stu-id="e711e-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="e711e-120">Revise los resultados y realice los cambios que considere necesarios.</span><span class="sxs-lookup"><span data-stu-id="e711e-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="e711e-121">Ejecute el proceso **Sugerir coste estándar capacidad**.</span><span class="sxs-lookup"><span data-stu-id="e711e-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="e711e-122">Revise los resultados y realice los cambios que considere necesarios.</span><span class="sxs-lookup"><span data-stu-id="e711e-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="e711e-123">Ejecute el proceso **Distribuir coste estándar**.</span><span class="sxs-lookup"><span data-stu-id="e711e-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="e711e-124">Revise los resultados y realice los cambios que considere necesarios.</span><span class="sxs-lookup"><span data-stu-id="e711e-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="e711e-125">Ejecute el proceso **Implementar cambios de coste estándar**.</span><span class="sxs-lookup"><span data-stu-id="e711e-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="e711e-126">Revise y registre la página **Diario revalorizac.** , el cual se ha rellenado con entradas provenientes de los pasos anteriores del proceso.</span><span class="sxs-lookup"><span data-stu-id="e711e-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e711e-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e711e-127">See Also</span></span>  
 <span data-ttu-id="e711e-128">[Acerca del cálculo de coste estándar](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="e711e-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="e711e-129">[Gestión de costes de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="e711e-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="e711e-130">[Detalles de diseño: Métodos de coste](design-details-costing-methods.md) [Finanzas](finance.md)</span><span class="sxs-lookup"><span data-stu-id="e711e-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="e711e-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e711e-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

