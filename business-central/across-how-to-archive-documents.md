---
title: Archivar documentos de venta y compra
description: Puede archivar pedidos de compra y venta, ofertas, pedidos de devolución y pedidos abiertos, y restaurar los originales si es necesario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 03/06/2022
ms.author: bholtorf
ms.openlocfilehash: c81248844f603f80304822c0ce089c666f9be9bc
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950334"
---
# <a name="archive-documents"></a>Archivar documentos
Puede archivar pedidos de venta y de compra, ofertas, devoluciones y pedidos abiertos. Archivar documentos le permite restaurar el original, si es necesario. Puede archivar un documento de ventas o compras varias veces y guardar una versión archivada diferente cada vez.

Para documentos de ventas archivados donde el original aún existe y no está registrado, puede usar la acción **Restaurar** para sobrescribir el documento original con una versión archivada del documento. 

Para los documentos archivados en los que se elimina el original, solo puede reutilizar el contenido copiando los datos, por ejemplo, usando la acción **Copiar desde documento**.  

## <a name="to-set-up-automatic-document-archiving"></a>Para configurar el archivado automático de documentos

Puede configurar el archivado automático de pedidos de venta y compra, presupuestos, pedidos abiertos y órdenes de devolución. Cuando el archivado automático está activado, se crea una nueva versión del documento archivado cuando alguien hace lo siguiente:

* Cambia o elimina un documento.
* Imprime, descarga o envía un documento por correo electrónico.
* Convierte una oferta en un pedido o factura.
* Publica un pedido.

El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas. Los pasos son parecidos para documentos de compra.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En la ficha desplegable **archivar**, especifique si desea activar el archivo automático para los distintos tipos de documentos de ventas. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

En la siguiente tabla se describen las opciones para el campo **Archivar ofertas**.

|Opción|Descripción|
|------|-----------|
|**Nunca**| No archive ofertas de venta cuando se eliminan.|
|**Pregunta**|Solicite al usuario que elija si desea archivar ofertas de ventas cuando se eliminan.|
|**Siempre**|Archive automáticamente las ofertas de venta cuando se eliminan.|

## <a name="to-archive-a-sales-order"></a>Archivar pedidos de venta

El siguiente procedimiento describe cómo archivar una orden de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra un pedido de venta del que desee archivar.  
3. Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la página **Pedidos de venta archivados**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Para restaurar un pedido de venta no registrado desde el archivo

El procedimiento siguiente describe cómo restaurar un pedido de venta archivado al pedido de venta original. Restaurar un documento solo es posible cuando el documento original no se ha registrado. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.  

El contenido del pedido original se sustituye con el de la versión archivada.

## <a name="to-delete-archived-sales-orders"></a>Para eliminar pedidos de venta archivados

El siguiente procedimiento describe cómo eliminar pedidos de venta archivados. Los pasos son similares para otros documentos de compra y venta archivados.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.  
2. Elija la acción **Eliminar versiones más antiguas** y luego, en la página **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.  
3. Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también

[Seguimiento de líneas de documentos](across-how-to-track-document-lines.md)  
[Ccial](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
