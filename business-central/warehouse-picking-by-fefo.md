---
title: Habilitar el picking por FEFO | Documentos de Microsoft
description: 'El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="enable-picking-items-by-fefo"></a>Habilitar la realización de picking de productos por FEFO
El primero que caduca es el primero en salir (FEFO en las siglas en inglés) es un método de ordenación que asegura que con los artículos más antiguos, aquéllos con las fechas de vencimiento más próxima, se hace el picking antes.  

 Esta funcionalidad sólo funciona únicamente cuando se cumplen los criterios siguientes:  

-   El artículo debe tener un número de serie/lote.  
-   En el código del seguimiento de producto del artículo, deben seleccionarse los campos **Seguim. nº serie almacén** o **Seguim. lote almacén**.  
-   El artículo debe registrarse para inventariar con una fecha de vencimiento.  
-   En la ubicación, los controles de alternancia **Picking requerido**, **Picking según FEFO (Primero en caducar, primero en salir)** y **Ubicación obligatoria** deben estar activados.  

 Cuando se cumplen todos los criterios, los artículos numeradas con serie/lote que sean susceptibles de picking se ordenan con el movimiento pendiente más antiguo los primero en todos los picking y movimientos, excepto los que utilizan el seguimiento específico de NS o de lote.  

> [!NOTE]  
> Si algún artículo numerado con serie o lote utiliza el seguimiento específico, se respetan primero y bajo ellos, se incluyen en una lista los restantes, no específicos, números de serie/lote según el FEFO.
<br /><br />
Si dos productos con número de serie o lote tienen la misma fecha de caducidad, la aplicación selecciona aquel cuyo número de lote o de serie sea menor.
<br /><br />
Cuando se realiza el picking de productos con números de lote o serie en ubicaciones configuradas para ubicación y picking directos, sólo se realiza el picking de las cantidades de ubicaciones de tipo *Picking* según FEFO.  
<br /><br />
Para activar movimientos según el FEFO, deje en blanco el campo **Desde ubicación** en la página **Movimiento de inventario** o en las páginas **Hoja trabajo movimiento**.  
<br /><br />
Si el campo **Registro caducidad requerido** está seleccionado en **Ficha cód. seguim. prod.**, solo los productos que no se caducan se incluirán en el picking y las líneas se ordenan según el principio FEFO.

## <a name="see-also"></a>Consulte también
[Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Realizar el picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
