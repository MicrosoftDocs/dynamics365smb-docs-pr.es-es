---
title: Registrar el movimiento de cierre del ejercicio
description: Describe cómo abrir el diario especificado en el proceso Asiento regularización y, a continuación, revisar y registrar el movimiento de cierre de ejercicio.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493358"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="c6294-103">Registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="c6294-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="c6294-104">Después de usar el proceso **Asiento regularización** para generar los movimientos de cierre de fin de año, debe abrir el diario especificado en el proceso y revisar y registrar los movimientos.</span><span class="sxs-lookup"><span data-stu-id="c6294-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="c6294-105">Dependiendo de los procesos de trabajo de su organización, puede optar por cerrar o no los períodos contables y los ejercicios en [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6294-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c6294-106">El siguiente procedimiento asume que ha cerrado el ejercicio utilizando la opción *Periodos contables*, ha generado una entrada de cierre de año utilizando el trabajo por lotes **Cerrar balance de ingresos** , y ahora está listos para contabilizar el movimiento de cierre de fin de año junto con las entradas de la cuenta de desplazamiento de capital.</span><span class="sxs-lookup"><span data-stu-id="c6294-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="c6294-107">Su organización puede optar por trabajar de manera diferente, como contabilizar la entrada de cierre de fin de año como parte del cierre del ejercicio.</span><span class="sxs-lookup"><span data-stu-id="c6294-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="c6294-108">Para registrar el movimiento de cierre del ejercicio</span><span class="sxs-lookup"><span data-stu-id="c6294-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="c6294-109">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="c6294-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c6294-110">En la página **Diario general**, en el campo **Nombre de sección**, seleccione la sección que contiene los movimientos de cierre.</span><span class="sxs-lookup"><span data-stu-id="c6294-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="c6294-111">Revise los movimientos.</span><span class="sxs-lookup"><span data-stu-id="c6294-111">Review the entries.</span></span>
4. <span data-ttu-id="c6294-112">Para registrar el diario, elija la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="c6294-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="c6294-113">Si se detecta algún error, se mostrará un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="c6294-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="c6294-114">Si el registro es correcto, se eliminan los movimientos registrados del diario.</span><span class="sxs-lookup"><span data-stu-id="c6294-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="c6294-115">Una vez registrados, los movimientos se registran en cada una de las cuentas de regularización, de forma que sus saldos pasan a ser cero y el resultado del año se transfiere al balance.</span><span class="sxs-lookup"><span data-stu-id="c6294-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6294-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c6294-116">See Also</span></span>

[<span data-ttu-id="c6294-117">Cerrar periodos contables</span><span class="sxs-lookup"><span data-stu-id="c6294-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="c6294-118">Cierre de libros</span><span class="sxs-lookup"><span data-stu-id="c6294-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="c6294-119">Asiento regularización</span><span class="sxs-lookup"><span data-stu-id="c6294-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="c6294-120">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c6294-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]