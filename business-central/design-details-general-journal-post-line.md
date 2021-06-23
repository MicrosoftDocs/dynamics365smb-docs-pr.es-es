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
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215233"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="3aa9b-103">Detalles de diseño: línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="3aa9b-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="3aa9b-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usaron para rediseñar la función de línea de registro en el diario general en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3aa9b-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3aa9b-105">El nuevo diseño hizo que codeunit 12 fuera más sencillo y más fácil de mantener.</span><span class="sxs-lookup"><span data-stu-id="3aa9b-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="3aa9b-106">La documentación comienza con la descripción de la información general conceptual del rediseño.</span><span class="sxs-lookup"><span data-stu-id="3aa9b-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="3aa9b-107">A continuación, explica la arquitectura técnica para mostrar los cambios resultantes del nuevo diseño.</span><span class="sxs-lookup"><span data-stu-id="3aa9b-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3aa9b-108">La información de esta sección se aplica al rediseño en una versión anterior del producto, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="3aa9b-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3aa9b-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3aa9b-109">In This Section</span></span>

[<span data-ttu-id="3aa9b-110">Descripción de la línea de registro en diario general</span><span class="sxs-lookup"><span data-stu-id="3aa9b-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="3aa9b-111">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="3aa9b-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="3aa9b-112">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="3aa9b-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="3aa9b-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3aa9b-113">See Also</span></span>

<span data-ttu-id="3aa9b-114">[Trabajar con diarios generales](ui-work-general-journals.md)
[Detalles de diseño: Línea de registro en el diario general (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="3aa9b-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]