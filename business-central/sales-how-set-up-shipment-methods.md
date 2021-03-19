---
title: Configuración de métodos de envío
description: Puede configurar un código para cada uno de los métodos de envío ofrecidos e introducir información sobre ellos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: 096b609d26ad24785f90634d725d751ac57b346e
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573306"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="166ea-103">Configurar métodos de envío</span><span class="sxs-lookup"><span data-stu-id="166ea-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="166ea-104">Los métodos de envío suelen depender del tipo de producto, de los clientes y de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="166ea-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="166ea-105">Por ejemplo, si el cliente reside en una isla, puede elegir que le envíen siempre los productos por barco o por avión.</span><span class="sxs-lookup"><span data-stu-id="166ea-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="166ea-106">Algunos clientes pueden requerir la entrega al día siguiente.</span><span class="sxs-lookup"><span data-stu-id="166ea-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="166ea-107">Algunos pueden querer recoger el pedido.</span><span class="sxs-lookup"><span data-stu-id="166ea-107">Some may want to pick up the order.</span></span> <span data-ttu-id="166ea-108">Puede especificar el tipo de entrega deseado en las fichas de cliente y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="166ea-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="166ea-109">En la página **Métodos de envío**, configure la descripción y el código correspondiente a cada método de envío.</span><span class="sxs-lookup"><span data-stu-id="166ea-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="166ea-110">Por ejemplo, puede configurar el código FAB e introducir Franco a bordo en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="166ea-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="166ea-111">A continuación, puede introducir el código en los campos **Código de método de envío** en otra parte del sistema, como en una ficha cliente.</span><span class="sxs-lookup"><span data-stu-id="166ea-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="166ea-112">A continuación, cuando cree nuevos pedidos, facturas, abonos, etc., el sistema introducirá la descripción incluida en el código.</span><span class="sxs-lookup"><span data-stu-id="166ea-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="166ea-113">Se puede modificar en el documento según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="166ea-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="166ea-114">Para configurar una forma de envío</span><span class="sxs-lookup"><span data-stu-id="166ea-114">To set up a shipment method</span></span>

1. <span data-ttu-id="166ea-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Métodos de envío** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="166ea-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="166ea-116">En la página **Métodos de envío**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="166ea-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="166ea-117">En la nueva línea especifique un código y una descripción para el método de envío.</span><span class="sxs-lookup"><span data-stu-id="166ea-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="166ea-118">Si usa Incoterms, configure métodos de envío para representar las reglas de Incoterms relevantes.</span><span class="sxs-lookup"><span data-stu-id="166ea-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="166ea-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="166ea-119">See Also</span></span>

[<span data-ttu-id="166ea-120">Configurar transportistas</span><span class="sxs-lookup"><span data-stu-id="166ea-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="166ea-121">Hacer un seguimiento de los paquetes</span><span class="sxs-lookup"><span data-stu-id="166ea-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="166ea-122">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="166ea-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="166ea-123">Inventario</span><span class="sxs-lookup"><span data-stu-id="166ea-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="166ea-124">Configuración de la gestión del almacén</span><span class="sxs-lookup"><span data-stu-id="166ea-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="166ea-125">Gestión de ensamblaje</span><span class="sxs-lookup"><span data-stu-id="166ea-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="166ea-126">Detalles de diseño: gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="166ea-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="166ea-127">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="166ea-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="166ea-128">Incoterms en iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="166ea-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]