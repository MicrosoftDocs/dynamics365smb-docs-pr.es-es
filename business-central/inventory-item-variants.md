---
title: Administrar variantes de productos
description: 'Aprenda cómo puede registrar como variantes de producto, productos que son casi idénticos pero varían en color, tamaño o material.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
---
# <a name="manage-product-variants"></a>Administrar variantes de productos

Las variantes de productos son una excelente manera de mantener su lista de productos bajo control. Por ejemplo, si tiene un gran número de productos que son casi idénticos y que se diferencian solo por el color. Puede definir cada variante como un producto independiente. Pero elige configurar un producto y especificar los distintos colores como variantes de dicho producto.  

> [!TIP]
> Para una introducción práctica al uso de variantes en la producción, consulte [Tutorial: variantes](contoso-coffee/manufacturing/variants.md) para los datos de demostración de Contoso Coffee.  

## <a name="add-variants-to-an-item"></a>Agregar variantes a un producto

Si su organización ha decidido utilizar variantes, es bastante fácil definir variantes para un producto.  

### <a name="to-add-variants"></a>Para agregar variantes

1. Abra la [página **Lista de productos**](https://businesscentral.dynamics.com/?page=31) y abra el producto pertinente.  
2. En la ficha **Producto**, elija la acción **Producto** y, a continuación, seleccione la acción **Variantes**.  
3. En la página **Variantes producto**, genere una lista de las variantes.  

Luego, cuando cree un documento de ventas y agregue el artículo, podrá especificar la variante del producto en el campo **Código de variante**. Lo mismo se aplica a los documentos de compra.  

## <a name="item-availability-by-variant"></a>Disponibilidad de productos por variante

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Requerir el uso de variantes

A partir del segundo lanzamiento de versiones de 2022, los administradores pueden solicitar a los usuarios que especifiquen la variante en los documentos y diarios de los artículos que tengan variantes. Para activar la capacidad, vaya a la página **Configuración de inventario** y, a continuación, seleccione el campo **Variante obligatoria si existe**. Puede anular esta configuración global en algunos productos específicos.  

En las fichas de artículo, el campo **Variante obligatoria si existe** tiene las siguientes opciones:

|Valor de campo |Descripción|
|---------|----|
|Valor predeterminado| El valor de **Configuración de inventario** se aplica a este producto.|
|No| Los usuarios no están obligados a especificar una variante para este producto.|
|Sí| Si el producto tiene una o más variantes, los usuarios deben especificar la variante pertinente. Si no lo hacen, no podrán registrar la transacción.|

> [!NOTE]
> Esta configuración no afecta a los artículos que no tienen variantes.

Si la capacidad está activada, los usuarios no pueden registrar movimientos si no se especifica la variante.

## <a name="categories-attributes-and-variants"></a>Categorías, atributos y desviaciones

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar información de inventario general](inventory-how-setup-general.md)  
[Tutorial: variantes](contoso-coffee/manufacturing/variants.md)  
