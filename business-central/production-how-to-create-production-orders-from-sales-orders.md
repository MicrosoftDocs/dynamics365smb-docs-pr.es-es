---
title: Crear órdenes de producción desde pedidos de venta
description: Puede crear órdenes de producción desde pedidos de venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115241"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="4aab7-103">Crear órdenes de producción desde pedidos de venta</span><span class="sxs-lookup"><span data-stu-id="4aab7-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="4aab7-104">Puede crear órdenes de producción para artículos producidos directamente desde los pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="4aab7-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="4aab7-105">Para crear una orden de producción desde un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="4aab7-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="4aab7-106">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4aab7-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4aab7-107">Seleccione el pedido de venta para el que desea crear una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="4aab7-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="4aab7-108">Seleccione la acción **Planificación**.</span><span class="sxs-lookup"><span data-stu-id="4aab7-108">Choose the **Planning** action.</span></span> <span data-ttu-id="4aab7-109">En la página **Planificación pedido venta**, puede consultar la disponibilidad de un producto incluido en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="4aab7-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="4aab7-110">Seleccione la acción **Orden de producción**.</span><span class="sxs-lookup"><span data-stu-id="4aab7-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="4aab7-111">Seleccione el tipo del estado y orden.</span><span class="sxs-lookup"><span data-stu-id="4aab7-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="4aab7-112">Seleccione el botón **Sí** para crear una o más órdenes de producción para las líneas que tengan **Ord. prod.** en su campo **Sistema de reposición**.</span><span class="sxs-lookup"><span data-stu-id="4aab7-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="4aab7-113">Las líneas de demanda en la orden de producción creada que disponen de **Prod. Pedido** en el campo de **Sistema reposición** representan las órdenes de producción subyacentes.</span><span class="sxs-lookup"><span data-stu-id="4aab7-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="4aab7-114">Después de generar estas órdenes de producción, recuerde identificar la demanda de componentes no satisfecha utilizando la página **Planificación de pedidos** o la función **Replanificar** desde las órdenes creadas.</span><span class="sxs-lookup"><span data-stu-id="4aab7-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="4aab7-115">Tipo orden</span><span class="sxs-lookup"><span data-stu-id="4aab7-115">Order type</span></span>  
<span data-ttu-id="4aab7-116">Puede elegir entre dos formas de crear las órdenes de producción, como se describe en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4aab7-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="4aab7-117">Opción</span><span class="sxs-lookup"><span data-stu-id="4aab7-117">Option</span></span>|<span data-ttu-id="4aab7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4aab7-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4aab7-119">Orden producto</span><span class="sxs-lookup"><span data-stu-id="4aab7-119">Item Order</span></span>|<span data-ttu-id="4aab7-120">Se crea una orden de producción para cada orden de producción necesaria representada por una línea en la ventana **Planificación pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="4aab7-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="4aab7-121">Orden proyecto</span><span class="sxs-lookup"><span data-stu-id="4aab7-121">Project Order</span></span>|<span data-ttu-id="4aab7-122">Se crea una orden de producción para todas las órdenes de producción necesarias representadas por líneas en la ventana **Planificación pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="4aab7-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="4aab7-123">Cuando utilice órdenes de proyecto, el campo **Tipo de procedencia** de la orden de producción contiene **Cabecera de ventas** y la orden tiene varias líneas, una para cada producto de línea de venta que debe fabricarse.</span><span class="sxs-lookup"><span data-stu-id="4aab7-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="4aab7-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4aab7-124">See Also</span></span>  
[<span data-ttu-id="4aab7-125">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="4aab7-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4aab7-126">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4aab7-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4aab7-127">Inventario</span><span class="sxs-lookup"><span data-stu-id="4aab7-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4aab7-128">Compras</span><span class="sxs-lookup"><span data-stu-id="4aab7-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4aab7-129">[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4aab7-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="4aab7-130">Procedimientos recomendados de configuración: planificación de suministros</span><span class="sxs-lookup"><span data-stu-id="4aab7-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="4aab7-131">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4aab7-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
