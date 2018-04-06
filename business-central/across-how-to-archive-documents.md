---
title: "Cómo archivar ventas y documentos de compra | Documentos de Microsoft"
description: "Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos y puede usar el documento archivado para recrear el documento desde el que se archivó."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Archivar documentos
Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos y puede usar el documento archivado para recrear el documento desde el que se archivó.

## <a name="to-set-up-automatic-document-archiving"></a>Para configurar el archivado automático de documentos  
Puede configurar el archivado automático de pedidos de venta y compra, presupuestos, pedidos abiertos y órdenes de devolución antes de eliminar documentos.

El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas. Los pasos son parecidos para documentos de compra.
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conf. ventas y cobros** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Conf. ventas y cobros**, rellene los campos de la manera siguiente:

|Campo|Description|
|-----|-----------|
|**Archivar ofertas venta**|**Nunca** para no archivar las ofertas de venta cuando se eliminan. **Pregunta** para solicitar al usuario que elija si desea archivar ofertas de ventas cuando se eliminan. **Siempre** para archivar automáticamente las ofertas de venta cuando se eliminan.|
|**Archivar pedidos de venta abiertos**|Seleccione archivar pedidos de venta genéricos automáticamente cada vez que se eliminen.|
|**Ped. arch. y Ped. dev.**|Seleccione archivar automáticamente pedidos de venta cada vez que se eliminen.|

## <a name="to-archive-a-sales-order"></a>Archivar pedidos de venta
El siguiente procedimiento describe cómo archivar una orden de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra un pedido de venta del que desee archivar.  
3.  Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la ventana **Pedidos de venta archivados**. Desde este momento, también puede usarlo para volver a crear el pedido de venta desde el que se archivó.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Para volver a crear un pedido de venta desde el archivo
El siguiente procedimiento describe cómo volver a crear una orden de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta archivados** y, a continuación, seleccione el vínculo relacionado.
2.  Seleccione el pedido de venta archivado que desea volver a crear y después seleccione **Volver a crear**.  

El pedido de venta se crea y se agrega a la ventana **Pedidos venta**.

## <a name="to-delete-archived-sales-orders"></a>Para eliminar pedidos de venta archivados
El siguiente procedimiento describe cómo eliminar pedidos de venta archivados. Los pasos son similares para otros documentos de compra y venta archivados.

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar versiones pedido venta archiv.** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.  
3.  Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Seguimiento de líneas de documentos](across-how-to-track-document-lines.md)  
[Ventas](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

