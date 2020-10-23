---
title: Configurar el seguro de activos fijos | Documentos de Microsoft
description: Configure una ficha de seguridad y la información de póliza de seguro general para administrar la cobertura del seguro de los activos fijos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e7396b4acfbed7199e1364287cfb7e8dcbe57c19
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924233"
---
# <a name="set-up-fixed-asset-insurance"></a><span data-ttu-id="e6f1f-103">Configure el seguro de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="e6f1f-103">Set Up Fixed Asset Insurance</span></span>
<span data-ttu-id="e6f1f-104">Para gestionar la cobertura del seguro de los activos fijos, debe configurar la información general de los seguros y una ficha de seguro por cada póliza.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-104">To manage fixed asset insurance coverage, you must first set up some general insurance information and an insurance card per policy.</span></span>

## <a name="to-set-up-general-insurance-information"></a><span data-ttu-id="e6f1f-105">Para configurar la información general de seguros</span><span class="sxs-lookup"><span data-stu-id="e6f1f-105">To set up general insurance information</span></span>
<span data-ttu-id="e6f1f-106">Para poder utilizar las características de seguro en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe configurar antes alguna información general de seguro.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-106">To use the insurance features in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set up some general insurance information.</span></span>  

1. <span data-ttu-id="e6f1f-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Setups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6f1f-108">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-108">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a><span data-ttu-id="e6f1f-109">Para configurar tipos de seguros</span><span class="sxs-lookup"><span data-stu-id="e6f1f-109">To set up insurance types</span></span>
<span data-ttu-id="e6f1f-110">Puede agrupar las pólizas de seguros en categorías, como seguro contra robo o contra incendios.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-110">You can group your insurance policies into categories, such as insurance against theft or fire insurance.</span></span> <span data-ttu-id="e6f1f-111">Los tipos de seguros se utilizan en la ficha de seguro.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-111">The insurance types are used on the insurance card.</span></span>

1. <span data-ttu-id="e6f1f-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Tipos seguros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Types**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6f1f-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-113">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-cards"></a><span data-ttu-id="e6f1f-114">Para configurar fichas de seguros</span><span class="sxs-lookup"><span data-stu-id="e6f1f-114">To set up insurance cards</span></span>
<span data-ttu-id="e6f1f-115">Puede acumular información acerca de cada póliza de seguros en la ficha de seguro.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-115">You may accumulate information about each insurance policy on the insurance card.</span></span>  

1. <span data-ttu-id="e6f1f-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Seguro** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6f1f-117">En la página **Seguro**, seleccione la acción **Nuevo** para crear una ficha de seguro nueva.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-117">On the **Insurance** page, choose the **New** action to create a  new insurance card.</span></span>  
3. <span data-ttu-id="e6f1f-118">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-118">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-templates"></a><span data-ttu-id="e6f1f-119">Para configurar libros diarios de seguros</span><span class="sxs-lookup"><span data-stu-id="e6f1f-119">To set up insurance journal templates</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e6f1f-120">crea automáticamente un libro de diario de seguros la primera vez que abra la página **Diario seguros**, pero puede configurar libros de diario adicionales.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-120">automatically creates an insurance journal template the first time that you open the **Insurance Journal** page, but you can set up additional journal templates.</span></span> <span data-ttu-id="e6f1f-121">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="e6f1f-121">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  

1. <span data-ttu-id="e6f1f-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Libros diario seguros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6f1f-123">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-123">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-batches"></a><span data-ttu-id="e6f1f-124">Para configurar secciones del diario de seguros</span><span class="sxs-lookup"><span data-stu-id="e6f1f-124">To set up insurance journal batches</span></span>
<span data-ttu-id="e6f1f-125">En un libro del diario de seguros puede configurar secciones.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-125">You can set up batches in an insurance journal template.</span></span> <span data-ttu-id="e6f1f-126">Los valores de la sección del diario se utilizan como valores predeterminados si no se rellenan los campos de las líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-126">The values in the journal batch are used as default values if the fields are not filled in on the journal lines.</span></span> <span data-ttu-id="e6f1f-127">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="e6f1f-127">For more information, see [Work with General Journals](ui-work-general-journals.md)</span></span>  

1. <span data-ttu-id="e6f1f-128">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Libros diario seguros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6f1f-129">Seleccione una plantilla de diario de seguros y, a continuación, selecciona la acción **Secciones**.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-129">Select an insurance journal template, and then choose the **Batches** action.</span></span>
3. <span data-ttu-id="e6f1f-130">En la página **Secciones diario seguros**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-130">On the **Insurance Journal Batches** page, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e6f1f-131">Los números tienen una función especial en los nombres de diario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-131">Numbers have a special function in journal names.</span></span> <span data-ttu-id="e6f1f-132">Si un nombre de libro diario o un nombre de sección del diario contiene un número, el número aumenta automáticamente en uno cada vez que se registra el diario.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-132">If a journal template name or journal batch name contains a number, the number automatically advances by one every time that the journal is posted.</span></span> <span data-ttu-id="e6f1f-133">Por ejemplo, si se escribe HH1 en el campo **Nombre**, el nombre del diario cambiará a HH2 después de registrar el diario llamado HH1.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-133">For example, if HH1 is entered in the **Name** field, the journal name will change to HH2 after the journal named HH1 has been posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6f1f-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e6f1f-134">See Also</span></span>
[<span data-ttu-id="e6f1f-135">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="e6f1f-135">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="e6f1f-136">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="e6f1f-136">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="e6f1f-137">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e6f1f-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="e6f1f-138">Introducción</span><span class="sxs-lookup"><span data-stu-id="e6f1f-138">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="e6f1f-139">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6f1f-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
