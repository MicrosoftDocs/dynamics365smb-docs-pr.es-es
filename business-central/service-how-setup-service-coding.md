---
title: Configurar códigos para servicios estándar | Documentos de Microsoft
description: Aprenda a configurar códigos para las actividades de servicio que realiza a menudo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 766af833ddef09b72a520e97d47a32fb7b77fd86
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877428"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="7c449-103">Configurar códigos de servicio estándar</span><span class="sxs-lookup"><span data-stu-id="7c449-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="7c449-104">Cuando se realiza un servicio habitual, a menudo es necesario crear documentos de servicio que utilicen líneas de servicio que contengan información similar.</span><span class="sxs-lookup"><span data-stu-id="7c449-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="7c449-105">Para facilitar la creación de estas líneas, puede configurar códigos de servicio estándar que tengan un conjunto predefinido de líneas de servicio.</span><span class="sxs-lookup"><span data-stu-id="7c449-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="7c449-106">Cuando elige el código en un documento de servicio, las líneas se introducen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7c449-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="7c449-107">Puede configurar números de códigos de servicio estándar, y cada código puede tener un número ilimitado de líneas de servicio de diferentes tipos, incluidas artículo, recurso, coste o texto estándar.</span><span class="sxs-lookup"><span data-stu-id="7c449-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="7c449-108">Cree líneas de servicio de cada código de servicio estándar en la ficha **Ficha código servicio estándar**.</span><span class="sxs-lookup"><span data-stu-id="7c449-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="7c449-109">Puede asignar códigos de servicio estándar a los grupos de producto de servicio en la página **Códs. grupo prod. serv. est.**</span><span class="sxs-lookup"><span data-stu-id="7c449-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="7c449-110">Más adelante, cuando cree un documento de servicio, podrá ejecutar la función **Obtener cód. servicio estánd.** para añadir líneas de servicio.</span><span class="sxs-lookup"><span data-stu-id="7c449-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="7c449-111">Puede utilizar el mismo concepto para crear líneas de ventas y documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="7c449-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="7c449-112">Para obtener más información, vea [Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="7c449-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="7c449-113">Para configurar un código de servicio estándar</span><span class="sxs-lookup"><span data-stu-id="7c449-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="7c449-114">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Códigos servicio estándar** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="7c449-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7c449-115">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7c449-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="7c449-116">Rellene las líneas de servicio vinculadas a este código de servicio.</span><span class="sxs-lookup"><span data-stu-id="7c449-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="7c449-117">Para asignar un código de servicio estándar a un grupo de productos de servicio</span><span class="sxs-lookup"><span data-stu-id="7c449-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="7c449-118">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos productos servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="7c449-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7c449-119">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7c449-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="7c449-120">Rellene las líneas de servicio vinculadas a este código de servicio.</span><span class="sxs-lookup"><span data-stu-id="7c449-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c449-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c449-121">See Also</span></span>
[<span data-ttu-id="7c449-122">Gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="7c449-122">Service Management</span></span>](service-service.md)