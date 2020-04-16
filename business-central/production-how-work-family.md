---
title: Cómo utilizar las familias de producto de fabricación | Documentos de Microsoft
description: La tarea principal en la personalización de un calendario base para su empresa, o uno de sus socios comerciales, es cambiar el estado de los días laborables y días no laborables.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e48d49e8f708026980e148a8b5457b3eb1e4711c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191384"
---
# <a name="work-with-production-families"></a><span data-ttu-id="281b3-103">Trabajar con familias de producción</span><span class="sxs-lookup"><span data-stu-id="281b3-103">Work with Production Families</span></span>
<span data-ttu-id="281b3-104">Una familia es un grupo de productos individuales cuya relación se basa en la similitud de sus procesos de fabricación.</span><span class="sxs-lookup"><span data-stu-id="281b3-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="281b3-105">Mediante la formación de familias, algunos productos se pueden fabricar dos o más veces en un mismo proceso productivo, lo que optimizará el consumo de material.</span><span class="sxs-lookup"><span data-stu-id="281b3-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="281b3-106">En el campo **Cantidad**, en la página **Familia**, introduzca la cantidad que se fabricará cuando se haya fabricado una vez toda la familia.</span><span class="sxs-lookup"><span data-stu-id="281b3-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="281b3-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="281b3-107">Example</span></span>
<span data-ttu-id="281b3-108">En los procesos de troquelado, se pueden fabricar cuatro piezas de un producto desde una plancha y 10 piezas más de otro producto distinto al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="281b3-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="281b3-109">La troqueladora fabricará 14 piezas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="281b3-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="281b3-110">La formación de familias de productos reduce la cantidad de rechazo que normalmente serían rechazadas como sobrantes al fabricar grandes piezas, que se utilizarán para fabricar productos pequeños.</span><span class="sxs-lookup"><span data-stu-id="281b3-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="281b3-111">Para configurar una familia de producción</span><span class="sxs-lookup"><span data-stu-id="281b3-111">To set up a production family</span></span>
1. <span data-ttu-id="281b3-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Familias** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="281b3-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="281b3-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="281b3-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="281b3-114">Para producir basándose en una familily producción</span><span class="sxs-lookup"><span data-stu-id="281b3-114">To produce based on a production family</span></span>
1. <span data-ttu-id="281b3-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="281b3-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="281b3-116">Crear una nueva orden de producción.</span><span class="sxs-lookup"><span data-stu-id="281b3-116">Create a new production order.</span></span> <span data-ttu-id="281b3-117">Para obtener más información, consulte [Crear órdenes de producción](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="281b3-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="281b3-118">En el campo **Tipo de origen**, seleccione **Familia**.</span><span class="sxs-lookup"><span data-stu-id="281b3-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="281b3-119">En el campo **Nº de origen**, seleccione la familia de producción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="281b3-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="281b3-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="281b3-120">See Also</span></span>
[<span data-ttu-id="281b3-121">Crear LM de producción</span><span class="sxs-lookup"><span data-stu-id="281b3-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="281b3-122">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="281b3-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="281b3-123">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="281b3-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="281b3-124">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="281b3-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="281b3-125">Inventario</span><span class="sxs-lookup"><span data-stu-id="281b3-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="281b3-126">Compras</span><span class="sxs-lookup"><span data-stu-id="281b3-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="281b3-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="281b3-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
