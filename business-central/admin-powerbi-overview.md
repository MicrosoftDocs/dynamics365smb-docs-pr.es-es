---
title: Descripción general de la arquitectura y el componente de integración de Power BI para Business Central | Documentos de Microsoft
description: Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con las aplicaciones de Business Central para Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753775"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="e450c-103">Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="e450c-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="e450c-104">En este artículo, aprenderá sobre los diferentes aspectos de la integración de Power BI con [!INCLUDE[prod_short](includes/prod_short.md)] para ayudarle a comprender su implementación y uso.</span><span class="sxs-lookup"><span data-stu-id="e450c-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="e450c-105">Componentes</span><span class="sxs-lookup"><span data-stu-id="e450c-105">Components</span></span>

<span data-ttu-id="e450c-106">La siguiente tabla describe los componentes principales relacionados con la integración de Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="e450c-107">Componente</span><span class="sxs-lookup"><span data-stu-id="e450c-107">Component</span></span>|<span data-ttu-id="e450c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e450c-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="e450c-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-109">Power BI</span></span>|<span data-ttu-id="e450c-110">Un servicio de administración y alojamiento de informes basado en la nube.</span><span class="sxs-lookup"><span data-stu-id="e450c-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="e450c-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e450c-111">Power BI Desktop</span></span>|<span data-ttu-id="e450c-112">Una herramienta de creación para crear informes y paneles, y le permite ejecutar informes.</span><span class="sxs-lookup"><span data-stu-id="e450c-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="e450c-113">Está disponible como descarga gratuita en Microsoft Store y se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="e450c-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="e450c-114">Solución en línea o local con conectores expuestos a Power BI y la capacidad de incrustar una parte de Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="e450c-115">Que hay disponible desde el principio</span><span class="sxs-lookup"><span data-stu-id="e450c-115">What's available from the start</span></span>

<span data-ttu-id="e450c-116">La siguiente tabla describe las características disponibles.</span><span class="sxs-lookup"><span data-stu-id="e450c-116">The following table describes available features.</span></span>

|<span data-ttu-id="e450c-117">Característica</span><span class="sxs-lookup"><span data-stu-id="e450c-117">Feature</span></span>|<span data-ttu-id="e450c-118">Soporte de [!INCLUDE[prod_short](includes/prod_short.md)] online o local</span><span class="sxs-lookup"><span data-stu-id="e450c-118">[!INCLUDE[prod_short](includes/prod_short.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="e450c-119">Conectores de Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-119">Power BI connectors</span></span>|<span data-ttu-id="e450c-120">Ambos.</span><span class="sxs-lookup"><span data-stu-id="e450c-120">Both.</span></span> <span data-ttu-id="e450c-121">Diferentes conectores para online y local.</span><span class="sxs-lookup"><span data-stu-id="e450c-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="e450c-122">Mismo conector usado para Power BI Desktop y el servicio Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="e450c-123">Experiencia integrada para ver un informe determinado dentro de un FactBox en [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="e450c-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="e450c-124">Ambos.</span><span class="sxs-lookup"><span data-stu-id="e450c-124">Both.</span></span> <span data-ttu-id="e450c-125">Requiere configuración para mostrar informes de forma local.</span><span class="sxs-lookup"><span data-stu-id="e450c-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="e450c-126">Gestión de informes de Power BI desde [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="e450c-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="e450c-127">Online</span><span class="sxs-lookup"><span data-stu-id="e450c-127">Online</span></span>|
|<span data-ttu-id="e450c-128">Los informes predeterminados de Power BI sobre centros de roles desplegados en Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="e450c-129">Online</span><span class="sxs-lookup"><span data-stu-id="e450c-129">Online</span></span>|
|<span data-ttu-id="e450c-130">Aplicaciones de Power BI en Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="e450c-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="e450c-131">Online.</span><span class="sxs-lookup"><span data-stu-id="e450c-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="e450c-132">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="e450c-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e450c-133">se integra con Power BI a través de un conector que utiliza OData.</span><span class="sxs-lookup"><span data-stu-id="e450c-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="e450c-134">La fuente de datos para los informes de Power BI se exponen como servicios web de OData.</span><span class="sxs-lookup"><span data-stu-id="e450c-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Arquitectura de Power BI para la integración con Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="e450c-136">Flujo general</span><span class="sxs-lookup"><span data-stu-id="e450c-136">General Flow</span></span>

<span data-ttu-id="e450c-137">El siguiente diagrama ilustra el flujo de trabajo básico para los usuarios al conectar [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Flujo de trabajo de Power BI para la integración con Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="e450c-139">El usuario se registra para una cuenta de Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="e450c-140">El usuario se conecta a Power BI desde [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e450c-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e450c-141">verifica la licencia.</span><span class="sxs-lookup"><span data-stu-id="e450c-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e450c-142">despliega informes predeterminados en el servicio de Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="e450c-143">Este paso solo ocurre para [!INCLUDE[prod_short](includes/prod_short.md)] online.</span><span class="sxs-lookup"><span data-stu-id="e450c-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e450c-144">hace que los informes en Power BI estén disponibles para la selección en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e450c-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e450c-145">Los informes predeterminados se muestran automáticamente en partes de Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="e450c-146">El usuario crea un informe en Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="e450c-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="e450c-147">El usuario publica el informe en el servicio Power BI.</span><span class="sxs-lookup"><span data-stu-id="e450c-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="e450c-148">Los informes están disponibles para su selección en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e450c-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="e450c-149">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="e450c-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="e450c-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e450c-150">See Also</span></span>

[<span data-ttu-id="e450c-151">Business Central y Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="e450c-152">Power BI para consumidores</span><span class="sxs-lookup"><span data-stu-id="e450c-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="e450c-153">El nuevo aspecto del servicio Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="e450c-154">Inicio rápido: Conectarse a los datos de Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e450c-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="e450c-155">Documentación de Power BI</span><span class="sxs-lookup"><span data-stu-id="e450c-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="e450c-156">Inteligencia empresarial</span><span class="sxs-lookup"><span data-stu-id="e450c-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="e450c-157">Introducción</span><span class="sxs-lookup"><span data-stu-id="e450c-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="e450c-158">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="e450c-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e450c-159">[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e450c-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="e450c-160">[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="e450c-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="e450c-161">[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="e450c-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="e450c-162">[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="e450c-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
