---
title: Cómo registrar por lotes el resultado y tiempos de ejecución de producción | Documentos de Microsoft
description: La cantidad de salida representa el trabajo en curso en términos de cantidad terminada.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a0eeb0a944a0feaee27fcb6d5891f83151499940
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877791"
---
# <a name="batch-post-output-and-run-times"></a>Registrar por lotes el resultado y los tiempos de ejecución
La cantidad de salida representa el trabajo en curso en términos de cantidad terminada.  

> [!NOTE]
> Solo cuando registra la cantidad de salida en la última operación, las existencias se actualizan automáticamente.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Para registrar cantidades de salida en una o varias líneas de la orden de producción
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y los datos de salida. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Si la operación se ha completado, seleccione el campo **Terminado**.  

    Si el almacén donde se deben ubicar los componentes utiliza ubicaciones, pero no requiere el proceso de ubicación,  asigne un código de ubicación a la línea del diario para especificar dónde se deben colocar los productos en el almacén. Para obtener más información, consulte [Sacar producción o salida de ensamblado](warehouse-how-to-put-away-production-output.md).  

4. Para registrar las operaciones, elija la acción **Registrar**. Se registrará la cantidad de salida. El producto estará disponible para su envío.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Para registrar el tiempo de ejecución en una o varias líneas de la orden de producción
El tiempo de ejecución representa el trabajo en curso en términos de tiempo de trabajo necesario.    

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario salida** y luego elija el enlace relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y los datos de salida.  
3.  Si la operación se ha completado, seleccione el campo **Terminado**.  
4. Seleccione la acción **Registrar** para registrar el tiempo empleado por operación. Los movimientos de capacidad se actualizan en los centros utilizados de trabajo o de máquina.

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
