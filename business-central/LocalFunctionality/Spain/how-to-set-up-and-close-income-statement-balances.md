---
title: "Configuración y asiento de la regularización"
description: "Puede utilizar cuentas de regularización para saldar y realizar el seguimiento de varias cuentas al mismo tiempo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 55c274c942816de432b98f37614f686bfcbebcc3
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="set-up-and-close-income-statement-balances"></a><span data-ttu-id="ffb6c-103">Configuración y asiento de la regularización</span><span class="sxs-lookup"><span data-stu-id="ffb6c-103">Set Up and Close Income Statement Balances</span></span>
<span data-ttu-id="ffb6c-104">Puede utilizar cuentas de regularización para saldar y realizar el seguimiento de varias cuentas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-104">You can use income statement balancing accounts to balance and track several accounts at the same time.</span></span> <span data-ttu-id="ffb6c-105">El proceso **Asiento regularización** transfiere las cuentas de regularización a una cuenta del balance y las cierra.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-105">The **Close Income Statement** batch job transfers income statement accounts to an account in the balance sheet, and closes the income statement accounts.</span></span> <span data-ttu-id="ffb6c-106">Cuando se ejecuta el proceso **Asiento regularización**, los movimientos se registran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-106">When the **Close Income Statement** batch job is run, the entries are automatically posted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ffb6c-107">Antes de ejecutar el proceso, se debe cerrar el ejercicio.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-107">The fiscal year must be closed before the batch job can run.</span></span>  

## <a name="to-set-up-the-income-statement-balance-account"></a><span data-ttu-id="ffb6c-108">Para configurar la cuenta de regularización</span><span class="sxs-lookup"><span data-stu-id="ffb6c-108">To set up the income statement balance account</span></span>  

1.  <span data-ttu-id="ffb6c-109">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ffb6c-110">Seleccione una cuenta de contabilidad existente y después seleccione **Editar** para abrir la página **Ficha cuenta**.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-110">Select an existing general ledger account, and then choose the **Edit** action to open the **G/L Account Card** page.</span></span>  
3.  <span data-ttu-id="ffb6c-111">Amplíe la ficha desplegable **General**.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-111">Expand the **General** FastTab.</span></span>  
4.  <span data-ttu-id="ffb6c-112">En el campo **Cta. regularización**, seleccione la cuenta de ajuste para la cuenta comercial auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-112">In the **Income Stmt. Bal. Acc.** field, select the adjustment account for the auxiliary commercial account.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ffb6c-113">Dicha cuenta será en la que se cargarán o abonarán los saldos al ejecutar el proceso de regularización.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-113">During adjustment, balances will be expensed or credited to this account.</span></span>  

5.  <span data-ttu-id="ffb6c-114">Escriba la información en los campos requeridos y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-114">Enter information into the required fields, and then choose the **OK** button.</span></span>  

## <a name="to-close-income-statement-balances"></a><span data-ttu-id="ffb6c-115">Para el asiento de la regularización</span><span class="sxs-lookup"><span data-stu-id="ffb6c-115">To close income statement balances</span></span>  

1.  <span data-ttu-id="ffb6c-116">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cerrar asiento de regularización** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ffb6c-117">En la ficha desplegable **Opciones**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-117">In the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ffb6c-118">Campo</span><span class="sxs-lookup"><span data-stu-id="ffb6c-118">Field</span></span>|<span data-ttu-id="ffb6c-119">Description</span><span class="sxs-lookup"><span data-stu-id="ffb6c-119">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ffb6c-120">**Fecha final ejercicio**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-120">**Fiscal Year Ending Date**</span></span>|<span data-ttu-id="ffb6c-121">Seleccione la fecha del ejercicio cerrado.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-121">Select the date of the closed fiscal year.</span></span>|  
    |<span data-ttu-id="ffb6c-122">**Libro del diario general**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-122">**Gen. Journal Template**</span></span>|<span data-ttu-id="ffb6c-123">Seleccione el libro del diario general requerido.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-123">Select the required general journal template.</span></span>|  
    |<span data-ttu-id="ffb6c-124">**Sección diario general**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-124">**Gen. Journal Batch**</span></span>|<span data-ttu-id="ffb6c-125">Seleccione la sección del diario general requerida.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-125">Select the required general journal batch.</span></span>|  
    |<span data-ttu-id="ffb6c-126">**Nº documento**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-126">**Document No.**</span></span>|<span data-ttu-id="ffb6c-127">Escriba el número de documento.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-127">Enter the document number.</span></span>|  
    |<span data-ttu-id="ffb6c-128">**Cta. ajtes. red. div. adic**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-128">**Retained Earnings Acc.**</span></span>|<span data-ttu-id="ffb6c-129">Seleccione la cuenta de movimientos de remanente.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-129">Select the account for the retained earnings entries.</span></span>|  
    |<span data-ttu-id="ffb6c-130">**Texto de registro**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-130">**Posting Description**</span></span>|<span data-ttu-id="ffb6c-131">Escriba la descripción requerida.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-131">Enter the required description.</span></span>|  

3.  <span data-ttu-id="ffb6c-132">En la sección **Cerrado por**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-132">In the **Close by** section, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ffb6c-133">Campo</span><span class="sxs-lookup"><span data-stu-id="ffb6c-133">Field</span></span>|<span data-ttu-id="ffb6c-134">Description</span><span class="sxs-lookup"><span data-stu-id="ffb6c-134">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ffb6c-135">**Código de empresa**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-135">**Business Unit Code**</span></span>|<span data-ttu-id="ffb6c-136">Seleccione esta opción para crear un movimiento para cada código de empresa.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-136">Select to create an entry for each business code.</span></span>|  
    |<span data-ttu-id="ffb6c-137">**Dimensiones**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-137">**Dimensions**</span></span>|<span data-ttu-id="ffb6c-138">Seleccione esta opción para crear un movimiento para cada dimensión de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-138">Select to create an entry for each general ledger dimension.</span></span>|  
    |<span data-ttu-id="ffb6c-139">**Periodo inventario cerrado**</span><span class="sxs-lookup"><span data-stu-id="ffb6c-139">**Inventory Period Closed**</span></span>|<span data-ttu-id="ffb6c-140">Seleccione esta opción para indicar que el periodo de inventario con fecha final igual o posterior a la fecha final del periodo contable está cerrado.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-140">Select to indicate that the inventory period with ending dates equal to or greater than the last date of the accounting period is closed.</span></span>|  

4.  <span data-ttu-id="ffb6c-141">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-141">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ffb6c-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ffb6c-142">See Also</span></span>  
 [<span data-ttu-id="ffb6c-143">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="ffb6c-143">Spain Local Functionality</span></span>](spain-local-functionality.md)

