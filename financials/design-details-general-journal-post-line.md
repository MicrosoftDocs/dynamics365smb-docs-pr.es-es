---
title: "Detalles de diseño: línea de registro en diario general | Documentos de Microsoft"
description: "En este tema se proporciona información de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: c8e2072ad2b9f93a0817b14a6556bc1d44367676
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="9f8a0-103">Detalles de diseño: línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="9f8a0-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="9f8a0-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9f8a0-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9f8a0-105">El nuevo diseño hace la unidad de código 12 más sencilla y más fácil de mantener.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="9f8a0-106">La documentación comienza con la descripción de la información general conceptual del rediseño.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="9f8a0-107">A continuación, explica la arquitectura técnica para mostrar los cambios resultantes del nuevo diseño.</span><span class="sxs-lookup"><span data-stu-id="9f8a0-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9f8a0-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9f8a0-108">In This Section</span></span>  
[<span data-ttu-id="9f8a0-109">Descripción de la línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="9f8a0-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="9f8a0-110">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="9f8a0-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="9f8a0-111">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="9f8a0-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="9f8a0-112">Cambios en unidad de código 12 cambios: asociación de variables globales para línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="9f8a0-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="9f8a0-113">Cambios en la unidad de código 12: cambios en los procedimientos de registro en el diario general</span><span class="sxs-lookup"><span data-stu-id="9f8a0-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="9f8a0-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f8a0-114">See Also</span></span>  
[<span data-ttu-id="9f8a0-115">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="9f8a0-115">Working with General Journals</span></span>](ui-work-general-journals.md)

