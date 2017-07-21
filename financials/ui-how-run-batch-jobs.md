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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-run-batch-jobs"></a>Ejecución de trabajos por lotes
Un proceso es una rutina que procesa datos por lotes, por ejemplo, el proceso **Ajustar tipo cambio**. Hay procesos que realizan actividades contables periódicas como, por ejemplo, el asiento de regularización al final de un ejercicio. Muchos procesos realizan cálculos, como el cálculo de intereses, el ajuste tipo cambio y el cálculo de precios de venta.

Un trabajo por lotes es como un informe, excepto en que el primero usa los resultados de su trabajo para actualizar información directamente en lugar de imprimir los resultados.

## <a name="to-run-a-batch-job"></a>Para ejecutar un trabajo por lotes
1. Para abrir la ventana de solicitud para el proceso pertinente, en la esquina superior derecha, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca el nombre del proceso y, a continuación, seleccione el vínculo relacionado.
2. Si hay una ficha desplegable **Opciones** para el proceso, complete los campos para determinar lo que deberá hacer el proceso.
3. En la ventana se puede incluir una o varias fichas desplegables con filtros, que se podrán usar para limitar los datos que se incluirán en el proceso. Puede especificar criterios para los filtros sugeridos o añadir más filtros.
4. Elija el botón **Aceptar** para iniciar el trabajo por lotes.

## <a name="see-also"></a>Consulte también
[Introducir criterios en los filtros](ui-enter-criteria-filters.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

