---
title: Archivar documentos de venta y compra
description: 'Puede archivar pedidos de venta y de compra, ofertas, devoluciones y pedidos abiertos.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# Archivar documentos

Puede archivar pedidos de venta y de compra, ofertas, devoluciones y pedidos abiertos. Si está utilizando funciones de administración de proyectos, también puede archivar sus proyectos. Puede archivar documentos y proyectos varias veces, lo que guarda una versión archivada diferente cada vez.

Para documentos de ventas, si el original aún existe y no está registrado, puede usar la acción **Restaurar** para sobrescribirlo con una versión archivada del documento. 

> [!NOTE]
> Solo puede restaurar documentos y proyectos de ventas. La acción no está disponible para documentos de compra archivados.

Para los documentos archivados en los que se elimina el original, puede reutilizar el contenido copiando los datos, por ejemplo, usando la acción **Copiar desde documento**.  

## Para configurar el archivado automático de documentos

Puede automatizar el archivado para crear una nueva versión del documento archivado cuando alguien haga lo siguiente:

* Cambia o elimina un documento o proyecto.
* Imprime, descarga o envía un documento por correo electrónico.
* Convierte una oferta en un pedido o factura.
* Publica un pedido.

Los siguientes pasos describen cómo configurar el archivado automático de documentos de ventas desde la página **Configuración de ventas y cuentas por cobrar**. Los pasos son similares para los documentos de compra y los proyectos. Para documentos de compra, utilice la página **Compras y cuentas por pagar**. Para proyectos, utilice la página **Configuración del proyecto**.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. En la ficha desplegable **archivar**, especifique si desea activar el archivo automático para los distintos tipos de documentos de ventas. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

En la siguiente tabla se describen las opciones para el campo **Archivar ofertas**.

|Opción|Descripción|
|------|-----------|
|**Nunca**| No archive ofertas de venta cuando se eliminan.|
|**Pregunta**|Solicite al usuario que elija si desea archivar ofertas de ventas cuando se eliminan.|
|**Siempre**|Archive automáticamente las ofertas de venta cuando se eliminan.|

## Archivar manualmente pedidos de venta

El siguiente procedimiento describe cómo archivar manualmente un pedido de venta. Los pasos son similares para todos los documentos y proyectos que puede archivar.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Abra un pedido de venta del que desee archivar.  
3. Elija la acción **Archivar documento**.

El pedido de ventas está archivado. Puede verlo en la página **Pedidos de venta archivados**.

## Para restaurar un documento de ventas no contabilizado o un proyecto del archivo

El procedimiento siguiente describe cómo restaurar un pedido de venta archivado al pedido de venta original. Restaurar un documento solo es posible cuando el documento original no se ha registrado. Los pasos son similares para todos los pedidos, pedidos abiertos, pedidos de devolución y presupuestos y también para proyectos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos pedido venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta archivado, o una versión de este, que desea restaurar y después seleccione **Volver a crear**.  

El contenido del pedido de cliente o proyecto original se sustituye por la versión archivada.

## Para eliminar versiones archivadas

Use una política de retención para limpiar las versiones archivadas que ya no necesita. Las políticas de retención permiten a los administradores definir cuánto tiempo desean almacenar los datos. Por ejemplo, pueden configurar una política que elimine datos después de una fecha de vencimiento. Para obtener más información, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Hay algunas cosas a tener en cuenta sobre la creación de políticas de retención para documentos y proyectos archivados:

* Si no se elimina el documento original, [!INCLUDE [prod_short](includes/prod_short.md)] no eliminará las versiones archivadas. Las versiones archivadas no caducan mientras exista el original.
* Cuando configura la directiva de retención, puede especificar que desea que la política elimine todas las versiones archivadas excepto la más reciente. Por ejemplo, puede tener 10 versiones y desea conservar una copia de la última. 
* [!INCLUDE [prod_short](includes/prod_short.md)] calcula la fecha de caducidad de los documentos en función de la fecha de la versión archivada más reciente.

## Consulte también

[Seguir líneas de documentos](across-how-to-track-document-lines.md)  
[Ventas](sales-manage-sales.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
