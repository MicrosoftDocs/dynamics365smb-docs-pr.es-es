---
title: 'Procedimiento: Asignar las ubicaciones predefinidas a los productos | Documentos de Microsoft'
description: "Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 290c26639234f3379fb4f9b6790fc511e17f683e
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="assign-default-bins-to-items"></a>Asignar las ubicaciones predefinidas a los productos
Si utiliza ubicaciones en un almacén, la asignación de ubicaciones genéricas a sus productos puede facilitar el proceso de envío, recepción y movimiento de sus productos. Cuando se asigna una ubicación genérica a un producto, se sugiere esta ubicación cada vez que se inicia una transacción de este producto. Las ubicaciones genéricas se definen en la página **Contenido ubicación**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Asignar una ubicación predeterminada a un producto
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trab. creac. cont. ubic.** y elija el enlace relacionado.  
2.  Rellene la información del código de ubicación y del artículo para cada ubicación que desee configurar como valor predeterminado para un artículo. Asegúrese de seleccionar el campo **Predeterminado**.  
3.  Seleccione la acción **Crear contenido ubicación**. Las ubicaciones ya están asignadas a su producto.  

> [!NOTE]  
>  Cuando se ubica un producto, si el producto no tiene asignada una ubicación genérica, se asignará aquélla en la que se ubique como genérica.  

## <a name="to-change-the-default-bin-for-an-item"></a>Para cambiar las ubicaciones predefinidas de los productos  
Puede que tenga que cambiar la asignación de la ubicación predeterminada de un artículo o que tenga que asignar una ubicación predeterminada a un artículo nuevo.    
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contenidos ubicación** y luego elija el enlace relacionado.  
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
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

