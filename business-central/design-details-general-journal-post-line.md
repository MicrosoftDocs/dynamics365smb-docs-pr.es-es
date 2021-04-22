---
title: 'Detalles de diseño: línea de registro en diario general | Documentos de Microsoft'
description: En este tema se proporciona información de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3ea2ea8a4ef5bbdff70346022ee226fd5e26748d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777828"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="04977-103">Detalles de diseño: línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="04977-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="04977-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan para rediseñar la función de línea de registro en el diario general en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="04977-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="04977-105">El nuevo diseño hace la codeunit 12 más sencillo y más fácil de mantener.</span><span class="sxs-lookup"><span data-stu-id="04977-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="04977-106">La documentación comienza con la descripción de la información general conceptual del rediseño.</span><span class="sxs-lookup"><span data-stu-id="04977-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="04977-107">A continuación, explica la arquitectura técnica para mostrar los cambios resultantes del nuevo diseño.</span><span class="sxs-lookup"><span data-stu-id="04977-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="04977-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="04977-108">In This Section</span></span>  
[<span data-ttu-id="04977-109">Descripción de la línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="04977-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="04977-110">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="04977-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="04977-111">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="04977-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="04977-112">Cambios en codeunit 12: asociación de variables globales para línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="04977-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="04977-113">Cambios en la codeunit 12: cambios en los procedimientos de registro en el diario general</span><span class="sxs-lookup"><span data-stu-id="04977-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="04977-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04977-114">See Also</span></span>  
[<span data-ttu-id="04977-115">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="04977-115">Working with General Journals</span></span>](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]