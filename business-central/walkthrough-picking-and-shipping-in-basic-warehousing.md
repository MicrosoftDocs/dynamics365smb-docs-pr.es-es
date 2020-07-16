---
title: Picking y envío en la configuración básica de almacén | Documentos de Microsoft
description: En Business Central, los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: 475f32dbaf9b4b80a61e1cad542fbf6db79cb029
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528315"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="d52a7-103">Tutorial: picking y envío en la configuración del almacenamiento básico</span><span class="sxs-lookup"><span data-stu-id="d52a7-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="d52a7-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de salida para el picking y el envío se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.</span><span class="sxs-lookup"><span data-stu-id="d52a7-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="d52a7-105">Método</span><span class="sxs-lookup"><span data-stu-id="d52a7-105">Method</span></span>|<span data-ttu-id="d52a7-106">Proceso de salida</span><span class="sxs-lookup"><span data-stu-id="d52a7-106">Inbound process</span></span>|<span data-ttu-id="d52a7-107">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="d52a7-107">Bins</span></span>|<span data-ttu-id="d52a7-108">Picking</span><span class="sxs-lookup"><span data-stu-id="d52a7-108">Picks</span></span>|<span data-ttu-id="d52a7-109">Envíos</span><span class="sxs-lookup"><span data-stu-id="d52a7-109">Shipments</span></span>|<span data-ttu-id="d52a7-110">Nivel de complejidad (consulte [Detalles de diseño: configuración de almacén](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="d52a7-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="d52a7-111">A</span><span class="sxs-lookup"><span data-stu-id="d52a7-111">A</span></span>|<span data-ttu-id="d52a7-112">Registro de picking y envío desde la línea de pedido</span><span class="sxs-lookup"><span data-stu-id="d52a7-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="d52a7-113">X</span><span class="sxs-lookup"><span data-stu-id="d52a7-113">X</span></span>|||<span data-ttu-id="d52a7-114">2</span><span class="sxs-lookup"><span data-stu-id="d52a7-114">2</span></span>|  
|<span data-ttu-id="d52a7-115">P</span><span class="sxs-lookup"><span data-stu-id="d52a7-115">B</span></span>|<span data-ttu-id="d52a7-116">Registro de picking y envío desde un documento de picking de existencias</span><span class="sxs-lookup"><span data-stu-id="d52a7-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="d52a7-117">X</span><span class="sxs-lookup"><span data-stu-id="d52a7-117">X</span></span>||<span data-ttu-id="d52a7-118">3</span><span class="sxs-lookup"><span data-stu-id="d52a7-118">3</span></span>|  
|<span data-ttu-id="d52a7-119">C</span><span class="sxs-lookup"><span data-stu-id="d52a7-119">C</span></span>|<span data-ttu-id="d52a7-120">Registro de picking y envío desde un documento de envío de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="d52a7-121">X</span><span class="sxs-lookup"><span data-stu-id="d52a7-121">X</span></span>|<span data-ttu-id="d52a7-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="d52a7-122">4/5/6</span></span>|  
|<span data-ttu-id="d52a7-123">D</span><span class="sxs-lookup"><span data-stu-id="d52a7-123">D</span></span>|<span data-ttu-id="d52a7-124">Registro de picking desde un documento de picking de almacén y registro de envío de un documento de envío de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="d52a7-125">X</span><span class="sxs-lookup"><span data-stu-id="d52a7-125">X</span></span>|<span data-ttu-id="d52a7-126">X</span><span class="sxs-lookup"><span data-stu-id="d52a7-126">X</span></span>|<span data-ttu-id="d52a7-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="d52a7-127">4/5/6</span></span>|  

<span data-ttu-id="d52a7-128">Para obtener más información, consulte [Detalles de diseño: Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d52a7-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="d52a7-129">En el siguiente tutorial se demuestra el método B de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="d52a7-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="d52a7-130">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="d52a7-130">About This Walkthrough</span></span>

<span data-ttu-id="d52a7-131">En la configuración del almacenamiento básico, donde el almacén está configurado para requerir proceso de picking, pero no de envío, utiliza la página **Picking inventario** para registrar la información de picking y envío de los documentos de origen salientes.</span><span class="sxs-lookup"><span data-stu-id="d52a7-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="d52a7-132">El documento de origen de salida puede ser un pedido de venta, un pedido de devolución de compra, un pedido de transferencia de salida o una orden de producción con necesidad de componentes.</span><span class="sxs-lookup"><span data-stu-id="d52a7-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="d52a7-133">En este tutorial, se demuestran las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d52a7-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="d52a7-134">Configuración del almacén PLATA para el picking de inventario.</span><span class="sxs-lookup"><span data-stu-id="d52a7-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="d52a7-135">Crear un pedido de venta para el cliente 10000 para 30 altavoces.</span><span class="sxs-lookup"><span data-stu-id="d52a7-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="d52a7-136">Liberar el pedido de venta para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="d52a7-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="d52a7-137">Crear un picking de existencias basado en un documento de origen lanzado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="d52a7-138">Registrar el movimiento de almacén desde el almacén y, al mismo tiempo, registrar el albarán de venta para el pedido de venta de origen.</span><span class="sxs-lookup"><span data-stu-id="d52a7-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="d52a7-139">Funciones</span><span class="sxs-lookup"><span data-stu-id="d52a7-139">Roles</span></span>

<span data-ttu-id="d52a7-140">En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:</span><span class="sxs-lookup"><span data-stu-id="d52a7-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="d52a7-141">Responsable de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-141">Warehouse Manager</span></span>  
- <span data-ttu-id="d52a7-142">Procesador de pedidos</span><span class="sxs-lookup"><span data-stu-id="d52a7-142">Order Processor</span></span>  
- <span data-ttu-id="d52a7-143">Trabajador de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="d52a7-144">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d52a7-144">Prerequisites</span></span>

<span data-ttu-id="d52a7-145">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="d52a7-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="d52a7-146">Para [!INCLUDE[prodshort](includes/prodshort.md)] online, una empresa basada en la opción **Evaluación avanzada: completar datos de muestra** en un entorno de espacio aislado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-146">For [!INCLUDE[prodshort](includes/prodshort.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="d52a7-147">Para [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. instalada.</span><span class="sxs-lookup"><span data-stu-id="d52a7-147">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="d52a7-148">Para convertirse en un empleado de almacén en la ubicación PLATA, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d52a7-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="d52a7-149">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="d52a7-150">Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="d52a7-151">En el campo **Cód. almacén**, especifique PLATA.</span><span class="sxs-lookup"><span data-stu-id="d52a7-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="d52a7-152">Seleccione el campo de **Predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="d52a7-153">Haga que el producto LS-81 esté disponible en el almacén PLATA siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="d52a7-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="d52a7-154">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de productos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="d52a7-155">Abra el diario predeterminado y después cree dos líneas del diario del producto con la siguiente información en la fecha de trabajo (23 de enero).</span><span class="sxs-lookup"><span data-stu-id="d52a7-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="d52a7-156">Tipo mov.</span><span class="sxs-lookup"><span data-stu-id="d52a7-156">Entry Type</span></span>|<span data-ttu-id="d52a7-157">Número de producto</span><span class="sxs-lookup"><span data-stu-id="d52a7-157">Item Number</span></span>|<span data-ttu-id="d52a7-158">Código de ubicación</span><span class="sxs-lookup"><span data-stu-id="d52a7-158">Location Code</span></span>|<span data-ttu-id="d52a7-159">Cód. ubicación</span><span class="sxs-lookup"><span data-stu-id="d52a7-159">Bin Code</span></span>|<span data-ttu-id="d52a7-160">Cantidad</span><span class="sxs-lookup"><span data-stu-id="d52a7-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="d52a7-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="d52a7-161">Positive Adjmt.</span></span>|<span data-ttu-id="d52a7-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="d52a7-162">LS-81</span></span>|<span data-ttu-id="d52a7-163">PLATA</span><span class="sxs-lookup"><span data-stu-id="d52a7-163">SILVER</span></span>|<span data-ttu-id="d52a7-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="d52a7-164">S-01-0001</span></span>|<span data-ttu-id="d52a7-165">nº 20</span><span class="sxs-lookup"><span data-stu-id="d52a7-165">20</span></span>|  
        |<span data-ttu-id="d52a7-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="d52a7-166">Positive Adjmt.</span></span>|<span data-ttu-id="d52a7-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="d52a7-167">LS-81</span></span>|<span data-ttu-id="d52a7-168">PLATA</span><span class="sxs-lookup"><span data-stu-id="d52a7-168">SILVER</span></span>|<span data-ttu-id="d52a7-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="d52a7-169">S-01-0002</span></span>|<span data-ttu-id="d52a7-170">nº 20</span><span class="sxs-lookup"><span data-stu-id="d52a7-170">20</span></span>|  

  3. <span data-ttu-id="d52a7-171">Elija la acción **Registrar** y, a continuación, seleccione el botón **Si**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="d52a7-172">Historia</span><span class="sxs-lookup"><span data-stu-id="d52a7-172">Story</span></span>

<span data-ttu-id="d52a7-173">Ellen, la administradora del almacén en CRONUS, configura el almacén PLATA para la manipulación de picking básica donde los trabajadores de almacén procesan los pedidos de salida individualmente.</span><span class="sxs-lookup"><span data-stu-id="d52a7-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="d52a7-174">Susana, la encargada de procesamiento de pedidos, crea un pedido de venta de 30 unidades del producto LS-81 que se deben enviar al cliente 10000 desde el almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="d52a7-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="d52a7-175">Juan, el trabajador de almacén debe comprobar que el envío se prepara y envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="d52a7-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="d52a7-176">Juan controla todas las tareas relacionadas con la página **Picking inventario**, que señala automáticamente a las ubicaciones donde se almacena LS-81.</span><span class="sxs-lookup"><span data-stu-id="d52a7-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="d52a7-177">Configuración del almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-177">Setting Up the Location</span></span>

<span data-ttu-id="d52a7-178">La configuración de la página **Ficha almacén** define los flujos de almacén de la empresa.</span><span class="sxs-lookup"><span data-stu-id="d52a7-178">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="d52a7-179">Configurar el almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-179">To set up the location</span></span>

1. <span data-ttu-id="d52a7-180">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d52a7-181">Abra la ficha de almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="d52a7-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="d52a7-182">En la ficha desplegable **Almacén**, marque la casilla **Picking requerido**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="d52a7-183">Crear el pedido de venta</span><span class="sxs-lookup"><span data-stu-id="d52a7-183">Creating the Sales Order</span></span>

<span data-ttu-id="d52a7-184">Los pedidos de venta son el tipo más común de documento de origen de salida.</span><span class="sxs-lookup"><span data-stu-id="d52a7-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="d52a7-185">Para crear el pedido de venta</span><span class="sxs-lookup"><span data-stu-id="d52a7-185">To create the sales order</span></span>

1. <span data-ttu-id="d52a7-186">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d52a7-187">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="d52a7-188">Crea un pedido de venta para el cliente 10000 en la fecha de trabajo (23 de enero) con la línea de pedido de venta siguiente.</span><span class="sxs-lookup"><span data-stu-id="d52a7-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="d52a7-189">Producto</span><span class="sxs-lookup"><span data-stu-id="d52a7-189">Item</span></span>|<span data-ttu-id="d52a7-190">Cód. almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-190">Location Code</span></span>|<span data-ttu-id="d52a7-191">Cantidad</span><span class="sxs-lookup"><span data-stu-id="d52a7-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="d52a7-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="d52a7-192">LS_81</span></span>|<span data-ttu-id="d52a7-193">PLATA</span><span class="sxs-lookup"><span data-stu-id="d52a7-193">SILVER</span></span>|<span data-ttu-id="d52a7-194">30</span><span class="sxs-lookup"><span data-stu-id="d52a7-194">30</span></span>|  

     <span data-ttu-id="d52a7-195">Empiece a notificar el almacén para el que el pedido de venta está preparado para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="d52a7-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="d52a7-196">Seleccione la acción **Liberar**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="d52a7-197">Juan comienza a realizar el picking y a enviar a productos vendidos.</span><span class="sxs-lookup"><span data-stu-id="d52a7-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="d52a7-198">Picking y envío de productos</span><span class="sxs-lookup"><span data-stu-id="d52a7-198">Picking and Shipping Items</span></span>

<span data-ttu-id="d52a7-199">En la página **Picking inventario**, puede administrar todas las actividades de almacén de salida para un documento de origen determinado, como un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="d52a7-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="d52a7-200">Realizar el picking y el envío de productos</span><span class="sxs-lookup"><span data-stu-id="d52a7-200">To pick and ship items</span></span>

1. <span data-ttu-id="d52a7-201">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Picking de existencias** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d52a7-202">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="d52a7-203">Asegúrese de que el campo **N.º**</span><span class="sxs-lookup"><span data-stu-id="d52a7-203">Make sure that the **No.**</span></span> <span data-ttu-id="d52a7-204">en desplegable **General** se haya rellenado.</span><span class="sxs-lookup"><span data-stu-id="d52a7-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="d52a7-205">Seleccione el campo **Documento origen** y luego **Pedido venta**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="d52a7-206">Seleccione el campo **Nº origen**, la línea para la venta al cliente 10000 y, a continuación, el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="d52a7-207">De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="d52a7-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="d52a7-208">Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="d52a7-209">También, en el campo **Cdad. a manipular**, introduzca 10 y 20 respectivamente en las dos líneas del picking de existencias.</span><span class="sxs-lookup"><span data-stu-id="d52a7-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="d52a7-210">Seleccione la acción **Registrar**, seleccione **Enviar** y, a continuación, el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d52a7-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="d52a7-211">Los 30 altavoces ahora se registran como preparados desde las ubicaciones S-01-0001 y S-01-0002, y un movimiento de producto negativo se crea para reflejar el histórico de albaranes de venta.</span><span class="sxs-lookup"><span data-stu-id="d52a7-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d52a7-212">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d52a7-212">See Also</span></span>

[<span data-ttu-id="d52a7-213">Realizar el picking de productos con picking inventario</span><span class="sxs-lookup"><span data-stu-id="d52a7-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="d52a7-214">Realizar un picking de los artículos para el envío de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="d52a7-215">Configurar almacenes básicos con áreas de operaciones</span><span class="sxs-lookup"><span data-stu-id="d52a7-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="d52a7-216">Mover componentes a un área de operaciones en configuraciones básicas de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="d52a7-217">Picking para producción o ensamblado</span><span class="sxs-lookup"><span data-stu-id="d52a7-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="d52a7-218">Mover productos ad hoc en configuraciones básicas de almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="d52a7-219">Detalles de diseño: Flujo de salida del almacén</span><span class="sxs-lookup"><span data-stu-id="d52a7-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="d52a7-220">Tutoriales de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="d52a7-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="d52a7-221">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d52a7-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
