---
title: Cómo utilizar las familias de producto de fabricación | Documentos de Microsoft
description: La tarea principal en la personalización de un calendario base para su empresa, o uno de sus socios comerciales, es cambiar el estado de los días laborables y días no laborables.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 483d78fcbb21cdfac8811c2bed06f591936577a9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313017"
---
# <a name="work-with-production-families"></a>Trabajar con familias de producción
Una familia es un grupo de productos individuales cuya relación se basa en la similitud de sus procesos de fabricación. Mediante la formación de familias, algunos productos se pueden fabricar dos o más veces en un mismo proceso productivo, lo que optimizará el consumo de material.

En el campo **Cantidad**, en la página **Familia**, introduzca la cantidad que se fabricará cuando se haya fabricado una vez toda la familia.

## <a name="example"></a>Ejemplo
En los procesos de troquelado, se pueden fabricar cuatro piezas de un producto desde una plancha y 10 piezas más de otro producto distinto al mismo tiempo. La troqueladora fabricará 14 piezas al mismo tiempo.

La formación de familias de productos reduce la cantidad de rechazo que normalmente serían rechazadas como sobrantes al fabricar grandes piezas, que se utilizarán para fabricar productos pequeños.

## <a name="to-set-up-a-production-family"></a>Para configurar una familia de producción
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Familias** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Para producir basándose en una familily producción
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer") escriba **O.P. Planificadas en firme** y luego elija el enlace relacionado.
2. Crear una nueva orden de producción. Para obtener más información, consulte [Crear órdenes de producción](production-how-to-create-production-orders.md).
3. En el campo **Tipo de origen**, seleccione **Familia**.  
4. En el campo **Nº de origen**, seleccione la familia de producción correspondiente.

## <a name="see-also"></a>Consulte también
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Planificación](production-planning.md)   
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
