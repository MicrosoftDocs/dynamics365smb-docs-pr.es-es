---
title: Como crear una empresa nueva | Documentos de Microsoft
description: Para usar las tablas y páginas de RapidStart Services creadas que no tienen datos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7583837e515a4fd5fb415fe1b482512e7edf6b5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754008"
---
# <a name="create-a-new-company"></a><span data-ttu-id="443d6-103">Cree una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="443d6-103">Create a New Company</span></span>
<span data-ttu-id="443d6-104">Para usar RapidStart Services para [!INCLUDE[prod_short](includes/prod_short.md)], primero debe crear una nueva empresa para la que desee realizar una implementación de cliente.</span><span class="sxs-lookup"><span data-stu-id="443d6-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="443d6-105">Al crear una empresa nueva, se crean las tablas y páginas estándar de [!INCLUDE[prod_short](includes/prod_short.md)], pero no existen datos en ellas.</span><span class="sxs-lookup"><span data-stu-id="443d6-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="443d6-106">Además, puede aplicar datos específicos de configuración a la empresa después de inicializarla.</span><span class="sxs-lookup"><span data-stu-id="443d6-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="443d6-107">La información se proporciona en un paquete de configuración, un archivo .rapidstart, que entrega contenido en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="443d6-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="443d6-108">La empresa de demostración CRONUS incluye paquetes de configuración de ejemplo, incluidos los archivos específicos del país o la región.</span><span class="sxs-lookup"><span data-stu-id="443d6-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="443d6-109">Utilice los procedimientos siguientes para utilizar el paquete de configuración de ejemplo con una nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="443d6-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="443d6-110">Utilizar el paquete de configuración BASICCONFIG de ejemplo</span><span class="sxs-lookup"><span data-stu-id="443d6-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="443d6-111">Abra la empresa CRONUS España S.A.</span><span class="sxs-lookup"><span data-stu-id="443d6-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="443d6-112">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="443d6-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="443d6-113">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="443d6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="443d6-114">Elija el paquete BASICCONFIG de la lista y, a continuación, seleccione la acción **Exportar paquete**.</span><span class="sxs-lookup"><span data-stu-id="443d6-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="443d6-115">Utilice el procedimiento siguiente para crear una nueva empresa y utilizar el paquete BASICCONFIG como parte del proceso.</span><span class="sxs-lookup"><span data-stu-id="443d6-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="443d6-116">Para crear una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="443d6-116">To create a new company</span></span>  
1. <span data-ttu-id="443d6-117">Cree una nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="443d6-117">Create a new company.</span></span> <span data-ttu-id="443d6-118">Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="443d6-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="443d6-119">Desde el área de trabajo del implementador de RapidStart Services, ahora puede importar el paquete de configuración que exportó de la empresa CRONUS España S.A.</span><span class="sxs-lookup"><span data-stu-id="443d6-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="443d6-120">Después de crear una empresa nueva, algunas tablas se rellenan automáticamente, incluso si no se aplica ningún plantilla de empresa.</span><span class="sxs-lookup"><span data-stu-id="443d6-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="443d6-121">Por ejemplo, puede revisar los códigos estándar para registrar y tratar las transacciones por lotes en la página **Código origen**.</span><span class="sxs-lookup"><span data-stu-id="443d6-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="443d6-122">Si proporciona una versión local de [!INCLUDE[prod_short](includes/prod_short.md)], debe revisar esta tabla y tener en cuenta cualquier problema de idioma local.</span><span class="sxs-lookup"><span data-stu-id="443d6-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="443d6-123">Acerca de las tablas de datos</span><span class="sxs-lookup"><span data-stu-id="443d6-123">About Data Tables</span></span>
<span data-ttu-id="443d6-124">Las tablas de datos de [!INCLUDE[prod_short](includes/prod_short.md)] se proporcionan en dos tipos básicos: principal y configuración.</span><span class="sxs-lookup"><span data-stu-id="443d6-124">[!INCLUDE[prod_short](includes/prod_short.md)], data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="443d6-125">Cuando está estableciendo la configuración de una empresa, puede usar estos tipos para centrar la estrategia de configuración.</span><span class="sxs-lookup"><span data-stu-id="443d6-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="443d6-126">Tablas de datos maestros</span><span class="sxs-lookup"><span data-stu-id="443d6-126">Master Data Tables</span></span>  
<span data-ttu-id="443d6-127">En la tabla siguiente se enumeran todas las tablas de datos maestros.</span><span class="sxs-lookup"><span data-stu-id="443d6-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="443d6-128">Cuando se inicializa una nueva empresa, estas tablas están vacías.</span><span class="sxs-lookup"><span data-stu-id="443d6-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="443d6-129">Tabla nº</span><span class="sxs-lookup"><span data-stu-id="443d6-129">Table No.</span></span>|<span data-ttu-id="443d6-130">Nombre de tabla</span><span class="sxs-lookup"><span data-stu-id="443d6-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="443d6-131">15</span><span class="sxs-lookup"><span data-stu-id="443d6-131">15</span></span>|<span data-ttu-id="443d6-132">Cuenta</span><span class="sxs-lookup"><span data-stu-id="443d6-132">G/L Account</span></span>|  
|<span data-ttu-id="443d6-133">18</span><span class="sxs-lookup"><span data-stu-id="443d6-133">18</span></span>|<span data-ttu-id="443d6-134">Cliente</span><span class="sxs-lookup"><span data-stu-id="443d6-134">Customer</span></span>|  
|<span data-ttu-id="443d6-135">23</span><span class="sxs-lookup"><span data-stu-id="443d6-135">23</span></span>|<span data-ttu-id="443d6-136">Proveedor</span><span class="sxs-lookup"><span data-stu-id="443d6-136">Vendor</span></span>|  
|<span data-ttu-id="443d6-137">27</span><span class="sxs-lookup"><span data-stu-id="443d6-137">27</span></span>|<span data-ttu-id="443d6-138">Artículo</span><span class="sxs-lookup"><span data-stu-id="443d6-138">Item</span></span>|  
|<span data-ttu-id="443d6-139">5050</span><span class="sxs-lookup"><span data-stu-id="443d6-139">5050</span></span>|<span data-ttu-id="443d6-140">Contacto</span><span class="sxs-lookup"><span data-stu-id="443d6-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="443d6-141">Tablas de datos de configuración</span><span class="sxs-lookup"><span data-stu-id="443d6-141">Setup Data Tables</span></span>  
<span data-ttu-id="443d6-142">En la tabla siguiente se enumeran algunas tablas de datos de configuración, en las que se captura información de configuración en el cuestionario de configuración.</span><span class="sxs-lookup"><span data-stu-id="443d6-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="443d6-143">Estas tablas contienen información de línea en el momento de crear la empresa.</span><span class="sxs-lookup"><span data-stu-id="443d6-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="443d6-144">Tabla nº</span><span class="sxs-lookup"><span data-stu-id="443d6-144">Table No.</span></span>|<span data-ttu-id="443d6-145">Nombre de tabla</span><span class="sxs-lookup"><span data-stu-id="443d6-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="443d6-146">98</span><span class="sxs-lookup"><span data-stu-id="443d6-146">98</span></span>|<span data-ttu-id="443d6-147">Configuración de contabilidad</span><span class="sxs-lookup"><span data-stu-id="443d6-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="443d6-148">311</span><span class="sxs-lookup"><span data-stu-id="443d6-148">311</span></span>|<span data-ttu-id="443d6-149">Configuración de ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="443d6-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="443d6-150">312</span><span class="sxs-lookup"><span data-stu-id="443d6-150">312</span></span>|<span data-ttu-id="443d6-151">Configuración de compras y pagos</span><span class="sxs-lookup"><span data-stu-id="443d6-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="443d6-152">313</span><span class="sxs-lookup"><span data-stu-id="443d6-152">313</span></span>|<span data-ttu-id="443d6-153">Configuración de inventario</span><span class="sxs-lookup"><span data-stu-id="443d6-153">Inventory Setup</span></span>|  

