---
title: Actividades de almacén | de Microsoft
description: Una vez recibidos los bienes, antes de que se envíen, se llevan a cabo una serie de actividades internas de almacén para garantizar un flujo eficaz por todo el almacén y para organizar y mantener las existencias de la empresa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: abeae11d09e4a07884969985667b8b6d480d2b09
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382309"
---
# <a name="warehouse-management"></a>Gestión almacén
Una vez recibidos los bienes, antes de que se envíen, se llevan a cabo una serie de actividades internas de almacén para garantizar un flujo eficaz por todo el almacén y para organizar y mantener las existencias de la empresa.

Entre las actividades de almacén habituales se encuentran la ubicación de productos, los movimientos de productos dentro de un mismo almacén o entre distintos almacenes y el picking de productos para las fases de ensamblado, producción o envío. Los productos de ensamblaje para la venta o el inventario también se pueden considerar actividades del almacén, pero éstos se cubren en otra parte. Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).  

En almacenes de grandes dimensiones, las distintas tareas de manipulación pueden distribuirse entre distintos departamentos y la integración puede gestionarse mediante un flujo de trabajo dirigido. En instalaciones más sencillas, el flujo no está tan formalizado y las actividades de almacén se llevan a cabo con las llamadas ubicaciones y picking de inventario. Para obtener más información sobre configuraciones de almacén básicas y avanzadas, consulte [Detalles de diseño: Vista general de almacén](design-details-warehouse-overview.md).

Antes de poder realizar actividades de almacén, debe configurar el sistema para la complejidad relevante del procesamiento del almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

Las tareas relacionadas con el inventario de recuento, ajuste y reclasificación de artículos pueden incluir tareas de almacén que deben realizarse en los movimientos del almacén antes de que puedan sincronizarse con los movimientos del producto relacionado. Para obtener más información, consulte [Recuento, ajuste, y reclasificación de inventario](inventory-how-count-adjust-reclassify.md).

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Registre la recepción (incluida la recepción en exceso) de productos en las ubicaciones del almacén, ya sea solo con una orden de compra, en configuraciones de ubicación sencillas o con un recibo de almacén, en caso de procesamiento semi o totalmente automatizado del almacén en la ubicación.|[Recibir productos](warehouse-how-receive-items.md)|
|Evite los procesos de ubicación y picking para acelerar un elemento directamente desde la recepción o producción hasta el envío.|[Productos de tránsito directo](warehouse-how-to-cross-dock-items.md)|    
|Ubicar los productos recibidos de compras, devoluciones de ventas, transferencias o salidas de producción de acuerdo con lo configurado en el proceso del almacén.|[Configurando los artículos componentes](warehouse-put-away-items.md)|
|Mover productos de una ubicación a otra en el almacén.|[Mover artículos](warehouse-move-items.md)|
|Realizar el picking de los productos para su envío, transferencia o consumo en producción o ensamblado, de acuerdo con lo configurado en el proceso del almacén.|[Realización de picking de artículos](warehouse-pick-items.md)|
|Registre la envío de productos desde las ubicaciones del almacén, ya sea solo con una orden de ventas, en configuraciones de ubicación sencillas o con un envío de almacén, en caso de proceso semi o totalmente automatizado del almacén en la ubicación.|[Enviar productos](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Consulte también  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]