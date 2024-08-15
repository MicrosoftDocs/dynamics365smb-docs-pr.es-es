---
title: Organizar los productos en categorías
description: 'Como ayuda para buscar y encontrar productos, puede asignar atributos de producto y organizar los productos en categorías.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'category, search, attribute, facet'
ms.search.form: '5730, 5733, 5401'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---

# Clasificar productos

Para mantener una visión general de sus productos y ayudarle a ordenar y encontrar los productos, es muy útil organizar los productos en categorías.

Para buscar productos por características, puede asignar los atributos de producto a los productos y también a las categorías. Para obtener más información sobre cómo trabajar con el formulario, consulte [Trabajar con atributos de producto](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## Para crear una categoría de producto
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Categorías de artículos** y luego elija el enlace relacionado.
2. En la página **Categorías producto**, seleccione la acción **Nuevo**.
3. En la ficha desplegable **General** de la página **Ficha de categoría de producto**, complete los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En la ficha desplegable **Atributos**, especifique atributos de producto a la categoría. Para obtener más información, consulte la sección [Para asignar un atributo de producto a una categoría](inventory-how-work-item-attributes.md#assign-item-attributes-to-item-categories).

> [!NOTE]  
> Si la categoría del producto tiene una categoría principal, como se indica en el campo **Categoría principal**, todos los atributos que se asignen a esa categoría principal se rellenan previamente en la ficha desplegable **Atributos**.

> [!NOTE]  
> Los atributos de producto que asigna a una categoría se aplicarán automáticamente al producto al que se le ha asignado la categoría.

Si cambia de opinión sobre una categoría de artículo, puede eliminarla. Sin embargo, si la categoría está asignada a un producto, deberá eliminar esa asignación previamente.

## Para asignar una categoría de producto a un producto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha del producto al que desee asignar una categoría de producto.
3. Elija el botón de búsqueda en el campo **Cód. categoría producto** y seleccione una categoría existente. De forma alternativa, elija la acción **Nuevo** para crear primero una nueva categoría de producto como se explica en [Para crear una categoría de producto](inventory-how-categorize-items.md#to-create-an-item-category).

## Categorías, atributos y variantes

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Consulte también .

[Trabajar con atributos de elementos](inventory-how-work-item-attributes.md)    
[Gestionar variantes de productos](inventory-item-variants.md)    
[Registrar nuevos artículos](inventory-how-register-new-items.md)    
[Grupos contables inventario](inventory-manage-inventory.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
