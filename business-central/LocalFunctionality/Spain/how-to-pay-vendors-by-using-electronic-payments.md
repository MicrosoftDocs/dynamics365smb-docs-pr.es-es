---
title: Pagar a los proveedores mediante pagos electrónicos
description: En Business Central, puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco. Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/26/2017
ms.author: sgroespe
ms.openlocfilehash: 5a7925c1faf09005d24e13224ee5f4eef446e96e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241709"
---
# <a name="pay-vendors-using-electronic-payments"></a><span data-ttu-id="debd3-105">Pagar a los proveedores mediante pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="debd3-105">Pay Vendors Using Electronic Payments</span></span>
<span data-ttu-id="debd3-106">En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede pagar a un proveedor mediante pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="debd3-106">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can pay a vendor using electronic payments.</span></span> <span data-ttu-id="debd3-107">Los pagos se exportarán a un archivo, que luego se transferirá al banco.</span><span class="sxs-lookup"><span data-stu-id="debd3-107">Payments will be exported to a file, which will then be transmitted to your bank.</span></span> <span data-ttu-id="debd3-108">Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).</span><span class="sxs-lookup"><span data-stu-id="debd3-108">The bank then electronically transfers the payments from your bank account to the payee’s (vendor) bank account.</span></span>  

<span data-ttu-id="debd3-109">Este proceso es parecido al de los cheques automáticos.</span><span class="sxs-lookup"><span data-stu-id="debd3-109">This process is similar to how computer checks are processed.</span></span>  

## <a name="to-pay-a-vendor-electronically"></a><span data-ttu-id="debd3-110">Para pagar a un proveedor electrónicamente</span><span class="sxs-lookup"><span data-stu-id="debd3-110">To pay a vendor electronically</span></span>  

1. <span data-ttu-id="debd3-111">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="debd3-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="debd3-112">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="debd3-112">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="debd3-113">Campo</span><span class="sxs-lookup"><span data-stu-id="debd3-113">Field</span></span>|<span data-ttu-id="debd3-114">Description</span><span class="sxs-lookup"><span data-stu-id="debd3-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="debd3-115">**Tipo pago por banco**</span><span class="sxs-lookup"><span data-stu-id="debd3-115">**Bank Payment Type**</span></span>|<span data-ttu-id="debd3-116">Especifique un **Pago electrónico** para crear un movimiento de cheque correspondiente a ese importe.</span><span class="sxs-lookup"><span data-stu-id="debd3-116">Specify **Electronic Payment** to create a corresponding check ledger entry for the amount.</span></span>|  
    |<span data-ttu-id="debd3-117">**Tipo pago**</span><span class="sxs-lookup"><span data-stu-id="debd3-117">**Payment Type**</span></span>|<span data-ttu-id="debd3-118">Especifique el tipo de pago para el pago de transferencia especial, si corresponde.</span><span class="sxs-lookup"><span data-stu-id="debd3-118">Specify the payment type for the special transfer payment, if applicable.</span></span> <span data-ttu-id="debd3-119">Seleccione **En blanco** si no desea usar el tipo de pago de transferencia especial.</span><span class="sxs-lookup"><span data-stu-id="debd3-119">Select **Blank** if you do not want to use the special transfer payment type.</span></span> <span data-ttu-id="debd3-120">Seleccione **01** para crear un pago especial para "artículos" en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="debd3-120">Select **01** to create a special payment for “goods” on the journal line.</span></span> <span data-ttu-id="debd3-121">Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.</span><span class="sxs-lookup"><span data-stu-id="debd3-121">Select **02** to create a special payment for “non-goods” on this journal line.</span></span>|  
    |<span data-ttu-id="debd3-122">**Código estadístico**</span><span class="sxs-lookup"><span data-stu-id="debd3-122">**Statistical Code**</span></span>|<span data-ttu-id="debd3-123">Especifique el código estadístico para el pago de transferencia especial, si corresponde.</span><span class="sxs-lookup"><span data-stu-id="debd3-123">Specify the statistical code for the special transfer payment, if applicable.</span></span> <span data-ttu-id="debd3-124">El código estadístico se tiene que usar conjuntamente con el tipo de pago.</span><span class="sxs-lookup"><span data-stu-id="debd3-124">The statistical code must be used at the same time as the payment type.</span></span> <span data-ttu-id="debd3-125">Seleccione **01** para crear un pago especial para "artículos" en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="debd3-125">Select **01** to create a special payment for “goods” on the journal line.</span></span> <span data-ttu-id="debd3-126">Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.</span><span class="sxs-lookup"><span data-stu-id="debd3-126">Select **02** to create a special payment for “non-goods” on this journal line.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="debd3-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="debd3-127">See Also</span></span>  
[<span data-ttu-id="debd3-128">Configurar cuentas bancarias para realizar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="debd3-128">Set Up Bank Accounts for Electronic Payments</span></span>](how-to-set-up-bank-accounts-for-electronic-payments.md)
