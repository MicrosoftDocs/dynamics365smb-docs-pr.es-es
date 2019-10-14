---
title: Configuración de los métodos de envío | Documentos de Microsoft
description: Puede configurar un código para cada uno de los métodos de envío ofrecidos, por ejemplo, e introducir información sobre ellos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: be65cd62cec984cd2571b6e88998dc169741f376
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312081"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="c4d26-103">Configuración de métodos de envío</span><span class="sxs-lookup"><span data-stu-id="c4d26-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="c4d26-104">Los métodos de envío, también llamados incoterms, a menudo dependen de los productos, los clientes y los proveedores.</span><span class="sxs-lookup"><span data-stu-id="c4d26-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="c4d26-105">Por ejemplo, si el cliente reside en una isla, puede elegir que le envíen siempre los productos por barco o por avión.</span><span class="sxs-lookup"><span data-stu-id="c4d26-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="c4d26-106">Algunos clientes pueden requerir la entrega al día siguiente.</span><span class="sxs-lookup"><span data-stu-id="c4d26-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="c4d26-107">Algunos pueden querer recoger el pedido.</span><span class="sxs-lookup"><span data-stu-id="c4d26-107">Some may want to pick up the order.</span></span> <span data-ttu-id="c4d26-108">Puede especificar el tipo de entrega deseado en las fichas de cliente y de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c4d26-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="c4d26-109">En la página **Métodos de envío**, configure la descripción y el código correspondiente a cada método de envío.</span><span class="sxs-lookup"><span data-stu-id="c4d26-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="c4d26-110">Por ejemplo, puede configurar el código FAB e introducir Franco a bordo en el campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="c4d26-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="c4d26-111">A continuación, puede introducir el código en los campos **Código de método de envío** en otra parte del sistema, como en una ficha cliente.</span><span class="sxs-lookup"><span data-stu-id="c4d26-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="c4d26-112">A continuación, cuando cree nuevos pedidos, facturas, abonos, etc., el sistema introducirá la descripción incluida en el código.</span><span class="sxs-lookup"><span data-stu-id="c4d26-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="c4d26-113">Se puede modificar en el documento según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c4d26-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="c4d26-114">Para configurar un código de envío</span><span class="sxs-lookup"><span data-stu-id="c4d26-114">To set up a shipment code</span></span>
1. <span data-ttu-id="c4d26-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Métodos de envío** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="c4d26-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="c4d26-116">En la página **Métodos de envío**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c4d26-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="c4d26-117">En la nueva línea especifique un código y una descripción para el método de envío.</span><span class="sxs-lookup"><span data-stu-id="c4d26-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4d26-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c4d26-118">See Also</span></span>
[<span data-ttu-id="c4d26-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="c4d26-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="c4d26-120">Configurar transportistas</span><span class="sxs-lookup"><span data-stu-id="c4d26-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="c4d26-121">[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="c4d26-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="c4d26-122">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="c4d26-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c4d26-123">Inventario</span><span class="sxs-lookup"><span data-stu-id="c4d26-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c4d26-124">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c4d26-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c4d26-125">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c4d26-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c4d26-126">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="c4d26-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c4d26-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c4d26-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
