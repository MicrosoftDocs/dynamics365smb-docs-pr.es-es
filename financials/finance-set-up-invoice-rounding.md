---
title: Configurar redondeo de facturas | Documentos de Microsoft
description: "Puede redondear los importes de las facturas en el momento en que éstas se crean. Además, las normativas o costumbres locales pueden requerir que el redondeo de las facturas se realice de un modo específico, por ejemplo, en una cantidad divisible por 0,05."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="d46b5-104">Configurar redondeo de factura</span><span class="sxs-lookup"><span data-stu-id="d46b5-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="d46b5-105">Si necesita redondear importes de facturas cuando se crean, puede utilizar la función de redondeo automático.</span><span class="sxs-lookup"><span data-stu-id="d46b5-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="d46b5-106">Cuando se redondea una factura, se añade una línea adicional en el importe redondeado y se registra con las demás líneas de la factura.</span><span class="sxs-lookup"><span data-stu-id="d46b5-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="d46b5-107">Las normativas o costumbres locales pueden requerir que el redondeo de las facturas se realice de un modo específico, por ejemplo, en una cantidad divisible por 0,05.</span><span class="sxs-lookup"><span data-stu-id="d46b5-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="d46b5-108">Para utilizar el redondeo de factura automático, debe:</span><span class="sxs-lookup"><span data-stu-id="d46b5-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="d46b5-109">Especificar las cuentas contables donde se van a registrar las diferencias de redondeo.</span><span class="sxs-lookup"><span data-stu-id="d46b5-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="d46b5-110">Configurar reglas de redondeo de la factura en la divisa local y en la divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="d46b5-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="d46b5-111">Activar la función.</span><span class="sxs-lookup"><span data-stu-id="d46b5-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="d46b5-112">Además de las funciones de redondeo de facturas, puede redondear los importes de las facturas mediante la función de redondeo de precio-producto y la función de redondeo de importe.</span><span class="sxs-lookup"><span data-stu-id="d46b5-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="d46b5-113">Configurar cuentas para diferencias de redondeo de facturas</span><span class="sxs-lookup"><span data-stu-id="d46b5-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="d46b5-114">Para utilizar la utilidad de redondeo de factura automático, debe configurar la cuenta o las cuentas en las que se registrarán las diferencias.</span><span class="sxs-lookup"><span data-stu-id="d46b5-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="d46b5-115">Antes de poder hacerlo, deberá configurar grupos de registro de IVA de producto.</span><span class="sxs-lookup"><span data-stu-id="d46b5-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="d46b5-116">Para obtener más información, consulte [Configurar IVA](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="d46b5-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="d46b5-117">Para configurar cuentas para diferencias de redondeo de facturas</span><span class="sxs-lookup"><span data-stu-id="d46b5-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="d46b5-118">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d46b5-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d46b5-119">En la página **Plan de cuentas**, configure la cuenta y denomínela **Redondeo factura** o algo parecido.</span><span class="sxs-lookup"><span data-stu-id="d46b5-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d46b5-120"> utilizará el nombre de la cuenta como texto en las facturas que se redondean.</span><span class="sxs-lookup"><span data-stu-id="d46b5-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="d46b5-121">Dependiendo de si utiliza el IVA o impuesto sobre las ventas, en los campos **Grupo registro impuesto prod.** o **Grupo reg. IVA producto**, seleccione un grupo de registro para los importes redondeados.</span><span class="sxs-lookup"><span data-stu-id="d46b5-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="d46b5-122">Puede que desee configurar un nuevo código de grupo para usarlo para el redondeo de factura.</span><span class="sxs-lookup"><span data-stu-id="d46b5-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="d46b5-123">Deje en blanco los campos **Tipo IVA** y **Grupo registro impuesto neg.** o **Grupo registro IVA neg**.</span><span class="sxs-lookup"><span data-stu-id="d46b5-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="d46b5-124">Ya puede asignar la cuenta de redondeo de factura a grupos de registro en la página **Grupo contable proveedor**.</span><span class="sxs-lookup"><span data-stu-id="d46b5-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="d46b5-125">Configurar redondeo para la divisa extranjera y local</span><span class="sxs-lookup"><span data-stu-id="d46b5-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="d46b5-126">Para poder utilizar la función de redondeo de factura automático, debe configurar reglas de redondeo para las divisas extranjera y local.</span><span class="sxs-lookup"><span data-stu-id="d46b5-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="d46b5-127">Configurar redondeo para la divisa extranjera</span><span class="sxs-lookup"><span data-stu-id="d46b5-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="d46b5-128">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Servicios de tipo de cambio de divisas"), escriba **Divisas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d46b5-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d46b5-129">En la página **Divisas**, seleccione la divisa extranjera para abrir **Ficha divisa**, y rellene los campos **Prec. redondeo importe**, **Prec. redondeo precio-prod.**, **Precisión redondeo factura** y **Tipo redondeo factura**.</span><span class="sxs-lookup"><span data-stu-id="d46b5-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="d46b5-130">Configurar redondeo para la divisa local</span><span class="sxs-lookup"><span data-stu-id="d46b5-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="d46b5-131">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración contabilidad** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d46b5-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d46b5-132">En la página **Configuración de contabilidad**, en la ficha desplegable **General**, rellene los campos **Precisión redondeo fact.** y **Tipo redondeo fact.**.</span><span class="sxs-lookup"><span data-stu-id="d46b5-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="d46b5-133">Activar la función de redondeo de factura</span><span class="sxs-lookup"><span data-stu-id="d46b5-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="d46b5-134">Para asegurarse de que se redondeen automáticamente las facturas de venta y compra, debe activar la función de redondeo de factura.</span><span class="sxs-lookup"><span data-stu-id="d46b5-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="d46b5-135">Active el redondeo de factura de forma independiente en las facturas de venta y en las de compra.</span><span class="sxs-lookup"><span data-stu-id="d46b5-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="d46b5-136">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración ventas y cobros** o **Configuración de compras y pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="d46b5-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d46b5-137">En la ficha desplegable **General**, elija la casilla de verificación **Redondeo de factura**.</span><span class="sxs-lookup"><span data-stu-id="d46b5-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d46b5-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d46b5-138">See Also</span></span>  
[<span data-ttu-id="d46b5-139">Facturar ventas</span><span class="sxs-lookup"><span data-stu-id="d46b5-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="d46b5-140">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="d46b5-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
