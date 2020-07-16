---
title: 'Tutorial: recepción y ubicación en la configuración básica de almacén | Documentos de Microsoft'
description: En Business Central, los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: sgroespe
ms.openlocfilehash: 22ad58aa06fc99d8199ec95df6015783f51920aa
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528165"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="662d6-103">Tutorial: recepción y ubicación en la configuración del almacenamiento básico</span><span class="sxs-lookup"><span data-stu-id="662d6-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

<span data-ttu-id="662d6-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], los procesos de entrada para la recepción y la ubicación se pueden realizar de cuatro maneras utilizando distintas funciones según el nivel de complejidad del almacén.</span><span class="sxs-lookup"><span data-stu-id="662d6-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="662d6-105">Método</span><span class="sxs-lookup"><span data-stu-id="662d6-105">Method</span></span>|<span data-ttu-id="662d6-106">Proceso de salida</span><span class="sxs-lookup"><span data-stu-id="662d6-106">Inbound process</span></span>|<span data-ttu-id="662d6-107">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="662d6-107">Bins</span></span>|<span data-ttu-id="662d6-108">Recepciones</span><span class="sxs-lookup"><span data-stu-id="662d6-108">Receipts</span></span>|<span data-ttu-id="662d6-109">Ubicaciones</span><span class="sxs-lookup"><span data-stu-id="662d6-109">Put-aways</span></span>|<span data-ttu-id="662d6-110">Nivel de complejidad (consulte [Detalles de diseño: Configuración de almacén](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="662d6-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="662d6-111">A</span><span class="sxs-lookup"><span data-stu-id="662d6-111">A</span></span>|<span data-ttu-id="662d6-112">Registro de la recepción y ubicación desde la línea de pedido</span><span class="sxs-lookup"><span data-stu-id="662d6-112">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="662d6-113">X</span><span class="sxs-lookup"><span data-stu-id="662d6-113">X</span></span>|||<span data-ttu-id="662d6-114">2</span><span class="sxs-lookup"><span data-stu-id="662d6-114">2</span></span>|  
|<span data-ttu-id="662d6-115">P</span><span class="sxs-lookup"><span data-stu-id="662d6-115">B</span></span>|<span data-ttu-id="662d6-116">Registro de la recepción y ubicación desde un documento de ubicación del inventario</span><span class="sxs-lookup"><span data-stu-id="662d6-116">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="662d6-117">X</span><span class="sxs-lookup"><span data-stu-id="662d6-117">X</span></span>|<span data-ttu-id="662d6-118">3</span><span class="sxs-lookup"><span data-stu-id="662d6-118">3</span></span>|  
|<span data-ttu-id="662d6-119">C</span><span class="sxs-lookup"><span data-stu-id="662d6-119">C</span></span>|<span data-ttu-id="662d6-120">Registro de la recepción y ubicación desde un documento de recepción de almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-120">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="662d6-121">X</span><span class="sxs-lookup"><span data-stu-id="662d6-121">X</span></span>||<span data-ttu-id="662d6-122">5/4/6</span><span class="sxs-lookup"><span data-stu-id="662d6-122">4/5/6</span></span>|  
|<span data-ttu-id="662d6-123">D</span><span class="sxs-lookup"><span data-stu-id="662d6-123">D</span></span>|<span data-ttu-id="662d6-124">Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-124">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="662d6-125">X</span><span class="sxs-lookup"><span data-stu-id="662d6-125">X</span></span>|<span data-ttu-id="662d6-126">X</span><span class="sxs-lookup"><span data-stu-id="662d6-126">X</span></span>|<span data-ttu-id="662d6-127">5/4/6</span><span class="sxs-lookup"><span data-stu-id="662d6-127">4/5/6</span></span>|  

<span data-ttu-id="662d6-128">Para obtener más información, consulte [Detalles de diseño: Flujo de entrada del almacén](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="662d6-128">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="662d6-129">En el siguiente tutorial se demuestra el método B de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="662d6-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="662d6-130">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="662d6-130">About This Walkthrough</span></span>  
<span data-ttu-id="662d6-131">En la configuración básica de almacén, donde el almacén está configurado para requerir proceso de ubicación, pero no de recepción, utiliza la página **Ubicación existencias** para registrar la información de ubicación y recepción de los documentos de origen entrantes.</span><span class="sxs-lookup"><span data-stu-id="662d6-131">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="662d6-132">El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de salida o una orden de producción con salida que está preparada para ubicarse.</span><span class="sxs-lookup"><span data-stu-id="662d6-132">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="662d6-133">A pesar de que las configuraciones se denominan **Picking requerido** y **Ubicación requerida**, todavía puede registrar recibos y envíos directamente desde los documentos empresariales de origen en las ubicaciones donde se selecciona estas casillas de verificación.</span><span class="sxs-lookup"><span data-stu-id="662d6-133">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="662d6-134">En este tutorial, se demuestran las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="662d6-134">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="662d6-135">Configuración del almacén PLATA para las ubicaciones de inventario.</span><span class="sxs-lookup"><span data-stu-id="662d6-135">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="662d6-136">Configuración del almacén PLATA para la manipulación en ubicación.</span><span class="sxs-lookup"><span data-stu-id="662d6-136">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="662d6-137">Definir una ubicación predeterminada para el producto LS-81.</span><span class="sxs-lookup"><span data-stu-id="662d6-137">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="662d6-138">(LS-75 ya está configurado en CRONUS).</span><span class="sxs-lookup"><span data-stu-id="662d6-138">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="662d6-139">Crear un pedido de compra para el proveedor 10000 para 40 altavoces.</span><span class="sxs-lookup"><span data-stu-id="662d6-139">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="662d6-140">Compruebe que las ubicaciones son preestablecidas por la configuración.</span><span class="sxs-lookup"><span data-stu-id="662d6-140">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="662d6-141">Liberar el pedido de compra para la manipulación en almacén.</span><span class="sxs-lookup"><span data-stu-id="662d6-141">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="662d6-142">Crear una ubicación de inventario basada en un documento de origen lanzado.</span><span class="sxs-lookup"><span data-stu-id="662d6-142">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="662d6-143">Compruebe que las ubicaciones se heredan del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="662d6-143">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="662d6-144">Registrar el movimiento de almacén en el almacén y, al mismo tiempo, registrar el albarán de compra para el pedido de compra de origen.</span><span class="sxs-lookup"><span data-stu-id="662d6-144">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="662d6-145">Funciones</span><span class="sxs-lookup"><span data-stu-id="662d6-145">Roles</span></span>  
<span data-ttu-id="662d6-146">En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:</span><span class="sxs-lookup"><span data-stu-id="662d6-146">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="662d6-147">Responsable de almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-147">Warehouse Manager</span></span>  
-   <span data-ttu-id="662d6-148">Agente de compras</span><span class="sxs-lookup"><span data-stu-id="662d6-148">Purchasing Agent</span></span>  
-   <span data-ttu-id="662d6-149">Trabajador de almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-149">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="662d6-150">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="662d6-150">Prerequisites</span></span>  
<span data-ttu-id="662d6-151">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="662d6-151">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="662d6-152">CRONUS España S.A. instalado.</span><span class="sxs-lookup"><span data-stu-id="662d6-152">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="662d6-153">Para convertirse en un empleado de almacén en el almacén PLATA, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="662d6-153">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="662d6-154">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="662d6-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="662d6-155">Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="662d6-155">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="662d6-156">En el campo **Cód. almacén**, especifique PLATA.</span><span class="sxs-lookup"><span data-stu-id="662d6-156">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="662d6-157">Seleccione el campo de **Predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="662d6-157">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="662d6-158">Historia</span><span class="sxs-lookup"><span data-stu-id="662d6-158">Story</span></span>  
<span data-ttu-id="662d6-159">Ellen, administradora del almacén en CRONUS España S.A., crea un pedido de compra de 10 unidades del producto LS-75 y 30 unidades del producto LS-81 del proveedor 10000 para su entrega al almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="662d6-159">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="662d6-160">Cuando la entrega llega al almacén, Juan, el trabajador del almacén, coloca los productos en las ubicaciones predeterminadas definidas para los productos.</span><span class="sxs-lookup"><span data-stu-id="662d6-160">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="662d6-161">Cuando Juan registra la ubicación, los productos se registran como recibidos en el inventario y estarán disponibles para la venta u otra demanda.</span><span class="sxs-lookup"><span data-stu-id="662d6-161">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="662d6-162">Configuración del almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-162">Setting up the Location</span></span>  
 <span data-ttu-id="662d6-163">La configuración de la página **Ficha almacén** define los flujos de almacén de la empresa.</span><span class="sxs-lookup"><span data-stu-id="662d6-163">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="662d6-164">Configurar el almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-164">To set up the location</span></span>  

1.  <span data-ttu-id="662d6-165">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="662d6-165">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="662d6-166">Abra la ficha de almacén PLATA.</span><span class="sxs-lookup"><span data-stu-id="662d6-166">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="662d6-167">Active la casilla **Ubicación requerida**.</span><span class="sxs-lookup"><span data-stu-id="662d6-167">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="662d6-168">Empiece a configurar una ubicación predeterminada para los dos números de producto para controlar dónde es la ubicación.</span><span class="sxs-lookup"><span data-stu-id="662d6-168">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="662d6-169">Seleccione la acción **Ubicaciones**.</span><span class="sxs-lookup"><span data-stu-id="662d6-169">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="662d6-170">Seleccione la primera fila, para la ubicación S-01-0001, y después seleccione **Contenidos**.</span><span class="sxs-lookup"><span data-stu-id="662d6-170">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="662d6-171">Observe en la página **Contenido ubicación** que el producto LS-75 ya está configurado como contenido de la ubicación S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="662d6-171">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="662d6-172">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="662d6-172">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="662d6-173">Seleccione los campos **Fijo** y **Predet.**.</span><span class="sxs-lookup"><span data-stu-id="662d6-173">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="662d6-174">En el campo **Nº producto**, introduzca LS-81.</span><span class="sxs-lookup"><span data-stu-id="662d6-174">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="662d6-175">Creación del pedido de compra</span><span class="sxs-lookup"><span data-stu-id="662d6-175">Creating the Purchase Order</span></span>  
<span data-ttu-id="662d6-176">Los pedidos de compra son el tipo más común de documento de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="662d6-176">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="662d6-177">Crear el pedido de compra</span><span class="sxs-lookup"><span data-stu-id="662d6-177">To create the purchase order</span></span>  

1.  <span data-ttu-id="662d6-178">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="662d6-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="662d6-179">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="662d6-179">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="662d6-180">Cree un pedido de compra para el proveedor 10000 en la fecha de trabajo (23 de enero) con las líneas de pedido de compra siguientes.</span><span class="sxs-lookup"><span data-stu-id="662d6-180">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="662d6-181">Producto</span><span class="sxs-lookup"><span data-stu-id="662d6-181">Item</span></span>|<span data-ttu-id="662d6-182">Cód. almacén</span><span class="sxs-lookup"><span data-stu-id="662d6-182">Location code</span></span>|<span data-ttu-id="662d6-183">Cód. ubicación</span><span class="sxs-lookup"><span data-stu-id="662d6-183">Bin code</span></span>|<span data-ttu-id="662d6-184">Cantidad</span><span class="sxs-lookup"><span data-stu-id="662d6-184">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="662d6-185">LS_75</span><span class="sxs-lookup"><span data-stu-id="662d6-185">LS_75</span></span>|<span data-ttu-id="662d6-186">PLATA</span><span class="sxs-lookup"><span data-stu-id="662d6-186">SILVER</span></span>|<span data-ttu-id="662d6-187">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="662d6-187">S-01-0001</span></span>|<span data-ttu-id="662d6-188">10</span><span class="sxs-lookup"><span data-stu-id="662d6-188">10</span></span>|  
    |<span data-ttu-id="662d6-189">LS-81</span><span class="sxs-lookup"><span data-stu-id="662d6-189">LS-81</span></span>|<span data-ttu-id="662d6-190">PLATA</span><span class="sxs-lookup"><span data-stu-id="662d6-190">SILVER</span></span>|<span data-ttu-id="662d6-191">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="662d6-191">S-01-0001</span></span>|<span data-ttu-id="662d6-192">30</span><span class="sxs-lookup"><span data-stu-id="662d6-192">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="662d6-193">El código de ubicación se especifica de forma automática según la configuración que ha realizado en sección "Configuración del almacén".</span><span class="sxs-lookup"><span data-stu-id="662d6-193">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="662d6-194">Empiece a notificar el almacén para el que el pedido de compra está preparado para la manipulación en almacén cuando llegue la entrega.</span><span class="sxs-lookup"><span data-stu-id="662d6-194">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="662d6-195">Seleccione la acción **Liberar**.</span><span class="sxs-lookup"><span data-stu-id="662d6-195">Choose the **Release** action.</span></span>  

    <span data-ttu-id="662d6-196">La entrega de los altavoces del proveedor 10000 ha llegado al almacén PLATA y Juan comienza a guardarlos en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="662d6-196">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="662d6-197">Recepción y ubicación de productos</span><span class="sxs-lookup"><span data-stu-id="662d6-197">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="662d6-198">En la página **Ubicación existencias**, puede administrar todas las actividades de almacén de entrada para un documento de origen determinado, como un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="662d6-198">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="662d6-199">Recibir y establecer la ubicación de los productos</span><span class="sxs-lookup"><span data-stu-id="662d6-199">To receive and put the items away</span></span>  

1.  <span data-ttu-id="662d6-200">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicaciones existencias** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="662d6-200">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="662d6-201">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="662d6-201">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="662d6-202">Seleccione el campo **Documento origen** y luego **Pedido compra**.</span><span class="sxs-lookup"><span data-stu-id="662d6-202">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="662d6-203">Seleccione el campo **Nº origen**, seleccione la línea para la compra del proveedor 10000 y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="662d6-203">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="662d6-204">De forma alternativa, seleccione la acción **Obtener documento de origen** y, a continuación, seleccione el pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="662d6-204">Alternatively, choose the **Get Source Document** action, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="662d6-205">Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.</span><span class="sxs-lookup"><span data-stu-id="662d6-205">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="662d6-206">También, en el campo **Cdad. a manipular**, introduzca 10 y 30 respectivamente en las dos líneas de ubicación de existencias.</span><span class="sxs-lookup"><span data-stu-id="662d6-206">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="662d6-207">Seleccione la acción **Registrar**, elija la acción **Recibir** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="662d6-207">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="662d6-208">Los 40 altavoces ahora se registran como en ubicaciones en la ubicación S-01-0001, y un movimiento de producto positivo se crea para reflejar la recepción de compra registrada.</span><span class="sxs-lookup"><span data-stu-id="662d6-208">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="662d6-209">Consulte también</span><span class="sxs-lookup"><span data-stu-id="662d6-209">See Also</span></span>  
 <span data-ttu-id="662d6-210">[Ubicar productos con ubicación de inventario](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-210">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="662d6-211">[Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-211">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="662d6-212">[Mover componentes a un área de operaciones en configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-212">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="662d6-213">[Selección de producción o la Lista montaje](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-213">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="662d6-214">[Mover productos ad hoc en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-214">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="662d6-215">[Detalles de diseño: Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="662d6-215">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="662d6-216">Tutoriales de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="662d6-216">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="662d6-217">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="662d6-217">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
