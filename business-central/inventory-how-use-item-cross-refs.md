---
title: Uso de referencias cruzadas de productos | Documentos de Microsoft
description: Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**. .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244050"
---
# <a name="use-item-cross-references"></a>Usar referencias cruzadas de producto
Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**. . Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.

Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra. Los pasos son parecidos para la venta.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.
3. Seleccione la acción **Referencias cruzadas**.
4. En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Para introducir la descripción del producto de un proveedor en un pedido de compra
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Pedidos compra** y luego elija el enlace relacionado.
2. Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.
3. Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.
4. En el campo **Nº tipo referencia cruzada** seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.

El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
