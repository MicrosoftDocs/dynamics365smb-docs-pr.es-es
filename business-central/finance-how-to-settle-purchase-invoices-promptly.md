---
title: Liquidar facturas de compra inmediatamente
description: Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 60d3cf3c9e141c8df36eaca2c1975b696fdb105b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387254"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="8f1fe-103">Liquidar facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="8f1fe-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="8f1fe-104">Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="8f1fe-105">Si paga a menudo facturas de compra en efectivo, con cheque o por transferencia bancaria, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la este método en el campo **Forma de pago** de la tarjeta del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="8f1fe-106">Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="8f1fe-107">Para obtener más información, consulte [Definición de formas de pago](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8f1fe-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="8f1fe-108">Para liquidar facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="8f1fe-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="8f1fe-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f1fe-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="8f1fe-111">Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="8f1fe-112">Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="8f1fe-113">Para contabilizar el pago de una factura, debe comunicarse con un socio de Microsoft que pueda agregar los campos en el código.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="8f1fe-114">Esta personalización solo es necesaria si no especifica cuentas de contrapartida en los métodos de pago, como se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f1fe-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f1fe-115">See Also</span></span>

[<span data-ttu-id="8f1fe-116">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="8f1fe-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8f1fe-117">Compras</span><span class="sxs-lookup"><span data-stu-id="8f1fe-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8f1fe-118">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f1fe-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]