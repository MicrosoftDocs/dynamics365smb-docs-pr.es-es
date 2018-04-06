---
title: Crear y ejecutar un proceso | Documentos de Microsoft
description: "Puede ejecutar procesos para procesar datos y actualizar la información, por ejemplo, para actividades contables periódicas o para cálculos."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8478a983da5020a4a7a49f6212c45a7a4c4d21a3
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="5e8fe-103">Ejecutar procesos</span><span class="sxs-lookup"><span data-stu-id="5e8fe-103">Run Batch Jobs</span></span>
<span data-ttu-id="5e8fe-104">Un proceso es una rutina que procesa datos por lotes, por ejemplo, el proceso **Ajustar tipo cambio**.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="5e8fe-105">Hay procesos que realizan actividades contables periódicas como, por ejemplo, el asiento de regularización al final de un ejercicio.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="5e8fe-106">Muchos procesos realizan cálculos, como el cálculo de intereses, el ajuste tipo cambio y el cálculo de precios de venta.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="5e8fe-107">Un trabajo por lotes es como un informe, excepto en que el primero usa los resultados de su trabajo para actualizar información directamente en lugar de imprimir los resultados.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="5e8fe-108">Para ejecutar un trabajo por lotes</span><span class="sxs-lookup"><span data-stu-id="5e8fe-108">To run a batch job</span></span>
1. <span data-ttu-id="5e8fe-109">Para abrir la ventana de solicitud para el proceso pertinente, en la esquina superior derecha, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca el nombre del proceso y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="5e8fe-110">Si hay una ficha desplegable **Opciones** para el proceso, complete los campos para determinar lo que deberá hacer el proceso.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="5e8fe-111">En la ventana se puede incluir una o varias fichas desplegables con filtros, que se podrán usar para limitar los datos que se incluirán en el proceso.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="5e8fe-112">Puede especificar criterios para los filtros sugeridos o añadir más filtros.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="5e8fe-113">Elija el botón **Aceptar** para iniciar el trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="5e8fe-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e8fe-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5e8fe-114">See Also</span></span>
[<span data-ttu-id="5e8fe-115">Introducir criterios en los filtros</span><span class="sxs-lookup"><span data-stu-id="5e8fe-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="5e8fe-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e8fe-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

