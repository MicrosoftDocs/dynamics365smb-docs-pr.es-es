---
title: Facturar prepagos | Documentos de Microsoft
description: Los prepagos son pagos que se facturan y registran en un pedido de prepago de ventas o compras antes de la facturación final. Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente. La funcionalidad de prepagos le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores. De este modo, puede asegurar que todos los pagos se registran contra una factura.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e4a3426ef55bdc08088bb13720be123c117043b8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380900"
---
# <a name="invoicing-prepayments"></a><span data-ttu-id="f4baf-106">Facturación de prepagos</span><span class="sxs-lookup"><span data-stu-id="f4baf-106">Invoicing Prepayments</span></span>

<span data-ttu-id="f4baf-107">Los prepagos son pagos que se facturan y registran en un pedido de prepago de ventas o compras antes de la facturación final.</span><span class="sxs-lookup"><span data-stu-id="f4baf-107">Prepayments are payments that are invoiced and posted to a sales or purchase prepayment order before final invoicing.</span></span> <span data-ttu-id="f4baf-108">Puede requerir un depósito antes de fabricar productos bajo pedido o puede requerir el pago antes de enviar productos a un cliente.</span><span class="sxs-lookup"><span data-stu-id="f4baf-108">You might require a deposit before you manufacture items to order, or you might require payment before you ship items to a customer.</span></span> <span data-ttu-id="f4baf-109">La funcionalidad de prepagos le permite facturar y cobrar depósitos requeridos de los clientes o remitir depósitos a proveedores.</span><span class="sxs-lookup"><span data-stu-id="f4baf-109">The prepayments functionality enables you to invoice and collect deposits required from customers or to remit deposits to vendors.</span></span> <span data-ttu-id="f4baf-110">De este modo, puede asegurar que todos los pagos se registran contra una factura.</span><span class="sxs-lookup"><span data-stu-id="f4baf-110">Thus, you can ensure that all payments are posted against an invoice.</span></span>  

 <span data-ttu-id="f4baf-111">Los requisitos de los prepagos se pueden definir para un cliente o proveedor, para todos los productos o para algunos.</span><span class="sxs-lookup"><span data-stu-id="f4baf-111">Prepayment requirements can be defined for a customer or vendor for all items or selected items.</span></span> <span data-ttu-id="f4baf-112">Una vez realizada la configuración necesaria, puede generar facturas de prepago a partir de pedidos de compra y venta para el importe calculado del prepago.</span><span class="sxs-lookup"><span data-stu-id="f4baf-112">After you complete the required setup, you can generate prepayment invoices from sales and purchase orders for the calculated prepayment amount.</span></span> <span data-ttu-id="f4baf-113">Puede cambiar los importes en la factura según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f4baf-113">You can change the amounts on the invoice as needed.</span></span> <span data-ttu-id="f4baf-114">Por ejemplo, puede especificar un importe total para todo el pedido.</span><span class="sxs-lookup"><span data-stu-id="f4baf-114">For example, you can specify a total amount for the entire order.</span></span> <span data-ttu-id="f4baf-115">También puede enviar facturas de prepago adicionales si, por ejemplo, es necesario añadir nuevos productos al pedido.</span><span class="sxs-lookup"><span data-stu-id="f4baf-115">You can also send additional prepayment invoices if, for example, additional items are added to the order.</span></span> <span data-ttu-id="f4baf-116">Puede aumentar las cantidades o añadir nuevas líneas a un pedido después de emitir un prepago y después puede registrar otra factura de prepago.</span><span class="sxs-lookup"><span data-stu-id="f4baf-116">You can increase quantities or add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice.</span></span> <span data-ttu-id="f4baf-117">Si desea eliminar una línea para la cual ya se ha facturado un prepago, deberá emitir un abono de prepago para poder eliminar la línea.</span><span class="sxs-lookup"><span data-stu-id="f4baf-117">If you want to delete a line for which a prepayment has already been invoiced, you must issue a prepayment credit memo before you can delete the line.</span></span>  

 <span data-ttu-id="f4baf-118">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="f4baf-118">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="f4baf-119">**Para**</span><span class="sxs-lookup"><span data-stu-id="f4baf-119">**To**</span></span>|<span data-ttu-id="f4baf-120">**Vea**</span><span class="sxs-lookup"><span data-stu-id="f4baf-120">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="f4baf-121">Configure grupos de registro de prepago y series numéricas y establezca porcentajes predeterminados de prepago para clientes, proveedores y productos.</span><span class="sxs-lookup"><span data-stu-id="f4baf-121">Set up prepayment posting groups and number series, and set up default prepayment percentages for customers, vendors, and items.</span></span>|[<span data-ttu-id="f4baf-122">Configurar prepagos</span><span class="sxs-lookup"><span data-stu-id="f4baf-122">Set Up Prepayments</span></span>](finance-set-up-prepayments.md)|
|<span data-ttu-id="f4baf-123">Crear un pedido, ajustar los importes de prepago y emitir una factura para los importes de prepago.</span><span class="sxs-lookup"><span data-stu-id="f4baf-123">Create an order, adjust the prepayment amounts, and issue an invoice for prepayment amounts.</span></span>|[<span data-ttu-id="f4baf-124">Crear facturas de prepagos</span><span class="sxs-lookup"><span data-stu-id="f4baf-124">Create Prepayment Invoices</span></span>](finance-how-to-create-prepayment-invoices.md)|  
|<span data-ttu-id="f4baf-125">Emitir una factura de prepago adicional, bien para productos adicionales o para un depósito adicional en el pedido original, o emitir un abono de prepago.</span><span class="sxs-lookup"><span data-stu-id="f4baf-125">Issue an additional prepayment invoice, either for additional items or for an additional deposit on the original order, or issue a prepayment credit memo.</span></span>|[<span data-ttu-id="f4baf-126">Corregir prepagos</span><span class="sxs-lookup"><span data-stu-id="f4baf-126">Correct Prepayments</span></span>](finance-how-to-correct-prepayments.md)|  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f4baf-127">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/prepayment-invoices-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="f4baf-127">See Related Training at [Microsoft Learn](/learn/modules/prepayment-invoices-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="f4baf-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4baf-128">See Also</span></span>

[<span data-ttu-id="f4baf-129">Tutorial: Configuración y facturación de prepagos de ventas</span><span class="sxs-lookup"><span data-stu-id="f4baf-129">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="f4baf-130">Finanzas</span><span class="sxs-lookup"><span data-stu-id="f4baf-130">Finance</span></span>](finance.md)  
<span data-ttu-id="f4baf-131">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f4baf-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]