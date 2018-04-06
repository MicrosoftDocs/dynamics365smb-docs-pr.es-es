---
title: Usar Excel para importar datos en Financials | Documentos de Microsoft
description: "Utilice el paquete de configuración predeterminado para agregar datos de cliente en Excel e importar los datos en Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="bed1f-103">Importar datos del software de contabilidad heredado mediante un paquete de configuración</span><span class="sxs-lookup"><span data-stu-id="bed1f-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="bed1f-104">Puede importar datos maestros y algunos datos transaccionales de otros sistemas de financieros mediante el paquete de configuración predeterminado en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bed1f-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bed1f-105">En la ventana **Paquetes de configuración** puede trabajar con el paquete para importar y validar los datos antes de aplicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="bed1f-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="bed1f-106">Los paquetes de configuración son parte de RapidStart Services para [!INCLUDE[d365fin](includes/d365fin_md.md)], un conjunto de herramientas extenso para configurar nuevas soluciones basadas en los requisitos comerciales de los clientes y los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="bed1f-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="bed1f-107">RapidStart Services también ofrece la funcionalidad de importar los datos heredados.</span><span class="sxs-lookup"><span data-stu-id="bed1f-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="bed1f-108">Para obtener más información, consulte [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="bed1f-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="bed1f-109">Opcionalmente, utilice asistentes de migración para importar datos de QuickBooks GP o Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="bed1f-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="bed1f-110">Para obtener más información, consulte [Migración de datos de QuickBooks](ui-extensions-quickbooks-data-migration.md) o [Migración de datos de Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="bed1f-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="bed1f-111">Trabajar con datos en Excel</span><span class="sxs-lookup"><span data-stu-id="bed1f-111">Working with Data in Excel</span></span>
<span data-ttu-id="bed1f-112">Al exportar el paquete de configuración predeterminado a Excel, el libro generado contiene una hoja de trabajo para cada tabla del paquete.</span><span class="sxs-lookup"><span data-stu-id="bed1f-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="bed1f-113">Para simplificar sus tareas, puede aprovechar las herramientas de manipulación de XML que se integran en Excel.</span><span class="sxs-lookup"><span data-stu-id="bed1f-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="bed1f-114">También puede utilizar las funciones integradas de Excel para ayudar con el formato de datos y para colocar los datos en la celda correcta.</span><span class="sxs-lookup"><span data-stu-id="bed1f-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="bed1f-115">Por ejemplo, agregue una hoja de cálculo en blanco y copie los datos heredados en ella.</span><span class="sxs-lookup"><span data-stu-id="bed1f-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="bed1f-116">A continuación, cree una fórmula de Excel para asignar datos en la hoja de cálculo de transformación entre los campos en la hoja de cálculo exportada y los datos heredados del cliente.</span><span class="sxs-lookup"><span data-stu-id="bed1f-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="bed1f-117">Después de asignar todos los datos, copie el intervalo de datos en la hoja de cálculo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bed1f-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="bed1f-118">No cambie las columnas en las hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="bed1f-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="bed1f-119">Si se mueven, modifican o eliminan, la hoja de cálculo no podrá importarse a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bed1f-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="bed1f-120">Tablas del paquete de configuración predeterminado</span><span class="sxs-lookup"><span data-stu-id="bed1f-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="bed1f-121">El paquete de configuración predeterminado admite las tablas siguientes:</span><span class="sxs-lookup"><span data-stu-id="bed1f-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="bed1f-122">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="bed1f-122">Payment Terms</span></span>
-   <span data-ttu-id="bed1f-123">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="bed1f-123">Customer Price Group</span></span>
-   <span data-ttu-id="bed1f-124">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="bed1f-124">Shipment Method</span></span>
-   <span data-ttu-id="bed1f-125">Vendedor/Comprador</span><span class="sxs-lookup"><span data-stu-id="bed1f-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="bed1f-126">Lugar</span><span class="sxs-lookup"><span data-stu-id="bed1f-126">Location</span></span>
-   <span data-ttu-id="bed1f-127">Cuenta</span><span class="sxs-lookup"><span data-stu-id="bed1f-127">GL Account</span></span>
-   <span data-ttu-id="bed1f-128">Cliente</span><span class="sxs-lookup"><span data-stu-id="bed1f-128">Customer</span></span>
-   <span data-ttu-id="bed1f-129">Proveedor</span><span class="sxs-lookup"><span data-stu-id="bed1f-129">Vendor</span></span>
-   <span data-ttu-id="bed1f-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="bed1f-130">Item</span></span>
-   <span data-ttu-id="bed1f-131">Cab. venta</span><span class="sxs-lookup"><span data-stu-id="bed1f-131">Sales Header</span></span>
-   <span data-ttu-id="bed1f-132">Lín. venta</span><span class="sxs-lookup"><span data-stu-id="bed1f-132">Sales Line</span></span>
-   <span data-ttu-id="bed1f-133">Cab. compra</span><span class="sxs-lookup"><span data-stu-id="bed1f-133">Purchase Header</span></span>
-   <span data-ttu-id="bed1f-134">Lín. compra</span><span class="sxs-lookup"><span data-stu-id="bed1f-134">Purchase Line</span></span>
-   <span data-ttu-id="bed1f-135">Lín. diario general</span><span class="sxs-lookup"><span data-stu-id="bed1f-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="bed1f-136">Lín. diario producto</span><span class="sxs-lookup"><span data-stu-id="bed1f-136">Item Journal Line</span></span>
-   <span data-ttu-id="bed1f-137">Grupo contable cliente</span><span class="sxs-lookup"><span data-stu-id="bed1f-137">Customer Posting Group</span></span>
-   <span data-ttu-id="bed1f-138">Grupo contable proveedor</span><span class="sxs-lookup"><span data-stu-id="bed1f-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="bed1f-139">Grupo contable inventario</span><span class="sxs-lookup"><span data-stu-id="bed1f-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="bed1f-140">Unidad de medida</span><span class="sxs-lookup"><span data-stu-id="bed1f-140">Unit of Measure</span></span>
-   <span data-ttu-id="bed1f-141">Gr. contable negocio</span><span class="sxs-lookup"><span data-stu-id="bed1f-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="bed1f-142">Gr. contable producto</span><span class="sxs-lookup"><span data-stu-id="bed1f-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="bed1f-143">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="bed1f-143">General Posting Setup</span></span>
-   <span data-ttu-id="bed1f-144">Territorio</span><span class="sxs-lookup"><span data-stu-id="bed1f-144">Territory</span></span>
-   <span data-ttu-id="bed1f-145">Categoría producto</span><span class="sxs-lookup"><span data-stu-id="bed1f-145">Item Category</span></span>
-   <span data-ttu-id="bed1f-146">Precio venta</span><span class="sxs-lookup"><span data-stu-id="bed1f-146">Sales Price</span></span>
-   <span data-ttu-id="bed1f-147">Precio compra</span><span class="sxs-lookup"><span data-stu-id="bed1f-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="bed1f-148">Importar datos de cliente</span><span class="sxs-lookup"><span data-stu-id="bed1f-148">Importing Customer Data</span></span>
<span data-ttu-id="bed1f-149">Después de que los datos del cliente se hayan introducido en Excel, importe los datos a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bed1f-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bed1f-150">En la ventana **Paquetes de configuración**, se importan los datos del archivo de Excel y puede validar que los datos sean coherentes con [!INCLUDE[d365fin](includes/d365fin_md.md)] antes de aplicar el paquete.</span><span class="sxs-lookup"><span data-stu-id="bed1f-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="bed1f-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bed1f-151">See Also</span></span>
[<span data-ttu-id="bed1f-152">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="bed1f-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="bed1f-153">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="bed1f-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="bed1f-154">Migración de datos de QuickBooks</span><span class="sxs-lookup"><span data-stu-id="bed1f-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="bed1f-155">Migración de datos de Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="bed1f-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

