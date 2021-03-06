---
title: 'Procedimiento: Asignar las ubicaciones predefinidas a los productos | Documentos de Microsoft'
description: Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6777f71e35792b4bb4dfb44d1267b59b90109438
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771884"
---
# <a name="assign-default-bins-to-items"></a>Asignar las ubicaciones predefinidas a los productos
Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto. Las ubicaciones genéricas se definen en la página **Contenido ubicación**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Asignar una ubicación predeterminada a un producto
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Hoja de creación de contenido de ubicación** y elija el enlace relacionado.  
2.  Rellene la información del código de ubicación y del artículo para cada ubicación que desee configurar como valor predeterminado para un artículo. Asegúrese de seleccionar el campo **Predeterminado**.  
3.  Seleccione la acción **Crear contenido ubicación**. Las ubicaciones ya están asignadas a su producto.  

> [!NOTE]  
>  Cuando se ubica un producto, si el producto no tiene asignada una ubicación genérica, se asignará aquélla en la que se ubique como genérica.  

## <a name="to-change-the-default-bin-for-an-item"></a>Para cambiar las ubicaciones predefinidas de los productos  
Puede que tenga que cambiar la asignación de la ubicación predeterminada de un artículo o que tenga que asignar una ubicación predeterminada a un artículo nuevo.    
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Contenidos ubicación** y luego elija el enlace relacionado.  
2.  En el campo **Filtro almacén**, seleccione el código de almacén correspondiente.  
3.  Busque el movimiento de contenido de ubicación actual del producto y desactive la casilla **Genérica**.  
4.  Busque la línea de contenido de la ubicación que desea que sea la nueva ubicación genérica. Seleccione la casilla de verificación **Ubicación predeterminada**.  

> [!NOTE]  
>  Cuando se ubica un producto por primera vez, si el producto no tienen asignada una ubicación genérica, el programa asignará la ubicación como ubicación genérica del producto.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]