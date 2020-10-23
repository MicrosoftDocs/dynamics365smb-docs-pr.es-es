---
title: Configurar formas de pago | Documentos de Microsoft
description: Las formas de pago, por ejemplo, cheque, transferencia bancaria, efectivo o PayPal, se usan para definir cómo se pagarán las facturas de venta y de compra.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: cba54a66815874a3885e038283e8fe9a84b9dd09
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916855"
---
# <a name="defining-payment-methods"></a><span data-ttu-id="8761d-103">Definir las formas de pago</span><span class="sxs-lookup"><span data-stu-id="8761d-103">Defining Payment Methods</span></span>
<span data-ttu-id="8761d-104">Las formas de pago definen la forma en que prefiere que los clientes le paguen y cómo desea pagar a sus proveedores.</span><span class="sxs-lookup"><span data-stu-id="8761d-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="8761d-105">El método puede variar para cada cliente o proveedor.</span><span class="sxs-lookup"><span data-stu-id="8761d-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="8761d-106">Ejemplos de formas de pago habituales son **banco**, **efectivo**, **cheque** o **cuenta**.</span><span class="sxs-lookup"><span data-stu-id="8761d-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="8761d-107">Puede asignar una forma de pago a clientes y proveedores para que siempre se utilice la misma forma en los documentos de compras y ventas que cree para ellos.</span><span class="sxs-lookup"><span data-stu-id="8761d-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="8761d-108">Si es necesario, puede cambiar la forma en el documento de venta o de compra.</span><span class="sxs-lookup"><span data-stu-id="8761d-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="8761d-109">Por ejemplo, si desea pagar una determinada factura de compra en efectivo en lugar de hacerlo en cheque.</span><span class="sxs-lookup"><span data-stu-id="8761d-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="8761d-110">Esto no cambia la forma de pago predeterminada asignada al proveedor.</span><span class="sxs-lookup"><span data-stu-id="8761d-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="8761d-111">Se usan mismas formas de pago para documentos de venta y compra.</span><span class="sxs-lookup"><span data-stu-id="8761d-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="8761d-112">Por ejemplo, se utiliza una forma de pago en _efectivo_ cuando crea pagos y cuando los recibe.</span><span class="sxs-lookup"><span data-stu-id="8761d-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8761d-113">sabe que cuando está creando una factura de ventas espera recibir el pago y lo contrario para las facturas de compra.</span><span class="sxs-lookup"><span data-stu-id="8761d-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="8761d-114">Sin embargo, los abonos para devoluciones son excepciones porque el dinero fluye en direcciones opuestas, de usted a su cliente y de su proveedor a usted.</span><span class="sxs-lookup"><span data-stu-id="8761d-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="8761d-115">Por lo tanto, no se asigna una forma de pago predeterminada a los abonos.</span><span class="sxs-lookup"><span data-stu-id="8761d-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="8761d-116">Sin embargo, existe una solución alternativa si se ha especificado condiciones de pago para el cliente o el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8761d-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="8761d-117">Aunque el campo **Calc. dto. P.P. en abonos** no se ha diseñado para este fin, si marca la casilla de la página **Condiciones de pago**, se añadirá una forma de pago predeterminada al crear un abono.</span><span class="sxs-lookup"><span data-stu-id="8761d-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="8761d-118">Para configurar una forma de pago</span><span class="sxs-lookup"><span data-stu-id="8761d-118">To set up a payment method</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8761d-119">proporciona algunas formas de pago que las empresas utilizan con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="8761d-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="8761d-120">Sin embargo, puede agregar tantas como necesite.</span><span class="sxs-lookup"><span data-stu-id="8761d-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="8761d-121">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Formas de pago** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8761d-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="8761d-122">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8761d-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="8761d-123">Para asignar una forma de pago a un cliente o proveedor</span><span class="sxs-lookup"><span data-stu-id="8761d-123">To assign a payment method to a customer or vendor</span></span>
1. <span data-ttu-id="8761d-124">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Cliente** o **Proveedor** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8761d-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="8761d-125">En el campo **Cód. forma pago**, seleccione la forma que se usará de forma predeterminada para el cliente o proveedor.</span><span class="sxs-lookup"><span data-stu-id="8761d-125">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="8761d-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8761d-126">See Also</span></span>
[<span data-ttu-id="8761d-127">Permite registrar nuevos clientes</span><span class="sxs-lookup"><span data-stu-id="8761d-127">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="8761d-128">Finanzas</span><span class="sxs-lookup"><span data-stu-id="8761d-128">Finance</span></span>](finance.md)  
<span data-ttu-id="8761d-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8761d-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
