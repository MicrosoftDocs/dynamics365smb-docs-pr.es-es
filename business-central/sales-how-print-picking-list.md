---
title: Cómo imprimir una lista de picking de inventario a partir de un pedido de venta
description: Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, ventas, factura y otros documentos de venta de salida.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: d5eaad5279445375ec00fdf42dd48bffa5d03645
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324477"
---
# <a name="print-the-picking-list"></a>Imprimir la lista de picking
Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, una factura de venta y otros documentos que inicien el envío de los productos.

Este informe se utiliza normalmente en empresas sin funcionalidad dedicada para la gestión de almacenes, de modo que un trabajador de inventario pueda ver o imprimir simplemente la lista de picking del documento de ventas relacionado. En empresas con un volumen más alto o procesos más complejos, el picking se planifica y se realiza en documentos de almacén dedicados. Para obtener más información, consulte [Elegir productos](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Para imprimir una lista de picking a partir de un pedido de venta  
El procedimiento siguiente se basa en un pedido de venta. Los pasos son similares para todos los documentos de ventas que se pueden usar para iniciar el envío de artículos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra el pedido de venta para el que desea elegir productos.  
3. Elija la acción **Informe** y luego elija la acción **Lista de selección por orden**.  
4. Seleccione el botón de **Imprimir** para imprimir la lista de picking o elija el botón de **Vista previa** para verlo en la pantalla.

También puede guardar la lista de picking como un documento, por ejemplo, para enviarla a alguien o para agregarla como un archivo adjunto al pedido de ventas. Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

> [!NOTE]
> Si ha usado la función **Desplegar L.M.** en el pedido de venta, solo se muestran en el informe los componentes del elemento del ensamblado relacionado. Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Consulte también  
[Inventario](inventory-manage-inventory.md)  
[Elegir productos](warehouse-pick-items.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)   
