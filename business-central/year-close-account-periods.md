---
title: Cerrar periodos contables para un ejercicio | Documentos de Microsoft
description: Describe cómo cerrar los periodos contables que componen el ejercicio.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: ba6cd85d50f9d2b4d98fb45cbd38bcc57e08e3a2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313813"
---
# <a name="close-accounting-periods"></a>Cerrar periodos contables
Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.

## <a name="to-close-accounting-periods"></a>Para cerrar periodos contables
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Periodos contables** y luego elija el enlace relacionado.
2. En la página **Periodos contables**, elija la acción **Cerrar ejercicio**.

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
