---
title: Cómo registrar consumibles por lotes | Documentos de Microsoft
description: Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bf0a92d05b6c9ecb3d5a5ba054b4675680ad43c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391804"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="87fb5-103">Registrar consumibles de producción por lotes</span><span class="sxs-lookup"><span data-stu-id="87fb5-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="87fb5-104">Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.</span><span class="sxs-lookup"><span data-stu-id="87fb5-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="87fb5-105">También puede configurar el sistema para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción.</span><span class="sxs-lookup"><span data-stu-id="87fb5-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="87fb5-106">Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="87fb5-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="87fb5-107">Para registrar el consumo en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="87fb5-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="87fb5-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario de consumo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="87fb5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="87fb5-109">Rellene los campos con los datos de las órdenes de producción y del consumo.</span><span class="sxs-lookup"><span data-stu-id="87fb5-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="87fb5-110">Si el almacén donde se almacenan los componentes está configurado para utilizar ubicaciones, pero no requiere el proceso de picking, asigne un código de ubicación a la línea del diario para indicar de dónde se deben obtener los productos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="87fb5-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="87fb5-111">Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="87fb5-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="87fb5-112">Para registrar el consumo, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="87fb5-113">Se reducen los correspondientes movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="87fb5-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="87fb5-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="87fb5-114">See Also</span></span>  
<span data-ttu-id="87fb5-115">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="87fb5-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="87fb5-116">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="87fb5-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="87fb5-117">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="87fb5-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="87fb5-118">Inventario</span><span class="sxs-lookup"><span data-stu-id="87fb5-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="87fb5-119">Compras</span><span class="sxs-lookup"><span data-stu-id="87fb5-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="87fb5-120">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87fb5-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]