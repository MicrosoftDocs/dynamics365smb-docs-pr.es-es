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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69829004c27ec56339269fe0534f45605efa807e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246681"
---
# <a name="set-up-fixed-asset-insurance"></a><span data-ttu-id="2f02c-103">Configure el seguro de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="2f02c-103">Set Up Fixed Asset Insurance</span></span>
<span data-ttu-id="2f02c-104">Para gestionar la cobertura del seguro de los activos fijos, debe configurar la información general de los seguros y una ficha de seguro por cada póliza.</span><span class="sxs-lookup"><span data-stu-id="2f02c-104">To manage fixed asset insurance coverage, you must first set up some general insurance information and an insurance card per policy.</span></span>

## <a name="to-set-up-general-insurance-information"></a><span data-ttu-id="2f02c-105">Para configurar la información general de seguros</span><span class="sxs-lookup"><span data-stu-id="2f02c-105">To set up general insurance information</span></span>
<span data-ttu-id="2f02c-106">Para poder utilizar las características de seguro en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe configurar antes alguna información general de seguro.</span><span class="sxs-lookup"><span data-stu-id="2f02c-106">To use the insurance features in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set up some general insurance information.</span></span>  

1. <span data-ttu-id="2f02c-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2f02c-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Setups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f02c-108">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-108">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a><span data-ttu-id="2f02c-109">Para configurar tipos de seguros</span><span class="sxs-lookup"><span data-stu-id="2f02c-109">To set up insurance types</span></span>
<span data-ttu-id="2f02c-110">Puede agrupar las pólizas de seguros en categorías, como seguro contra robo o contra incendios.</span><span class="sxs-lookup"><span data-stu-id="2f02c-110">You can group your insurance policies into categories, such as insurance against theft or fire insurance.</span></span> <span data-ttu-id="2f02c-111">Los tipos de seguros se utilizan en la ficha de seguro.</span><span class="sxs-lookup"><span data-stu-id="2f02c-111">The insurance types are used on the insurance card.</span></span>

1. <span data-ttu-id="2f02c-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Tipos de seguro** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2f02c-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Types**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f02c-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-113">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-cards"></a><span data-ttu-id="2f02c-114">Para configurar fichas de seguros</span><span class="sxs-lookup"><span data-stu-id="2f02c-114">To set up insurance cards</span></span>
<span data-ttu-id="2f02c-115">Puede acumular información acerca de cada póliza de seguros en la ficha de seguro.</span><span class="sxs-lookup"><span data-stu-id="2f02c-115">You may accumulate information about each insurance policy on the insurance card.</span></span>  

1. <span data-ttu-id="2f02c-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Seguro** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2f02c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f02c-117">En la página **Seguro**, seleccione la acción **Nuevo** para crear una ficha de seguro nueva.</span><span class="sxs-lookup"><span data-stu-id="2f02c-117">On the **Insurance** page, choose the **New** action to create a  new insurance card.</span></span>  
3. <span data-ttu-id="2f02c-118">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-118">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-templates"></a><span data-ttu-id="2f02c-119">Para configurar libros diarios de seguros</span><span class="sxs-lookup"><span data-stu-id="2f02c-119">To set up insurance journal templates</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2f02c-120">crea automáticamente un libro de diario de seguros la primera vez que abra la página **Diario seguros**, pero puede configurar libros de diario adicionales.</span><span class="sxs-lookup"><span data-stu-id="2f02c-120">automatically creates an insurance journal template the first time that you open the **Insurance Journal** page, but you can set up additional journal templates.</span></span> <span data-ttu-id="2f02c-121">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="2f02c-121">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  

1. <span data-ttu-id="2f02c-122">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plantillas diario de seguros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2f02c-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f02c-123">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-123">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-batches"></a><span data-ttu-id="2f02c-124">Para configurar secciones del diario de seguros</span><span class="sxs-lookup"><span data-stu-id="2f02c-124">To set up insurance journal batches</span></span>
<span data-ttu-id="2f02c-125">En un libro del diario de seguros puede configurar secciones.</span><span class="sxs-lookup"><span data-stu-id="2f02c-125">You can set up batches in an insurance journal template.</span></span> <span data-ttu-id="2f02c-126">Los valores de la sección del diario se utilizan como valores predeterminados si no se rellenan los campos de las líneas de diario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-126">The values in the journal batch are used as default values if the fields are not filled in on the journal lines.</span></span> <span data-ttu-id="2f02c-127">Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="2f02c-127">For more information, see [Work with General Journals](ui-work-general-journals.md)</span></span>  

1. <span data-ttu-id="2f02c-128">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plantillas diario de seguros** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2f02c-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2f02c-129">Seleccione una plantilla de diario de seguros y, a continuación, selecciona la acción **Secciones**.</span><span class="sxs-lookup"><span data-stu-id="2f02c-129">Select an insurance journal template, and then choose the **Batches** action.</span></span>
3. <span data-ttu-id="2f02c-130">En la página **Secciones diario seguros**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-130">On the **Insurance Journal Batches** page, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2f02c-131">Los números tienen una función especial en los nombres de diario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-131">Numbers have a special function in journal names.</span></span> <span data-ttu-id="2f02c-132">Si un nombre de libro diario o un nombre de sección del diario contiene un número, el número aumenta automáticamente en uno cada vez que se registra el diario.</span><span class="sxs-lookup"><span data-stu-id="2f02c-132">If a journal template name or journal batch name contains a number, the number automatically advances by one every time that the journal is posted.</span></span> <span data-ttu-id="2f02c-133">Por ejemplo, si se escribe HH1 en el campo **Nombre**, el nombre del diario cambiará a HH2 después de registrar el diario llamado HH1.</span><span class="sxs-lookup"><span data-stu-id="2f02c-133">For example, if HH1 is entered in the **Name** field, the journal name will change to HH2 after the journal named HH1 has been posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f02c-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f02c-134">See Also</span></span>
[<span data-ttu-id="2f02c-135">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="2f02c-135">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="2f02c-136">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="2f02c-136">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="2f02c-137">Finanzas</span><span class="sxs-lookup"><span data-stu-id="2f02c-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="2f02c-138">Introducción</span><span class="sxs-lookup"><span data-stu-id="2f02c-138">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="2f02c-139">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f02c-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
