---
title: Mostrar informes de Power BI personalizados para datos de Business Central
description: Puede usar los informes de Power BI para obtener más información sobre los datos en las listas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/26/2021
ms.author: jswymer
ms.openlocfilehash: d2ce2588604ae676ba8b2cb73878a2d8dfd32b63
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087699"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="504fa-103">Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="504fa-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="504fa-104">incluye un elemento de control de cuadro informativo de Power BI en muchas páginas de lista clave.</span><span class="sxs-lookup"><span data-stu-id="504fa-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="504fa-105">El objetivo de este cuadro informativo es mostrar informes de Power BI relacionados con los registros de las listas, lo que ofrece más información sobre los datos.</span><span class="sxs-lookup"><span data-stu-id="504fa-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="504fa-106">La idea es que a, medida que se desplaza por las filas de la lista, el informe se actualice para la entrada seleccionada.</span><span class="sxs-lookup"><span data-stu-id="504fa-106">The idea is that as you move between rows in the list, the report updates for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="504fa-107">viene listo con algunos de estos informes.</span><span class="sxs-lookup"><span data-stu-id="504fa-107">comes ready with some of these reports.</span></span> <span data-ttu-id="504fa-108">También puede crear sus propios informes personalizados que se muestran en este cuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="504fa-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="504fa-109">La creación de estos informes es similar a otros informes.</span><span class="sxs-lookup"><span data-stu-id="504fa-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="504fa-110">Pero hay algunas reglas de diseño que deberá seguir para asegurarse de que los informes se muestren como se espera.</span><span class="sxs-lookup"><span data-stu-id="504fa-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="504fa-111">En este artículo se explica estas reglas.</span><span class="sxs-lookup"><span data-stu-id="504fa-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="504fa-112">Para obtener información general sobre la creación y la publicación de informes de Power BI para Business Central, consulte [Creación de informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="504fa-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="504fa-113">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="504fa-113">Prerequisites</span></span>

- <span data-ttu-id="504fa-114">Una cuenta de Power BI.</span><span class="sxs-lookup"><span data-stu-id="504fa-114">A Power BI account.</span></span>
- <span data-ttu-id="504fa-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="504fa-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="504fa-116">Crear un informe para una página de lista</span><span class="sxs-lookup"><span data-stu-id="504fa-116">Create a report for a list page</span></span>

1. <span data-ttu-id="504fa-117">Inicie Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="504fa-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="504fa-118">Seleccione **Obtener datos** y comience a elegir el origen de datos para el informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="504fa-119">Especifique las páginas de lista de Business Central que contienen los datos que desea en el informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-119">Specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="504fa-120">Por ejemplo, para crear un informe para la lista **Facturas de venta**, incluya páginas relacionadas con las ventas.</span><span class="sxs-lookup"><span data-stu-id="504fa-120">For example, to create a report for the **Sales Invoices** list, include pages related to sales.</span></span>

    <span data-ttu-id="504fa-121">Para obtener más información, siga las instrucciones [Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos en Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="504fa-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="504fa-122">Establezca el filtro de informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-122">Set the report filter.</span></span>

    <span data-ttu-id="504fa-123">Para hacer que los datos se actualicen en el registro seleccionado en la lista, agregue un filtro al informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="504fa-124">El filtro debe incluir un campo del origen de datos que se usa para identificar cada registro de la lista de forma única.</span><span class="sxs-lookup"><span data-stu-id="504fa-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="504fa-125">En términos de desarrollador, este campo es la *clave primaria*.</span><span class="sxs-lookup"><span data-stu-id="504fa-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="504fa-126">En la mayoría de los casos, la clave primaria de una lista es **Nº**</span><span class="sxs-lookup"><span data-stu-id="504fa-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="504fa-127">.</span><span class="sxs-lookup"><span data-stu-id="504fa-127">field.</span></span>

    <span data-ttu-id="504fa-128">Para configurar el filtro, siga los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="504fa-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="504fa-129">En **Filtros**, seleccione el campo de clave primaria de la lista de campos disponibles.</span><span class="sxs-lookup"><span data-stu-id="504fa-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="504fa-130">Arrastre el campo al panel **Filtros** y colóquelo en el cuadro **Filtros en todas las páginas**.</span><span class="sxs-lookup"><span data-stu-id="504fa-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="504fa-131">Establezca el **Tipo de filtro** en **Filtrado básico**.</span><span class="sxs-lookup"><span data-stu-id="504fa-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="504fa-132">No puede ser un filtro de página, visual o avanzado.</span><span class="sxs-lookup"><span data-stu-id="504fa-132">It can't be page, visual, or advanced filter.</span></span>

    ![Configurar el filtro para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="504fa-134">Diseñe el informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-134">Design the report layout.</span></span>

    <span data-ttu-id="504fa-135">Cree el diseño arrastrando campos y agregando visualizaciones.</span><span class="sxs-lookup"><span data-stu-id="504fa-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="504fa-136">Para obtener más información, consulte [Trabajar con la vista Informe en Power BI Desktop](/power-bi/create-reports/desktop-report-view) en la documentación de Power BI.</span><span class="sxs-lookup"><span data-stu-id="504fa-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="504fa-137">Consulte las siguientes secciones sobre el tamaño del informe y el uso de varias páginas.</span><span class="sxs-lookup"><span data-stu-id="504fa-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="504fa-138">Guarde y asigne un nombre al informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-138">Save and name the report.</span></span>

    <span data-ttu-id="504fa-139">Dele al informe un nombre que contenga el nombre de la página de lista asociada con el informe, como esté en el cliente.</span><span class="sxs-lookup"><span data-stu-id="504fa-139">Give the report a name that contains the name of the list page associated with the report, as it is in the client.</span></span> <span data-ttu-id="504fa-140">Sin embargo, el nombre no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="504fa-140">The name isn't case-sensitive though.</span></span> <span data-ttu-id="504fa-141">Suponga que el informe es para la página de lista **Facturas de venta**.</span><span class="sxs-lookup"><span data-stu-id="504fa-141">Suppose the report is for the **Sales Invoices** list page.</span></span> <span data-ttu-id="504fa-142">En este caso, incluya las palabras **facturas de venta** en algún lugar del nombre, como **mis facturas de venta.pbix** o **mi_lista_facturas_de_venta.pbix**.</span><span class="sxs-lookup"><span data-stu-id="504fa-142">In this case, include the words **sales invoices** somewhere in the name, like **my sales invoices.pbix** or **my_Sales Invoices_list.pbix**.</span></span>

    <span data-ttu-id="504fa-143">Esta convención de nomenclatura no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="504fa-143">This naming convention isn't a requirement.</span></span> <span data-ttu-id="504fa-144">Sin embargo, hace que la selección de informes en [!INCLUDE[prod_short](includes/prod_short.md)] sea más rápida.</span><span class="sxs-lookup"><span data-stu-id="504fa-144">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="504fa-145">Cuando la página de selección de informes se abre desde una página de lista, se aplica automáticamente un filtro según el nombre de la página.</span><span class="sxs-lookup"><span data-stu-id="504fa-145">When the report selection page opens from a list page, it's automatically applied a filter based on the page name.</span></span> <span data-ttu-id="504fa-146">El filtro tiene la sintaxis: `@*<caption>*`, como `@*Sales Invoices*`.</span><span class="sxs-lookup"><span data-stu-id="504fa-146">The filter has the syntax: `@*<caption>*`,  like `@*Sales Invoices*`.</span></span> <span data-ttu-id="504fa-147">Este filtrado se realiza para limitar los informes que se muestran.</span><span class="sxs-lookup"><span data-stu-id="504fa-147">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="504fa-148">Los usuarios pueden borrar el filtro para obtener una lista completa de los informes disponibles en Power BI.</span><span class="sxs-lookup"><span data-stu-id="504fa-148">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="504fa-149">Cuando haya terminado, publique el informe como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="504fa-149">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="504fa-150">Para obtener más información, consulte [Publicar un informe](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="504fa-150">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="504fa-151">Pruebe el informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-151">Test the report.</span></span>

    <span data-ttu-id="504fa-152">Una vez que el informe se haya publicado en su área de trabajo, debería estar disponible en el cuadro informativo de Power BI en la página de lista en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="504fa-152">Once the report's been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="504fa-153">Para probarlo, siga los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="504fa-153">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="504fa-154">Abra [!INCLUDE[prod_short](includes/prod_short.md)] y vaya a la página de la lista.</span><span class="sxs-lookup"><span data-stu-id="504fa-154">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="504fa-155">Si no ve el cuadro informativo de Power BI, vaya a la barra de acciones y seleccione **Acciones** > **Mostrar** > **Mostrar/ocultar informes de Power BI**.</span><span class="sxs-lookup"><span data-stu-id="504fa-155">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="504fa-156">En el cuadro informativo de Power BI, seleccione **Seleccionar informes**, seleccione el cuadro **Habilitar** para el informe y, a continuación, **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="504fa-156">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="504fa-157">Si está diseñado correctamente, se muestra el informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-157">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="504fa-158">Configurar el tamaño y el color del informe</span><span class="sxs-lookup"><span data-stu-id="504fa-158">Set the report size and color</span></span>

<span data-ttu-id="504fa-159">El tamaño del informe se debe configurar en 325 píxeles por 310 píxeles.</span><span class="sxs-lookup"><span data-stu-id="504fa-159">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="504fa-160">Este tamaño proporciona el escalado correcto del informe en el espacio disponible del control del cuadro informativo de Power BI en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="504fa-160">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="504fa-161">Para definir el tamaño del informe, coloque el enfoque fuera del área de diseño de informe y, a continuación, elija el icono de rodillo de pintura.</span><span class="sxs-lookup"><span data-stu-id="504fa-161">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Configurar la anchura y la altura para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="504fa-163">Puede cambiar el ancho y el alto del informe eligiendo **Personalizado** en el campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="504fa-163">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="504fa-164">Si desea que el fondo del informe se mezcle con el color de fondo del control del cuadro informativo de Power BI, defina un color de fondo de informe personalizado como *#FFFFFF* (blanco).</span><span class="sxs-lookup"><span data-stu-id="504fa-164">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="504fa-165">Use el archivo de tema [!INCLUDE [prod_short](includes/prod_short.md)] para crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="504fa-165">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="504fa-166">Para obtener más información, consulte [Usar el tema de informe de [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="504fa-166">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="504fa-167">Informes con varias páginas</span><span class="sxs-lookup"><span data-stu-id="504fa-167">Reports with multiple pages</span></span>

<span data-ttu-id="504fa-168">Con Power BI, puede crear un solo informe con varias páginas.</span><span class="sxs-lookup"><span data-stu-id="504fa-168">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="504fa-169">Sin embargo, para los informes que se mostrarán con páginas de lista, no recomendamos que tengan más de una página.</span><span class="sxs-lookup"><span data-stu-id="504fa-169">However, for reports that will display with list pages, we recommend that they don't have more than one page.</span></span> <span data-ttu-id="504fa-170">El cuadro informativo de Power BI solo mostrará la primera página de su informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-170">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="504fa-171">Solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="504fa-171">Fixing problems</span></span>

<span data-ttu-id="504fa-172">En esta sección se explica cómo solucionar los problemas que puede encontrar al intentar ver un informe de Power BI para una página de lista en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="504fa-172">This section explains how to fix problems that you might run into when you try to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="504fa-173">No puede ver el cuadro informativo de Power BI en una página de lista</span><span class="sxs-lookup"><span data-stu-id="504fa-173">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="504fa-174">De forma predeterminada, el cuadro informativo de Power BI está oculto a la vista.</span><span class="sxs-lookup"><span data-stu-id="504fa-174">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="504fa-175">Para mostrar el cuadro informativo en una página, en la barra de acciones, seleccione **Acciones** > **Mostrar** > **Mostrar/ocultar informes de Power BI**.</span><span class="sxs-lookup"><span data-stu-id="504fa-175">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="504fa-176">No puede ver el informe en el panel Seleccionar informe</span><span class="sxs-lookup"><span data-stu-id="504fa-176">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="504fa-177">El nombre del informe no contiene el nombre de la página de la lista que se muestra.</span><span class="sxs-lookup"><span data-stu-id="504fa-177">The report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="504fa-178">Borre el filtro para obtener una lista completa de los informes de Power BI disponibles.</span><span class="sxs-lookup"><span data-stu-id="504fa-178">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="504fa-179">El informe está cargado pero en blanco, no filtrado o filtrado incorrectamente</span><span class="sxs-lookup"><span data-stu-id="504fa-179">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="504fa-180">Verifique que el filtro de informes contenga la clave principal correcta.</span><span class="sxs-lookup"><span data-stu-id="504fa-180">Verify the report filter contains the right primary key.</span></span> <span data-ttu-id="504fa-181">En la mayoría de los casos, este campo es **Nº**,</span><span class="sxs-lookup"><span data-stu-id="504fa-181">In most cases, this field is the **No.**</span></span> <span data-ttu-id="504fa-182">pero en la tabla **Mov. contabilidad**, por ejemplo, debe usar el campo **Nº mov.**.</span><span class="sxs-lookup"><span data-stu-id="504fa-182">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="504fa-183">El informe está cargado, pero muestra una página que no esperaba</span><span class="sxs-lookup"><span data-stu-id="504fa-183">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="504fa-184">Verifique que la página que desea que se muestre es la primera página de su informe.</span><span class="sxs-lookup"><span data-stu-id="504fa-184">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="504fa-185">El informe aparecerá con un borde gris no deseado o es demasiado pequeño o demasiado grande</span><span class="sxs-lookup"><span data-stu-id="504fa-185">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="504fa-186">Compruebe que el tamaño del informe se ha configurado en 325 píxeles x 310 píxeles.</span><span class="sxs-lookup"><span data-stu-id="504fa-186">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="504fa-187">Guarde el informe y, a continuación, actualice la página de listas.</span><span class="sxs-lookup"><span data-stu-id="504fa-187">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="504fa-188">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="504fa-188">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="504fa-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="504fa-189">See Also</span></span>

[<span data-ttu-id="504fa-190">Habilitar los datos de negocio para Power BI</span><span class="sxs-lookup"><span data-stu-id="504fa-190">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="504fa-191">[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="504fa-191">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="504fa-192">Preparación para hacer negocios</span><span class="sxs-lookup"><span data-stu-id="504fa-192">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="504fa-193">[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="504fa-193">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="504fa-194">Finanzas</span><span class="sxs-lookup"><span data-stu-id="504fa-194">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]