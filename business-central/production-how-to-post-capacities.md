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
ms.author: edupont
ms.openlocfilehash: 8a36f33da482970a21ed44ca5541675f05ed955d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788730"
---
# <a name="post-capacities"></a><span data-ttu-id="21edf-104">Registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="21edf-104">Post Capacities</span></span>
<span data-ttu-id="21edf-105">En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="21edf-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="21edf-106">Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="21edf-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="21edf-107">Para registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="21edf-107">To post capacities</span></span>  
1.  <span data-ttu-id="21edf-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios capacidad** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="21edf-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="21edf-109">Rellene los campos **Fecha registro** y **Nº documento**.</span><span class="sxs-lookup"><span data-stu-id="21edf-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="21edf-110">En el campo **Tipo**, introduzca el tipo de capacidad, ya sea **Centro máquina** o **Centro trabajo**, que esté registrando.</span><span class="sxs-lookup"><span data-stu-id="21edf-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="21edf-111">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="21edf-111">In the **No.**</span></span> <span data-ttu-id="21edf-112">introduzca el número del centro de trabajo o del centro de máquina.</span><span class="sxs-lookup"><span data-stu-id="21edf-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="21edf-113">Introduzca los datos correspondientes en el resto de los campos, como **Hora inicial**, **Hora final**, **Cantidad** y **Rechazo**.</span><span class="sxs-lookup"><span data-stu-id="21edf-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="21edf-114">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="21edf-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="21edf-115">Para consultar los movimientos de centros de trabajo</span><span class="sxs-lookup"><span data-stu-id="21edf-115">To view work center ledger entries</span></span>  
<span data-ttu-id="21edf-116">En las páginas **Ficha de centro de trabajo** y **Ficha de centro de máquina**, puede ver las capacidades registradas como resultado de órdenes de producción terminadas.</span><span class="sxs-lookup"><span data-stu-id="21edf-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="21edf-117">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Centros de trabajo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="21edf-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="21edf-118">Abra la ficha relevante **Centro trabajo** de lista, y seleccione la acción **Movimientos de capacidad**.</span><span class="sxs-lookup"><span data-stu-id="21edf-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="21edf-119">La página **Movs. capacidad** muestra los movimientos registrados desde el centro de trabajo en la orden en que fueron registrados.</span><span class="sxs-lookup"><span data-stu-id="21edf-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="21edf-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="21edf-120">See Also</span></span>  
<span data-ttu-id="21edf-121">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="21edf-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="21edf-122">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="21edf-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="21edf-123">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="21edf-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="21edf-124">Inventario</span><span class="sxs-lookup"><span data-stu-id="21edf-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="21edf-125">Compras</span><span class="sxs-lookup"><span data-stu-id="21edf-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="21edf-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="21edf-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
