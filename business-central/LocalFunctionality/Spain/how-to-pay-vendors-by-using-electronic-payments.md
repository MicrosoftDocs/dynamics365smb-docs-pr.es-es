---
title: Pagar a los proveedores mediante pagos electrónicos
description: En Business Central, puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco. Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cb0ce17f180d2c4a9db44c8059127b27eadd6899
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753197"
---
# <a name="pay-vendors-using-electronic-payments"></a><span data-ttu-id="f93d8-105">Pagar a los proveedores mediante pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="f93d8-105">Pay Vendors Using Electronic Payments</span></span>
<span data-ttu-id="f93d8-106">En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede pagar a un proveedor mediante pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="f93d8-106">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can pay a vendor using electronic payments.</span></span> <span data-ttu-id="f93d8-107">Los pagos se exportarán a un archivo, que luego se transferirá al banco.</span><span class="sxs-lookup"><span data-stu-id="f93d8-107">Payments will be exported to a file, which will then be transmitted to your bank.</span></span> <span data-ttu-id="f93d8-108">Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).</span><span class="sxs-lookup"><span data-stu-id="f93d8-108">The bank then electronically transfers the payments from your bank account to the payee’s (vendor) bank account.</span></span>  

<span data-ttu-id="f93d8-109">Este proceso es parecido al de los cheques automáticos.</span><span class="sxs-lookup"><span data-stu-id="f93d8-109">This process is similar to how computer checks are processed.</span></span>  

## <a name="to-pay-a-vendor-electronically"></a><span data-ttu-id="f93d8-110">Para pagar a un proveedor electrónicamente</span><span class="sxs-lookup"><span data-stu-id="f93d8-110">To pay a vendor electronically</span></span>  

1. <span data-ttu-id="f93d8-111">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="f93d8-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f93d8-112">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f93d8-112">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f93d8-113">Campo</span><span class="sxs-lookup"><span data-stu-id="f93d8-113">Field</span></span>|<span data-ttu-id="f93d8-114">Description</span><span class="sxs-lookup"><span data-stu-id="f93d8-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f93d8-115">**Tipo pago por banco**</span><span class="sxs-lookup"><span data-stu-id="f93d8-115">**Bank Payment Type**</span></span>|<span data-ttu-id="f93d8-116">Especifique un **Pago electrónico** para crear un movimiento de cheque correspondiente a ese importe.</span><span class="sxs-lookup"><span data-stu-id="f93d8-116">Specify **Electronic Payment** to create a corresponding check ledger entry for the amount.</span></span>|  
    |<span data-ttu-id="f93d8-117">**Tipo pago**</span><span class="sxs-lookup"><span data-stu-id="f93d8-117">**Payment Type**</span></span>|<span data-ttu-id="f93d8-118">Especifique el tipo de pago para el pago de transferencia especial, si corresponde.</span><span class="sxs-lookup"><span data-stu-id="f93d8-118">Specify the payment type for the special transfer payment, if applicable.</span></span> <span data-ttu-id="f93d8-119">Seleccione **En blanco** si no desea usar el tipo de pago de transferencia especial.</span><span class="sxs-lookup"><span data-stu-id="f93d8-119">Select **Blank** if you do not want to use the special transfer payment type.</span></span> <span data-ttu-id="f93d8-120">Seleccione **01** para crear un pago especial para "artículos" en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f93d8-120">Select **01** to create a special payment for “goods” on the journal line.</span></span> <span data-ttu-id="f93d8-121">Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f93d8-121">Select **02** to create a special payment for “non-goods” on this journal line.</span></span>|  
    |<span data-ttu-id="f93d8-122">**Código estadístico**</span><span class="sxs-lookup"><span data-stu-id="f93d8-122">**Statistical Code**</span></span>|<span data-ttu-id="f93d8-123">Especifique el código estadístico para el pago de transferencia especial, si corresponde.</span><span class="sxs-lookup"><span data-stu-id="f93d8-123">Specify the statistical code for the special transfer payment, if applicable.</span></span> <span data-ttu-id="f93d8-124">El código estadístico se tiene que usar conjuntamente con el tipo de pago.</span><span class="sxs-lookup"><span data-stu-id="f93d8-124">The statistical code must be used at the same time as the payment type.</span></span> <span data-ttu-id="f93d8-125">Seleccione **01** para crear un pago especial para "artículos" en la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f93d8-125">Select **01** to create a special payment for “goods” on the journal line.</span></span> <span data-ttu-id="f93d8-126">Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.</span><span class="sxs-lookup"><span data-stu-id="f93d8-126">Select **02** to create a special payment for “non-goods” on this journal line.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="f93d8-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f93d8-127">See Also</span></span>  
[<span data-ttu-id="f93d8-128">Configurar cuentas bancarias para realizar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="f93d8-128">Set Up Bank Accounts for Electronic Payments</span></span>](how-to-set-up-bank-accounts-for-electronic-payments.md)
