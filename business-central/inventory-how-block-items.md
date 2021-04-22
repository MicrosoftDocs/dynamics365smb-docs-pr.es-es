---
title: Cómo bloquear productos de venta o de compra
description: Puede evitar que se use un artículo, por ejemplo, en documentos de compra o venta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bc130d6982d969084f7fcbf3618893978317f36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786053"
---
# <a name="block-items-from-sales-or-purchasing"></a>Bloquear productos de venta o de compra
Puede bloquear que un producto entre en líneas de documentos de compra y venta, y puede bloquearlo para que no se registre en ninguna transacción. Por ejemplo, esto es útil cuando un artículo tiene un defecto conocido. Si alguien elige un artículo bloqueado en un documento de compra o venta, un mensaje le informará de que el artículo está bloqueado.

En la tabla siguiente se describe qué sucede cuando se bloquean los artículos.  

|Opción|Descripción|  
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

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Para bloquear que un producto se introduzca en líneas de compra  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.  

## <a name="to-block-an-item-from-being-posted"></a>Para bloquear que se registre un producto
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.

## <a name="see-also"></a>Consulte también  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]