---
title: Configurar activos fijos | Documentos de Microsoft
description: "Obtenga información sobre la secuencia de tareas que debe realizar para configurar activos fijos, como maquinaria o edificios."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 98cf0364b9983e2bf62fe6a3ce4aa882af3ece14
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="e8259-103">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="e8259-104">Antes de trabajar con activos fijos, debe definir algunos parámetros:</span><span class="sxs-lookup"><span data-stu-id="e8259-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="e8259-105">Cómo asegurar, mantener y amortizar los activos fijos.</span><span class="sxs-lookup"><span data-stu-id="e8259-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="e8259-106">Cómo registrar costes y otros valores en el libro mayor.</span><span class="sxs-lookup"><span data-stu-id="e8259-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="e8259-107">La siguiente tabla tiene vínculos a más información.</span><span class="sxs-lookup"><span data-stu-id="e8259-107">The table below has links to more information.</span></span> <span data-ttu-id="e8259-108">Una vez configurados estos parámetros, pueda empezar las distintas actividades.</span><span class="sxs-lookup"><span data-stu-id="e8259-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="e8259-109">Para obtener más información, vea [Activos fijos](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="e8259-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e8259-110">Puede registrar transacciones de activos en las ventanas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna.</span><span class="sxs-lookup"><span data-stu-id="e8259-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="e8259-111">La ayuda para los activos fijos solo describe cómo utilizar ventana **A/F Diario general**.</span><span class="sxs-lookup"><span data-stu-id="e8259-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="e8259-112">Cuando habilita una actividad de activo fijo en la sección **Integración contabilidad** de la ventana **Ficha libro amortización**, la ventana **A/F Diario general** se usa para registrar las transacciones de la actividad.</span><span class="sxs-lookup"><span data-stu-id="e8259-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="e8259-113">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="e8259-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="e8259-114">Para</span><span class="sxs-lookup"><span data-stu-id="e8259-114">To</span></span> | <span data-ttu-id="e8259-115">Vea</span><span class="sxs-lookup"><span data-stu-id="e8259-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="e8259-116">Configurar las cuentas predeterminadas, las claves de asignación, las plantillas y las secciones del diario utilizadas para registrar los activos fijos, y configurar las clases y subclases de activos fijos como, por ejemplo, Tangible e Intangible.</span><span class="sxs-lookup"><span data-stu-id="e8259-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="e8259-117">Configurar información general de activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-117">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="e8259-118">Crear libros de amortización y definir varios métodos de amortización, integrarlos con el libro mayor y permitir la duplicación de movimientos en varios libros de amortización.</span><span class="sxs-lookup"><span data-stu-id="e8259-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="e8259-119">Configurar la amortización de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-119">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="e8259-120">Activar el seguro de activos fijos, configurar la información del seguro, una ficha de seguro por póliza y preparar los diarios para registrar los costes del seguro.</span><span class="sxs-lookup"><span data-stu-id="e8259-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="e8259-121">Configurar el seguro de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-121">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="e8259-122">Activar el mantenimiento de activos fijos, configurar la información general de mantenimiento, configurar el mantenimiento de las cuentas de registro y definir los tipos de trabajo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="e8259-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="e8259-123">Configurar el mantenimiento de los activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-123">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="e8259-124">Conocer varios métodos de amortización de activos fijos.</span><span class="sxs-lookup"><span data-stu-id="e8259-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="e8259-125">Métodos de amortización</span><span class="sxs-lookup"><span data-stu-id="e8259-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="e8259-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8259-126">See Also</span></span>
[<span data-ttu-id="e8259-127">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="e8259-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="e8259-128">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e8259-128">Finance</span></span>](finance.md)  
<span data-ttu-id="e8259-129">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="e8259-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="e8259-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8259-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

