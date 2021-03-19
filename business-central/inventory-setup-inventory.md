---
title: Configurar inventario | Documentos de Microsoft
description: Describe cómo configurar los procesos de stock e inventario, incluidas las rutas de transferencia y ubicaciones, como los almacenes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3d11e39e54d864db2eac0a1a2e1919a3cfd7a767
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393004"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="55c67-103">Configurar inventario</span><span class="sxs-lookup"><span data-stu-id="55c67-103">Setting Up Inventory</span></span>
<span data-ttu-id="55c67-104">Para poder administrar la actividad de un almacén y los costes de inventario, debe configurar las reglas y valores que definen las políticas de inventario de la empresa.</span><span class="sxs-lookup"><span data-stu-id="55c67-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="55c67-105">Puede obtener un mejor servicio al cliente y optimizar la cadena de suministro si organiza las existencias en varias direcciones.</span><span class="sxs-lookup"><span data-stu-id="55c67-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="55c67-106">Puede comprar, almacenar o vender productos en distintos almacenes y transferir inventarios entre ellos.</span><span class="sxs-lookup"><span data-stu-id="55c67-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="55c67-107">Cuando haya configurado su inventario, puede gestionar varios procesos relacionados con transacciones de productos.</span><span class="sxs-lookup"><span data-stu-id="55c67-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="55c67-108">Para obtener más información, vea [Gestión de inventario](inventory-manage-inventory.md) y [Gestión de almacén](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="55c67-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="55c67-109">Para</span><span class="sxs-lookup"><span data-stu-id="55c67-109">To</span></span> | <span data-ttu-id="55c67-110">Vea</span><span class="sxs-lookup"><span data-stu-id="55c67-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="55c67-111">Definir la configuración general de inventario, por ejemplo, las series numéricas y cómo utilizar los almacenes.</span><span class="sxs-lookup"><span data-stu-id="55c67-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="55c67-112">Configurar información de inventario general</span><span class="sxs-lookup"><span data-stu-id="55c67-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="55c67-113">Configure un modelo de distribución eficiente con una combinación de distintas ubicaciones y centros de responsabilidad asignados a empresas colaboradoras o empleados.</span><span class="sxs-lookup"><span data-stu-id="55c67-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="55c67-114">Trabajar con centros de responsabilidad</span><span class="sxs-lookup"><span data-stu-id="55c67-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="55c67-115">Organizar su inventario en varios almacenes, incluidas las rutas de transferencia.</span><span class="sxs-lookup"><span data-stu-id="55c67-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="55c67-116">Configurar ubicaciones</span><span class="sxs-lookup"><span data-stu-id="55c67-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="55c67-117">Cree fichas de producto para los productos de inventario, de no inventario o servicio que comercialice.</span><span class="sxs-lookup"><span data-stu-id="55c67-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="55c67-118">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="55c67-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="55c67-119">Utilice la función **Copiar producto** para crear rápidamente una nueva ficha de producto basada en una ya existente.</span><span class="sxs-lookup"><span data-stu-id="55c67-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="55c67-120">Copiar productos existentes para crear productos nuevos</span><span class="sxs-lookup"><span data-stu-id="55c67-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="55c67-121">Aprenda a completar el campo **Tipo** en las fichas de producto de acuerdo con el propósito comercial.</span><span class="sxs-lookup"><span data-stu-id="55c67-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="55c67-122">Acerca de los tipos de productos</span><span class="sxs-lookup"><span data-stu-id="55c67-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="55c67-123">Configure varias unidades de medida para un artículo que pueda usar como UOM alternativas, por ejemplo, en transacciones de ventas, compras o producción.</span><span class="sxs-lookup"><span data-stu-id="55c67-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="55c67-124">Configurar unidades de medida de producto</span><span class="sxs-lookup"><span data-stu-id="55c67-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="55c67-125">Como suplemento de las fichas de producto, registre la información sobre los productos en un determinado almacén o de un código de variante en particular.</span><span class="sxs-lookup"><span data-stu-id="55c67-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="55c67-126">Configurar unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="55c67-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="55c67-127">Asigne productos a categorías y asígneles atributos como ayuda, tanto para usted como para los clientes, para buscar productos.</span><span class="sxs-lookup"><span data-stu-id="55c67-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="55c67-128">Clasificar productos</span><span class="sxs-lookup"><span data-stu-id="55c67-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="55c67-129">Importe varias imágenes de producto de una sola vez desde un archivo zip en el que los archivos se denominan según los números de los elementos.</span><span class="sxs-lookup"><span data-stu-id="55c67-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="55c67-130">Importar varias imágenes de producto</span><span class="sxs-lookup"><span data-stu-id="55c67-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|
|<span data-ttu-id="55c67-131">Especifique informes predeterminados que se utilizarán para diferentes tipos de documentos.</span><span class="sxs-lookup"><span data-stu-id="55c67-131">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="55c67-132">Selección de informes en Business Central</span><span class="sxs-lookup"><span data-stu-id="55c67-132">Report Selection in Business Central</span></span>](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="55c67-133">Consulte Formación relacionada en [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="55c67-133">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="55c67-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="55c67-134">See Also</span></span>

[<span data-ttu-id="55c67-135">Administrar inventario</span><span class="sxs-lookup"><span data-stu-id="55c67-135">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="55c67-136">Administrar compras</span><span class="sxs-lookup"><span data-stu-id="55c67-136">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="55c67-137">[Administrar ventas](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="55c67-137">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="55c67-138">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55c67-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="55c67-139">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="55c67-139">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]