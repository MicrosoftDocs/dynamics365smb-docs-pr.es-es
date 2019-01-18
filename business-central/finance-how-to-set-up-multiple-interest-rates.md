---
title: "Configurar varios tipos de interés"
description: "Puede calcular cargos financieros con tasas de interés múltiples para un período específico. El cálculo de intereses es similar para todos los cargos financieros, con variación solo en la tasa de interés para un período específico."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 85e295997089ea10b956fe0a5d087652c190fb44
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="2d9fc-104">Configurar varios tipos de interés.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="2d9fc-105">Las tasas de interés múltiples se utilizan para diferentes períodos de pagos retrasados en las transacciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="2d9fc-106">Por ejemplo, un gobierno especifica el interés máximo que debe percibirse por un consumidor.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="2d9fc-107">Esta tipo de interés se puede modificar dos veces al año el 1 de enero y el 1 de julio.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="2d9fc-108">Las partes acuerdan la tasa de interés entre las empresas (B2B) y no existe un límite para ese grupo de clientes.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="2d9fc-109">La tasa anunciada es usualmente cuatro por ciento más que el interés bancario normal.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="2d9fc-110">Cuando cree los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="2d9fc-111">Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="2d9fc-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="2d9fc-112">Configurar varios tipos de interés</span><span class="sxs-lookup"><span data-stu-id="2d9fc-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="2d9fc-113">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Términos de interés** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2d9fc-114">En la página **Términos interés**, seleccione el término requerido de interés y después seleccione la acción **Tipos de interés**.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="2d9fc-115">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="2d9fc-116">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="2d9fc-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Términos recordatorio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="2d9fc-118">En la página **Términos recordatorio**, seleccione el término recordatorio requerido y después seleccione la acción **Niveles**.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="2d9fc-119">En la página **Niveles recordatorio**, seleccione el campo **Cálculo interés**.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="2d9fc-120">Cuando emite una nota de cargo financiero, la nota muestra los cargos financieros con tasas de interés múltiples para un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="2d9fc-121">La nota también contiene los detalles de contacto del cliente, la empresa que emite la nota, el importe adicional y el importe total.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="2d9fc-122">El movimiento inicial de la nota se muestra en negrita.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="2d9fc-123">Los cargos financieros se calculan con tasas de interés múltiples para un período de tiempo específico y se imprimen después del movimiento inicial de la nota.</span><span class="sxs-lookup"><span data-stu-id="2d9fc-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d9fc-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2d9fc-124">See Also</span></span>  
[<span data-ttu-id="2d9fc-125">Cobrar saldos pendientes</span><span class="sxs-lookup"><span data-stu-id="2d9fc-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="2d9fc-126">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="2d9fc-126">Setting Up Finance</span></span>](finance-setup-finance.md)

