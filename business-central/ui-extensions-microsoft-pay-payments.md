---
title: Microsoft Pay estándar | Microsoft Docs
description: Proporciona información acerca de la extensión Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 01/08/2020
ms.author: sgroespe
ms.openlocfilehash: 336aa735b703d7924914f4180ce46fd00ea23479
ms.sourcegitcommit: 70fe73040126960c813804d001b646f81cbf2f38
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943288"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="ce419-103">Extensión Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="ce419-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce419-104">A partir del 8 de febrero de 2020, los cambios en el servicio Microsoft Pay afectarán a la extensión Microsoft Pay en Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce419-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="ce419-105">Debido a los cambios, después del 8 de febrero, los vínculos de pago **Pagar ahora** que la extensión Microsoft Pay genera para las facturas en [!INCLUDE[d365fin](includes/d365fin_md.md)] no abrirán Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="ce419-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="ce419-106">Los clientes que usan la extensión deben cambiar la configuración de los Servicios de pago para comenzar a usar la extensión PayPal en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ce419-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="ce419-107">A partir del 8 de enero, mostraremos una notificación en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce419-107">From January 8, we will display a notification in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ce419-108">La notificación contendrá un vínculo a la configuración que necesita cambiar y a más información.</span><span class="sxs-lookup"><span data-stu-id="ce419-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="ce419-109">Después del 8 de febrero, la extensión Microsoft Pay ya no estará disponible en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce419-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span><br /></br>
>
> <span data-ttu-id="ce419-110">Las modificaciones afectan a las siguientes versiones de Business Central:</span><span class="sxs-lookup"><span data-stu-id="ce419-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="ce419-111">Microsoft Dynamics 365 Business Central de octubre de 2018</span><span class="sxs-lookup"><span data-stu-id="ce419-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="ce419-112">Microsoft Dynamics 365 Business Central de abril de 2019</span><span class="sxs-lookup"><span data-stu-id="ce419-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="ce419-113">Fase de lanzamiento 2 de Microsoft Dynamics 365 Business Central 2019</span><span class="sxs-lookup"><span data-stu-id="ce419-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="ce419-114">Los clientes requieren continuamente un servicio de atención mejor, ya sea en cuanto a la calidad de los productos como en las opciones de pago y envío.</span><span class="sxs-lookup"><span data-stu-id="ce419-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="ce419-115">El servicio Microsoft Pay ayuda a mejorar el servicio de atención al cliente.</span><span class="sxs-lookup"><span data-stu-id="ce419-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="ce419-116">La extensión de Microsoft Pay agrega un vínculo de Microsoft Pay a los documentos de venta para que los clientes pueden pagar fácilmente mediante Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="ce419-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="ce419-117">Después podrá registrar los documentos por correo electrónico para proporcionar un servicio al cliente superior y acortar el tiempo necesario para que los pagos de los clientes lleguen a su cuenta del banco.</span><span class="sxs-lookup"><span data-stu-id="ce419-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="ce419-118">La extensión de Microsoft Pay proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="ce419-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="ce419-119">Los pagos del cliente llegan más rápido a su cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="ce419-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="ce419-120">El cliente tiene más formas de pagar la factura.</span><span class="sxs-lookup"><span data-stu-id="ce419-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="ce419-121">Microsoft Pay ofrece un servicio de pago de confianza que los clientes prefieren para introducir la información de su tarjeta de crédito en sitios web desconocidos.</span><span class="sxs-lookup"><span data-stu-id="ce419-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="ce419-122">Microsoft Pay ofrece varias maneras de gestionar los pagos, incluido el procesamiento de tarjetas de crédito, como PayPal y Stripe.</span><span class="sxs-lookup"><span data-stu-id="ce419-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="ce419-123">El vínculo de Microsoft Pay se puede incrustar automáticamente en cada documento de la factura o por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ce419-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="ce419-124">Como esta funcionalidad está diseñada como extensión, tiene un control total para activarla cuando y si sus procesos empresariales lo requieren.</span><span class="sxs-lookup"><span data-stu-id="ce419-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="ce419-125">La activación de extensiones de servicio de pago es gratuita en [!INCLUDE[d365fin](includes/d365fin_md.md)], pero deberá ponerse en contacto con el servicio de pago para obtener una cuenta.</span><span class="sxs-lookup"><span data-stu-id="ce419-125">Enabling payment service extensions is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="ce419-126">Para obtener más información, consulte [Permitir pagos de cliente a través de servicios de pago](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ce419-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ce419-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ce419-127">See Also</span></span>
<span data-ttu-id="ce419-128">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ce419-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="ce419-129">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="ce419-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="ce419-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce419-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
