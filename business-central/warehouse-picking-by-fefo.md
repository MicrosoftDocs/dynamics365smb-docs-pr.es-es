---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1c7896988545d6f1b8269ead90dff7350bc6f320
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755836"
---
# <a name="enable-picking-items-by-fefo"></a>Habilitar la realización de picking de productos por FEFO
El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.  

 Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:  

-   El artículo debe tener un número de serie/lote.  
-   En el código del seguimiento de producto del artículo, deben seleccionarse los campos **Seguim. nº serie almacén** o **Seguim. lote almacén**.  
-   El artículo debe registrarse para inventariar con una fecha de vencimiento.  
-   En la ficha de almacén, debe estar seleccionada la casilla **Picking requerido**.  
-   En la ficha de almacén, debe seleccionar la casilla **Picking según FEFO (Primero en caducar, primero en salir)**.  
-   En la ficha de almacén, debe estar seleccionada la casilla **Ubicac. obligatoria**.  

 Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.  

> [!NOTE]  
> Si algún artículo numerado con serie/lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.
<br /><br />
Si dos productos con número de serie o lote tienen la misma fecha de caducidad, la aplicación selecciona aquel cuyo número de lote o de serie sea menor.
<br /><br />
Cuando se realiza el picking de productos con números de lote/serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.  
<br /><br />
Para activar movimientos según el FEFO, en la página **Movimiento inventario** o en la página **Hoja trabajo movimiento**, debe dejar en blanco el campo **De ubicación**.  
<br /><br />
Si se selecciona el campo **Registro caducidad requerido**, sólo los productos que no caducan se incluirán en el picking. Esto se aplica incluso si no utiliza picking según FEFO.

## <a name="see-also"></a>Consulte también  
[Realización de picking de artículos](warehouse-pick-items.md)   
[Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]