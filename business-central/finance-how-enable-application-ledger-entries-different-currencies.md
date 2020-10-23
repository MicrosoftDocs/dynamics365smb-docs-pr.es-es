---
title: Liquidar movimientos en distintas divisas | Documentos de Microsoft
description: Puede liquidar movimientos en varias divisas, por ejemplo, si vende a un cliente en una divisa y cobra en otra.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c11939306e56299347a5f80d9ccfbc35c22fe5aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917031"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="8186f-103">Permitir la liquidación de movimientos de cliente en distintas divisas</span><span class="sxs-lookup"><span data-stu-id="8186f-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="8186f-104">Si se realiza una compra a un proveedor en una divisa y se emite el pago en otra divisa, es posible liquidar la compra con el pago.</span><span class="sxs-lookup"><span data-stu-id="8186f-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="8186f-105">De igual modo, si vende a un cliente en una divisa y cobra en otra, puede liquidar el pago con la factura de venta.</span><span class="sxs-lookup"><span data-stu-id="8186f-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="8186f-106">El procedimiento siguiente describe cómo configurarlo para movimientos de proveedor en la página **Configuración de compras y pagos**.</span><span class="sxs-lookup"><span data-stu-id="8186f-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="8186f-107">La configuración es similar para los movimientos de cliente en la página **Configuración de ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="8186f-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="8186f-108">Para permitir la liquidación de movimientos de proveedor en divisas distintas</span><span class="sxs-lookup"><span data-stu-id="8186f-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="8186f-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de compras y pagos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8186f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="8186f-110">En el campo **Liquidación entre divisas**, seleccione una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="8186f-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="8186f-111">Opción</span><span class="sxs-lookup"><span data-stu-id="8186f-111">Option</span></span> | <span data-ttu-id="8186f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8186f-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8186f-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8186f-113">None</span></span> |<span data-ttu-id="8186f-114">No se permite la liquidación entre divisas.</span><span class="sxs-lookup"><span data-stu-id="8186f-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="8186f-115">UME</span><span class="sxs-lookup"><span data-stu-id="8186f-115">EMU</span></span> |<span data-ttu-id="8186f-116">Se permite la liquidación entre divisas de la UME.</span><span class="sxs-lookup"><span data-stu-id="8186f-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="8186f-117">Todo</span><span class="sxs-lookup"><span data-stu-id="8186f-117">All</span></span> |<span data-ttu-id="8186f-118">Se permite la liquidación entre todas las divisas.</span><span class="sxs-lookup"><span data-stu-id="8186f-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="8186f-119">Para configurar cuentas para liquidar diferencias de redondeo en divisa</span><span class="sxs-lookup"><span data-stu-id="8186f-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="8186f-120">Si liquida movimientos en varias divisas distintas, debe configurar las cuentas en las que se registrarán las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="8186f-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8186f-121">Primero debe configurar las cuentas contables antes de completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8186f-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="8186f-122">Para obtener más información, consulte [Descripción del libro mayor y plan de cuentas](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="8186f-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="8186f-123">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos contables clientes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8186f-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8186f-124">En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="8186f-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="8186f-125">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Grupos registro proveedor** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8186f-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="8186f-126">En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="8186f-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8186f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8186f-127">See Also</span></span>
[<span data-ttu-id="8186f-128">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="8186f-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8186f-129">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="8186f-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8186f-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8186f-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
