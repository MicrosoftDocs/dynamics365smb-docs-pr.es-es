---
title: Cómo archivar ventas y documentos de compra | Documentos de Microsoft
description: Puede archivar pedidos de compra y venta, presupuestos, órdenes de devolución y pedidos abiertos y puede usar el documento archivado para recrear el documento desde el que se archivó.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/14/2018
ms.author: sgroespe
ms.openlocfilehash: 2f05313d30aede255e4ef49065f0189d649ce93c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806566"
---
# <a name="archive-documents"></a>Archivar documentos
Puede archivar pedidos de compra y venta, ofertas, pedidos de devolución y pedidos abiertos, por ejemplo, porque desea guardar una copia de un documento para reutilizarla más tarde. Puede archivar un documento de ventas o compras varias veces y guardar una versión archivada diferente cada vez.

Para documentos archivados donde el original aún existe y no está registrado, puede usar la función **Restaurar** para sobrescribir el original con la versión archivada del documento. Esto es práctico si tiene que restaurar el contenido de un documento a un estado anterior.

Para los documentos archivados en los que se elimina el original, solo puede reutilizar el contenido copiando los datos, por ejemplo, con la función **Copiar documento**.   

## <a name="to-set-up-automatic-document-archiving"></a>Para configurar el archivado automático de documentos  
Puede configurar el archivado automático de pedidos de venta y compra, presupuestos, pedidos abiertos y órdenes de devolución antes de eliminar documentos.

El siguiente procedimiento describe cómo configurar el archivado automático de los documentos de ventas. Los pasos son parecidos para documentos de compra.
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Conf. ventas y cobros**, rellene los campos del modo que se indica a continuación.

|Campo|Description|
|-----|-----------|
|**Archivar ofertas venta**|**Nunca** para no archivar las ofertas de venta cuando se eliminan. **Pregunta** para solicitar al usuario que elija si desea archivar ofertas de ventas cuando se eliminan. **Siempre** para archivar automáticamente las ofertas de venta cuando se eliminan.|
|**Archivar pedidos de venta abiertos**|Seleccione archivar pedidos de venta genéricos automáticamente cada vez que se eliminen.|
|**Ped. arch. y Ped. dev.**|Seleccione archivar automáticamente pedidos de venta cada vez que se eliminen.|

## <a name="to-archive-a-sales-order"></a>Archivar pedidos de venta
El siguiente procedimiento describe cómo archivar una orden de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  Abra un pedido de venta del que desee archivar.  
3.  Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la página **Pedidos de venta archivados**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Para restaurar un pedido de venta no registrado desde el archivo
El procedimiento siguiente describe cómo traer el contenido de un pedido de venta archivado de nuevo al pedido de venta original. Esto solo es posible cuando el documento original no se ha registrado. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos de venta archivados** y luego elija el enlace relacionado.
2. Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.  

El contenido del pedido original se sustituyen con el de la versión almacenada seleccionada.

## <a name="to-delete-archived-sales-orders"></a>Para eliminar pedidos de venta archivados
El siguiente procedimiento describe cómo eliminar pedidos de venta archivados. Los pasos son similares para otros documentos de compra y venta archivados.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar versiones pedido venta archiv.** y luego elija el enlace relacionado.  
2.  En la página **Eliminar versiones pedido venta archiv.**, seleccione los filtros apropiados.  
3.  Elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Seguimiento de líneas de documentos](across-how-to-track-document-lines.md)  
[Ventas](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
