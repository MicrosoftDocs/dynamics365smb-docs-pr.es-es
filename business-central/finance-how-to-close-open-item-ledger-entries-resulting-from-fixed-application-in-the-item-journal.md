---
title: Cómo cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos | Documentos de Microsoft
description: Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original. Por ejemplo, para corregir la transacción de salida o procesar su devolución.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 7a7f31ea698a314d8a69c3bf9c2e7ab04ccd5f46
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783454"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="38136-104">Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="38136-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="38136-105">Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original.</span><span class="sxs-lookup"><span data-stu-id="38136-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="38136-106">Por ejemplo, para corregir la transacción de salida o procesar su devolución.</span><span class="sxs-lookup"><span data-stu-id="38136-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="38136-107">Para obtener más información, consulte Liquidar por mov.</span><span class="sxs-lookup"><span data-stu-id="38136-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="38136-108">Las liquidaciones fijas realizadas de esta forma aplican solo al coste, no a la cantidad.</span><span class="sxs-lookup"><span data-stu-id="38136-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="38136-109">Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida liquidado y seguirá abierto.</span><span class="sxs-lookup"><span data-stu-id="38136-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="38136-110">Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.</span><span class="sxs-lookup"><span data-stu-id="38136-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="38136-111">Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="38136-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="38136-112">El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="38136-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="38136-113">Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="38136-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="38136-114">Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="38136-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="38136-115">Esto cierra el movimiento negativo original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="38136-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="38136-116">Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo.</span><span class="sxs-lookup"><span data-stu-id="38136-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="38136-117">Esto cierra el movimiento positivo de corrección original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="38136-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="38136-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38136-118">See Also</span></span>  
[<span data-ttu-id="38136-119">Eliminar y liquidar de nuevo los movimientos contables de producto</span><span class="sxs-lookup"><span data-stu-id="38136-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="38136-120">[Procesamiento de devoluciones de ventas y cancelaciones](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="38136-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="38136-121">[Configuración de valoración de existencias](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="38136-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="38136-122">[Gestión de costes de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="38136-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="38136-123">Detalles de diseño: Métodos de coste</span><span class="sxs-lookup"><span data-stu-id="38136-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
