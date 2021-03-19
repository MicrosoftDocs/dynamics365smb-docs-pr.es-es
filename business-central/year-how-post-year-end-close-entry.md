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
# <a name="post-the-year-end-closing-entry"></a>Registrar el movimiento de cierre del ejercicio

Después de usar el proceso **Asiento regularización** para generar los movimientos de cierre de fin de año, debe abrir el diario especificado en el proceso y revisar y registrar los movimientos.  

> [!TIP]
> Dependiendo de los procesos de trabajo de su organización, puede optar por cerrar o no los períodos contables y los ejercicios en [!INCLUDE [prod_short](includes/prod_short.md)]. El siguiente procedimiento asume que ha cerrado el ejercicio utilizando la opción *Periodos contables*, ha generado una entrada de cierre de año utilizando el trabajo por lotes **Cerrar balance de ingresos** , y ahora está listos para contabilizar el movimiento de cierre de fin de año junto con las entradas de la cuenta de desplazamiento de capital. Su organización puede optar por trabajar de manera diferente, como contabilizar la entrada de cierre de fin de año como parte del cierre del ejercicio.

## <a name="to-post-the-year-end-closing-entry"></a>Para registrar el movimiento de cierre del ejercicio

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general** y luego elija el enlace relacionado.
2. En la página **Diario general**, en el campo **Nombre de sección**, seleccione la sección que contiene los movimientos de cierre.
3. Revise los movimientos.
4. Para registrar el diario, elija la acción **Registrar**.

> [!NOTE]  
> Si se detecta algún error, se mostrará un mensaje de error. Si el registro es correcto, se eliminan los movimientos registrados del diario. Una vez registrados, los movimientos se registran en cada una de las cuentas de regularización, de forma que sus saldos pasan a ser cero y el resultado del año se transfiere al balance.

## <a name="see-also"></a>Consulte también

[Cerrar periodos contables](year-close-account-periods.md)  
[Cierre de libros](year-close-books.md)  
[Asiento regularización](year-close-income-statement.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]