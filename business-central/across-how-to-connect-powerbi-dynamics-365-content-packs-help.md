---
title: "Cómo conectar Power BI a Business Central | Documentos de Microsoft"
description: "Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con Power BI y los paquetes de contenido de Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: es-es
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="00445-103">Conectar Power BI con los paquetes de contenido de Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="00445-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="00445-104">Obtener información de los datos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] resulta muy sencillo con los paquetes de contenido de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="00445-105">Power BI extrae los datos, genera un panel original y envía informes en función de los datos.</span><span class="sxs-lookup"><span data-stu-id="00445-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="00445-106">Debe disponer de una cuenta válida con Dynamics 365 y con Power BI.</span><span class="sxs-lookup"><span data-stu-id="00445-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="00445-107">Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) si desea crear sus propios informes de Power BI.</span><span class="sxs-lookup"><span data-stu-id="00445-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="00445-108">Los paquetes de contenido de Power BI requieren permisos para las tablas desde donde se recuperan los datos.</span><span class="sxs-lookup"><span data-stu-id="00445-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="00445-109">A continuación se describen más detalles sobre los requisitos.</span><span class="sxs-lookup"><span data-stu-id="00445-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="00445-110">Cómo conectarse</span><span class="sxs-lookup"><span data-stu-id="00445-110">How to Connect</span></span>
1. <span data-ttu-id="00445-111">Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.</span><span class="sxs-lookup"><span data-stu-id="00445-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="00445-112">![Navegar para obtener datos](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="00445-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="00445-113">También puede empezar desde Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="00445-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="00445-114">En el área de trabajo, vaya a **Selección de informe** de la parte Área de trabajo de Power BI.</span><span class="sxs-lookup"><span data-stu-id="00445-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="00445-115">Seleccione **Servicio** o **Mi organización** en la cinta.</span><span class="sxs-lookup"><span data-stu-id="00445-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="00445-116">Cuando cualquiera de estas acciones está seleccionada, accederá a la galería de la organización en Power BI o a la biblioteca de servicios en Power BI, que también se filtrarán para mostrar solo los paquetes de contenido relacionados con [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="00445-117">En el cuadro **Servicios**, seleccione **Obtener**.</span><span class="sxs-lookup"><span data-stu-id="00445-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="00445-118">Se abrirá una ventana con **AppSource** y **aplicaciones para aplicaciones de Power BI**.</span><span class="sxs-lookup"><span data-stu-id="00445-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="00445-119">![Seleccionar paquetes de contenidos de servicios en línea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="00445-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="00445-120">Seleccione **Aplicaciones** de la pestaña **Aplicaciones para aplicaciones de Power BI** y elija el paquete de contenidos **Microsoft Dynamics 365 Business Central** que quiera usar, a continuación, seleccione **Obtener ahora**.</span><span class="sxs-lookup"><span data-stu-id="00445-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="00445-121">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="00445-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="00445-122">Cuando se lo solicite, escriba el nombre de *su empresa* en [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="00445-123">Este no es el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="00445-123">This is not the display name.</span></span> <span data-ttu-id="00445-124">El nombre de la empresa puede encontrarse en la página "Empresas" de su instancia de [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="00445-125">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="00445-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="00445-126">Una vez conectado se cargarán automáticamente un panel, un informe y un conjunto de datos en su espacio de trabajo de Power BI.</span><span class="sxs-lookup"><span data-stu-id="00445-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="00445-127">Cuando se haya completado, se actualizarán los mosaicos con datos de su empresa de [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="00445-128">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="00445-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="00445-129">¿Y ahora qué?</span><span class="sxs-lookup"><span data-stu-id="00445-129">What Now?</span></span>

- <span data-ttu-id="00445-130">Intente [hacer una pregunta en el cuadro de preguntas](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) en la parte superior del escritorio.</span><span class="sxs-lookup"><span data-stu-id="00445-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="00445-131">[Cambie los mosaicos](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="00445-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="00445-132">[Seleccione un mosaico](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) para abrir el informe subyacente.</span><span class="sxs-lookup"><span data-stu-id="00445-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="00445-133">Mientras que su conjunto de datos se programa para actualizarse diariamente, puede cambiar el programa de actualización o intentar actualizarlo bajo demanda mediante **Actualizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="00445-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="00445-134">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="00445-134">System Requirements</span></span>
<span data-ttu-id="00445-135">Para importar los datos de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] en Power BI, necesita permisos para los servicios web utilizados para recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="00445-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="00445-136">Los servicios web necesarios para los contenidos de paquetes incluyen:</span><span class="sxs-lookup"><span data-stu-id="00445-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="00445-137">Informes de Área de trabajo</span><span class="sxs-lookup"><span data-stu-id="00445-137">Role Center Reports</span></span>

<span data-ttu-id="00445-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="00445-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="00445-139">Oportunidades de venta</span><span class="sxs-lookup"><span data-stu-id="00445-139">Sales Opportunities</span></span>
- <span data-ttu-id="00445-140">Empresa de vista de plantilla de Excel</span><span class="sxs-lookup"><span data-stu-id="00445-140">Excel Template View Company</span></span>
- <span data-ttu-id="00445-141">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-141">Power BI Report Labels</span></span>

<span data-ttu-id="00445-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="00445-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="00445-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="00445-143">PowerBIFinance</span></span>
- <span data-ttu-id="00445-144">Empresa de vista de plantilla de Excel</span><span class="sxs-lookup"><span data-stu-id="00445-144">Excel Template View Company</span></span>
- <span data-ttu-id="00445-145">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-145">Power BI Report Labels</span></span>

<span data-ttu-id="00445-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="00445-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="00445-147">Lista de proyectos</span><span class="sxs-lookup"><span data-stu-id="00445-147">Job List</span></span>
- <span data-ttu-id="00445-148">Líneas planificación proyecto</span><span class="sxs-lookup"><span data-stu-id="00445-148">Job Planning Lines</span></span>
- <span data-ttu-id="00445-149">Líneas tarea proyecto</span><span class="sxs-lookup"><span data-stu-id="00445-149">Job Task Lines</span></span>
- <span data-ttu-id="00445-150">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-150">Power BI Report Labels</span></span>
- <span data-ttu-id="00445-151">Empresa de vista de plantilla de Excel</span><span class="sxs-lookup"><span data-stu-id="00445-151">Excel Template View Company</span></span>

<span data-ttu-id="00445-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="00445-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="00445-153">Panel de ventas</span><span class="sxs-lookup"><span data-stu-id="00445-153">Sales Dashboard</span></span>
- <span data-ttu-id="00445-154">Empresa de vista de plantilla de Excel</span><span class="sxs-lookup"><span data-stu-id="00445-154">Excel Template View Company</span></span>
- <span data-ttu-id="00445-155">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="00445-156">Informes de páginas de listas</span><span class="sxs-lookup"><span data-stu-id="00445-156">List Page Reports</span></span> 

<span data-ttu-id="00445-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="00445-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="00445-158">Ventas de productos por cliente</span><span class="sxs-lookup"><span data-stu-id="00445-158">Item Sales by Customer</span></span>
- <span data-ttu-id="00445-159">Lista de compra del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="00445-160">Lista de ventas del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="00445-161">Panel de ventas</span><span class="sxs-lookup"><span data-stu-id="00445-161">Sales Dashboard</span></span>
- <span data-ttu-id="00445-162">Lista de clientes de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-162">Power BI Customer List</span></span>
- <span data-ttu-id="00445-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-164">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-164">Power BI Report Labels</span></span> 

<span data-ttu-id="00445-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="00445-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="00445-166">Lista de importes CG de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="00445-167">Cantidad presupuestada CG de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="00445-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-169">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-169">Power BI Report Labels</span></span>

<span data-ttu-id="00445-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="00445-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="00445-171">Ventas de productos por cliente</span><span class="sxs-lookup"><span data-stu-id="00445-171">Item Sales by Customer</span></span>
- <span data-ttu-id="00445-172">Lista de compra del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="00445-173">Lista de ventas del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="00445-174">Panel de ventas</span><span class="sxs-lookup"><span data-stu-id="00445-174">Sales Dashboard</span></span>
- <span data-ttu-id="00445-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-176">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-176">Power BI Report Labels</span></span>

<span data-ttu-id="00445-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="00445-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="00445-178">Lista de proyectos de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-178">Power BI Jobs List</span></span>
- <span data-ttu-id="00445-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-180">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-180">Power BI Report Labels</span></span>

<span data-ttu-id="00445-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="00445-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="00445-182">Lista de compras de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-182">Power BI Purchase List</span></span>
- <span data-ttu-id="00445-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-184">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-184">Power BI Report Labels</span></span>

<span data-ttu-id="00445-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="00445-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="00445-186">Lista de ventas de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-186">Power BI Sales List</span></span>
- <span data-ttu-id="00445-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-188">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-188">Power BI Report Labels</span></span>


<span data-ttu-id="00445-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="00445-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="00445-190">Lista de compra del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="00445-191">Lista de ventas del producto Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="00445-192">Lista de proveedores de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-192">Power BI Vendor List</span></span>
- <span data-ttu-id="00445-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="00445-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="00445-194">Etiquetas de informe de Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="00445-195">Servicios Web</span><span class="sxs-lookup"><span data-stu-id="00445-195">Web Services</span></span>
<span data-ttu-id="00445-196">Un modo de fácil de encontrar los servicios web es buscarlos en [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="00445-197">En la lista, asegúrese de que el cuadro Publicar esté marcado para los servicios web enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="00445-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="00445-198">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="00445-198">Troubleshooting</span></span>
<span data-ttu-id="00445-199">El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual.</span><span class="sxs-lookup"><span data-stu-id="00445-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="00445-200">Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.</span><span class="sxs-lookup"><span data-stu-id="00445-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="00445-201">Nombre empresa incorrecto</span><span class="sxs-lookup"><span data-stu-id="00445-201">Incorrect Company Name</span></span>  
<span data-ttu-id="00445-202">Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="00445-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="00445-203">Para buscar el nombre de la empresa, busque **Empresas**.</span><span class="sxs-lookup"><span data-stu-id="00445-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="00445-204">A continuación, use el campo **Nombre** al introducir el nombre de su empresa.</span><span class="sxs-lookup"><span data-stu-id="00445-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="00445-205">Nombre de usuario y contraseña incorrectos</span><span class="sxs-lookup"><span data-stu-id="00445-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="00445-206">El nombre de usuario y la contraseña utilizados para conectarse deben ser los mismos que se usan para conectarse a su cuenta de Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="00445-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="00445-207">Los paquetes de contenido requieren también que tenga una cuenta de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00445-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="00445-208">Una vez que introduzca sus credenciales, descubriremos automáticamente los inquilinos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a los que tenga acceso.</span><span class="sxs-lookup"><span data-stu-id="00445-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="00445-209">Si no tiene una cuenta de prueba o con licencia de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="00445-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="00445-210">La clave no coincidió con ninguna fila de la tabla</span><span class="sxs-lookup"><span data-stu-id="00445-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="00445-211">Si introduce un nombre de empresa no válido durante el proceso de conexión, puede recibir el mensaje de error "La clave no coincidió con ninguna fila de la tabla".</span><span class="sxs-lookup"><span data-stu-id="00445-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="00445-212">Proporcione el nombre correcto de la empresa e intente conectarse de nuevo.</span><span class="sxs-lookup"><span data-stu-id="00445-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="00445-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00445-213">See Also</span></span>
[<span data-ttu-id="00445-214">Introducción a Power BI</span><span class="sxs-lookup"><span data-stu-id="00445-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="00445-215">Power BI - Conceptos básicos</span><span class="sxs-lookup"><span data-stu-id="00445-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="00445-216">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="00445-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="00445-217">Introducción</span><span class="sxs-lookup"><span data-stu-id="00445-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="00445-218">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="00445-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="00445-219">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="00445-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="00445-220">Finanzas</span><span class="sxs-lookup"><span data-stu-id="00445-220">Finance</span></span>](finance.md)  
<span data-ttu-id="00445-221">[Informe de configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="00445-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

