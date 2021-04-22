---
title: Cálculo de la fecha de compra | Documentos de Microsoft
description: La aplicación calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b65e082355623f422cfb03698f6413fdb04f0daf
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780262"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="e9ed8-104">Cálculo de la fecha de compras</span><span class="sxs-lookup"><span data-stu-id="e9ed8-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e9ed8-105">calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="e9ed8-106">Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="e9ed8-107">Si especifica una fecha de recepción solicitada en la cabecera de un pedido de compra, la fecha de pedido calculada será aquella en la que se debe realizar el pedido para recibir los artículos en la fecha solicitada.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="e9ed8-108">A continuación, la fecha en que los artículos estarán disponibles para picking se calcula y se especifica en el campo **Fecha recepción esperada**.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="e9ed8-109">Si no especifica una fecha de recepción esperada, se utiliza la fecha de pedido de la línea como punto inicial para calcular la fecha en la que se espera recibir los productos y la fecha en la que estarán disponibles para picking.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="e9ed8-110">Realizar cálculos con una fecha de recepción solicitada</span><span class="sxs-lookup"><span data-stu-id="e9ed8-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="e9ed8-111">Si hay una fecha de recepción solicitada en la línea de pedido de compra, esa fecha se utiliza como punto inicial de los cálculos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="e9ed8-112">fecha de recepción solicitada – plazo entrega (días) = fecha de pedido</span><span class="sxs-lookup"><span data-stu-id="e9ed8-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="e9ed8-113">fecha recepción solicitada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada</span><span class="sxs-lookup"><span data-stu-id="e9ed8-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="e9ed8-114">Si introdujo una fecha de recepción solicitada en la cabecera del pedido de compra, se copia al campo correspondiente en todas las líneas.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="e9ed8-115">Puede modificarla o eliminarla en cualquiera de las líneas.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="e9ed8-116">Si su proceso se basa en el cálculo hacia atrás, por ejemplo, si utiliza la fecha de recepción solicitada para obtener la fecha de pedido, le recomendamos que utilice fórmulas de fecha que tengan duraciones fijas, como "5D" para cinco días o "1S" para una semana.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="e9ed8-117">Las fórmulas de fecha sin duraciones fijas, como "SA" para la semana actual o MA para el mes actual, pueden dar lugar a cálculos de fecha incorrectos.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="e9ed8-118">Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="e9ed8-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="e9ed8-119">Realizar cálculos sin una fecha de entrega requerida</span><span class="sxs-lookup"><span data-stu-id="e9ed8-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="e9ed8-120">Si especifica una línea de pedido de compra sin una fecha de entrega solicitada, se rellena el campo **Fecha pedido** de la línea con la fecha del campo **Fecha pedido** de la cabecera del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="e9ed8-121">Se trata de la fecha que especificó o la fecha del trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="e9ed8-122">Se utiliza la fecha del pedido como punto inicial para calcular las fechas siguientes de la línea del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="e9ed8-123">fecha pedido + plazo entrega (días) = fecha recepción planificada.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="e9ed8-124">fecha recepción planificada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada</span><span class="sxs-lookup"><span data-stu-id="e9ed8-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="e9ed8-125">Si modifica la fecha de pedido de la línea, por ejemplo, cuando el proveedor no va tener los productos disponibles sino para una fecha posterior, se vuelven a calcular automáticamente las fechas correspondientes de la línea.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="e9ed8-126">Si modifica la fecha de pedido de la cabecera, se copia en el campo **Fecha pedido** de todas las líneas y se vuelven a calcular todos los campos de fecha relacionados.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="e9ed8-127">Valores predeterminados para el cálculo del tiempo de entrega</span><span class="sxs-lookup"><span data-stu-id="e9ed8-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e9ed8-128">usa el valor del campo **Cálculo del plazo de entrega** en la línea del pedido de compra para calcular el pedido y las fechas de recepción esperadas.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="e9ed8-129">Puede especificar manualmente el valor en la línea o dejar que el programa utilice valores definidos en la tarjeta de proveedor, la tarjeta de artículo, la tarjeta de la unidad de almacenamiento o el catálogo de proveedores de artículos.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="e9ed8-130">Sin embargo, el valor del tiempo de entrega en la tarjeta de proveedor se usa solo si no se especifica un tiempo de entrega en la tarjeta del artículo, la tarjeta de la unidad de almacenamiento o el catálogo del proveedor del artículo.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="e9ed8-131">Este es también el orden de prioridad creciente de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="e9ed8-132">Si se proporcionan todos, el tiempo de entrega de la tarjeta de proveedor tiene la prioridad más baja y el tiempo de entrega del catálogo de proveedores de artículos tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="e9ed8-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9ed8-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9ed8-133">See Also</span></span>

<span data-ttu-id="e9ed8-134">[Cálculo de fecha de ventas](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="e9ed8-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="e9ed8-135">Calcular fechas de compromiso de entrega de pedido</span><span class="sxs-lookup"><span data-stu-id="e9ed8-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="e9ed8-136">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9ed8-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]