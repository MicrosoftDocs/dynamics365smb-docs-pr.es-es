---
title: Organizar los productos en categorías | Documentos de Microsoft
description: Como ayuda para buscar y encontrar productos, puede asignar atributos de producto y organizar los productos en categorías.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/22/2020
ms.author: sgroespe
ms.openlocfilehash: 206a7bcfe9152102dffbb9b2653c273dc8a27cdd
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528568"
---
# <a name="categorize-items"></a>Clasificar productos

Para mantener una visión general de sus productos y ayudarle a ordenar y encontrar los productos, es muy útil organizar los productos en categorías.

Para buscar productos por características, puede asignar los atributos de producto a los productos y también a las categorías. Para obtener más información sobre cómo trabajar con el formulario, consulte [Trabajar con atributos de producto](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Para crear una categoría de producto
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Categorías de producto** y luego elija el enlace relacionado.
2. En la página **Categorías producto**, seleccione la acción **Nuevo**.
3. En la ficha desplegable **General** de la página **Ficha de categoría de producto**, complete los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En la ficha desplegable **Atributos**, especifique atributos de producto a la categoría. Para obtener más información, consulte la sección [Para asignar un atributo de producto a una categoría](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Si la categoría del producto tiene una categoría principal, como se indica en el campo **Categoría principal**, todos los atributos que se asignen a esa categoría principal se rellenan previamente en la ficha desplegable **Atributos**.

> [!NOTE]  
> Los atributos de producto que asigna a una categoría se aplicarán automáticamente al producto al que se le ha asignado la categoría.

## <a name="to-assign-an-item-category-to-an-item"></a>Para asignar una categoría de producto a un producto

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha del producto al que desee asignar una categoría de producto.
3. Elija el botón de búsqueda en el campo **Cód. categoría producto** y seleccione una categoría existente. De forma alternativa, elija la acción **Nuevo** para crear primero una nueva categoría de producto como se explica en [Para crear una categoría de producto](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Categorías, atributos y desviaciones

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Consulte también

[Trabajar con atributos de producto](inventory-how-work-item-attributes.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
