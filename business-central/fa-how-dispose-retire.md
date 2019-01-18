---
title: Cancelar o retirar activos fijos | Documentos de Microsoft
description: Debe registrar un valor de baja cuando se rechaza, vende o retira un activo fijo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 10e7939378d222e2e2f915c89f820e000615ac1e
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="707c2-103">Cancelar o retirar activos fijos</span><span class="sxs-lookup"><span data-stu-id="707c2-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="707c2-104">En el momento de vender o dar de baja un activo, el valor de venta o baja debe registrarse para calcular y anotar las ganancias o las pérdidas.</span><span class="sxs-lookup"><span data-stu-id="707c2-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="707c2-105">Un movimiento de venta o baja debe ser el último movimiento registrado de un activo.</span><span class="sxs-lookup"><span data-stu-id="707c2-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="707c2-106">Puede registrar más de un movimiento de venta o baja en activos fijos que desea dar de baja parcialmente.</span><span class="sxs-lookup"><span data-stu-id="707c2-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="707c2-107">El total de todos los importes de venta o baja registrados debe ser un abono.</span><span class="sxs-lookup"><span data-stu-id="707c2-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="707c2-108">Si negocia con un activo fijo y lo cambia por otro, deberá registrar la venta del activo anterior (venta/baja) y la compra del nuevo (adquisición).</span><span class="sxs-lookup"><span data-stu-id="707c2-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="707c2-109">Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="707c2-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="707c2-110">Para registrar una venta/baja desde el diario general de activos fijos</span><span class="sxs-lookup"><span data-stu-id="707c2-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="707c2-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios generales A/F** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="707c2-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="707c2-112">Cree una línea inicial de diario y rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="707c2-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="707c2-113">En el campo **A/F Tipo registro**, seleccione **Venta/baja**.</span><span class="sxs-lookup"><span data-stu-id="707c2-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="707c2-114">Elija la acción **Introducir saldo AF**.</span><span class="sxs-lookup"><span data-stu-id="707c2-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="707c2-115">Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de venta/baja.</span><span class="sxs-lookup"><span data-stu-id="707c2-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="707c2-116">El paso 4 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cuenta de venta/baja** contiene la cuenta de cargo y el campo **Cuenta contrapartida venta/baja** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación.</span><span class="sxs-lookup"><span data-stu-id="707c2-116">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="707c2-117">Para obtener más información, vea la sección "Para configurar grupos contables de activos fijos" en [Configurar información general del activo fijo](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="707c2-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="707c2-118">Seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="707c2-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="707c2-119">Si vende o dispone de parte de un activo, debe dividir el activo antes de poder grabar la transacción de venta/baja.</span><span class="sxs-lookup"><span data-stu-id="707c2-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="707c2-120">Para obtener más información, consulte [Transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="707c2-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="707c2-121">Para ver movimientos venta/baja</span><span class="sxs-lookup"><span data-stu-id="707c2-121">To view disposal ledger entries</span></span>
<span data-ttu-id="707c2-122">En el momento de vender o dar de baja un activo, el valor de venta o baja se registra en las cuentas contables en las que puede ver el resultado.</span><span class="sxs-lookup"><span data-stu-id="707c2-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="707c2-123">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="707c2-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="707c2-124">Seleccione el activo en el que desea ver los movimientos y, a continuación, elija la acción **Libros amortización**.</span><span class="sxs-lookup"><span data-stu-id="707c2-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="707c2-125">Seleccione el libro de amortización en el que desea ver los movimientos y, a continuación, elija la acción **Movimientos**.</span><span class="sxs-lookup"><span data-stu-id="707c2-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="707c2-126">Seleccione una línea con **Venta/baja** en el campo **A/F Categoría registro**, y a continuación seleccione la acción **Navegar**.</span><span class="sxs-lookup"><span data-stu-id="707c2-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="707c2-127">En la página **Navegar**, seleccione la línea del movimiento de contabilidad y, a continuación, seleccione la acción **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="707c2-127">On the **Navigate** page, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="707c2-128">La página **Movs. contabilidad** se abre y puede ver los movimientos que se produjeron al registrar la venta/baja.</span><span class="sxs-lookup"><span data-stu-id="707c2-128">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="707c2-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="707c2-129">See Also</span></span>
[<span data-ttu-id="707c2-130">Activos fijos</span><span class="sxs-lookup"><span data-stu-id="707c2-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="707c2-131">Configurar activos fijos</span><span class="sxs-lookup"><span data-stu-id="707c2-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="707c2-132">Finanzas</span><span class="sxs-lookup"><span data-stu-id="707c2-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="707c2-133">Introducción</span><span class="sxs-lookup"><span data-stu-id="707c2-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="707c2-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="707c2-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

