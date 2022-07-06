---
title: Crear y administrar productos en catálogo
description: Describe cómo vender artículos que no mantiene en su lista de artículos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: c12eb256d4e7f1e211e28dacf4c403406dba3d85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077012"
---
# <a name="work-with-catalog-items"></a>Trabajar con productos del catálogo

Los elementos del catálogo son artículos que no administra en [!INCLUDE[prod_short](includes/prod_short.md)] hasta que los vende. Cuando usa la acción **Seleccionar artículo del catálogo** para agregar un artículo de catálogo a una línea en un pedido u ofertaa de ventas, el artículo de catálogo se convierte en un artículo normal.

> [!NOTE]  
> No puede seleccionar un producto del catálogo de la página **Facturas venta**.

Un producto del catálogo normalmente tiene el número del proveedor que lo suministra. Antes de que pueda convertir un artículo del catálogo en un artículo normal, debe especificar cómo convertir los números de artículos del proveedor a su numeración de artículos. Para obtener más información, consulte [Especificar cómo los números de productos del catálogo se convierten a su propia numeración](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Los artículos del catálogo no deben confundirse con los artículos que no están en el inventario, que son artículos regulares a los que se les asigna el tipo **No inventario** para mantenerlos fuera de disponibilidad y de los cálculos de costes, por ejemplo, porque solo se usan internamente y tienen un bajo coste. Para obtener más información, consulte [unidad física sin seguimiento en el inventario](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Crear un producto del catálogo

Las fichas de productos del catálogo disponen de mucha menos información que las normales puesto que solo las utiliza en ofertas de ventas y en otras maneras. Por esa razón, se convertirán en fichas de producto normal antes de que pueda registrarles las transacciones de venta.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos del catálogo** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Especificar cómo los números de productos del catálogo se convierten a su propia numeración

Antes de que pueda convertir un artículo del catálogo en un artículo normal, debe especificar cómo convertir los números de artículos del proveedor a su numeración de artículos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de productos de catálogo** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Convertir un producto del catálogo en un producto normal

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos del catálogo** y luego elija el enlace relacionado.
2. Abra la ficha de un producto del catálogo que desee convertir a uno normal.
3. En la página **Ficha de producto del catálogo**, seleccione la acción **Crear producto**.

Se ha creado una plantilla y una nueva ficha de producto con la información del producto del catálogo rellenada previamente. Si es necesario, podrá rellenar o editar los campos en la nueva ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Para vender un producto del catálogo y convertirlo en un producto normal

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**. Rellene los campos de la ficha desplegable **General** para cada pedido. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
3. En una nueva línea de venta, en el campo **Tipo**, seleccione **Producto**, pero deje **N.º** campo vacío.
4. Elija la acción **Línea** y, a continuación, elija la acción **Seleccionar artículos del catálogo**.

    El producto del catálogo se ha convertido en un producto normal. Se ha creado una plantilla y una nueva ficha de producto con la información del producto del catálogo rellenada previamente.
5. En la página **Productos del catálogo**, seleccione el producto del catálogo que desee vender y, a continuación, haga clic en **Aceptar**.
6. Cuando el pedido de venta ya está completo, seleccione la acción **Registrar**.

Si es necesario, podrá rellenar o editar los campos en la nueva ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

> [!NOTE]  
> Una referencia de producto se crea automáticamente entre el número del producto del proveedor y su nuevo número de producto. Para obtener más información, vea [Usar referencias de producto](inventory-how-use-item-cross-refs.md).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
