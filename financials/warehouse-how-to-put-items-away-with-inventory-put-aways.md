---
title: "Ubicación de productos con ubicación de inventario | Documentos de Microsoft"
description: "Cuando el almacén está configurado para requerir el proceso de ubicación, pero no el proceso de recepción, utilice el documento **Ubicac. inventario** para registrar la información de ubicación y recepción de sus documentos de origen. El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de salida o una orden de producción cuya salida está preparados para ubicarse."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92eae2f24daf8181e39b3d22ea23c31a9ee85347
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="put-items-away-with-inventory-put-aways"></a>Ubicar productos con ubicación de inventario
Cuando el almacén está configurado para requerir el proceso de ubicación, pero no el proceso de recepción, utilice el documento **Ubicac. inventario** para registrar la información de ubicación y recepción de sus documentos de origen. El documento de origen de entrada puede ser un pedido de compra, una devolución de ventas, un pedido de transferencia de salida o una orden de producción o ensamblado cuya salida está preparados para ubicarse.  

Puede crear una ubicación de inventario de tres formas:  

- Cree la ubicación en dos pasos; para ello cree primero una solicitud de almacén desde el documento de origen, que actúa como una señal para el almacén de que el documento de origen está preparado para la ubicación. A continuación, se puede crear la ubicación de inventario en la ventana **Ubicac. inventario** según el documento de origen.  
- Cree la ubicación de inventario directamente desde el propio documento de origen.  
- Cree las ubicaciones de inventario para varios documentos de origen mediante un proceso.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Para solicitar una ubicación de inventario lanzando el documento de origen
En el caso de pedidos de compra, pedidos de devolución de venta, pedidos de transferencia de entrada y pedidos de ensamblado, para crear la solicitud de almacén, lance el pedido. A continuación se describe cómo hacerlo des de un pedido de compra.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el pedido de compra que desea lanzar, y después seleccione **Lanzar**.  

    En el caso de los pedidos de producción, se crea la solicitud de almacén creando una solicitud de entrada a partir del pedido de producción lanzado.  
3.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Órdenes producción lanzadas** y, a continuación, seleccione el vínculo relacionado.  
4. Seleccione la acción **Crear solicitud entrada almacén**.  

> [!NOTE]  
>  También puede crear la solicitud de almacén de entrada seleccionando la casilla de verificación **Crear solicitud de entrada** cuando actualice la orden de producción. Para obtener más información, vea [Actualizar o replanificar o actualizar las órdenes de producción](production-how-to-replan-refresh-production-orders.md).  

Cuando se crea la solicitud de almacén, un empleado de almacén asignado para realizar las ubicaciones de productos puede ver que el documento de origen está preparado y puede crear un documento de ubicación de inventario.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Para crear una ubicación de inventario según el documento de origen
Ahora que se ha creado la solicitud, el empleado del almacén puede crear un nueva ubicación de inventario basado en el documento de origen lanzado.   
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ubicac. inventario** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Documento origen**, seleccione el tipo de documento de origen que está ubicando.  
4. En el campo **Cód. procedencia mov.**, seleccione el documento de origen.  
5. También, elija la acción **Traer documento origen** para seleccionar un documento de una lista de documentos de origen de entrada que están preparados para la ubicación en el almacén.  
6. Elija el botón **Aceptar** para rellenar las líneas de ubicación según el documento de origen seleccionado.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Para crear una ubicación de inventario desde el documento de origen  
1.  En el documento de origen, que puede ser un pedido de compras, una devolución de ventas, un pedido de transferencia de entrada o un pedido de producción, elija la acción **Crear ubicac. invent./picking**.  
2. Active la casilla **Crear ubicación exist**.
3. Elija el botón **Aceptar**. Se crea una ubicación de inventario nueva.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Para crear varias Ubicaciones de existencias con un proceso  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Crear ubicac./pick. exist.** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Solicitud almacén** de la ventana respectiva, utilice los campos **Documento origen** y **Cód. procedencia mov.** para filtrar determinados tipos de documentos o intervalos de números de documento.  
3.  En la ficha desplegable **Opciones**, seleccione la casilla **Crear ubicación exist.**
4.  Elija el botón **Aceptar**. Se crean las ubicaciones de inventario especificadas.

## <a name="to-record-the-inventory-put-away"></a>Para registrar las ubicaciones de inventario  
1. Abra un documento de ubicación creado previamente seleccionando uno de la ventana **Ubicac. existencias**.  
2. En las líneas de ubicación del campo **Cód. ubicación**, la ubicación en la cual se debe realizar la ubicación se sugiere como la ubicación predeterminada del artículo. Si es necesario puede cambiar la ubicación en esta ventana.  
3. Realice la ubicación e introduzca la información de la cantidad de ubicación real en la ventana **Cdad. a manipular**.

    Si es necesario colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la función **Dividir línea** en la ficha desplegable **Líneas**. Para obtener más información acerca de cómo dividir líneas, consulte[Dividir las líneas de actividad de almacén](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Cuando haya realizado la ubicación, elija la acción **Registrar**.  

El proceso de registro contabilizará la recepción, o para las órdenes de producción, la salida, de las líneas del documento de origen que se han ubicado y, si la ubicación utiliza ubicaciones, el registro también creará movimientos de almacén para registrar los cambios de cantidad en la ubicación.

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

