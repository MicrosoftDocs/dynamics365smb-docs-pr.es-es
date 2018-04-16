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
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: f13da8ac565e0af7f4ab612ebd23c9cee158dbb9
ms.contentlocale: es-es
ms.lasthandoff: 04/16/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="91ea7-103">Transferir el inventario entre almacenes</span><span class="sxs-lookup"><span data-stu-id="91ea7-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="91ea7-104">Puede transferir inventarios de productos entre almacenes creando pedidos de transferencia.</span><span class="sxs-lookup"><span data-stu-id="91ea7-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="91ea7-105">También puede usar el diario de reclasificación de productos.</span><span class="sxs-lookup"><span data-stu-id="91ea7-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="91ea7-106">Con los pedidos de transferencia, se envía la transferencia de salida desde un almacén y se recibe la transferencia de entrada en el otro almacén.</span><span class="sxs-lookup"><span data-stu-id="91ea7-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="91ea7-107">Esto permite administrar las actividades de almacén correspondientes y proporciona más certidumbre de que las cantidades del inventario se actualizan correctamente.</span><span class="sxs-lookup"><span data-stu-id="91ea7-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="91ea7-108">Cono el diario de reclasificación, simplemente se rellenan los campos **Código de almacén** y **Nuevo código de almacén**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="91ea7-109">Al registrar el diario, los movimientos de productos se ajustan en los almacenes en cuestión.</span><span class="sxs-lookup"><span data-stu-id="91ea7-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="91ea7-110">Con este método, las actividades de almacén no se administran.</span><span class="sxs-lookup"><span data-stu-id="91ea7-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="91ea7-111">Si tiene productos registrados en el inventario sin un código de almacén, por ejemplo cuando solo tenía un almacén, no podrá transferir estos productos con pedidos de transferencia.</span><span class="sxs-lookup"><span data-stu-id="91ea7-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="91ea7-112">En su lugar, deberá utilizar el diario de reclasificación para reclasificar los productos desde un código de almacén en blanco a un código de almacén real.</span><span class="sxs-lookup"><span data-stu-id="91ea7-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="91ea7-113">Para obtener más información, vea el paso 3 en la sección "Para transferir productos con el diario de reclasificación".</span><span class="sxs-lookup"><span data-stu-id="91ea7-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="91ea7-114">Para transferir productos, se deben configurar las ubicaciones y las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="91ea7-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="91ea7-115">Para obtener más información, consulte [Configurar ubicaciones](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="91ea7-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="91ea7-116">Para transferir productos con un pedido de transferencia</span><span class="sxs-lookup"><span data-stu-id="91ea7-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="91ea7-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de transferencia** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="91ea7-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="91ea7-118">En la ventana **Pedido de transferencia**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="91ea7-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
   >   <span data-ttu-id="91ea7-119">Si ha rellenado los campos **Cód. en tránsito**, **Cód. transportista** y **Cód. servicio transportista** en la ventana **Ruta transf. espec.** cuando configuró la ruta de transferencia, los campos correspondientes del pedido de transferencia se rellenan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="91ea7-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="91ea7-120">Cuando se especifica un valor en el campo **Servicio transportista**, se calcula la fecha de recepción en el almacén de destino de la transferencia, sumando el tiempo de envío del transportista a la fecha de envío.</span><span class="sxs-lookup"><span data-stu-id="91ea7-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="91ea7-121">Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con el envío de los productos.</span><span class="sxs-lookup"><span data-stu-id="91ea7-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="91ea7-122">Seleccione la acción **Registrar**, seleccione la opción **Envío** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="91ea7-123">Los productos ahora se encuentran en tránsito entre las ubicaciones especificadas, según la ruta de transferencia especificada.</span><span class="sxs-lookup"><span data-stu-id="91ea7-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="91ea7-124">Como trabajador de almacén en el almacén de procedencia de la transferencia, continúe con la recepción de los productos.</span><span class="sxs-lookup"><span data-stu-id="91ea7-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="91ea7-125">Seleccione la acción **Registrar**, seleccione la opción **Recepción** y seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="91ea7-126">Para transferir productos con el diario de reclasificación de productos</span><span class="sxs-lookup"><span data-stu-id="91ea7-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="91ea7-127">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios reclas. producto** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="91ea7-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="91ea7-128">En la ventana **Diarios reclasif. producto**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="91ea7-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="91ea7-129">En el campo **Cód. almacén**, escriba la ubicación donde se almacenan los productos actualmente.</span><span class="sxs-lookup"><span data-stu-id="91ea7-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
   >   <span data-ttu-id="91ea7-130">Para transferir productos que no tienen código de almacén, deje en blanco el campo **Cód. almacén**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="91ea7-131">En el campo **Cód. almacén destino**, especifique la ubicación a la que desee transferir los productos.</span><span class="sxs-lookup"><span data-stu-id="91ea7-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="91ea7-132">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="91ea7-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="91ea7-133">See Also</span></span>
[<span data-ttu-id="91ea7-134">Gestionar inventario</span><span class="sxs-lookup"><span data-stu-id="91ea7-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="91ea7-135">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="91ea7-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  

<span data-ttu-id="91ea7-136">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91ea7-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="91ea7-137">[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="91ea7-137">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="91ea7-138">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="91ea7-138">General Business Functionality</span></span>](ui-across-business-areas.md)

