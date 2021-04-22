---
title: Registrar por lotes el resultado y tiempos de ejecución de producción
description: La cantidad de salida representa el trabajo en curso en términos de cantidad terminada y capacidad utilizada del centro de trabajo o de máquina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787882"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="1d2f0-103">Registrar por lotes el resultado y los tiempos de ejecución</span><span class="sxs-lookup"><span data-stu-id="1d2f0-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="1d2f0-104">La cantidad de salida representa el trabajo en curso en términos de cantidad terminada y capacidad utilizada del centro de trabajo o de máquina.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="1d2f0-105">Puede usar el diario de salida para:</span><span class="sxs-lookup"><span data-stu-id="1d2f0-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="1d2f0-106">Ajustar el inventario en relación con la salida de los productos terminados de producción.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="1d2f0-107">Registrar las cantidades y el rechazo para cada operación en la ruta de producción.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="1d2f0-108">Registrar la configuración y el tiempo de ejecución de los centros de trabajo y de máquina.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="1d2f0-109">Si se usa la ruta de producción, se actualiza solo cuando registra la cantidad de salida en la última operación.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="1d2f0-110">Con la ventana **Diario de producción**, puede realizar las mismas tareas que las de la ventana **Diario de salida** y al mismo tiempo realizar las tareas de registro de consumo relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="1d2f0-111">Para obtener más información, consulte [Registrar el consumo y la salida de una línea de orden de producción lanzada](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="1d2f0-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="1d2f0-112">Para registrar cantidades de salida y/o registrar tiempos de ejecución en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="1d2f0-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="1d2f0-113">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1d2f0-114">Rellene los campos con los datos de las órdenes de producción y los datos de salida y/o tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="1d2f0-115">Puede usar la función **Desplegar ruta** para generar líneas de diario a partir de órdenes de producción.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="1d2f0-116">Si la operación se ha completado, seleccione el campo **Terminado**.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="1d2f0-117">Para registrar las operaciones, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="1d2f0-118">Los movimientos de capacidad se actualizan para los centros de trabajo o de máquinas usados con información sobre el tiempo y la cantidad de salida y rechazo.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="1d2f0-119">Si registró la última operación, el producto se agregará al inventario.</span><span class="sxs-lookup"><span data-stu-id="1d2f0-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="1d2f0-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1d2f0-120">See Also</span></span>  
<span data-ttu-id="1d2f0-121">[Registrar el material de rechazo manualmente](production-how-to-post-scrap.md)
[Revertir el registro de la salida](production-how-to-reverse-output-posting.md)
[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="1d2f0-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="1d2f0-122">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="1d2f0-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="1d2f0-123">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="1d2f0-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="1d2f0-124">Inventario</span><span class="sxs-lookup"><span data-stu-id="1d2f0-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="1d2f0-125">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d2f0-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
