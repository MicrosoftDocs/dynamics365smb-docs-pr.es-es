---
title: Archivar documentos de venta y compra
description: Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos para poder usar el documento archivado para recrear el documento desde el que se archivó.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: a12d8d7a11e581a6cfe93b6a1f4588cd87efc98f
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543277"
---
# <a name="archive-documents"></a>Archivar documentos
Puede archivar pedidos de compra y venta, ofertas, pedidos de devolución y pedidos abiertos, por ejemplo, porque desea guardar una copia de un documento para reutilizarla más tarde. Puede archivar un documento de ventas o compras varias veces y guardar una versión archivada diferente cada vez.

Para documentos de ventas archivados donde el original aún existe y no está registrado, puede usar la función **Restaurar** para sobrescribir el original con la versión archivada del documento. Esto es práctico si tiene que restaurar el contenido de un documento a un estado anterior.

Para los documentos archivados en los que se elimina el original, solo puede reutilizar el contenido copiando los datos, por ejemplo, con la función **Copiar desde documento**.  

## <a name="to-set-up-automatic-document-archiving"></a>Para configurar el archivado automático de documentos

Puede configurar el archivado automático de pedidos de venta y compra, presupuestos, pedidos abiertos y órdenes de devolución antes de eliminar documentos.

El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas. Los pasos son parecidos para documentos de compra.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Conf. ventas y cobros**, rellene los campos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Específicamente para el campo **Archivar ofertas**, la siguiente tabla describe la diferencia entre las opciones.

|Opción|Descripción|
|------|-----------|
|**Nunca**| Nunca archivar las ofertas de venta cuando se eliminan.|
|**Pregunta**|Seleccione solicitar al usuario que elija si desea archivar ofertas de ventas cuando se eliminan.|
|**Siempre**|Seleccione archivar automáticamente las ofertas de venta cuando se eliminan.|

## <a name="to-archive-a-sales-order"></a>Archivar pedidos de venta

El siguiente procedimiento describe cómo archivar una orden de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra un pedido de venta del que desee archivar.  
3. Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la página **Pedidos de venta archivados**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Para restaurar un pedido de venta no registrado desde el archivo

El procedimiento siguiente describe cómo traer el contenido de un pedido de venta archivado de nuevo al pedido de venta original. Esto solo es posible cuando el documento original no se ha registrado. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.  

El contenido del pedido original se sustituyen con el de la versión almacenada seleccionada.

## <a name="to-delete-archived-sales-orders"></a>Para eliminar pedidos de venta archivados

El siguiente procedimiento describe cómo eliminar pedidos de venta archivados. Los pasos son similares para otros documentos de compra y venta archivados.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.  
2. Elija la acción **Eliminar versiones pedido venta archiv.** y luego, en la página **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.  
3. Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también

[Seguimiento de líneas de documentos](across-how-to-track-document-lines.md)  
[Ccial](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
