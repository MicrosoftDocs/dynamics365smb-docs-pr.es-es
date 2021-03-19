---
title: Revertir registro de salida | Documentos de Microsoft
description: En ciertas ocasiones es necesario revertir el registro de la salida. Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5901ad209149c113497d676a5c86379fc8424a0e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392754"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="49aa6-104">Revertir el registro de la salida</span><span class="sxs-lookup"><span data-stu-id="49aa6-104">Reverse Output Posting</span></span>
<span data-ttu-id="49aa6-105">En ciertas ocasiones es necesario revertir el registro de la salida.</span><span class="sxs-lookup"><span data-stu-id="49aa6-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="49aa6-106">Por ejemplo, si se ha cometido un error en la introducción de los datos y se ha registrado una cantidad de salida incorrecta en una orden de producción.</span><span class="sxs-lookup"><span data-stu-id="49aa6-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="49aa6-107">Para revertir un registro de salida</span><span class="sxs-lookup"><span data-stu-id="49aa6-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="49aa6-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="49aa6-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="49aa6-109">Seleccione el lote.</span><span class="sxs-lookup"><span data-stu-id="49aa6-109">Select your batch.</span></span>  
2. <span data-ttu-id="49aa6-110">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="49aa6-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="49aa6-111">Para obtener más información, vea [Registro de salida y tiempos de ejecución por lotes](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="49aa6-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="49aa6-112">En el campo **Liq. por nº orden**, seleccione el movimiento de contabilidad de productos asociado.</span><span class="sxs-lookup"><span data-stu-id="49aa6-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="49aa6-113">De esta forma se reserva la capacidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="49aa6-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="49aa6-114">Registre la reversión registrando el diario.</span><span class="sxs-lookup"><span data-stu-id="49aa6-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="49aa6-115">Los movimientos del diario de salida se registran como un ajuste positivo.</span><span class="sxs-lookup"><span data-stu-id="49aa6-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="49aa6-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="49aa6-116">See Also</span></span>  
 <span data-ttu-id="49aa6-117">[Fabricación](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="49aa6-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="49aa6-118">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="49aa6-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="49aa6-119">[Planificación](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="49aa6-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="49aa6-120">Inventario</span><span class="sxs-lookup"><span data-stu-id="49aa6-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="49aa6-121">Compras</span><span class="sxs-lookup"><span data-stu-id="49aa6-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="49aa6-122">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="49aa6-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]