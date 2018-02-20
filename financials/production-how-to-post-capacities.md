---
title: "Cómo registrar capacidades | Documentos de Microsoft"
description: "En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción. Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="post-capacities"></a><span data-ttu-id="7f8bc-104">Registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="7f8bc-104">Post Capacities</span></span>
<span data-ttu-id="7f8bc-105">En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="7f8bc-106">Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="7f8bc-107">Para registrar capacidades</span><span class="sxs-lookup"><span data-stu-id="7f8bc-107">To post capacities</span></span>  
1.  <span data-ttu-id="7f8bc-108">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios de Capacidad** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7f8bc-109">Rellene los campos **Fecha registro** y **Nº documento**.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="7f8bc-110">En el campo **Tipo**, introduzca el tipo de capacidad, ya sea **Centro máquina** o **Centro trabajo**, que esté registrando.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="7f8bc-111">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="7f8bc-111">In the **No.**</span></span> <span data-ttu-id="7f8bc-112">introduzca el número del centro de trabajo o del centro de máquina.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="7f8bc-113">Introduzca los datos correspondientes en el resto de los campos, como **Hora inicial**, **Hora final**, **Cantidad** y **Rechazo**.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="7f8bc-114">Para registrar la factura, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="7f8bc-115">Para consultar los movimientos de centros de trabajo</span><span class="sxs-lookup"><span data-stu-id="7f8bc-115">To view work center ledger entries</span></span>  
<span data-ttu-id="7f8bc-116">En las ventanas **Ficha de centro de trabajo** y **Ficha de centro de máquina**, puede ver las capacidades registradoa como resultado de órdenes de producción terminadas.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="7f8bc-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Centros de trabajo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7f8bc-118">Abra la ficha relevante **Centro trabajo** de lista, y seleccione la acción **Movimientos de capacidad**.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="7f8bc-119">La ventana **Movs. capacidad** muestra los movimientos registrados desde el centro de trabajo en la orden en que fueron registrados.</span><span class="sxs-lookup"><span data-stu-id="7f8bc-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="7f8bc-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f8bc-120">See Also</span></span>  
<span data-ttu-id="7f8bc-121">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7f8bc-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7f8bc-122">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="7f8bc-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7f8bc-123">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="7f8bc-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="7f8bc-124">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="7f8bc-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7f8bc-125">Compras</span><span class="sxs-lookup"><span data-stu-id="7f8bc-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7f8bc-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7f8bc-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

