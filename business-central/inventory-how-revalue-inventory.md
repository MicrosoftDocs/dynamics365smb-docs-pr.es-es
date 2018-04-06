---
title: Crear nuevos movimientos de valor para los productos del inventario | Documentos de Microsoft
description: "Describe cómo apreciar o amortizar los movimientos de valor de uno o varios productos del inventario enviando el valor calculado actual."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6f52795bf47b3ebddd446105b92d526a83748fc8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="cdfa9-103">Revaluar inventario</span><span class="sxs-lookup"><span data-stu-id="cdfa9-103">Revalue Inventory</span></span>
<span data-ttu-id="cdfa9-104">Si desea apreciar o depreciar un producto o el movimiento de un determinado producto, utilice el diario de revalorización.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="cdfa9-105">Para revaluar el inventario</span><span class="sxs-lookup"><span data-stu-id="cdfa9-105">To revalue inventory</span></span>
1. <span data-ttu-id="cdfa9-106">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario revalorizac.** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cdfa9-107">Elija la acción **Calcular valor inventario**.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="cdfa9-108">En la ventana **Calcular valor inventario**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="cdfa9-109">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="cdfa9-110">En cada línea de la ventana **Diario de revalorización**, en el campo **Prec. coste (revaluado)**, especifique el nuevo coste unitario.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="cdfa9-111">También puede especificar el nuevo importe total en el campo **Valor inventario (revalorado)**.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="cdfa9-112">Los campos correspondientes se actualizan de forma automática.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="cdfa9-113">Observe que el campo **Importe** muestra el cambio real ocurrido en el valor de inventario del movimiento de producto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="cdfa9-114">Muestra la diferencia entre el valor del campo **Valor stock (calculado)** y el del campo **Valor inventario (revaluado)**.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="cdfa9-115">Una vez completadas todas las líneas en el diario de revalorización, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="cdfa9-116">Las nuevas entradas de valor ahora se crean de modo que reflejan las revalorizaciones que ha registrado.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="cdfa9-117">Puede ver los nuevos valores en las respectivas tarjetas de producto.</span><span class="sxs-lookup"><span data-stu-id="cdfa9-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdfa9-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cdfa9-118">See Also</span></span>
[<span data-ttu-id="cdfa9-119">Detalles de diseño: Revalorización</span><span class="sxs-lookup"><span data-stu-id="cdfa9-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="cdfa9-120">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="cdfa9-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="cdfa9-121">Ccial</span><span class="sxs-lookup"><span data-stu-id="cdfa9-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="cdfa9-122">Compras</span><span class="sxs-lookup"><span data-stu-id="cdfa9-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cdfa9-123">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cdfa9-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

