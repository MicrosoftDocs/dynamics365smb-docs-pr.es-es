---
title: Cálculo de la fecha de ventas | Documentos de Microsoft
description: La aplicación calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a8f272b73f7cc5940f2e0b845c62fd28395b6923
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926327"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="9648c-104">Cálculo de fecha de ventas</span><span class="sxs-lookup"><span data-stu-id="9648c-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9648c-105">calcula automáticamente la fecha más próxima posible en la que se puede enviar un producto incluido en una línea de pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="9648c-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="9648c-106">Si el cliente solicita una fecha de entrega concreta, se calcula la fecha en que los productos deberán estar disponibles para el picking y poder realizar su entrega en dicha fecha.</span><span class="sxs-lookup"><span data-stu-id="9648c-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="9648c-107">Si el cliente no solicita una fecha de entrega concreta, se calcula la fecha en que los productos se podrán entregar, a partir de la fecha en que estén disponibles para el picking.</span><span class="sxs-lookup"><span data-stu-id="9648c-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="9648c-108">Realizar cálculos de una Fecha de entrega requerida</span><span class="sxs-lookup"><span data-stu-id="9648c-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="9648c-109">Si escribe una fecha de entrega requerida en la línea de pedido de venta, dicha fecha se convertirá en el punto inicial para los cálculos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9648c-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="9648c-110">Fecha entrega requerida - Hora envío = Fecha envío planeada</span><span class="sxs-lookup"><span data-stu-id="9648c-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="9648c-111">Fecha envío planeada - Tiempo manip. alm. salida = Fecha envío</span><span class="sxs-lookup"><span data-stu-id="9648c-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="9648c-112">Si los productos están disponibles para el picking en la fecha de envío, el proceso de venta puede continuar.</span><span class="sxs-lookup"><span data-stu-id="9648c-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="9648c-113">De lo contrario, se muestra una advertencia de falta de stock.</span><span class="sxs-lookup"><span data-stu-id="9648c-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="9648c-114">Si su proceso se basa en el cálculo hacia atrás, por ejemplo, si utiliza la fecha de entrega solicitada para obtener la fecha de envío planificada, le recomendamos que utilice fórmulas de fecha que tengan duraciones fijas, como "5D" para cinco días o "1S" para una semana.</span><span class="sxs-lookup"><span data-stu-id="9648c-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="9648c-115">Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos.</span><span class="sxs-lookup"><span data-stu-id="9648c-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="9648c-116">Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="9648c-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="9648c-117">Cálculo de fecha de entrega más próxima posible</span><span class="sxs-lookup"><span data-stu-id="9648c-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="9648c-118">Si no especifica una fecha de entrega requerida en la línea de pedido de venta, o si la fecha de entrega requerida no se puede cumplir, se calculará la fecha más próxima en la que estarán disponibles los productos.</span><span class="sxs-lookup"><span data-stu-id="9648c-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="9648c-119">A continuación se insertará dicha fecha en la línea del campo Fecha envío y utiliza las siguientes formulas para calcular la fecha prevista para el envío de los productos y la fecha de su entrega al cliente:</span><span class="sxs-lookup"><span data-stu-id="9648c-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="9648c-120">Fecha envío + Tiempo manip. alm. salida = Fecha envío planeada</span><span class="sxs-lookup"><span data-stu-id="9648c-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="9648c-121">Fecha envío planeada + Hora envío = Fecha entrega planeada</span><span class="sxs-lookup"><span data-stu-id="9648c-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="9648c-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9648c-122">See Also</span></span>  
 <span data-ttu-id="9648c-123">[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="9648c-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="9648c-124">Calcular fechas de compromiso de entrega de pedido</span><span class="sxs-lookup"><span data-stu-id="9648c-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="9648c-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9648c-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
