---
title: Cerrar entradas del libro mayor de artículos que provienen del uso de una aplicación fija
description: Aprenda a crear una aplicación fija entre una transacción de entrada y la transacción de salida original en el diario de productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4fac4871fdf42210dfd48ca6dd7d9c2fede0c7ef
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788288"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="bcb01-103">Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="bcb01-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="bcb01-104">Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original.</span><span class="sxs-lookup"><span data-stu-id="bcb01-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="bcb01-105">Por ejemplo, para corregir la transacción de salida o procesar su devolución.</span><span class="sxs-lookup"><span data-stu-id="bcb01-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="bcb01-106">Las liquidaciones fijas realizadas de esta forma aplican solo al coste, no a la cantidad.</span><span class="sxs-lookup"><span data-stu-id="bcb01-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="bcb01-107">Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida liquidado y seguirá abierto.</span><span class="sxs-lookup"><span data-stu-id="bcb01-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="bcb01-108">Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.</span><span class="sxs-lookup"><span data-stu-id="bcb01-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="bcb01-109">Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.</span><span class="sxs-lookup"><span data-stu-id="bcb01-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="bcb01-110">Puede cambiar y volver a liquidar los movimientos de liquidación en determinadas condiciones mediante la página **Hoja liquidación**.</span><span class="sxs-lookup"><span data-stu-id="bcb01-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="bcb01-111">El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="bcb01-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="bcb01-112">Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos</span><span class="sxs-lookup"><span data-stu-id="bcb01-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="bcb01-113">Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcb01-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="bcb01-114">Esto cierra el movimiento negativo original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="bcb01-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="bcb01-115">El campo **Liquidar por mov.** especifica el número del movimiento de productos de salida cuyo coste se desvía al movimiento de producto de entrada cuando se registra una transacción de entrada de tipo **Entrada** o **Compra** con el diario de productos.</span><span class="sxs-lookup"><span data-stu-id="bcb01-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="bcb01-116">Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo.</span><span class="sxs-lookup"><span data-stu-id="bcb01-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="bcb01-117">Esto cierra el movimiento positivo de corrección original con una liquidación fija.</span><span class="sxs-lookup"><span data-stu-id="bcb01-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="bcb01-118">El campo **Liq. por nº orden** especifica si la cantidad que aparece en la línea del diario de productos debe liquidarse en un documento ya registrado.</span><span class="sxs-lookup"><span data-stu-id="bcb01-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="bcb01-119">Si es así, introduzca el número de movimiento del producto sobre el que debería liquidarse la línea del diario.</span><span class="sxs-lookup"><span data-stu-id="bcb01-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcb01-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcb01-120">See Also</span></span>

[<span data-ttu-id="bcb01-121">Eliminar y liquidar de nuevo los movimientos contables de producto</span><span class="sxs-lookup"><span data-stu-id="bcb01-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="bcb01-122">Procesamiento de devoluciones de ventas y cancelaciones</span><span class="sxs-lookup"><span data-stu-id="bcb01-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="bcb01-123">Configuración de valoración de existencias</span><span class="sxs-lookup"><span data-stu-id="bcb01-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="bcb01-124">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="bcb01-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="bcb01-125">Detalles de diseño: Métodos de coste</span><span class="sxs-lookup"><span data-stu-id="bcb01-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]