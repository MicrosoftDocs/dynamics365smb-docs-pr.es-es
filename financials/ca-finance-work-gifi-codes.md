---
title: "Códigos GIFI en Canadá | Documentos de Microsoft"
Description: "En Canadá, puede configurar códigos GIFI (índice general de información financiera) y asignarlos a cuentas contables"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="ea2d2-103">Procedimiento: Trabajar con los códigos GIFI en Canadá</span><span class="sxs-lookup"><span data-stu-id="ea2d2-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="ea2d2-104">La información fiscal puede incluir cuentas contables, informes, balances de ingresos, hojas de balance y extractos de remanentes.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="ea2d2-105">La información se fiscal clasifica mediante códigos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="ea2d2-106">El uso de los códigos ayuda al director a procesar la información, a prepararse para el registro electrónico y a validar la información de impuestos electrónicamente.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="ea2d2-107">El uso de los códigos ayuda también a las organizaciones estadísticas a trabajar más eficazmente puesto que la información financiera es más fácilmente accesible.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="ea2d2-108">Para obtener más información, vea [la página web de la Agencia de Ingresos de Canadá](http://www.cra-arc.gc.ca/)</span><span class="sxs-lookup"><span data-stu-id="ea2d2-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="ea2d2-109">La Agencia de Ingresos de Canadá usa el código del Índice General de Información Financiera (GIFI) para recopilar, validar y procesar la información financiera y de impuestos electrónicamente.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="ea2d2-110">Se recomienda asignar códigos del GIFI únicamente a las cuentas auxiliares, de forma que todo se realice mediante el software de preparación de impuestos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="ea2d2-111">Cuando una cuenta está asociada a un código GIFI se informa a la agencia de ingresos que está bajo ese código.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="ea2d2-112">Varias cuentas pueden tener el mismo código GIFI pero cada cuenta solo puede tener un código.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="ea2d2-113">Puede exportar la información del saldo con el código GIFI y guardar el archivo exportado en un Excel que será útil para transferir la información en el software de preparación de impuestos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="ea2d2-114">Para configurar códigos GIFI</span><span class="sxs-lookup"><span data-stu-id="ea2d2-114">To set up GIFI codes</span></span>
<span data-ttu-id="ea2d2-115">En Dynamics NAV deberá configurar los códigos GIFI para las cuentas contables, los informes, los balances de ingresos, las hojas de balance y los extractos de remanentes.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="ea2d2-116">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códigos GIFI** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea2d2-117">En la ventana **Códigos GIFI**, seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="ea2d2-118">Configurar los códigos GIFI rellenando los campos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="ea2d2-119">Para asignar códigos GIFI a cuentas</span><span class="sxs-lookup"><span data-stu-id="ea2d2-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="ea2d2-120">Para realizar un informe sobre la información financiera por código GIFI, cada uno de éstos debe estar asociado con la cuenta apropiada en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="ea2d2-121">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea2d2-122">Seleccione una cuenta contable relevante y, a continuación, seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="ea2d2-123">En la ficha desplegable **Contabilidad de costes**, en el campo **Código GIFI**, seleccione un código GIFI apropiado.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="ea2d2-124">Para ver los saldos de la cuenta usando el informe del código GIFI</span><span class="sxs-lookup"><span data-stu-id="ea2d2-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="ea2d2-125">Puede revisar los saldos de su cuenta con el código GIFI usando el informe **Saldos de cuenta con código GIFI**.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="ea2d2-126">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Saldos de cuenta con código GIFI** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea2d2-127">Especifique qué se debe incluir en el informe rellenando los campos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ea2d2-128">Haga clic en el botón **Imprimir** o **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="ea2d2-129">Para exportar información del saldo usando los códigos GIFI</span><span class="sxs-lookup"><span data-stu-id="ea2d2-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="ea2d2-130">Puede exportar la información del saldo usando los códigos GIFI y guardar el archivo exportado en Excel.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="ea2d2-131">Puede modificar, guardar o eliminar el archivo.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="ea2d2-132">Puede usar el archivo para transferir información sobre el software de preparación de impuestos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="ea2d2-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Exportar info. GIFI a Excel** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="ea2d2-134">Especifique que desea exportar a Excel rellenando los campos.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ea2d2-135">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ea2d2-136">El archivo de Excel tiene las características siguientes:</span><span class="sxs-lookup"><span data-stu-id="ea2d2-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="ea2d2-137">El saldo se redondea al porcentaje más próximo, pero el valor de celda mantiene el mismo como hace en la contabilidad general.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="ea2d2-138">Los números negativos se representan como número positivo entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="ea2d2-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="ea2d2-139">Por consiguiente, -123 se representa como (123).</span><span class="sxs-lookup"><span data-stu-id="ea2d2-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="ea2d2-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea2d2-140">See Also</span></span>
<span data-ttu-id="ea2d2-141">[Finanzas](finance.md) </span><span class="sxs-lookup"><span data-stu-id="ea2d2-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="ea2d2-142">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="ea2d2-142">Setting Up Finance</span></span>](finance-setup-finance.md)

