---
title: Ver información de tabla
description: Descubra cómo puede ver información sobre las tablas de bases de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a4695594573056ec492bc15c29d1b6fca3100e97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388679"
---
# <a name="viewing-table-information"></a><span data-ttu-id="a69cd-103">Visualización de información de tabla</span><span class="sxs-lookup"><span data-stu-id="a69cd-103">Viewing Table Information</span></span>

<span data-ttu-id="a69cd-104">La página **8700 Información de tabla** proporciona información sobre todas las tablas de sistema y de negocios en una solución Business Central.</span><span class="sxs-lookup"><span data-stu-id="a69cd-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="a69cd-105">En particular, la página muestra información sobre la cantidad de datos que contienen las tablas.</span><span class="sxs-lookup"><span data-stu-id="a69cd-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="a69cd-106">Esta información es útil para solucionar problemas de rendimiento, porque le permite ver la distribución del tamaño de los datos en las tablas.</span><span class="sxs-lookup"><span data-stu-id="a69cd-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="a69cd-107">Visualización de información de tabla</span><span class="sxs-lookup"><span data-stu-id="a69cd-107">Viewing table information</span></span>

<span data-ttu-id="a69cd-108">Para abrir esta página, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Información de tabla** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a69cd-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="a69cd-109">La siguiente tabla describe la información proporcionada para cada tabla:</span><span class="sxs-lookup"><span data-stu-id="a69cd-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="a69cd-110">Columna</span><span class="sxs-lookup"><span data-stu-id="a69cd-110">Column</span></span>|<span data-ttu-id="a69cd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a69cd-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="a69cd-112">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="a69cd-112">Company Name</span></span>|<span data-ttu-id="a69cd-113">El nombre de la empresa, si existe, a la que pertenece la tabla.</span><span class="sxs-lookup"><span data-stu-id="a69cd-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="a69cd-114">Nombre tabla</span><span class="sxs-lookup"><span data-stu-id="a69cd-114">Table Name</span></span>|<span data-ttu-id="a69cd-115">El nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a69cd-115">The name of the table.</span></span>|
|<span data-ttu-id="a69cd-116">Nº tabla</span><span class="sxs-lookup"><span data-stu-id="a69cd-116">Table No.</span></span>|<span data-ttu-id="a69cd-117">El id. de la tabla</span><span class="sxs-lookup"><span data-stu-id="a69cd-117">The ID of the table</span></span>|
|<span data-ttu-id="a69cd-118">Nº</span><span class="sxs-lookup"><span data-stu-id="a69cd-118">No.</span></span> <span data-ttu-id="a69cd-119">de registros</span><span class="sxs-lookup"><span data-stu-id="a69cd-119">of Records</span></span>|<span data-ttu-id="a69cd-120">El número total de registros almacenados en la tabla.</span><span class="sxs-lookup"><span data-stu-id="a69cd-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="a69cd-121">Tamaño del registro</span><span class="sxs-lookup"><span data-stu-id="a69cd-121">Record Size</span></span>|<span data-ttu-id="a69cd-122">El tamaño de registro promedio en KB/registro.</span><span class="sxs-lookup"><span data-stu-id="a69cd-122">The average record size in KB/record.</span></span> <span data-ttu-id="a69cd-123">El valor se calcula utilizando la siguiente fórmula: 1024 (Tamaño)/(N.º</span><span class="sxs-lookup"><span data-stu-id="a69cd-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="a69cd-124">de registros).</span><span class="sxs-lookup"><span data-stu-id="a69cd-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a69cd-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a69cd-125">See Also</span></span>

[<span data-ttu-id="a69cd-126">Inspección de páginas</span><span class="sxs-lookup"><span data-stu-id="a69cd-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="a69cd-127">Artículos de rendimiento para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="a69cd-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]