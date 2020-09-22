---
title: Revertir registro de salida | Documentos de Microsoft
description: En ciertas ocasiones es necesario revertir el registro de la salida. Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788755"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="11d90-104">Revertir el registro de la salida</span><span class="sxs-lookup"><span data-stu-id="11d90-104">Reverse Output Posting</span></span>
<span data-ttu-id="11d90-105">En ciertas ocasiones es necesario revertir el registro de la salida.</span><span class="sxs-lookup"><span data-stu-id="11d90-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="11d90-106">Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="11d90-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="11d90-107">Para revertir un registro de salida</span><span class="sxs-lookup"><span data-stu-id="11d90-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="11d90-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="11d90-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="11d90-109">Seleccione el lote.</span><span class="sxs-lookup"><span data-stu-id="11d90-109">Select your batch.</span></span>  
2. <span data-ttu-id="11d90-110">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11d90-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="11d90-111">Para obtener más información, vea [Registro de salida y tiempos de ejecución por lotes](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="11d90-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="11d90-112">En el campo **Liq. por nº orden**, seleccione el movimiento de contabilidad de productos asociado.</span><span class="sxs-lookup"><span data-stu-id="11d90-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="11d90-113">De esta forma se reserva la capacidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="11d90-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="11d90-114">Registre la reversión registrando el diario.</span><span class="sxs-lookup"><span data-stu-id="11d90-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="11d90-115">Los movimientos del diario de salida se registran como un ajuste positivo.</span><span class="sxs-lookup"><span data-stu-id="11d90-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11d90-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11d90-116">See Also</span></span>  
 <span data-ttu-id="11d90-117">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="11d90-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="11d90-118">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="11d90-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="11d90-119">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="11d90-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="11d90-120">Inventario</span><span class="sxs-lookup"><span data-stu-id="11d90-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="11d90-121">Compras</span><span class="sxs-lookup"><span data-stu-id="11d90-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="11d90-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11d90-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
