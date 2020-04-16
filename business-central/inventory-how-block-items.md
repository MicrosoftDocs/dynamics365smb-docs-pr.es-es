---
title: Cómo bloquear productos de venta o de compra
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182305"
---
# <a name="block-items-from-sales-or-purchasing"></a>Bloquear productos de venta o de compra
Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.  

La siguiente tabla muestra qué sucede cuando se bloquean los productos.  

|Opción|Description|  
|--------------------|------------|  
|**Venta bloqueada**|No puede introducir el producto en un documento de venta ni en un diario de productos de venta.|  
|**Compra bloqueada**|No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.|  
|**Bloqueado**|No puede usar el producto en ninguna transacción de producto.|  

> [!NOTE]
> Los productos bloqueados se pueden devolver. Esto significa que ninguna de las opciones de configuración anteriores se aplica cuando se utiliza el producto en devoluciones y abonos.

Cuando usa la función **Copiar de documento** para crear nuevos documentos basados en documentos existentes, se le notifica si algún producto en las líneas del documento de origen está bloqueado. Las líneas de documento bloqueadas se excluyen del nuevo documento y una notificación muestra una descripción general de todas las líneas de documento que están bloqueadas en el documento de origen.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Para bloquear que un producto se introduzca en líneas de venta  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.  

Si intenta introducir el producto en un documento de venta o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Para bloquear que un producto se introduzca en líneas de compra  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.  

Si intenta introducir el producto en un documento de compra o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="to-block-an-item-from-being-posted"></a>Para bloquear que se registre un producto
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.

Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="see-also"></a>Consulte también  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
