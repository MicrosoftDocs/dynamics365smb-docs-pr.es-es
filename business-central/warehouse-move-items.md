---
title: Mover productos | Documentos de Microsoft
description: "En el inventario, los productos deben moverse de una ubicación a la otra para posibilitar las actividades diarias del almacén relacionadas con el mantenimiento de productos general. Algunos movimientos suceden en relación directa a las operaciones internas, como un orden de producción que necesite ubicar los componentes entregados o los productos finales. Otros movimientos suceden como sencilla optimización de los de almacén o como movimientos ad hoc o desde las operaciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6efb709151ea98b5c8d89d67138b52bac5751c56
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="moving-items"></a>Mover artículos
La actividad de almacén consistente en mover productos entre los almacenes se realiza de modo distinto según estén configuradas las funciones de gestión del almacén. La complejidad puede oscilar desde la ausencia total de funciones de almacén, pasando por configuraciones básicas de almacén para la gestión pedido por pedido en sólo una o más actividades, hasta configuraciones más avanzadas en las que todas las actividades del almacén se llevan a cabo como parte de un flujo de trabajo dirigido. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

En una ubicación de almacén, los productos deben moverse de una ubicación a la otra para posibilitar las actividades diarias del almacén relacionadas con el mantenimiento de productos general. Algunos movimientos suceden en relación directa a las operaciones internas, como un orden de producción que necesite ubicar los componentes entregados o los productos finales. Otros movimientos suceden como sencilla optimización de los de almacén o como movimientos ad hoc o desde las operaciones.

El movimiento de productos a otras ubicaciones afecta los movimientos de productos y, en consecuencia, debe realizarse por medio de una orden de transferencia. Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).  

Se llevan a cabo tareas adicionales de movimiento para reponer periódicamente las ubicaciones de picking o las ubicaciones de control de planta y modificar la información del contenido de la ubicación.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Mueva los artículos entre las ubicaciones en configuraciones de almacén básico en cualquier momento o sin los documentos de origen.|[Mover productos en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utilice la hoja de cálculo del movimiento de almacén para desplazar los artículos en configuraciones avanzadas de almacén, tanto para los documentos de origen y como los ad hoc.|[Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Traiga los artículos componentes a las operaciones internas en configuraciones de almacén básico que solicita los documentos de origen para aquellos operaciones.|[Mover componentes a un área de operaciones en configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Planificar qué ubicaciones deben llenarse o vaciarse para mantener establecer un flujo eficiente, como por ejemplo vaciar un área de almacenaje de bultos antes de recibir un gran volumen.|[Planificar movimientos de almacén en hojas de trabajo](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Actualizar la frecuencia con la que las ubicaciones, por ejemplo las ubicaciones de picking, deben reponerse como resultado de las fluctuaciones en la demanda.|[Calcular reposición ubicación](warehouse-how-to-calculate-bin-replenishment.md)|
|Vuelva a estructurar el almacén con nuevos códigos y características de ubicación y muévalos.|[Reestructurar almacenes](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

