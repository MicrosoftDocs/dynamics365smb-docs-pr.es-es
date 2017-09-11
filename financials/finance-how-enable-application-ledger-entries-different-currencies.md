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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="7dafd-103">Procedimiento: Permitir la liquidación de movimientos de cliente en distintas divisas</span><span class="sxs-lookup"><span data-stu-id="7dafd-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="7dafd-104">Si se realiza una compra a un proveedor en una divisa y se emite el pago en otra divisa, es posible liquidar la compra con el pago.</span><span class="sxs-lookup"><span data-stu-id="7dafd-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="7dafd-105">De igual modo, si vende a un cliente en una divisa y cobra en otra, puede liquidar el pago con la factura de venta.</span><span class="sxs-lookup"><span data-stu-id="7dafd-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="7dafd-106">El procedimiento siguiente describe cómo configurarlo para movimientos de proveedor en la ventana **Configuración de compras y pagos**.</span><span class="sxs-lookup"><span data-stu-id="7dafd-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="7dafd-107">La configuración es similar para los movimientos de cliente en la ventana **Configuración de ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="7dafd-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7dafd-108">Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="7dafd-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="7dafd-109">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="7dafd-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="7dafd-110">Para permitir la liquidación de movimientos de proveedor en divisas distintas</span><span class="sxs-lookup"><span data-stu-id="7dafd-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="7dafd-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de compras y pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7dafd-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="7dafd-112">En el campo **Liquidación entre divisas**, seleccione una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="7dafd-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="7dafd-113">Opción</span><span class="sxs-lookup"><span data-stu-id="7dafd-113">Option</span></span> | <span data-ttu-id="7dafd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dafd-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="7dafd-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7dafd-115">None</span></span> |<span data-ttu-id="7dafd-116">No se permite la liquidación entre divisas.</span><span class="sxs-lookup"><span data-stu-id="7dafd-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="7dafd-117">UME</span><span class="sxs-lookup"><span data-stu-id="7dafd-117">EMU</span></span> |<span data-ttu-id="7dafd-118">Se permite la liquidación entre divisas de la UME.</span><span class="sxs-lookup"><span data-stu-id="7dafd-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="7dafd-119">Todo</span><span class="sxs-lookup"><span data-stu-id="7dafd-119">All</span></span> |<span data-ttu-id="7dafd-120">Se permite la liquidación entre todas las divisas.</span><span class="sxs-lookup"><span data-stu-id="7dafd-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7dafd-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7dafd-121">See Also</span></span>
[<span data-ttu-id="7dafd-122">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="7dafd-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="7dafd-123">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="7dafd-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="7dafd-124">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7dafd-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

