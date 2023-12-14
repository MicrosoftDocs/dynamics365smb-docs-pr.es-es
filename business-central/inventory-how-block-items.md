---
title: Cómo bloquear productos o variantes de producto desde Ventas o Compras
description: 'Puede bloquear elementos y variantes de producto para que no se introduzcan en líneas de documentos de compra y venta, así como no se registren en una transacción.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
---
# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Bloquear productos o variantes de producto desde Ventas o Compras

Puede bloquear productos y variantes de productoque un producto entre en líneas de documentos de compra y venta, y puede bloquearlos para que no se registre en transacciones. Por ejemplo, esto es útil cuando un artículo tiene un defecto conocido. Si alguien elige un artículo bloqueado o variante en un documento de compra o venta, un mensaje le informará de que el artículo está bloqueado.

En la tabla siguiente se describe qué sucede cuando se bloquean los artículos o variantes.  

|Opción|Descripción|  
|--------------------|------------|  
|**Ventas bloqueadas**|No puede elegir el producto o variante en un documento de venta ni en un diario de productos de venta.|  
|**Compras bloqueadas**|No puede elegir el producto o variante en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.|  
|**Bloqueado**|No puede incluir el artículo o la variante cuando registra transacciones.|  

> [!NOTE]
> Los productos bloqueados se pueden devolver. Esto significa que ninguna de las opciones de configuración anteriores se aplica a devoluciones y abonos.

Cuando usa la acción **Copiar de documento** para crear nuevos documentos basados en documentos existentes, se le notifica si algún producto o variante en las líneas del documento de origen está bloqueado. Las líneas de documento bloqueadas se excluyen del nuevo documento y una notificación muestra una descripción general de todas las líneas de documento que están bloqueadas en el documento de origen.

## <a name="to-block-an-item"></a>Para bloquear un artículo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Dependiendo de qué quiera hacer, seleccione el producto y después elija una o más de las casillas de comprobación siguientes:
    * **Bloqueado**
    * **Ventas bloqueadas**
    * **Compras bloqueadas**  

## <a name="to-block-an-item-variant"></a>Para bloquear una variante de artículo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione el artículo que tiene una variante que desea bloquear, elija **Variantes** y luego elija una o más de las siguientes casillas de verificación:  
    * **Bloqueado**
    * **Ventas bloqueadas**
    * **Compras bloqueadas**

## <a name="see-also"></a>Consulte también

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
