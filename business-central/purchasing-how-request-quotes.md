---
title: Crear una oferta de compra para solicitar una oferta | Documentos de Microsoft
description: Describe cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cff54e778beb1bb08342835419998242eed4adf3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758472"
---
# <a name="request-quotes"></a><span data-ttu-id="0e034-103">Solicitar presupuestos</span><span class="sxs-lookup"><span data-stu-id="0e034-103">Request Quotes</span></span>
<span data-ttu-id="0e034-104">Las ofertas de compra pueden utilizarse como borradores de pedidos de compra, que luego se pueden convertir en facturas de compra o en pedidos.</span><span class="sxs-lookup"><span data-stu-id="0e034-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="0e034-105">Para crear una oferta de compra</span><span class="sxs-lookup"><span data-stu-id="0e034-105">To create a purchase quote</span></span>
1. <span data-ttu-id="0e034-106">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ofertas compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0e034-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0e034-107">Crear un documento nuevo, de la misma forma que hace un pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="0e034-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="0e034-108">Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0e034-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="0e034-109">Para convertir una oferta de compra en un pedido de compra</span><span class="sxs-lookup"><span data-stu-id="0e034-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="0e034-110">Cuando haya aceptado la oferta del proveedor, puede convertirla en una factura o una orden de compra para procesar la compra.</span><span class="sxs-lookup"><span data-stu-id="0e034-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="0e034-111">Abra una oferta de compra que esté lista para convertir, y haga clic en **Convertir en pedido**.</span><span class="sxs-lookup"><span data-stu-id="0e034-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="0e034-112">La oferta de compra se quita de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0e034-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="0e034-113">Se crea una factura o un pedido de compra a partir de la información en la oferta de compra en la que puede procesar la venta.</span><span class="sxs-lookup"><span data-stu-id="0e034-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="0e034-114">En el campo **Nº oferta** de la factura de compra se muestra o pedido de compra, el número de la oferta de compra a partir de la que se creó.</span><span class="sxs-lookup"><span data-stu-id="0e034-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e034-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0e034-115">See Also</span></span>
[<span data-ttu-id="0e034-116">Compras</span><span class="sxs-lookup"><span data-stu-id="0e034-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="0e034-117">Configurar compras</span><span class="sxs-lookup"><span data-stu-id="0e034-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="0e034-118">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="0e034-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="0e034-119">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0e034-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
