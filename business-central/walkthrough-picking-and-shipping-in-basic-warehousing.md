---
title: Picking y envío en la configuración del almacenamiento básico
description: En Business Central, los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214658"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="af360-103">Tutorial: picking y envío en la configuración del almacenamiento básico</span><span class="sxs-lookup"><span data-stu-id="af360-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="af360-104">En [!INCLUDE[prod_short](includes/prod_short.md)], los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.</span><span class="sxs-lookup"><span data-stu-id="af360-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="af360-105">Método</span><span class="sxs-lookup"><span data-stu-id="af360-105">Method</span></span>|<span data-ttu-id="af360-106">Proceso de salida</span><span class="sxs-lookup"><span data-stu-id="af360-106">Inbound process</span></span>|<span data-ttu-id="af360-107">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="af360-107">Bins</span></span>|<span data-ttu-id="af360-108">Picking</span><span class="sxs-lookup"><span data-stu-id="af360-108">Picks</span></span>|<span data-ttu-id="af360-109">Envíos</span><span class="sxs-lookup"><span data-stu-id="af360-109">Shipments</span></span>|<span data-ttu-id="af360-110">Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="af360-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="af360-111">A</span><span class="sxs-lookup"><span data-stu-id="af360-111">A</span></span>|<span data-ttu-id="af360-112">Registro de picking y envío desde la línea de pedido</span><span class="sxs-lookup"><span data-stu-id="af360-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="af360-113">X</span><span class="sxs-lookup"><span data-stu-id="af360-113">X</span></span>|||<span data-ttu-id="af360-114">2</span><span class="sxs-lookup"><span data-stu-id="af360-114">2</span></span>|  
|<span data-ttu-id="af360-115">P</span><span class="sxs-lookup"><span data-stu-id="af360-115">B</span></span>|<span data-ttu-id="af360-116">Registro de picking y envío desde un documento de picking de existencias</span><span class="sxs-lookup"><span data-stu-id="af360-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="af360-117">X</span><span class="sxs-lookup"><span data-stu-id="af360-117">X</span></span>||<span data-ttu-id="af360-118">3</span><span class="sxs-lookup"><span data-stu-id="af360-118">3</span></span>|  
|<span data-ttu-id="af360-119">C</span><span class="sxs-lookup"><span data-stu-id="af360-119">C</span></span>|<span data-ttu-id="af360-120">Registro de picking y envío desde un documento de envío de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="af360-121">X</span><span class="sxs-lookup"><span data-stu-id="af360-121">X</span></span>|<span data-ttu-id="af360-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="af360-122">4/5/6</span></span>|  
|<span data-ttu-id="af360-123">D</span><span class="sxs-lookup"><span data-stu-id="af360-123">D</span></span>|<span data-ttu-id="af360-124">Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="af360-125">X</span><span class="sxs-lookup"><span data-stu-id="af360-125">X</span></span>|<span data-ttu-id="af360-126">X</span><span class="sxs-lookup"><span data-stu-id="af360-126">X</span></span>|<span data-ttu-id="af360-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="af360-127">4/5/6</span></span>|  

