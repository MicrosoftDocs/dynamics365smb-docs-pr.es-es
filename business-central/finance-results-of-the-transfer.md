---
title: Resultados de transferencia | Documentos de Microsoft
description: En este tema se describe qué ocurre después de transferir movimientos de contabilidad a los movimientos de coste.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0e17ff5ad60014cba6ce866c9ddae848b1239167
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806232"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="9a288-103">Los resultados de la transferencia de movimientos de contabilidad a movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="9a288-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="9a288-104">Durante la transferencia de movimientos de contabilidad a movimientos de coste, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Movimiento de coste** y la tabla **Registro de costes** para permitir realizar un seguimiento de las conexiones entre los movimientos de costes y los movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="9a288-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="9a288-105">Movs. contabilidad</span><span class="sxs-lookup"><span data-stu-id="9a288-105">General Ledger Entries</span></span>  
<span data-ttu-id="9a288-106">Para cada movimiento de contabilidad que se transfiere a la contabilidad de costes, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellena el campo de coste **N.º mov.**.</span><span class="sxs-lookup"><span data-stu-id="9a288-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="9a288-107">Movs. coste</span><span class="sxs-lookup"><span data-stu-id="9a288-107">Cost Entries</span></span>  
<span data-ttu-id="9a288-108">Para cada movimiento de coste, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Movimiento de coste**.</span><span class="sxs-lookup"><span data-stu-id="9a288-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="9a288-109">Para movimientos de coste combinados, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.</span><span class="sxs-lookup"><span data-stu-id="9a288-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="9a288-110">El campo **Cuenta** en la tabla **Movimiento de coste** contiene el número de la cuenta de la que provino el movimiento de coste.</span><span class="sxs-lookup"><span data-stu-id="9a288-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="9a288-111">Para movimientos de coste únicos, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="9a288-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="9a288-112">Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados.</span><span class="sxs-lookup"><span data-stu-id="9a288-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="9a288-113">Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.</span><span class="sxs-lookup"><span data-stu-id="9a288-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="9a288-114">Registro costes</span><span class="sxs-lookup"><span data-stu-id="9a288-114">Cost Register</span></span>  
<span data-ttu-id="9a288-115">En la tabla **Registro de costes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea un movimiento con la transferencia de origen de la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="9a288-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="9a288-116">El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de coste creados.</span><span class="sxs-lookup"><span data-stu-id="9a288-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a288-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9a288-117">See Also</span></span>  
[<span data-ttu-id="9a288-118">Transferencia y registro de movimientos de coste</span><span class="sxs-lookup"><span data-stu-id="9a288-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
