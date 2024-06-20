---
title: Desplazar productos
description: Obtenga más información sobre cómo mover productos entre contenedores en el almacén.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345'
---
# <a name="moving-items"></a>Mover artículos

Puede mover productos en e almacén de diferentes maneras, dependiendo de cómo haya configurado su almacén. La complejidad puede variar:

* Los almacenes pequeños pueden usar configuraciones básicas de almacén para manejar pedidos individualmente, en uno o varios pasos.
* Los almacenes grandes pueden usar configuraciones avanzadas en las que todas las actividades del almacén se coordinan mediante un flujo de trabajo dirigido. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

Es posible que sea necesario mover artículos entre ubicaciones, por ejemplo, debido a operaciones internas:

* Una orden de producción necesita que se entreguen los componentes o que se almacenen los productos terminados.
* Un responsable de almacén quiere optimizar el espacio.
* Movimientos no planificados hacia y desde las operaciones.
* Restablecer las ubicaciones de picking o las ubicaciones de planta.
* Actualizar los contenidos de la ubicación.

Las actividades de recuento, ajuste y reclasificación de productos pueden incluir tareas de almacén que deben realizarse en los movimientos del almacén antes de que puedan sincronizarse con los movimientos del producto. Obtenga más información en [Recuento, ajuste y reclasificación de inventario](inventory-how-count-adjust-reclassify.md).  

 En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Mover productos entre almacenes|[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)|
|Mueva los artículos entre las ubicaciones en configuraciones de almacén básico en cualquier momento o sin los documentos de origen.|[Mover productos en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Utilice la hoja de trabajo del movimiento de almacén, el picking y el almacenamiento internos para mover los productos en configuraciones avanzadas de almacén con el picking y el almacenamiento dirigidos.|[Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Vuelva a estructurar el almacén con nuevos códigos y características de ubicación y muévalos.|[Reestructurar almacenes](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Consulte también .

[Información general de la administración de almacenes](design-details-warehouse-management.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
