---
title: "Tutorial: elaboración de previsiones del flujo de efectivo con esquemas de cuentas | Documentos de Microsoft"
description: "Este tutorial describe cómo puede utilizar los esquemas de cuentas para elaborar previsiones del flujo de efectivo. Los esquemas de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de efectivo. En los esquemas de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de efectivo. Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de efectivo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c66fc5da322ddb1d217b61da0b563faab27b344e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="65cd7-106">Tutorial: elaboración de previsiones del flujo de efectivo con esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="65cd7-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="65cd7-107">Este tutorial describe cómo puede utilizar los esquemas de cuentas para elaborar previsiones del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="65cd7-108">Los esquemas de cuentas realizan cálculos que no se puedan realizar directamente en el plan de cuentas del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="65cd7-109">En los esquemas de cuentas, puede configurar los subtotales para las recepciones y los desembolsos del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="65cd7-110">Estos subtotales se pueden incluir de los nuevos totales que pueden usarse en la elaboración de previsiones del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="65cd7-111">Acerca de este tutorial</span><span class="sxs-lookup"><span data-stu-id="65cd7-111">About This Walkthrough</span></span>  
<span data-ttu-id="65cd7-112">En este tutorial se describen las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="65cd7-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="65cd7-113">Configuración de un nuevo nombre de esquema de cuenta del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="65cd7-114">Configuración de líneas de esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="65cd7-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="65cd7-115">Configuración de un nuevo diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="65cd7-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="65cd7-116">Asignación de un diseño de columna a un esquema de cuentas</span><span class="sxs-lookup"><span data-stu-id="65cd7-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="65cd7-117">Ver e imprimir la previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="65cd7-118">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="65cd7-118">Prerequisites</span></span>  
<span data-ttu-id="65cd7-119">Para completar este tutorial, necesitará:</span><span class="sxs-lookup"><span data-stu-id="65cd7-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="65cd7-120"> Instalada.</span><span class="sxs-lookup"><span data-stu-id="65cd7-120"> installed.</span></span>  
- <span data-ttu-id="65cd7-121">Se registran las líneas de la hoja de trabajo del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="65cd7-122">Roles</span><span class="sxs-lookup"><span data-stu-id="65cd7-122">Roles</span></span>  
<span data-ttu-id="65cd7-123">En este tutorial, se demuestran las tareas realizadas por el siguiente rol de usuario:</span><span class="sxs-lookup"><span data-stu-id="65cd7-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="65cd7-124">Controlador</span><span class="sxs-lookup"><span data-stu-id="65cd7-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="65cd7-125">Historia</span><span class="sxs-lookup"><span data-stu-id="65cd7-125">Story</span></span>  
<span data-ttu-id="65cd7-126">Ken es un controlador de CRONUS que efectúa previsiones mensuales del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="65cd7-127">Incluye las finanzas, ventas, compras y activos fijos en la previsión y, a continuación, lo envía a CFO Sara para una perspectiva de negocio.</span><span class="sxs-lookup"><span data-stu-id="65cd7-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="65cd7-128">Configuración de un nuevo nombre de esquema de cuenta.</span><span class="sxs-lookup"><span data-stu-id="65cd7-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="65cd7-129">Un esquema de cuentas consta de un nombre de esquema de cuenta del flujo de efectivo con una serie de líneas y un diseño de columna.</span><span class="sxs-lookup"><span data-stu-id="65cd7-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="65cd7-130">Configuración de un nuevo nombre de esquema de cuenta</span><span class="sxs-lookup"><span data-stu-id="65cd7-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="65cd7-131">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="65cd7-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="65cd7-132">En la ventana **Nombres de esquema de cuenta**, elija **Nuevo** para crear un nuevo nombre de cuenta de flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="65cd7-133">En el campo **Nombre**, especifique **Previsiones**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="65cd7-134">En el campo **Descripción**, introduzca **Previsión de flujo de efectivo**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="65cd7-135">Deje en blanco los campos **Plantilla columna genér.** y **Nombre vista análisis**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="65cd7-136">Configuración de líneas de esquema de cuenta</span><span class="sxs-lookup"><span data-stu-id="65cd7-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="65cd7-137">Después de configurar el nombre del esquema de cuentas, Ken define cada línea que aparece en el esquema de cuenta del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="65cd7-138">Ken define las líneas que se pueden mostrar en los informes además de las líneas que se sólo se utilizan para realizar cálculos.</span><span class="sxs-lookup"><span data-stu-id="65cd7-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="65cd7-139">Para configurar líneas de esquema de cuenta</span><span class="sxs-lookup"><span data-stu-id="65cd7-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="65cd7-140">En la ventana **Nombre esquema cuenta**, seleccione el nuevo nombre del esquema de cuentas de **Previsiones** que ha creado.</span><span class="sxs-lookup"><span data-stu-id="65cd7-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="65cd7-141">En la pestaña **Inicio**, en el grupo **Procesar**, elija **Editar esquema cuentas**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="65cd7-142">En la ventana **Esquema cuentas**, especifique cada línea exactamente como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="65cd7-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="65cd7-143">Con la función **Insertar cuentas de coste y flete**, puede marcar rápidamente los cuentas de flujo de efectivo del plan de cuentas del flujo de efectivo y copiar las líneas del esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="65cd7-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="65cd7-144">|Nº fila|Descripción|Tipo sumatorio|Sumatorio|Tipo fila|Tipo importe|Mostrar|</span><span class="sxs-lookup"><span data-stu-id="65cd7-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="65cd7-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Importe|Cambio neto|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="65cd7-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="65cd7-146">|C20|Importe hasta fecha|Saldo a la fecha|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="65cd7-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="65cd7-147">|C30|Todo el ejercicio|Todo el ejercicio|Movimientos|Importe neto|Siempre|</span><span class="sxs-lookup"><span data-stu-id="65cd7-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="65cd7-148">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="65cd7-149">Asigna el nombre de la plantilla de columnas del esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="65cd7-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="65cd7-150">Ken ahora está preparado para asignar el diseño de columna al nombre del esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="65cd7-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="65cd7-151">Para asignar el nombre de la plantilla de columnas del esquema de cuentas.</span><span class="sxs-lookup"><span data-stu-id="65cd7-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="65cd7-152">En la ventana **Nombres esquemas de cuentas**, seleccione **Previsión** en el campo **Nombre**.</span><span class="sxs-lookup"><span data-stu-id="65cd7-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="65cd7-153">En el campo **Plantilla columna genér.**, seleccione el diseño de columna **Flujo de efectivo** para asignar como diseño de columnas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="65cd7-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="65cd7-154">Para ver e imprimir la previsión del flujo de efectivo</span><span class="sxs-lookup"><span data-stu-id="65cd7-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="65cd7-155">En la ventana **Nombres de esquemas de cuentas**, seleccione la acción **Información general** para ver la previsión del flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="65cd7-156">En la ventana **Panorama esq. cta.**, puede seleccionar un importe y después ver los movimientos de la previsión del flujo de efectivo que conforman el importe.</span><span class="sxs-lookup"><span data-stu-id="65cd7-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="65cd7-157">Además, puede ver la fórmula que se utiliza para calcular el importe.</span><span class="sxs-lookup"><span data-stu-id="65cd7-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="65cd7-158">También puede filtrar los importes por fecha y dimensión.</span><span class="sxs-lookup"><span data-stu-id="65cd7-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="65cd7-159">Elija la acción **Imprimir** para que se imprima la previsión de flujo de efectivo.</span><span class="sxs-lookup"><span data-stu-id="65cd7-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="65cd7-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="65cd7-160">See Also</span></span>  
 <span data-ttu-id="65cd7-161">[Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="65cd7-161">[How to: Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="65cd7-162">Tutoriales de procesos empresariales</span><span class="sxs-lookup"><span data-stu-id="65cd7-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="65cd7-163">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="65cd7-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

