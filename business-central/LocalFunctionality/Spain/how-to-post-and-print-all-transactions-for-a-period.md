---
title: Registro e impresión de todas las transacciones de un periodo
description: Las empresas deben enviar los movimientos de transacciones de su negocio, agrupados por números de transacción, en un informe anual a la administración fiscal.
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
ms.author: sgroespe
ms.openlocfilehash: b17cbc70fb9f783aa44a952a88f5c2ad3fe47ed8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189177"
---
# <a name="post-and-print-all-transactions-for-a-period"></a><span data-ttu-id="26386-103">Registrar e imprimir todas las transacciones de un periodo</span><span class="sxs-lookup"><span data-stu-id="26386-103">Post and Print All Transactions for a Period</span></span>
<span data-ttu-id="26386-104">Las empresas deben enviar los movimientos de transacciones de su negocio, agrupados por números de transacción, en un informe anual a la administración fiscal.</span><span class="sxs-lookup"><span data-stu-id="26386-104">Companies must submit their business transaction entries, grouped by transaction numbers, in an annual report to tax authorities.</span></span> <span data-ttu-id="26386-105">Cada transacción de contabilidad debe tener un número secuencial para el ejercicio.</span><span class="sxs-lookup"><span data-stu-id="26386-105">Every general ledger transaction must have a sequential number for the fiscal year.</span></span> <span data-ttu-id="26386-106">Al registrar las transacciones, se asignarán números de transacción a los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="26386-106">Posting transactions will assign transaction numbers to general ledger entries.</span></span>  

## <a name="to-post-all-transactions-for-a-period"></a><span data-ttu-id="26386-107">Para registrar todas las transacciones de un periodo</span><span class="sxs-lookup"><span data-stu-id="26386-107">To post all transactions for a period</span></span>  

1.  <span data-ttu-id="26386-108">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Diario general** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="26386-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26386-109">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="26386-109">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="26386-110">Campo</span><span class="sxs-lookup"><span data-stu-id="26386-110">Field</span></span>|<span data-ttu-id="26386-111">Description</span><span class="sxs-lookup"><span data-stu-id="26386-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="26386-112">**Nombre sección**</span><span class="sxs-lookup"><span data-stu-id="26386-112">**Batch Name**</span></span>|<span data-ttu-id="26386-113">Seleccione el nombre de sección del diario requerido.</span><span class="sxs-lookup"><span data-stu-id="26386-113">Select the required general journal batch name.</span></span>|  
    |<span data-ttu-id="26386-114">**Nº asiento**</span><span class="sxs-lookup"><span data-stu-id="26386-114">**Transaction No.**</span></span>|<span data-ttu-id="26386-115">Escriba el número de transacción.</span><span class="sxs-lookup"><span data-stu-id="26386-115">Enter the transaction number.</span></span> <span data-ttu-id="26386-116">**Nota**: Si la transacción está saldada, el siguiente número aparecerá automáticamente y los detalles de transacción relacionados aparecerán en la siguiente fila.</span><span class="sxs-lookup"><span data-stu-id="26386-116">**Note:**  If the transaction is balanced, the next number displays automatically, and the related transaction details appear in the next row.</span></span> <span data-ttu-id="26386-117">Si la transacción no está saldada, aparecerá el mismo número de transacción con detalles de transacción relacionados.</span><span class="sxs-lookup"><span data-stu-id="26386-117">If the transaction is not balanced, the same transaction number is displayed with related transaction details.</span></span>|  

3.  <span data-ttu-id="26386-118">Elija la acción **Registrar** y el botón **Sí** para confirmar el registro.</span><span class="sxs-lookup"><span data-stu-id="26386-118">Choose the **Post** action, and then choose the **Yes** button to confirm posting.</span></span>  
4.  <span data-ttu-id="26386-119">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="26386-119">Choose the **OK** button.</span></span>  

    <span data-ttu-id="26386-120">Una vez registrado el diario, se asigna un número de transacción final a los movimientos del diario.</span><span class="sxs-lookup"><span data-stu-id="26386-120">After the journal is posted, a final transaction number is assigned to entries in the journal.</span></span> <span data-ttu-id="26386-121">Este número es secuencial, sin discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="26386-121">This number is a sequential, non-gap number.</span></span> <span data-ttu-id="26386-122">Por lo tanto, para cada ejercicio, todos los movimientos agrupados por su número de transacción se clasifican en orden secuencial, sin discontinuidades o espacios en blanco.</span><span class="sxs-lookup"><span data-stu-id="26386-122">Thus, for each fiscal year, all of the entries grouped by their transaction number are sorted by date in sequential order, with no gaps or blanks.</span></span>  

## <a name="to-print-all-transactions-for-a-period"></a><span data-ttu-id="26386-123">Para imprimir todas las transacciones de un periodo</span><span class="sxs-lookup"><span data-stu-id="26386-123">To print all transactions for a period</span></span>  

1.  <span data-ttu-id="26386-124">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Registro movs. contabilidad** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="26386-124">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Registers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="26386-125">Para definir el campo **Nº asiento periodo**</span><span class="sxs-lookup"><span data-stu-id="26386-125">To set the **Period Trans. No.**</span></span> <span data-ttu-id="26386-126">para todos los movimientos de contabilidad del periodo en un orden secuencial, elija **Asignar nº asiento periodo**.</span><span class="sxs-lookup"><span data-stu-id="26386-126">field for all of the general ledger entries in the period in a sequential order, choose the **Set Period Transaction No.**</span></span> <span data-ttu-id="26386-127">.</span><span class="sxs-lookup"><span data-stu-id="26386-127">action.</span></span>  
3.  <span data-ttu-id="26386-128">Seleccione los filtros apropiados.</span><span class="sxs-lookup"><span data-stu-id="26386-128">Select the appropriate filters.</span></span>  
4.  <span data-ttu-id="26386-129">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="26386-129">Choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="26386-130">Todas las transacciones se ordenan por fecha de registro y se asigna un número secuencial a cada movimiento del campo **Nº asiento periodo**</span><span class="sxs-lookup"><span data-stu-id="26386-130">All transactions are ordered by posting date, and a sequential number is assigned to each entry in the **Period Trans. No.**</span></span> <span data-ttu-id="26386-131">.</span><span class="sxs-lookup"><span data-stu-id="26386-131">field.</span></span>  

5.  <span data-ttu-id="26386-132">En la página **Registro movs. contabilidad**, elija la acción **Imprimir página**.</span><span class="sxs-lookup"><span data-stu-id="26386-132">On the **G/L Registers** page, choose the **Print Page** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26386-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26386-133">See Also</span></span>  
 [<span data-ttu-id="26386-134">Números de transacción</span><span class="sxs-lookup"><span data-stu-id="26386-134">Transaction Numbers</span></span>](transaction-numbers.md)
