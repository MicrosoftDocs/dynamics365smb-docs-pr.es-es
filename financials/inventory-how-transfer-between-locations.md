---
title: Transferir productos entre almacenes | Documentos de Microsoft
description: "Describe cómo mover el inventario de un lugar o almacén a otro con el diario de reclasificación o con pedidos de transferencia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 41804dc183f9fa05ec1599db34c2b4f76a790a72
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="55a06-103">Procedimiento: Transferir el inventario entre almacenes</span><span class="sxs-lookup"><span data-stu-id="55a06-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="55a06-104">Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia.</span><span class="sxs-lookup"><span data-stu-id="55a06-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="55a06-105">También puede usar el diario de reclasificación de productos.</span><span class="sxs-lookup"><span data-stu-id="55a06-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="55a06-106">Con los pedidos de transferencia, se envía la transferencia de salida desde un almacén y se recibe la transferencia de entrada en el otro almacén.</span><span class="sxs-lookup"><span data-stu-id="55a06-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="55a06-107">Esto permite administrar las actividades de almacén correspondientes y proporciona más certidumbre de que las cantidades del inventario se actualizan correctamente.</span><span class="sxs-lookup"><span data-stu-id="55a06-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="55a06-108">Cono el diario de reclasificación, simplemente se rellenan los campos **Código de almacén** y **Nuevo código de almacén**.</span><span class="sxs-lookup"><span data-stu-id="55a06-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="55a06-109">Al registrar el diario, los movimientos de productos se ajustan en los almacenes en cuestión.</span><span class="sxs-lookup"><span data-stu-id="55a06-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="55a06-110">Con este método, las actividades de almacén no se administran.</span><span class="sxs-lookup"><span data-stu-id="55a06-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="55a06-111">Si tiene productos registrados en el inventario sin un código de almacén, por ejemplo cuando solo tenía un almacén, no podrá transferir estos productos con pedidos de transferencia.</span><span class="sxs-lookup"><span data-stu-id="55a06-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="55a06-112">En su lugar, deberá utilizar el diario de reclasificación para reclasificar los productos desde un código de almacén en blanco a un código de almacén real.</span><span class="sxs-lookup"><span data-stu-id="55a06-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="55a06-113">Para obtener más información, vea el paso 3 en la sección "Para transferir productos con el diario de reclasificación".</span><span class="sxs-lookup"><span data-stu-id="55a06-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="55a06-114">Para transferir productos, se deben configurar las ubicaciones y las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="55a06-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="55a06-115">Para obtener más información, vea [Procedimiento: Configurar almacenes](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="55a06-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="55a06-116">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="55a06-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="55a06-117">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="55a06-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="55a06-118">Para transferir productos con un pedido de transferencia</span><span class="sxs-lookup"><span data-stu-id="55a06-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="55a06-119">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de transferencia** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="55a06-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="55a06-120">En la ventana **Pedido de transferencia**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="55a06-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="55a06-121">Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la ventana **Ruta transf. espec.** cuando configuró la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="55a06-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="55a06-122">Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.</span><span class="sxs-lookup"><span data-stu-id="55a06-122">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="55a06-123">Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con el envío de los productos.</span><span class="sxs-lookup"><span data-stu-id="55a06-123">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="55a06-124">Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="55a06-124">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="55a06-125">Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.</span><span class="sxs-lookup"><span data-stu-id="55a06-125">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="55a06-126">Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos.</span><span class="sxs-lookup"><span data-stu-id="55a06-126">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="55a06-127">Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="55a06-127">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="55a06-128">Para transferir productos con el diario de reclasificación de productos</span><span class="sxs-lookup"><span data-stu-id="55a06-128">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="55a06-129">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios reclas. producto** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="55a06-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="55a06-130">En la ventana **Diarios reclasif. producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="55a06-130">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="55a06-131">En el campo **Cód. almacén**, escriba la ubicación donde se almacenan los productos actualmente.</span><span class="sxs-lookup"><span data-stu-id="55a06-131">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="55a06-132">Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.</span><span class="sxs-lookup"><span data-stu-id="55a06-132">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="55a06-133">En el campo **Cód. almacén destino**, especifique la ubicación a la que desee transferir los productos.</span><span class="sxs-lookup"><span data-stu-id="55a06-133">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="55a06-134">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="55a06-134">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="55a06-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="55a06-135">See Also</span></span>
[<span data-ttu-id="55a06-136">Gestionar inventario</span><span class="sxs-lookup"><span data-stu-id="55a06-136">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="55a06-137">Configuración de almacenes</span><span class="sxs-lookup"><span data-stu-id="55a06-137">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
  
<span data-ttu-id="55a06-138">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55a06-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="55a06-139">[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="55a06-139">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="55a06-140">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="55a06-140">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
