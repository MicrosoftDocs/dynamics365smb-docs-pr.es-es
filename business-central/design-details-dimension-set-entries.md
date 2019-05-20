---
title: 'Detalles de diseño: Movimientos de grupo de dimensiones | Documentos de Microsoft'
description: En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan para rediseñar la característica de almacenamiento y registro de movimientos de dimensión.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242749"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="578c0-103">Detalles de diseño: Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="578c0-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="578c0-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios de la funcionalidad de almacenamiento y registro de movimientos de dimensión en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="578c0-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="578c0-105">La documentación comienza con la descripción de la información general conceptual.</span><span class="sxs-lookup"><span data-stu-id="578c0-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="578c0-106">Luego se explica la arquitectura técnica.</span><span class="sxs-lookup"><span data-stu-id="578c0-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="578c0-107">Finalmente, proporciona ejemplos de código para preparar la migración y actualización del código de dimensión desde versiones anteriores a Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="578c0-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="578c0-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="578c0-108">In This Section</span></span>  
[<span data-ttu-id="578c0-109">Información general de los movimientos del grupo dimensiones</span><span class="sxs-lookup"><span data-stu-id="578c0-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="578c0-110">Detalles de diseño: Búsqueda de combinaciones de dimensiones</span><span class="sxs-lookup"><span data-stu-id="578c0-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="578c0-111">Detalles de diseño: Estructura de tablas</span><span class="sxs-lookup"><span data-stu-id="578c0-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="578c0-112">Detalles de diseño: Gestión de dimensiones de codeunit 408</span><span class="sxs-lookup"><span data-stu-id="578c0-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="578c0-113">Detalles de diseño: Ejemplos de código de patrones cambiados en las modificaciones</span><span class="sxs-lookup"><span data-stu-id="578c0-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
