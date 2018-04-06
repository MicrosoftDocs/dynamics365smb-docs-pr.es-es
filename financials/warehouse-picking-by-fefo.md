---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: "El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc45bf06ab5d12cf393d48b7b1c295db28f56b3b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="bf73e-103">Habilitar la realización de picking de productos por FEFO</span><span class="sxs-lookup"><span data-stu-id="bf73e-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="bf73e-104">El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.</span><span class="sxs-lookup"><span data-stu-id="bf73e-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="bf73e-105">Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf73e-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="bf73e-106">El artículo debe tener un número de serie/lote.</span><span class="sxs-lookup"><span data-stu-id="bf73e-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="bf73e-107">En el código del seguimiento de producto del artículo de instalación, debe seleccionarse el campo **Seguimiento almacén específico NS** o el **Seguimiento almacén específico lote**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="bf73e-108">El artículo debe registrarse para inventariar con una fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="bf73e-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="bf73e-109">En la ficha de almacén, debe estar seleccionada la casilla **Picking requerido**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="bf73e-110">En la ficha de almacén, debe seleccionar la casilla **Picking según FEFO (Primero en caducar, primero en salir)**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="bf73e-111">En la ficha de almacén, debe estar seleccionada la casilla **Ubicac. obligatoria**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="bf73e-112">Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.</span><span class="sxs-lookup"><span data-stu-id="bf73e-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bf73e-113">Si algún artículo numerado con serie/lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.</span><span class="sxs-lookup"><span data-stu-id="bf73e-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>  

 <span data-ttu-id="bf73e-114">Si dos productos con número de serie o lote tienen la misma fecha de caducidad, el programa selecciona aquel cuyo número de lote o de serie sea menor.</span><span class="sxs-lookup"><span data-stu-id="bf73e-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span> <span data-ttu-id="bf73e-115">Si los números de lote o de serie son iguales, entonces selecciona el producto que se registró en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="bf73e-115">If the serial or lot numbers are the same, then the program selects the item that was registered first.</span></span>  

> [!NOTE]  
>  -   <span data-ttu-id="bf73e-116">Cuando se realiza el picking de productos con números de lote/serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.</span><span class="sxs-lookup"><span data-stu-id="bf73e-116">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
> -   <span data-ttu-id="bf73e-117">Para activar movimientos según el FEFO, en la ventana **Movimiento inventario** o en la **Hoja trabajo movimiento**, debe dejar en blanco el campo **De ubicación**.</span><span class="sxs-lookup"><span data-stu-id="bf73e-117">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
> -   <span data-ttu-id="bf73e-118">Si se selecciona el campo **Registro caducidad requerido**, sólo los productos que no caducan se incluirán en el picking.</span><span class="sxs-lookup"><span data-stu-id="bf73e-118">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="bf73e-119">Esto se aplica incluso si no utiliza picking según FEFO.</span><span class="sxs-lookup"><span data-stu-id="bf73e-119">This applies even if you are not using Pick according to FEFO.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf73e-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf73e-120">See Also</span></span>  
<span data-ttu-id="bf73e-121">[Realización de picking de artículos](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="bf73e-121">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="bf73e-122">[Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="bf73e-122">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="bf73e-123">[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="bf73e-123">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="bf73e-124">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="bf73e-124">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="bf73e-125">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="bf73e-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="bf73e-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf73e-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

