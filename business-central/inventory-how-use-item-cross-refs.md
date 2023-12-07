---
title: Usar referencias de producto
description: 'Configure referencias entre las descripciones, la unidad de medida y las variantes que usted y su proveedor o cliente utilizan para un artículo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
---
# Usar referencias de producto

Si compra o vende artículos para los que usted y su proveedor o cliente usan términos diferentes, puede establecer una referencia entre sus términos para los artículos y los términos que usa el cliente o el proveedor de ese artículo. De esta manera, la descripción del artículo del proveedor o del cliente, la unidad de medida o el código de variante se insertan automáticamente en los documentos relevantes cuando se completa el **No. de referencia del artículo** .  

## Para configurar una referencia de artículo

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de un producto del que quiera crear una referencia.
3. Elija la acción **Referencias de producto**.

     Si no puede encontrar la acción **Referencias de producto**, elija ver más opciones y luego búsquela en **Relacionado** > **Producto**.
  
4. En una línea nueva en la página **Movimientos de referencia de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Los procedimientos siguientes describen cómo especificar la referencia del artículo en un pedido de compra. Pasos similares se aplican a documentos de venta y otros documentos de compra.  

## Para introducir la descripción del producto de un proveedor en un documento

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.
2. Cree un pedido de compra para el proveedor para el que configuró una referencia del producto en el procedimiento anterior.
3. Cree una línea de compra para el producto para el que configuró una referencia del producto en el procedimiento anterior.
4. En el campo **N.º de referencia producto** seleccione la referencia de producto relevante y después seleccione el botón **Aceptar**.

El campo **Descripción** de la línea se sobrescribe con la descripción del producto del proveedor, tal como está configurado en la entrada de referencia del producto. Si la referencia de artículo incluye un código de variante o una unidad de medida, estos valores también se copian en el documento.  

## Escanear códigos de barras con la aplicación móvil Business Central

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

La siguiente tabla enumera las páginas que admiten el escaneado de códigos de barras de referencias de artículos desde la aplicación móvil [!INCLUDE [prod_short](includes/prod_short.md)].

|Página  |Valor del campo que puede escanear  |
|---------|---------|
|Referencia artículo     | N.º referencia        |
|Lín. diario producto     | N.º referencia prod.        |
|Línea pedido inv. fís.     |N.º referencia prod.         |
|Lín. compra     |   N.º referencia prod.      |
|Lín. venta     | N.º referencia prod.        |

## Consulte también

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
