---
title: Crear y ejecutar un proceso | Documentos de Microsoft
description: Puede ejecutar procesos para procesar datos y actualizar la información, por ejemplo, para actividades contables periódicas o para cálculos.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 260cd7761b130bbe3748de3cc109a9f4f56c1384
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2019
ms.locfileid: "853263"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="a9c14-103">Ejecutar procesos</span><span class="sxs-lookup"><span data-stu-id="a9c14-103">Run Batch Jobs</span></span>
<span data-ttu-id="a9c14-104">Un proceso es una rutina que procesa datos por lotes, por ejemplo, el proceso **Ajustar tipo cambio**.</span><span class="sxs-lookup"><span data-stu-id="a9c14-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="a9c14-105">Hay procesos que realizan actividades contables periódicas como, por ejemplo, el asiento de regularización al final de un ejercicio.</span><span class="sxs-lookup"><span data-stu-id="a9c14-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="a9c14-106">Muchos procesos realizan cálculos, como el cálculo de intereses, el ajuste tipo cambio y el cálculo de precios de venta.</span><span class="sxs-lookup"><span data-stu-id="a9c14-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="a9c14-107">Un trabajo por lotes es como un informe, excepto en que el primero usa los resultados de su trabajo para actualizar información directamente en lugar de imprimir los resultados.</span><span class="sxs-lookup"><span data-stu-id="a9c14-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="a9c14-108">Para ejecutar un trabajo por lotes</span><span class="sxs-lookup"><span data-stu-id="a9c14-108">To run a batch job</span></span>
1. <span data-ttu-id="a9c14-109">Para abrir la página de solicitud para el proceso pertinente, en la esquina superior derecha, seleccione el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), introduzca el nombre del proceso y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a9c14-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="a9c14-110">Si hay una ficha desplegable **Opciones** para el proceso, complete los campos para determinar lo que deberá hacer el proceso.</span><span class="sxs-lookup"><span data-stu-id="a9c14-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="a9c14-111">En la página se puede incluir una o varias fichas desplegables con filtros, que se podrán usar para limitar los datos que se incluirán en el proceso.</span><span class="sxs-lookup"><span data-stu-id="a9c14-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="a9c14-112">Puede especificar criterios para los filtros sugeridos o añadir más filtros.</span><span class="sxs-lookup"><span data-stu-id="a9c14-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="a9c14-113">Elija el botón **Aceptar** para iniciar el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="a9c14-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9c14-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9c14-114">See Also</span></span>
[<span data-ttu-id="a9c14-115">Ordenar, buscar y filtrar listas</span><span class="sxs-lookup"><span data-stu-id="a9c14-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="a9c14-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9c14-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
