---
title: Cree informes financieros con esquemas de cuentas
description: "Describe cómo utilizar los esquemas de cuentas para crear varias vistas e informes para analizar los datos de rendimiento financiero."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="62f4b-103">Preparar informes financieros con esquemas de cuentas y categorías de cuentas</span><span class="sxs-lookup"><span data-stu-id="62f4b-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="62f4b-104">Use esquemas de cuentas para obtener información sobre los datos financieros almacenados en su plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="62f4b-105">Los esquemas de cuentas analizan cifras en cuentas de contabilidad y comparan los movimientos de contabilidad con los presupuestados.</span><span class="sxs-lookup"><span data-stu-id="62f4b-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="62f4b-106">Los resultados se muestran en gráficos en su área de trabajo, como el gráfico de flujo de efectivo, y en informes, como los informes Balance de ingresos y Balance.</span><span class="sxs-lookup"><span data-stu-id="62f4b-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="62f4b-107">Se obtiene acceso a estos dos informes, por ejemplo, con la acción **Estados financieros** en las áreas de trabajo de Business Manager y Contable.</span><span class="sxs-lookup"><span data-stu-id="62f4b-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="62f4b-108">proporciona algunos esquemas de cuentas de ejemplo que puede utilizar inmediatamente o puede configurar sus propias filas y columnas para especificar las cifras que se compararán.</span><span class="sxs-lookup"><span data-stu-id="62f4b-108">provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="62f4b-109">Por ejemplo, puede crear esquemas de cuentas para calcular márgenes de beneficios en dimensiones como departamentos o grupos de clientes.</span><span class="sxs-lookup"><span data-stu-id="62f4b-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="62f4b-110">Puede crear tantos resultados financieros personalizados como desee.</span><span class="sxs-lookup"><span data-stu-id="62f4b-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="62f4b-111">Configurar esquemas de cuentas requiere obtener una comprensión de los datos financieros del plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="62f4b-112">Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="62f4b-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="62f4b-113">Para ello es necesario que se creen presupuestos.</span><span class="sxs-lookup"><span data-stu-id="62f4b-113">This requires that budgets are created.</span></span> <span data-ttu-id="62f4b-114">Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="62f4b-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="62f4b-115">Categorías de cuentas y esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="62f4b-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="62f4b-116">Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros.</span><span class="sxs-lookup"><span data-stu-id="62f4b-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="62f4b-117">Después de configurar las categorías de cuentas en la ventana **Categorías de cuenta** y haya elegido la acción **Generar esquemas de cuentas**, se actualizan los esquemas de cuentas subyacentes para los informes financieros principales.</span><span class="sxs-lookup"><span data-stu-id="62f4b-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="62f4b-118">La próxima vez que ejecute uno de estos informes, como el informe Extracto del saldo, se agregan los nuevos totales y subtotales en función de los cambios que haya realizado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="62f4b-119">Para obtener más información, consulte la sesión "Categorías de cuentas" en [Descripción del libro mayor y plan de cuentas](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="62f4b-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="62f4b-120">Para crear nuevos esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="62f4b-120">To create new account schedules</span></span>  
 <span data-ttu-id="62f4b-121">Usar esquemas de cuentas para analizar cifras en cuentas de contabilidad o comparar los movimientos de contabilidad con los presupuestados.</span><span class="sxs-lookup"><span data-stu-id="62f4b-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="62f4b-122">Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="62f4b-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="62f4b-123">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="62f4b-124">En la ventana **Nombre esquema cuenta**, elija la acción **Nuevo** para crear un nuevo nombre de esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="62f4b-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="62f4b-125">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="62f4b-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="62f4b-126">Elija la acción **Editar esquema cuentas**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="62f4b-127">En la ventana **Esquema cuentas** rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="62f4b-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="62f4b-128">Cuando haya creado un nuevo esquema de cuentas y haya configurado las filas, debe configurar las columnas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="62f4b-129">Puede configurarlas manualmente o bien puede asignar una plantilla de columna predefinida al esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="62f4b-130">Elija la acción **Editar configuración de disposición de columna**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="62f4b-131">En la ventana **Plantilla columna** rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="62f4b-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="62f4b-132">Si no ha asignado una plantilla de columna genérica al esquema de cuentas, debe configurar las columnas manualmente.</span><span class="sxs-lookup"><span data-stu-id="62f4b-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="62f4b-133">Para copiar un esquema de cuentas existente</span><span class="sxs-lookup"><span data-stu-id="62f4b-133">To copy an existing account schedule</span></span>
