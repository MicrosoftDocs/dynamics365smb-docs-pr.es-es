---
title: Establecer límites para fechas de vencimiento
description: Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7685ef682f0d79c68cc694f665fc0da89cd84b5e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189175"
---
# <a name="set-limits-for-due-dates"></a><span data-ttu-id="c720c-103">Establecer límites para fechas de vencimiento</span><span class="sxs-lookup"><span data-stu-id="c720c-103">Set Limits for Due Dates</span></span>
<span data-ttu-id="c720c-104">Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c720c-104">You can modify payment terms to have limits for the maximum number of days that can be between a delivery and the corresponding payment.</span></span>  

<span data-ttu-id="c720c-105">Los límites legales del espacio entre su entrega y pago determinan cómo se calculan las fechas de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="c720c-105">Legal limits for the gap between delivery and payment determine how due dates are calculated.</span></span> <span data-ttu-id="c720c-106">Por ejemplo, si crea un término de pago que se utilizará para ventas al sector público, el campo **Nº máx. días hasta fecha vencimiento** para ese plazo de pago debe establecerse en 30 días.</span><span class="sxs-lookup"><span data-stu-id="c720c-106">For example, if you create a payment term that will be used for sales to the public sector, the **Max. No. of Days till Due Date** field for that payment term must be set to 30 days.</span></span>  

## <a name="to-set-limits-for-due-dates-on-payment-terms"></a><span data-ttu-id="c720c-107">Para definir los límites para las fechas de vencimiento en términos de pago</span><span class="sxs-lookup"><span data-stu-id="c720c-107">To set limits for due dates on payment terms</span></span>  

1.  <span data-ttu-id="c720c-108">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Condiciones de pago** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c720c-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c720c-109">Seleccione el término de pago que desea modificar y, a continuación, en el campo **Nº máx. días hasta fecha vencimiento**, especifique el número de días naturales permitidos entre su entrega y el pago.</span><span class="sxs-lookup"><span data-stu-id="c720c-109">Select the payment term that you want to modify, and then, in the **Max. No. of Days till Due Date** field, specify the number of calendar days to allow between delivery and payment.</span></span>  

<span data-ttu-id="c720c-110">A continuación, debe asegurarse de especificar los términos de pago adecuados para sus clientes y proveedores públicos y privados.</span><span class="sxs-lookup"><span data-stu-id="c720c-110">Next, you must make sure that you specify the appropriate payment terms for your public and private customers and vendors.</span></span> <span data-ttu-id="c720c-111">Cuando crea un documento para ese cliente o proveedor, la fecha de vencimiento del pago se calcula a partir del día en que el cliente recibió los artículos o servicios.</span><span class="sxs-lookup"><span data-stu-id="c720c-111">When you create a document for that customer or vendor, the due date for the payment is calculated from the day that the customer received the items or services.</span></span> <span data-ttu-id="c720c-112">A continuación, debe actualizar el campo **Fecha del documento** con la fecha del recibo.</span><span class="sxs-lookup"><span data-stu-id="c720c-112">Then, you must update the **Document Date** field for the document with the date of the receipt.</span></span> <span data-ttu-id="c720c-113">Por ejemplo, si actualiza una factura de ventas cuando se le informa de la entrega, la fecha de vencimiento se calcula en función de la nueva fecha del documento que especificó.</span><span class="sxs-lookup"><span data-stu-id="c720c-113">For example, if you update a sales invoice when you are informed of delivery, the due date is calculated based on the new document date that you specified.</span></span> <span data-ttu-id="c720c-114">La fecha de vencimiento calculada no puede superar el límite que especificó para el plazo de pago.</span><span class="sxs-lookup"><span data-stu-id="c720c-114">The calculated due date cannot be further away than the limit that you specified for the payment term.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c720c-115">No puede registrar un documento que crea una remesa donde uno o varios plazos tienen una fecha de vencimiento posterior al límite que se especifica en el campo **Nº máx. días hasta fecha vencimiento**.</span><span class="sxs-lookup"><span data-stu-id="c720c-115">You cannot post a document that creates a bill where one or more installments have a due date that is later than the limit that is specified in the **Max. No. of Days till Due Date** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c720c-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c720c-116">See Also</span></span>  
 [<span data-ttu-id="c720c-117">Cálculo de fechas de vencimiento</span><span class="sxs-lookup"><span data-stu-id="c720c-117">Calculating Due Dates</span></span>](calculating-due-dates.md)
