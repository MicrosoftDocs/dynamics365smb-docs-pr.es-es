---
title: Usar referencias cruzadas de producto
description: Configure referencias entre las descripciones que usted y su proveedor usan para un producto para que pueda insertar la descripción del artículo del proveedor en los documentos de compra.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0a9f84522598344435ad9c1263fe8cdea2e2a1e0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785653"
---
# <a name="use-item-cross-references"></a>Usar referencias cruzadas de producto
Si configura una referencia cruzada entre la descripción del producto que usa para un producto y la descripción que utiliza el proveedor de ese producto, la descripción del producto del proveedor se inserta automáticamente en los documentos de compra del proveedor cuando complete el campo **Nº referencia cruzada**. . Se aplica la misma funcionalidad para los números de producto del cliente en los documentos de venta.

Los procedimientos siguientes describen cómo utilizar referencias cruzadas de producto en la compra. Los pasos son parecidos para la venta.

> [!NOTE]
> Es cada vez más común que los identificadores de productos, como GTIN o GUID, contengan 30 o más caracteres, que es más de lo que la función actual para referencias cruzadas de productos puede manejar. Si necesita utilizar referencias que contengan más de 30 caracteres, su administrador puede activar la característica **Escribir referencias de productos más largas** en la página [Gestión de funciones](https://businesscentral.dynamics.com/?page=2610) (el vínculo requiere que tenga un suscriptor [!INCLUDE[prod_short](includes/prod_short.md)]). La forma en que usa las referencias no cambia, pero los nombres de cosas como páginas y botones sí. Por ejemplo, la página **Entradas de referencias cruzadas de productos** se convertirá en la página **Entradas de referencia de artículo**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Para configurar una referencia cruzada de producto en la descripción del producto de un proveedor

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de un producto para el que desea crear una referencia cruzada a la descripción del producto que el proveedor utiliza para dicho producto.
3. Seleccione la acción **Referencias cruzadas**.

     Si no puede encontrar la acción **Referencias cruzadas**, elija ver más opciones y luego búsquela en **Relacionado** > **Producto**.
  
4. En una línea nueva en la página **Movimientos de referencia cruzada de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Para introducir la descripción del producto de un proveedor en un pedido de compra

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de compra** y luego elija el enlace relacionado.
2. Cree un pedido de compra para el proveedor para el que configuró una referencia cruzada del producto en el procedimiento anterior.
3. Cree una línea de compra para el producto para el que configuró una referencia cruzada del producto en el procedimiento anterior.
4. En el campo **Nº tipo referencia cruzada** seleccione la referencia cruzada de producto que ha creado y después seleccione el botón **Aceptar**.

El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia cruzada del producto.

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]