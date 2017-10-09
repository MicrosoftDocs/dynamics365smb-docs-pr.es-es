---
title: "Liquidación de facturas de compra inmediatamente | Documentos de Microsoft"
description: Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ab72dbc70405323e5dcf7aafb1120f63bd15246c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-settle-purchase-invoices-promptly"></a><span data-ttu-id="ff06f-103">Liquidación de facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="ff06f-103">How to: Settle Purchase Invoices Promptly</span></span>
<span data-ttu-id="ff06f-104">Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.</span><span class="sxs-lookup"><span data-stu-id="ff06f-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  
  
### <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="ff06f-105">Para liquidar facturas de compra inmediatamente</span><span class="sxs-lookup"><span data-stu-id="ff06f-105">To settle purchase invoices promptly</span></span>  
1. <span data-ttu-id="ff06f-106">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas compra** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ff06f-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ff06f-107">En la pestaña **Inicio**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ff06f-107">On the **Home** tab, choose **New**.</span></span>  
3.  <span data-ttu-id="ff06f-108">Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.</span><span class="sxs-lookup"><span data-stu-id="ff06f-108">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="ff06f-109">Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura.</span><span class="sxs-lookup"><span data-stu-id="ff06f-109">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="ff06f-110">Para registrar el pago de una factura, primero deberá insertarlos con las utilidades de diseño.</span><span class="sxs-lookup"><span data-stu-id="ff06f-110">In order to post the payment of an invoice, you must first insert them with the design facilities.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="ff06f-111">Si paga a menudo facturas de compra en efectivo, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la forma en el campo **Forma de pago** de la ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="ff06f-111">If you frequently pay purchase invoices in cash, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="ff06f-112">Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva.</span><span class="sxs-lookup"><span data-stu-id="ff06f-112">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff06f-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff06f-113">See Also</span></span>  
[<span data-ttu-id="ff06f-114">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="ff06f-114">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="ff06f-115">Compras</span><span class="sxs-lookup"><span data-stu-id="ff06f-115">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ff06f-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff06f-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
