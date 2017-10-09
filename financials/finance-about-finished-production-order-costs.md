---
title: "Sobre los costes del orden de producción terminada | Documentos de Microsoft"
description: "La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Los costes finales, incluidas las desviaciones en un entorno de costes estándar, costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso de trabajo por lotes **costes ajustados - movimientos de productos**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 010d4d4568f45cbe8fe13864ac6996de1e224b76
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="1c9a5-104">Sobre los costes del orden de producción terminada</span><span class="sxs-lookup"><span data-stu-id="1c9a5-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="1c9a5-105">La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="1c9a5-106">Los costes finales, entre los que se incluyen las desviaciones en un entorno de costes estándar y los costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso **Valorar stock - movs. producto**, que permite realizar la conciliación financiera de los costes de la fabricación de productos.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="1c9a5-107">Para que una orden de producción se tenga en cuenta en el ajuste de costes, el estado debe ser **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="1c9a5-108">Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="1c9a5-109">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1c9a5-109">Example</span></span>  
 <span data-ttu-id="1c9a5-110">En un entorno de coste estándar, cuando se consume material para fabricar un producto, el coste del producto más la mano de obra y los gastos generales se incluyen en el WIP.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="1c9a5-111">Cuando se fabrica el producto, el WIP es reduce en el importe del coste estándar del artículo.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="1c9a5-112">Normalmente, estos costes no dan cero como resultado.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="1c9a5-113">Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar stock - movs. producto**, teniendo en cuenta que sólo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="1c9a5-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1c9a5-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c9a5-114">See Also</span></span>  
[<span data-ttu-id="1c9a5-115">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="1c9a5-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="1c9a5-116">Fabricación</span><span class="sxs-lookup"><span data-stu-id="1c9a5-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="1c9a5-117">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c9a5-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

