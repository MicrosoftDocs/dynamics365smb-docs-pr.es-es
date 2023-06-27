---
title: Deshacer registro de ensamblado.
description: Aprenda a corregir errores en una orden de ensamblado registrada.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="undo-assembly-posting"></a><a name="undo-assembly-posting"></a>Deshacer registro de ensamblado.

Deshacer la publicación de una orden de ensamblado para corregir un error o eliminar una publicación no deseada.

Cuando se deshace un pedido de ensamblado registrado, se crean movimientos de producto correctores para revertir las entradas originales. Cada entrada positiva de salida para el artículo de montaje se revierte mediante una entrada negativa de salida. Cada entrada de consumo negativo de un componente de ensamblado se revierte mediante una entrada de consumo positivo. La solicitud del coste fijo se crea automáticamente entre las entradas correctoras y originales para garantizar una reversión exacta del coste.  

Cuando deshace un pedido de ensamblado registrado por completo, puede volver a crear el pedido original. Por ejemplo, para hacer correcciones antes de volver a publicarlo.  

Cuando se deshace parcialmente un pedido de ensamblado registrado, todos los campos de cantidad afectados, por ejemplo **Cantidad ensamblada**, **Cantidad consumida** y **Cantidad pendiente**, se restablecen a los valores que tenían antes del registro.  

Para volver a crear o restaurar los pedidos de ensamblado, el artículo del registro original debe cumplir estas condiciones:  

* Todavía está en inventario. Es decir, no debe haberse vendido ni consumido de otra forma por las transacciones de salida.  
* No está reservado.  
* Está en la ubicación que de salida.  

Los pedidos de ensamblado existentes se pueden restablecer sólo si no se modifican el número y la secuencia de líneas en el pedido de ensamblado original.  

> [!TIP]  
> Para resolver conflictos provocados por cambios en las líneas, revierta manualmente los cambios en las líneas en cuestión antes de deshacer el pedido de ensamblado registrado. Puede registrar el pedido de ensamblado y volver a reconstruirlo al deshacer el registro.  

El procedimiento siguiente describe cómo deshacer los pedidos de ensamblado registrado que contengan artículos que se ensamblaron para stock. Para deshacer pedidos de ensamblado registrados con artículos ensamblados a pedido, use la acción **Deshacer envío** en el envío registrado relacionado. Para obtener más información sobre cómo deshacer envíos, vaya a [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md). El pedido de ensamblado registrado se deshace tal como se describe en este artículo.  

## <a name="to-undo-posting-of-an-assembly-order"></a><a name="to-undo-posting-of-an-assembly-order"></a>Para deshacer el registro de un pedido de ensamblado

Puede deshacer total o parcialmente las órdenes de ensamblado registradas.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos ensamblados reg.** y, a continuación, el vínculo relacionado.  

   Cada registro parcial crea un pedido de ensamblado registrado diferente.  
2. Abra el pedido de ensamblado registrado que desea revertir y elija la acción **Deshacer ensamblado**.  

    Si el pedido de ensamblado publicado está relacionado con un pedido de ensamblado completamente registrado que se eliminó, puede volver a crear el pedido eliminado. Por ejemplo, puede volver a crear el pedido porque desea volver a procesarlo.  
3. Para volver a crear el orden de montaje, seleccione **Sí**. Para deshacer el registro sin la reconstrucción del pedido de ensamblado, seleccione **No**.  

El campo **Revertido** del pedido de ensamblado cambia a **Sí**. La contabilización del pedido de ensamblado ahora está invertida. Puede procesar todo el pedido de ensamblaje si elige volver a crearlo, o el pedido de ensamblaje abierto que ha restaurado a su estado original.  

> [!NOTE]  
> Para restaurar las cantidades de los registros parciales múltiples en un pedido de ensamblado, deberá deshacer todos los pedidos de ensamblado registrados siguiendo los pasos 1 a 3.  

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Gestión de ensamblaje](assembly-assemble-items.md)  
[Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md)  
[Procesamiento de devoluciones de ventas o cancelaciones](sales-how-process-sales-returns-cancellations.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
