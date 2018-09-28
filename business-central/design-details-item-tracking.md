---
title: "Detalles de diseño: Seguimiento de productos | Documentos de Microsoft"
description: "Este tema proporciona un resumen de los detalles de diseño del seguimiento de producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 93207b1bbccd389c6a3e60b0587cdb0044bf2259
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-item-tracking"></a><span data-ttu-id="cf243-103">Detalles de diseño: Seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="cf243-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="cf243-104">A medida que el flujo de productos en la cadena de suministro actual se hace cada vez más complejo, la posibilidad de hacer un seguimiento de los productos cobra mayor importancia para las empresas implicadas.</span><span class="sxs-lookup"><span data-stu-id="cf243-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="cf243-105">La supervisión del flujo de transacciones de un producto es un requisito legal en el suministro de productos médicos y químicos, pero en otros sectores se pueden supervisar los productos con garantías o fechas de vencimiento por motivos de servicio al cliente.</span><span class="sxs-lookup"><span data-stu-id="cf243-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="cf243-106">El sistema de seguimiento de productos debe proveer a una empresa una fácil gestión de los números de serie y de lote, de forma que cada uno de ellos corresponda a un único artículo de mercancía: cuándo y dónde se ha recibido, dónde se ha almacenado y cuándo y dónde se ha vendido.</span><span class="sxs-lookup"><span data-stu-id="cf243-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="cf243-107">ha expandido gradualmente la cobertura de esta exigencia empresarial y hoy proporciona funciones de aplicación global y a una base sólida sobre la que desarrollar extensiones.</span><span class="sxs-lookup"><span data-stu-id="cf243-107"> has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="cf243-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cf243-108">In This Section</span></span>  
* [<span data-ttu-id="cf243-109">Detalles de diseño: Diseño de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="cf243-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
* [<span data-ttu-id="cf243-110">Detalles de diseño: Estructura de registro de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="cf243-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
* [<span data-ttu-id="cf243-111">Detalles de diseño: registros de seguimiento de productos históricos frente a activos</span><span class="sxs-lookup"><span data-stu-id="cf243-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
* [<span data-ttu-id="cf243-112">Detalles de diseño: Ventana de líneas de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="cf243-112">Design Details: Item Tracking Lines Window</span></span>](design-details-item-tracking-lines-window.md)  
* [<span data-ttu-id="cf243-113">Detalles de diseño: Disponibilidad de seguimiento de productos</span><span class="sxs-lookup"><span data-stu-id="cf243-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
* [<span data-ttu-id="cf243-114">Detalles de diseño: Seguimiento de productos y planificación</span><span class="sxs-lookup"><span data-stu-id="cf243-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
* [<span data-ttu-id="cf243-115">Detalles de diseño: Seguimiento de productos y reservas</span><span class="sxs-lookup"><span data-stu-id="cf243-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
* [<span data-ttu-id="cf243-116">Detalles de diseño: Seguimiento de productos en el almacén</span><span class="sxs-lookup"><span data-stu-id="cf243-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)

