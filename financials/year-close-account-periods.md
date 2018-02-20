---
title: Cerrar periodos contables para un ejercicio | Documentos de Microsoft
description: "Describe cómo cerrar los periodos contables que componen el ejercicio."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e136195c7b89635ca85601cdae5047493c237d09
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="close-accounting-periods"></a>Cerrar periodos contables
Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.

## <a name="to-close-accounting-periods"></a>Para cerrar periodos contables
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Periodos contables** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Periodos contables**, elija la acción **Fijar cierre**.

    Si hay más de un ejercicio abierto, se selecciona automáticamente el más antiguo para cerrarse. Se muestra un mensaje para identificar el ejercicio que se va a cerrar y las consecuencias del cierre.
3. Para cerrar el ejercicio, elija el botón **Sí**.

El ejercicio se ha cerrado y se seleccionan los campos **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio. No se puede volver a abrir el ejercicio ni desactivar la casilla de verificación de los campos **Cerrado** o **Fecha inicial bloqueada**.

> [!NOTE]  
>   No puede cerrar un ejercicio antes de haber creado uno nuevo. Conviene advertir que, una vez cerrado un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.

Incluso aunque un ejercicio se haya cerrado, todavía podrá registrar en él movimientos de contabilidad. Al hacerlo, los movimientos se marcarán como registrados en un ejercicio cerrado y se seleccionará el campo **Asiento post-cierre**.

Después de cerrar un ejercicio, debe regularizar las cuentas de explotación y transferir los resultados del año a una cuenta del balance. Puede repetirlo cada vez que registre el ejercicio cerrado.

## <a name="see-also"></a>Consulte también
[Cierre de libros](year-close-books.md)  
[Registrar el movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md)  
[Abrir un nuevo ejercicio](finance-how-open-new-fiscal-year.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

