---
title: "Configuración de estados para órdenes y reparaciones de servicio | Documentos de Microsoft"
description: "Debe configurar nueve opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio."
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
ms.openlocfilehash: 8ffd5d6893b2b6c8ce7b7377c586f4f5414279b5
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="37022-103">Configuración de estados para órdenes y reparaciones de servicio</span><span class="sxs-lookup"><span data-stu-id="37022-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="37022-104">Debe configurar opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="37022-105">Debe configurar como mínimo nueve opciones de estado de reparación que identifiquen situaciones o acciones realizadas durante el servicio de productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="37022-106">Puede establecer el nivel de prioridad de las opciones de estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="37022-107">Las cuatro prioridades son: Alta, Media alta, Media baja y Baja.</span><span class="sxs-lookup"><span data-stu-id="37022-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="37022-108">Cuando se modifica el estado de reparación de un producto de servicio de un pedido de servicio, se actualiza el estado de la orden de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="37022-109">El estado de reparación de cada producto de servicio se encuentra vinculado al estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="37022-110">Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona el estado de pedido de servicio con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="37022-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="37022-111">Para configurar un estado de reparación</span><span class="sxs-lookup"><span data-stu-id="37022-111">To set up a repair status</span></span>  
1. <span data-ttu-id="37022-112">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Estado reparación** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="37022-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="37022-113">2.</span><span class="sxs-lookup"><span data-stu-id="37022-113">2.</span></span> <span data-ttu-id="37022-114">Cree un estado de reparación nuevo.</span><span class="sxs-lookup"><span data-stu-id="37022-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="37022-115">Rellene los campos **Código** y **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="37022-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="37022-116">En el campo **Estado ped. servicio**, seleccione el estado de pedido para enlazar el estado de reparación.</span><span class="sxs-lookup"><span data-stu-id="37022-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="37022-117">El campo **Prioridad** muestra la prioridad del estado de pedido de servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="37022-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="37022-118">Elegir un estado de reparación.</span><span class="sxs-lookup"><span data-stu-id="37022-118">Choose a repair status.</span></span> <span data-ttu-id="37022-119">Puede seleccionar solo uno.</span><span class="sxs-lookup"><span data-stu-id="37022-119">You can choose only one.</span></span>  
6. <span data-ttu-id="37022-120">Para poder registrar pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Registro permitido**.</span><span class="sxs-lookup"><span data-stu-id="37022-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="37022-121">Para poder cambiar manualmente la opción de estado de pedido de servicio a la opción **Pendiente** en pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Estado pendiente permitido**.</span><span class="sxs-lookup"><span data-stu-id="37022-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="37022-122">Elija las casillas **Estado en proceso permitido**, **Estado terminado permitido** y **Estado en espera permitido** del mismo modo.</span><span class="sxs-lookup"><span data-stu-id="37022-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="37022-123">Para configurar prioridades de estado de servicio</span><span class="sxs-lookup"><span data-stu-id="37022-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="37022-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Estado pedido servicio** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="37022-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37022-125">Seleccione el estado de pedido de servicio para el que desea establecer la prioridad.</span><span class="sxs-lookup"><span data-stu-id="37022-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="37022-126">En el campo **Prioridad**, seleccione la prioridad que desea para el estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="37022-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="37022-127">Repita este paso para cada estado.</span><span class="sxs-lookup"><span data-stu-id="37022-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37022-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="37022-128">See Also</span></span>  
[<span data-ttu-id="37022-129">Descripción del estado de pedido de servicio y estado de reparación</span><span class="sxs-lookup"><span data-stu-id="37022-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="37022-130">Configurar la gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="37022-130">Setting Up Service Management</span></span>](service-setup-service.md)  

