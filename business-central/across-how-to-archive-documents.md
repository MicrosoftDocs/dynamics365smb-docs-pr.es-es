---
title: Archivar documentos de venta y compra
description: 'Puede archivar pedidos de compra y venta, ofertas, pedidos de devolución y pedidos abiertos, y restaurar los originales si es necesario.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 06/02/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# <a name="archive-documents" />Archivar documentos

Puede archivar pedidos de venta y de compra, ofertas, devoluciones y pedidos abiertos. Archivar documentos le permite restaurar el original, si es necesario. Puede archivar un documento de ventas o compras varias veces y guardar una versión archivada diferente cada vez.

Para documentos de ventas archivados donde el original aún existe y no está registrado, puede usar la acción **Restaurar** para sobrescribir el documento original con una versión archivada del documento.

Para los documentos archivados en los que se elimina el original, solo puede reutilizar el contenido copiando los datos, por ejemplo, usando la acción **Copiar desde documento**.  

## <a name="to-set-up-automatic-document-archiving" />Para configurar el archivado automático de documentos

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

## <a name="to-manually-archive-a-sales-order" />Archivar manualmente pedidos de venta

El siguiente procedimiento describe cómo archivar manualmente un pedido de venta. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra un pedido de venta del que desee archivar.  
3. Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la página **Pedidos de venta archivados**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive" />Para restaurar un pedido de venta no registrado desde el archivo

El procedimiento siguiente describe cómo restaurar un pedido de venta archivado al pedido de venta original. Restaurar un documento solo es posible cuando el documento original no se ha registrado. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.  

El contenido del pedido original se sustituye con el de la versión archivada.

## <a name="to-delete-archived-sales-orders" />Para eliminar pedidos de venta archivados

Use una política de retención para limpiar los documentos archivados que ya no necesita. Las políticas de retención permiten a los administradores definir cuánto tiempo desean almacenar los datos. Por ejemplo, pueden configurar una política que elimine datos después de una fecha de vencimiento. Para obtener más información, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Hay algunas cosas a tener en cuenta sobre la creación de políticas de retención para documentos archivados:

* *Si no se eliminó el documento original, Business Central no eliminará las versiones archivadas. Las versiones archivadas no caducan mientras exista el original.
* Cuando configura la directiva de retención, puede especificar que desea que la política elimine todas las versiones archivadas de un documento excepto la más reciente. Por ejemplo, puede tener 10 versiones de un documento y desea conservar una copia de la última. 
* Business Central calcula la fecha de caducidad de los documentos en función de la fecha de la versión archivada más reciente.

## <a name="see-also" />Consulte también

[Seguir líneas de documentos](across-how-to-track-document-lines.md)  
[Ventas](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
