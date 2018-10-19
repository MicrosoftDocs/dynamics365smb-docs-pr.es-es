---
title: "Cómo registrar consumibles por lotes | Documentos de Microsoft"
description: "Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b7799e652394e8b9b96a168c0cb8945ec332734e
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="bd401-103">Registrar consumibles de producción por lotes</span><span class="sxs-lookup"><span data-stu-id="bd401-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="bd401-104">Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.</span><span class="sxs-lookup"><span data-stu-id="bd401-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="bd401-105">También puede configurar el sistema para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción.</span><span class="sxs-lookup"><span data-stu-id="bd401-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="bd401-106">Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="bd401-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="bd401-107">Para registrar el consumo en una o varias líneas de la orden de producción</span><span class="sxs-lookup"><span data-stu-id="bd401-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="bd401-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario consumo** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="bd401-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bd401-109">Rellene los campos con los datos de las órdenes de producción y del consumo.</span><span class="sxs-lookup"><span data-stu-id="bd401-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="bd401-110">Si el almacén donde se almacenan los componentes está configurado para utilizar ubicaciones, pero no requiere el proceso de picking, asigne un código de ubicación a la línea del diario para indicar de dónde se deben obtener los productos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="bd401-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="bd401-111">Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="bd401-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="bd401-112">Para registrar el consumo, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="bd401-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="bd401-113">Se reducen los correspondientes movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="bd401-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd401-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd401-114">See Also</span></span>  
<span data-ttu-id="bd401-115">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="bd401-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="bd401-116">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="bd401-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="bd401-117">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="bd401-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="bd401-118">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="bd401-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="bd401-119">Compras</span><span class="sxs-lookup"><span data-stu-id="bd401-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bd401-120">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd401-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

