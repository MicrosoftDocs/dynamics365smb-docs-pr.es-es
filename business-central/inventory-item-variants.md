---
title: Administrar variantes del producto
description: 'Aprenda cómo puede registrar como variantes de producto, productos que son casi idénticos pero varían en color, tamaño o material.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# <a name="manage-product-variants"></a>Administrar variantes del producto

Las variantes de productos son una excelente manera de mantener su lista de productos bajo control. Por ejemplo, si tiene un gran número de productos que son casi idénticos y que se diferencian solo por el color. Puede definir cada variante como un producto independiente. Pero también puede elegir configurar un producto y especificar los distintos colores como variantes de dicho producto.  

> [!TIP]
> Para una introducción práctica al uso de variantes en la producción, consulte [Tutorial: variantes](contoso-coffee/manufacturing/variants.md) para los datos de demostración de Contoso Coffee.  

## <a name="add-variants-to-an-item"></a>Agregar variantes a un producto

Es bastante fácil definir variantes para un artículo.  

### <a name="to-add-variants"></a>Para agregar variantes

1. Abra la [página **Lista de productos**](https://businesscentral.dynamics.com/?page=31) y abra el producto pertinente.  
2. En el  **Elemento** tarjeta, elija la acción  **Relacionado**, luego elija  **Elemento** y luego elija la acción  **Variantes** .  
3. En la página  **Variantes del artículo**, enumere las variantes.  

Luego, cuando crea un documento de ventas y agrega el artículo, puede especificar la variante del artículo en el campo Código de **variante** . Lo mismo se aplica a los documentos de compra.  

## <a name="item-availability-by-variant"></a>Disponibilidad de productos por variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Requerir el uso de variantes

A partir del segundo lanzamiento de versiones de 2022, los administradores pueden solicitar a los usuarios que especifiquen la variante en los documentos y diarios de los artículos que tengan variantes. Para activar la capacidad, en la página **Configuración de inventario** seleccione el campo **Variante obligatoria si existe**. Puede anular esta configuración global en algunos productos específicos.  

En las fichas de artículo, el campo **Variante obligatoria si existe** tiene las siguientes opciones:

|Valor de campo |Descripción|
|---------|----|
|Valor predeterminado (No)| El valor de **Configuración de inventario** se aplica a este producto.|
|N.º| Los usuarios no están obligados a especificar una variante para este producto.|
|Sí| Si el producto tiene una o más variantes, los usuarios deben especificar la variante pertinente. Si no lo hacen, se les bloquea la contabilización de la transacción.|

> [!NOTE]
> Esta configuración no afecta a los artículos que no tienen variantes.

Si la capacidad está activada, no puede registrar movimientos si no se especifica la variante.

## <a name="categories-attributes-and-variants"></a>Categorías, atributos y variantes

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Consulte también .

[Registrar nuevos artículos](inventory-how-register-new-items.md)    
[Configurar información general del inventario](inventory-how-setup-general.md)    
[Tutorial: variantes](contoso-coffee/manufacturing/variants.md)    
