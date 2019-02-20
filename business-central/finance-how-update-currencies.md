---
title: Actualizar los tipos de cambio de divisa | Documentos de Microsoft
description: "Para utilizar varias divisas en su empresa, puede configurar un código para cada divisa y usar un servicio externo para el tipo de cambio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: es-es
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="793ac-103">Actualizar tipos cambio divisa</span><span class="sxs-lookup"><span data-stu-id="793ac-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="793ac-104">Las empresas trabajan cada vez en un mayor número de países o regiones, por lo que es muy importante que puedan comercializar y crear informes financieros en más de una divisa.</span><span class="sxs-lookup"><span data-stu-id="793ac-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="793ac-105">Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.</span><span class="sxs-lookup"><span data-stu-id="793ac-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="793ac-106">La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="793ac-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="793ac-107">Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[d365fin](includes/d365fin_md.md)] registrará automáticamente los importes tanto en la divisa local como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA.</span><span class="sxs-lookup"><span data-stu-id="793ac-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="793ac-108">Para obtener más información, vea [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="793ac-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="793ac-109">Ajustar los tipos de cambio</span><span class="sxs-lookup"><span data-stu-id="793ac-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="793ac-110">Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de la divisa adicional del sistema se deben ajustar regularmente.</span><span class="sxs-lookup"><span data-stu-id="793ac-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="793ac-111">Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos.</span><span class="sxs-lookup"><span data-stu-id="793ac-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="793ac-112">Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en el programa se tienen que actualizar una vez que se haya introducido esta información.</span><span class="sxs-lookup"><span data-stu-id="793ac-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="793ac-113">El proceso Ajustar tipos de cambio se usa para ajustar los tipos de cambio de los movimientos de clientes, proveedores y bancos.</span><span class="sxs-lookup"><span data-stu-id="793ac-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="793ac-114">También sirve para actualizar los importes en la divisa adicional de los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="793ac-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="793ac-115">Para configurar un servicio de tipo de cambio de divisa</span><span class="sxs-lookup"><span data-stu-id="793ac-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="793ac-116">Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates.</span><span class="sxs-lookup"><span data-stu-id="793ac-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="793ac-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Servicios de tipo de cambio de divisas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="793ac-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="793ac-118">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="793ac-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="793ac-119">En la página **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="793ac-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="793ac-120">Seleccione la casilla de verificación **Activado** para activar el servicio.</span><span class="sxs-lookup"><span data-stu-id="793ac-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="793ac-121">Para actualizar los tipos de cambio de divisa mediante un servicio</span><span class="sxs-lookup"><span data-stu-id="793ac-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="793ac-122">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Divisas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="793ac-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="793ac-123">Seleccione la acción **Actualizar tipos de cambio**.</span><span class="sxs-lookup"><span data-stu-id="793ac-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="793ac-124">El valor del campo **Tipo cambio** en la página **Divisas** se actualiza con el último tipo de cambio de divisa.</span><span class="sxs-lookup"><span data-stu-id="793ac-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="793ac-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="793ac-125">See Also</span></span>
[<span data-ttu-id="793ac-126">Configurar una divisa de informes adicional</span><span class="sxs-lookup"><span data-stu-id="793ac-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="793ac-127">Cerrar años y periodos</span><span class="sxs-lookup"><span data-stu-id="793ac-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="793ac-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="793ac-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

