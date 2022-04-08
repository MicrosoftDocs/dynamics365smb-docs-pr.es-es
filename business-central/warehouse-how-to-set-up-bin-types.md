---
title: Configurar tipos de ubicación
description: Asigne tipos y actividades de flujo básicas a ubicaciones y, al hacerlo, defina la forma en que se utilizan las ubicaciones para determinadas actividades de almacén.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 8fb409e9ca0a8540fa2ea997faae790f78086d6e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520053"
---
# <a name="set-up-bin-types"></a>Configurar tipos de ubicación
Puede dirigir el flujo de productos por las ubicaciones que ha definido para las actividades de un almacén determinado. Indique las actividades de flujo básicas para cada ubicación y defina la forma en que se utilizará la ubicación, asignándola a un tipo de ubicación.  

Existen seis tipos. Puede trabajar en el almacén con seis tipos de ubicaciones posibles, o puede trabajar con sólo los tipos de ubicaciones RECIBIR, COLOCARPICKING, ENVIAR y QC. Estos cuatro tipos permiten realizar sugerencias para admitir el flujo de productos y registrar las diferencias de existencias.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Para configurar los tipos de ubicaciones que desea utilizar  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tipos de ubicación** y luego elija el enlace relacionado.  
2.  En la página **Tipos ubicación**, cree un código d e10 caracteres para el tipo de ubicación.  
3.  Seleccione las actividades que se pueden realizar con cada tipo de ubicación.  

> [!NOTE]  
>  Los tipos de ubicación sólo son aplicables si utiliza ubicación y picking directos en el almacén.  

El tipo de ubicación sólo determina cómo se utilizará una ubicación determinada cuando procese el flujo de productos a través del almacén. Siempre puede anular las sugerencias del sistema de cualquier documento de almacén, y puede mover productos desde o hacia cualquier ubicación ejecutando un movimiento de almacén.  

A continuación, se muestran los tipos de ubicaciones que puede crear.  

|Tipo ubicación|Description|  
|------------------|---------------------------------------|  
|RECEPC|Los productos registrados como recepciones registradas, pero no ubicados.|  
|ENVIAR|Los productos de los que se ha realizado el picking de las líneas de los envíos de almacén, pero que no se han registrado como enviados.|  
|UBICAR|Normalmente, los productos se almacenan en unidades de medida grandes a las que no desea que tenga acceso para realizar el picking. Debido a que no se realiza el picking de estas ubicaciones, ya sea de órdenes de producción o envíos, el uso de una ubicación de tipo Ubicar puede estar limitado, pero este tipo de ubicación podría ser útil si ha comprado una gran cantidad de productos. Las ubicaciones de este tipo siempre deben tener un ranking de ubicación bajo, para que cuando se coloquen los productos recibidos, se ubiquen primero otras ubicaciones COLOCARPICKING de ranking más alto asignados al producto. Si utiliza este tipo de ubicación, debe realizar con regularidad la reposición de ubicación para que los productos almacenados en estas ubicaciones también estén disponibles en ubicaciones de tipo COLOCARPICKING o PICKING.|  
|PICKING|Los productos utilizados sólo para picking, por ejemplo, para los productos con una fecha de caducidad próxima que ha movido a este tipo de ubicación. En estas ubicaciones debería indicar un ranking de ubicación alto para que el sistema sugiera primero el picking de estas ubicaciones.|  
|COLOCARPICKING|Artículos en ubicaciones que se sugieren para funciones de ubicación y de picking. Probablemente, las ubicaciones de este tipo tengan distintos rankings de ubicación. Puede configurar las ubicaciones de almacenamiento masivo como de este tipo con rankings de ubicación bajos comparados con las ubicaciones de picking normales o las ubicaciones del área de picking de seguimiento.|  
|QC|Esta ubicación se utiliza para ajustes de inventario si se especifica en la ficha de almacén en el campo **Cód. ubicación ajuste**. También puede configurar ubicaciones de este tipo para productos defectuosos y productos que es preciso inspeccionar. puede mover productos a este tipo de ubicación si desea que no se tenga a consulta a los mismos desde el flujo de productos normal.<br /><br /> **NOTA**: A diferencia de resto de tipos de ubicación, el de **QC** no tiene seleccionada de forma predeterminada ninguna de las casillas de verificación de manejo de artículos. Esto indica que el contenido que sitúe en una ubicación de control de calidad no se incluye de los flujos del artículo.|  

## <a name="see-also"></a>Consulte también
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
