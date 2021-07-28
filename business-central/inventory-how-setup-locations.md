---
title: Configurar una ficha de almacén y definir las rutas de transferencia
description: Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: d22bbea911bed7e1ea3c756e0861111a26b5df0a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435577"
---
# <a name="set-up-locations"></a>Configurar ubicaciones

Si compra, almacena o vende productos en más de un sitio o almacén, debe configurar cada ubicación con una ficha de almacén y definir las rutas de transferencia. [!INCLUDE [prod_short](includes/prod_short.md)] utiliza ubicaciones para ayudar a realizar un seguimiento del inventario tanto en los casos más simples como en los procesos de almacén más complejos.

Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes. Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Fichas de almacén

La ficha de almacén especifica información sobre una ubicación, como un almacén o un centro de distribución. Proporcione un nombre y un código que represente a cada almacén. A continuación, puede introducir el código de almacén en otras partes del sistema cuando desee registrar transacciones de un almacén determinado.  

Puede introducir información sobre ubicaciones y políticas de almacén para cada almacén. Basándose en las políticas de almacén que seleccione, puede utilizar las opciones de la ficha desplegable **Ubic**. para definir las ubicaciones que se utilizarán como genéricas al realizar transacciones. Si utiliza ubicación y picking directos, puede usar la mayoría de las opciones de la ficha desplegable **Políticas ubic.** para definir cómo desea utilizar las diversas funcionalidades ampliadas de almacén.  

Algunos campos de opción están grises y deshabilitados por otras opciones en la página **Ficha almacén** para restringir las combinaciones de configuración no compatibles.  

Seleccione la acción **Zonas** o **Ubicaciones** para ver información acerca de las zonas y ubicaciones que se pueden definir para el almacén.

### <a name="to-create-a-location-card"></a>Para crear una ficha de almacén

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.

> [!NOTE]  
> Muchos campos de la ficha de almacén se refieren a la manipulación de productos en los procesos de almacén de entrada y salida. Los campos no son relevantes para empresas que no requieren funcionalidades de almacén más complejas. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

Puede cambiar la configuración de una ubicación más adelante, pero no puede editar la configuración de las ubicaciones que tienen movimientos contables de productos.  

A continuación, si tiene varios almacenes, puede definir rutas de transferencia entre almacenes.  

### <a name="to-create-a-transfer-route"></a>Para crear una ruta de transferencia

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Rutas de transferencia** y luego elija el enlace relacionado.
2. Opcionalmente, desde cualquier página **Ficha almacén**, elija la acción **Rutas de transferencia**.
3. Seleccione la acción **Nuevo**.
4. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ahora puede transferir productos de inventario entre dos almacenes. Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Ubicaciones

Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos. Cuando haya creado sus ubicaciones, puede definir con precisión el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico. Las ubicaciones se utilizan principalmente en operaciones de almacén básicas y avanzadas. Si administra el inventario en una configuración más sencilla, probablemente no necesite ubicaciones.

Para utilizar la función de contenedor en una ubicación, primero active la función en la ficha **Almacén** seleccionando el campo **Ubicaciones obligatorias** en la ficha desplegable **Almacén**. A continuación podrá diseñar el flujo del artículo en la ubicación especificando los códigos de ubicación en los campos de instalación que representan a los distintos flujos.

> [!NOTE]
> Para poder especificar los códigos de ubicación en la ficha de almacén, deben crearse.

Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md) y [Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zonas

Si desea estructurar sus ubicaciones en zonas, puede hacerlo en la página **Zonas**.

[!INCLUDE [prod_short](includes/prod_short.md)] copia los campos que ha definido para una zona determinada se copian en las ubicaciones de la misma. De esta forma, puede asignar una zona a una ubicación o a una plantilla de ubicación (filtro de creación de ubicación) y otros campos se rellenarán automáticamente.

No obstante, puede configurar sólo una zona y organizar el almacén según ubicaciones independientes. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Consulte también

[Gestionar inventario](inventory-manage-inventory.md)  
[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)  
[Crear ubicaciones](warehouse-how-to-create-individual-bins.md)  
[Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]