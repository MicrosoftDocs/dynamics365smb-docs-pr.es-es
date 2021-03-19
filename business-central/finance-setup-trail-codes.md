---
title: Configurar códigos para pistas de auditoría | Documentos de Microsoft
description: Aprenda sobre las tareas para configurar códigos de origen y códigos de auditoría que puede usar para realizar un seguimiento de pistas de auditoría.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dab74a6a8debd20de781890c3b391457c6034e3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386904"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="96775-103">Configuración de códigos de origen y códigos de auditoría para pistas de auditoría</span><span class="sxs-lookup"><span data-stu-id="96775-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="96775-104">Todos los movimientos registrados se asignan automáticamente a un código de origen de forma que pueda realizarse un seguimiento del origen de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="96775-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="96775-105">Si desea asignar a los movimientos un código de origen adicional, utilice códigos de auditoría.</span><span class="sxs-lookup"><span data-stu-id="96775-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="96775-106">Los códigos de auditoría se utilizan para indicar el motivo por el que se ha creado un movimiento.</span><span class="sxs-lookup"><span data-stu-id="96775-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="96775-107">Al configurar códigos de auditoría, puede asignarlos a libros de diarios o a secciones de diarios, así como a líneas de diarios y a documentos individuales.</span><span class="sxs-lookup"><span data-stu-id="96775-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="96775-108">Tanto para los códigos fuente como para los códigos de auditoría, use códigos que sean descriptivos y fáciles de recordar.</span><span class="sxs-lookup"><span data-stu-id="96775-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="96775-109">El código debe ser único y puede configurar tantos códigos como desee.</span><span class="sxs-lookup"><span data-stu-id="96775-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="96775-110">Definir los códigos de origen</span><span class="sxs-lookup"><span data-stu-id="96775-110">Define source codes</span></span>

<span data-ttu-id="96775-111">A veces querrá saber cómo surge un movimiento determinado, por ejemplo, si procedía del registro de un diario general o de una factura de compra.</span><span class="sxs-lookup"><span data-stu-id="96775-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="96775-112">Un código de origen indica dónde se creó un movimiento.</span><span class="sxs-lookup"><span data-stu-id="96775-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="96775-113">Los movimientos se crean cuando se registran los diarios y facturas, y cuando se ejecutan determinados trabajos por lotes.</span><span class="sxs-lookup"><span data-stu-id="96775-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="96775-114">Cada tipo de registro tiene un código de origen diferente que se asigna cuando se crean entradas individuales.</span><span class="sxs-lookup"><span data-stu-id="96775-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="96775-115">El registro de diarios, pedidos, facturas o abonos, así como la ejecución de diversos trabajos por lotes, genera movimientos en los extractos financieros.</span><span class="sxs-lookup"><span data-stu-id="96775-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="96775-116">La página **Configuración códigos origen** contiene varias fichas desplegables, una por cada área de aplicación.</span><span class="sxs-lookup"><span data-stu-id="96775-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="96775-117">Cada ficha desplegable contiene los códigos de origen correspondientes a esa área de aplicación.</span><span class="sxs-lookup"><span data-stu-id="96775-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="96775-118">Cuando registra o ejecuta un trabajo por lotes, el programa adjunta automáticamente el código de origen correspondiente al movimiento.</span><span class="sxs-lookup"><span data-stu-id="96775-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="96775-119">Por ejemplo, al registrar desde el diario general, el programa codificará el movimiento con la abreviatura *DIAGEN*.</span><span class="sxs-lookup"><span data-stu-id="96775-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="96775-120">Luego puede filtrar la página **Movs. contabilidad** para mostrar qué movimientos se publicaron desde el diario general o desde documentos de ventas, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="96775-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="96775-121">Para definir códigos de origen</span><span class="sxs-lookup"><span data-stu-id="96775-121">To define source codes</span></span>

1. <span data-ttu-id="96775-122">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Configuración códigos origen** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="96775-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="96775-123">En la ventana **Configuración del código fuente**, especifique el código fuente relevante para cada tipo de registro y trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="96775-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="96775-124">Puede cambiar el contenido de un campo más tarde, y ese cambio afectará a futuros registros.</span><span class="sxs-lookup"><span data-stu-id="96775-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="96775-125">Cambiar códigos de origen</span><span class="sxs-lookup"><span data-stu-id="96775-125">Change source codes</span></span>

<span data-ttu-id="96775-126">Puede querer cambiar un código de origen.</span><span class="sxs-lookup"><span data-stu-id="96775-126">You may want to change a source code.</span></span> <span data-ttu-id="96775-127">Por ejemplo, quiere modificar el código de origen *GENJNL* a *GNJ*.</span><span class="sxs-lookup"><span data-stu-id="96775-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="96775-128">Para modificar códigos de origen</span><span class="sxs-lookup"><span data-stu-id="96775-128">To change source codes</span></span>

