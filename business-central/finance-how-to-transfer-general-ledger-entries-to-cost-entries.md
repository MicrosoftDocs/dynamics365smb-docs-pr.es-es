---
title: 'Procedimiento: transferencia de movimientos de contabilidad a los movimientos de coste | Documentos de Microsoft'
description: Puede transferir movimientos de contabilidad a movimientos de coste.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806547"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="8ab11-103">Transferir movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="8ab11-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="8ab11-104">Puede transferir movimientos de contabilidad a movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="8ab11-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="8ab11-105">Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de coste, debe preparar la transferencia para evitar el registro manual de corrección.</span><span class="sxs-lookup"><span data-stu-id="8ab11-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="8ab11-106">Para preparar la transferencia</span><span class="sxs-lookup"><span data-stu-id="8ab11-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="8ab11-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de contabilidad de costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ab11-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8ab11-108">En la página **Configuración contabilidad costes**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="8ab11-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="8ab11-109">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan tipos coste** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ab11-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="8ab11-110">En la página **Ficha tipo coste**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de coste para tomar movimientos de la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="8ab11-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="8ab11-111">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ab11-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="8ab11-112">Para cada cuenta contable correspondiente, en la página **Ficha cuenta**, compruebe que el campo **Nº tipo coste**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="8ab11-113">está vinculado correctamente a un tipo de coste.</span><span class="sxs-lookup"><span data-stu-id="8ab11-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="8ab11-114">Para obtener más información, consulte [Configuración de contabilidad de costes](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="8ab11-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="8ab11-115">Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de coste y a un objeto de coste.</span><span class="sxs-lookup"><span data-stu-id="8ab11-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="8ab11-116">Para transferir movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="8ab11-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="8ab11-117">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="8ab11-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8ab11-118">Para iniciar la transferencia, elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="8ab11-119">El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.</span><span class="sxs-lookup"><span data-stu-id="8ab11-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="8ab11-120">Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Movimiento de coste** y la tabla **Registro de costes**.</span><span class="sxs-lookup"><span data-stu-id="8ab11-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="8ab11-121">Esto permite realizar un seguimiento del origen de los movimientos de coste.</span><span class="sxs-lookup"><span data-stu-id="8ab11-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ab11-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ab11-122">See Also</span></span>  
<span data-ttu-id="8ab11-123">[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="8ab11-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="8ab11-124">Configuración de contabilidad de costes</span><span class="sxs-lookup"><span data-stu-id="8ab11-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
