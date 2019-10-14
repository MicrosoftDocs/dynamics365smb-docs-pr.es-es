---
title: 'Procedimiento: realice un picking de los artículos para el envío de almacén | Documentos de Microsoft'
description: Cuando el almacén está configurado para requerir los procesos de picking y envío, utilice documentos de picking de almacén para crear y procesar la información de picking anterior al registro del envío de almacén.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b136b5a1c06ee61313596f7613cb99fb4bf11e86
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313981"
---
# <a name="pick-items-for-warehouse-shipment"></a>Realizar un picking de los artículos para el envío de almacén
Cuando el almacén está configurado para requerir los procesos de picking y envío, utilice documentos de picking de almacén para crear y procesar la información de picking anterior al registro del envío de almacén.  

No se puede crear un documento de picking de almacén desde cero porque una actividad de picking siempre forma parte de un flujo de trabajo, tanto en un escenario de extracción como de inserción.  

Puede crear los documentos de picking de almacén en forma de extracción abriendo un documento de envío vacío de almacén, detectando los documentos de origen para lanzar el envío y creando las líneas de picking de almacén para esos envíos. Puede utilizar las funciones **Traer doc. origen** o **Utilizar filtro para obtener documentos origen** para detectar los documentos de origen que están preparados para el envío.

Como alternativa, puede utilizar la página **Preparar hoj. trab. pedido** para obtener y crear líneas de picking en lote. Para obtener más información, consulte [Planifique pickings en hojas de trabajo](warehouse-how-to-plan-picks-in-worksheets.md).  

También puede crear los documentos de picking de almacén en forma de empuje de la página **Envío almacén** seleccionando **Crear picking**.  

> [!NOTE]  
>  Picking en el envío de almacén de los productos que se ensamblan al pedido de venta que se envía sigue los mismos pasos que para picking de almacén normales para envío, tal como se describe en este tema. Sin embargo, el número de líneas de picking por la cantidad a enviar puede ser de "muchas a una" porque realiza el picking de los componentes, no el producto del ensamblado.  
>   
>  Las líneas de picking de almacén se crean para el valor del campo **Cantidad pendiente** en las líneas de pedido de ensamblado vinculado a la línea de pedido de venta que se envía. Esto garantiza que se realice el picking de todos los componentes en una acción.  
>   
>  Para obtener más información, vea la sección “Tratamiento de productos ensamblar para pedido en los envíos de almacén”.  
>   
>  Para obtener información acerca de la realización de picking de componentes para pedidos de ensamblado en general, incluidas las situaciones en las que no caduca el producto de ensamblado en un envío de ventas, consulte [Selección de producción o la Lista montaje](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Para realizar un picking de los artículos para el envío de almacén  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Picking** y luego elija el enlace relacionado.  

    Si tiene que trabajar con un picking determinado, seleccione el picking de la lista o filtre la lista para encontrar los pickings que se le han asignado específicamente. Abra la ficha de la tarjeta.  
2.  Si el campo **Id. usuario asignado** está vacío, escriba el id. para identificarse si es necesario.  
3.  Realice el picking real de los artículos.  

    Si el almacén está configurado para utilizar ubicaciones, las ubicaciones genéricas de los artículos se utilizan para sugerir de dónde tomar los artículos. Las instrucciones aparecen en dos líneas independientes, al menos una para cada tipo de acción, Traer y Colocar.  

    Si el almacén está configurado para utilizar ubicación y picking directos, el ranking de ubicación se utiliza para calcular las mejores ubicaciones de las que hacer picking y, a continuación, se sugieren en las líneas de picking. Las instrucciones aparecen en dos líneas independientes, al menos una para cada tipo de acción, Traer y Colocar.  

4.  Cuando haya hecho el picking y colocado los productos en el área de o ubicación de envío, elija la acción **Registrar picking**.  

La persona responsable de envío ahora puede llevar los artículos al muelle de envío y registrar el envío, incluido el documento de origen relacionado, en la página **Envío de almacén**. Para obtener más información, consulte [Enviar productos](warehouse-how-ship-items.md).   

Además del picking para los documentos de origen, tal como se describe en este tema, puede traer y situar los artículos entre las ubicaciones sin hacer referencia a los documentos de origen. Para obtener más información, vea [Realizar el picking y la ubicación sin un documento de origen](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Tratamiento de productos ensamblar para pedido en los envíos de almacén
En escenarios de ensamblar para pedido, el campo **Cdad. a enviar** de las líneas de envío de almacén se utiliza para registrar cuántas unidades se ensamblan. La cantidad especificada se registra como salida de ensamblado cuando se registra el envío de almacén.

Para las demás líneas de envío de almacén, el valor del campo **Cdad. a enviar** es cero desde el principio.

Cuando los trabajadores responsables del ensamblado terminan de montar componentes o toda la cantidad de ensamblar para pedido, la registran en el campo **Cdad. a enviar** de la línea de envío de almacén y eligen la acción **Registrar envío**. El resultado es que se registra la salida de ensamblado correspondiente, incluido el consumo de componentes. Un envío de venta para la cantidad se registra para el pedido de venta.

Desde el pedido de ensamblado, puede elegir **Lín. envío almacén ensamblar para pedido** para acceder a la línea de envío de almacén. Esto resulta adecuado para los trabajadores que no utilizan normalmente la página **Envío de almacén**.

Una vez registrado el envío de almacén, los distintos campos de la línea de pedido de venta se actualizan para mostrar el progreso en el almacén. Los siguientes campos también se actualizan para mostrar cuántas cantidades de ensamblar para pedido faltan ensamblar y enviar:

- **Cdad. pdte. almacén de ATO**
- **Cdad. pdte. salida alm. de ATO**

> [!NOTE]
> En escenarios de combinación, en los que una parte de la cantidad debe ensamblarse primero y la otra se debe enviar desde el inventario, se crean dos líneas de envío de almacén. Uno es para la cantidad de ensamblar para pedido y otro es para la cantidad de existencias.

> En ese caso, la cantidad de ensamblar para pedido se controla tal como se describe en este tema, y la cantidad de existencias se controla como cualquier otra línea de envío normal de almacén. Para obtener más información sobre los escenarios de combinación, consulte [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
