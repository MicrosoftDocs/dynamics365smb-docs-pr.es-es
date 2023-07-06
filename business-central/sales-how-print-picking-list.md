---
title: Imprimir lista de picking almacén a partir de un pedido de venta
description: 'Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, ventas, factura y otros documentos de venta de salida.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="print-the-picking-list"></a><a name="print-the-picking-list"></a><a name="print-the-picking-list"></a><a name="print-the-picking-list"></a>Imprimir la lista de picking

Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas y otros documentos que inicien el envío de los productos.

Este informe se utiliza normalmente en empresas sin funcionalidad dedicada a la gestión de almacenes, de modo que un trabajador de inventario pueda ver o imprimir la lista de picking del documento de ventas relacionado. En empresas con un volumen más alto o procesos más complejos, el envío y el picking se planifican y se realizan en documentos de almacén dedicados. Obtenga más información en [Flujo de salida del almacén](design-details-outbound-warehouse-flow.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a><a name="to-print-a-picking-list-from-a-sales-order"></a><a name="to-print-a-picking-list-from-a-sales-order"></a><a name="to-print-a-picking-list-from-a-sales-order"></a>Para imprimir una lista de picking a partir de un pedido de venta

El procedimiento siguiente se basa en un pedido de venta. Los pasos son similares para otros documentos de ventas que se pueden usar para iniciar el envío de productos, como pedidos de transferencia.

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta para el que desea elegir productos.  
3. Elija la acción **Informe** y luego elija la acción **Lista de selección por orden**.  
4. Seleccione el botón de **Imprimir** para imprimir la lista de picking o elija el botón de **Vista previa** para verlo en la pantalla.

También puede guardar la lista de picking como un documento, por ejemplo, para enviarla a alguien o para agregarla como un archivo adjunto al pedido de ventas. Obtenga más información en [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

> [!NOTE]
> Si ha usado la función **Desplegar L.M.** en el pedido de venta, solo se muestran en el informe los componentes del elemento del ensamblado relacionado. Obtenga más información en [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Inventario](inventory-manage-inventory.md)  
[Flujo de salida del almacén](design-details-outbound-warehouse-flow.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
