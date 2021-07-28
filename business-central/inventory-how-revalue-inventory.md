---
title: Crear nuevos movimientos de valor para los productos del inventario | Documentos de Microsoft
description: Describe cómo apreciar o amortizar los movimientos de valor de uno o varios productos del inventario enviando el valor calculado actual.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 01710b23c56634b91b86f3f1c6e6c87415a787c6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435602"
---
# <a name="revalue-inventory"></a>Revaluar inventario
Si desea apreciar o depreciar un producto o el movimiento de un determinado producto, utilice el diario de revalorización.

## <a name="to-revalue-inventory"></a>Para revaluar el inventario
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de revaluación**, y luego elija el enlace relacionado.
2. Elija la acción **Calcular valor inventario**.
3. En la página **Calcular valor inventario**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.
5. En cada línea de la página **Diario de revalorización**, en el campo **Prec. coste (revaluado)**, especifique el nuevo coste unitario. También puede especificar el nuevo importe total en el campo **Valor inventario (revalorado)**.

    Los campos correspondientes se actualizan de forma automática. Observe que el campo **Importe** muestra el cambio real ocurrido en el valor de inventario del movimiento de producto seleccionado. Muestra la diferencia entre el valor del campo **Valor stock (calculado)** y el del campo **Valor inventario (revaluado)**.
6. Una vez completadas todas las líneas en el diario de revalorización, elija la acción **Registrar**.

Las nuevas entradas de valor ahora se crean de modo que reflejan las revalorizaciones que ha registrado. Puede ver los nuevos valores en las respectivas tarjetas de producto.

## <a name="see-also"></a>Consulte también
[Detalles de diseño: Revalorización](design-details-revaluation.md)  
[Inventario](inventory-manage-inventory.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]