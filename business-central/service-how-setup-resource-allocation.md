---
title: "Configurar asignación de recursos | Documentos de Microsoft"
description: "Obtener información sobre cómo el sistema puede ayudar a asegurar que se asigna a alguien que tiene las habilidades necesarias para proporcionar un servicio."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7ce128aa32d650cf756117ab46987167d9a3781a
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="93c02-103">Configurar asignación de recursos</span><span class="sxs-lookup"><span data-stu-id="93c02-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="93c02-104">Para garantizar que una tarea de servicio esté bien efectuada, es importante encontrar un recurso que esté cualificado para hacer el trabajo.</span><span class="sxs-lookup"><span data-stu-id="93c02-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="93c02-105">Puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] de forma que resulte fácil asignar a quien tiene las habilidades correctas para el trabajo.</span><span class="sxs-lookup"><span data-stu-id="93c02-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="93c02-106">En [!INCLUDE[d365fin](includes/d365fin_md.md)], llamamos a esto _asignación de recursos_.</span><span class="sxs-lookup"><span data-stu-id="93c02-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="93c02-107">Puede asignar recursos basándose en las habilidades, disponibilidad o si se encuentran en la misma zona que el cliente.</span><span class="sxs-lookup"><span data-stu-id="93c02-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="93c02-108">Para usar la asignación de recursos, debe configurar:</span><span class="sxs-lookup"><span data-stu-id="93c02-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="93c02-109">Las habilidades necesarias para la reparación y mantenimiento de productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="93c02-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="93c02-110">Las asigna a productos y recursos de servicio.</span><span class="sxs-lookup"><span data-stu-id="93c02-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="93c02-111">Las áreas geográficas, llamadas zonas, que define para su mercado.</span><span class="sxs-lookup"><span data-stu-id="93c02-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="93c02-112">Por ejemplo, este, oeste, central, etc.</span><span class="sxs-lookup"><span data-stu-id="93c02-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="93c02-113">Las asigna a clientes y recursos.</span><span class="sxs-lookup"><span data-stu-id="93c02-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="93c02-114">Si desea mostrar las habilidades y zonas del recurso y si desea mostrar una advertencia si alguien elige un recurso no calificado, o un recurso que no está en la zona de cliente.</span><span class="sxs-lookup"><span data-stu-id="93c02-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="93c02-115">Para configurar habilidades</span><span class="sxs-lookup"><span data-stu-id="93c02-115">To set up skills</span></span>
1. <span data-ttu-id="93c02-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cualificaciones** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-117">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="93c02-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="93c02-118">Para asignar habilidades a productos y recursos de servicio</span><span class="sxs-lookup"><span data-stu-id="93c02-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="93c02-119">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos de servicio** o **Recursos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-120">Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="93c02-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="93c02-121">Para productos de servicio, elija **Cualificaciones recurso**.</span><span class="sxs-lookup"><span data-stu-id="93c02-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="93c02-122">Para los recursos, elija **Cualificaciones**.</span><span class="sxs-lookup"><span data-stu-id="93c02-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="93c02-123">Para configurar zonas</span><span class="sxs-lookup"><span data-stu-id="93c02-123">To set up zones</span></span>
1. <span data-ttu-id="93c02-124">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Zonas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-125">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="93c02-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="93c02-126">Para asignar zonas a clientes y recursos</span><span class="sxs-lookup"><span data-stu-id="93c02-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="93c02-127">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Clientes** o **Recursos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-128">Abra la ficha del producto o recurso de servicio y elija una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="93c02-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="93c02-129">Para los clientes, elija una zona en el campo **Cód. zona servicio**.</span><span class="sxs-lookup"><span data-stu-id="93c02-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="93c02-130">Para los recursos, elija la acción de **Zonas servicio**.</span><span class="sxs-lookup"><span data-stu-id="93c02-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="93c02-131">Para especificar qué mostrar cuando seleccione un recurso</span><span class="sxs-lookup"><span data-stu-id="93c02-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="93c02-132">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Config. servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="93c02-133">En el campo **Opción cualificaciones recurso**, seleccione una de las opciones descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="93c02-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="93c02-134">**Opción**</span><span class="sxs-lookup"><span data-stu-id="93c02-134">**Option**</span></span>|<span data-ttu-id="93c02-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="93c02-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="93c02-136">Código mostrado</span><span class="sxs-lookup"><span data-stu-id="93c02-136">Code Shown</span></span> | <span data-ttu-id="93c02-137">Se muestra solo el código.</span><span class="sxs-lookup"><span data-stu-id="93c02-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="93c02-138">Advertencia mostrada</span><span class="sxs-lookup"><span data-stu-id="93c02-138">Warning Displayed</span></span> | <span data-ttu-id="93c02-139">Muestra la información y una advertencia si elige un recurso que no está calificado.</span><span class="sxs-lookup"><span data-stu-id="93c02-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="93c02-140">No utilizado</span><span class="sxs-lookup"><span data-stu-id="93c02-140">Not Used</span></span> | <span data-ttu-id="93c02-141">No muestra esta información.</span><span class="sxs-lookup"><span data-stu-id="93c02-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="93c02-142">Para actualizar capacidad de recurso</span><span class="sxs-lookup"><span data-stu-id="93c02-142">To update resource capacity</span></span>  
<span data-ttu-id="93c02-143">Es posible que tenga que cambiar la capacidad de los recursos.</span><span class="sxs-lookup"><span data-stu-id="93c02-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="93c02-144">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Capacidad recurso** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-145">Elija el recurso y, a continuación, elija la acción **Fijar capacidad**.</span><span class="sxs-lookup"><span data-stu-id="93c02-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="93c02-146">Realice los cambios y, a continuación, seleccione **Actualizar capacidad**.</span><span class="sxs-lookup"><span data-stu-id="93c02-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="93c02-147">Para actualizar las cualificaciones para los productos, productos de servicio o grupos de producto de servicio</span><span class="sxs-lookup"><span data-stu-id="93c02-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="93c02-148">Si desea cambiar los códigos de habilidades asignados a elementos, por ejemplo de **PC** a **PCS**, puede hacerlo para un producto, un producto de servicio o para todos los productos de un grupo de productos de servicio.</span><span class="sxs-lookup"><span data-stu-id="93c02-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="93c02-149">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), especifique **Productos**, **Producto servicio** o **Grupo producto servicio** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="93c02-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93c02-150">Elija la entidad que desee actualizar y, a continuación, elija la acción **Capacidades recurso**.</span><span class="sxs-lookup"><span data-stu-id="93c02-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="93c02-151">En la línea con el código que desea modificar, en el campo **Cód. cualificación**, elija el código de cualificación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="93c02-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="93c02-152">Si el producto tiene productos de servicio asociados, se abrirá un cuadro de diálogo con las dos opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="93c02-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="93c02-153">Cambiar el código de capacidad al valor seleccionado: seleccione esta opción si desea reemplazar el antiguo código de cualificación por el nuevo en todos los productos de servicio relacionados.</span><span class="sxs-lookup"><span data-stu-id="93c02-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="93c02-154">Elimine los códigos de aptitudes o actualice sus relaciones: seleccione esta opción si desea modificar el código de aptitud solo en este artículo.</span><span class="sxs-lookup"><span data-stu-id="93c02-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="93c02-155">El código de cualificación de los productos de servicio relacionados se reasignará, es decir, se actualizará el campo **Se asigna de**.</span><span class="sxs-lookup"><span data-stu-id="93c02-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93c02-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="93c02-156">See Also</span></span>
[<span data-ttu-id="93c02-157">Asignar recursos</span><span class="sxs-lookup"><span data-stu-id="93c02-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="93c02-158">Configurar horas de trabajo y de servicio</span><span class="sxs-lookup"><span data-stu-id="93c02-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="93c02-159">Crear informes de defecto</span><span class="sxs-lookup"><span data-stu-id="93c02-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="93c02-160">Configurar códigos para servicios estándar</span><span class="sxs-lookup"><span data-stu-id="93c02-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 


