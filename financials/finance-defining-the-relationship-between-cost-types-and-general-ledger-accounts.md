---
title: "Definición de la relación entre los tipos de coste y las cuentas de contabilidad | Documentos de Microsoft"
description: "Obtenga información sobre cómo definir la relación entre el tipo de coste y la cuenta de contabilidad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="be6e0-103">Definición de la relación entre los tipos de coste y las cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="be6e0-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="be6e0-104">La relación entre el tipo de coste y la cuenta de contabilidad se crea en el tipo de coste y en la cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="be6e0-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="be6e0-105">El campo **Intervalo cuenta C/G** en la tabla **Tipo coste** establece qué cuentas de contabilidad pertenecen a un tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="be6e0-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="be6e0-106">El campo **Nº tipo coste**</span><span class="sxs-lookup"><span data-stu-id="be6e0-106">The **Cost Type No.**</span></span> <span data-ttu-id="be6e0-107">en el plan de cuentas establece a qué tipo de coste pertenece una cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="be6e0-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="be6e0-108">Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos coste de plan ctas.**</span><span class="sxs-lookup"><span data-stu-id="be6e0-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="be6e0-109">Relación entre las cuentas de contabilidad y los tipos de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="be6e0-110">Existe una relación n:1 entre las cuentas de contabilidad y los tipos de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="be6e0-111">Varias cuentas de contabilidad pueden pertenecer a un tipo de coste, pero cada cuenta de contabilidad pertenece a sólo un tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="be6e0-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="be6e0-112">La siguiente tabla describe los detalles de la relación.</span><span class="sxs-lookup"><span data-stu-id="be6e0-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="be6e0-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="be6e0-113">Relationship</span></span>|<span data-ttu-id="be6e0-114">**Intervalo cuenta CG**</span><span class="sxs-lookup"><span data-stu-id="be6e0-114">**G/L Account Range**</span></span>|<span data-ttu-id="be6e0-115">**Nº tipo coste**</span><span class="sxs-lookup"><span data-stu-id="be6e0-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="be6e0-116">Una cuenta de contabilidad para cada tipo de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="be6e0-117">Cuentas contables</span><span class="sxs-lookup"><span data-stu-id="be6e0-117">One general ledger account</span></span>|<span data-ttu-id="be6e0-118">Un tipo de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-118">One cost type</span></span>|  
|<span data-ttu-id="be6e0-119">Varias cuentas de contabilidad para un tipo de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="be6e0-120">Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad</span><span class="sxs-lookup"><span data-stu-id="be6e0-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="be6e0-121">Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de coste</span><span class="sxs-lookup"><span data-stu-id="be6e0-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="be6e0-122">Tipos de coste sin las cuentas de contabilidad correspondientes</span><span class="sxs-lookup"><span data-stu-id="be6e0-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="be6e0-123">Cuentas de contabilidad cuyos movimientos no se transferirán</span><span class="sxs-lookup"><span data-stu-id="be6e0-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="be6e0-124">Tipos de coste sin una relación con la contabilidad</span><span class="sxs-lookup"><span data-stu-id="be6e0-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="be6e0-125">Un tipo de coste puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:</span><span class="sxs-lookup"><span data-stu-id="be6e0-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="be6e0-126">Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costes de la contabilidad operativa.</span><span class="sxs-lookup"><span data-stu-id="be6e0-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="be6e0-127">Los tipos de coste de ayuda, como los tipos de coste 9901, 9902 y 9903, en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], se utilizan como cuentas de crédito y débito para asignaciones.</span><span class="sxs-lookup"><span data-stu-id="be6e0-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="be6e0-128">La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], contiene las acumulaciones reales que muestran la diferencia entre los costes y el gasto de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="be6e0-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be6e0-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="be6e0-129">See Also</span></span>  
[<span data-ttu-id="be6e0-130">Contabilidad para costes</span><span class="sxs-lookup"><span data-stu-id="be6e0-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="be6e0-131">[Configuración de contabilidad de costes](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="be6e0-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="be6e0-132">Acerca de la contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="be6e0-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="be6e0-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be6e0-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

