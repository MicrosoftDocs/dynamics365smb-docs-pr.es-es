---
title: Usar el proceso Proponer pagos a proveedores | Documentos de Microsoft
description: "Puede especificar la configuración de pago al proveedor para obtener sugerencias o propuestas de pagos que están a punto de vencer o en los que hay un descuento."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: af35aa77bfe288fb810dd2b9b06be6026e012da7
ms.contentlocale: es-es
ms.lasthandoff: 04/16/2018

---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="7f970-103">Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="7f970-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="7f970-104">En la ventana **Diario de pagos** puede usar el proceso **Proponer pagos a proveedores** para sugerir líneas de pago.</span><span class="sxs-lookup"><span data-stu-id="7f970-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="7f970-105">Las líneas de elementos como pagos que están a punto de vencer, o de pagos en los que hay disponible un descuento por pronto pago, se sugieren según la configuración.</span><span class="sxs-lookup"><span data-stu-id="7f970-105">Lines for things like payments that are due soon, or payments where a payment discount is available, are suggested based on your settings.</span></span>

<span data-ttu-id="7f970-106">Para obtener ventaja completa de las líneas sugeridas, primero debe asignar prioridades a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="7f970-106">To benefit fully from suggested lines, you must first prioritize your vendors.</span></span> <span data-ttu-id="7f970-107">Para obtener más información, consulte [Dar prioridad a proveedores](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="7f970-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

<span data-ttu-id="7f970-108">No se incluyen los movimientos de proveedor no son del tipo **Esperar**.</span><span class="sxs-lookup"><span data-stu-id="7f970-108">Vendor entries that are not **On Hold** are not included.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="7f970-109">Si desea aprovechar los descuentos por pronto pago y ha introducido un importe disponible, el importe se utilizará para:</span><span class="sxs-lookup"><span data-stu-id="7f970-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  

* <span data-ttu-id="7f970-110">Movimientos de proveedor vencidos con prioridad, primero en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="7f970-110">Prioritized overdue vendor entries first in order of priority.</span></span>  
* <span data-ttu-id="7f970-111">Movimientos de proveedor vencidos que no tienen prioridad.</span><span class="sxs-lookup"><span data-stu-id="7f970-111">Overdue vendor entries that are not prioritized.</span></span>  
* <span data-ttu-id="7f970-112">Movimientos de proveedor pendientes que cumplen los requisitos para descuentos por pronto pago, organizados por número del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7f970-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="7f970-113">Para usar la función Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="7f970-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="7f970-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7f970-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7f970-115">Abra el diario pertinente y, a continuación, elija la acción **Proponer pagos a proveedor**.</span><span class="sxs-lookup"><span data-stu-id="7f970-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="7f970-116">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7f970-116">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="7f970-117">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7f970-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="7f970-118">Para insertar la fecha de vencimiento como fecha de registro en líneas de diario de pagos</span><span class="sxs-lookup"><span data-stu-id="7f970-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="7f970-119">Cuando use el proceso **Proponer pagos a proveedores** para crear las líneas de pago para los proveedores, puede rellenar dos campos especiales para asegurarse de que las líneas de planificación usan la fecha de vencimiento para calcular la fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="7f970-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="7f970-120">Estos campos son **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** y **Desfase fecha de vencimiento de documento de aplicación**.</span><span class="sxs-lookup"><span data-stu-id="7f970-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="7f970-121">No puede usar el campo **Calcular fecha de registro a partir de fecha de vencimiento de documento de aplicación** junto con el campo **Buscar dtos. P.P.** o el campo **Una línea por proveedor**.</span><span class="sxs-lookup"><span data-stu-id="7f970-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="7f970-122">Si la fecha de registro se basa en la fecha de vencimiento, es posible que no se puedan calcular correctamente los descuentos por pronto pago, porque la fecha de registro es posterior a la fecha del descuento por pronto pago.</span><span class="sxs-lookup"><span data-stu-id="7f970-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="7f970-123">Además, si la fecha de registro calculada está en el pasado, la fecha de registro se adelanta a la fecha de trabajo y aparece una advertencia.</span><span class="sxs-lookup"><span data-stu-id="7f970-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="7f970-124">De forma alternativa, puede crear manualmente las líneas de pago con la fecha de vencimiento a fin de calcular la fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="7f970-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="7f970-125">Después de aplicar los movimientos de proveedor, puede utilizar la acción **Calcular fecha de registro** para actualizar la fecha de registro de la línea del diario con la fecha de vencimiento de la factura de compra relacionada.</span><span class="sxs-lookup"><span data-stu-id="7f970-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="7f970-126">Para obtener más información, consulte [Liquidar transacciones de compra manualmente](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="7f970-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="7f970-127">Si la factura de compra tiene fecha vencida, la fecha de registro se establece en la fecha de trabajo, y la fuente de la línea cambia a color rojo.</span><span class="sxs-lookup"><span data-stu-id="7f970-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7f970-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f970-128">See Also</span></span>
[<span data-ttu-id="7f970-129">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="7f970-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="7f970-130">Creación de pagos</span><span class="sxs-lookup"><span data-stu-id="7f970-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="7f970-131">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="7f970-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="7f970-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7f970-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

