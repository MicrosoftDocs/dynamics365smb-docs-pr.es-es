---
title: "Establecer límites para fechas de vencimiento"
description: "Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a9718dfdacdc360f59621d0264211046d5b1b537
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-limits-for-due-dates"></a><span data-ttu-id="60ce0-103">Establecer límites para fechas de vencimiento</span><span class="sxs-lookup"><span data-stu-id="60ce0-103">Set Limits for Due Dates</span></span>
<span data-ttu-id="60ce0-104">Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente.</span><span class="sxs-lookup"><span data-stu-id="60ce0-104">You can modify payment terms to have limits for the maximum number of days that can be between a delivery and the corresponding payment.</span></span>  

<span data-ttu-id="60ce0-105">Los límites legales del espacio entre su entrega y pago determinan cómo se calculan las fechas de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="60ce0-105">Legal limits for the gap between delivery and payment determine how due dates are calculated.</span></span> <span data-ttu-id="60ce0-106">Por ejemplo, si crea un término de pago que se utilizará para ventas al sector público, el campo **Nº máx. días hasta fecha vencimiento** para ese plazo de pago debe establecerse en 30 días.</span><span class="sxs-lookup"><span data-stu-id="60ce0-106">For example, if you create a payment term that will be used for sales to the public sector, the **Max. No. of Days till Due Date** field for that payment term must be set to 30 days.</span></span>  

## <a name="to-set-limits-for-due-dates-on-payment-terms"></a><span data-ttu-id="60ce0-107">Para definir los límites para las fechas de vencimiento en términos de pago</span><span class="sxs-lookup"><span data-stu-id="60ce0-107">To set limits for due dates on payment terms</span></span>  

1.  <span data-ttu-id="60ce0-108">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Condiciones de pago** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="60ce0-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="60ce0-109">Seleccione el término de pago que desea modificar y, a continuación, en el campo **Nº máx. días hasta fecha vencimiento**, especifique el número de días naturales permitidos entre su entrega y el pago.</span><span class="sxs-lookup"><span data-stu-id="60ce0-109">Select the payment term that you want to modify, and then, in the **Max. No. of Days till Due Date** field, specify the number of calendar days to allow between delivery and payment.</span></span>  

<span data-ttu-id="60ce0-110">A continuación, debe asegurarse de especificar los términos de pago adecuados para sus clientes y proveedores públicos y privados.</span><span class="sxs-lookup"><span data-stu-id="60ce0-110">Next, you must make sure that you specify the appropriate payment terms for your public and private customers and vendors.</span></span> <span data-ttu-id="60ce0-111">Cuando crea un documento para ese cliente o proveedor, la fecha de vencimiento del pago se calcula a partir del día en que el cliente recibió los artículos o servicios.</span><span class="sxs-lookup"><span data-stu-id="60ce0-111">When you create a document for that customer or vendor, the due date for the payment is calculated from the day that the customer received the items or services.</span></span> <span data-ttu-id="60ce0-112">A continuación, debe actualizar el campo **Fecha del documento** con la fecha del recibo.</span><span class="sxs-lookup"><span data-stu-id="60ce0-112">Then, you must update the **Document Date** field for the document with the date of the receipt.</span></span> <span data-ttu-id="60ce0-113">Por ejemplo, si actualiza una factura de ventas cuando se le informa de la entrega, la fecha de vencimiento se calcula en función de la nueva fecha del documento que especificó.</span><span class="sxs-lookup"><span data-stu-id="60ce0-113">For example, if you update a sales invoice when you are informed of delivery, the due date is calculated based on the new document date that you specified.</span></span> <span data-ttu-id="60ce0-114">La fecha de vencimiento calculada no puede superar el límite que especificó para el plazo de pago.</span><span class="sxs-lookup"><span data-stu-id="60ce0-114">The calculated due date cannot be further away than the limit that you specified for the payment term.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="60ce0-115">No puede registrar un documento que crea una remesa donde uno o varios plazos tienen una fecha de vencimiento posterior al límite que se especifica en el campo **Nº máx. días hasta fecha vencimiento**.</span><span class="sxs-lookup"><span data-stu-id="60ce0-115">You cannot post a document that creates a bill where one or more installments have a due date that is later than the limit that is specified in the **Max. No. of Days till Due Date** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60ce0-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60ce0-116">See Also</span></span>  
 [<span data-ttu-id="60ce0-117">Cálculo de fechas de vencimiento</span><span class="sxs-lookup"><span data-stu-id="60ce0-117">Calculating Due Dates</span></span>](calculating-due-dates.md)

