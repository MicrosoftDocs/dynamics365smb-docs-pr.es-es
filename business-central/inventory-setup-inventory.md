---
title: Configurar inventario | Documentos de Microsoft
description: Describe cómo configurar los procesos de stock e inventario, incluidas las rutas de transferencia y ubicaciones, como los almacenes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2018
ms.author: SorenGP
ms.openlocfilehash: 8e4033412560e8dc847397c4399e12985490bf78
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805349"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="ff4a8-103">Configurar inventario</span><span class="sxs-lookup"><span data-stu-id="ff4a8-103">Setting Up Inventory</span></span>
<span data-ttu-id="ff4a8-104">Para poder administrar la actividad de un almacén y los costes de inventario, debe configurar las reglas y valores que definen las políticas de inventario de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="ff4a8-105">Puede obtener un mejor servicio al cliente y optimizar la cadena de suministro si organiza las existencias en varias direcciones.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="ff4a8-106">Puede comprar, almacenar o vender productos en distintos almacenes y transferir inventarios entre ellos.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="ff4a8-107">Cuando haya configurado su inventario, puede gestionar varios procesos relacionados con transacciones de productos.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="ff4a8-108">Para obtener más información, vea [Gestión de inventario](inventory-manage-inventory.md) y [Gestión de almacén](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ff4a8-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="ff4a8-109">Para</span><span class="sxs-lookup"><span data-stu-id="ff4a8-109">To</span></span> | <span data-ttu-id="ff4a8-110">Vea</span><span class="sxs-lookup"><span data-stu-id="ff4a8-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="ff4a8-111">Definir la configuración general de inventario, por ejemplo, las series numéricas y cómo utilizar los almacenes.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="ff4a8-112">Configurar información de inventario general</span><span class="sxs-lookup"><span data-stu-id="ff4a8-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="ff4a8-113">Configure un modelo de distribución eficiente con una combinación de distintas ubicaciones y centros de responsabilidad asignados a empresas colaboradoras o empleados.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="ff4a8-114">Trabajar con centros de responsabilidad</span><span class="sxs-lookup"><span data-stu-id="ff4a8-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="ff4a8-115">Organizar su inventario en varios almacenes, incluidas las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="ff4a8-116">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="ff4a8-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="ff4a8-117">Cree fichas de producto para los productos de inventario, de no inventario o servicio que comercialice.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="ff4a8-118">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="ff4a8-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="ff4a8-119">Aprenda a completar el campo **Tipo** en las fichas de producto de acuerdo con el propósito comercial.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="ff4a8-120">Acerca de los tipos de productos</span><span class="sxs-lookup"><span data-stu-id="ff4a8-120">About Item Types</span></span>](inventory-about-item-types.md)| 
|<span data-ttu-id="ff4a8-121">Configure varias unidades de medida para un artículo que pueda usar como UOM alternativas, por ejemplo, en transacciones de ventas, compras o producción.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="ff4a8-122">Configurar unidades de medida de producto</span><span class="sxs-lookup"><span data-stu-id="ff4a8-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="ff4a8-123">Como suplemento de las fichas de producto, registre la información sobre los productos en un determinado almacén o de un código de variante en particular.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="ff4a8-124">Configurar unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="ff4a8-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="ff4a8-125">Asigne productos a categorías y asígneles atributos como ayuda, tanto para usted como para los clientes, para buscar productos.</span><span class="sxs-lookup"><span data-stu-id="ff4a8-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="ff4a8-126">Clasificar productos</span><span class="sxs-lookup"><span data-stu-id="ff4a8-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="ff4a8-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff4a8-127">See Also</span></span>
[<span data-ttu-id="ff4a8-128">Administrar inventario</span><span class="sxs-lookup"><span data-stu-id="ff4a8-128">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ff4a8-129">Administrar compras</span><span class="sxs-lookup"><span data-stu-id="ff4a8-129">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ff4a8-130">[Administrar ventas](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="ff4a8-130">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="ff4a8-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff4a8-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ff4a8-132">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="ff4a8-132">General Business Functionality</span></span>](ui-across-business-areas.md)
