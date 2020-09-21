---
title: Impresión de informes de libro diario
description: Los informes de libro diario muestran todos los movimientos de contabilidad creados en un periodo específico.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a9c2f44eccad32eff840b14e3b9f63410646180f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778323"
---
# <a name="print-account-book-reports"></a><span data-ttu-id="7d759-103">Imprimir informes de libro diario</span><span class="sxs-lookup"><span data-stu-id="7d759-103">Print Account Book Reports</span></span>
<span data-ttu-id="7d759-104">Los informes de libro diario muestran todos los movimientos de contabilidad creados en un periodo específico.</span><span class="sxs-lookup"><span data-stu-id="7d759-104">Account book reports display all the general ledger entries created in a specific period.</span></span> <span data-ttu-id="7d759-105">Los dos informes de libro diario son:</span><span class="sxs-lookup"><span data-stu-id="7d759-105">The two account book reports are:</span></span>  

- <span data-ttu-id="7d759-106">Informe **Libro diario oficial**: muestra información sobre todos los movimientos de contabilidad, agrupados por transacción.</span><span class="sxs-lookup"><span data-stu-id="7d759-106">**Official Account Book** report - Displays information for every general ledger entry, grouped by transaction.</span></span>  
- <span data-ttu-id="7d759-107">Informe **Libro diario oficial resumido**: muestra un resumen de los movimientos generales, agrupados por cuentas de registro o mayores.</span><span class="sxs-lookup"><span data-stu-id="7d759-107">**Official Account Summarized Book** report - Displays a summary of general entries, grouped by heading or posting accounts.</span></span>  

<span data-ttu-id="7d759-108">Al enviar estos informes a la administración o a los auditores, se pueden incluir páginas adicionales que precederán el informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-108">When sending these reports to the authorities or auditors, you can include additional pages that will precede your report.</span></span> <span data-ttu-id="7d759-109">Para ello, se debe definir manualmente el número de la primera página del informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-109">To do this, you need to manually set the report's first page number.</span></span> <span data-ttu-id="7d759-110">Por ejemplo, si tiene tres páginas de información que preceden el informe, puede definir la primera página del informe para indicar que es la página 4.</span><span class="sxs-lookup"><span data-stu-id="7d759-110">For example, if you have three pages of information preceding your report, you can set the first page of the report to indicate that it is page 4.</span></span>  

## <a name="to-print-an-official-account-book-report"></a><span data-ttu-id="7d759-111">Para imprimir un informe de libro diario oficial</span><span class="sxs-lookup"><span data-stu-id="7d759-111">To print an official account book report</span></span>  

1.  <span data-ttu-id="7d759-112">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Cuenta - Libro diario oficial** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7d759-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account - Official Acc. Book**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7d759-113">En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d759-113">In the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7d759-114">Campo</span><span class="sxs-lookup"><span data-stu-id="7d759-114">Field</span></span>|<span data-ttu-id="7d759-115">Description</span><span class="sxs-lookup"><span data-stu-id="7d759-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7d759-116">**Texto asiento cierre**</span><span class="sxs-lookup"><span data-stu-id="7d759-116">**Closing Transaction Description**</span></span>|<span data-ttu-id="7d759-117">Escriba la descripción de la transacción de cierre del periodo.</span><span class="sxs-lookup"><span data-stu-id="7d759-117">Enter the description for the closing period transaction.</span></span>|  
    |<span data-ttu-id="7d759-118">**Texto asiento apertura**</span><span class="sxs-lookup"><span data-stu-id="7d759-118">**Opening Transaction Description**</span></span>|<span data-ttu-id="7d759-119">Escriba la descripción de la transacción de apertura del periodo.</span><span class="sxs-lookup"><span data-stu-id="7d759-119">Enter the description for the opening period transaction.</span></span>|  
    |<span data-ttu-id="7d759-120">**Primera página**</span><span class="sxs-lookup"><span data-stu-id="7d759-120">**First Page**</span></span>|<span data-ttu-id="7d759-121">Introduzca el número que desea incluir en la primera página del informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-121">Enter the number that you want to include on the first page of the report.</span></span>|  
    |<span data-ttu-id="7d759-122">**Muestra importes en divisa adicional**</span><span class="sxs-lookup"><span data-stu-id="7d759-122">**Show Amounts in Add. Currency**</span></span>|<span data-ttu-id="7d759-123">Seleccione que se muestren los importes del informe en una divisa adicional de informe (DA).</span><span class="sxs-lookup"><span data-stu-id="7d759-123">Select to show the report amounts in additional reporting currency (ACY).</span></span>|  

