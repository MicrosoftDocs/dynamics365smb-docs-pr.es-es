---
title: Actualizar los tipos de cambio de divisa | Documentos de Microsoft
description: "Para utilizar varias divisas en su empresa, puede configurar un código para cada divisa y usar un servicio externo para el tipo de cambio, como Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="31bd3-103">Actualizar los tipos de cambio de divisa</span><span class="sxs-lookup"><span data-stu-id="31bd3-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="31bd3-104">Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.</span><span class="sxs-lookup"><span data-stu-id="31bd3-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="31bd3-105">Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="31bd3-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="31bd3-106">Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="31bd3-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="31bd3-107">Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa.</span><span class="sxs-lookup"><span data-stu-id="31bd3-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="31bd3-108">El servicio de tipos de cambio de divisa de Yahoo está preinstalado y listo para activarse.</span><span class="sxs-lookup"><span data-stu-id="31bd3-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="31bd3-109">Para configurar un servicio de tipo de cambio de divisa</span><span class="sxs-lookup"><span data-stu-id="31bd3-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="31bd3-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Servicios de tipo de cambio de divisas** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="31bd3-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="31bd3-111">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="31bd3-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="31bd3-112">En la ventana **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="31bd3-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="31bd3-113">Seleccione la casilla de verificación **Activado** para activar el servicio.</span><span class="sxs-lookup"><span data-stu-id="31bd3-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="31bd3-114">Para actualizar los tipos de cambio de divisa mediante un servicio</span><span class="sxs-lookup"><span data-stu-id="31bd3-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="31bd3-115">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Servicios de tipo de cambio de divisas"), escriba **Divisas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="31bd3-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="31bd3-116">Seleccione la acción **Actualizar tipos de cambio**.</span><span class="sxs-lookup"><span data-stu-id="31bd3-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="31bd3-117">El valor del campo **Tipo cambio** en la ventana **Divisas** se actualiza con el último tipo de cambio de divisa.</span><span class="sxs-lookup"><span data-stu-id="31bd3-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="31bd3-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31bd3-118">See Also</span></span>
[<span data-ttu-id="31bd3-119">Cerrar años y periodos</span><span class="sxs-lookup"><span data-stu-id="31bd3-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="31bd3-120">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31bd3-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

