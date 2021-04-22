---
title: Obtener información sobre contabilidad y plan de cuentas | Documentos de Microsoft
description: Describe la contabilidad, el plan de cuentas y las categorías de cuentas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f242bce26f55fe446ac8dc96335a8da835dd259c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774010"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="8006f-103">Descripción de contabilidad y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="8006f-103">Understanding the General Ledger and the COA</span></span>

<span data-ttu-id="8006f-104">La contabilidad almacena sus datos financieros y el plan de cuentas muestra las cuentas donde se registran todos los movimientos contables.</span><span class="sxs-lookup"><span data-stu-id="8006f-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="8006f-105">incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.</span><span class="sxs-lookup"><span data-stu-id="8006f-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="8006f-106">Configuración de contabilidad y grupos contables</span><span class="sxs-lookup"><span data-stu-id="8006f-106">General Ledger Setup and General Posting Setup</span></span>

<span data-ttu-id="8006f-107">La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos.</span><span class="sxs-lookup"><span data-stu-id="8006f-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="8006f-108">En la página **Configuración contabilidad** especifique cómo gestionar determinados asuntos de contabilidad en su empresa, como:</span><span class="sxs-lookup"><span data-stu-id="8006f-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="8006f-109">Detalles de redondeo de factura</span><span class="sxs-lookup"><span data-stu-id="8006f-109">Invoice rounding details</span></span>  
* <span data-ttu-id="8006f-110">Formatos de dirección</span><span class="sxs-lookup"><span data-stu-id="8006f-110">Address formats</span></span>  
* <span data-ttu-id="8006f-111">Informes financieros</span><span class="sxs-lookup"><span data-stu-id="8006f-111">Financial reporting</span></span>  

<span data-ttu-id="8006f-112">De manera similar, en la página **Configuración grupos contables**, puede especificar cómo desea configurar las combinaciones generales del negocio y los grupos contables de producto.</span><span class="sxs-lookup"><span data-stu-id="8006f-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="8006f-113">Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables.</span><span class="sxs-lookup"><span data-stu-id="8006f-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="8006f-114">Rellene una línea por cada combinación de grupo contable de negocio y de producto.</span><span class="sxs-lookup"><span data-stu-id="8006f-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="8006f-115">Para obtener más información, consulte [Configuraciones de grupos de registro](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8006f-115">For more information, see [Posting Group Setups](finance-posting-groups.md).</span></span>  

> [!TIP]
> <span data-ttu-id="8006f-116">La página **Configuración de contabilidad:** incluye campos genéricos y campos que son específicos de su país o región.</span><span class="sxs-lookup"><span data-stu-id="8006f-116">The **General Ledger Setup** page includes generic fields and fields that are particular to your country or region.</span></span> <span data-ttu-id="8006f-117">Si no está seguro del significado de un campo, le sugerimos que trabaje con su contable para determinar si es relevante para su organización.</span><span class="sxs-lookup"><span data-stu-id="8006f-117">If you are not sure of the meaning of a field, we suggest you work with your accountant to determine whether it is of relevance to your organization.</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="8006f-118">Plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="8006f-118">The Chart of Accounts</span></span>

<span data-ttu-id="8006f-119">El plan de cuentas muestra todas las cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="8006f-119">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="8006f-120">Desde el plan de cuentas, puede realizar acciones como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8006f-120">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="8006f-121">Ver informes que muestran movimientos de contabilidad y saldos.</span><span class="sxs-lookup"><span data-stu-id="8006f-121">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="8006f-122">Cerrar el asiento de regularización.</span><span class="sxs-lookup"><span data-stu-id="8006f-122">Close your income statement.</span></span>  
* <span data-ttu-id="8006f-123">Abrir la ficha de cuenta para agregar o cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="8006f-123">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="8006f-124">Ver una lista de grupos contables que registran en dicha cuenta.</span><span class="sxs-lookup"><span data-stu-id="8006f-124">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="8006f-125">Para ver los saldos del Debe y el Haber de una sola cuenta</span><span class="sxs-lookup"><span data-stu-id="8006f-125">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="8006f-126">Puede agregar, cambiar o eliminar cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="8006f-126">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="8006f-127">Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="8006f-127">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="8006f-128">Categorías de cuenta</span><span class="sxs-lookup"><span data-stu-id="8006f-128">Account Categories</span></span>

<span data-ttu-id="8006f-129">Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.</span><span class="sxs-lookup"><span data-stu-id="8006f-129">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="8006f-130">La página **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas que asignó a cada categoría.</span><span class="sxs-lookup"><span data-stu-id="8006f-130">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="8006f-131">Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.</span><span class="sxs-lookup"><span data-stu-id="8006f-131">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="8006f-132">Puede crear un grupo de categorías marcando otras subcategorías debajo de una línea en la página **Categorías de cuenta**.</span><span class="sxs-lookup"><span data-stu-id="8006f-132">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="8006f-133">Esto le facilita la obtención de una descripción general, porque cada agrupación muestra un balance total.</span><span class="sxs-lookup"><span data-stu-id="8006f-133">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="8006f-134">Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.</span><span class="sxs-lookup"><span data-stu-id="8006f-134">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="8006f-135">Puede especificar si las cuentas de cada categoría deben incluirse en los tipos específicos de informes.</span><span class="sxs-lookup"><span data-stu-id="8006f-135">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="8006f-136">Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.</span><span class="sxs-lookup"><span data-stu-id="8006f-136">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="8006f-137">Por ejemplo, el extracto de saldo predeterminado tiene una subcategoría para efectivo en Activos fijos.</span><span class="sxs-lookup"><span data-stu-id="8006f-137">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="8006f-138">Si desea que el extracto de saldo tenga en cuenta el efectivo pequeño y la cuenta corriente, puede:</span><span class="sxs-lookup"><span data-stu-id="8006f-138">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="8006f-139">Agregar dos nuevas subcategorías.</span><span class="sxs-lookup"><span data-stu-id="8006f-139">Add two new subcategories.</span></span> <span data-ttu-id="8006f-140">Una para el efectivo pequeño y otra para su cuenta corriente.</span><span class="sxs-lookup"><span data-stu-id="8006f-140">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="8006f-141">Especifique la definición de informe adicional **Cuentas de efectivo** de estas subcategorías.</span><span class="sxs-lookup"><span data-stu-id="8006f-141">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="8006f-142">Aplique sangría en la subcategoría **Efectivo**.</span><span class="sxs-lookup"><span data-stu-id="8006f-142">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="8006f-143">La próxima vez que genere los esquemas de cuentas, su extracto de saldo mostrará un extracto total de efectivo y dos líneas con extractos para efectivo pequeño y cuenta corriente.</span><span class="sxs-lookup"><span data-stu-id="8006f-143">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8006f-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8006f-144">See Also</span></span>

[<span data-ttu-id="8006f-145">Finanzas</span><span class="sxs-lookup"><span data-stu-id="8006f-145">Finance</span></span>](finance.md)  
[<span data-ttu-id="8006f-146">Configurar o cambiar el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="8006f-146">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="8006f-147">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="8006f-147">Business Intelligence</span></span>](bi.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]