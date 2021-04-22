---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784072"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="d3e72-103">Habilitar la realización de picking de productos por FEFO</span><span class="sxs-lookup"><span data-stu-id="d3e72-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="d3e72-104">El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.</span><span class="sxs-lookup"><span data-stu-id="d3e72-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="d3e72-105">Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3e72-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="d3e72-106">El artículo debe tener un número de serie/lote.</span><span class="sxs-lookup"><span data-stu-id="d3e72-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="d3e72-107">En el código del seguimiento de producto del artículo, deben seleccionarse los campos **Seguim. nº serie almacén** o **Seguim. lote almacén**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="d3e72-108">El artículo debe registrarse para inventariar con una fecha de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="d3e72-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="d3e72-109">En la ubicación, los controles de alternancia **Picking requerido**, **Picking según FEFO (Primero en caducar, primero en salir)** y **Ubicación obligatoria** deben estar activados.</span><span class="sxs-lookup"><span data-stu-id="d3e72-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="d3e72-110">Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.</span><span class="sxs-lookup"><span data-stu-id="d3e72-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d3e72-111">Si algún artículo numerado con serie o lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.</span><span class="sxs-lookup"><span data-stu-id="d3e72-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="d3e72-112">Si dos productos con número de serie o lote tienen la misma fecha de caducidad, la aplicación selecciona aquel cuyo número de lote o de serie sea menor.</span><span class="sxs-lookup"><span data-stu-id="d3e72-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="d3e72-113">Cuando se realiza el picking de productos con números de lote o serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.</span><span class="sxs-lookup"><span data-stu-id="d3e72-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="d3e72-114">Para activar movimientos según el FEFO, deje en blanco el campo **Desde ubicación** en la página **Movimiento de inventario** o en las páginas **Hoja trabajo movimiento**.</span><span class="sxs-lookup"><span data-stu-id="d3e72-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="d3e72-115">Si el campo **Registro caducidad requerido** está seleccionado en **Ficha cód. seguim. prod.**, solo los productos que no se caducan se incluirán en el picking y las líneas se ordenan según el principio FEFO.</span><span class="sxs-lookup"><span data-stu-id="d3e72-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3e72-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d3e72-116">See Also</span></span>  
<span data-ttu-id="d3e72-117">[Realización de picking de artículos](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="d3e72-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="d3e72-118">[Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="d3e72-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="d3e72-119">[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="d3e72-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="d3e72-120">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="d3e72-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="d3e72-121">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="d3e72-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d3e72-122">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d3e72-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]