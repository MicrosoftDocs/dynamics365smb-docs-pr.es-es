---
title: Asignar un nivel de prioridad a un proveedor | Documentos de Microsoft
description: "Puede asignar números a los proveedores para darles prioridad y facilitar las sugerencias de pago en Dynamics 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d19d0bce7290ce42b37dd1dfbea5213c6580e2da
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-prioritize-vendors"></a><span data-ttu-id="12fa5-103">Asignación de prioridad a proveedores</span><span class="sxs-lookup"><span data-stu-id="12fa5-103">How to: Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="12fa5-104"> puede proponer diversos pagos a proveedores, como los pagos que están próximos a vencer o los pagos en los que se pueden realizar descuentos.</span><span class="sxs-lookup"><span data-stu-id="12fa5-104"> can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="12fa5-105">Para obtener más información, vea [Procedimiento: Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="12fa5-105">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="12fa5-106">Primero, debe dar prioridad a los proveedores asignándoles números.</span><span class="sxs-lookup"><span data-stu-id="12fa5-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="12fa5-107">Para dar prioridad a proveedores</span><span class="sxs-lookup"><span data-stu-id="12fa5-107">To prioritize vendors</span></span>
1. <span data-ttu-id="12fa5-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="12fa5-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="12fa5-109">Seleccione el proveedor correspondiente y, a continuación, elija **Editar**.</span><span class="sxs-lookup"><span data-stu-id="12fa5-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="12fa5-110">En el campo **Prioridad**, escriba un número.</span><span class="sxs-lookup"><span data-stu-id="12fa5-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="12fa5-111"> considera que el número más bajo, excepto el 0, tiene la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="12fa5-111"> considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="12fa5-112">Por ejemplo, si utiliza 1, 2 y 3; 1 tendrá la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="12fa5-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="12fa5-113">Si no desea dar prioridad a un proveedor, deje el campo **Prioridad** en blanco.</span><span class="sxs-lookup"><span data-stu-id="12fa5-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="12fa5-114">Más adelante, si utiliza la característica de propuesta de pago, el proveedor se mostrará después de todos los proveedores que poseen un número de prioridad.</span><span class="sxs-lookup"><span data-stu-id="12fa5-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="12fa5-115">Puede introducir tantos niveles de prioridad como considere necesario.</span><span class="sxs-lookup"><span data-stu-id="12fa5-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="12fa5-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12fa5-116">See Also</span></span>
[<span data-ttu-id="12fa5-117">Configurar compras</span><span class="sxs-lookup"><span data-stu-id="12fa5-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="12fa5-118">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="12fa5-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="12fa5-119">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12fa5-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

