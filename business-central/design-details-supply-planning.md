---
title: 'Detalles de diseño: Gestión de almacenes | Documentos de Microsoft'
description: Este tema proporciona un resumen de los conceptos y los principios que se usan en las características de planificación de suministros en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 51fbc5e8e99cedd16f50d471a3cc36958549ecec
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787126"
---
# <a name="design-details-supply-planning"></a><span data-ttu-id="290cd-103">Detalles de diseño: Planificación de aprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="290cd-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="290cd-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de planificación de suministros en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="290cd-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="290cd-105">Explica cómo funciona el sistema de planificación y cómo ajustar los algoritmos para cumplir con los requisitos de planificación en distintos entornos.</span><span class="sxs-lookup"><span data-stu-id="290cd-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="290cd-106">Primero introduce los conceptos centrales de la solución y después describe la lógica del mecanismo principal, equilibrado del aprovisionamiento, antes de continuar explicando cómo se realiza la planificación del inventario con el uso de directivas de reaprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="290cd-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="290cd-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="290cd-107">In This Section</span></span>  
[<span data-ttu-id="290cd-108">Detalles de diseño: Conceptos centrales del sistema de planificación</span><span class="sxs-lookup"><span data-stu-id="290cd-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="290cd-109">Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones</span><span class="sxs-lookup"><span data-stu-id="290cd-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="290cd-110">Detalles de diseño: Equilibrio de aprovisionamiento y demanda</span><span class="sxs-lookup"><span data-stu-id="290cd-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="290cd-111">Detalles de diseño: Gestión de directivas de reaprovisionamiento</span><span class="sxs-lookup"><span data-stu-id="290cd-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="290cd-112">Detalles de diseño: Parámetros de la planificación</span><span class="sxs-lookup"><span data-stu-id="290cd-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="290cd-113">Detalles de diseño: Tabla de asignación de planificación</span><span class="sxs-lookup"><span data-stu-id="290cd-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="290cd-114">Detalles de diseño: Demanda en almacén vacío</span><span class="sxs-lookup"><span data-stu-id="290cd-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="290cd-115">Detalles de diseño: Transferencias en planificación</span><span class="sxs-lookup"><span data-stu-id="290cd-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)
