---
title: Crear y ejecutar un proceso | Documentos de Microsoft
description: "Puede ejecutar procesos para procesar datos y actualizar la información, por ejemplo, para actividades contables periódicas o para cálculos."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ac50d0ca59ece5365c000a9bfca06a0c18654512
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="run-batch-jobs"></a>Ejecutar procesos
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
