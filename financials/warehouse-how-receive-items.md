---
title: "Cómo recibir productos | Documentos de Microsoft"
description: "Cuando los productos llegan al almacén, se recuperan las líneas del documento de origen que ha activado su recepción. "
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
ms.openlocfilehash: 3e6ab403945df0f3c98ab1d47eefa0633f0172e3
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="receive-items"></a>Recibir productos
Cuando los artículos llegan a un almacén que no está configurado para el procesamiento de recibo de almacén, simplemente registre el recibo en el documento comercial relacionado, como una orden de compra, una orden de devolución de ventas o una orden de transferencia de entrada.

Cuando los productos llegan al almacén, se recuperan las líneas del documento de origen que ha activado su recepción. Si tiene ubicaciones, puede aceptar que se rellene la ubicación genérica o, si el producto no se ha utiliza nunca antes en el almacén, rellenar la ubicación donde debe ubicarse el producto.  A continuación, debe rellenar las cantidades de los productos que ha recibido y registrar la recepción.  

## <a name="to-receive-items-with-a-purchase-order"></a>Para recibir productos con un pedido de compra
A continuación se describe cómo recibir productos con un pedido de compra. Los pasos son iguales para las órdenes de devolución de venta y las órdenes de transferencia.  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.
2. Abra un pedido de compra existente o cree uno nuevo. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
3. Escriba la cantidad recibida en el campo **Cantidad a recibir**.

    El valor del campo **Cdad. recibida** se actualiza según corresponde. Si se trata de un recibo parcial, el valor es menor que el valor del campo **Cantidad**.
4. Seleccione la acción **Registrar**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Para recibir productos con recibo de almacén
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recepciones almacén** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  

    Rellene los campos en la ficha desplegable **General**. Al recuperar las líneas del documento de origen, se copia parte de la información en cada línea.  

    Para la configuración de almacén con ubicación y picking directos, si el almacén tiene una zona y ubicación genéricas para los recibos, se rellenarán automáticamente los campos **Cód. zona** y **Cód. ubicación**, pero puede cambiarlos como considere.  

    > [!NOTE]  
    >  Si desea recibir productos con códigos de clase de almacén de la ubicación en el campo **Cód. ubicación** de la cabecera de documento, debe eliminar el contenido del campo **Cód. ubicación** en la cabecera antes de recuperar líneas del documento de origen para los productos.  
3.  Seleccione la acción **Traer doc. origen**. Se abre la ventana **Documentos origen**.

    Desde una recepción o un recibo de almacén nuevos o abiertos, puede utilizar la ventana de **Filtros para traer docs. orig.** para recuperar las líneas del documento de origen lanzado que definen la artículos para recibir o enviar.

    1. Elija la acción **Utiliz. filt. para traer docs.**.  
    2. Para configurar un nuevo filtro introduzca un código descriptivo en el campo **Código** y, a continuación, elija la acción **Modificar**.  
    3. Defina el tipo de líneas del documento de origen que desea que recupere el sistema rellenando los campos de filtro correspondientes.  
    4. Seleccione la acción **Ejecutar**.  

    Todas las líneas del documento de origen lanzado que cumplan los criterios del filtro se insertarán en la ventana **Recibo almacén** desde las que se activó la función del filtro.  

    Las combinaciones de filtros que defina se guardan en la ventana de **Filtros para traer docs. orig.** hasta que la próxima vez que las necesite. Puede crear un número ilimitado de combinaciones de filtros. Puede modificar los criterios en cualquier momento eligiendo la acción **Modificar**.

4.  Seleccione los documentos de origen de los que desea recibir productos y, a continuación, haga clic en **Aceptar**.  

    Las líneas de los documentos de origen aparecerán en la ventana **Recep. almacén**. El campo **Cantidad a recibir** se rellena con la cantidad pendiente de cada línea, pero puede cambiarla según necesite. Si ha eliminado el contenido del campo **Cód. ubicación** de la ficha desplegable **General** antes de traer las líneas, debe rellenar un código de ubicación apropiado en cada línea de recepción.  

    > [!NOTE]  
    >  Para rellenar el campo de **Cdad. para recibir** en todas las líneas con cero, elija la acción **Eliminar cdad. a recibir**. Para rellenarlo de nuevo con la cantidad pendiente, elija la acción **Rellenar cdad. a recibir aut.**  

    > [!NOTE]  
    >  No puede recibir más productos que el número que se muestra en el campo **Cdad. pendiente** de la línea del documento de origen. Para recibir más productos, recupere otro documento de origen que contenga una línea para el producto mediante la función de filtro para traer documentos de origen con el producto.  

5.  Registre la recepción de almacén. Los campos de cantidad se actualizan en el documento de origen y se registran los productos como parte de las existencias de la empresa.  

Si utiliza ubicación y picking directos, las líneas de recepción se envían a la función de ubicación de almacén. No es posible hacer picking de los productos, aunque se hayan recibido, hasta que se ubiquen. Los productos recibidos se identifican como existencias disponibles sólo cuando se haya registrado la ubicación.  

Si no utiliza ubicación de almacén, pero sí utiliza ubicaciones, se registra la ubicación de los productos en la ubicación especificada en la línea del documento de origen.  

> [!NOTE]  
>  Si utiliza la función **Registrar e imprimir**, se registra la recepción y se imprime la instrucción de ubicación que muestra dónde se colocan los productos en el almacén.  
>   
>  Si su almacén utiliza ubicación y picking directos, las plantillas de ubicación se usarán para calcular el mejor lugar donde ubicar los productos. A continuación, esto se imprime en la instrucción de ubicación.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