3.  <span data-ttu-id="7d759-124">En la ficha desplegable **Registro contabilidad**, seleccione los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="7d759-124">In the **GL Register** FastTab, select appropriate filters.</span></span>  
4.  <span data-ttu-id="7d759-125">Seleccione el botón de **Imprimir** para imprimir el informe o elegir el botón de **Vista previa** para verlo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7d759-125">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="to-print-an-official-account-summarized-book-report"></a><span data-ttu-id="7d759-126">Para imprimir un libro diario oficial resumido</span><span class="sxs-lookup"><span data-stu-id="7d759-126">To print an official account summarized book report</span></span>  

1.  <span data-ttu-id="7d759-127">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Libro diario oficial resumido** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7d759-127">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Official Acc.Summarized Book**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="7d759-128">En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d759-128">In the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7d759-129">Campo</span><span class="sxs-lookup"><span data-stu-id="7d759-129">Field</span></span>|<span data-ttu-id="7d759-130">Description</span><span class="sxs-lookup"><span data-stu-id="7d759-130">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7d759-131">**Desde fecha**</span><span class="sxs-lookup"><span data-stu-id="7d759-131">**From Date**</span></span>|<span data-ttu-id="7d759-132">Indique la fecha de inicio del informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-132">Enter the start date of the report.</span></span>|  
    |<span data-ttu-id="7d759-133">**Hasta fecha**</span><span class="sxs-lookup"><span data-stu-id="7d759-133">**To Date**</span></span>|<span data-ttu-id="7d759-134">Indique la fecha de fin del informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-134">Enter the end date of the report.</span></span>|  
    |<span data-ttu-id="7d759-135">**Incluir movs. Regularización**</span><span class="sxs-lookup"><span data-stu-id="7d759-135">**Include Closing Entries**</span></span>|<span data-ttu-id="7d759-136">Seleccione esta opción para incluir movimientos de regularización en el informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-136">Select to include the closing entries in the report.</span></span>|  
    |<span data-ttu-id="7d759-137">**Muestra importes en divisa adicional**</span><span class="sxs-lookup"><span data-stu-id="7d759-137">**Show Amounts in Add. Currency**</span></span>|<span data-ttu-id="7d759-138">Seleccione que se muestren los importes del informe en una divisa adicional de informe (DA).</span><span class="sxs-lookup"><span data-stu-id="7d759-138">Select to show the report amounts in additional reporting currency (ACY).</span></span>|  
    |<span data-ttu-id="7d759-139">**Primera página**</span><span class="sxs-lookup"><span data-stu-id="7d759-139">**First page**</span></span>|<span data-ttu-id="7d759-140">Introduzca el número que desea incluir en la primera página del informe.</span><span class="sxs-lookup"><span data-stu-id="7d759-140">Enter the number that you want to include on the first page of the report.</span></span>|  
    |<span data-ttu-id="7d759-141">**Tipo mov.**</span><span class="sxs-lookup"><span data-stu-id="7d759-141">**Account Type**</span></span>|<span data-ttu-id="7d759-142">Seleccione **Registro** o **Mayor**.</span><span class="sxs-lookup"><span data-stu-id="7d759-142">Select **Posting** or **Heading**.</span></span> <span data-ttu-id="7d759-143">**Registro** implica que se pueden registrar movimientos en la cuenta y **Mayor** implica que no se pueden registrar movimientos en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="7d759-143">**Posting** implies that entries can be posted to the account, and **Heading** implies that entries cannot be posted to the account.</span></span>|  

3.  <span data-ttu-id="7d759-144">Seleccione el botón de **Imprimir** para imprimir el informe o elegir el botón de **Vista previa** para verlo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7d759-144">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d759-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7d759-145">See Also</span></span>  
 [<span data-ttu-id="7d759-146">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="7d759-146">Spain Local Functionality</span></span>](spain-local-functionality.md)
