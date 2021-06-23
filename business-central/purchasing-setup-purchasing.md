---
title: Resumen de tareas para configurar las compras | Documentos de Microsoft
description: Describe las tareas para definir las directivas de aprovisionamiento de su empresa y configurar sus procesos de compra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9d0058c707862144592278d08a494175adf67a2a
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115441"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="efe21-103">Configurar compras</span><span class="sxs-lookup"><span data-stu-id="efe21-103">Setting Up Purchasing</span></span>
<span data-ttu-id="efe21-104">Para poder administrar procesos de compra, debe configurar las reglas y valores que definen las políticas de compra de la empresa.</span><span class="sxs-lookup"><span data-stu-id="efe21-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="efe21-105">Debe definir la configuración general, por ejemplo, qué documentos son necesarios y cómo se registran sus valores.</span><span class="sxs-lookup"><span data-stu-id="efe21-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="efe21-106">Esta configuración general se efectúa normalmente una vez durante la implementación inicial.</span><span class="sxs-lookup"><span data-stu-id="efe21-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="efe21-107">Una serie de tareas independientes relacionadas con el registro de nuevos proveedores es registrar acuerdos de precios especiales o descuentos que tenga con cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="efe21-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="efe21-108">La configuración de compra relacionada con las finanzas, como las formas de pago o las divisas, se describe en la sección Configuración de finanzas.</span><span class="sxs-lookup"><span data-stu-id="efe21-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="efe21-109">Para obtener más información, consulte [Configurar finanzas](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="efe21-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="efe21-110">Para</span><span class="sxs-lookup"><span data-stu-id="efe21-110">To</span></span> | <span data-ttu-id="efe21-111">Vea</span><span class="sxs-lookup"><span data-stu-id="efe21-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="efe21-112">Cree una ficha de proveedor para cada proveedor al que compre.</span><span class="sxs-lookup"><span data-stu-id="efe21-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="efe21-113">Permite registrar nuevos proveedores</span><span class="sxs-lookup"><span data-stu-id="efe21-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="efe21-114">Introduzca los diferentes descuentos y precios especiales que los proveedores le ofrecen en función del producto, la cantidad y/o la fecha.</span><span class="sxs-lookup"><span data-stu-id="efe21-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="efe21-115">Registrar acuerdos de pago, descuentos y precios de venta</span><span class="sxs-lookup"><span data-stu-id="efe21-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="efe21-116">De prioridad a los proveedores</span><span class="sxs-lookup"><span data-stu-id="efe21-116">Prioritize vendors</span></span> |[<span data-ttu-id="efe21-117">De prioridad a los proveedores</span><span class="sxs-lookup"><span data-stu-id="efe21-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="efe21-118">Configure los compradores</span><span class="sxs-lookup"><span data-stu-id="efe21-118">Set up purchasers</span></span> |[<span data-ttu-id="efe21-119">Configurar compradores</span><span class="sxs-lookup"><span data-stu-id="efe21-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="efe21-120">Especifique informes predeterminados que se utilizarán para diferentes tipos de documentos.</span><span class="sxs-lookup"><span data-stu-id="efe21-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="efe21-121">Selección de informes en Business Central</span><span class="sxs-lookup"><span data-stu-id="efe21-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="efe21-122">Según su ubicación geográfica, algunas páginas pueden contener campos que no se describen en los productos que se enumeran aquí, porque se aplican a funciones o personalizaciones locales.</span><span class="sxs-lookup"><span data-stu-id="efe21-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="external-document-number"></a><span data-ttu-id="efe21-123">Número de documento externo</span><span class="sxs-lookup"><span data-stu-id="efe21-123">External document number</span></span>

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="efe21-124">Consulte Formación relacionada en [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="efe21-124">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="efe21-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="efe21-125">See Also</span></span>

[<span data-ttu-id="efe21-126">Compras</span><span class="sxs-lookup"><span data-stu-id="efe21-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="efe21-127">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="efe21-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]