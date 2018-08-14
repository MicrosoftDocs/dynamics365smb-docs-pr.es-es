---
title: "Cómo bloquear productos de venta o de compra"
description: "En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: es-es
ms.lasthandoff: 07/30/2018

---
# <a name="block-items-from-sales-or-purchasing"></a>Bloquear productos de venta o de compra
Puede bloquear que un producto entre en líneas de compras y ventas, y puede bloquearlo para que no se registre en ninguna transacción.  

La siguiente tabla muestra qué sucede cuando se bloquean los productos.  

|Opción|Description|  
|--------------------|------------|  
|**Venta bloqueada**|No puede introducir el producto en un documento de venta ni en un diario de productos de venta.|  
|**Compra bloqueada**|No puede introducir el producto en un documento de compra, en un diario de productos de compra ni en procesos de planificación de compras.|  
|**Bloqueado**|No puede usar el producto en ninguna transacción de producto. Para obtener más información sobre el bloqueo de un producto para todos los propósitos, consulte la ficha de producto.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Para bloquear que un producto se introduzca en líneas de venta  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Venta bloqueada**.  

Si intenta introducir el producto en un documento de venta o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Para bloquear que un producto se introduzca en líneas de compra  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Compra bloqueada**.  

Si intenta introducir el producto en un documento de compra o en una línea de diario, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="to-block-an-item-from-being-posted"></a>Para bloquear que se registre un producto
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el producto que desea bloquear y, a continuación, marque la casilla **Bloqueado**.

Si intenta registrar algún tipo de transacción para el producto, ahora obtendrá un mensaje de error que indica que el producto está bloqueado.

## <a name="see-also"></a>Consulte también  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  

