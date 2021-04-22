---
title: Ubicar la salida de producción
description: La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2b04e07a6660ebeb32cc93594c77b8ff8e782766
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784222"
---
# <a name="put-away-production-or-assembly-output"></a>Ubicar la salida de producción o la salida de ensamblado

La forma de ubicar la salida de su producción depende de cómo esté configurado el almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

En las configuraciones básicas de almacén, donde el almacén requiere el proceso de ubicación, utilice el documento **Ubicación inventario** para la salida posproducción y registrar la ubicación de la salida.  

> [!NOTE]  
> La ubicación de inventario no es compatible con los procesos de ensamblaje. PublicRegistre un pedido de ensamblado para registrar la salida. Si usa ubicaciones, puede mover elementos entre ubicaciones más tarde. Para obtener más información, consulte [Mover productos ad hoc en las configuraciones avanzadas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

En las configuraciones avanzadas de almacén, donde el almacén no requiere los procesos de ubicación y recepción, cree un documento de ubicación interno o un documento de movimiento para ubicar la salida.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Para colocar la salida de producción con una colocación de inventario

El primer paso para crear la ubicación de salida es crear la solicitud de almacén de entrada. Esta solicitud informa al almacén de que la salida del pedido de producción o ensamblado está preparada para ubicación.

### <a name="to-create-the-inbound-warehouse-request"></a>Para crear la solicitud de entrada al almacén  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Orden de producción lanzada** y luego elija el enlace relacionado.  
2.  En la orden de producción que está preparada para ubicación, elija la acción **Crear petición entrada alm.**  

> [!NOTE]  
> También puede crear la solicitud de almacén de entrada eligiendo el campo **Crear solicitud de entrada** al actualizar la orden de producción. Para obtener más información, vea [Actualizar o replanificar o actualizar las órdenes de producción](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Para ubicar la salida con una ubicación de inventario  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ubicación existencias** y luego elija el enlace relacionado.  
2.  Cree una ubicación de inventario nueva. Para obtener más información, vea [Ubicar productos con ubicaciones de almacén](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Para tener acceso a la salida de la orden de producción, elija la acción **Traer doc. origen** y, a continuación, seleccione la orden de producción lanzada.  
4.  Rellene las líneas de ubicación como crea conveniente.
5.  Cuando las líneas estén preparadas para registrar, elija la acción **Registrar**. El registro creará los movimientos de almacén necesarios y registrará la salida de los productos.  

También puede crear **Ubicación existencias** directamente de la orden de producción lanzada. Para obtener más información, vea [Ubicar productos con ubicaciones de almacén](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Al ubicar y registrar el inventario, se asume que todas las operaciones se registran según la ruta estándar, es decir, la cantidad de salida se registra de acuerdo con la última operación. Puede usar el diario de salida para registrar las desviaciones de la cantidad de salida y los tiempos de preparación y ejecución. Si es necesario realizar un registro parcial después de crear la ubicación de inventario, puede hacerlo con los tiempos de preparación y las cantidades de todas las operaciones, excepto la última. En tal caso, la ubicación de inventario controla la última operación.  

Si solo necesita registrar el tiempo de preparación y ejecución de la última operación, defina la cantidad de salida de la última operación en 0. También puede decidir no registrar la última línea eliminándola.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Para colocar el ensamblado y la producción en configuraciones avanzadas de almacén
Al registrar la salida de la orden de producción o ensamblado en el almacén que está configurado para utilizar la ubicación y la recogida dirigidos, la salida se coloca en la ubicación definida en la orden de producción o ensamblado. 

La siguiente tabla describe diferentes formas de mover artículos dentro del almacén con configuraciones avanzadas donde todas las actividades del almacén deben realizarse en un flujo de trabajo dirigido. 

|**Para**|**Vea**|  
|------------|-------------|  
|Mover productos con la hoja de cálculo de movimientos de almacén.|[Mover productos en configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Crear una colocación interna para dejar los productos producidos o ensamblados en una configuración avanzada de inventario.|[Crear una colocación interna](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> En los documentos de almacén (documentos de ubicación interna, ubicación o movimiento) no puede introducir el número del documento de origen (número de orden de producción) de cada proceso.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
