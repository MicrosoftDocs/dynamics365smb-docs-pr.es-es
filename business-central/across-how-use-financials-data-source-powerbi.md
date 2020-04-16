---
title: Usar Business Central en los informes de Power BI | Microsoft Docs
description: Haga que los datos estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187897"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="8a951-103">Usar [!INCLUDE [prodlong](includes/prodlong.md)] como fuente de datos de Power BI para generar informes</span><span class="sxs-lookup"><span data-stu-id="8a951-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="8a951-104">Puede hacer que los datos de [!INCLUDE[prodlong](includes/prodlong.md)] estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.</span><span class="sxs-lookup"><span data-stu-id="8a951-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="8a951-105">Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power BI.</span><span class="sxs-lookup"><span data-stu-id="8a951-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="8a951-106">Debe descargar también [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span><span class="sxs-lookup"><span data-stu-id="8a951-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="8a951-107">Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="8a951-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="8a951-108">Para agregar [!INCLUDE[prodshort](includes/prodshort.md)] como origen de datos de Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8a951-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="8a951-109">En Power BI Desktop, en el panel de navegador izquierdo, elija **Obtener datos**.</span><span class="sxs-lookup"><span data-stu-id="8a951-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="8a951-110">En la página **Obtener datos**, **Servicios en línea**, elija **Microsoft Dynamics 365 Business Central** y después seleccione el botón **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="8a951-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="8a951-111">Power BI muestra un asistente que le guiará por el proceso de conexión, incluido el inicio de sesión en [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8a951-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="8a951-112">Elija **Iniciar sesión** y luego elija la cuenta pertinente.</span><span class="sxs-lookup"><span data-stu-id="8a951-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="8a951-113">Use la misma cuenta con la que inicia sesión en [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8a951-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="8a951-114">Elija el botón **Conectar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="8a951-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="8a951-115">El asistente de Power BI muestra una lista de los entornos, las empresas y los orígenes de datos de Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8a951-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="8a951-116">Estos orígenes de datos todos los servicios web que haya publicado desde [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8a951-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="8a951-117">También puede crear una nueva URL de servicio web en [!INCLUDE [prodshort](includes/prodshort.md)] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8a951-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="8a951-118">Elija uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="8a951-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="8a951-119">Utilizar la acción **Crear conjunto de datos** en la página **Servicios web**</span><span class="sxs-lookup"><span data-stu-id="8a951-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="8a951-120">Utilizar la guía de configuración asistida **Configurar informes**</span><span class="sxs-lookup"><span data-stu-id="8a951-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="8a951-121">Elegir la acción **Editar en Excel** en cualquier lista</span><span class="sxs-lookup"><span data-stu-id="8a951-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="8a951-122">Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.</span><span class="sxs-lookup"><span data-stu-id="8a951-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="8a951-123">Repita los pasos anteriores agregar datos de [!INCLUDE [prodshort](includes/prodshort.md)] adicionales, u otros datos, a su modelo de datos de Power BI.</span><span class="sxs-lookup"><span data-stu-id="8a951-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="8a951-124">Una vez que se haya conectado correctamente a [!INCLUDE [prodshort](includes/prodshort.md)], no se le volverá a solicitar que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="8a951-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="8a951-125">Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página.</span><span class="sxs-lookup"><span data-stu-id="8a951-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="8a951-126">Se ha conectado correctamente con los datos de [!INCLUDE [prodshort](includes/prodshort.md)] y puede comenzar a crear su informe de Power BI.</span><span class="sxs-lookup"><span data-stu-id="8a951-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="8a951-127">Antes de elaborar el informe, le recomendamos que importe el archivo de tema de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8a951-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="8a951-128">El archivo de tema creará una paleta de colores de forma que pueda crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prodshort](includes/prodshort.md)] sin pedirle que defina colores personalizados para cada elemento visual.</span><span class="sxs-lookup"><span data-stu-id="8a951-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="8a951-129">Para obtener más información, consulte la [documentación de Power BI](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="8a951-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8a951-130">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="8a951-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="8a951-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a951-131">See Also</span></span>

[<span data-ttu-id="8a951-132">Habilitar los datos de negocio para Power BI</span><span class="sxs-lookup"><span data-stu-id="8a951-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="8a951-133">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="8a951-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="8a951-134">Introducción</span><span class="sxs-lookup"><span data-stu-id="8a951-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="8a951-135">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="8a951-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="8a951-136">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="8a951-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="8a951-137">Finanzas</span><span class="sxs-lookup"><span data-stu-id="8a951-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="8a951-138">Inicio rápido: Conectarse a los datos de Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8a951-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
