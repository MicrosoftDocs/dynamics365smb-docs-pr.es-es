---
title: Imprimir una lista de picking de inventario a partir de un pedido de venta
description: Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, ventas, factura y otros documentos de venta de salida.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4cddce48df3be0a3fadaa74ed751b274ccce7f31
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115466"
---
# <a name="print-the-picking-list"></a>Imprimir la lista de picking

Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas y otros documentos que inicien el envío de los productos.

Este informe se utiliza normalmente en empresas sin funcionalidad dedicada para la gestión de almacenes, de modo que un trabajador de inventario pueda ver o imprimir simplemente la lista de picking del documento de ventas relacionado. En empresas con un volumen más alto o procesos más complejos, el picking se planifica y se realiza en documentos de almacén dedicados. Para obtener más información, consulte [Elegir productos](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Para imprimir una lista de picking a partir de un pedido de venta

El procedimiento siguiente se basa en un pedido de venta. Los pasos son similares para otros documentos de ventas que se pueden usar para iniciar el envío de productos, como pedidos de transferencia.

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
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]