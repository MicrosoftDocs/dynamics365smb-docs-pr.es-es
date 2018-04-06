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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="c6dec-103">Conectar Power BI con los paquetes de contenido Business Central</span><span class="sxs-lookup"><span data-stu-id="c6dec-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="c6dec-104">Obtener información de los datos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] resulta muy sencillo con los paquetes de contenido de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6dec-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="c6dec-105">Power BI extrae los datos, genera un panel original y envía informes en función de los datos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="c6dec-106">Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Power BI.</span><span class="sxs-lookup"><span data-stu-id="c6dec-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="c6dec-107">Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="c6dec-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="c6dec-108">Los paquetes de contenido de Power BI requieren permisos para las tablas desde donde se recuperan los datos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="c6dec-109">A continuación se describen más detalles sobre los requisitos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="c6dec-110">Cómo conectarse</span><span class="sxs-lookup"><span data-stu-id="c6dec-110">How to Connect</span></span>
1. <span data-ttu-id="c6dec-111">Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.</span><span class="sxs-lookup"><span data-stu-id="c6dec-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="c6dec-112">![Navegar para obtener datos](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="c6dec-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="c6dec-113">En el cuadro **Servicios**, seleccione **Obtener**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="c6dec-114">Se abrirá una ventana con **AppSource** y **aplicaciones para aplicaciones de Power BI**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="c6dec-115">![Seleccionar paquetes de contenidos de servicios en línea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="c6dec-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="c6dec-116">Seleccione **Aplicaciones** de la pestaña **Aplicaciones para aplicaciones de Power BI** y elija el paquete de contenidos **Microsoft Dynamics 365 Business Central** que quiera usar, a continuación, seleccione **Obtener ahora**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="c6dec-117">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="c6dec-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="c6dec-118">Cuando se lo solicite, escriba el nombre de *su empresa* en [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6dec-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="c6dec-119">Este no es el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c6dec-119">This is not the display name.</span></span>  
<span data-ttu-id="c6dec-120">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="c6dec-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="c6dec-121">Una vez conectado se cargarán automáticamente un panel, un informe y un conjunto de datos en su espacio de trabajo de Power BI.</span><span class="sxs-lookup"><span data-stu-id="c6dec-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="c6dec-122">Cuando se haya completado, se actualizarán los mosaicos con datos de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c6dec-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="c6dec-123">![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="c6dec-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="c6dec-124">¿Y ahora qué?</span><span class="sxs-lookup"><span data-stu-id="c6dec-124">What Now?</span></span>

- <span data-ttu-id="c6dec-125">[Cambie los mosaicos](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c6dec-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="c6dec-126">[Seleccione un mosaico](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) para abrir el informe subyacente.</span><span class="sxs-lookup"><span data-stu-id="c6dec-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="c6dec-127">Mientras que su conjunto de datos se programa para actualizarse diariamente, puede cambiar el programa de actualización o intentar actualizarlo bajo demanda mediante **Actualizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="c6dec-128">Requisitos del sistema</span><span class="sxs-lookup"><span data-stu-id="c6dec-128">System Requirements</span></span>
<span data-ttu-id="c6dec-129">Para importar los datos de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] en Power BI, necesita permisos para los servicios web utilizados para recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="c6dec-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="c6dec-130">Los servicios web necesarios para los contenidos de paquetes incluyen:</span><span class="sxs-lookup"><span data-stu-id="c6dec-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="c6dec-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="c6dec-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="c6dec-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="c6dec-132">SalesOpportunities</span></span>
- <span data-ttu-id="c6dec-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="c6dec-134">**Microsoft Dynamics 365 Business Central – Sales**</span><span class="sxs-lookup"><span data-stu-id="c6dec-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="c6dec-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="c6dec-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="c6dec-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="c6dec-136">SalesDashboard</span></span>
- <span data-ttu-id="c6dec-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="c6dec-138">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="c6dec-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="c6dec-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="c6dec-139">PowerBIFinance</span></span>
- <span data-ttu-id="c6dec-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="c6dec-141">**Microsoft Dynamics 365 Business Central – Proyectos**</span><span class="sxs-lookup"><span data-stu-id="c6dec-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="c6dec-142">Lista de proyectos</span><span class="sxs-lookup"><span data-stu-id="c6dec-142">Job List</span></span>
- <span data-ttu-id="c6dec-143">Líneas planificación proyecto</span><span class="sxs-lookup"><span data-stu-id="c6dec-143">Job Planning Lines</span></span>
- <span data-ttu-id="c6dec-144">Líneas tarea proyecto</span><span class="sxs-lookup"><span data-stu-id="c6dec-144">Job Task Lines</span></span>

<span data-ttu-id="c6dec-145">**Microsoft Dynamics 365 Business Central – Lista Clientes**</span><span class="sxs-lookup"><span data-stu-id="c6dec-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="c6dec-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="c6dec-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="c6dec-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="c6dec-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="c6dec-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="c6dec-149">SalesDashboard</span></span>
- <span data-ttu-id="c6dec-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="c6dec-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="c6dec-152">**Microsoft Dynamics 365 Business Central – Lista Productos**</span><span class="sxs-lookup"><span data-stu-id="c6dec-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="c6dec-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="c6dec-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="c6dec-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="c6dec-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="c6dec-156">Productos</span><span class="sxs-lookup"><span data-stu-id="c6dec-156">Items</span></span>
- <span data-ttu-id="c6dec-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="c6dec-157">SalesDashboard</span></span>
- <span data-ttu-id="c6dec-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="c6dec-159">**Microsoft Dynamics 365 Business Central – Lista Proveedores**</span><span class="sxs-lookup"><span data-stu-id="c6dec-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="c6dec-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="c6dec-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="c6dec-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="c6dec-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="c6dec-163">Productos</span><span class="sxs-lookup"><span data-stu-id="c6dec-163">Items</span></span>
- <span data-ttu-id="c6dec-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="c6dec-164">SalesDashboard</span></span>
- <span data-ttu-id="c6dec-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="c6dec-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="c6dec-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="c6dec-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="c6dec-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="c6dec-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="c6dec-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="c6dec-169">Servicios Web</span><span class="sxs-lookup"><span data-stu-id="c6dec-169">Web Services</span></span>
<span data-ttu-id="c6dec-170">Un modo de fácil de encontrar los servicios web es buscarlos en [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6dec-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="c6dec-171">En la lista, asegúrese de que el cuadro Publicar esté marcado para los servicios web enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c6dec-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c6dec-172">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="c6dec-172">Troubleshooting</span></span>
<span data-ttu-id="c6dec-173">El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual.</span><span class="sxs-lookup"><span data-stu-id="c6dec-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="c6dec-174">Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.</span><span class="sxs-lookup"><span data-stu-id="c6dec-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="c6dec-175">Nombre empresa incorrecto</span><span class="sxs-lookup"><span data-stu-id="c6dec-175">Incorrect Company Name</span></span>  
<span data-ttu-id="c6dec-176">Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c6dec-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="c6dec-177">Para buscar el nombre de la empresa, busque **Empresas**.</span><span class="sxs-lookup"><span data-stu-id="c6dec-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="c6dec-178">A continuación, use el campo **Nombre** al introducir el nombre de su empresa.</span><span class="sxs-lookup"><span data-stu-id="c6dec-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="c6dec-179">Nombre de usuario y contraseña incorrectos</span><span class="sxs-lookup"><span data-stu-id="c6dec-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="c6dec-180">El nombre de usuario y la contraseña utilizados para conectarse deben ser los mismos que se usan para conectarse a su cuenta de Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6dec-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="c6dec-181">Los paquetes de contenido requieren también que tenga una cuenta de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6dec-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="c6dec-182">Una vez que introduzca sus credenciales, descubriremos automáticamente los inquilinos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a los que tenga acceso.</span><span class="sxs-lookup"><span data-stu-id="c6dec-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="c6dec-183">Si no tiene una cuenta de prueba o con licencia de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], recibirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="c6dec-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="c6dec-184">La clave no coincidió con ninguna fila de la tabla</span><span class="sxs-lookup"><span data-stu-id="c6dec-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="c6dec-185">Si introduce un nombre de empresa no válido durante el proceso de conexión, puede recibir el mensaje de error "La clave no coincidió con ninguna fila de la tabla".</span><span class="sxs-lookup"><span data-stu-id="c6dec-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="c6dec-186">Proporcione el nombre correcto de la empresa e intente conectarse de nuevo.</span><span class="sxs-lookup"><span data-stu-id="c6dec-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6dec-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c6dec-187">See Also</span></span>
[<span data-ttu-id="c6dec-188">Introducción a Power BI</span><span class="sxs-lookup"><span data-stu-id="c6dec-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="c6dec-189">[Power BI - Conceptos básicos](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Inteligencia empresarial](bi.md)</span><span class="sxs-lookup"><span data-stu-id="c6dec-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="c6dec-190">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="c6dec-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="c6dec-191">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="c6dec-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="c6dec-192">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="c6dec-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="c6dec-193">Finanzas</span><span class="sxs-lookup"><span data-stu-id="c6dec-193">Finance</span></span>](finance.md)  
<span data-ttu-id="c6dec-194">[Informe de configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="c6dec-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

