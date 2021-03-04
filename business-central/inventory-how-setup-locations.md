---
title: Configurar una ficha de almacén y definir las rutas de transferencia | Documentos de Microsoft
description: Puede crear una ficha de almacén para cada lugar donde almacene productos de inventario, por ejemplo, un almacén o un centro de distribución, y configurar rutas para transferir los productos entre almacenes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6cdfee54927dd6e966f1fd1ac0b4e40ba9df1135
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750085"
---
# <a name="set-up-locations"></a>Configurar ubicaciones
Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia.

Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes. Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a>Para crear una ficha de almacén
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.

> [!NOTE]  
> Muchos campos de la ficha de almacén se refieren a la manipulación de productos en los procesos de almacén de entrada y salida. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Para crear una ruta de transferencia
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas de transferencia** y luego elija el enlace relacionado.
2. Opcionalmente, desde cualquier página **Ficha almacén**, elija la acción **Rutas de transferencia**.
3. Seleccione la acción **Nuevo**.
4. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ahora puede transferir productos de inventario entre dos almacenes. Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Consulte también
[Gestionar inventario](inventory-manage-inventory.md)  
[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]