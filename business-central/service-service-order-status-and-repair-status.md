---
title: Estado de pedido de servicio y estado de reparación
description: El campo Estado de la página Pedido servicio y el estado de reparación del producto de servicio, que se representa en el campo Código estado reparación de la página Pedido servicio están relacionados en Gestión servicios. El estado de pedido de servicio indica el estado de reparación de todos los productos de servicio del pedido de servicio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386829"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="d7d83-104">Estado de pedido de servicio y estado de reparación</span><span class="sxs-lookup"><span data-stu-id="d7d83-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="d7d83-105">El campo **Estado** de la página **Pedido servicio** y el estado de reparación del producto de servicio, que se representa en el campo **Código estado reparación** de la página **Pedido servicio** están relacionados en Gestión servicios.</span><span class="sxs-lookup"><span data-stu-id="d7d83-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="d7d83-106">El estado de pedido de servicio indica el estado de reparación de todos los productos de servicio del pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d7d83-107">Estos dos campos de estado no están relacionados con el campo **Estado lanzamiento** de la cabecera del pedido de servicio, que determina el modo en que el almacén controla los productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="d7d83-108">Cada vez que se modifica el estado de reparación de un producto de servicio en un pedido, se actualiza el estado del pedido.</span><span class="sxs-lookup"><span data-stu-id="d7d83-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="d7d83-109">Para mostrar el estado que indica el estado de reparación general de cada producto de servicio, deberá especificar la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="d7d83-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="d7d83-110">El estado de pedido de servicio al que está vinculado cada estado de reparación.</span><span class="sxs-lookup"><span data-stu-id="d7d83-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="d7d83-111">El nivel de prioridad de cada opción de estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="d7d83-112">Cuando se convierte una oferta de servicio en un pedido, cambia el estado de reparación de cada producto de servicio del pedido a **Inicial** y el estado del pedido de servicio cambia a **Pendiente**.</span><span class="sxs-lookup"><span data-stu-id="d7d83-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="d7d83-113">Antes de poder crear órdenes de servicio, debe configurar estados de reparación y prioridades de estado de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="d7d83-114">Para obtener más información, vea [Configurar estados para pedidos de servicio y reparaciones](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="d7d83-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="d7d83-115">Especificar el estado de pedido de servicio para el estado de reparación</span><span class="sxs-lookup"><span data-stu-id="d7d83-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="d7d83-116">Cada estado de reparación se encuentra vinculado a un estado de pedido de servicio determinado.</span><span class="sxs-lookup"><span data-stu-id="d7d83-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="d7d83-117">Las opciones para el estado de la orden de servicio son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7d83-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="d7d83-118">**Pendiente**</span><span class="sxs-lookup"><span data-stu-id="d7d83-118">**Pending**</span></span>
* <span data-ttu-id="d7d83-119">**En proceso**</span><span class="sxs-lookup"><span data-stu-id="d7d83-119">**In Process**</span></span>
* <span data-ttu-id="d7d83-120">**Esperar**</span><span class="sxs-lookup"><span data-stu-id="d7d83-120">**On Hold**</span></span>
* <span data-ttu-id="d7d83-121">**Terminada**</span><span class="sxs-lookup"><span data-stu-id="d7d83-121">**Finished**</span></span>

<span data-ttu-id="d7d83-122">Las opciones de estado de reparación son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7d83-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="d7d83-123">**Inicial**</span><span class="sxs-lookup"><span data-stu-id="d7d83-123">**Initial**</span></span>
* <span data-ttu-id="d7d83-124">**En proceso**</span><span class="sxs-lookup"><span data-stu-id="d7d83-124">**In Process**</span></span>
* <span data-ttu-id="d7d83-125">**Remitido**</span><span class="sxs-lookup"><span data-stu-id="d7d83-125">**Referred**</span></span>
* <span data-ttu-id="d7d83-126">**Parcialmente servido**</span><span class="sxs-lookup"><span data-stu-id="d7d83-126">**Partly Serviced**</span></span>
* <span data-ttu-id="d7d83-127">**Oferta terminada**</span><span class="sxs-lookup"><span data-stu-id="d7d83-127">**Quote Finished**</span></span>
* <span data-ttu-id="d7d83-128">**Esperando al cliente**</span><span class="sxs-lookup"><span data-stu-id="d7d83-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="d7d83-129">**Componente pedido**</span><span class="sxs-lookup"><span data-stu-id="d7d83-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="d7d83-130">**Componente recibido**</span><span class="sxs-lookup"><span data-stu-id="d7d83-130">**Spare Part Received**</span></span>
* <span data-ttu-id="d7d83-131">**Terminada**</span><span class="sxs-lookup"><span data-stu-id="d7d83-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="d7d83-132">Pendiente</span><span class="sxs-lookup"><span data-stu-id="d7d83-132">Pending</span></span>

<span data-ttu-id="d7d83-133">El estado de pedido de servicio **Pendiente** indica que el servicio puede iniciarse o continuar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="d7d83-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="d7d83-134">Por lo tanto, las opciones de estado de reparación **Inicial**, **Remitido**, **Parcialmente servido** y **Componente recibido** pueden vincularse a este estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="d7d83-135">En proceso</span><span class="sxs-lookup"><span data-stu-id="d7d83-135">In Process</span></span>

<span data-ttu-id="d7d83-136">El estado de pedido de servicio **En proceso** indica que el servicio está en curso.</span><span class="sxs-lookup"><span data-stu-id="d7d83-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="d7d83-137">Por lo tanto, las opciones de estado de reparación **En proceso** y **Componente pedido** pueden vincularse a este estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="d7d83-138">Si vincula el estado **Componente pedido** al estado **En proceso** de un pedido de servicio, también deberá vincular el estado **Componente recibido** a este estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="d7d83-139">Esperar</span><span class="sxs-lookup"><span data-stu-id="d7d83-139">On Hold</span></span>

<span data-ttu-id="d7d83-140">El estado de pedido de servicio **En espera** indica que el servicio se encuentra retenido de forma temporal a la espera de una respuesta del cliente o de componentes para que pueda iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="d7d83-141">Por lo tanto, las opciones de estado de reparación **Oferta terminada**, **Componente pedido** y **Esperando al cliente** pueden vincularse a este estado de pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="d7d83-142">Terminada</span><span class="sxs-lookup"><span data-stu-id="d7d83-142">Finished</span></span>

<span data-ttu-id="d7d83-143">El estado de pedido de servicio **Terminado** indica que se ha completado el servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="d7d83-144">Por lo tanto, el estado de reparación **Terminado** está vinculado a este estado.</span><span class="sxs-lookup"><span data-stu-id="d7d83-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="d7d83-145">Asignar prioridad al estado de pedido de servicio</span><span class="sxs-lookup"><span data-stu-id="d7d83-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="d7d83-146">Cuando se modifica el estado de reparación de un producto de servicio, se identifican las opciones de estado de pedido de servicio vinculadas a las distintas opciones de estado de reparación de todos los productos de servicio del pedido.</span><span class="sxs-lookup"><span data-stu-id="d7d83-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="d7d83-147">Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona la opción del estado de pedido de servicio con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="d7d83-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="d7d83-148">Deberá decidir qué estado de pedido de servicio contiene la información más importante acerca del estado del pedido de servicio y asignar la prioridad más alta a ese estado, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d7d83-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="d7d83-149">Luego, cuando crea una nueva orden de servicio y le agrega elementos de servicio, el campo **Prioridad** en el encabezado de la orden de servicio se actualiza según las prioridades de los artículos de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7d83-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="d7d83-150">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d7d83-150">Example</span></span>

<span data-ttu-id="d7d83-151">Un ejemplo típico de asignación de nivel de prioridad podría ser:</span><span class="sxs-lookup"><span data-stu-id="d7d83-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="d7d83-152">En proceso: Alta</span><span class="sxs-lookup"><span data-stu-id="d7d83-152">In Process - High</span></span>  
* <span data-ttu-id="d7d83-153">Pendiente: Media alta</span><span class="sxs-lookup"><span data-stu-id="d7d83-153">Pending - Medium high</span></span>  
* <span data-ttu-id="d7d83-154">En espera: Media baja</span><span class="sxs-lookup"><span data-stu-id="d7d83-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="d7d83-155">Terminado: Baja</span><span class="sxs-lookup"><span data-stu-id="d7d83-155">Finished - Low</span></span>  

<span data-ttu-id="d7d83-156">Por ejemplo, si un producto de servicio tiene el estado de reparación **Inicial**, vinculado al estado de pedido de servicio **Pendiente**, otro producto tiene el estado **En proceso**, vinculado al estado de pedido de servicio **En proceso**, y el tercer producto tiene el estado **Componente pedido**, vinculado al estado de pedido de servicio **En espera**, el estado de pedido de servicio resultante será **En proceso**, porque tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="d7d83-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d7d83-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7d83-157">See Also</span></span>

[<span data-ttu-id="d7d83-158">Configuración de estados para órdenes y reparaciones de servicio</span><span class="sxs-lookup"><span data-stu-id="d7d83-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="d7d83-159">Configurar la gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="d7d83-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]