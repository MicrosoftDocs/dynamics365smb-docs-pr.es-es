---
title: Permitir los pagos de clientes mediante servicios de pago | Documentos de Microsoft
description: Facilite a los clientes el pago de las facturas activando los servicios de pago.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3bcfac75d1d161a4163fda466e320b0efd408655
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758272"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="df04a-103">Permitir los pagos de clientes mediante servicios de pago</span><span class="sxs-lookup"><span data-stu-id="df04a-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="df04a-104">Como alternativa a recopilar pagos a través de transferencia bancaria o tarjetas de crédito, los clientes pueden pagarle a través de su cuenta en servicios de pago, como Microsoft Pay, PayPal o WorldPay.</span><span class="sxs-lookup"><span data-stu-id="df04a-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="df04a-105">Al habilitar un servicio de pago en [!INCLUDE[prod_short](includes/prod_short.md)], hay disponible un vínculo al servicio en los documentos de venta que envíe por correo electrónico a los clientes.</span><span class="sxs-lookup"><span data-stu-id="df04a-105">After you enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="df04a-106">Los clientes pueden utilizar el vínculo para ir al servicio de pago y pagar la factura, directamente desde el documento de venta.</span><span class="sxs-lookup"><span data-stu-id="df04a-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="df04a-107">Si no desea incluir el vínculo, por ejemplo, si un cliente paga en efectivo, puede quitar el servicio de pago de la factura antes de registrarla.</span><span class="sxs-lookup"><span data-stu-id="df04a-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="df04a-108">Las extensiones Microsoft Pay, PayPal Payments Standard y WorldPay Payments Standard están instaladas en [!INCLUDE[prod_short](includes/prod_short.md)] y están preparadas para que las active.</span><span class="sxs-lookup"><span data-stu-id="df04a-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[prod_short](includes/prod_short.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-prod_short"></a><span data-ttu-id="df04a-109">Para activar un servicio de pago en [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="df04a-109">To enable a payment service in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>
1. <span data-ttu-id="df04a-110">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios de pagos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="df04a-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="df04a-111">En la página **Servicios de pago**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="df04a-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="df04a-112">Seleccione el servicio de pago y luego cierre la página.</span><span class="sxs-lookup"><span data-stu-id="df04a-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="df04a-113">En la página **Servicios de pago**, seleccione la acción **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="df04a-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="df04a-114">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="df04a-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="df04a-115">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="df04a-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="df04a-116">Para seleccionar un servicio de pago en una factura de ventas</span><span class="sxs-lookup"><span data-stu-id="df04a-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="df04a-117">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas venta** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="df04a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="df04a-118">Abra la factura de venta que desee pagar mediante el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="df04a-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="df04a-119">En el campo **Servicio de pago**, elija el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="df04a-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="df04a-120">El campo **Servicio de pago** solo está disponible si ha activado el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="df04a-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="df04a-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df04a-121">See Also</span></span>  
[<span data-ttu-id="df04a-122">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="df04a-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="df04a-123">Ccial</span><span class="sxs-lookup"><span data-stu-id="df04a-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="df04a-124">[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="df04a-124">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="df04a-125">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df04a-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
