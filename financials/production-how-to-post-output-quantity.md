---
title: "Cómo registrar por lotes el resultado y tiempos de ejecución de producción | Documentos de Microsoft"
description: "La cantidad de salida representa el trabajo en curso en términos de cantidad terminada."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a>Registrar por lotes el resultado y los tiempos de ejecución
La cantidad de salida representa el trabajo en curso en términos de cantidad terminada.  

> [!NOTE]
> Solo cuando registra la cantidad de salida en la última operación, las existencias se actualizan automáticamente.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Para registrar cantidades de salida en una o varias líneas de la orden de producción
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de salida** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y los datos de salida. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Si la operación se ha completado, seleccione el campo **Terminado**.  

    Si el almacén donde se deben ubicar los componentes utiliza ubicaciones, pero no requiere el proceso de ubicación,  asigne un código de ubicación a la línea del diario para especificar dónde se deben colocar los productos en el almacén. Para obtener más información, consulte [Sacar producción o salida de ensamblado](warehouse-how-to-put-away-production-output.md).  

4. Para registrar las operaciones, elija la acción **Registrar**. Se registrará la cantidad de salida. El producto estará disponible para su envío.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Para registrar el tiempo de ejecución en una o varias líneas de la orden de producción
El tiempo de ejecución representa el trabajo en curso en términos de tiempo de trabajo necesario.    

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de salida** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y los datos de salida.  
3.  Si la operación se ha completado, seleccione el campo **Terminado**.  
4. Seleccione la acción **Registrar** para registrar el tiempo empleado por operación. Los movimientos de capacidad se actualizan en los centros utilizados de trabajo o de máquina.

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

