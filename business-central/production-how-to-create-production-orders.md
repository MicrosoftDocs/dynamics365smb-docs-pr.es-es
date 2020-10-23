---
title: Como crear una cabecera de orden de producción | Documentos de Microsoft
description: Puede crear una orden de producción manualmente y el primer paso es crear la cabecera.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f03bb162bc73d45068579a20bcdd90f632ede9de
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922749"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="cf5f3-103">Crear cabeceras de orden de producción</span><span class="sxs-lookup"><span data-stu-id="cf5f3-103">Create Production Order Headers</span></span>
<span data-ttu-id="cf5f3-104">Puede crear una orden de producción manualmente y el primer paso es crear la cabecera.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="cf5f3-105">Las órdenes de producción normalmente se crean automáticamente por algunas tareas de planificación para cubrir una demanda conocida.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="cf5f3-106">Para obtener más información, consulte [Planificación](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f3-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="cf5f3-107">En el siguiente procedimiento, se crea una orden de producción planificada en firme.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="cf5f3-108">Puede también crear órdenes de producción con estados distintos.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="cf5f3-109">Para crear la cabecera de una orden de producción</span><span class="sxs-lookup"><span data-stu-id="cf5f3-109">To create a production order header</span></span>  
1.  <span data-ttu-id="cf5f3-110">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cf5f3-111">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="cf5f3-112">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="cf5f3-112">In the **No.**</span></span> <span data-ttu-id="cf5f3-113">inserte el número siguiente de la serie.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="cf5f3-114">En el campo **Tipo procedencia mov.**, seleccione la procedencia del movimiento de la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="cf5f3-115">Aquí puede seleccionar producir para una familia de productos.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="cf5f3-116">Para obtener más información, consulte [Trabajar con familias de producción](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f3-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="cf5f3-117">En el campo **Cód. procedencia mov.**, seleccione el código de producto, familia o cabecera de venta para el cual se va a generar la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="cf5f3-118">Rellene los campos **Cantidad** y **Fecha vencimiento** según sus especificaciones.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="cf5f3-119">Cuando cambian las necesidades de producción, como componentes u operaciones, puede replantear rápidamente la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="cf5f3-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="cf5f3-120">Para obtener más información, vea [Actualizar o replanificar las órdenes de producción directamente](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f3-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="cf5f3-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf5f3-121">See Also</span></span>  
<span data-ttu-id="cf5f3-122">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="cf5f3-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="cf5f3-123">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="cf5f3-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="cf5f3-124">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="cf5f3-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="cf5f3-125">Inventario</span><span class="sxs-lookup"><span data-stu-id="cf5f3-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cf5f3-126">Compras</span><span class="sxs-lookup"><span data-stu-id="cf5f3-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cf5f3-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf5f3-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
