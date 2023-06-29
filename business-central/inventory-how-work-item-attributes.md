---
title: Configurar atributos de producto y asignarlos a los productos
description: 'Describe cómo configurar los valores de atributo de producto, por ejemplo, que pueden utilizarse como palabras de búsqueda, y asignarlos a productos y categorías de productos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'categories, search words, facets'
ms.search.forms: '7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-item-attributes"></a><a name="work-with-item-attributes"></a><a name="work-with-item-attributes"></a>Trabajar con atributos de producto

Cuando los clientes hacen consultas sobre un producto, ya sea por correspondencia o en una tienda en línea integrada, pueden preguntar por las características como la altura y el año del modelo. Para proporcionar este servicio al cliente, puede asignar valores de atributo de producto de diferentes tipos a sus productos, que podrán usarse posteriormente en la búsqueda de productos.

También puede asignar los atributos de producto a categorías de producto que se aplican después a los productos que las utilizan. Para obtener más información, consulte [Clasificar productos](inventory-how-categorize-items.md).

> [!TIP]  
> Si asocia imágenes a productos, la extensión Analizador de imágenes puede detectar los atributos en la imagen y sugerir los atributos que puede decidir si se los asigna. La extensión está lista para usarse. Solo debe habilitarla. Para obtener más información, vea [Extensión del analizador de imágenes](ui-extensions-image-analyzer.md).

## <a name="create-item-attributes"></a><a name="create-item-attributes"></a><a name="create-item-attributes"></a>Crear atributos de producto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , entr en **Atributos de producto** y luego elija el enlace relacionado.
2. En la página **Atributos de producto**, seleccione la acción **Nuevo**.
3. En la página **Atributos de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si selecciona **Opción** en el campo **Tipo**, puede seleccionar la acción **Valores de atributo de producto** para crear valores de atributo de producto. Para obtener más información, consulte [Para crear valores de atributo de producto del tipo Opción](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="create-values-for-item-attributes-of-type-option"></a><a name="create-values-for-item-attributes-of-type-option"></a><a name="create-values-for-item-attributes-of-type-option"></a>Crear los valores de los atributos de producto del tipo Opción

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , entr en **Atributos de producto** y luego elija el enlace relacionado.
2. En la página **Atributos de producto**, seleccione un atributo de producto del tipo **Opción** al que quiere asignarle un valor y, a continuación, seleccione la acción **Valores de atributo de producto**.
3. En la página **Valores de atributo de producto**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="assign-item-attributes-to-items"></a><a name="assign-item-attributes-to-items"></a><a name="assign-item-attributes-to-items"></a>Asignar un atributo de producto a productos

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. En la página **Producto**, seleccione el producto al que quiere asignarle un atributo de producto y, a continuación, seleccione la acción **Atributos**.
3. En la página **Valores de atributo de producto**, seleccione la acción **Nuevo**.
4. Seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto existente. De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo atributo de producto como se explica en [Para crear atributos de producto](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. En el campo **Valor**, introduzca el valor del atributo de producto, como por ejemplo "2010" en el atributo **Año de modelo**.
6. Para los atributos de producto del tipo **Opción**, seleccione el botón de búsqueda en el campo **Valor** y seleccione un valor de atributo de producto. De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo valor de atributo de producto como se explica en [Para crear valores de atributo de producto del tipo Opción](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Repita los pasos del 4 al 6 para todos los atributos de producto que desea asignar al producto.

## <a name="assign-item-attributes-to-item-categories"></a><a name="assign-item-attributes-to-item-categories"></a><a name="assign-item-attributes-to-item-categories"></a>Asignar un atributo de producto a una categoría

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Categorías de artículos** y luego elija el enlace relacionado.
2. En la página **Categoría de producto**, seleccione la categoría de producto al que quiere asignarle un atributo y, a continuación, seleccione la acción **Editar**.
3. En la página **Ficha de categoría de artículo**, en la ficha desplegable **Atributos**, seleccione la acción **Nuevo**.
4. Seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto existente. De forma alternativa, elija la acción **Nuevo** para crear primero un nuevo atributo de producto como se explica en [Para crear atributos de producto](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. En el campo **Valor predeterminado**, seleccione el botón de búsqueda y seleccione un valor de atributo de producto.
6. Repita los pasos 4 y 5 para todos los atributos de producto que desea asignar a la categoría.

> [!NOTE]  
> Las categorías de producto secundarias deben heredar los atributos de producto de las categorías principales. Esto está indicado en el campo **Origen de herencia** de la ficha desplegable **Atributos**. Para obtener más información, consulte [Clasificar productos](inventory-how-categorize-items.md).

## <a name="filter-by-item-attributes"></a><a name="filter-by-item-attributes"></a><a name="filter-by-item-attributes"></a>Filtrar por atributos de producto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. En la página **Producto**, seleccione la acción **Filtrar por atributo**.
3. En la página **Filtrar productos por atributo** seleccione el botón de búsqueda en el campo **Atributo** y seleccione un atributo de producto.
4. En el campo **Valor**, seleccione el botón de búsqueda y seleccione un valor de atributo de producto para filtrar los productos.

    > [!NOTE]  
    > Solo puede seleccionar los valores directamente para los atributos del producto que tienen valores fijos, como por ejemplo el Color. Para los atributos de producto que tienen valores variables, como por ejemplo el Ancho, debe especificar el valor del atributo de producto primero seleccionando una condición. Consulte el paso 5.
5. En el campo **Valor** para un atributo de producto variable, seleccione el botón de búsqueda.
6. En la página **Especificar valor de filtro**, en el campo **Condición**, haga clic en la flecha desplegable y seleccione una condición.
7. En el campo **Valor**, introduzca un valor de atributo para filtrar los productos.

    **Ejemplo**: Para filtrar los productos en que la descripción del material empieza por "azul", rellene los campos como se indica a continuación: campo **Atributo**: descripción de material; campo **Condición**: empieza por; campo **Valor**: azul.
8. Elija el botón **Aceptar**.

Los productos de la página **Productos** se filtran por los valores de atributo de productos especificados.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Clasificar productos](inventory-how-categorize-items.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
