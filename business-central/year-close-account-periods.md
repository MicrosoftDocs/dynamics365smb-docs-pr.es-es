---
title: Cerrar periodos contables para un ejercicio | Documentos de Microsoft
description: Describe cómo cerrar los periodos contables que componen el ejercicio.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a26baaf947fdac133e3bfcd50489d680231d9971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786687"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="0beab-103">Cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="0beab-103">Close Accounting Periods</span></span>
<span data-ttu-id="0beab-104">Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.</span><span class="sxs-lookup"><span data-stu-id="0beab-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="0beab-105">Para cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="0beab-105">To close accounting periods</span></span>
1. <span data-ttu-id="0beab-106">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Periodos contables** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="0beab-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="0beab-107">En la página **Periodos contables**, elija la acción **Cerrar ejercicio**.</span><span class="sxs-lookup"><span data-stu-id="0beab-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="0beab-108">Si hay más de un ejercicio abierto, se selecciona automáticamente el más antiguo para cerrarse.</span><span class="sxs-lookup"><span data-stu-id="0beab-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="0beab-109">Se muestra un mensaje para identificar el ejercicio que se va a cerrar y las consecuencias del cierre.</span><span class="sxs-lookup"><span data-stu-id="0beab-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="0beab-110">Para cerrar el ejercicio, elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="0beab-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="0beab-111">El ejercicio se ha cerrado y se seleccionan los campos **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio.</span><span class="sxs-lookup"><span data-stu-id="0beab-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="0beab-112">No se puede volver a abrir el ejercicio ni desactivar la casilla de verificación de los campos **Cerrado** o **Fecha inicial bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="0beab-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0beab-113">No puede cerrar un ejercicio antes de haber creado uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="0beab-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="0beab-114">Conviene advertir que, una vez cerrado un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.</span><span class="sxs-lookup"><span data-stu-id="0beab-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="0beab-115">Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="0beab-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="0beab-116">Al hacerlo, los movimientos se marcarán como registrados en un ejercicio cerrado y se seleccionará el campo **Asiento post-cierre**.</span><span class="sxs-lookup"><span data-stu-id="0beab-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="0beab-117">Después de cerrar un ejercicio, debe regularizar las cuentas de explotación y transferir los resultados del año a una cuenta del balance.</span><span class="sxs-lookup"><span data-stu-id="0beab-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="0beab-118">Puede repetirlo cada vez que registre el ejercicio cerrado.</span><span class="sxs-lookup"><span data-stu-id="0beab-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="0beab-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0beab-119">See Also</span></span>

[<span data-ttu-id="0beab-120">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="0beab-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="0beab-121">Registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="0beab-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="0beab-122">Trabajar con periodos contables y ejercicios</span><span class="sxs-lookup"><span data-stu-id="0beab-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="0beab-123">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0beab-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]