<span data-ttu-id="62f4b-134">Los esquemas de cuentas en la versión estándar de [!INCLUDE[d365fin](includes/d365fin_md.md)] son la base de los informes financieros estándar, que pueden no adaptarse a las necesidades de su empresa.</span><span class="sxs-lookup"><span data-stu-id="62f4b-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="62f4b-135">Para crear rápidamente sus propios informes financieros, puede empezar por copiar un esquema de cuentas existente.</span><span class="sxs-lookup"><span data-stu-id="62f4b-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="62f4b-136">En la ventana **Esquemas de cuentas**, seleccione un esquema de cuentas correspondiente y después seleccione **Copiar esquema de cuentas**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="62f4b-137">En la ventana **Copiar esquema de cuentas**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="62f4b-138">Para crear una columna que calcule porcentajes</span><span class="sxs-lookup"><span data-stu-id="62f4b-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="62f4b-139">En ocasiones, podría desear incluir una columna en un esquema de cuentas para calcular los porcentajes de un total.</span><span class="sxs-lookup"><span data-stu-id="62f4b-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="62f4b-140">Por ejemplo, si tiene una serie de filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales que representa cada fila.</span><span class="sxs-lookup"><span data-stu-id="62f4b-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="62f4b-141">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="62f4b-142">En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="62f4b-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="62f4b-143">Elija la acción **Editar esquema cuentas** para configurar una fila del esquema de cuentas para calcular el total en el que se basarán los porcentajes.</span><span class="sxs-lookup"><span data-stu-id="62f4b-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="62f4b-144">Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="62f4b-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="62f4b-145">Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="62f4b-146">En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará.</span><span class="sxs-lookup"><span data-stu-id="62f4b-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="62f4b-147">Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="62f4b-148">Elija la acción **Editar configuración de disposición de columna** para configurar una columna.</span><span class="sxs-lookup"><span data-stu-id="62f4b-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="62f4b-149">Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="62f4b-150">En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida de %.</span><span class="sxs-lookup"><span data-stu-id="62f4b-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="62f4b-151">Por ejemplo, si el número de columna N contiene los saldos periodos, escriba **N%**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="62f4b-152">Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="62f4b-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="62f4b-153">Para configurar esquemas de cuentas con resúmenes</span><span class="sxs-lookup"><span data-stu-id="62f4b-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="62f4b-154">Puede usar un esquema de cuentas para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="62f4b-155">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-155">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="62f4b-156">En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="62f4b-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="62f4b-157">Elija la acción **Editar esquema cuentas**</span><span class="sxs-lookup"><span data-stu-id="62f4b-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="62f4b-158">En la ventana **Esquema cuentas**, en el campo **Nombre**, seleccione el nombre del esquema de cuentas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="62f4b-159">Elija la acción **Insertar cuentas**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="62f4b-160">Seleccione la cuenta que desea incluir en la declaración y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="62f4b-161">Estas cuentas se insertan en el esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="62f4b-162">Si lo desea, puede modificar la plantilla de columna.</span><span class="sxs-lookup"><span data-stu-id="62f4b-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="62f4b-163">Seleccione la acción **Resumen**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="62f4b-164">Haga clic en la ficha desplegable **Filtros dimensión** y asigne al filtro de presupuesto el nombre que desee.</span><span class="sxs-lookup"><span data-stu-id="62f4b-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="62f4b-165">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="62f4b-166">Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="62f4b-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="62f4b-167">Comparación de períodos contables usando fórmulas de períodos</span><span class="sxs-lookup"><span data-stu-id="62f4b-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="62f4b-168">El esquema de cuentas puede comparar los resultados de diferentes períodos contables, como este mes en comparación con el mismo mes del año anterior.</span><span class="sxs-lookup"><span data-stu-id="62f4b-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="62f4b-169">Para hacerlo, agregue una columna con el campo **Fórmula de periodo comparativo** y luego establezca ese campo en una fórmula de período.</span><span class="sxs-lookup"><span data-stu-id="62f4b-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="62f4b-170">Un periodo contable no tiene que coincidir con el calendario, pero el año fiscal debe tener el mismo número de periodos contables, aunque cada periodo tenga una duración diferente.</span><span class="sxs-lookup"><span data-stu-id="62f4b-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="62f4b-171">utiliza la fórmula de periodo para calcular el importe a partir del periodo comparativo en relación con el periodo representado por el filtro de fecha de la solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="62f4b-171">uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="62f4b-172">El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha.</span><span class="sxs-lookup"><span data-stu-id="62f4b-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="62f4b-173">Las abreviaturas de las especificaciones del periodo son:</span><span class="sxs-lookup"><span data-stu-id="62f4b-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62f4b-174">Siglas</span><span class="sxs-lookup"><span data-stu-id="62f4b-174">Abbreviation</span></span></th>
<th><span data-ttu-id="62f4b-175">Description</span><span class="sxs-lookup"><span data-stu-id="62f4b-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-176">P</span><span class="sxs-lookup"><span data-stu-id="62f4b-176">P</span></span></p></td>
<td><p><span data-ttu-id="62f4b-177">Periodo</span><span class="sxs-lookup"><span data-stu-id="62f4b-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62f4b-178">LP</span><span class="sxs-lookup"><span data-stu-id="62f4b-178">LP</span></span></p></td>
<td><p><span data-ttu-id="62f4b-179">Último periodo de un año fiscal, medio año o trimestre.</span><span class="sxs-lookup"><span data-stu-id="62f4b-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-180">CP</span><span class="sxs-lookup"><span data-stu-id="62f4b-180">CP</span></span></p></td>
<td><p><span data-ttu-id="62f4b-181">Periodo actual de un año fiscal, medio año o trimestre.</span><span class="sxs-lookup"><span data-stu-id="62f4b-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62f4b-182">FY</span><span class="sxs-lookup"><span data-stu-id="62f4b-182">FY</span></span></p></td>
<td><p><span data-ttu-id="62f4b-183">Año fiscal.</span><span class="sxs-lookup"><span data-stu-id="62f4b-183">Fiscal year.</span></span> <span data-ttu-id="62f4b-184">Por ejemplo, AF[1..3] indica el primer trimestre del año fiscal actual</span><span class="sxs-lookup"><span data-stu-id="62f4b-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62f4b-185">Ejemplos de fórmulas:</span><span class="sxs-lookup"><span data-stu-id="62f4b-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62f4b-186">Fórmula</span><span class="sxs-lookup"><span data-stu-id="62f4b-186">Formula</span></span></th>
<th><span data-ttu-id="62f4b-187">Description</span><span class="sxs-lookup"><span data-stu-id="62f4b-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-188">&lt;En blanco&gt;</span><span class="sxs-lookup"><span data-stu-id="62f4b-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="62f4b-189">Periodo actual</span><span class="sxs-lookup"><span data-stu-id="62f4b-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62f4b-190">-1P</span><span class="sxs-lookup"><span data-stu-id="62f4b-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="62f4b-191">Periodo anterior</span><span class="sxs-lookup"><span data-stu-id="62f4b-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-192">-1AF[1..UP]</span><span class="sxs-lookup"><span data-stu-id="62f4b-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="62f4b-193">Todo el año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="62f4b-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62f4b-194">-1AF</span><span class="sxs-lookup"><span data-stu-id="62f4b-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="62f4b-195">Periodo actual del año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="62f4b-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-196">-1AF[1..3]</span><span class="sxs-lookup"><span data-stu-id="62f4b-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="62f4b-197">Primer trimestre del año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="62f4b-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62f4b-198">-1AF[1..PA]</span><span class="sxs-lookup"><span data-stu-id="62f4b-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="62f4b-199">Desde el principio de año fiscal anterior hasta el periodo actual en el año fiscal anterior, ambos inclusive</span><span class="sxs-lookup"><span data-stu-id="62f4b-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62f4b-200">-1AF[PA..UP]</span><span class="sxs-lookup"><span data-stu-id="62f4b-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="62f4b-201">Desde el periodo actual del año fiscal anterior hasta el último periodo del año fiscal anterior, ambos inclusive</span><span class="sxs-lookup"><span data-stu-id="62f4b-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62f4b-202">Si desea calcular el importe del periodo de comparación para periodos de tiempo regulares, deberá introducir una fórmula en el campo **Fórmula fecha comparación**.</span><span class="sxs-lookup"><span data-stu-id="62f4b-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="62f4b-203">No siempre es transparente qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables que se reflejan en los datos del plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="62f4b-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="62f4b-204">Por ejemplo, cree un esquema de cuentas en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Filtro de período de fecha de comparación** en *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="62f4b-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="62f4b-205">Luego, ejecute el informe el 28 de febrero y configure el filtro de fecha en enero y febrero.</span><span class="sxs-lookup"><span data-stu-id="62f4b-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="62f4b-206">Como resultado, el calendario de cuentas compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.</span><span class="sxs-lookup"><span data-stu-id="62f4b-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="62f4b-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62f4b-207">See Also</span></span>
[<span data-ttu-id="62f4b-208">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="62f4b-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="62f4b-209">Finanzas</span><span class="sxs-lookup"><span data-stu-id="62f4b-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="62f4b-210">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="62f4b-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="62f4b-211">Libro mayor y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="62f4b-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="62f4b-212">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="62f4b-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

