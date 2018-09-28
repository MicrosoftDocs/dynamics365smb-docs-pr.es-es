---
title: "Detalles de diseño: Pedido | Documentos de Microsoft"
description: "Este tema proporciona información acerca de vínculos de pedido a pedido en un entorno de fabricación contra pedido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c864663f4dee41b161cf79cba74a49ea4f0a90ed
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-order"></a><span data-ttu-id="4ae43-103">Detalles de diseño: Pedidos</span><span class="sxs-lookup"><span data-stu-id="4ae43-103">Design Details: Order</span></span>
<span data-ttu-id="4ae43-104">En un entorno de fabricación contra pedido, el producto se compra o se produce para cubrir exclusivamente una demanda concreta.</span><span class="sxs-lookup"><span data-stu-id="4ae43-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="4ae43-105">Normalmente, se relaciona con productos A y el motivo para elegir la política de reaprovisionamiento de pedido puede ser que la demanda se produce con poca frecuencia, el plazo es insignificante o varían los atributos requeridos.</span><span class="sxs-lookup"><span data-stu-id="4ae43-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  
  
<span data-ttu-id="4ae43-106">El programa crea un vínculo de pedido contra pedido, que actúa de conexión preliminar entre el suministro, un pedido de suministro o inventario, y la demanda que se va a cumplir.</span><span class="sxs-lookup"><span data-stu-id="4ae43-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  
  
<span data-ttu-id="4ae43-107">Aparte de utilizar la directiva de pedido, el vínculo de pedido a pedido se puede aplicar de las siguientes formas durante la planificación:</span><span class="sxs-lookup"><span data-stu-id="4ae43-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  
  
* <span data-ttu-id="4ae43-108">Al usar la directiva de fabricación Fab-contra-pedido para crear órdenes de producción multinivel o de tipo de proyecto (que producen los componentes necesarios en la misma orden de producción).</span><span class="sxs-lookup"><span data-stu-id="4ae43-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="4ae43-109">Al usar la característica de planificación de pedido de venta para crear una orden de producción a partir de un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="4ae43-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  
  
<span data-ttu-id="4ae43-110">Aunque una empresa de fabricación se considere a sí misma como entorno de fabricación contra pedido, puede ser preferible utilizar una directiva de lote por lote si los productos son puramente estándar sin variación en los atributos.</span><span class="sxs-lookup"><span data-stu-id="4ae43-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="4ae43-111">Como resultado, el programa utilizará un inventario no planificado y solo acumulará los pedidos de venta con la misma fecha de envío o dentro de un ciclo definido.</span><span class="sxs-lookup"><span data-stu-id="4ae43-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  
  
## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="4ae43-112">Conexiones de pedido contra pedido y fechas vencidas</span><span class="sxs-lookup"><span data-stu-id="4ae43-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="4ae43-113">A diferencia de la mayoría de conjuntos de suministro-demanda, el sistema ha planificado completamente los pedidos vinculados con fechas de vencimiento anteriores a la fecha inicial de planificación.</span><span class="sxs-lookup"><span data-stu-id="4ae43-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="4ae43-114">El motivo empresarial de esta excepción es que los conjuntos de demanda-suministro específicos se deben sincronizar mediante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="4ae43-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="4ae43-115">Para obtener más información acerca de la zona congelada aplicable a la mayoría de los tipos de aprovisionamiento-demanda, consulte [Detalles de diseño: Gestión de pedidos antes de la fecha de inicio de planificación](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="4ae43-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ae43-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4ae43-116">See Also</span></span>  
<span data-ttu-id="4ae43-117">[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4ae43-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="4ae43-118">[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="4ae43-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="4ae43-119">[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="4ae43-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="4ae43-120">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="4ae43-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
