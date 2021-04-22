---
title: Configurar el mantenimiento de activos fijos | Documentos de Microsoft
description: Para administrar las reparaciones y el servicio de los activos fijos, puede especificar información de mantenimiento general, códigos para el tipo de trabajo y una cuenta de mayor para costes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b437f7508537ec438bf90c3a1239e2620e9db196
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775555"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="4767f-103">Configure el mantenimiento de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="4767f-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="4767f-104">Para gestionar el mantenimiento de los activos fijos, primero debe configurar la información de mantenimiento en una cuenta de registro para los costes de mantenimiento y los códigos de mantenimiento para los tipos de trabajo, como por ejemplo Servicio rutinario o Reparación.</span><span class="sxs-lookup"><span data-stu-id="4767f-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="4767f-105">Para configurar la información general de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4767f-105">To set up general maintenance information</span></span>
<span data-ttu-id="4767f-106">Si configura los campos para el mantenimiento, puede registrar los gastos de mantenimiento en un diario de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="4767f-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="4767f-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4767f-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="4767f-108">Seleccione el activo fijo del que definirá la cobertura de seguro y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="4767f-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="4767f-109">En la ficha desplegable **Mantenimiento**, rellene los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4767f-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="4767f-110">Para configurar los códigos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4767f-110">To set up maintenance codes</span></span>
<span data-ttu-id="4767f-111">Al registrar costes de mantenimiento desde un diario general, puede rellenar el campo **Cód. mantenimiento** para registrar el tipo de mantenimiento efectuado, como un servicio rutinario o una reparación.</span><span class="sxs-lookup"><span data-stu-id="4767f-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="4767f-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Mantenimiento** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4767f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="4767f-113">En la página **Mantenimiento**, configure los códigos para cada tipo de trabajo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4767f-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="4767f-114">Para configurar las cuentas de gastos de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="4767f-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="4767f-115">Para registrar los costes de mantenimiento, primero debe introducir un número de cuenta en la página **A/F Grupos contables**.</span><span class="sxs-lookup"><span data-stu-id="4767f-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="4767f-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos registro A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4767f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="4767f-117">Rellene el campo **Cta. gastos mantenimiento** de cada grupo contable.</span><span class="sxs-lookup"><span data-stu-id="4767f-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4767f-118">Para indicar que los costes de mantenimiento están distribuidos entre departamentos o proyectos, debe configurar claves de distribución.</span><span class="sxs-lookup"><span data-stu-id="4767f-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="4767f-119">Para obtener más información, consulte [Configurar funciones generales a los activos fijos](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="4767f-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4767f-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4767f-120">See Also</span></span>
[<span data-ttu-id="4767f-121">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="4767f-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="4767f-122">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="4767f-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="4767f-123">Finanzas</span><span class="sxs-lookup"><span data-stu-id="4767f-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="4767f-124">Preparación para hacer negocios</span><span class="sxs-lookup"><span data-stu-id="4767f-124">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="4767f-125">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4767f-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]