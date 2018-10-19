---
title: "Usar la extensión de migración de datos C5 | Documentos de Microsoft"
description: "Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="e5b8c-103">Extensión de migración de datos de C5</span><span class="sxs-lookup"><span data-stu-id="e5b8c-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="e5b8c-104">Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e5b8c-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e5b8c-105">También puede migrar los movimientos históricos para cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="e5b8c-106">La empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] no debe contener ningún dato.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="e5b8c-107">Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="e5b8c-108">¿Qué datos se migran?</span><span class="sxs-lookup"><span data-stu-id="e5b8c-108">What Data is Migrated?</span></span>
<span data-ttu-id="e5b8c-109">Se migran los datos siguientes para cada entidad:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="e5b8c-110">**Clientes**</span><span class="sxs-lookup"><span data-stu-id="e5b8c-110">**Customers**</span></span>
* <span data-ttu-id="e5b8c-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-111">Contacts</span></span>  
* <span data-ttu-id="e5b8c-112">Lugar</span><span class="sxs-lookup"><span data-stu-id="e5b8c-112">Location</span></span>
* <span data-ttu-id="e5b8c-113">País</span><span class="sxs-lookup"><span data-stu-id="e5b8c-113">Country</span></span>
* <span data-ttu-id="e5b8c-114">Dimensiones de cliente (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e5b8c-115">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="e5b8c-115">Shipment method</span></span>
* <span data-ttu-id="e5b8c-116">Vendedor</span><span class="sxs-lookup"><span data-stu-id="e5b8c-116">Sales Person</span></span>
* <span data-ttu-id="e5b8c-117">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="e5b8c-117">Payment terms</span></span>
* <span data-ttu-id="e5b8c-118">Forma pago</span><span class="sxs-lookup"><span data-stu-id="e5b8c-118">Payment method</span></span>
* <span data-ttu-id="e5b8c-119">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-119">Customer price group</span></span>
* <span data-ttu-id="e5b8c-120">Descuento de la factura del cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-120">Customer invoice discount</span></span>

<span data-ttu-id="e5b8c-121">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e5b8c-122">Configuración contable cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-122">Customer posting setup</span></span>
* <span data-ttu-id="e5b8c-123">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="e5b8c-123">General journal batch</span></span>
* <span data-ttu-id="e5b8c-124">Transacciones abiertas (movimientos de cliente)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="e5b8c-125">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="e5b8c-125">**Vendors**</span></span>
* <span data-ttu-id="e5b8c-126">Contactos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-126">Contacts</span></span>
* <span data-ttu-id="e5b8c-127">Lugar</span><span class="sxs-lookup"><span data-stu-id="e5b8c-127">Location</span></span>
* <span data-ttu-id="e5b8c-128">País</span><span class="sxs-lookup"><span data-stu-id="e5b8c-128">Country</span></span>
* <span data-ttu-id="e5b8c-129">Dimensiones de proveedor (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e5b8c-130">Descuento en factura</span><span class="sxs-lookup"><span data-stu-id="e5b8c-130">Invoice discount</span></span>
* <span data-ttu-id="e5b8c-131">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="e5b8c-131">Shipment method</span></span>
* <span data-ttu-id="e5b8c-132">Comprador</span><span class="sxs-lookup"><span data-stu-id="e5b8c-132">Purchaser</span></span>
* <span data-ttu-id="e5b8c-133">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="e5b8c-133">Payment terms</span></span>
* <span data-ttu-id="e5b8c-134">Forma pago</span><span class="sxs-lookup"><span data-stu-id="e5b8c-134">Payment method</span></span>
* <span data-ttu-id="e5b8c-135">Descuento de factura del proveedor</span><span class="sxs-lookup"><span data-stu-id="e5b8c-135">Vendor invoice discount</span></span>

<span data-ttu-id="e5b8c-136">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e5b8c-137">Configuración contable proveedor</span><span class="sxs-lookup"><span data-stu-id="e5b8c-137">Vendor posting setup</span></span>
* <span data-ttu-id="e5b8c-138">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="e5b8c-138">General journal batch</span></span>
* <span data-ttu-id="e5b8c-139">Abra transacciones (movimientos de proveedores)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="e5b8c-140">**Productos**</span><span class="sxs-lookup"><span data-stu-id="e5b8c-140">**Items**</span></span>
* <span data-ttu-id="e5b8c-141">Lugar</span><span class="sxs-lookup"><span data-stu-id="e5b8c-141">Location</span></span>
* <span data-ttu-id="e5b8c-142">País</span><span class="sxs-lookup"><span data-stu-id="e5b8c-142">Country</span></span>
* <span data-ttu-id="e5b8c-143">Dimensiones de producto (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="e5b8c-144">Descuentos línea de ventas</span><span class="sxs-lookup"><span data-stu-id="e5b8c-144">Sales line discounts</span></span>
* <span data-ttu-id="e5b8c-145">Grupos descuento cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-145">Customer discount groups</span></span>
* <span data-ttu-id="e5b8c-146">Grupos descuento productos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-146">Item discount groups</span></span>
* <span data-ttu-id="e5b8c-147">Precio venta</span><span class="sxs-lookup"><span data-stu-id="e5b8c-147">Sales price</span></span>
* <span data-ttu-id="e5b8c-148">Código arancelario</span><span class="sxs-lookup"><span data-stu-id="e5b8c-148">Tariff number</span></span>
* <span data-ttu-id="e5b8c-149">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="e5b8c-149">Units of measure</span></span>
* <span data-ttu-id="e5b8c-150">Código seguimiento producto</span><span class="sxs-lookup"><span data-stu-id="e5b8c-150">Item tracking code</span></span>
* <span data-ttu-id="e5b8c-151">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-151">Customer price group</span></span>
* <span data-ttu-id="e5b8c-152">L.M. de ensamblado</span><span class="sxs-lookup"><span data-stu-id="e5b8c-152">Assembly BOMs</span></span>

<span data-ttu-id="e5b8c-153">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="e5b8c-154">Configuración contable inventario</span><span class="sxs-lookup"><span data-stu-id="e5b8c-154">Inventory posting setup</span></span>
* <span data-ttu-id="e5b8c-155">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="e5b8c-155">General posting setup</span></span>
* <span data-ttu-id="e5b8c-156">Sección diario producto</span><span class="sxs-lookup"><span data-stu-id="e5b8c-156">Item journal batch</span></span>
* <span data-ttu-id="e5b8c-157">Abra transacciones (movimientos de productos)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="e5b8c-158">Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="e5b8c-159">Otros tipos de cambio no se migran.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="e5b8c-160">**Plan de cuentas**</span><span class="sxs-lookup"><span data-stu-id="e5b8c-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="e5b8c-161">Dimensiones estándar: departamento, centro de coste, propósito</span><span class="sxs-lookup"><span data-stu-id="e5b8c-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="e5b8c-162">Transacciones históricas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="e5b8c-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="e5b8c-163">Las transacciones históricas de contabilidad se gestionan de un modo un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="e5b8c-164">Al migrar datos se establece un parámetro **Periodo actual**.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="e5b8c-165">Este parámetro especifica cómo procesar transacciones de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="e5b8c-166">Las transacciones después de esta fecha se migran por separado.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="e5b8c-167">Las transacciones anteriores a esta fecha se agregan por cuenta y se migran como un único importe.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="e5b8c-168">Por ejemplo, supongamos que hay transacciones en 2015, 2016, 2017 y 2018, y especifica el 1 de enero de 2017 en el campo Período actual.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="e5b8c-169">Para cada cuenta, los importes de las transacciones del 31 de diciembre de 2016 o anteriores se agregarán en una sola línea de diario general para cada cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="e5b8c-170">Todas las transacciones después de esta fecha se migrarán por separado.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="e5b8c-171">Para migrar datos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-171">To migrate data</span></span>
<span data-ttu-id="e5b8c-172">Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="e5b8c-173">En la C5, utilice la función **Base de datos de exportación** para exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="e5b8c-174">Envíe la carpeta de exportación a una carpeta comprimida.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="e5b8c-175">En [!INCLUDE[d365fin](includes/d365fin_md.md)], elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Migración de datos** y luego elija **Migración de datos**.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="e5b8c-176">Complete los pasos de la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="e5b8c-177">Asegúrese de elegir **Importar de Microsoft Dynamcis C5 2012** como origen de datos.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="e5b8c-178">Las empresas a menudo agregan campos para personalizar la C5 para su línea de negocio específica.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e5b8c-179">no migra datos de campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="e5b8c-180">Además, la migración dará error si tiene más de 10 campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="e5b8c-181">Ver el estado de la migración</span><span class="sxs-lookup"><span data-stu-id="e5b8c-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="e5b8c-182">Utilice la ventana **Información general sobre migración de datos** para controlar el éxito de la migración.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="e5b8c-183">La página muestra información como el número de entidades que la migración incluirá, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="e5b8c-184">También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="e5b8c-185">Para obtener más información, consulte la siguiente sección de este tema.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="e5b8c-186">Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="e5b8c-187">Cómo evitar el doble registro</span><span class="sxs-lookup"><span data-stu-id="e5b8c-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="e5b8c-188">Para ayudar a evitar el registro doble en la contabilidad, se utilizan las siguientes cuentas de saldo para las transacciones abiertas:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="e5b8c-189">Para los proveedores, usamos la cuenta de A/P del grupo de publicación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="e5b8c-190">Para los clientes, usamos la cuenta de A/R del grupo de publicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="e5b8c-191">Para los elementos, creamos una configuración general de contabilización donde la cuenta de ajuste es la cuenta especificada como cuenta de inventario en la configuración de contabilización del inventario.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="e5b8c-192">Corrección de errores</span><span class="sxs-lookup"><span data-stu-id="e5b8c-192">Correcting Errors</span></span>
<span data-ttu-id="e5b8c-193">Si algo sale mal y se produce un error, el campo **Estado** mostrará **Completado con errores** y el campo **Recuento de errores** mostrará cuántos.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="e5b8c-194">Para ver una lista de los errores, puede abrir la ventana **Errores de migración de datos** si elige:</span><span class="sxs-lookup"><span data-stu-id="e5b8c-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="e5b8c-195">El número en el campo **Recuento de errores** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="e5b8c-196">La entidad y la acción **Mostrar errores**.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="e5b8c-197">En la ventana **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para ver los datos migrados de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="e5b8c-198">Si tiene varios errores a corregir, puede elegir **Corrección masiva de errores** para modificar las entidades de una lista.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="e5b8c-199">Aún así, debe abrir registros individuales si el error lo causó una entrada relacionada.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="e5b8c-200">Por ejemplo, un proveedor no se migrará si una dirección de correo electrónico a uno de sus contactos tiene un formato no válido.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="e5b8c-201">Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que reparó, sin tener que reiniciar por completo la migración.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="e5b8c-202">Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="e5b8c-203">De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="e5b8c-204">Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="e5b8c-205">Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="e5b8c-206">Comprobar datos después de migrar</span><span class="sxs-lookup"><span data-stu-id="e5b8c-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="e5b8c-207">Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e5b8c-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="e5b8c-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="e5b8c-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="e5b8c-209">Trabajo por lotes para utilizar</span><span class="sxs-lookup"><span data-stu-id="e5b8c-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="e5b8c-210">Movimientos de cliente</span><span class="sxs-lookup"><span data-stu-id="e5b8c-210">Customer Entries</span></span>| <span data-ttu-id="e5b8c-211">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="e5b8c-211">General Journals</span></span>| <span data-ttu-id="e5b8c-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="e5b8c-212">CUSTMIGR</span></span> |
|<span data-ttu-id="e5b8c-213">Movimientos de proveedor</span><span class="sxs-lookup"><span data-stu-id="e5b8c-213">Vendor Entries</span></span>| <span data-ttu-id="e5b8c-214">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="e5b8c-214">General Journals</span></span>| <span data-ttu-id="e5b8c-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="e5b8c-215">VENDMIGR</span></span>|
|<span data-ttu-id="e5b8c-216">Movs. prods.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-216">Item Entries</span></span>| <span data-ttu-id="e5b8c-217">Diarios de productos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-217">Item Journals</span></span>| <span data-ttu-id="e5b8c-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="e5b8c-218">ITEMMIGR</span></span> |
|<span data-ttu-id="e5b8c-219">Movimientos de contabilidad</span><span class="sxs-lookup"><span data-stu-id="e5b8c-219">G/L Entries</span></span>| <span data-ttu-id="e5b8c-220">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="e5b8c-220">General Journals</span></span>| <span data-ttu-id="e5b8c-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="e5b8c-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="e5b8c-222">Detener la migración de datos</span><span class="sxs-lookup"><span data-stu-id="e5b8c-222">Stopping Data Migration</span></span>
<span data-ttu-id="e5b8c-223">Puede detener la migración de datos con la opción **Detener todas las migraciones**.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="e5b8c-224">Si utiliza esta opción, todas las migraciones pendientes también se detendrán.</span><span class="sxs-lookup"><span data-stu-id="e5b8c-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5b8c-225">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e5b8c-225">See Also</span></span>
<span data-ttu-id="e5b8c-226">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e5b8c-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e5b8c-227">Introducción</span><span class="sxs-lookup"><span data-stu-id="e5b8c-227">Getting Started</span></span>](product-get-started.md)

