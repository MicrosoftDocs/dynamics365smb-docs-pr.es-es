---
title: 'Procedimiento: divida las líneas de actividad de almacén | Documentos de Microsoft'
description: En ubicaciones, movimientos o picking de almacén y en ubicaciones y picking de inventario, se sugieren las ubicaciones para el picking o la ubicación de productos. La cantidad real de la ubicación sugerida quizá no sea suficiente, o no hay sitio suficiente en la ubicación sugerida para ubicar la cantidad requerida. En estos casos, necesita dividir la línea para que los productos de esa línea se obtengan o coloquen en varias ubicaciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4484f4fcaef8f48642f83984f1b3dab8acc14def
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784976"
---
# <a name="split-warehouse-activity-lines"></a><span data-ttu-id="4e0af-105">Dividir líneas de actividad de almacén</span><span class="sxs-lookup"><span data-stu-id="4e0af-105">Split Warehouse Activity Lines</span></span>
<span data-ttu-id="4e0af-106">En ubicaciones, movimientos o picking de almacén y en ubicaciones y picking de inventario, se sugieren las ubicaciones para el picking o la ubicación de productos.</span><span class="sxs-lookup"><span data-stu-id="4e0af-106">In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items.</span></span> <span data-ttu-id="4e0af-107">La cantidad real de la ubicación sugerida quizá no sea suficiente, o no hay sitio suficiente en la ubicación sugerida para ubicar la cantidad requerida.</span><span class="sxs-lookup"><span data-stu-id="4e0af-107">The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity.</span></span> <span data-ttu-id="4e0af-108">En estos casos, necesita dividir la línea para que los productos de esa línea se obtengan o coloquen en varias ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="4e0af-108">In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.</span></span>  

<span data-ttu-id="4e0af-109">El procedimiento siguiente se aplica a todos los documentos de almacén, como ubicación de almacén, movimiento y las líneas de picking, o la ubicación de inventario, movimiento y líneas de picking.</span><span class="sxs-lookup"><span data-stu-id="4e0af-109">The following procedure applies to warehouse documents, such as warehouse put-away, movement, and pick lines, or inventory put-away, movement, and pick lines.</span></span>  

## <a name="to-split-warehouse-activity-lines"></a><span data-ttu-id="4e0af-110">Para dividir líneas de actividad de almacén</span><span class="sxs-lookup"><span data-stu-id="4e0af-110">To split warehouse activity lines</span></span>  
1.  <span data-ttu-id="4e0af-111">Abra una línea de actividad de almacén en donde esté intentando gestionar una cantidad insuficiente.</span><span class="sxs-lookup"><span data-stu-id="4e0af-111">Open a warehouse activity line where you are trying to handle an insufficient quantity.</span></span>  
2.  <span data-ttu-id="4e0af-112">En el campo de **Cdad. a manipular**, introduzca la cantidad reducida que pueda manipular.</span><span class="sxs-lookup"><span data-stu-id="4e0af-112">In the **Qty. to Handle** field, enter the reduced quantity that you are able to handle.</span></span>  
3.  <span data-ttu-id="4e0af-113">En la ficha desplegable **Líneas**, elija **Acciones**, **Funciones** y **Dividir línea**.</span><span class="sxs-lookup"><span data-stu-id="4e0af-113">On the **Lines** FastTab, choose the **Actions** action, choose the **Functions** action, and then choose the **Split Line** action.</span></span> <span data-ttu-id="4e0af-114">Aparecerá una nueva línea, que es una copia de la línea original, excepto en que el campo **Cdad. a manipular** contiene la cantidad que ha eliminado de la línea original.</span><span class="sxs-lookup"><span data-stu-id="4e0af-114">A new line appears, which is a copy of the original line, except that the **Qty. to Handle** field contains the quantity that you removed from the original line.</span></span>  
4.  <span data-ttu-id="4e0af-115">Asigne una ubicación adecuada y, si utiliza ubicación y picking directos, una zona, a esta nueva línea, o continúe dividiendo la línea según sea necesario hasta que encuentre ubicaciones apropiadas para toda la cantidad.</span><span class="sxs-lookup"><span data-stu-id="4e0af-115">Assign an appropriate bin and, if you are using directed put-away and pick, a zone, to this new line, or continue splitting the line as necessary until you find appropriate bins for all of the quantity.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4e0af-116">Si utiliza ubicación y picking directos y divide las líneas, debe estar familiarizado con el almacén y poder elegir una ubicación que cumpla los requisitos de almacenamiento del producto y cubra los requisitos generales del documento de almacén.</span><span class="sxs-lookup"><span data-stu-id="4e0af-116">If the location uses directed put-away and pick and you split the lines, you must be familiar with the warehouse and be able to choose a bin that matches the storage requirements of the item and that fulfills the general requirements of the warehouse document.</span></span> <span data-ttu-id="4e0af-117">Por ejemplo, no debería dividir una línea de un documento de picking y colocar algunos productos en el área de almacenamiento masivo.</span><span class="sxs-lookup"><span data-stu-id="4e0af-117">For example, you would not split a line on a pick document and place some items in the bulk storage.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e0af-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e0af-118">See Also</span></span>  
[<span data-ttu-id="4e0af-119">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="4e0af-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4e0af-120">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="4e0af-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4e0af-121">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="4e0af-121">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="4e0af-122">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4e0af-122">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4e0af-123">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="4e0af-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4e0af-124">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e0af-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
