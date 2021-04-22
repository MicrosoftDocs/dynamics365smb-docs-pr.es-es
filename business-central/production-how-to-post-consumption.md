---
title: Registrar consumibles por lotes
description: Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787907"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="66502-103">Registrar consumibles de producción por lotes</span><span class="sxs-lookup"><span data-stu-id="66502-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="66502-104">Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.</span><span class="sxs-lookup"><span data-stu-id="66502-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="66502-105">Si ha activado el campo **Picking requerido** en la ficha de almacén para indicar que el almacén requiere proceso de picking de existencias, no necesita usar este trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="66502-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="66502-106">manejará el consumo cuando registro el picking de existencias.</span><span class="sxs-lookup"><span data-stu-id="66502-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="66502-107">Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="66502-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="66502-108">También puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción.</span><span class="sxs-lookup"><span data-stu-id="66502-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="66502-109">Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="66502-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="66502-110">Para registrar el consumo en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="66502-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="66502-111">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario de consumo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="66502-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="66502-112">Rellene los campos con los datos de las órdenes de producción y del consumo.</span><span class="sxs-lookup"><span data-stu-id="66502-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="66502-113">Use la acción **Calcular consumo** para generar líneas del diario de las órdenes de producción basadas en la salida real (la cantidad de productos terminados sobre la que se ha informado) o en la salida esperada (la cantidad de productos terminados que espera producir).</span><span class="sxs-lookup"><span data-stu-id="66502-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="66502-114">Si configuró la ficha de almacén para requerir el proceso de picking y envío, en el campo **Cantidad** de la página **Diario de consumo** solo se pueden introducir cantidades que ya se han seleccionado a través de un actividad de almacén , no una cantidad calculada.</span><span class="sxs-lookup"><span data-stu-id="66502-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="66502-115">Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="66502-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="66502-116">Para registrar el consumo, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="66502-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="66502-117">Los inventarios relacionados se reducen.</span><span class="sxs-lookup"><span data-stu-id="66502-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="66502-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="66502-118">See Also</span></span>

<span data-ttu-id="66502-119">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="66502-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="66502-120">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="66502-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="66502-121">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="66502-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="66502-122">Inventario</span><span class="sxs-lookup"><span data-stu-id="66502-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="66502-123">Compras</span><span class="sxs-lookup"><span data-stu-id="66502-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="66502-124">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66502-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
