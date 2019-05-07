---
title: Configuración de estados para órdenes y reparaciones de servicio | Documentos de Microsoft
description: Debe configurar nueve opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 64afbccba0573445902efdaf3c3919dacdb40e8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "928421"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="fb148-103">Configuración de estados para órdenes y reparaciones de servicio</span><span class="sxs-lookup"><span data-stu-id="fb148-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="fb148-104">Debe configurar opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="fb148-105">Debe configurar como mínimo nueve opciones de estado de reparación que identifiquen situaciones o acciones realizadas durante el servicio de productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="fb148-106">Puede establecer el nivel de prioridad de las opciones de estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="fb148-107">Las cuatro prioridades son: Alta, Media alta, Media baja y Baja.</span><span class="sxs-lookup"><span data-stu-id="fb148-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  

<span data-ttu-id="fb148-108">Cuando se modifica el estado de reparación de un producto de servicio de un pedido de servicio, se actualiza el estado de la orden de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="fb148-109">El estado de reparación de cada producto de servicio se encuentra vinculado al estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="fb148-110">Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona el estado de pedido de servicio con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="fb148-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="fb148-111">Para configurar un estado de reparación</span><span class="sxs-lookup"><span data-stu-id="fb148-111">To set up a repair status</span></span>  
1. <span data-ttu-id="fb148-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Estado reparación** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="fb148-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="fb148-113">Cree un estado de reparación nuevo.</span><span class="sxs-lookup"><span data-stu-id="fb148-113">Create a new repair status.</span></span>  
3. <span data-ttu-id="fb148-114">Rellene los campos **Código** y **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="fb148-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="fb148-115">En el campo **Estado ped. servicio**, seleccione el estado de pedido para enlazar el estado de reparación.</span><span class="sxs-lookup"><span data-stu-id="fb148-115">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="fb148-116">El campo **Prioridad** muestra la prioridad del estado de pedido de servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="fb148-116">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="fb148-117">Elegir un estado de reparación.</span><span class="sxs-lookup"><span data-stu-id="fb148-117">Choose a repair status.</span></span> <span data-ttu-id="fb148-118">Puede seleccionar solo uno.</span><span class="sxs-lookup"><span data-stu-id="fb148-118">You can choose only one.</span></span>  
6. <span data-ttu-id="fb148-119">Para poder registrar pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Registro permitido**.</span><span class="sxs-lookup"><span data-stu-id="fb148-119">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="fb148-120">Para poder cambiar manualmente la opción de estado de pedido de servicio a la opción **Pendiente** en pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Estado pendiente permitido**.</span><span class="sxs-lookup"><span data-stu-id="fb148-120">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="fb148-121">Elija las casillas **Estado en proceso permitido**, **Estado terminado permitido** y **Estado en espera permitido** del mismo modo.</span><span class="sxs-lookup"><span data-stu-id="fb148-121">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="fb148-122">Para configurar prioridades de estado de servicio</span><span class="sxs-lookup"><span data-stu-id="fb148-122">To set up service status priorities</span></span>  
1. <span data-ttu-id="fb148-123">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Estado pedido servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="fb148-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fb148-124">Seleccione el estado de pedido de servicio para el que desea establecer la prioridad.</span><span class="sxs-lookup"><span data-stu-id="fb148-124">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="fb148-125">En el campo **Prioridad**, seleccione la prioridad que desea para el estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb148-125">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="fb148-126">Repita este paso para cada estado.</span><span class="sxs-lookup"><span data-stu-id="fb148-126">Repeat this step for each status.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb148-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb148-127">See Also</span></span>  
[<span data-ttu-id="fb148-128">Estado de pedido de servicio y estado de reparación</span><span class="sxs-lookup"><span data-stu-id="fb148-128">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="fb148-129">Configurar la gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="fb148-129">Setting Up Service Management</span></span>](service-setup-service.md)  
