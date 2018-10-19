---
title: 'Procedimiento: transferencia de movimientos de contabilidad a los movimientos de coste | Documentos de Microsoft'
description: Puede transferir movimientos de contabilidad a movimientos de coste.
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 62ed00ef7ca278245b9cdd1a28a4ee70cf9a8f11
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="12e21-103">Transferir movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="12e21-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="12e21-104">Puede transferir movimientos de contabilidad a movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="12e21-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="12e21-105">Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de coste, debe preparar la transferencia para evitar el registro manual de corrección.</span><span class="sxs-lookup"><span data-stu-id="12e21-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="12e21-106">Para preparar la transferencia</span><span class="sxs-lookup"><span data-stu-id="12e21-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="12e21-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de contabilidad de costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="12e21-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="12e21-108">En la ventana **Configuración contabilidad costes**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="12e21-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="12e21-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan tipos coste** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="12e21-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="12e21-110">En la ventana **Ficha tipo coste**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de coste para tomar movimientos de la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="12e21-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="12e21-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="12e21-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="12e21-112">Para cada cuenta contable correspondiente, en la ventana **Ficha cuenta**, compruebe que el campo **Nº tipo coste**</span><span class="sxs-lookup"><span data-stu-id="12e21-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="12e21-113">está vinculado correctamente a un tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="12e21-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="12e21-114">Para obtener más información, consulte [Definición de la relación entre los tipos de coste y las cuentas de contabilidad](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="12e21-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="12e21-115">Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de coste y a un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="12e21-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="12e21-116">Para transferir movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="12e21-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="12e21-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="12e21-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="12e21-118">Para iniciar la transferencia, elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="12e21-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="12e21-119">El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.</span><span class="sxs-lookup"><span data-stu-id="12e21-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="12e21-120">Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Movimiento de coste** y la tabla **Registro de costes**.</span><span class="sxs-lookup"><span data-stu-id="12e21-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="12e21-121">Esto permite realizar un seguimiento del origen de los movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="12e21-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12e21-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12e21-122">See Also</span></span>  
 <span data-ttu-id="12e21-123">[Criterios para la transferencia de movimientos de contabilidad a movimientos de coste](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="12e21-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="12e21-124">[Transferencia automática y movimientos combinados](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="12e21-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="12e21-125">[Resultados de la transferencia](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="12e21-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="12e21-126">[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="12e21-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="12e21-127">Definición de la relación entre los tipos de coste y las cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="12e21-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

