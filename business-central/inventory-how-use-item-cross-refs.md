---
title: Usar referencias de producto
description: 'Configure referencias entre las descripciones, la unidad de medida y las variantes que usted y su proveedor o cliente utilizan para un artículo.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: edupont
---
# <a name="use-item-references"></a>Usar referencias de producto

Si compra o vende artículos para los que usted y su proveedor o cliente usan términos diferentes, puede establecer una referencia entre sus términos para los artículos y los términos que usa el cliente o el proveedor de ese artículo. De esta manera, la descripción del artículo del proveedor o del cliente, la unidad de medida o el código de variante se insertan automáticamente en los documentos relevantes cuando se completa el **No. de referencia del artículo** .  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> No todas las empresas utilizan referencias de artículos. Para minimizar el desorden en las páginas, hemos ocultado los campos y acciones relacionados de forma predeterminada. Si decide utilizarlos, puede seleccionar el campo **Usar referencias de producto** en la página **Configuración de inventario**. Después de habilitar las referencias de productos, los campos y las acciones están disponibles en las páginas Ficha de producto, Ficha de proveedor y Ficha de cliente y en los documentos de compra y venta.
>
> En versiones anteriores al lanzamiento de versiones 2 de 2021, su administrador puede activar la característica *Escribir referencias de productos más largas* en la página [Gestión de funciones](https://businesscentral.dynamics.com/?page=2610) (el vínculo requiere que tenga un suscriptor [!INCLUDE [prod_short](includes/prod_short.md)]). La forma en que usa las referencias no cambia, pero los nombres de cosas como páginas y botones sí. Por ejemplo, la página **Entradas de referencias cruzadas de productos** se convertirá en la página **Entradas de referencia de artículo**.

## <a name="to-start-using-item-references"></a>Para comenzar a usar referencias de productos

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, escriba **Configuración de inventario** y luego elija el enlace relacionado.
2. Seleccione el campo **Usar referencias de artículos** campo.

## <a name="to-set-up-an-item-reference"></a>Para configurar una referencia de artículo

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de un producto del que quiera crear una referencia.
3. Elija la acción **Referencias de producto**.

     Si no puede encontrar la acción **Referencias de producto**, elija ver más opciones y luego búsquela en **Relacionado** > **Producto**.
  
4. En una línea nueva en la página **Movimientos de referencia de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Los procedimientos siguientes describen cómo especificar la referencia del artículo en un pedido de compra. Pasos similares se aplican a documentos de venta y otros documentos de compra.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Para introducir la descripción del producto de un proveedor en un documento

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Cree un pedido de compra para el proveedor para el que configuró una referencia del producto en el procedimiento anterior.
3. Cree una línea de compra para el producto para el que configuró una referencia del producto en el procedimiento anterior.
4. En el campo **N.º de referencia producto** seleccione la referencia de producto relevante y después seleccione el botón **Aceptar**.

El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia del producto. Si la referencia de artículo incluye un código de variante o una unidad de medida, estos valores también se copian en el documento.  

## <a name="see-also"></a>Consulte también

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
