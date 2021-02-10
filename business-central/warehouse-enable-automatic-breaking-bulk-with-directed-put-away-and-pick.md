---
title: Interrupción automática masiva con picking y ubicaciones directas | Documentos de Microsoft
description: En almacenes que utilizan ubicación y picking directos, puede dividir una unidad de medida grande en otras unidades de medida más pequeñas, cuando crea instrucciones de almacén que cubren las necesidades de los documentos de origen, órdenes de producción o ubicaciones y picking internos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8d3ce697bb627bcc8acebc2392fe86b6af4b370b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759972"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Habilitar interrupción automática masiva con ubicaciones y picking directos
En almacenes que utilizan ubicación y picking directos, [!INCLUDE[prod_short](includes/prod_short.md)] puede dividir los bultos automáticamente, es decir, dividir una unidad de medida grande en otras unidades de medida más pequeñas, cuando crea instrucciones de almacén que cubren las necesidades de los documentos de origen, órdenes de producción o ubicaciones y picking internos. A veces, dividir bultos también significa reunir unidades de medida menores, si es necesario, para cumplir las solicitudes de salida dividiendo una unidad de medida grande del documento de origen u orden de producción en unidades de medida menores que están disponibles en el almacén.   

## <a name="breakbulking-in-picks"></a>Dividir bultos en picking  
Si desea almacenar productos en varias unidades de medida distintas y permitir que se combinen automáticamente según las necesidades en el proceso de picking, seleccione el campo **Permite división bulto** de la ficha de almacén.  

Para cubrir una tarea, la aplicación busca automáticamente un producto en la misma unidad de medida. Pero si no encuentra este formato de producto, y ha seleccionado el campo, la aplicación sugerirá que divida una unidad de medida grande en las unidades de medida necesarias.  

Si el sistema sólo encuentra unidades de medida pequeñas, sugerirá que reúna productos para hacer frente a la cantidad de la recepción o la orden de producción. De hecho, divide la unidad de medida grande del documento de origen en unidades menores para el picking.  

## <a name="breakbulking-in-put-aways"></a>Dividir bultos en ubicaciones  
En la ubicación de almacén, la aplicación sugiere automáticamente líneas de acción de apartado en la unidad de medida de ubicación, por ejemplo, piezas, aunque los productos hayan llegado en una unidad de medida diferente.  

## <a name="breakbulking-in-movements"></a>Dividir bultos en movimientos  
La aplicación también realiza la división de bultos automáticamente en los movimientos de reposición, si el campo **Permitir división bulto** está seleccionado en la ficha desplegable **Opción** de la página **Calcular reposición ubicación**.  

Puede ver el resultado del proceso de conversión de una unidad de medida a otra como líneas de división de bulto intermedias en las instrucciones de movimiento, picking o ubicación.  

> [!NOTE]  
>  Si selecciona el campo **Define filtro div. bulto** en la cabecera de instrucciones del almacén, la aplicación ocultará las líneas de división de bultos siempre que se utilice íntegramente la unidad de medida más grande. Por ejemplo, si un palé tiene 12 unidades y va a utilizar esas 12 unidades, el picking indicará que utilice 1 palé y que coloque 12 unidades. No obstante, si sólo tiene que hacer picking de 9 unidades, no se ocultarán las líneas de división de bultos, aunque haya seleccionado el campo **Filtro división de bultos**, porque ha colocado las tres unidades restantes en alguna parte del almacén.  

> [!NOTE]  
>  Si desea que sus unidades de medida se distribuyan de una forma óptima en el almacén, junto con la funcionalidad de división de bultos, debería intentar:  
>   
> - Configurar la unidad de medida base de un producto según la unidad de medida más pequeña que espera manipular en los procesos de almacén.  
> - Configurar unidades de medida alternativas del producto como múltiplos de la unidad de medida base.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
