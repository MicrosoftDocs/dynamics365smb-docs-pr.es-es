---
title: Cómo configurar plantillas de ubicación | Documentos de Microsoft
description: Con la funcionalidad de ubicación y picking directo, se sugiere la ubicación más adecuada para los productos en un momento determinado, según la plantilla de ubicación que ha configurado para el almacén, los rankings que ha dado a las ubicaciones y las cantidades máxima y mínima que ha definido para las ubicaciones fijas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2c8cd73e1dd47549cab57e9fd44fe52232437175
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925302"
---
# <a name="set-up-put-away-templates"></a>Configurar plantillas de ubicación

Con la funcionalidad de ubicación y picking directo, se sugiere la ubicación más adecuada para los productos en un momento determinado, según la plantilla de ubicación que ha configurado para el almacén, los rankings que ha dado a las ubicaciones y las cantidades máxima y mínima que ha definido para las ubicaciones fijas.  

Puede configurar varias plantillas de ubicación y seleccionar una para controlar las ubicaciones en general en el almacén. También puede seleccionar una plantilla de ubicación para cualquier producto o unidad de almacenamiento que tenga unos requisitos de ubicación especiales.  

## <a name="to-set-up-put-away-templates"></a>Para configurar las plantillas de ubicación

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plantillas de ubicación** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Escriba un código que sea el identificador exclusivo de la plantilla que va a crear.  
4. Escriba una breve descripción, si lo desea.  
5. Rellene la primera línea con los requisitos de la ubicación que desea que se rellenen en primer lugar cuando se sugiera una ubicación.

    Por ejemplo, si desea que el método de almacenamiento predeterminado se base en ubicaciones fijas, elija el campo **Buscar ubicación fija**. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Rellene la segunda línea con los requisitos de ubicación que serán la segunda opción a seguir para utilizar esta ubicación. El programa sólo se utilizará si no encuentra una ubicación que cumpla los requisitos de la primera línea.  
7. Continúe rellenando las líneas hasta que haya descrito todos los lugares de ubicación adecuados que desea utilizar en el proceso de ubicación.  
8. En la última línea de la plantilla de ubicación, seleccione la casilla **Busca ubicación aleatoria**.  

Puede crear varias plantillas de ubicación y, a continuación, aplicarlas como necesite. Se utilizará primero la plantilla de ubicación que ha seleccionado para el producto o unidad de almacenamiento, si existe. Si estos campos no están rellenos, se utilizará la plantilla que ha seleccionado para el almacén en la ficha desplegable **Políticas ubic.** de la ficha de almacén.  

## <a name="see-also"></a>Consulte también

[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