<span data-ttu-id="443d6-154">Además de las tablas de datos de configuración, [!INCLUDE[prod_short](includes/prod_short.md)] también incluye tablas de datos de tipo de configuración que especifican información básica acerca de la empresa y sus procesos empresariales.</span><span class="sxs-lookup"><span data-stu-id="443d6-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="443d6-155">En la tabla siguiente aparecen algunos.</span><span class="sxs-lookup"><span data-stu-id="443d6-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="443d6-156">Tabla nº</span><span class="sxs-lookup"><span data-stu-id="443d6-156">Table No.</span></span>|<span data-ttu-id="443d6-157">Nombre de tabla</span><span class="sxs-lookup"><span data-stu-id="443d6-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="443d6-158">3</span><span class="sxs-lookup"><span data-stu-id="443d6-158">3</span></span>|<span data-ttu-id="443d6-159">Términos de pago</span><span class="sxs-lookup"><span data-stu-id="443d6-159">Payment Terms</span></span>|  
|<span data-ttu-id="443d6-160">4</span><span class="sxs-lookup"><span data-stu-id="443d6-160">4</span></span>|<span data-ttu-id="443d6-161">Divisa</span><span class="sxs-lookup"><span data-stu-id="443d6-161">Currency</span></span>|  
|<span data-ttu-id="443d6-162">6</span><span class="sxs-lookup"><span data-stu-id="443d6-162">6</span></span>|<span data-ttu-id="443d6-163">Grupos precio cliente</span><span class="sxs-lookup"><span data-stu-id="443d6-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="443d6-164">5700</span><span class="sxs-lookup"><span data-stu-id="443d6-164">5700</span></span>|<span data-ttu-id="443d6-165">Ud. de almacenam.</span><span class="sxs-lookup"><span data-stu-id="443d6-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="443d6-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="443d6-166">See Also</span></span>  
[<span data-ttu-id="443d6-167">Aplicar la configuración a nuevas empresas</span><span class="sxs-lookup"><span data-stu-id="443d6-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="443d6-168">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="443d6-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="443d6-169">Administración</span><span class="sxs-lookup"><span data-stu-id="443d6-169">Administration</span></span>](admin-setup-and-administration.md)
