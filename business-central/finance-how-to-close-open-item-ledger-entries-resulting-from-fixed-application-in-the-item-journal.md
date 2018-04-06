---
title: "Cómo cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos | Documentos de Microsoft"
description: "Puede utilizar el campo **Liquidar por mov.** en la ventana **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original. Por ejemplo, para corregir la transacción de salida o procesar su devolución."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879688bd458714f354b2e98e58ce78686cf79d9
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="2cf35-104">Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="2cf35-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="2cf35-105">Puede utilizar el campo **Liquidar por mov.** en la ventana **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original.</span><span class="sxs-lookup"><span data-stu-id="2cf35-105">You can use the **Applies-from Entry** field in the **Item Journal** window to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="2cf35-106">Por ejemplo, para corregir la transacción de salida o procesar su devolución.</span><span class="sxs-lookup"><span data-stu-id="2cf35-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="2cf35-107">Para obtener más información, consulte Liquidar por mov.</span><span class="sxs-lookup"><span data-stu-id="2cf35-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="2cf35-108">Las liquidaciones fijas realizadas de esta forma aplican solo al coste, no a la cantidad.</span><span class="sxs-lookup"><span data-stu-id="2cf35-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="2cf35-109">Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida liquidado y seguirá abierto.</span><span class="sxs-lookup"><span data-stu-id="2cf35-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="2cf35-110">Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.</span><span class="sxs-lookup"><span data-stu-id="2cf35-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="2cf35-111">Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="2cf35-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="2cf35-112">El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="2cf35-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="2cf35-113">Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="2cf35-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="2cf35-114">Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2cf35-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="2cf35-115">Esto cierra el movimiento negativo original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="2cf35-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="2cf35-116">Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo.</span><span class="sxs-lookup"><span data-stu-id="2cf35-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="2cf35-117">Esto cierra el movimiento positivo de corrección original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="2cf35-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2cf35-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2cf35-118">See Also</span></span>  
[<span data-ttu-id="2cf35-119">Eliminar y liquidar de nuevo los movimientos contables de producto</span><span class="sxs-lookup"><span data-stu-id="2cf35-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="2cf35-120">[Procesamiento de devoluciones de ventas y cancelaciones](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="2cf35-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="2cf35-121">[Configuración de valoración de existencias](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="2cf35-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="2cf35-122">[Gestión de costes de inventario](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="2cf35-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="2cf35-123">Detalles de diseño: Métodos de coste</span><span class="sxs-lookup"><span data-stu-id="2cf35-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)

