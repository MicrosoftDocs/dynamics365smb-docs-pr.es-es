---
title: 'Detalles de diseño: Aprovisionamiento y demanda | Documentos de Microsoft'
description: "\"Demanda\" es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción. Además, el programa permite tipos de demanda más técnicos, como inventario negativo y devoluciones de compra."
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ad6684bb1fefe10fc965c3c8a7780c6aa8a9d685
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806449"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="de1dc-104">Detalles de diseño: Demanda y aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="de1dc-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="de1dc-105">"Demanda" es el término común usado para todo tipo de demanda bruta, como un pedido de venta o una necesidad de componente de una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="de1dc-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="de1dc-106">Además, el programa permite tipos de demanda más técnicos, como inventario negativo y devoluciones de compra.</span><span class="sxs-lookup"><span data-stu-id="de1dc-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="de1dc-107">Suministro es el término habitual que se usa para cualquier tipo de cantidad positiva o de entrada, como inventario, compras, ensamblado, producción o transferencias de entrada.</span><span class="sxs-lookup"><span data-stu-id="de1dc-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="de1dc-108">Además, una devolución de ventas también puede representar un aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="de1dc-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="de1dc-109">Para organizar los numerosos orígenes de demanda y suministro, el sistema de planificación las organiza en dos escalas temporales denominadas perfiles de inventario.</span><span class="sxs-lookup"><span data-stu-id="de1dc-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="de1dc-110">Un perfil contiene eventos de demanda y el otro incluye los eventos de suministro correspondientes.</span><span class="sxs-lookup"><span data-stu-id="de1dc-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="de1dc-111">Cada evento representa una entidad de red de pedidos, como una línea de pedido de venta, un movimiento de producto o una línea de orden de producción.</span><span class="sxs-lookup"><span data-stu-id="de1dc-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="de1dc-112">Cuando se cargan los perfiles de inventario, se equilibran los distintos conjuntos de demanda-suministro para generar un plan de suministro que cumpla los objetivos enumerados.</span><span class="sxs-lookup"><span data-stu-id="de1dc-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="de1dc-113">Los parámetros de planificación y los niveles de inventario son otros tipos de demanda y suministro respectivamente, en los que se realizará una contrapartida integrada para reponer los productos en existencias.</span><span class="sxs-lookup"><span data-stu-id="de1dc-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="de1dc-114">Para obtener más información, consulte [Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="de1dc-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="de1dc-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de1dc-115">See Also</span></span>  
 <span data-ttu-id="de1dc-116">[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="de1dc-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="de1dc-117">[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="de1dc-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="de1dc-118">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="de1dc-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
