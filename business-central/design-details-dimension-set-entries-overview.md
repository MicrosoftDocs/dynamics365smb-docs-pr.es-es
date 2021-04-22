---
title: Información general de los movimientos del grupo dimensiones | Documentos de Microsoft
description: Este tema describe cómo se almacenan y se registran los movimientos de grupo de dimensiones en Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e03275c55290cccb2d8e91d7a934379184744a36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788338"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="bdf31-103">Información general de los movimientos del grupo dimensiones</span><span class="sxs-lookup"><span data-stu-id="bdf31-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="bdf31-104">Este tema describe cómo se almacenan y se registran los movimientos de grupo de dimensiones en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="bdf31-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="bdf31-105">Conjuntos de dimensiones</span><span class="sxs-lookup"><span data-stu-id="bdf31-105">Dimension Sets</span></span>  
<span data-ttu-id="bdf31-106">Un grupo de dimensiones es una combinación única de valores de dimensión.</span><span class="sxs-lookup"><span data-stu-id="bdf31-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="bdf31-107">Se almacena como movimientos de grupo de dimensiones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bdf31-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="bdf31-108">Cada movimiento de grupo de dimensiones representa un valor de dimensión único.</span><span class="sxs-lookup"><span data-stu-id="bdf31-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="bdf31-109">El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="bdf31-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="bdf31-110">El siguiente ejemplo muestra un grupo de dimensiones que tiene tres movimientos de grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="bdf31-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="bdf31-111">El grupo de dimensiones se identifica por medio de un número de grupo de dimensiones, que es 108.</span><span class="sxs-lookup"><span data-stu-id="bdf31-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="bdf31-112">Id. grupo dimensiones</span><span class="sxs-lookup"><span data-stu-id="bdf31-112">Dimension Set ID</span></span>|<span data-ttu-id="bdf31-113">Cód. dimensión</span><span class="sxs-lookup"><span data-stu-id="bdf31-113">Dimension Code</span></span>|<span data-ttu-id="bdf31-114">Cód. valor dimensión</span><span class="sxs-lookup"><span data-stu-id="bdf31-114">Dimension Value Code</span></span>|<span data-ttu-id="bdf31-115">Nombre valor dimensión</span><span class="sxs-lookup"><span data-stu-id="bdf31-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="bdf31-116">108</span><span class="sxs-lookup"><span data-stu-id="bdf31-116">108</span></span>|<span data-ttu-id="bdf31-117">ÁREA</span><span class="sxs-lookup"><span data-stu-id="bdf31-117">AREA</span></span>|<span data-ttu-id="bdf31-118">nº 70</span><span class="sxs-lookup"><span data-stu-id="bdf31-118">70</span></span>|<span data-ttu-id="bdf31-119">Norte América</span><span class="sxs-lookup"><span data-stu-id="bdf31-119">America North</span></span>|  
|<span data-ttu-id="bdf31-120">108</span><span class="sxs-lookup"><span data-stu-id="bdf31-120">108</span></span>|<span data-ttu-id="bdf31-121">GRUPONEGOCIO</span><span class="sxs-lookup"><span data-stu-id="bdf31-121">BUSINESSGROUP</span></span>|<span data-ttu-id="bdf31-122">INICIO</span><span class="sxs-lookup"><span data-stu-id="bdf31-122">HOME</span></span>|<span data-ttu-id="bdf31-123">Inicio</span><span class="sxs-lookup"><span data-stu-id="bdf31-123">Home</span></span>|  
|<span data-ttu-id="bdf31-124">108</span><span class="sxs-lookup"><span data-stu-id="bdf31-124">108</span></span>|<span data-ttu-id="bdf31-125">DPTO</span><span class="sxs-lookup"><span data-stu-id="bdf31-125">DEPARTMENT</span></span>|<span data-ttu-id="bdf31-126">CCIAL</span><span class="sxs-lookup"><span data-stu-id="bdf31-126">SALES</span></span>|<span data-ttu-id="bdf31-127">Ccial</span><span class="sxs-lookup"><span data-stu-id="bdf31-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="bdf31-128">Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="bdf31-128">Dimension Set Entries</span></span>  
<span data-ttu-id="bdf31-129">Los grupos de dimensiones se almacenan en la tabla **Mov. grupo de dimensiones** como movimientos de grupo de dimensiones con el mismo Id. del grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="bdf31-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="bdf31-130">![Flujo de movimientos del grupo dimensiones](media/dimensionentrynav7.png "Flujo de movimientos del grupo dimensiones")</span><span class="sxs-lookup"><span data-stu-id="bdf31-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="bdf31-131">Cuando crea una nueva línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión.</span><span class="sxs-lookup"><span data-stu-id="bdf31-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="bdf31-132">En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="bdf31-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="bdf31-133">Cuando modifica y cierra la página **Editar movimientos de grupo de dimensiones**, se realiza una comprobación para ver si la combinación de valores de dimensión existe como grupo de dimensiones en la tabla.</span><span class="sxs-lookup"><span data-stu-id="bdf31-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="bdf31-134">Si la combinación tiene lugar en la tabla, el Id. correspondiente del grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos.</span><span class="sxs-lookup"><span data-stu-id="bdf31-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="bdf31-135">Si no, un nuevo grupo de dimensiones se agrega a la tabla, y el nuevo Id. del grupo de dimensiones se asigna a la línea de diario, cabecera de documento o línea de documento.</span><span class="sxs-lookup"><span data-stu-id="bdf31-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="bdf31-136">Gestión de dimensiones de codeunit 408</span><span class="sxs-lookup"><span data-stu-id="bdf31-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="bdf31-137">Codeunit 408, gestión de dimensiones, es una biblioteca de funciones que controla tareas comunes relacionadas con las dimensiones, como copiar desde una tabla a otra o desde un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="bdf31-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="bdf31-138">Mejora del rendimiento</span><span class="sxs-lookup"><span data-stu-id="bdf31-138">Performance Improvement</span></span>  
<span data-ttu-id="bdf31-139">Al almacenar grupos de dimensiones una vez en la base de datos, se preserva el espacio de la base de datos y se mejora el rendimiento total.</span><span class="sxs-lookup"><span data-stu-id="bdf31-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bdf31-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bdf31-140">See Also</span></span>
<span data-ttu-id="bdf31-141">[Detalles de diseño: Búsqueda de combinaciones de dimensiones](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="bdf31-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="bdf31-142">[Detalles de diseño: Estructura de tablas](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="bdf31-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="bdf31-143">Detalles de diseño: Movimientos de grupo de dimensiones</span><span class="sxs-lookup"><span data-stu-id="bdf31-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
