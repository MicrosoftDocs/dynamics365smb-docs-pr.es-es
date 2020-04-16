---
title: Configuración de los métodos de envío | Documentos de Microsoft
description: Puede configurar un código para cada uno de los métodos de envío ofrecidos, por ejemplo, e introducir información sobre ellos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: dc4864f27490a9cef7d3401f67c8ef177a5c7ef3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193893"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="6e1ff-103">Configuración de métodos de envío</span><span class="sxs-lookup"><span data-stu-id="6e1ff-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="6e1ff-104">Los métodos de envío, también llamados incoterms, a menudo dependen de los productos, los clientes y los proveedores.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="6e1ff-105">Por ejemplo, si el cliente reside en una isla, puede elegir que le envíen siempre los productos por barco o por avión.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="6e1ff-106">Algunos clientes pueden requerir la entrega al día siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="6e1ff-107">Algunos pueden querer recoger el pedido.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-107">Some may want to pick up the order.</span></span> <span data-ttu-id="6e1ff-108">Puede especificar el tipo de entrega deseado en las fichas de cliente y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="6e1ff-109">En la página **Métodos de envío**, configure la descripción y el código correspondiente a cada método de envío.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="6e1ff-110">Por ejemplo, puede configurar el código FAB e introducir Franco a bordo en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="6e1ff-111">A continuación, puede introducir el código en los campos **Código de método de envío** en otra parte del sistema, como en una ficha cliente.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="6e1ff-112">A continuación, cuando cree nuevos pedidos, facturas, abonos, etc., el sistema introducirá la descripción incluida en el código.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="6e1ff-113">Se puede modificar en el documento según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="6e1ff-114">Para configurar un código de envío</span><span class="sxs-lookup"><span data-stu-id="6e1ff-114">To set up a shipment code</span></span>
1. <span data-ttu-id="6e1ff-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Métodos de envío** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="6e1ff-116">En la página **Métodos de envío**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="6e1ff-117">En la nueva línea especifique un código y una descripción para el método de envío.</span><span class="sxs-lookup"><span data-stu-id="6e1ff-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e1ff-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e1ff-118">See Also</span></span>
[<span data-ttu-id="6e1ff-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="6e1ff-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="6e1ff-120">Configurar transportistas</span><span class="sxs-lookup"><span data-stu-id="6e1ff-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="6e1ff-121">[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="6e1ff-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="6e1ff-122">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="6e1ff-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="6e1ff-123">Inventario</span><span class="sxs-lookup"><span data-stu-id="6e1ff-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="6e1ff-124">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="6e1ff-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="6e1ff-125">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="6e1ff-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="6e1ff-126">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="6e1ff-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6e1ff-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e1ff-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
