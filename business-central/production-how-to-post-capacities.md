---
title: Cómo registrar capacidades | Documentos de Microsoft
description: En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción. Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e244f66e5bb080ff1bec0177d31079e0af39e701
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191600"
---
# <a name="post-capacities"></a><span data-ttu-id="48687-104">Registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="48687-104">Post Capacities</span></span>
<span data-ttu-id="48687-105">En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="48687-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="48687-106">Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="48687-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="48687-107">Para registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="48687-107">To post capacities</span></span>  
1.  <span data-ttu-id="48687-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios capacidad** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="48687-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48687-109">Rellene los campos **Fecha registro** y **Nº documento**.</span><span class="sxs-lookup"><span data-stu-id="48687-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="48687-110">En el campo **Tipo**, introduzca el tipo de capacidad, ya sea **Centro máquina** o **Centro trabajo**, que esté registrando.</span><span class="sxs-lookup"><span data-stu-id="48687-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="48687-111">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="48687-111">In the **No.**</span></span> <span data-ttu-id="48687-112">introduzca el número del centro de trabajo o del centro de máquina.</span><span class="sxs-lookup"><span data-stu-id="48687-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="48687-113">Introduzca los datos correspondientes en el resto de los campos, como **Hora inicial**, **Hora final**, **Cantidad** y **Rechazo**.</span><span class="sxs-lookup"><span data-stu-id="48687-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="48687-114">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="48687-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="48687-115">Para consultar los movimientos de centros de trabajo</span><span class="sxs-lookup"><span data-stu-id="48687-115">To view work center ledger entries</span></span>  
<span data-ttu-id="48687-116">En las páginas **Ficha de centro de trabajo** y **Ficha de centro de máquina**, puede ver las capacidades registradas como resultado de órdenes de producción terminadas.</span><span class="sxs-lookup"><span data-stu-id="48687-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="48687-117">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Centros de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="48687-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48687-118">Abra la ficha relevante **Centro trabajo** de lista, y seleccione la acción **Movimientos de capacidad**.</span><span class="sxs-lookup"><span data-stu-id="48687-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="48687-119">La página **Movs. capacidad** muestra los movimientos registrados desde el centro de trabajo en la orden en que fueron registrados.</span><span class="sxs-lookup"><span data-stu-id="48687-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="48687-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48687-120">See Also</span></span>  
<span data-ttu-id="48687-121">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="48687-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="48687-122">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="48687-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="48687-123">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="48687-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="48687-124">Inventario</span><span class="sxs-lookup"><span data-stu-id="48687-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="48687-125">Compras</span><span class="sxs-lookup"><span data-stu-id="48687-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="48687-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48687-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
