---
title: Configurar los productos de servicio y los componentes del producto de servicio | Documentos de Microsoft
description: Conozca los aspectos que debe configurar antes de poder utilizar los productos del servicio, incluidos los valores predeterminados, como el tiempo de respuesta, el porcentaje de descuento del contrato y el grupo de precios de servicio.
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
ms.openlocfilehash: e946bab348aeee1b65b85165b2d9d553736813ba
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="1c8aa-103">Configurar componentes de servicio y de productos</span><span class="sxs-lookup"><span data-stu-id="1c8aa-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="1c8aa-104">Para trabajar con productos de servicio, debe configurar lo siguiente</span><span class="sxs-lookup"><span data-stu-id="1c8aa-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="1c8aa-105">Grupos de producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-105">Service item groups.</span></span>
* <span data-ttu-id="1c8aa-106">Opcional</span><span class="sxs-lookup"><span data-stu-id="1c8aa-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="1c8aa-107">Para configurar grupos de producto de servicio</span><span class="sxs-lookup"><span data-stu-id="1c8aa-107">To set up service item groups</span></span>
<span data-ttu-id="1c8aa-108">Puede establecer los grupos de productos relacionados en relación con la reparación y el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="1c8aa-109">Puede definir valores predeterminados para productos de servicio de un grupo de productos de servicio, como el tiempo de respuesta, el porcentaje de descuento de contrato y el grupo de precios de servicio.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="1c8aa-110">Para productos de un grupo de productos de servicio, puede seleccionar si desea que se registren automáticamente como productos de servicio cuando se vendan.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="1c8aa-111">Puede asignar grupos de producto de servicio a productos de la ficha de **producto** y a productos de servicio de la ficha de **producto de servicio**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="1c8aa-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos producto servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1c8aa-113">Cree un grupo de productos de servicio nuevo.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="1c8aa-114">Rellene los campos **Código** y **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="1c8aa-115">En el campo **% Descuento contrato genér.**, introduzca el porcentaje de descuento de contrato genérico que desea que tengan los productos de servicio del grupo.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="1c8aa-116">En el campo **Cód. grupo precio serv. genér.**, introduzca el código de grupo de precio de servicio genérico que desea que tengan los productos de servicio del grupo.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="1c8aa-117">En el campo **Tiempo respuesta genér.(horas)**, introduzca el tiempo de respuesta genérico en horas que desea que tengan los productos de servicio del grupo.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="1c8aa-118">Si desea registrar los artículos del grupo como artículos de servicio cuando se vendan, seleccione el campo **Crea prod. servicio**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="1c8aa-119">Para configurar componentes de producto de servicio</span><span class="sxs-lookup"><span data-stu-id="1c8aa-119">To set up service item components</span></span>
<span data-ttu-id="1c8aa-120">Los productos de servicio pueden constar de varios componentes que se pueden reemplazar con otros componentes durante el servicio del producto.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="1c8aa-121">Estos componentes se configuran en la ventana **Lista componente producto servicio**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-121">These components are set up in the **Service Item Component List** window.</span></span> <span data-ttu-id="1c8aa-122">Además, si desea configurar componentes para productos de servicio que sean L.M., puede copiar los productos de la L.M. y los cree como componentes de producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="1c8aa-123">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos de servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c8aa-124">Abra el producto de servicio cuyos componentes desea configurar.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="1c8aa-125">Seleccione la acción **Componentes**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-125">Choose the **Components** action.</span></span> <span data-ttu-id="1c8aa-126">Se abrirá la ventana **Lista componente prod. serv.**</span><span class="sxs-lookup"><span data-stu-id="1c8aa-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="1c8aa-127">Agregue un componente nuevo.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-127">Add a new component.</span></span>  
5. <span data-ttu-id="1c8aa-128">En el campo **Tipo**, seleccione **Producto de servicio** si el propio componente es un producto de servicio registrado.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="1c8aa-129">De lo contrario, seleccione **Artículo**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="1c8aa-130">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="1c8aa-130">In the **No.**</span></span> <span data-ttu-id="1c8aa-131">seleccione el producto o producto de servicio que sea un componente del producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="1c8aa-132">Para configurar componentes de producto de servicio desde una L.M.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="1c8aa-133">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos de servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1c8aa-134">Abra el producto de servicio para el cual desee configurar componentes desde una L.M.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="1c8aa-135">Seleccione la acción **Componentes**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-135">Choose the **Components** action.</span></span> <span data-ttu-id="1c8aa-136">Se abrirá la ventana **Lista componentes prod.de serv.**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="1c8aa-137">Elija la acción **Copiar desde L.M.**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="1c8aa-138">Si el producto al que está vinculado el producto de servicio es una L.M., los componentes para todos los productos de la L.M. se crearán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="1c8aa-139">Para configurar una estantería de servicio</span><span class="sxs-lookup"><span data-stu-id="1c8aa-139">To set up a service shelf</span></span>
<span data-ttu-id="1c8aa-140">Puede configurar estanterías de servicio que identifiquen dónde almacena los artículos de servicio.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="1c8aa-141">Las estanterías de servicio se asignan a los productos de servicio en las ventanas **Pedido servicio** y **Hoja trabajo producto servicio**.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** windows.</span></span>  

1. <span data-ttu-id="1c8aa-142">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Estanterías servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="1c8aa-143">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1c8aa-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c8aa-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c8aa-144">See Also</span></span>
<span data-ttu-id="1c8aa-145">[Configurar códigos para servicios estándar](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="1c8aa-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="1c8aa-146">Configurar detección errores</span><span class="sxs-lookup"><span data-stu-id="1c8aa-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)

