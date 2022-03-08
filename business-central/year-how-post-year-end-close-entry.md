---
title: Revisar y registrar el movimiento de cierre del ejercicio | Documentos de Microsoft
description: Describe cómo abrir el diario especificado en el proceso Asiento regularización y, a continuación, revisar y registrar el movimiento de cierre de ejercicio.
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
ms.openlocfilehash: bafb11ebe021a07ad9f9d8b9af36e68cf9cb94d0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314358"
---
# <a name="post-the-year-end-closing-entry"></a>Registrar el movimiento de cierre del ejercicio
Después de usar el proceso **Asiento regularización** para generar los movimientos de cierre de fin de año, debe abrir el diario especificado en el proceso y revisar y registrar los movimientos.

## <a name="to-post-the-year-end-closing-entry"></a>Para registrar el movimiento de cierre del ejercicio
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario general** y luego elija el enlace relacionado.
2. En la página **Diario general**, en el campo **Nombre de sección**, seleccione la sección que contiene los movimientos de cierre.
3. Revise los movimientos.
4. Para registrar el diario, elija la acción **Registrar**.

> [!NOTE]  
>   Si se detecta algún error, se mostrará un mensaje de error. Si el registro es correcto, se eliminan los movimientos registrados del diario. Una vez registrados, los movimientos se registran en cada una de las cuentas de regularización, de forma que sus saldos pasan a ser cero y el resultado del año se transfiere al balance.

## <a name="see-also"></a>Consulte también
[Cerrar periodos contables](year-close-account-periods.md)  
[Cierre de libros](year-close-books.md)  
[Asiento regularización](year-close-income-statement.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
