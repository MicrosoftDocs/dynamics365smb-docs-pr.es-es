---
title: Ver información de tabla
description: Descubra cómo puede ver información sobre las tablas de bases de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776896"
---
# <a name="viewing-table-information"></a><span data-ttu-id="8f8e0-103">Visualización de información de tabla</span><span class="sxs-lookup"><span data-stu-id="8f8e0-103">Viewing Table Information</span></span>

<span data-ttu-id="8f8e0-104">La página **8700 Información de tabla** proporciona información sobre todas las tablas de sistema y de negocios en una solución Business Central.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="8f8e0-105">En particular, la página muestra información sobre la cantidad de datos que contienen las tablas.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="8f8e0-106">Esta información es útil para solucionar problemas de rendimiento, porque le permite ver la distribución del tamaño de los datos en las tablas.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="8f8e0-107">Visualización de información de tabla</span><span class="sxs-lookup"><span data-stu-id="8f8e0-107">Viewing table information</span></span>

<span data-ttu-id="8f8e0-108">Para abrir esta página, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Información de tabla** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="8f8e0-109">La siguiente tabla describe la información proporcionada para cada tabla:</span><span class="sxs-lookup"><span data-stu-id="8f8e0-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="8f8e0-110">Columna</span><span class="sxs-lookup"><span data-stu-id="8f8e0-110">Column</span></span>|<span data-ttu-id="8f8e0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f8e0-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="8f8e0-112">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="8f8e0-112">Company Name</span></span>|<span data-ttu-id="8f8e0-113">El nombre de la empresa, si existe, a la que pertenece la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="8f8e0-114">Nombre tabla</span><span class="sxs-lookup"><span data-stu-id="8f8e0-114">Table Name</span></span>|<span data-ttu-id="8f8e0-115">El nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-115">The name of the table.</span></span>|
|<span data-ttu-id="8f8e0-116">Nº tabla</span><span class="sxs-lookup"><span data-stu-id="8f8e0-116">Table No.</span></span>|<span data-ttu-id="8f8e0-117">El id. de la tabla</span><span class="sxs-lookup"><span data-stu-id="8f8e0-117">The ID of the table</span></span>|
|<span data-ttu-id="8f8e0-118">Nº</span><span class="sxs-lookup"><span data-stu-id="8f8e0-118">No.</span></span> <span data-ttu-id="8f8e0-119">de registros</span><span class="sxs-lookup"><span data-stu-id="8f8e0-119">of Records</span></span>|<span data-ttu-id="8f8e0-120">El número total de registros almacenados en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="8f8e0-121">Tamaño del registro</span><span class="sxs-lookup"><span data-stu-id="8f8e0-121">Record Size</span></span>|<span data-ttu-id="8f8e0-122">El tamaño de registro promedio en KB/registro.</span><span class="sxs-lookup"><span data-stu-id="8f8e0-122">The average record size in KB/record.</span></span> <span data-ttu-id="8f8e0-123">El valor se calcula utilizando la siguiente fórmula: 1024 (Tamaño)/(N.º</span><span class="sxs-lookup"><span data-stu-id="8f8e0-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="8f8e0-124">de registros).</span><span class="sxs-lookup"><span data-stu-id="8f8e0-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8f8e0-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f8e0-125">See Also</span></span>

[<span data-ttu-id="8f8e0-126">Inspección de páginas</span><span class="sxs-lookup"><span data-stu-id="8f8e0-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="8f8e0-127">Artículos de rendimiento para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="8f8e0-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]