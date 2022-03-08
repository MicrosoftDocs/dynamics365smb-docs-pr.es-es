---
title: Cómo registrar consumibles por lotes | Documentos de Microsoft
description: Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bf0a92d05b6c9ecb3d5a5ba054b4675680ad43c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391804"
---
# <a name="batch-post-production-consumption"></a>Registrar consumibles de producción por lotes
Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.

También puede configurar el sistema para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción. Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Para registrar el consumo en una o varias líneas de la orden de producción  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario de consumo** y luego elija el enlace relacionado.  
2.  Rellene los campos con los datos de las órdenes de producción y del consumo. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Si el almacén donde se almacenan los componentes está configurado para utilizar ubicaciones, pero no requiere el proceso de picking, asigne un código de ubicación a la línea del diario para indicar de dónde se deben obtener los productos en el almacén. Para obtener más información, consulte [Picking para producción o ensamblado](warehouse-how-to-pick-for-production.md).  
3.  Para registrar el consumo, elija la acción **Registrar**. Se reducen los correspondientes movimientos de producto.

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]