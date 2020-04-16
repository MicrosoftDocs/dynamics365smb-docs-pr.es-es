---
title: 'Procedimiento: Baje componentes según la producción de la operación | Documentos de Microsoft'
description: Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**. Para obtener más información, consulte Método de baja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2c063c243f37c44ad7d84b2fc4303e72487c97d5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190472"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="2de21-104">Bajar componentes según la salida de la operación</span><span class="sxs-lookup"><span data-stu-id="2de21-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="2de21-105">Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="2de21-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="2de21-106">Si también define los códigos de vínculo de ruta, el cálculo y el registro se producen cuando termina cada operación, y se registra la cantidad realmente consumida en la operación.</span><span class="sxs-lookup"><span data-stu-id="2de21-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="2de21-107">Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="2de21-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="2de21-108">Por ejemplo, si una orden de producción para producir 800 metros requiere 8 kg de un componente, cuando se registran 200 metros como salida, se registran automáticamente 2 kg de consumo.</span><span class="sxs-lookup"><span data-stu-id="2de21-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="2de21-109">Esta funcionalidad se útil por los motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2de21-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="2de21-110">**Valoración inventario**: los movimientos de valores para la salida y el consumo se crean en paralelo según progresa la orden de producción.</span><span class="sxs-lookup"><span data-stu-id="2de21-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="2de21-111">Sin los códigos de vínculo de ruta, el valor de inventario aumentará mientras se registra salida y después disminuirá en un momento posterior cuando el valor del consumo de componentes se registra con la orden de producción terminada.</span><span class="sxs-lookup"><span data-stu-id="2de21-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="2de21-112">**Disponibilidad stock**: con el registro gradual del consumo, la disponibilidad de productos de componentes está más actualizado, que es importante para mantener los saldos internos entre la demanda y el suministro.</span><span class="sxs-lookup"><span data-stu-id="2de21-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="2de21-113">Sin los códigos de vínculo de ruta, otras demandas para el componente pueden creer que está disponible mientras se encuentre pendiente un registro retrasado del consumo.</span><span class="sxs-lookup"><span data-stu-id="2de21-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="2de21-114">**A tiempo**: con la posibilidad de personalizar los productos para las solicitudes de cliente, puede minimizar la pérdida de tiempo de asegurarse de que solo se produzcan cambios de trabajo y del sistema si es necesario.</span><span class="sxs-lookup"><span data-stu-id="2de21-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="2de21-115">El siguiente procedimiento muestra cómo combinar códigos de vínculo de ruta y baja hacia atrás de modo que la cantidad que se baja para cada operación es proporcional a la salida real de la operación terminada.</span><span class="sxs-lookup"><span data-stu-id="2de21-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="2de21-116">Para bajar componentes según la salida de la operación</span><span class="sxs-lookup"><span data-stu-id="2de21-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="2de21-117">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2de21-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2de21-118">Seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="2de21-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="2de21-119">En la ficha desplegable **Reposición**, en el campo **Método de baja**, seleccione **Anticipada**.</span><span class="sxs-lookup"><span data-stu-id="2de21-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2de21-120">Seleccione **Pick+ Adelante** si el componente se utiliza en un almacén que está configurado para la ubicación y picking directos.</span><span class="sxs-lookup"><span data-stu-id="2de21-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="2de21-121">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2de21-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="2de21-122">Defina los códigos de vínculo de ruta para cada operación que consume el componente.</span><span class="sxs-lookup"><span data-stu-id="2de21-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="2de21-123">Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="2de21-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="2de21-124">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **L.M. de producción** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2de21-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="2de21-125">Defina los códigos de vínculo de ruta desde cada instancia del componente hasta la operación donde se consume.</span><span class="sxs-lookup"><span data-stu-id="2de21-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="2de21-126">El componente debe tener un vínculo de ruta hasta la última operación en la ruta.</span><span class="sxs-lookup"><span data-stu-id="2de21-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2de21-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2de21-127">See Also</span></span>  
[<span data-ttu-id="2de21-128">Crear LM de producción</span><span class="sxs-lookup"><span data-stu-id="2de21-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="2de21-129">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="2de21-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2de21-130">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="2de21-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="2de21-131">[Planificación](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="2de21-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="2de21-132">Inventario</span><span class="sxs-lookup"><span data-stu-id="2de21-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2de21-133">Compras</span><span class="sxs-lookup"><span data-stu-id="2de21-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2de21-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2de21-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
