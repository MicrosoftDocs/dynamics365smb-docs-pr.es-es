---
title: Registrar pagos de adeudo directo SEPA | Documentos de Microsoft
description: "Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 021c48efc6bf6b1fdb7b17bf742cb6f084d3964b
ms.contentlocale: es-es
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="f0464-103">Registro de recibos de pagos de domiciliación de adeudo directo SEPA</span><span class="sxs-lookup"><span data-stu-id="f0464-103">How to: Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="f0464-104">Cuando el banco procesa correctamente un cobro por adeudo directo, puede proceder con el registro de la recepción del pago para las facturas de venta implicadas.</span><span class="sxs-lookup"><span data-stu-id="f0464-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="f0464-105">Para obtener más información, consulte [Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="f0464-105">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="f0464-106">Puede registrar el recibo de pago directamente desde la ventana **Cobros por adeudo directo** o la ventana **Movimientos de cobros por adeudo directo**.</span><span class="sxs-lookup"><span data-stu-id="f0464-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="f0464-107">Como alternativa, puede delegar el trabajo a otro usuario mediante la preparación de las líneas de diario relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f0464-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="f0464-108">Registro de un recibo de pago de domiciliación desde la ventana Cobros por adeudo directo</span><span class="sxs-lookup"><span data-stu-id="f0464-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="f0464-109">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cobros por adeudo directo** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f0464-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0464-110">Seleccione una línea para un cobro por adeudo directo que se ha exportado a un archivo de banco y procesado correctamente por el banco.</span><span class="sxs-lookup"><span data-stu-id="f0464-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="f0464-111">Para obtener más información, consulte [Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="f0464-111">For more information, see [How to: Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="f0464-112">Seleccione la acción **Registrar recibos de pago**.</span><span class="sxs-lookup"><span data-stu-id="f0464-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="f0464-113">En la ventana **Registrar cobro por adeudo directo**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f0464-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f0464-114">Campo</span><span class="sxs-lookup"><span data-stu-id="f0464-114">Field</span></span>|<span data-ttu-id="f0464-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0464-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f0464-116">**Nº cobro por adeudo directo**</span><span class="sxs-lookup"><span data-stu-id="f0464-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="f0464-117">Especifique el cobro por adeudo directo para el que desea registrar el albarán de pago.</span><span class="sxs-lookup"><span data-stu-id="f0464-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="f0464-118">**Plantilla de libros diario general**</span><span class="sxs-lookup"><span data-stu-id="f0464-118">**General Journal Template**</span></span>|<span data-ttu-id="f0464-119">Especifique la plantilla de diario general que se debe usar para registrar el albarán de pago, tal como la plantilla de recibo de cobro.</span><span class="sxs-lookup"><span data-stu-id="f0464-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="f0464-120">**Nombre sección diario general**</span><span class="sxs-lookup"><span data-stu-id="f0464-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="f0464-121">Especifique qué sección del diario general se debe usar para registrar el albarán de pago.</span><span class="sxs-lookup"><span data-stu-id="f0464-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="f0464-122">**Crear solo diario**</span><span class="sxs-lookup"><span data-stu-id="f0464-122">**Create Journal Only**</span></span>|<span data-ttu-id="f0464-123">Seleccione esta casilla si no desea registrar el recibo de pago al seleccionar el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0464-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="f0464-124">El recibo de pago se preparará en el diario especificado y no se registrará hasta que alguien registre las líneas de diario en cuestión.</span><span class="sxs-lookup"><span data-stu-id="f0464-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="f0464-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f0464-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0464-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f0464-126">See Also</span></span>  
 <span data-ttu-id="f0464-127">[Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="f0464-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="f0464-128">Ccial</span><span class="sxs-lookup"><span data-stu-id="f0464-128">Sales</span></span>](sales-manage-sales.md)

