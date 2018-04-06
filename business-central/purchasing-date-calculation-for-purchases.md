---
title: "Cálculo de la fecha de compra | Documentos de Microsoft"
description: "El programa calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada. Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8224f609dd110cd9f5d01d33d8e207f0c4aef6e0
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="d93fe-104">Cálculo de la fecha de compras</span><span class="sxs-lookup"><span data-stu-id="d93fe-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d93fe-105"> calcula automáticamente la fecha en la que se debe solicitar un producto para tenerlo en el inventario en una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="d93fe-105"> automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="d93fe-106">Esta es la fecha en la que puede contar con que los productos solicitados en una fecha determinada estén disponibles para picking.</span><span class="sxs-lookup"><span data-stu-id="d93fe-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="d93fe-107">Si especifica una fecha de recepción solicitada en la cabecera de un pedido de compra, la fecha de pedido calculada será aquella en la que se debe realizar el pedido para recibir los artículos en la fecha solicitada.</span><span class="sxs-lookup"><span data-stu-id="d93fe-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="d93fe-108">A continuación, la fecha en que los artículos estarán disponibles para picking se calcula y se especifica en el campo **Fecha recepción esperada**.</span><span class="sxs-lookup"><span data-stu-id="d93fe-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="d93fe-109">Si no especifica una fecha de recepción esperada, se utiliza la fecha de pedido de la línea como punto inicial para calcular la fecha en la que se espera recibir los productos y la fecha en la que estarán disponibles para picking.</span><span class="sxs-lookup"><span data-stu-id="d93fe-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="d93fe-110">Realizar cálculos con una fecha de recepción solicitada</span><span class="sxs-lookup"><span data-stu-id="d93fe-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="d93fe-111">Si hay una fecha de recepción solicitada en la línea de pedido de compra, esa fecha se utiliza como punto inicial de los cálculos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d93fe-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="d93fe-112">fecha de recepción solicitada – plazo entrega (días) = fecha de pedido</span><span class="sxs-lookup"><span data-stu-id="d93fe-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="d93fe-113">fecha recepción solicitada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada</span><span class="sxs-lookup"><span data-stu-id="d93fe-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="d93fe-114">Si introdujo una fecha de recepción solicitada en la cabecera del pedido de compra, se copia al campo correspondiente en todas las líneas.</span><span class="sxs-lookup"><span data-stu-id="d93fe-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="d93fe-115">Puede modificarla o eliminarla en cualquiera de las líneas.</span><span class="sxs-lookup"><span data-stu-id="d93fe-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="d93fe-116">Realizar cálculos sin una fecha de entrega requerida</span><span class="sxs-lookup"><span data-stu-id="d93fe-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="d93fe-117">Si especifica una línea de pedido de compra sin una fecha de entrega solicitada, se rellena el campo **Fecha pedido** de la línea con la fecha del campo **Fecha pedido** de la cabecera del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="d93fe-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="d93fe-118">Se trata de la fecha que especificó o la fecha del trabajo.</span><span class="sxs-lookup"><span data-stu-id="d93fe-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="d93fe-119">Se utiliza la fecha del pedido como punto inicial para calcular las fechas siguientes de la línea del pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="d93fe-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="d93fe-120">fecha pedido + plazo entrega (días) = fecha recepción planificada.</span><span class="sxs-lookup"><span data-stu-id="d93fe-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="d93fe-121">fecha recepción planificada + tiempo manipulación almacén salida + plazo de seguridad = fecha recepción esperada</span><span class="sxs-lookup"><span data-stu-id="d93fe-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="d93fe-122">Si modifica la fecha de pedido de la línea, por ejemplo, cuando el proveedor no va tener los productos disponibles sino para una fecha posterior, se vuelven a calcular automáticamente las fechas correspondientes de la línea.</span><span class="sxs-lookup"><span data-stu-id="d93fe-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="d93fe-123">Si modifica la fecha de pedido de la cabecera, se copia en el campo **Fecha pedido** de todas las líneas y se vuelven a calcular todos los campos de fecha relacionados.</span><span class="sxs-lookup"><span data-stu-id="d93fe-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d93fe-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d93fe-124">See Also</span></span>  
 <span data-ttu-id="d93fe-125">[Cálculo de fecha de ventas](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="d93fe-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="d93fe-126">Calcular fechas de compromiso de entrega de pedido</span><span class="sxs-lookup"><span data-stu-id="d93fe-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="d93fe-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d93fe-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

