---
title: Sobre los costes del orden de producción terminada | Documentos de Microsoft
description: La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Los costes finales, incluidas las desviaciones en un entorno de costes estándar, costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso de trabajo por lotes Costes ajustados - movimientos de productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e1116d99a2893c3fef8fd2306b79cb2252c04d77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389429"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="04a04-104">Sobre los costes del orden de producción terminada</span><span class="sxs-lookup"><span data-stu-id="04a04-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="04a04-105">La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando.</span><span class="sxs-lookup"><span data-stu-id="04a04-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="04a04-106">Los costes finales, entre los que se incluyen las desviaciones en un entorno de costes estándar y los costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso **Valorar stock - movs. producto**, que permite realizar la conciliación financiera de los costes de la fabricación de productos.</span><span class="sxs-lookup"><span data-stu-id="04a04-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="04a04-107">Para que una orden de producción se tenga en cuenta en el ajuste de costes, el estado debe ser **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="04a04-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="04a04-108">Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="04a04-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="04a04-109">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="04a04-109">Example</span></span>  
 <span data-ttu-id="04a04-110">En un entorno de coste estándar, cuando se consume material para fabricar un producto, el coste del producto más la mano de obra y los gastos generales se incluyen en el WIP.</span><span class="sxs-lookup"><span data-stu-id="04a04-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="04a04-111">Cuando se fabrica el producto, el WIP es reduce en el importe del coste estándar del artículo.</span><span class="sxs-lookup"><span data-stu-id="04a04-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="04a04-112">Normalmente, estos costes no dan cero como resultado.</span><span class="sxs-lookup"><span data-stu-id="04a04-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="04a04-113">Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar stock - movs. producto**, teniendo en cuenta que sólo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.</span><span class="sxs-lookup"><span data-stu-id="04a04-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04a04-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04a04-114">See Also</span></span>  
[<span data-ttu-id="04a04-115">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="04a04-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="04a04-116">Fabricación</span><span class="sxs-lookup"><span data-stu-id="04a04-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="04a04-117">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04a04-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]