---
title: Configurar activos fijos | Documentos de Microsoft
description: "Obtenga información sobre la secuencia de tareas que debe realizar para configurar activos fijos, como maquinaria o edificios."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="becd0-103">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="becd0-104">Antes de trabajar con activos fijos, debe definir algunos parámetros:</span><span class="sxs-lookup"><span data-stu-id="becd0-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="becd0-105">Cómo asegurar, mantener y amortizar los activos fijos.</span><span class="sxs-lookup"><span data-stu-id="becd0-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="becd0-106">Cómo registrar costes y otros valores en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="becd0-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="becd0-107">La siguiente tabla tiene vínculos a más información.</span><span class="sxs-lookup"><span data-stu-id="becd0-107">The table below has links to more information.</span></span> <span data-ttu-id="becd0-108">Una vez configurados estos parámetros, pueda empezar las distintas actividades.</span><span class="sxs-lookup"><span data-stu-id="becd0-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="becd0-109">Para obtener más información, vea [Activos fijos](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="becd0-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="becd0-110">Puede registrar transacciones de activos en las ventanas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna.</span><span class="sxs-lookup"><span data-stu-id="becd0-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="becd0-111">La ayuda para los activos fijos solo describe cómo utilizar ventana **A/F Diario general**.</span><span class="sxs-lookup"><span data-stu-id="becd0-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="becd0-112">Cuando habilita una actividad de activo fijo en la sección **Integración contabilidad** de la ventana **Ficha libro amortización**, la ventana **A/F Diario general** se usa para registrar las transacciones de la actividad.</span><span class="sxs-lookup"><span data-stu-id="becd0-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="becd0-113">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="becd0-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="becd0-114">Para obtener más información, consulte [Personalizar la experiencia de Financials](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="becd0-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="becd0-115">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="becd0-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="becd0-116">Para</span><span class="sxs-lookup"><span data-stu-id="becd0-116">To</span></span> | <span data-ttu-id="becd0-117">Vea</span><span class="sxs-lookup"><span data-stu-id="becd0-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="becd0-118">Configurar las cuentas predeterminadas, las claves de asignación, las plantillas y las secciones del diario utilizadas para registrar los activos fijos, y configurar las clases y subclases de activos fijos como, por ejemplo, Tangible e Intangible.</span><span class="sxs-lookup"><span data-stu-id="becd0-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="becd0-119">Configurar información general de activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="becd0-120">Crear libros de amortización y definir varios métodos de amortización, integrarlos con el libro mayor y permitir la duplicación de movimientos en varios libros de amortización.</span><span class="sxs-lookup"><span data-stu-id="becd0-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="becd0-121">Configurar la amortización de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="becd0-122">Activar el seguro de activos fijos, configurar la información del seguro, una ficha de seguro por póliza y preparar los diarios para registrar los costes del seguro.</span><span class="sxs-lookup"><span data-stu-id="becd0-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="becd0-123">Configurar el seguro de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="becd0-124">Activar el mantenimiento de activos fijos, configurar la información general de mantenimiento, configurar el mantenimiento de las cuentas de registro y definir los tipos de trabajo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="becd0-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="becd0-125">Configurar el mantenimiento de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="becd0-126">Conocer varios métodos de amortización de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="becd0-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="becd0-127">Métodos de amortización</span><span class="sxs-lookup"><span data-stu-id="becd0-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="becd0-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="becd0-128">See Also</span></span>
[<span data-ttu-id="becd0-129">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="becd0-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="becd0-130">Finanzas</span><span class="sxs-lookup"><span data-stu-id="becd0-130">Finance</span></span>](finance.md)  
<span data-ttu-id="becd0-131">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="becd0-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="becd0-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="becd0-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

