---
title: Configurar los procesos de solución de problemas | Documentos de Microsoft
description: Aprenda a configurar procesos que ayuden a los representantes de servicio a identificar y resolver problemas con productos de servicio.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 24a4fa9811547acfd3372d3eaf7de7b9f1882c7d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806015"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="de5f2-103">Configuración de la solución de problemas de los productos de servicio</span><span class="sxs-lookup"><span data-stu-id="de5f2-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="de5f2-104">Puede configurar pautas de solución de problemas que ayuden a los técnicos a resolver problemas al proporcionar servicio.</span><span class="sxs-lookup"><span data-stu-id="de5f2-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="de5f2-105">Por ejemplo, las directrices pueden ser una lista de pasos para realizar una reparación, o una serie de preguntas sobre los productos.</span><span class="sxs-lookup"><span data-stu-id="de5f2-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="de5f2-106">Después de configurar las directrices de solución de problemas, puede asignarlas a grupos de productos de servicio, productos de servicio y productos.</span><span class="sxs-lookup"><span data-stu-id="de5f2-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="de5f2-107">Hay una jerarquía de herencia para las directrices.</span><span class="sxs-lookup"><span data-stu-id="de5f2-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="de5f2-108">Si las asigna a un grupo de productos de servicio, los productos incluidos en el grupo heredarán las directrices, a menos que las especifique previamente.</span><span class="sxs-lookup"><span data-stu-id="de5f2-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="de5f2-109">Del mismo modo, los productos de servicio heredarán las directrices de los productos.</span><span class="sxs-lookup"><span data-stu-id="de5f2-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="de5f2-110">Para configurar instrucciones de detección de errores</span><span class="sxs-lookup"><span data-stu-id="de5f2-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="de5f2-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Solución de problemas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="de5f2-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="de5f2-112">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="de5f2-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="de5f2-113">Para asignar directrices de solución de problemas a productos, productos de servicio o grupos de productos de servicio</span><span class="sxs-lookup"><span data-stu-id="de5f2-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="de5f2-114">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), especifique **Productos**, **Productos servicio** o **Grupos producto servicio** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="de5f2-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="de5f2-115">Elija la entidad correspondiente y, a continuación, elija la acción **Solución de problemas**.</span><span class="sxs-lookup"><span data-stu-id="de5f2-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="de5f2-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de5f2-116">See Also</span></span>
[<span data-ttu-id="de5f2-117">Gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="de5f2-117">Service Management</span></span>](service-service.md)