---
title: Crear y ejecutar un proceso | Documentos de Microsoft
description: Puede ejecutar procesos para procesar datos y actualizar la información, por ejemplo, para actividades contables periódicas o para cálculos.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782258"
---
# <a name="run-batch-jobs-and-xmlports"></a>Ejecutar trabajos por lotes y XMLports
Un proceso es una rutina que procesa datos por lotes, por ejemplo, el proceso **Ajustar tipo cambio**. Hay procesos que realizan actividades contables periódicas como, por ejemplo, el asiento de regularización al final de un ejercicio. Muchos procesos realizan cálculos, como el cálculo de intereses, el ajuste tipo cambio y el cálculo de precios de venta.

Un trabajo por lotes es como un informe, excepto en que el primero usa los resultados de su trabajo para actualizar información directamente en lugar de imprimir los resultados.

Puede programar cuándo se ejecuta un trabajo por lotes. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Para ejecutar un trabajo por lotes
1. Para abrir la página de solicitud para el proceso pertinente, en la esquina superior derecha, seleccione el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca el nombre del proceso y, a continuación, seleccione el vínculo relacionado.
2. Si hay una ficha desplegable **Opciones** para el proceso, complete los campos para determinar lo que deberá hacer el proceso.
3. En la página se puede incluir una o varias fichas desplegables con filtros, que se podrán usar para limitar los datos que se incluirán en el proceso. Puede especificar criterios para los filtros sugeridos o añadir más filtros.
4. Elija el botón **Aceptar** para iniciar el trabajo por lotes.

## <a name="see-also"></a>Consulte también
[Ordenar, buscar y filtrar listas](ui-enter-criteria-filters.md)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]