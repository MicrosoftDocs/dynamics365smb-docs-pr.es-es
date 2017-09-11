---
title: Emitir, imprimir, cancelar y anular cheques | Documentos de Microsoft
description: "Describe cómo emitir cheques con el diario de pagos, imprimir cheques y anular o ver movimientos de cheques en Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0875164a3afee7a835346a8d4b9323dda9ebf080
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-checks"></a><span data-ttu-id="7e707-103">Procedimiento: Trabajar con cheques</span><span class="sxs-lookup"><span data-stu-id="7e707-103">How to: Work With Checks</span></span>
<span data-ttu-id="7e707-104">Puede emitir cheques electrónicos y manuales en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7e707-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7e707-105">Ambos métodos utilizan el diario de pagos para emitir los cheques a proveedores.</span><span class="sxs-lookup"><span data-stu-id="7e707-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="7e707-106">También puede anular cheques y ver movimientos de cheques.</span><span class="sxs-lookup"><span data-stu-id="7e707-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="7e707-107">El proceso de emisión de cheques propone pagos, crea movimientos e imprime los cheques automáticos.</span><span class="sxs-lookup"><span data-stu-id="7e707-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7e707-108">Para asegurarse de que su banco solo compensa cheques e importes validados, puede enviarles un archivo que contenga la información de proveedor, cheque y pago.</span><span class="sxs-lookup"><span data-stu-id="7e707-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="7e707-109">Para obtener más información, vea [Exportar un archivo de Positive Pay](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="7e707-109">For more information, see [How to: Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="7e707-110">Su impresora tiene que haber configurado correctamente los documentos y usted deberá definir qué plantilla de cheques va a usar.</span><span class="sxs-lookup"><span data-stu-id="7e707-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="7e707-111">Para obtener más información , vea [Procedimiento: Definir plantillas de cheques](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="7e707-111">For more information, see [How to: Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="7e707-112">Para emitir cheques</span><span class="sxs-lookup"><span data-stu-id="7e707-112">To issue checks</span></span>
1. <span data-ttu-id="7e707-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7e707-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="7e707-114">Rellene el diario con los pagos relevantes, por ejemplo, mediante la función Proponer pagos a proveedores.</span><span class="sxs-lookup"><span data-stu-id="7e707-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="7e707-115">Para obtener más información, vea [Procedimiento: Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="7e707-115">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="7e707-116">En el campo **Tipo de pago bancario** en las líneas de diario para el pago que desea realizar mediante cheques, seleccione una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e707-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="7e707-117">**Cheque automático**: Seleccione esta opción si desea imprimir un cheque por el importe de la línea del diario de pagos.</span><span class="sxs-lookup"><span data-stu-id="7e707-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="7e707-118">Debe imprimir los cheques antes de que pueda registrar las líneas del diario.</span><span class="sxs-lookup"><span data-stu-id="7e707-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="7e707-119">solo puede seleccionar **Cheque automático** si el valor de **Tipo contrapartida** o el de **Tipo mov.** es **Cuenta banco**.</span><span class="sxs-lookup"><span data-stu-id="7e707-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="7e707-120">**Cheque manual**: Seleccione esta opción si ha creado manualmente un cheque y desea crear el movimiento de cheque correspondiente a ese importe.</span><span class="sxs-lookup"><span data-stu-id="7e707-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="7e707-121">Usando esta opción no puede imprimir cheques de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7e707-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7e707-122">solo puede seleccionar **Cheque manual** si el valor de **Tipo contrapartida** o el de **Tipo mov.** es **Cuenta banco**.</span><span class="sxs-lookup"><span data-stu-id="7e707-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="7e707-123">Debe imprimir los cheques automáticos antes de registrar las líneas del diario relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7e707-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="7e707-124">En el caso de los cheques automáticos, seleccione **Imprimir cheque**.</span><span class="sxs-lookup"><span data-stu-id="7e707-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="7e707-125">En la ventana **Cheque**, rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7e707-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="7e707-126">Elija el botón **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="7e707-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7e707-127">Si desea imprimir cheques en varias divisas de distintas cuentas bancarias, deberá ejecutar el trabajo por lotes **Imprimir cheque** por separado para cada divisa y especificar la cuenta bancaria correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7e707-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="7e707-128">Para anular los cheques imprimidos que no han sido registrados</span><span class="sxs-lookup"><span data-stu-id="7e707-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="7e707-129">Puede anular los cheques no registrados después de que hayan sido imprimidos usando la acción **Anular cheque** de la ventana **Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="7e707-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="7e707-130">En la ventana **Diario de pagos**, seleccione **Anular cheque** y, a continuación, seleccione que cheques desea cancelar.</span><span class="sxs-lookup"><span data-stu-id="7e707-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="7e707-131">Para anular cheques</span><span class="sxs-lookup"><span data-stu-id="7e707-131">To void checks</span></span>
<span data-ttu-id="7e707-132">Cuando se ha registrado el pago del cheque, solo puede cancelar (anular) cheques en los movimientos resultantes del banco.</span><span class="sxs-lookup"><span data-stu-id="7e707-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="7e707-133">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="7e707-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="7e707-134">Seleccione la cuenta bancaria correspondiente, seleccione la acción **Editar** y, a continuación, seleccione la acción **Movs. cheques**.</span><span class="sxs-lookup"><span data-stu-id="7e707-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="7e707-135">En la ventana **Movs. cheques**, seleccione la acción **Anular cheque**.</span><span class="sxs-lookup"><span data-stu-id="7e707-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="7e707-136">Seleccione la casilla **Anular cheque solo**.</span><span class="sxs-lookup"><span data-stu-id="7e707-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="7e707-137">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7e707-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e707-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e707-138">See Also</span></span>
[<span data-ttu-id="7e707-139">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="7e707-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="7e707-140">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="7e707-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="7e707-141">Exportar un archivo de Positive Pay</span><span class="sxs-lookup"><span data-stu-id="7e707-141">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="7e707-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7e707-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

