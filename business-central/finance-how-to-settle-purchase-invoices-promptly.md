---
title: Liquidar facturas de compra inmediatamente
description: Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: fb442c7b1e9e7bdcb727ca6de157657e370e254f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746846"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="f333c-103">Liquidar facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="f333c-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="f333c-104">Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.</span><span class="sxs-lookup"><span data-stu-id="f333c-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="f333c-105">Si paga a menudo facturas de compra en efectivo, con cheque o por transferencia bancaria, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la este método en el campo **Forma de pago** de la tarjeta del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f333c-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="f333c-106">Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva.</span><span class="sxs-lookup"><span data-stu-id="f333c-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="f333c-107">Para obtener más información, consulte [Definición de formas de pago](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f333c-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="f333c-108">Para liquidar facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="f333c-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="f333c-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="f333c-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f333c-110">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="f333c-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="f333c-111">Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.</span><span class="sxs-lookup"><span data-stu-id="f333c-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="f333c-112">Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura.</span><span class="sxs-lookup"><span data-stu-id="f333c-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="f333c-113">Para contabilizar el pago de una factura, debe comunicarse con un socio de Microsoft que pueda agregar los campos en el código.</span><span class="sxs-lookup"><span data-stu-id="f333c-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="f333c-114">Esta personalización solo es necesaria si no especifica cuentas de contrapartida en los métodos de pago, como se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f333c-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="f333c-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f333c-115">See Also</span></span>

[<span data-ttu-id="f333c-116">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="f333c-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="f333c-117">Compras</span><span class="sxs-lookup"><span data-stu-id="f333c-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f333c-118">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f333c-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