<span data-ttu-id="af360-128">Para obtener más información, consulte [Detalles de diseño: Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="af360-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="af360-129">En el siguiente tutorial se demuestra el método B de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="af360-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="af360-130">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="af360-130">About This Walkthrough</span></span>

<span data-ttu-id="af360-131">En la configuración del almacenamiento básico, donde el almacén está configurado para requerir proceso de picking, pero no de envío, utiliza la página **Picking inventario** para registrar la información de picking y envío de los documentos de origen salientes.</span><span class="sxs-lookup"><span data-stu-id="af360-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="af360-132">El documento de origen de salida puede ser un pedido de venta, un pedido de devolución de compra, un pedido de transferencia de salida o una orden de producción con necesidad de componentes.</span><span class="sxs-lookup"><span data-stu-id="af360-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="af360-133">En este tutorial, se demuestran las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="af360-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="af360-134">Configuración del almacén SUR para el picking de inventario.</span><span class="sxs-lookup"><span data-stu-id="af360-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="af360-135">Crear un pedido de venta para el cliente 10000 para 30 lámparas Ámsterdam.</span><span class="sxs-lookup"><span data-stu-id="af360-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="af360-136">Liberar el pedido de venta para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="af360-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="af360-137">Crear un picking de existencias basado en un documento de origen lanzado.</span><span class="sxs-lookup"><span data-stu-id="af360-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="af360-138">Registrar el movimiento de almacén desde el almacén y, al mismo tiempo, registrar el albarán de venta para el pedido de venta de origen.</span><span class="sxs-lookup"><span data-stu-id="af360-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="af360-139">Funciones</span><span class="sxs-lookup"><span data-stu-id="af360-139">Roles</span></span>

<span data-ttu-id="af360-140">En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:</span><span class="sxs-lookup"><span data-stu-id="af360-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="af360-141">Responsable de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-141">Warehouse Manager</span></span>  
- <span data-ttu-id="af360-142">Procesador de pedidos</span><span class="sxs-lookup"><span data-stu-id="af360-142">Order Processor</span></span>  
- <span data-ttu-id="af360-143">Trabajador de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="af360-144">Historia</span><span class="sxs-lookup"><span data-stu-id="af360-144">Story</span></span>

<span data-ttu-id="af360-145">Ellen, la administradora del almacén en CRONUS, configura el almacén SUR para la manipulación de picking básica donde los trabajadores de almacén procesan los pedidos de salida individualmente.</span><span class="sxs-lookup"><span data-stu-id="af360-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="af360-146">Susana, la encargada de procesamiento de pedidos, crea un pedido de venta de 30 unidades del producto 1928-S que se deben enviar al cliente 10000 desde el almacén SUR.</span><span class="sxs-lookup"><span data-stu-id="af360-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="af360-147">Juan, el trabajador de almacén debe comprobar que el envío se prepara y envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="af360-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="af360-148">Juan controla todas las tareas relacionadas con la página **Picking inventario**, que señala automáticamente a las ubicaciones donde se almacena 1928-S.</span><span class="sxs-lookup"><span data-stu-id="af360-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="af360-149">Configuración los códigos de ubicación</span><span class="sxs-lookup"><span data-stu-id="af360-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="af360-150">Una vez que haya configurado el almacén, debe agregar dos ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="af360-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="af360-151">Para configurar los códigos de ubicación</span><span class="sxs-lookup"><span data-stu-id="af360-151">To setup the bin codes</span></span>

1. <span data-ttu-id="af360-152">Seleccione la acción **Ubicaciones**.</span><span class="sxs-lookup"><span data-stu-id="af360-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="af360-153">Crea dos ubicaciones, con los códigos *S-01-0001* y *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="af360-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="af360-154">Convertirse en un empleado de almacén en el almacén SUR</span><span class="sxs-lookup"><span data-stu-id="af360-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="af360-155">Para utilizar esta funcionalidad, debe agregarse al almacén como trabajador del almacén.</span><span class="sxs-lookup"><span data-stu-id="af360-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="af360-156">Para convertirte en un empleado de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="af360-157">Elija el icono ![Bombilla que abre la función Dígame, primero](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="af360-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="af360-158">Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Empleados de almacén**.</span><span class="sxs-lookup"><span data-stu-id="af360-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="af360-159">En el campo **Cód. almacén**, elija SUR.</span><span class="sxs-lookup"><span data-stu-id="af360-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="af360-160">Seleccione el campo **Predeterminado** y, a continuación, seleccione el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="af360-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="af360-161">Hacer que el producto 1928-S esté disponible</span><span class="sxs-lookup"><span data-stu-id="af360-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="af360-162">Para que el producto 1928-S esté disponible en el almacén SUR siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="af360-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="af360-163">Elija el icono ![Bombilla que abre la función Dígame, segundo](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios reclasif. producto** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="af360-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="af360-164">Abra el diario predeterminado y después cree dos líneas del diario del producto con la siguiente información en la fecha de trabajo (23 de enero).</span><span class="sxs-lookup"><span data-stu-id="af360-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="af360-165">Tipo mov.</span><span class="sxs-lookup"><span data-stu-id="af360-165">Entry Type</span></span>|<span data-ttu-id="af360-166">Número de producto</span><span class="sxs-lookup"><span data-stu-id="af360-166">Item Number</span></span>|<span data-ttu-id="af360-167">Código de ubicación</span><span class="sxs-lookup"><span data-stu-id="af360-167">Location Code</span></span>|<span data-ttu-id="af360-168">Cód. ubicación</span><span class="sxs-lookup"><span data-stu-id="af360-168">Bin Code</span></span>|<span data-ttu-id="af360-169">Cantidad</span><span class="sxs-lookup"><span data-stu-id="af360-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="af360-170">Entradas</span><span class="sxs-lookup"><span data-stu-id="af360-170">Positive Adjmt.</span></span>|<span data-ttu-id="af360-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="af360-171">1928-S</span></span>|<span data-ttu-id="af360-172">SUR</span><span class="sxs-lookup"><span data-stu-id="af360-172">SOUTH</span></span>|<span data-ttu-id="af360-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="af360-173">S-01-0001</span></span>|<span data-ttu-id="af360-174">nº 20</span><span class="sxs-lookup"><span data-stu-id="af360-174">20</span></span>|  
        |<span data-ttu-id="af360-175">Entradas</span><span class="sxs-lookup"><span data-stu-id="af360-175">Positive Adjmt.</span></span>|<span data-ttu-id="af360-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="af360-176">1928-S</span></span>|<span data-ttu-id="af360-177">SUR</span><span class="sxs-lookup"><span data-stu-id="af360-177">SOUTH</span></span>|<span data-ttu-id="af360-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="af360-178">S-01-0002</span></span>|<span data-ttu-id="af360-179">nº 20</span><span class="sxs-lookup"><span data-stu-id="af360-179">20</span></span>|  

        <span data-ttu-id="af360-180">De forma predeterminada, el campo **Código de ubicación** de las líneas de ventas están ocultos, por lo que deberá mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="af360-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="af360-181">Para hacer esto, necesita personalizar la página.</span><span class="sxs-lookup"><span data-stu-id="af360-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="af360-182">Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="af360-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="af360-183">Elija **Acciones**, **Registro** y, a continuación, elija **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="af360-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="af360-184">Seleccione el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="af360-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="af360-185">Crear el pedido de venta</span><span class="sxs-lookup"><span data-stu-id="af360-185">Creating the Sales Order</span></span>

<span data-ttu-id="af360-186">Los pedidos de venta son el tipo más común de documento de origen de salida.</span><span class="sxs-lookup"><span data-stu-id="af360-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="af360-187">Para crear el pedido de venta</span><span class="sxs-lookup"><span data-stu-id="af360-187">To create the sales order</span></span>

1. <span data-ttu-id="af360-188">Elija el icono ![Bombilla que abre la función Dígame, tercero](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="af360-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af360-189">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="af360-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="af360-190">Crea un pedido de venta para el cliente 10000 en la fecha de trabajo (23 de enero) con la línea de pedido de venta siguiente.</span><span class="sxs-lookup"><span data-stu-id="af360-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="af360-191">Producto</span><span class="sxs-lookup"><span data-stu-id="af360-191">Item</span></span>|<span data-ttu-id="af360-192">Código de ubicación</span><span class="sxs-lookup"><span data-stu-id="af360-192">Location Code</span></span>|<span data-ttu-id="af360-193">Cantidad</span><span class="sxs-lookup"><span data-stu-id="af360-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="af360-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="af360-194">1928-S</span></span>|<span data-ttu-id="af360-195">SUR</span><span class="sxs-lookup"><span data-stu-id="af360-195">SOUTH</span></span>|<span data-ttu-id="af360-196">30</span><span class="sxs-lookup"><span data-stu-id="af360-196">30</span></span>|  

     <span data-ttu-id="af360-197">Empiece a notificar el almacén para el que el pedido de venta está preparado para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="af360-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="af360-198">Seleccione la acción **Liberar**.</span><span class="sxs-lookup"><span data-stu-id="af360-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="af360-199">Juan comienza a realizar el picking y a enviar a productos vendidos.</span><span class="sxs-lookup"><span data-stu-id="af360-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="af360-200">Picking y envío de productos</span><span class="sxs-lookup"><span data-stu-id="af360-200">Picking and Shipping Items</span></span>

<span data-ttu-id="af360-201">En la página **Picking inventario**, puede administrar todas las actividades de almacén de salida para un documento de origen determinado, como un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="af360-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="af360-202">Realizar el picking y el envío de productos</span><span class="sxs-lookup"><span data-stu-id="af360-202">To pick and ship items</span></span>

1. <span data-ttu-id="af360-203">Elija el icono ![Bombilla que abre la función Dígame, cuarto](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Picking de existencias** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="af360-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="af360-204">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="af360-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="af360-205">Asegúrese de que el campo **N.º**</span><span class="sxs-lookup"><span data-stu-id="af360-205">Make sure that the **No.**</span></span> <span data-ttu-id="af360-206">en desplegable **General** se haya rellenado.</span><span class="sxs-lookup"><span data-stu-id="af360-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="af360-207">Seleccione el campo **Documento origen** y luego **Pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="af360-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="af360-208">Seleccione el campo **Nº origen**, la línea para la venta al cliente 10000 y, a continuación, el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="af360-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="af360-209">De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="af360-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="af360-210">Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.</span><span class="sxs-lookup"><span data-stu-id="af360-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="af360-211">También, en el campo **Cdad. a manipular**, introduzca 10 y 20 respectivamente en las dos líneas del picking de existencias.</span><span class="sxs-lookup"><span data-stu-id="af360-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="af360-212">Seleccione la acción **Registrar**, seleccione **Enviar** y, a continuación, el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="af360-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="af360-213">Los 30 lámparas Ámsterdam ahora se registran como preparados desde las ubicaciones S-01-0001 y S-01-0002, y un movimiento de producto negativo se crea para reflejar el histórico de albaranes de venta.</span><span class="sxs-lookup"><span data-stu-id="af360-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af360-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="af360-214">See Also</span></span>

[<span data-ttu-id="af360-215">Realizar el picking de productos con picking inventario</span><span class="sxs-lookup"><span data-stu-id="af360-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="af360-216">Realizar un picking de los artículos para el envío de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="af360-217">Configurar almacenes básicos con áreas de operaciones</span><span class="sxs-lookup"><span data-stu-id="af360-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="af360-218">Mover componentes a un área de operaciones en configuraciones básicas de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="af360-219">Picking para producción o ensamblado</span><span class="sxs-lookup"><span data-stu-id="af360-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="af360-220">Mover productos ad hoc en configuraciones básicas de almacén</span><span class="sxs-lookup"><span data-stu-id="af360-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="af360-221">Detalles de diseño: Flujo de salida del almacén</span><span class="sxs-lookup"><span data-stu-id="af360-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="af360-222">Tutoriales de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="af360-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="af360-223">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af360-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
