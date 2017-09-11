---
title: Configurar el mantenimiento de activos fijos | Documentos de Microsoft
description: "Para administrar las reparaciones y el servicio de los activos fijos, puede especificar información de mantenimiento general, códigos para el tipo de trabajo y una cuenta de mayor para costes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cdf1183fb5383311dc34d8c2c619a1eddf7e8851
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-fixed-asset-maintenance"></a><span data-ttu-id="9c37a-103">Procedimiento: Configurar el mantenimiento de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="9c37a-103">How to: Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="9c37a-104">Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costes de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, como por ejemplo Servicio rutinario o Reparación.</span><span class="sxs-lookup"><span data-stu-id="9c37a-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="9c37a-105">Para configurar la información general de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="9c37a-105">To set up general maintenance information</span></span>
<span data-ttu-id="9c37a-106">Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="9c37a-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="9c37a-107">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9c37a-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c37a-108">Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="9c37a-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="9c37a-109">En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9c37a-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="9c37a-110">Para configurar los códigos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="9c37a-110">To set up maintenance codes</span></span>
<span data-ttu-id="9c37a-111">Al registrar costes de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.</span><span class="sxs-lookup"><span data-stu-id="9c37a-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="9c37a-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Mantenimiento** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9c37a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c37a-113">En la ventana **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="9c37a-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="9c37a-114">Para configurar las cuentas de gastos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="9c37a-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="9c37a-115">Para registrar los costes de mantenimiento, primero debe introducir un número de cuenta en la ventana **A/F Grupos contables**.</span><span class="sxs-lookup"><span data-stu-id="9c37a-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="9c37a-116">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Grupos contables** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="9c37a-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c37a-117">Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.</span><span class="sxs-lookup"><span data-stu-id="9c37a-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="9c37a-118">Para indicar que los costes de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución.</span><span class="sxs-lookup"><span data-stu-id="9c37a-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="9c37a-119">Para obtener más información, consulte [Procedimiento: Configurar funciones generales a los activos fijos](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="9c37a-119">For more information, see [How to: Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9c37a-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9c37a-120">See Also</span></span>
[<span data-ttu-id="9c37a-121">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="9c37a-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="9c37a-122">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="9c37a-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="9c37a-123">Finanzas</span><span class="sxs-lookup"><span data-stu-id="9c37a-123">Finance</span></span>](finance.md)  
<span data-ttu-id="9c37a-124">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="9c37a-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="9c37a-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c37a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

