---
title: Liquidar movimientos en distintas divisas | Documentos de Microsoft
description: Puede liquidar movimientos en varias divisas, por ejemplo, si vende a un cliente en una divisa y cobra en otra.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="b8aa5-103">Procedimiento: Permitir la liquidación de movimientos de cliente en distintas divisas</span><span class="sxs-lookup"><span data-stu-id="b8aa5-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="b8aa5-104">Si se realiza una compra a un proveedor en una divisa y se emite el pago en otra divisa, es posible liquidar la compra con el pago.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="b8aa5-105">De igual modo, si vende a un cliente en una divisa y cobra en otra, puede liquidar el pago con la factura de venta.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="b8aa5-106">El procedimiento siguiente describe cómo configurarlo para movimientos de proveedor en la ventana **Configuración de compras y pagos**.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="b8aa5-107">La configuración es similar para los movimientos de cliente en la ventana **Configuración de ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b8aa5-108">Esta funcionalidad requiere que la experiencia esté definida en **Suite**.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="b8aa5-109">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="b8aa5-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="b8aa5-110">Para permitir la liquidación de movimientos de proveedor en divisas distintas</span><span class="sxs-lookup"><span data-stu-id="b8aa5-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="b8aa5-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de compras y pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="b8aa5-112">En el campo **Liquidación entre divisas**, seleccione una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="b8aa5-113">Opción</span><span class="sxs-lookup"><span data-stu-id="b8aa5-113">Option</span></span> | <span data-ttu-id="b8aa5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8aa5-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="b8aa5-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8aa5-115">None</span></span> |<span data-ttu-id="b8aa5-116">No se permite la liquidación entre divisas.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="b8aa5-117">UME</span><span class="sxs-lookup"><span data-stu-id="b8aa5-117">EMU</span></span> |<span data-ttu-id="b8aa5-118">Se permite la liquidación entre divisas de la UME.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="b8aa5-119">Todo</span><span class="sxs-lookup"><span data-stu-id="b8aa5-119">All</span></span> |<span data-ttu-id="b8aa5-120">Se permite la liquidación entre todas las divisas.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-120">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="b8aa5-121">Para configurar cuentas para liquidar diferencias de redondeo en divisa</span><span class="sxs-lookup"><span data-stu-id="b8aa5-121">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="b8aa5-122">Si liquida movimientos en varias divisas distintas, debe configurar las cuentas en las que se registrarán las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-122">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="b8aa5-123">Primero debe configurar las cuentas contables antes de completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-123">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="b8aa5-124">Para obtener más información, consulte [Descripción del libro mayor y plan de cuentas](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="b8aa5-124">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span> 
  
1. <span data-ttu-id="b8aa5-125">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contables clientes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b8aa5-126">En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="b8aa5-127">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de registro del proveedor** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="b8aa5-128">En los campos **Cta. neg. red. liquids. divisa** y **Cta. pos. red. liquids. divisa**, especifique el número de cuentas contables para registrar las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="b8aa5-128">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8aa5-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b8aa5-129">See Also</span></span>
[<span data-ttu-id="b8aa5-130">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="b8aa5-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="b8aa5-131">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="b8aa5-131">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="b8aa5-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8aa5-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

