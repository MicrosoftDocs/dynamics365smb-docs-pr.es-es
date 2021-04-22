---
title: Configurar unidades de almacenamiento | Documentos de Microsoft
description: Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 18923708fdad1b88714d2dcb2c61bfd2e4259f4b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785724"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="3c497-103">Configurar unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="3c497-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="3c497-104">Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.</span><span class="sxs-lookup"><span data-stu-id="3c497-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="3c497-105">Las unidades de almacenamiento vienen a complementar las fichas del producto.</span><span class="sxs-lookup"><span data-stu-id="3c497-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="3c497-106">No los reemplazan, aunque guardan cierta relación con ellos.</span><span class="sxs-lookup"><span data-stu-id="3c497-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="3c497-107">Estas unidades le permiten distinguir información sobre un producto de un determinado almacén, como un almacén o un centro de distribución, o de una determinada variante, como distintos códigos de situación e información de reposición.</span><span class="sxs-lookup"><span data-stu-id="3c497-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="3c497-108">Para configurar una unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="3c497-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="3c497-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Unidades de almacenamiento** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="3c497-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3c497-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="3c497-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="3c497-111">Complete los campos de la ficha.</span><span class="sxs-lookup"><span data-stu-id="3c497-111">Fill in the fields on the card.</span></span> <span data-ttu-id="3c497-112">Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**.</span><span class="sxs-lookup"><span data-stu-id="3c497-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="3c497-113">Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe ud. de almacenam.** de la ficha **Producto**.</span><span class="sxs-lookup"><span data-stu-id="3c497-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="3c497-114">Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**.</span><span class="sxs-lookup"><span data-stu-id="3c497-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3c497-115">La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.</span><span class="sxs-lookup"><span data-stu-id="3c497-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="3c497-116">Si UA se suministra a través de producción, el campo **Coste estándar** no se usa al facturar y ajustar el coste real del producto fabricado.</span><span class="sxs-lookup"><span data-stu-id="3c497-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="3c497-117">En su lugar, el campo **Coste estándar** de la ficha subyacente de producto se utiliza, y cualquier desviación se calcula con el reparto de costes de dicho producto.</span><span class="sxs-lookup"><span data-stu-id="3c497-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="3c497-118">Porque las L.M. y ruta no se pueden asignar a UA, la distribución del coste unitario y el cálculo relacionado de la parte de costes tampoco están disponibles en UA.</span><span class="sxs-lookup"><span data-stu-id="3c497-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="3c497-119">Para obtener más información, consulte [Acerca de Calcular el coste estándar](finance-about-calculating-standard-cost.md)</span><span class="sxs-lookup"><span data-stu-id="3c497-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="3c497-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3c497-120">See Also</span></span>  
[<span data-ttu-id="3c497-121">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="3c497-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="3c497-122">Configurar la gestión del almacén</span><span class="sxs-lookup"><span data-stu-id="3c497-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="3c497-123">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="3c497-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="3c497-124">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="3c497-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3c497-125">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="3c497-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="3c497-126">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="3c497-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="3c497-127">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3c497-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]