---
title: "Detalles de diseño: Integración con inventario | Documentos de Microsoft"
description: "Las áreas de aplicación de Gestión de almacén e Inventario interactúan entre sí en el inventario físico y en el ajuste de inventario o de almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: df77e655c58b6eba6f431ef66be3152f56ac634f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="fa0e1-103">Detalles de diseño: Integración con inventario</span><span class="sxs-lookup"><span data-stu-id="fa0e1-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="fa0e1-104">Las áreas de aplicación de Gestión de almacén e Inventario interactúan entre sí en el inventario físico y en el ajuste de inventario o de almacén.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="fa0e1-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="fa0e1-105">Physical Inventory</span></span>  
 <span data-ttu-id="fa0e1-106">La ventana **Diario de inventario físico de almacén** se usa en la ventana **Diario inventario físico** para todas las ubicaciones de almacén avanzadas.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="fa0e1-107">Se calcula el inventario en el nivel de ubicación y se proporciona una lista impresa al empleado del almacén.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="fa0e1-108">La lista muestra los productos en los que se deben contar las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="fa0e1-109">El empleado de almacén introduce la cantidad contada en la ventana **Diario de inventario físico de almacén** y, a continuación, registra el diario.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="fa0e1-110">Si la cantidad contada es mayor que la cantidad en la línea del diario, se registra un movimiento para esta diferencia desde la ubicación de ajuste predeterminada a la ubicación contada.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="fa0e1-111">Esto aumenta la cantidad en la ubicación contada y reduce la cantidad en la ubicación de ajuste predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="fa0e1-112">Si la cantidad contada es menor que la cantidad en la línea del diario, se registra un movimiento para esta diferencia desde la ubicación contada a la ubicación de ajuste predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="fa0e1-113">Esto reduce la cantidad en la ubicación contada y aumenta la cantidad en la ubicación de ajuste predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="fa0e1-114">En las configuraciones avanzadas de almacén, el valor del campo **Cantidad (calculada)** se recupera de los movimientos de producto, y valor del campo **Cantidad (stock físico)** se recupera de los movimientos de almacén, excepto el contenido de la ubicación de ajuste.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="fa0e1-115">El campo **Cantidad** especifica la diferencia entre los dos primeros campos, que deben ser iguales al contenido de la ubicación de ajuste.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="fa0e1-116">Cuando se registra el diario de inventario físico, se actualizan el inventario y la ubicación de ajuste predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="fa0e1-117">Ajustes de almacén en los movimientos de productos</span><span class="sxs-lookup"><span data-stu-id="fa0e1-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="fa0e1-118">Use la ventana **Diario de producto** y la función **Calcular ajuste almacén** para ajustar el inventario en el movimiento de producto según un ajuste que se ha realizado en la cantidad de producto en una ubicación de almacén.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="fa0e1-119">Para crear un vínculo entre el inventario y el almacén, debe definir una ubicación de ajuste predeterminado por ubicación.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="fa0e1-120">La ubicación de ajuste predeterminado registra los productos en el almacén al registrar una entrada de existencias.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="fa0e1-121">No obstante, si se registra una disminución, la cantidad en la ubicación predeterminada también disminuye.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="fa0e1-122">En ambos casos, se crean movimientos de producto y movimientos de almacén.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="fa0e1-123">La ubicación de ajuste no se incluye en el cálculo de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="fa0e1-124">Si desea ajustar el contenido de la ubicación, puede utilizar el diario de productos de almacén, desde el cual podrá introducir el número de producto, el código de la zona, el código de ubicación y la cantidad que se desee ajustar.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="fa0e1-125">Si introduce una cantidad positiva y registra la línea, el inventario almacenado en la ubicación se incrementará, y la cantidad de la ubicación de ajuste predeterminada se reducirá en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa0e1-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa0e1-126">See Also</span></span>  
 <span data-ttu-id="fa0e1-127">[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="fa0e1-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="fa0e1-128">Detalles de diseño: Disponibilidad en el almacén</span><span class="sxs-lookup"><span data-stu-id="fa0e1-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
