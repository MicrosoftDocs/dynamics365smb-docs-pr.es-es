---
title: "Cerrar asiento de regularización | Documentos de Microsoft"
description: "Explica cómo cerrar un asiento de regularización."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: dde7b93c6a3dcf78173494f1c6fa09a38207e676
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="close-income-statement"></a>Asiento regularización
Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman. Para ello, puede ejecutar el proceso **Cerrar asiento de regularización**. Esta tarea transfiere el resultado anual a una cuenta en la hoja de balance y cierra las cuentas del balance de ingresos. Se realiza creando líneas en un diario, que después puede registrar.

## <a name="to-run-the-close-income-statement-batch-job"></a>Para ejecutar el proceso Cerrar asiento de regularización
1. Cierre el ejercicio fiscal. Antes de ejecutar el proceso se debe cerrar el ejercicio fiscal. Para obtener más información, vea [Procedimiento: Cerrar periodos contables](year-close-account-periods.md).
2. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Asiento regularización** y elija el vínculo relacionado.
3. Elija el botón **Aceptar** para iniciar el trabajo por lotes.

## <a name="about-the-close-income-statement-batch-job"></a>Acerca del proceso Cerrar asiento de regularización
El trabajo por lotes procesa todas las cuentas generales del tipo balance de ingresos y crea movimientos que cancelan los saldos respectivos. Es decir, cada movimiento es la suma de todos los movimientos de contabilidad de la cuenta del ejercicio. Estos nuevos movimientos se disponen en un diario, en el que debe especificar una cuenta de contrapartida y una cuenta de retención de beneficios en el balance antes del registro. Cuando se registra el diario, también se registra un movimiento en cada cuenta del comercial, de manera que su saldo sea cero y, a la vez, el resultado del año se transfiera al balance.

Debe registrar el diario manualmente. El trabajo por lotes no registra los movimientos automáticamente, salvo cuando se utiliza una divisa adicional. En ese caso, el proceso registra los movimientos directamente en contabilidad.

La fecha de las líneas que inserta el trabajo por lotes en el diario siempre es una fecha de cierre de ejercicio. La U-fecha es una fecha ficticia comprendida entre el último día de un ejercicio y el día primero del siguiente. La ventaja de registrar en una U-fecha es que se mantienen los saldos correctos para las fechas ordinarias del ejercicio.

El proceso **Cerrar asiento de regularización** se puede usar varias veces. Puede registrar en un ejercicio anterior, incluso después de que haya cerrado las cuentas de comercial (siempre que vuelva a ejecutar nuevamente este proceso).

## <a name="see-also"></a>Consulte también
[Cierre de libros](year-close-books.md)  
[Registrar movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md)  
[Abrir un nuevo ejercicio](finance-how-open-new-fiscal-year.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

