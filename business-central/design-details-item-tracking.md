---
title: 'Detalles de diseño: Seguimiento de productos | Documentos de Microsoft'
description: Este tema proporciona un resumen de los detalles de diseño del seguimiento de producto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 50ae6f2f3538269cc7c82dd2d84644a1a31d7f56
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751360"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="b2488-103">Detalles de diseño: Seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="b2488-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="b2488-104">A medida que el flujo de productos en la cadena de suministro actual se hace cada vez más complejo, la posibilidad de hacer un seguimiento de los productos cobra mayor importancia para las empresas implicadas.</span><span class="sxs-lookup"><span data-stu-id="b2488-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="b2488-105">La supervisión del flujo de transacciones de un producto es un requisito legal en el suministro de productos médicos y químicos, pero en otros sectores se pueden supervisar los productos con garantías o fechas de vencimiento por motivos de servicio al cliente.</span><span class="sxs-lookup"><span data-stu-id="b2488-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="b2488-106">El sistema de seguimiento de productos debe proveer a una empresa una fácil gestión de los números de serie y de lote, de forma que cada uno de ellos corresponda a un único artículo de mercancía: cuándo y dónde se ha recibido, dónde se ha almacenado y cuándo y dónde se ha vendido.</span><span class="sxs-lookup"><span data-stu-id="b2488-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b2488-107">ha expandido gradualmente la cobertura de esta exigencia empresarial y hoy proporciona funciones de aplicación global y a una base sólida sobre la que desarrollar extensiones.</span><span class="sxs-lookup"><span data-stu-id="b2488-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="b2488-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b2488-108">In This Section</span></span>  
[<span data-ttu-id="b2488-109">Detalles de diseño: Diseño de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="b2488-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="b2488-110">Detalles de diseño: Estructura de registro de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="b2488-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="b2488-111">Detalles de diseño: registros de seguimiento de productos históricos frente a activos</span><span class="sxs-lookup"><span data-stu-id="b2488-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="b2488-112">Detalles de diseño: página Líns. seguim. prod.</span><span class="sxs-lookup"><span data-stu-id="b2488-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="b2488-113">Detalles de diseño: Disponibilidad de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="b2488-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="b2488-114">Detalles de diseño: Seguimiento de productos y planificación</span><span class="sxs-lookup"><span data-stu-id="b2488-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="b2488-115">Detalles de diseño: Seguimiento de productos y reservas</span><span class="sxs-lookup"><span data-stu-id="b2488-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="b2488-116">Detalles de diseño: Seguimiento de productos en el almacén</span><span class="sxs-lookup"><span data-stu-id="b2488-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
