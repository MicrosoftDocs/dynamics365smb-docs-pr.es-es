---
title: Permitir los pagos de clientes mediante servicios de pago | Documentos de Microsoft
description: Facilite a los clientes el pago de las facturas activando los servicios de pago.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 49e75c5f43b495bfc053c58b27e06feace62971c
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a><span data-ttu-id="25ee3-103">Permitir los pagos de clientes mediante servicios de pago</span><span class="sxs-lookup"><span data-stu-id="25ee3-103">How to: Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="25ee3-104">Como alternativa a recopilar pagos a través de transferencia bancaria o tarjetas de crédito, los clientes pueden pagarle a través de su cuenta en servicios de pago, como PayPal o WorldPay.</span><span class="sxs-lookup"><span data-stu-id="25ee3-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as PayPal or WorldPay.</span></span>  

<span data-ttu-id="25ee3-105">Al habilitar un servicio de pago en [!INCLUDE[d365fin](includes/d365fin_md.md)], hay disponible un vínculo al servicio en los documentos de venta que envíe por correo electrónico a los clientes.</span><span class="sxs-lookup"><span data-stu-id="25ee3-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="25ee3-106">Los clientes pueden utilizar el vínculo para ir al servicio de pago y pagar la factura, directamente desde el documento de venta.</span><span class="sxs-lookup"><span data-stu-id="25ee3-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="25ee3-107">Si no desea incluir el vínculo, por ejemplo, si un cliente paga en efectivo, puede quitar el servicio de pago de la factura antes de registrarla.</span><span class="sxs-lookup"><span data-stu-id="25ee3-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="25ee3-108">Las extensiones Estándar de pagos de PayPal y Estándar de pagos de WorldPay están instalados en [!INCLUDE[d365fin](includes/d365fin_md.md)] y están preparados para que los active.</span><span class="sxs-lookup"><span data-stu-id="25ee3-108">The PayPal Payments Standard and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="25ee3-109">Para activar un servicio de pago en [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="25ee3-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="25ee3-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Servicios de pago** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="25ee3-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="25ee3-111">En la ventana **Servicios de pago**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="25ee3-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="25ee3-112">Seleccione el servicio de pago y luego cierre la ventana.</span><span class="sxs-lookup"><span data-stu-id="25ee3-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="25ee3-113">En la ventana **Servicios de pago**, seleccione la acción **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="25ee3-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="25ee3-114">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="25ee3-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="25ee3-115">Cierre la ventana.</span><span class="sxs-lookup"><span data-stu-id="25ee3-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="25ee3-116">Para seleccionar un servicio de pago en una factura de ventas</span><span class="sxs-lookup"><span data-stu-id="25ee3-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="25ee3-117">En la página Inicio, seleccione **Facturas de ventas**.</span><span class="sxs-lookup"><span data-stu-id="25ee3-117">On the Home page, choose **Sales Invoices**.</span></span>  
2. <span data-ttu-id="25ee3-118">Abra la factura de venta que desee pagar mediante el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="25ee3-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="25ee3-119">En el campo **Servicio de pago**, elija el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="25ee3-119">In the **Payment Service** field, choose the payment service.</span></span>  
  
    > [!NOTE]  
>   <span data-ttu-id="25ee3-120">El campo **Servicio de pago** solo está disponible si ha activado el servicio de pago.</span><span class="sxs-lookup"><span data-stu-id="25ee3-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25ee3-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="25ee3-121">See Also</span></span>  
[<span data-ttu-id="25ee3-122">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="25ee3-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="25ee3-123">Ventas</span><span class="sxs-lookup"><span data-stu-id="25ee3-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="25ee3-124">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="25ee3-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="25ee3-125">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="25ee3-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

