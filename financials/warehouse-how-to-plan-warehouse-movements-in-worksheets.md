---
title: "Cómo planificar los movimientos de almacén en la hoja de trabajo | Documentos de Microsoft"
description: "Planifique los movimientos en la hoja de trabajo con una función de reposición de ubicación o manualmente mediante la planificación de las líneas que desea crear como instrucciones de movimiento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e2cefcc91b823ac4a75d1eb209e892bc56b13de2
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="456d2-103">Procedimiento: planifique movimientos de almacén en hojas de trabajo</span><span class="sxs-lookup"><span data-stu-id="456d2-103">How to: Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="456d2-104">Planifique los movimientos en la hoja de trabajo con una función de reposición de ubicación o manualmente mediante la planificación de las líneas que desea crear como instrucciones de movimiento.</span><span class="sxs-lookup"><span data-stu-id="456d2-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="456d2-105">Para calcular un movimiento de reposición</span><span class="sxs-lookup"><span data-stu-id="456d2-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="456d2-106">Cuando el almacén envía los productos a los clientes, las ubicaciones con los ranking de ubicación más altos contienen cada vez menos productos.</span><span class="sxs-lookup"><span data-stu-id="456d2-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="456d2-107">Para rellenar estas ubicaciones de picking de ranking más alto con productos de otras ubicaciones, ejecute la función **Calcular reposición ubicación** de la ventana **Hoja trabajo movimiento**.</span><span class="sxs-lookup"><span data-stu-id="456d2-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="456d2-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja movimiento** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="456d2-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="456d2-109">Elija la acción **Calcular reposición ubicación**.</span><span class="sxs-lookup"><span data-stu-id="456d2-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="456d2-110"> crea líneas que indican exactamente cómo debe mover los productos de las ubicaciones de ranking inferior a las ubicaciones de ranking superior.</span><span class="sxs-lookup"><span data-stu-id="456d2-110"> creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="456d2-111">Un movimiento se sugiere según el FEFO cuando se activa la función **Crear movimiento** si cumple las siguientes condiciones para un artículo:</span><span class="sxs-lookup"><span data-stu-id="456d2-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="456d2-112">El producto tiene fecha de caducidad.</span><span class="sxs-lookup"><span data-stu-id="456d2-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="456d2-113">Se selecciona la casilla **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén.</span><span class="sxs-lookup"><span data-stu-id="456d2-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="456d2-114">La casilla **Ubicac. obligatoria** de la ficha de almacén está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="456d2-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="456d2-115">Los campos **Desde zona** y **Desde ubicación** están en blanco.</span><span class="sxs-lookup"><span data-stu-id="456d2-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="456d2-116">Para obtener más información, consulte [Realización de picking por el FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="456d2-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="456d2-117">Observe las líneas y cámbielas si es necesario, o elimine algunas si no tiene tiempo suficiente para ejecutar todas.</span><span class="sxs-lookup"><span data-stu-id="456d2-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="456d2-118">Elija la acción **Crear movimiento** para crear una instrucción de almacén para que los empleados de almacén realicen una acción.</span><span class="sxs-lookup"><span data-stu-id="456d2-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="456d2-119">Mover todo el contenido de una o varias ubicaciones con la función Traer contenido ubicación</span><span class="sxs-lookup"><span data-stu-id="456d2-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="456d2-120">También puede utilizar la hoja de trabajo de movimiento para planificar otros movimientos de inventario en el almacén.</span><span class="sxs-lookup"><span data-stu-id="456d2-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="456d2-121">Por ejemplo, cuando desee colocar productos en una ubicación para controlar la calidad, puede utilizar la hoja de trabajo de movimiento para planificar esta acción y, a continuación, crear un movimiento para darle instrucciones a un empleado.</span><span class="sxs-lookup"><span data-stu-id="456d2-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="456d2-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja movimiento** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="456d2-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="456d2-123">Seleccione la acción **Traer contenido ubicación**.</span><span class="sxs-lookup"><span data-stu-id="456d2-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="456d2-124">Utilice la ventana de solicitud para filtrar las ubicaciones y productos que desea que aparezcan en las líneas de la hoja de trabajo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="456d2-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="456d2-125">Rellene los campos correspondientes de la ventana de condiciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="456d2-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="456d2-126">Por ejemplo, si desea ver el contenido de todas las ubicaciones en una determinada zona del almacén, rellene el campo **Cód. zona**.</span><span class="sxs-lookup"><span data-stu-id="456d2-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="456d2-127">Si desea recuperar líneas de cada ubicación que contenga un producto determinado, rellene el campo **Nº producto**.</span><span class="sxs-lookup"><span data-stu-id="456d2-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="456d2-128">No puede mover manualmente productos dentro o fuera de una ubicación de tipo RECEPCIÓN, porque los productos que están en una ubicación de tipo RECEPCIÓN deben ubicarse antes de que formen parte del inventario disponible.</span><span class="sxs-lookup"><span data-stu-id="456d2-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="456d2-129">Si recupera muchas líneas, seleccione **Ordenar** para seleccionar un método de ordenación que determine el orden en el que aparecerán las líneas en la hoja de trabajo y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="456d2-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="456d2-130">Las líneas de movimiento se recuperan según el FEFO cuando se activa la función **Traer conten. ubicac.** si cumple las siguientes condiciones para un producto:</span><span class="sxs-lookup"><span data-stu-id="456d2-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="456d2-131">El producto tiene fecha de caducidad.</span><span class="sxs-lookup"><span data-stu-id="456d2-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="456d2-132">Se selecciona la casilla **Picking según FEFO (Primero en caducar, primero en salir)** de la ficha de almacén.</span><span class="sxs-lookup"><span data-stu-id="456d2-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="456d2-133">La casilla **Ubicac. obligatoria** de la ficha de almacén está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="456d2-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="456d2-134">Los campos **Desde zona** y **Desde ubicación** están en blanco.</span><span class="sxs-lookup"><span data-stu-id="456d2-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="456d2-135">Complete algunas de las líneas recuperadas para reflejar los cambios que desea realizar.</span><span class="sxs-lookup"><span data-stu-id="456d2-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="456d2-136">En cada producto que desee mover, debe rellenar los campos **Nº producto**, **Desde cód. ubicación**, **Hasta cód. ubicación** y **Cantidad**.</span><span class="sxs-lookup"><span data-stu-id="456d2-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="456d2-137">Elimine las líneas incompletas que ha utilizado para su información.</span><span class="sxs-lookup"><span data-stu-id="456d2-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="456d2-138">Cuando las líneas de la hoja de trabajo de movimiento reflejen exactamente cómo debe realizar el empleado del almacén la acción de movimiento, elija la acción **Crear movimiento** para crear las instrucciones para el empleado.</span><span class="sxs-lookup"><span data-stu-id="456d2-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="456d2-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="456d2-139">See Also</span></span>  
[<span data-ttu-id="456d2-140">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="456d2-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="456d2-141">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="456d2-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="456d2-142">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="456d2-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="456d2-143">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="456d2-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="456d2-144">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="456d2-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="456d2-145">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="456d2-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

