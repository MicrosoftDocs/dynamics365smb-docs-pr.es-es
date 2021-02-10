---
title: 'Detalles de diseño: Gestión del almacén | Documentos de Microsoft'
description: En este tema se ofrece un resumen de los diseños, conceptos y principios que están detrás de las características de gestión de almacén en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ea9974a8fb63d4e119cdc8b78930fd94777e6a38
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749573"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="575b4-103">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="575b4-104">En esta documentación se ofrece un resumen de los conceptos y los principios que se usan en las características de gestión de almacén en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="575b4-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="575b4-105">Explica el diseño de las funciones de almacén central y cómo se integra el almacén con otras funciones de la cadena de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="575b4-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="575b4-106">Para distinguir los distintos niveles de complejidad del almacenamiento, esta documentación se divide en dos grupos generales, configuraciones básicas y avanzadas de almacén, lo cual se indica mediante los títulos de sección.</span><span class="sxs-lookup"><span data-stu-id="575b4-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="575b4-107">Esta diferenciación sencilla abarca diferentes niveles de complejidad, tal como se define mediante los módulos de producto y de ubicación.</span><span class="sxs-lookup"><span data-stu-id="575b4-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="575b4-108">Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="575b4-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="575b4-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="575b4-109">In This Section</span></span>  
[<span data-ttu-id="575b4-110">Detalles de diseño: Resumen de almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="575b4-111">Detalles de diseño: Configuración de almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="575b4-112">Detalles de diseño: Flujo de entrada en almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="575b4-113">Detalles de diseño: Flujos de almacén internos</span><span class="sxs-lookup"><span data-stu-id="575b4-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="575b4-114">Detalles de diseño: Disponibilidad en el almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="575b4-115">Detalles de diseño: Flujo de salida del almacén</span><span class="sxs-lookup"><span data-stu-id="575b4-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="575b4-116">Detalles de diseño: Integración con inventario</span><span class="sxs-lookup"><span data-stu-id="575b4-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
