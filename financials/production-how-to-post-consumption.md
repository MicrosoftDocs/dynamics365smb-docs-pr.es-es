---
title: "Cómo registrar consumibles por lotes | Documentos de Microsoft"
description: "Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo."
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
ms.openlocfilehash: 67d80735f7ea217fa62317283246f098294323da
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-production-consumption"></a>Registrar consumibles de producción por lotes
Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.

También puede configurar el sistema para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción. Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Para registrar el consumo en una o varias líneas de la orden de producción  
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario de consumo** y elija el vínculo relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y del consumo. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Si el almacén donde se almacenan los componentes está configurado para utilizar ubicaciones, pero no requiere el proceso de picking, asigne un código de ubicación a la línea del diario para indicar de dónde se deben obtener los productos en el almacén. Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md).  
3. Para registrar el consumo, elija la acción **Registrar**. Se reducen los correspondientes movimientos de producto.

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

