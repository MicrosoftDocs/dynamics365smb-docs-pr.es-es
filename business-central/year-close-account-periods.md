---
title: Cerrar periodos contables para un ejercicio | Documentos de Microsoft
description: Describe cómo cerrar los periodos contables que componen el ejercicio.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: a696f45446f93dba2dedb0976ff646dd6e4b12b1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195880"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="d4fd3-103">Cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="d4fd3-103">Close Accounting Periods</span></span>
<span data-ttu-id="d4fd3-104">Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="d4fd3-105">Para cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="d4fd3-105">To close accounting periods</span></span>
1. <span data-ttu-id="d4fd3-106">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Periodos contables** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="d4fd3-107">En la página **Periodos contables**, elija la acción **Cerrar ejercicio**.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="d4fd3-108">Si hay más de un ejercicio abierto, se selecciona automáticamente el más antiguo para cerrarse.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="d4fd3-109">Se muestra un mensaje para identificar el ejercicio que se va a cerrar y las consecuencias del cierre.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="d4fd3-110">Para cerrar el ejercicio, elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="d4fd3-111">El ejercicio se ha cerrado y se seleccionan los campos **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="d4fd3-112">No se puede volver a abrir el ejercicio ni desactivar la casilla de verificación de los campos **Cerrado** o **Fecha inicial bloqueada**.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d4fd3-113">No puede cerrar un ejercicio antes de haber creado uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="d4fd3-114">Conviene advertir que, una vez cerrado un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="d4fd3-115">Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="d4fd3-116">Al hacerlo, los movimientos se marcarán como registrados en un ejercicio cerrado y se seleccionará el campo **Asiento post-cierre**.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="d4fd3-117">Después de cerrar un ejercicio, debe regularizar las cuentas de explotación y transferir los resultados del año a una cuenta del balance.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="d4fd3-118">Puede repetirlo cada vez que registre el ejercicio cerrado.</span><span class="sxs-lookup"><span data-stu-id="d4fd3-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4fd3-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d4fd3-119">See Also</span></span>

[<span data-ttu-id="d4fd3-120">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="d4fd3-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="d4fd3-121">Registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="d4fd3-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="d4fd3-122">Trabajar con periodos contables y ejercicios</span><span class="sxs-lookup"><span data-stu-id="d4fd3-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="d4fd3-123">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4fd3-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