1. <span data-ttu-id="96775-129">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Códigos de origen** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="96775-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="96775-130">En la línea que contiene el código que debe modificarse, seleccione el código en el campo **Código**.</span><span class="sxs-lookup"><span data-stu-id="96775-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="96775-131">Introduzca el nuevo código y, a continuación, elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="96775-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="96775-132">También puede modificar el contenido del campo **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="96775-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="96775-133">Todos los nuevos movimientos que se registren posteriormente del diario general tendrán el nuevo código de origen.</span><span class="sxs-lookup"><span data-stu-id="96775-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="96775-134">Definir códigos de auditoría</span><span class="sxs-lookup"><span data-stu-id="96775-134">Define reason codes</span></span>

<span data-ttu-id="96775-135">Los códigos de auditoría complementan los código de origen y se utilizan para indicar por qué se creó una entrada.</span><span class="sxs-lookup"><span data-stu-id="96775-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="96775-136">Puede asignar códigos de auditoría en movimientos individuales y puede asignar códigos permanentes a libros de diarios y secciones de diario específicos.</span><span class="sxs-lookup"><span data-stu-id="96775-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="96775-137">Cuando un código de auditoría está vinculado a una línea del diario o a una cabecera de ventas o de compra, se marcan todos los movimientos con el código de auditoria al registrarlos.</span><span class="sxs-lookup"><span data-stu-id="96775-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="96775-138">Para configurar códigos de auditoría</span><span class="sxs-lookup"><span data-stu-id="96775-138">To set up reason codes</span></span>

1. <span data-ttu-id="96775-139">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Código de auditoría** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="96775-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="96775-140">En la ventana **Códigos auditoría**, introduzca el primer código en el campo **Código**.</span><span class="sxs-lookup"><span data-stu-id="96775-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="96775-141">En el campo **Descripción**, escriba un texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="96775-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="96775-142">Repita el procedimiento para cada código que desee utilizar.</span><span class="sxs-lookup"><span data-stu-id="96775-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="96775-143">Puede configurar cualquier número de códigos.</span><span class="sxs-lookup"><span data-stu-id="96775-143">You can set up any number of codes.</span></span>

<span data-ttu-id="96775-144">El siguiente procedimiento describe cómo agregar un código de auditoría a un libro del diario, pero se aplican pasos similares para agregar un código de auditoría a una línea del diario o sección del diario.</span><span class="sxs-lookup"><span data-stu-id="96775-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="96775-145">Para asignar códigos de auditoría a libros de diarios</span><span class="sxs-lookup"><span data-stu-id="96775-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="96775-146">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Libro diario general** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="96775-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="96775-147">En la línea que contiene el libro del diario seleccionado, en el campo **Código de auditoría**, especifique el código relevante.</span><span class="sxs-lookup"><span data-stu-id="96775-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="96775-148">Cierre el libro del diario.</span><span class="sxs-lookup"><span data-stu-id="96775-148">Close the journal template.</span></span>

<span data-ttu-id="96775-149">El código de auditoría seleccionado se copiará en las nuevas secciones de diario creadas en este libro del diario.</span><span class="sxs-lookup"><span data-stu-id="96775-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="96775-150">Para asignar códigos de auditoría a libros de diario de otras áreas de aplicación, deberá proceder del mismo modo.</span><span class="sxs-lookup"><span data-stu-id="96775-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="96775-151">Para usar códigos de auditoría en documentos de compras y ventas</span><span class="sxs-lookup"><span data-stu-id="96775-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="96775-152">Abra el documento de compras correspondiente.</span><span class="sxs-lookup"><span data-stu-id="96775-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="96775-153">En la cabecera de ventas o de compra, escriba el código en el campo **Código de auditoría**.</span><span class="sxs-lookup"><span data-stu-id="96775-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="96775-154">Al registrar la factura, el código de auditoría se copia en cada movimiento de contabilidad, cliente y proveedor.</span><span class="sxs-lookup"><span data-stu-id="96775-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="96775-155">No puede asignar códigos de auditoría distintos a cada una de las líneas de compra porque todas las líneas se registran como un solo movimiento.</span><span class="sxs-lookup"><span data-stu-id="96775-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="96775-156">Consulte Formación relacionada en [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="96775-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="96775-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="96775-157">See Also</span></span>

[<span data-ttu-id="96775-158">Finanzas</span><span class="sxs-lookup"><span data-stu-id="96775-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="96775-159">Conciliar bancos</span><span class="sxs-lookup"><span data-stu-id="96775-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="96775-160">Trabajar con dimensiones</span><span class="sxs-lookup"><span data-stu-id="96775-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="96775-161">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="96775-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="96775-162">Analizar el flujo de efectivo de la empresa</span><span class="sxs-lookup"><span data-stu-id="96775-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="96775-163">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="96775-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]