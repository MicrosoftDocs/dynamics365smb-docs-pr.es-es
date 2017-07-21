---
title: Crear nuevos movimientos de valor para los productos del inventario | Documentos de Microsoft
description: "Describe cómo apreciar o amortizar los movimientos de valor de uno o varios productos del inventario enviando el valor calculado actual."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1935f53db068047921e44109cd4b23bbb51f0890
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-revalue-inventory"></a>Revaluación de inventario
Si desea apreciar o depreciar un producto o el movimiento de un determinado producto, utilice el diario de revalorización.

## <a name="to-revalue-inventory"></a>Para revaluar el inventario
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario revalorizac.** y elija el vínculo relacionado.
2. Elija la acción **Calcular valor inventario**.
3. En la ventana **Calcular valor inventario**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija el botón **Aceptar**.
5. En cada línea de la ventana **Diario de revalorización**, en el campo **Prec. coste (revaluado)**, especifique el nuevo coste unitario. También puede especificar el nuevo importe total en el campo **Valor inventario (revalorado)**.

    Los campos correspondientes se actualizan de forma automática. Observe que el campo **Importe** muestra el cambio real ocurrido en el valor de inventario del movimiento de producto seleccionado. Muestra la diferencia entre el valor del campo **Valor stock (calculado)** y el del campo **Valor inventario (revaluado)**.
6. Una vez completadas todas las líneas en el diario de revalorización, elija la acción **Registrar**.

Las nuevas entradas de valor ahora se crean de modo que reflejan las revalorizaciones que ha registrado. Puede ver los nuevos valores en las respectivas tarjetas de producto.

## <a name="see-also"></a>Consulte también
[Inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

