---
title: Elegir productos | Documentos de Microsoft
description: "La actividad de almacén consistente en realizar el picking de los productos antes de enviarlos o consumirlos se realiza de modo distinto según estén configuradas las funciones de gestión del almacén. La complejidad de la [configuración](../configure-warehouse-processes.md) puede oscilar desde la ausencia total de funciones de almacén, pasando por configuraciones de almacén básicas para la gestión pedido-por-pedido en sólo una o más actividades, hasta configuraciones más avanzadas en las que todas las actividades del almacén se llevan a cabo como parte de un flujo de trabajo dirigido."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 132408d095edbfa1a60577cdd19022920088670b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="pick-items"></a>Elegir productos
La actividad de almacén consistente en realizar el picking de los productos antes de enviarlos o consumirlos se realiza de modo distinto según estén configuradas las funciones de gestión del almacén. La complejidad puede oscilar desde la ausencia total de funciones de almacén, pasando por configuraciones básicas de almacén para la gestión pedido-por-pedido en sólo una o más actividades, hasta configuraciones más avanzadas en las que todas las actividades del almacén se llevan a cabo como parte de un flujo de trabajo dirigido. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

Si decide organizar y registrar su actividad de picking con documentos de almacén, active el campo **Picking requerido** en la ficha de almacén. Esto indica que, cuando tenga que realizar el picking de productos para un documento de origen de salida, desea que el picking de estos productos se controle por el sistema. El documento de origen de salida puede ser un pedido de venta, una devolución de compras, un pedido de transferencia de salida, un pedido de servicio o una orden de producción de cuyos componentes debe realizarse el picking.

> [!NOTE]
> A pesar de que la configuración se denomina **Picking requerido**, todavía puede registrar envíos directamente desde el documento empresarial de origen en la ubicación donde se selecciona esta casilla de verificación.

Si el almacén está configurado para requerir el proceso de picking, pero no el proceso de envío, utilice la ventana **Picking inventario** para organizar la información de picking, imprimirla, especificar el resultado del picking real y registrar la información de picking, que, a su vez, registra el envío de los productos. En caso de realizar el picking de componentes para una orden de producción, el registro del picking también registra el consumo.

Si su ubicación se ha configurado para requerir picking y procesamiento de envío, con lo que ha activado las marcas de verificación de los campos de **Picking requerido** y **Envío requerido** en la ficha de almacén, utilice la ventana **Picking de almacén** para gestionar el picking. El picking de almacén funciona de forma similar al picking de inventario, excepto que en vez de registrar información de picking, se registra el picking. Este proceso de registro no registra el envío, sino simplemente hacer que los artículos estén disponibles para el envío. Como administrador del almacén, puede utilizar las hojas de trabajo de un picking para organizar la información antes de crear las instrucciones individuales de picking de almacén.

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|
|------------|-------------|  
|Registrar el envío de los productos directamente en el documento de pedido de salida puesto que no existen funciones de almacén. (Funciona igual para los pedidos de venta, pedidos de transferencia de salida y envíos de devoluciones.)|[Enviar productos](warehouse-how-ship-items.md)|  
|Realizar el picking de los productos pedido a pedido y registrar el envío como parte de la misma actividad, en una configuración básica de almacén.|[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Realizar el picking de productos de distintos pedidos en una configuración avanzada de almacén.|[Realizar picking de productos con picking almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Realizar picking de componentes para la producción o ensamblado en una configuración avanzada o básica de almacén.|[Selección de producción o la Lista montaje](warehouse-how-to-pick-for-production.md)|  
|Planificar instrucciones optimizadas de picking para un número de envíos en lugar de que los empleados del almacén actúen directamente en los envíos registrados.|[Planificar los picking en la hoja de trabajo](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Realizar el picking de productos técnicamente con un propósito determinado, como puede ser una unidad de producción que solicita componentes adicionales, de forma que los productos no abandonen técnicamente el almacén.|[Realizar el picking y la ubicación sin un documento de origen](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Comprender cómo realizar automáticamente el picking de los productos de acuerdo con su fecha de caducidad, por ejemplo productos perecederos.|[Realización de picking por el FEFO](warehouse-picking-by-fefo.md)|
|Dividir una línea de picking en varias líneas, por ejemplo, porque no hay suficientes elementos relacionados en la ubicación designada.|[Dividir líneas de actividad de almacén](warehouse-how-to-split-warehouse-activity-lines.md)|
|Obtener acceso inmediato al picking que está asignado al usuario en calidad de empleado del almacén.|[Buscar las asignaciones de almacén](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

