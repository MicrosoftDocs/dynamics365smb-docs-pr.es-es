---
title: Configurar transportistas | Documentos de Microsoft
description: Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e1f6af964dad89a8a311f315f8885aaa94b92427
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252348"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="9fe08-103">Configurar transportistas</span><span class="sxs-lookup"><span data-stu-id="9fe08-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="9fe08-104">Configure un código para cada uno de sus transportistas e introduzca información acerca de ellos.</span><span class="sxs-lookup"><span data-stu-id="9fe08-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="9fe08-105">Si introduce una dirección de Internet para el transportista, y éste ofrece servicios de seguimiento de paquetes a través de Internet, utilice la función de seguimiento automático de paquetes.</span><span class="sxs-lookup"><span data-stu-id="9fe08-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="9fe08-106">Para obtener más información, vea [Realizar seguimiento de paquetes](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9fe08-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="9fe08-107">Cuando configura transportistas en los pedidos de venta, también puede especificar los servicios que cada uno ofrece.</span><span class="sxs-lookup"><span data-stu-id="9fe08-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="9fe08-108">Puede configurar un número ilimitado de servicios para cada transportista y especificar un tiempo de envío para cada servicio.</span><span class="sxs-lookup"><span data-stu-id="9fe08-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="9fe08-109">Una vez asignado un servicio de transportista a una línea de pedido de venta, el tiempo de envío del servicio se incluirá en el cálculo del compromiso de entrega de dicha línea.</span><span class="sxs-lookup"><span data-stu-id="9fe08-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="9fe08-110">Para obtener más información, consulte [Calcular las fechas de compromiso de entrega de pedido](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="9fe08-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="9fe08-111">Para configurar un transportista</span><span class="sxs-lookup"><span data-stu-id="9fe08-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="9fe08-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transportistas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9fe08-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9fe08-113">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9fe08-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="9fe08-114">.</span><span class="sxs-lookup"><span data-stu-id="9fe08-114">.</span></span>  
3.  <span data-ttu-id="9fe08-115">Elija la acción **Servicios transportista**.</span><span class="sxs-lookup"><span data-stu-id="9fe08-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="9fe08-116">En **Servicios transportista**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9fe08-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="9fe08-117">Si elimina el transportista de la línea de pedido, también se eliminará el código de servicio de transportista.</span><span class="sxs-lookup"><span data-stu-id="9fe08-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="9fe08-118">Se volverá a calcular el contenido de los campos basados en parte en el servicio de transportista.</span><span class="sxs-lookup"><span data-stu-id="9fe08-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fe08-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9fe08-119">See Also</span></span>
<span data-ttu-id="9fe08-120">[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="9fe08-120">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="9fe08-121">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="9fe08-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="9fe08-122">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="9fe08-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="9fe08-123">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="9fe08-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="9fe08-124">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="9fe08-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="9fe08-125">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="9fe08-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="9fe08-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9fe08-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
