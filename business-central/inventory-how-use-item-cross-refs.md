---
title: Usar referencias de producto
description: Configure referencias entre las descripciones que usted y su proveedor usan para un producto para insertar la descripción del artículo del proveedor en los documentos de compra.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588606"
---
# <a name="use-item-references"></a>Usar referencias de producto
Si configura una referencia entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **N.º referencia de producto**. . Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.

Los procedimientos siguientes describen cómo utilizar referencias de producto en la compra. Los pasos son parecidos para la venta.

> [!NOTE]
> No todas las empresas utilizan referencias de productos, por lo que para minimizar el desorden en las páginas, hemos ocultado los campos y acciones relacionados. Si decide utilizarlos, puede encender el botón de alternancia **Usar referencias de producto** en la página **Configuración de inventario**. Después de habilitar las referencias de productos, los campos y las acciones están disponibles en las páginas Ficha de producto, Ficha de proveedor y Ficha de cliente, y en los documentos de compra y venta.

## <a name="to-start-using-item-references"></a>Para comenzar a usar referencias de productos
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. existencias** y luego elija el enlace relacionado.
2. Active el botón de alternancia **Usar referencias de productos**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Para configurar una referencia de producto en la descripción del producto de un proveedor

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un producto para el que desea crear una referencia a la descripción del producto que el proveedor utiliza para dicho producto.
3. Elija la acción **Referencias de producto**.

     Si no puede encontrar la acción **Referencias de producto**, elija ver más opciones y luego búsquela en **Relacionado** > **Producto**.
  
4. En una línea nueva en la página **Movimientos de referencia de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Para introducir la descripción del producto de un proveedor en un pedido de compra

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Cree un pedido de compra para el proveedor para el que configuró una referencia del producto en el procedimiento anterior.
3. Cree una línea de compra para el producto para el que configuró una referencia del producto en el procedimiento anterior.
4. En el campo **N.º de referencia producto** seleccione la referencia de producto que ha creado y después seleccione el botón **Aceptar**.

El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia del producto.

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]