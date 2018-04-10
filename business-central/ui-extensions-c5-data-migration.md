---
title: "Usar la extensión de migración de datos C5 | Documentos de Microsoft"
description: "Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="7a99c-103">Extensión de la migración de datos de C5 para Business Central</span><span class="sxs-lookup"><span data-stu-id="7a99c-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="7a99c-104">Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a99c-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7a99c-105">También puede migrar los movimientos históricos para cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="7a99c-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="7a99c-106">La empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] no debe contener ningún dato.</span><span class="sxs-lookup"><span data-stu-id="7a99c-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="7a99c-107">Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.</span><span class="sxs-lookup"><span data-stu-id="7a99c-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="7a99c-108">¿Qué datos se migran?</span><span class="sxs-lookup"><span data-stu-id="7a99c-108">What Data is Migrated?</span></span>
<span data-ttu-id="7a99c-109">Se migran los datos siguientes para cada entidad:</span><span class="sxs-lookup"><span data-stu-id="7a99c-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="7a99c-110">**Clientes**</span><span class="sxs-lookup"><span data-stu-id="7a99c-110">**Customers**</span></span>
* <span data-ttu-id="7a99c-111">Lugar</span><span class="sxs-lookup"><span data-stu-id="7a99c-111">Location</span></span>
* <span data-ttu-id="7a99c-112">País</span><span class="sxs-lookup"><span data-stu-id="7a99c-112">Country</span></span>
* <span data-ttu-id="7a99c-113">Dimensiones de cliente (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="7a99c-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a99c-114">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="7a99c-114">Shipment method</span></span>
* <span data-ttu-id="7a99c-115">Vendedor</span><span class="sxs-lookup"><span data-stu-id="7a99c-115">Sales Person</span></span>
* <span data-ttu-id="7a99c-116">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="7a99c-116">Payment terms</span></span>
* <span data-ttu-id="7a99c-117">Forma pago</span><span class="sxs-lookup"><span data-stu-id="7a99c-117">Payment method</span></span>
* <span data-ttu-id="7a99c-118">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-118">Customer price group</span></span>
* <span data-ttu-id="7a99c-119">Descuento de la factura del cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-119">Customer invoice discount</span></span>

<span data-ttu-id="7a99c-120">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="7a99c-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a99c-121">Configuración contable cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-121">Customer posting setup</span></span>
* <span data-ttu-id="7a99c-122">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="7a99c-122">General journal batch</span></span>
* <span data-ttu-id="7a99c-123">Transacciones abiertas (movimientos de cliente)</span><span class="sxs-lookup"><span data-stu-id="7a99c-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="7a99c-124">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="7a99c-124">**Vendors**</span></span>
* <span data-ttu-id="7a99c-125">Lugar</span><span class="sxs-lookup"><span data-stu-id="7a99c-125">Location</span></span>
* <span data-ttu-id="7a99c-126">País</span><span class="sxs-lookup"><span data-stu-id="7a99c-126">Country</span></span>
* <span data-ttu-id="7a99c-127">Dimensiones de proveedor (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="7a99c-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a99c-128">Descuento en factura</span><span class="sxs-lookup"><span data-stu-id="7a99c-128">Invoice discount</span></span>
* <span data-ttu-id="7a99c-129">Condiciones de envío</span><span class="sxs-lookup"><span data-stu-id="7a99c-129">Shipment method</span></span>
* <span data-ttu-id="7a99c-130">Comprador</span><span class="sxs-lookup"><span data-stu-id="7a99c-130">Purchaser</span></span>
* <span data-ttu-id="7a99c-131">Condiciones de pago</span><span class="sxs-lookup"><span data-stu-id="7a99c-131">Payment terms</span></span>
* <span data-ttu-id="7a99c-132">Forma pago</span><span class="sxs-lookup"><span data-stu-id="7a99c-132">Payment method</span></span>
* <span data-ttu-id="7a99c-133">Descuento de factura del proveedor</span><span class="sxs-lookup"><span data-stu-id="7a99c-133">Vendor invoice discount</span></span>

<span data-ttu-id="7a99c-134">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="7a99c-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a99c-135">Configuración contable proveedor</span><span class="sxs-lookup"><span data-stu-id="7a99c-135">Vendor posting setup</span></span>
* <span data-ttu-id="7a99c-136">Lote diario general</span><span class="sxs-lookup"><span data-stu-id="7a99c-136">General journal batch</span></span>
* <span data-ttu-id="7a99c-137">Abra transacciones (movimientos de proveedores)</span><span class="sxs-lookup"><span data-stu-id="7a99c-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="7a99c-138">**Productos**</span><span class="sxs-lookup"><span data-stu-id="7a99c-138">**Items**</span></span>
* <span data-ttu-id="7a99c-139">Lugar</span><span class="sxs-lookup"><span data-stu-id="7a99c-139">Location</span></span>
* <span data-ttu-id="7a99c-140">País</span><span class="sxs-lookup"><span data-stu-id="7a99c-140">Country</span></span>
* <span data-ttu-id="7a99c-141">Dimensiones de producto (departamento, centro, propósito)</span><span class="sxs-lookup"><span data-stu-id="7a99c-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7a99c-142">Descuentos línea de ventas</span><span class="sxs-lookup"><span data-stu-id="7a99c-142">Sales line discounts</span></span>
* <span data-ttu-id="7a99c-143">Grupos descuento cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-143">Customer discount groups</span></span>
* <span data-ttu-id="7a99c-144">Grupos descuento productos</span><span class="sxs-lookup"><span data-stu-id="7a99c-144">Item discount groups</span></span>
* <span data-ttu-id="7a99c-145">Precio venta</span><span class="sxs-lookup"><span data-stu-id="7a99c-145">Sales price</span></span>
* <span data-ttu-id="7a99c-146">Código arancelario</span><span class="sxs-lookup"><span data-stu-id="7a99c-146">Tariff number</span></span>
* <span data-ttu-id="7a99c-147">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="7a99c-147">Units of measure</span></span>
* <span data-ttu-id="7a99c-148">Código seguimiento producto</span><span class="sxs-lookup"><span data-stu-id="7a99c-148">Item tracking code</span></span>
* <span data-ttu-id="7a99c-149">Grupo precio cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-149">Customer price group</span></span>

<span data-ttu-id="7a99c-150">Si migra cuentas, los datos siguientes también se migrarán:</span><span class="sxs-lookup"><span data-stu-id="7a99c-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7a99c-151">Configuración contable inventario</span><span class="sxs-lookup"><span data-stu-id="7a99c-151">Inventory posting setup</span></span>
* <span data-ttu-id="7a99c-152">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="7a99c-152">General posting setup</span></span>
* <span data-ttu-id="7a99c-153">Sección diario producto</span><span class="sxs-lookup"><span data-stu-id="7a99c-153">Item journal batch</span></span>
* <span data-ttu-id="7a99c-154">Abra transacciones (movimientos de productos)</span><span class="sxs-lookup"><span data-stu-id="7a99c-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="7a99c-155">Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran.</span><span class="sxs-lookup"><span data-stu-id="7a99c-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="7a99c-156">Otros tipos de cambio no se migran.</span><span class="sxs-lookup"><span data-stu-id="7a99c-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="7a99c-157">Para migrar datos</span><span class="sxs-lookup"><span data-stu-id="7a99c-157">To migrate data</span></span>
<span data-ttu-id="7a99c-158">Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="7a99c-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="7a99c-159">En la C5, utilice la función **Base de datos de exportación** para exportar los datos.</span><span class="sxs-lookup"><span data-stu-id="7a99c-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="7a99c-160">Envíe la carpeta de exportación a una carpeta comprimida.</span><span class="sxs-lookup"><span data-stu-id="7a99c-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="7a99c-161">En [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione el ícono ![Buscar página o informe](media/ui-search/search_small.png "Buscar página o informe"), introduzca **Migración de datos** y, a continuación, seleccione **Migración de datos**.</span><span class="sxs-lookup"><span data-stu-id="7a99c-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="7a99c-162">Complete los pasos de la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="7a99c-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="7a99c-163">Asegúrese de elegir **Importar de Microsoft Dynamcis C5 2012** como origen de datos.</span><span class="sxs-lookup"><span data-stu-id="7a99c-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="7a99c-164">Las empresas a menudo agregan campos para personalizar la C5 para su línea de negocio específica.</span><span class="sxs-lookup"><span data-stu-id="7a99c-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7a99c-165"> no migra datos de campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7a99c-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="7a99c-166">Además, la migración dará error si tiene más de 10 campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7a99c-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="7a99c-167">Ver el estado de la migración</span><span class="sxs-lookup"><span data-stu-id="7a99c-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="7a99c-168">Utilice la página **Información general sobre migración de datos** para controlar el éxito de la migración.</span><span class="sxs-lookup"><span data-stu-id="7a99c-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="7a99c-169">La página muestra información como el número de entidades que la migración incluirá, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a99c-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="7a99c-170">También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas.</span><span class="sxs-lookup"><span data-stu-id="7a99c-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="7a99c-171">Para obtener más información, consulte la siguiente sección de este tema.</span><span class="sxs-lookup"><span data-stu-id="7a99c-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="7a99c-172">Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="7a99c-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="7a99c-173">Corrección de errores</span><span class="sxs-lookup"><span data-stu-id="7a99c-173">Correcting Errors</span></span>
<span data-ttu-id="7a99c-174">Si algo sale mal y se produce un error, el campo **Estado** mostrará **Completado con errores** y el campo **Recuento de errores** mostrará cuántos.</span><span class="sxs-lookup"><span data-stu-id="7a99c-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="7a99c-175">Para ver una lista de los errores, puede abrir la página **Errores de migración de datos** si elige:</span><span class="sxs-lookup"><span data-stu-id="7a99c-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="7a99c-176">El número en el campo **Recuento de errores** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a99c-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="7a99c-177">La entidad y la acción **Mostrar errores**.</span><span class="sxs-lookup"><span data-stu-id="7a99c-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="7a99c-178">En la página **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para abrir una página que muestre los datos migrados de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a99c-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="7a99c-179">Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que reparó, sin tener que reiniciar por completo la migración.</span><span class="sxs-lookup"><span data-stu-id="7a99c-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="7a99c-180">Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar.</span><span class="sxs-lookup"><span data-stu-id="7a99c-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="7a99c-181">De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.</span><span class="sxs-lookup"><span data-stu-id="7a99c-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="7a99c-182">Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="7a99c-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="7a99c-183">Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="7a99c-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="7a99c-184">Comprobar datos después de migrar</span><span class="sxs-lookup"><span data-stu-id="7a99c-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="7a99c-185">Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a99c-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="7a99c-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="7a99c-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="7a99c-187">Movimientos de cliente</span><span class="sxs-lookup"><span data-stu-id="7a99c-187">Customer Entries</span></span>| <span data-ttu-id="7a99c-188">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="7a99c-188">General Journals</span></span>|
|<span data-ttu-id="7a99c-189">Movimientos de proveedor</span><span class="sxs-lookup"><span data-stu-id="7a99c-189">Vendor Entries</span></span>| <span data-ttu-id="7a99c-190">Diarios generales</span><span class="sxs-lookup"><span data-stu-id="7a99c-190">General Journals</span></span>|
|<span data-ttu-id="7a99c-191">Movs. prods.</span><span class="sxs-lookup"><span data-stu-id="7a99c-191">Item Entries</span></span>| <span data-ttu-id="7a99c-192">Diarios de productos</span><span class="sxs-lookup"><span data-stu-id="7a99c-192">Item Journals</span></span>|

<span data-ttu-id="7a99c-193">En [!INCLUDE[d365fin](includes/d365fin_md.md)], el proceso de los datos migrados se denomina **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="7a99c-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="7a99c-194">Detener la migración de datos</span><span class="sxs-lookup"><span data-stu-id="7a99c-194">Stopping Data Migration</span></span>
<span data-ttu-id="7a99c-195">Puede detener la migración de datos con la opción **Detener todas las migraciones**.</span><span class="sxs-lookup"><span data-stu-id="7a99c-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="7a99c-196">Si utiliza esta opción, todas las migraciones pendientes también se detendrán.</span><span class="sxs-lookup"><span data-stu-id="7a99c-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a99c-197">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7a99c-197">See Also</span></span>
<span data-ttu-id="7a99c-198">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7a99c-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="7a99c-199">Introducción</span><span class="sxs-lookup"><span data-stu-id="7a99c-199">Getting Started</span></span>](product-get-started.md) 

