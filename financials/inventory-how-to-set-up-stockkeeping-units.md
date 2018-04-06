---
title: Configurar unidades de almacenamiento | Documentos de Microsoft
description: "Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bc323e4dac1b62802e999e2780352634e25e482d
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="00e3f-103">Configurar unidades de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="00e3f-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="00e3f-104">Utilice unidades de almacenamiento para registrar información sobre los productos de un determinado almacén o de un código de variante en particular.</span><span class="sxs-lookup"><span data-stu-id="00e3f-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="00e3f-105">Las unidades de almacenamiento vienen a complementar las fichas del producto.</span><span class="sxs-lookup"><span data-stu-id="00e3f-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="00e3f-106">No los reemplazan, aunque guardan cierta relación con ellos.</span><span class="sxs-lookup"><span data-stu-id="00e3f-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="00e3f-107">Estas unidades le permiten distinguir información sobre un producto de un determinado almacén, como un almacén o un centro de distribución, o de una determinada variante, como distintos códigos de situación e información de reposición.</span><span class="sxs-lookup"><span data-stu-id="00e3f-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="00e3f-108">Para configurar una unidad de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="00e3f-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="00e3f-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Uds. de almacenam.** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="00e3f-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="00e3f-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="00e3f-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="00e3f-111">Complete los campos de la ficha.</span><span class="sxs-lookup"><span data-stu-id="00e3f-111">Fill in the fields on the card.</span></span> <span data-ttu-id="00e3f-112">Se requieren los siguientes campos: **Nº producto**, **Cód. almacén** y/o **Cód. variante**.</span><span class="sxs-lookup"><span data-stu-id="00e3f-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="00e3f-113">Una vez configurada la primera unidad de almacenamiento para un producto, se selecciona la casilla **Existe ud. de almacenam.** de la ficha **Producto**.</span><span class="sxs-lookup"><span data-stu-id="00e3f-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="00e3f-114">Para crear varias unidades de almacenamiento para un producto, utilice el proceso **Crear ud. de almacenan.**.</span><span class="sxs-lookup"><span data-stu-id="00e3f-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="00e3f-115">La información de la ficha **Unidad de almacenamiento** tiene prioridad sobre la ficha de **Producto**.</span><span class="sxs-lookup"><span data-stu-id="00e3f-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00e3f-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00e3f-116">See Also</span></span>  
[<span data-ttu-id="00e3f-117">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="00e3f-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="00e3f-118">Configuración de la gestión del almacén</span><span class="sxs-lookup"><span data-stu-id="00e3f-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="00e3f-119">Gestión de almacenes</span><span class="sxs-lookup"><span data-stu-id="00e3f-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="00e3f-120">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="00e3f-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="00e3f-121">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="00e3f-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="00e3f-122">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="00e3f-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="00e3f-123">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00e3f-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

