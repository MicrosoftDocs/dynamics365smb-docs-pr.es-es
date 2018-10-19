---
title: "Cómo registrar por lotes el resultado y tiempos de ejecución de producción | Documentos de Microsoft"
description: "La cantidad de salida representa el trabajo en curso en términos de cantidad terminada."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7b895978bd55cd6ed7086326036016002519817e
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="15c67-103">Registrar por lotes el resultado y los tiempos de ejecución</span><span class="sxs-lookup"><span data-stu-id="15c67-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="15c67-104">La cantidad de salida representa el trabajo en curso en términos de cantidad terminada.</span><span class="sxs-lookup"><span data-stu-id="15c67-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="15c67-105">Solo cuando registra la cantidad de salida en la última operación, las existencias se actualizan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="15c67-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="15c67-106">Para registrar cantidades de salida en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="15c67-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="15c67-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="15c67-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="15c67-108">Rellene los campos con los datos de las órdenes de producción y los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="15c67-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="15c67-109">Si la operación se ha completado, seleccione el campo **Terminado**.</span><span class="sxs-lookup"><span data-stu-id="15c67-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="15c67-110">Si el almacén donde se deben ubicar los componentes utiliza ubicaciones, pero no requiere el proceso de ubicación,  asigne un código de ubicación a la línea del diario para especificar dónde se deben colocar los productos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="15c67-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="15c67-111">Para obtener más información, consulte [Sacar producción o salida de ensamblado](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="15c67-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="15c67-112">Para registrar las operaciones, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="15c67-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="15c67-113">Se registrará la cantidad de salida.</span><span class="sxs-lookup"><span data-stu-id="15c67-113">The output quantity will be posted.</span></span> <span data-ttu-id="15c67-114">El producto estará disponible para su envío.</span><span class="sxs-lookup"><span data-stu-id="15c67-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="15c67-115">Para registrar el tiempo de ejecución en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="15c67-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="15c67-116">El tiempo de ejecución representa el trabajo en curso en términos de tiempo de trabajo necesario.</span><span class="sxs-lookup"><span data-stu-id="15c67-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="15c67-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="15c67-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="15c67-118">Rellene los campos con los datos de las órdenes de producción y los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="15c67-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="15c67-119">Si la operación se ha completado, seleccione el campo **Terminado**.</span><span class="sxs-lookup"><span data-stu-id="15c67-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="15c67-120">Seleccione la acción **Registrar** para registrar el tiempo empleado por operación.</span><span class="sxs-lookup"><span data-stu-id="15c67-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="15c67-121">Los movimientos de capacidad se actualizan en los centros utilizados de trabajo o de máquina.</span><span class="sxs-lookup"><span data-stu-id="15c67-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="15c67-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="15c67-122">See Also</span></span>  
<span data-ttu-id="15c67-123">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="15c67-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="15c67-124">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="15c67-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="15c67-125">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="15c67-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="15c67-126">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="15c67-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="15c67-127">Compras</span><span class="sxs-lookup"><span data-stu-id="15c67-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="15c67-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="15c67-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

