---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: "El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 34d6e46146f3072da49cd28e4b4bf1b0f00d1369
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-picking-items-by-fefo"></a>Habilitar la realización de picking de productos por FEFO
El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.  

 Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:  

-   El artículo debe tener un número de serie/lote.  
-   En el código del seguimiento de producto del artículo de instalación, debe seleccionarse el campo **Seguimiento almacén específico NS** o el **Seguimiento almacén específico lote**.  
-   El artículo debe registrarse para inventariar con una fecha de vencimiento.  
-   En la ficha de almacén, debe estar seleccionada la casilla **Picking requerido**.  
-   En la ficha de almacén, debe seleccionar la casilla **Picking según FEFO (Primero en caducar, primero en salir)**.  
-   En la ficha de almacén, debe estar seleccionada la casilla **Ubicac. obligatoria**.  

 Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.  

> [!NOTE]  
>  Si algún artículo numerado con serie/lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.  

 Si dos productos con número de serie o lote tienen la misma fecha de caducidad, el programa selecciona aquel cuyo número de lote o de serie sea menor. Si los números de lote o de serie son iguales, entonces selecciona el producto que se registró en primer lugar.  

> [!NOTE]  
>  -   Cuando se realiza el picking de productos con números de lote/serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.  
> -   Para activar movimientos según el FEFO, en la ventana **Movimiento inventario** o en la **Hoja trabajo movimiento**, debe dejar en blanco el campo **De ubicación**.  
> -   Si se selecciona el campo **Registro caducidad requerido**, sólo los productos que no caducan se incluirán en el picking. Esto se aplica incluso si no utiliza picking según FEFO.  

## <a name="see-also"></a>Consulte también  
[Realización de picking de artículos](warehouse-pick-items.md)   
[Procedimiento: realice un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Cómo realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

