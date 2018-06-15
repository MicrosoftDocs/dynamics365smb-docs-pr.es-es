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
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: es-es
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="a848c-103">Trabajar con esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="a848c-103">Work with Account Schedules</span></span>
<span data-ttu-id="a848c-104">Use esquemas de cuentas para obtener información sobre los datos financieros almacenados en su plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="a848c-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="a848c-105">Los esquemas de cuentas analizan cifras en cuentas de contabilidad y comparan los movimientos de contabilidad con los presupuestados.</span><span class="sxs-lookup"><span data-stu-id="a848c-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="a848c-106">Los resultados se muestran en gráficos en el área de trabajo, como el gráfico Flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="a848c-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a848c-107"> proporciona algunos esquemas de cuentas de ejemplo que puede utilizar inmediatamente o puede configurar sus propias filas y columnas para especificar las cifras que se compararán.</span><span class="sxs-lookup"><span data-stu-id="a848c-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="a848c-108">Por ejemplo, puede crear esquemas de cuentas para calcular márgenes de beneficios en dimensiones como departamentos o grupos de clientes.</span><span class="sxs-lookup"><span data-stu-id="a848c-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="a848c-109">Puede crear tantos resultados financieros personalizados como desee.</span><span class="sxs-lookup"><span data-stu-id="a848c-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="a848c-110">Configurar esquemas de cuentas requiere obtener una comprensión de los datos financieros del plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="a848c-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="a848c-111">Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="a848c-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="a848c-112">Para ello es necesario que se creen presupuestos.</span><span class="sxs-lookup"><span data-stu-id="a848c-112">This requires that budgets are created.</span></span> <span data-ttu-id="a848c-113">Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="a848c-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="a848c-114">Categorías de cuentas y esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="a848c-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="a848c-115">Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros.</span><span class="sxs-lookup"><span data-stu-id="a848c-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="a848c-116">Después de configurar las categorías de cuentas en la ventana **Categorías de cuenta** y haya elegido la acción **Generar esquemas de cuentas**, se actualizan los esquemas de cuentas subyacentes para los informes financieros principales.</span><span class="sxs-lookup"><span data-stu-id="a848c-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="a848c-117">La próxima vez que ejecute uno de estos informes, como el extracto del saldo, se agregan los nuevos totales y subtotales en función de los cambios que haya realizado.</span><span class="sxs-lookup"><span data-stu-id="a848c-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="a848c-118">Para obtener más información, consulte [Libro mayor y plan de cuentas](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="a848c-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="a848c-119">Para crear nuevos esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="a848c-119">To create new account schedules</span></span>  
 <span data-ttu-id="a848c-120">Usar esquemas de cuentas para analizar cifras en cuentas de contabilidad o comparar los movimientos de contabilidad con los presupuestados.</span><span class="sxs-lookup"><span data-stu-id="a848c-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="a848c-121">Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="a848c-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="a848c-122">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a848c-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a848c-123">En la ventana **Nombre esquema cuenta**, elija la acción **Nuevo** para crear un nuevo nombre de esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="a848c-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="a848c-124">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a848c-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="a848c-125">Elija la acción **Editar esquema cuentas**.</span><span class="sxs-lookup"><span data-stu-id="a848c-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="a848c-126">En la ventana **Esquema cuentas** rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a848c-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="a848c-127">Cuando haya creado un nuevo esquema de cuentas y haya configurado las filas, debe configurar las columnas.</span><span class="sxs-lookup"><span data-stu-id="a848c-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="a848c-128">Puede configurarlas manualmente o bien puede asignar una plantilla de columna predefinida al esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="a848c-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="a848c-129">Elija la acción **Editar configuración de disposición de columna**.</span><span class="sxs-lookup"><span data-stu-id="a848c-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="a848c-130">En la ventana **Plantilla columna** rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a848c-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a848c-131">Si no ha asignado una plantilla de columna genérica al esquema de cuentas, debe configurar las columnas manualmente.</span><span class="sxs-lookup"><span data-stu-id="a848c-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="a848c-132">Para crear una columna que calcule porcentajes</span><span class="sxs-lookup"><span data-stu-id="a848c-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="a848c-133">En ocasiones, podría desear incluir una columna en un esquema de cuentas para calcular los porcentajes de un total.</span><span class="sxs-lookup"><span data-stu-id="a848c-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="a848c-134">Por ejemplo, si tiene una serie de filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales que representa cada fila.</span><span class="sxs-lookup"><span data-stu-id="a848c-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="a848c-135">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a848c-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="a848c-136">En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="a848c-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="a848c-137">Elija la acción **Editar esquema cuentas** para configurar una fila del esquema de cuentas para calcular el total en el que se basarán los porcentajes.</span><span class="sxs-lookup"><span data-stu-id="a848c-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="a848c-138">Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="a848c-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="a848c-139">Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**.</span><span class="sxs-lookup"><span data-stu-id="a848c-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="a848c-140">En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará.</span><span class="sxs-lookup"><span data-stu-id="a848c-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="a848c-141">Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.</span><span class="sxs-lookup"><span data-stu-id="a848c-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="a848c-142">Elija la acción **Editar configuración de disposición de columna** para configurar una columna.</span><span class="sxs-lookup"><span data-stu-id="a848c-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="a848c-143">Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="a848c-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="a848c-144">En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida de %.</span><span class="sxs-lookup"><span data-stu-id="a848c-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="a848c-145">Por ejemplo, si el número de columna N contiene los saldos periodos, escriba **N%**.</span><span class="sxs-lookup"><span data-stu-id="a848c-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="a848c-146">Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.</span><span class="sxs-lookup"><span data-stu-id="a848c-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="a848c-147">Para configurar esquemas de cuentas con resúmenes</span><span class="sxs-lookup"><span data-stu-id="a848c-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="a848c-148">Puede usar un esquema de cuentas para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.</span><span class="sxs-lookup"><span data-stu-id="a848c-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="a848c-149">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a848c-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="a848c-150">En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="a848c-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="a848c-151">Elija la acción **Editar esquema cuentas**</span><span class="sxs-lookup"><span data-stu-id="a848c-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="a848c-152">En la ventana **Esquema cuentas**, en el campo **Nombre**, seleccione el nombre del esquema de cuentas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a848c-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="a848c-153">Elija la acción **Insertar cuentas**.</span><span class="sxs-lookup"><span data-stu-id="a848c-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="a848c-154">Seleccione la cuenta que desea incluir en la declaración y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a848c-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="a848c-155">Estas cuentas se insertan en el esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="a848c-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="a848c-156">Si lo desea, puede modificar la plantilla de columna.</span><span class="sxs-lookup"><span data-stu-id="a848c-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="a848c-157">Seleccione la acción **Resumen**.</span><span class="sxs-lookup"><span data-stu-id="a848c-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="a848c-158">Haga clic en la ficha desplegable **Filtros dimensión** y asigne al filtro de presupuesto el nombre que desee.</span><span class="sxs-lookup"><span data-stu-id="a848c-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="a848c-159">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a848c-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="a848c-160">Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a848c-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="a848c-161">Comparación de períodos contables usando fórmulas de períodos</span><span class="sxs-lookup"><span data-stu-id="a848c-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="a848c-162">El esquema de cuentas puede comparar los resultados de diferentes períodos contables, como este mes en comparación con el mismo mes del año anterior.</span><span class="sxs-lookup"><span data-stu-id="a848c-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="a848c-163">Para hacerlo, agregue una columna con el campo **Fórmula de periodo comparativo** y luego establezca ese campo en una fórmula de período.</span><span class="sxs-lookup"><span data-stu-id="a848c-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="a848c-164">Un periodo contable no tiene que coincidir con el calendario, pero el año fiscal debe tener el mismo número de periodos contables, aunque cada periodo tenga una duración diferente.</span><span class="sxs-lookup"><span data-stu-id="a848c-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a848c-165"> utiliza la fórmula de periodo para calcular el importe a partir del periodo comparativo en relación con el periodo representado por el filtro de fecha de la solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="a848c-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="a848c-166">El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha.</span><span class="sxs-lookup"><span data-stu-id="a848c-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="a848c-167">Las abreviaturas de las especificaciones del periodo son:</span><span class="sxs-lookup"><span data-stu-id="a848c-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a848c-168">Siglas</span><span class="sxs-lookup"><span data-stu-id="a848c-168">Abbreviation</span></span></th>
<th><span data-ttu-id="a848c-169">Description</span><span class="sxs-lookup"><span data-stu-id="a848c-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a848c-170">P</span><span class="sxs-lookup"><span data-stu-id="a848c-170">P</span></span></p></td>
<td><p><span data-ttu-id="a848c-171">Periodo</span><span class="sxs-lookup"><span data-stu-id="a848c-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a848c-172">LP</span><span class="sxs-lookup"><span data-stu-id="a848c-172">LP</span></span></p></td>
<td><p><span data-ttu-id="a848c-173">Último periodo de un año fiscal, medio año o trimestre.</span><span class="sxs-lookup"><span data-stu-id="a848c-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a848c-174">CP</span><span class="sxs-lookup"><span data-stu-id="a848c-174">CP</span></span></p></td>
<td><p><span data-ttu-id="a848c-175">Periodo actual de un año fiscal, medio año o trimestre.</span><span class="sxs-lookup"><span data-stu-id="a848c-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a848c-176">FY</span><span class="sxs-lookup"><span data-stu-id="a848c-176">FY</span></span></p></td>
<td><p><span data-ttu-id="a848c-177">Año fiscal.</span><span class="sxs-lookup"><span data-stu-id="a848c-177">Fiscal year.</span></span> <span data-ttu-id="a848c-178">Por ejemplo, AF[1..3] indica el primer trimestre del año fiscal actual</span><span class="sxs-lookup"><span data-stu-id="a848c-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a848c-179">Ejemplos de fórmulas:</span><span class="sxs-lookup"><span data-stu-id="a848c-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a848c-180">Fórmula</span><span class="sxs-lookup"><span data-stu-id="a848c-180">Formula</span></span></th>
<th><span data-ttu-id="a848c-181">Description</span><span class="sxs-lookup"><span data-stu-id="a848c-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a848c-182">&lt;En blanco&gt;</span><span class="sxs-lookup"><span data-stu-id="a848c-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="a848c-183">Periodo actual</span><span class="sxs-lookup"><span data-stu-id="a848c-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a848c-184">-1P</span><span class="sxs-lookup"><span data-stu-id="a848c-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="a848c-185">Periodo anterior</span><span class="sxs-lookup"><span data-stu-id="a848c-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a848c-186">-1AF[1..UP]</span><span class="sxs-lookup"><span data-stu-id="a848c-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="a848c-187">Todo el año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="a848c-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a848c-188">-1AF</span><span class="sxs-lookup"><span data-stu-id="a848c-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="a848c-189">Periodo actual del año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="a848c-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a848c-190">-1AF[1..3]</span><span class="sxs-lookup"><span data-stu-id="a848c-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="a848c-191">Primer trimestre del año fiscal anterior</span><span class="sxs-lookup"><span data-stu-id="a848c-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a848c-192">-1AF[1..PA]</span><span class="sxs-lookup"><span data-stu-id="a848c-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="a848c-193">Desde el principio de año fiscal anterior hasta el periodo actual en el año fiscal anterior, ambos inclusive</span><span class="sxs-lookup"><span data-stu-id="a848c-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a848c-194">-1AF[PA..UP]</span><span class="sxs-lookup"><span data-stu-id="a848c-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="a848c-195">Desde el periodo actual del año fiscal anterior hasta el último periodo del año fiscal anterior, ambos inclusive</span><span class="sxs-lookup"><span data-stu-id="a848c-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a848c-196">Si desea calcular el importe del periodo de comparación para periodos de tiempo regulares, deberá introducir una fórmula en el campo **Fórmula fecha comparación**.</span><span class="sxs-lookup"><span data-stu-id="a848c-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="a848c-197">No siempre es transparente qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables que se reflejan en los datos del plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="a848c-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="a848c-198">Por ejemplo, cree un esquema de cuentas en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Filtro de período de fecha de comparación** en *-1FY*.</span><span class="sxs-lookup"><span data-stu-id="a848c-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="a848c-199">Luego, ejecute el informe el 28 de febrero y configure el filtro de fecha en enero y febrero.</span><span class="sxs-lookup"><span data-stu-id="a848c-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="a848c-200">Como resultado, el calendario de cuentas compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.</span><span class="sxs-lookup"><span data-stu-id="a848c-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="a848c-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a848c-201">See Also</span></span>
[<span data-ttu-id="a848c-202">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="a848c-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="a848c-203">Finanzas</span><span class="sxs-lookup"><span data-stu-id="a848c-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="a848c-204">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="a848c-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="a848c-205">Libro mayor y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="a848c-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="a848c-206">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a848c-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

