---
title: Usar la extensión de migración de datos C5 | Documentos de Microsoft
description: Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Business Central.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: c8eba304746125e9262ebfff95cfd2379eec08c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311337"
---
# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="edc68-103">Extensión de migración de datos de C5</span><span class="sxs-lookup"><span data-stu-id="edc68-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="edc68-104">Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="edc68-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="edc68-105">También puede migrar los movimientos históricos para cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="edc68-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="edc68-106">La empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] no debe contener ningún dato.</span><span class="sxs-lookup"><span data-stu-id="edc68-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="edc68-107">Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.</span><span class="sxs-lookup"><span data-stu-id="edc68-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="edc68-108">¿Qué datos se migran?</span><span class="sxs-lookup"><span data-stu-id="edc68-108">What Data is Migrated?</span></span>
<span data-ttu-id="edc68-109">Se migran los datos siguientes para cada entidad:</span><span class="sxs-lookup"><span data-stu-id="edc68-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="edc68-110">**Clientes**</span><span class="sxs-lookup"><span data-stu-id="edc68-110">**Customers**</span></span>
* <span data-ttu-id="edc68-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="edc68-111">Contacts</span></span>  
* <span data-ttu-id="edc68-112">Lugar</span><span class="sxs-lookup"><span data-stu-id="edc68-112">Location</span></span>
* <span data-ttu-id="edc68-113">País</span><span class="sxs-lookup"><span data-stu-id="edc68-113">Country</span></span>
* <span data-ttu-id="edc68-114">Dimensiones de cliente (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="edc68-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="edc68-115">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="edc68-115">Shipment method</span></span>
* <span data-ttu-id="edc68-116">Vendedor</span><span class="sxs-lookup"><span data-stu-id="edc68-116">Sales Person</span></span>
* <span data-ttu-id="edc68-117">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="edc68-117">Payment terms</span></span>
* <span data-ttu-id="edc68-118">Forma pago</span><span class="sxs-lookup"><span data-stu-id="edc68-118">Payment method</span></span>
* <span data-ttu-id="edc68-119">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-119">Customer price group</span></span>
* <span data-ttu-id="edc68-120">Descuento de la factura del cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-120">Customer invoice discount</span></span>

<span data-ttu-id="edc68-121">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="edc68-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="edc68-122">Configuración contable cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-122">Customer posting setup</span></span>
* <span data-ttu-id="edc68-123">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="edc68-123">General journal batch</span></span>
* <span data-ttu-id="edc68-124">Transacciones abiertas (movimientos de cliente)</span><span class="sxs-lookup"><span data-stu-id="edc68-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="edc68-125">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="edc68-125">**Vendors**</span></span>
* <span data-ttu-id="edc68-126">Contactos</span><span class="sxs-lookup"><span data-stu-id="edc68-126">Contacts</span></span>
* <span data-ttu-id="edc68-127">Lugar</span><span class="sxs-lookup"><span data-stu-id="edc68-127">Location</span></span>
* <span data-ttu-id="edc68-128">País</span><span class="sxs-lookup"><span data-stu-id="edc68-128">Country</span></span>
* <span data-ttu-id="edc68-129">Dimensiones de proveedor (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="edc68-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="edc68-130">Descuento en factura</span><span class="sxs-lookup"><span data-stu-id="edc68-130">Invoice discount</span></span>
* <span data-ttu-id="edc68-131">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="edc68-131">Shipment method</span></span>
* <span data-ttu-id="edc68-132">Comprador</span><span class="sxs-lookup"><span data-stu-id="edc68-132">Purchaser</span></span>
* <span data-ttu-id="edc68-133">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="edc68-133">Payment terms</span></span>
* <span data-ttu-id="edc68-134">Forma pago</span><span class="sxs-lookup"><span data-stu-id="edc68-134">Payment method</span></span>
* <span data-ttu-id="edc68-135">Descuento de factura del proveedor</span><span class="sxs-lookup"><span data-stu-id="edc68-135">Vendor invoice discount</span></span>

<span data-ttu-id="edc68-136">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="edc68-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="edc68-137">Configuración contable proveedor</span><span class="sxs-lookup"><span data-stu-id="edc68-137">Vendor posting setup</span></span>
* <span data-ttu-id="edc68-138">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="edc68-138">General journal batch</span></span>
* <span data-ttu-id="edc68-139">Abra transacciones (movimientos de proveedores)</span><span class="sxs-lookup"><span data-stu-id="edc68-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="edc68-140">**Productos**</span><span class="sxs-lookup"><span data-stu-id="edc68-140">**Items**</span></span>
* <span data-ttu-id="edc68-141">Lugar</span><span class="sxs-lookup"><span data-stu-id="edc68-141">Location</span></span>
* <span data-ttu-id="edc68-142">País</span><span class="sxs-lookup"><span data-stu-id="edc68-142">Country</span></span>
* <span data-ttu-id="edc68-143">Dimensiones de producto (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="edc68-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="edc68-144">Descuentos línea de ventas</span><span class="sxs-lookup"><span data-stu-id="edc68-144">Sales line discounts</span></span>
* <span data-ttu-id="edc68-145">Grupos descuento cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-145">Customer discount groups</span></span>
* <span data-ttu-id="edc68-146">Grupos descuento productos</span><span class="sxs-lookup"><span data-stu-id="edc68-146">Item discount groups</span></span>
* <span data-ttu-id="edc68-147">Precio venta</span><span class="sxs-lookup"><span data-stu-id="edc68-147">Sales price</span></span>
* <span data-ttu-id="edc68-148">Código arancelario</span><span class="sxs-lookup"><span data-stu-id="edc68-148">Tariff number</span></span>
* <span data-ttu-id="edc68-149">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="edc68-149">Units of measure</span></span>
* <span data-ttu-id="edc68-150">Código seguimiento producto</span><span class="sxs-lookup"><span data-stu-id="edc68-150">Item tracking code</span></span>
* <span data-ttu-id="edc68-151">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-151">Customer price group</span></span>
* <span data-ttu-id="edc68-152">L.M. de ensamblado</span><span class="sxs-lookup"><span data-stu-id="edc68-152">Assembly BOMs</span></span>

<span data-ttu-id="edc68-153">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="edc68-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="edc68-154">Configuración contable inventario</span><span class="sxs-lookup"><span data-stu-id="edc68-154">Inventory posting setup</span></span>
* <span data-ttu-id="edc68-155">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="edc68-155">General posting setup</span></span>
* <span data-ttu-id="edc68-156">Sección diario producto</span><span class="sxs-lookup"><span data-stu-id="edc68-156">Item journal batch</span></span>
* <span data-ttu-id="edc68-157">Abra transacciones (movimientos de productos)</span><span class="sxs-lookup"><span data-stu-id="edc68-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="edc68-158">Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran.</span><span class="sxs-lookup"><span data-stu-id="edc68-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="edc68-159">Otros tipos de cambio no se migran.</span><span class="sxs-lookup"><span data-stu-id="edc68-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="edc68-160">**Plan de cuentas**</span><span class="sxs-lookup"><span data-stu-id="edc68-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="edc68-161">Dimensiones estándar: departamento, centro de coste, propósito</span><span class="sxs-lookup"><span data-stu-id="edc68-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="edc68-162">Transacciones históricas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="edc68-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="edc68-163">Las transacciones históricas de contabilidad se gestionan de un modo un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="edc68-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="edc68-164">Al migrar datos se establece un parámetro **Periodo actual**.</span><span class="sxs-lookup"><span data-stu-id="edc68-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="edc68-165">Este parámetro especifica cómo procesar transacciones de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="edc68-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="edc68-166">Las transacciones después de esta fecha se migran por separado.</span><span class="sxs-lookup"><span data-stu-id="edc68-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="edc68-167">Las transacciones anteriores a esta fecha se agregan por cuenta y se migran como un único importe.</span><span class="sxs-lookup"><span data-stu-id="edc68-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="edc68-168">Por ejemplo, supongamos que hay transacciones en 2015, 2016, 2017 y 2018, y especifica el 1 de enero de 2017 en el campo Período actual.</span><span class="sxs-lookup"><span data-stu-id="edc68-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="edc68-169">Para cada cuenta, los importes de las transacciones del 31 de diciembre de 2106 o anteriores se agregarán en una sola línea de diario general para cada cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="edc68-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="edc68-170">Todas las transacciones después de esta fecha se migrarán por separado.</span><span class="sxs-lookup"><span data-stu-id="edc68-170">All trascations after this date will be migrated individually.</span></span>

## <a name="file-size-requirements"></a><span data-ttu-id="edc68-171">Requisitos de tamaño del archivo</span><span class="sxs-lookup"><span data-stu-id="edc68-171">File Size Requirements</span></span>
<span data-ttu-id="edc68-172">El tamaño máximo del archivo que puede descargar en [!INCLUDE[d365fin](includes/d365fin_md.md)] es de 150 MB.</span><span class="sxs-lookup"><span data-stu-id="edc68-172">The largest file size you can upload to [!INCLUDE[d365fin](includes/d365fin_md.md)] is 150 MB.</span></span> <span data-ttu-id="edc68-173">Si el archivo que se exporta de C5 es más grande, tenga en cuenta migrar datos en varios archivos.</span><span class="sxs-lookup"><span data-stu-id="edc68-173">If the file you export from C5 is larger than that, consider migrating data in multiple files.</span></span> <span data-ttu-id="edc68-174">Por ejemplo, exporte uno o dos tipos de entidades de C5, como clientes y proveedores, a un archivo y luego exporte los elementos a otro archivo, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="edc68-174">For example, export one or two types of entities from C5, such as customers and vendors, to a file, and then export items to another file, and so on.</span></span> <span data-ttu-id="edc68-175">Puede importar archivos individualmente en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="edc68-175">You can import files individually in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="edc68-176">Para migrar datos</span><span class="sxs-lookup"><span data-stu-id="edc68-176">To migrate data</span></span>
<span data-ttu-id="edc68-177">Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="edc68-177">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="edc68-178">En la C5, utilice la función **Base de datos de exportación** para exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="edc68-178">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="edc68-179">Envíe la carpeta de exportación a una carpeta comprimida.</span><span class="sxs-lookup"><span data-stu-id="edc68-179">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="edc68-180">En [!INCLUDE[d365fin](includes/d365fin_md.md)], elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Migración de datos** y luego elija **Migración de datos**.</span><span class="sxs-lookup"><span data-stu-id="edc68-180">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="edc68-181">Complete los pasos de la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="edc68-181">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="edc68-182">Asegúrese de elegir **Importar de Microsoft Dynamcis C5 2012** como origen de datos.</span><span class="sxs-lookup"><span data-stu-id="edc68-182">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="edc68-183">Ver el estado de la migración</span><span class="sxs-lookup"><span data-stu-id="edc68-183">Viewing the Status of the Migration</span></span>
<span data-ttu-id="edc68-184">Utilice la página **Información general sobre migración de datos** para controlar el éxito de la migración.</span><span class="sxs-lookup"><span data-stu-id="edc68-184">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="edc68-185">La página muestra información como el número de entidades que la migración incluirá, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="edc68-185">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="edc68-186">También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas.</span><span class="sxs-lookup"><span data-stu-id="edc68-186">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="edc68-187">Para obtener más información, consulte la siguiente sección de este tema.</span><span class="sxs-lookup"><span data-stu-id="edc68-187">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="edc68-188">Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="edc68-188">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="edc68-189">Cómo evitar el doble registro</span><span class="sxs-lookup"><span data-stu-id="edc68-189">How to Avoid Double-Posting</span></span>
<span data-ttu-id="edc68-190">Para ayudar a evitar el registro doble en la contabilidad, se utilizan las siguientes cuentas de saldo para las transacciones abiertas:</span><span class="sxs-lookup"><span data-stu-id="edc68-190">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="edc68-191">Para los proveedores, usamos la cuenta de A/P del grupo de publicación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="edc68-191">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="edc68-192">Para los clientes, usamos la cuenta de A/R del grupo de publicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="edc68-192">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="edc68-193">Para los elementos, creamos una configuración general de contabilización donde la cuenta de ajuste es la cuenta especificada como cuenta de inventario en la configuración de contabilización del inventario.</span><span class="sxs-lookup"><span data-stu-id="edc68-193">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="edc68-194">Corrección de errores</span><span class="sxs-lookup"><span data-stu-id="edc68-194">Correcting Errors</span></span>
<span data-ttu-id="edc68-195">Si algo sale mal y se produce un error, el campo **Estado** mostrará **Completado con errores** y el campo **Recuento de errores** mostrará cuántos.</span><span class="sxs-lookup"><span data-stu-id="edc68-195">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="edc68-196">Para ver una lista de los errores, puede abrir la página **Errores de migración de datos** si elige:</span><span class="sxs-lookup"><span data-stu-id="edc68-196">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="edc68-197">El número en el campo **Recuento de errores** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="edc68-197">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="edc68-198">La entidad y la acción **Mostrar errores**.</span><span class="sxs-lookup"><span data-stu-id="edc68-198">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="edc68-199">En la página **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para ver los datos migrados de la entidad.</span><span class="sxs-lookup"><span data-stu-id="edc68-199">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="edc68-200">Si tiene varios errores a corregir, puede elegir **Corrección masiva de errores** para modificar las entidades de una lista.</span><span class="sxs-lookup"><span data-stu-id="edc68-200">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="edc68-201">Aún así, debe abrir registros individuales si el error lo causó una entrada relacionada.</span><span class="sxs-lookup"><span data-stu-id="edc68-201">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="edc68-202">Por ejemplo, un proveedor no se migrará si una dirección de correo electrónico a uno de sus contactos tiene un formato no válido.</span><span class="sxs-lookup"><span data-stu-id="edc68-202">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="edc68-203">Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que reparó, sin tener que reiniciar por completo la migración.</span><span class="sxs-lookup"><span data-stu-id="edc68-203">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="edc68-204">Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar.</span><span class="sxs-lookup"><span data-stu-id="edc68-204">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="edc68-205">De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.</span><span class="sxs-lookup"><span data-stu-id="edc68-205">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="edc68-206">Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="edc68-206">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="edc68-207">Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="edc68-207">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="edc68-208">Comprobar datos después de migrar</span><span class="sxs-lookup"><span data-stu-id="edc68-208">Verifying Data After Migrating</span></span>
<span data-ttu-id="edc68-209">Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="edc68-209">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="edc68-210">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="edc68-210">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="edc68-211">Trabajo por lotes para utilizar</span><span class="sxs-lookup"><span data-stu-id="edc68-211">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="edc68-212">Movimientos de cliente</span><span class="sxs-lookup"><span data-stu-id="edc68-212">Customer Entries</span></span>| <span data-ttu-id="edc68-213">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="edc68-213">General Journals</span></span>| <span data-ttu-id="edc68-214">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="edc68-214">CUSTMIGR</span></span> |
|<span data-ttu-id="edc68-215">Movimientos de proveedor</span><span class="sxs-lookup"><span data-stu-id="edc68-215">Vendor Entries</span></span>| <span data-ttu-id="edc68-216">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="edc68-216">General Journals</span></span>| <span data-ttu-id="edc68-217">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="edc68-217">VENDMIGR</span></span>|
|<span data-ttu-id="edc68-218">Movs. prods.</span><span class="sxs-lookup"><span data-stu-id="edc68-218">Item Entries</span></span>| <span data-ttu-id="edc68-219">Diarios de productos</span><span class="sxs-lookup"><span data-stu-id="edc68-219">Item Journals</span></span>| <span data-ttu-id="edc68-220">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="edc68-220">ITEMMIGR</span></span> |
|<span data-ttu-id="edc68-221">Movimientos de contabilidad</span><span class="sxs-lookup"><span data-stu-id="edc68-221">G/L Entries</span></span>| <span data-ttu-id="edc68-222">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="edc68-222">General Journals</span></span>| <span data-ttu-id="edc68-223">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="edc68-223">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="edc68-224">Detener la migración de datos</span><span class="sxs-lookup"><span data-stu-id="edc68-224">Stopping Data Migration</span></span>
<span data-ttu-id="edc68-225">Puede detener la migración de datos con la opción **Detener todas las migraciones**.</span><span class="sxs-lookup"><span data-stu-id="edc68-225">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="edc68-226">Si utiliza esta opción, todas las migraciones pendientes también se detendrán.</span><span class="sxs-lookup"><span data-stu-id="edc68-226">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="edc68-227">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edc68-227">See Also</span></span>
<span data-ttu-id="edc68-228">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="edc68-228">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="edc68-229">Introducción</span><span class="sxs-lookup"><span data-stu-id="edc68-229">Getting Started</span></span>](product-get-started.md)
