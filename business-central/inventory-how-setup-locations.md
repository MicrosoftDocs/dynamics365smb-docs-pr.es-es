---
title: Configurar una ficha de almacén y definir las rutas de transferencia (contiene vídeo)
description: Si compra, almacena o vende productos en más de un lugar, puede configurar cada lugar como una ubicación.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 07/05/2022
ms.author: bholtorf
ms.openlocfilehash: 882c7c0506439aba55d5b1c2d0cc23bd79db9d6e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605812"
---
# <a name="set-up-locations"></a>Configurar ubicaciones

Las ubicaciones son lugares como almacenes donde compra, almacena o vende artículos. [!INCLUDE [prod_short](includes/prod_short.md)] utiliza ubicaciones para ayudar a realizar un seguimiento del inventario tanto en los casos simples como en los procesos de almacén complejos.

Así podrá crear las líneas de documento para un almacén específico, consultar la disponibilidad por almacén y transferir inventario entre almacenes. Para obtener más información, vea [Administrar inventario](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Fichas de almacén

Debe especificar la información sobre ubicaciones, como un almacén o un centro de distribución, en la **Tarjeta de almacén**. Proporcione un nombre y un código que represente a cada almacén. A continuación, puede introducir el código de almacén en otras partes del sistema cuando desee registrar transacciones de un almacén determinado.  

Puede introducir información sobre ubicaciones y políticas de almacén para cada almacén. Según las directivas de su almacén, puede utilizar las opciones de la ficha desplegable **Ubicaciones** para especificar las ubicaciones que se utilizarán de forma predeterminada para las transacciones. Si utiliza almacenamiento y selección directos, las opciones de la ficha desplegable **Directivas ubicación** le permiten definir cómo utilizar las diversas funcionalidades ampliadas de almacén.  

Algunos campos de opción dependen de la configuración de la página **Tarjeta de almacén** para restringir las combinaciones de configuración no compatibles.  

Seleccione las acciones **Zonas** o **Ubicaciones** para ver información acerca de las zonas y ubicaciones que están definidas para el almacén.

### <a name="to-set-up-a-location"></a>Para configurar un almacén

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Repita los pasos 2 y 3 para cada almacén en el que desea guardar el inventario.

> [!NOTE]  
> Muchos campos de la página Tarjeta de almacén se refieren a la manipulación de productos en los procesos de entrada y salida de almacén. Estos campos no son relevantes para empresas que no requieran funcionalidades de almacén complejas. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).

Puede cambiar la configuración de una ubicación siempre que no tenga movimientos de productos.  

Si tiene varios almacenes, puede definir rutas de transferencia entre almacenes. Para obtener más información, consulte [Para crear una ruta de transferencia](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route"></a>Para crear una ruta de transferencia

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Rutas de transferencia** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
4. En la página **Ficha de almacén**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ahora puede transferir productos de inventario entre dos almacenes. Para obtener más información, vea [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Ubicaciones

Las ubicaciones representan la estructura básica del almacén y pueden sugerir dónde colocar los productos. Sus ubicaciones pueden tener contenido o ser ubicaciones flotantes sin contenido específico. 

Para utilizar la funcionalidad de ubicación en un almacén, en la página **Ficha almacén** de la ficha desplegable **Almacén**, active el botón de alternancia **Ubicac. obligatoria**. Puede diseñar el flujo de productos de la ubicación especificando códigos de ubicación en los campos para los procesos de almacén de las fichas desplegables **Ubicaciones** y **Directivas ubicación**.

> [!NOTE]
> Para poder especificar los códigos de ubicación en un almacén, deben crearlos. Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md) y [Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zonas

Si desea estructurar sus ubicaciones en zonas, puede hacerlo en la página **Zonas**. Cuando asigna una zona a las ubicaciones, [!INCLUDE [prod_short](includes/prod_short.md)] copia la información de la zona a las ubicaciones. También puede optar por configurar una zona y usar ubicaciones solas para organizar su almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Dimensiones predeterminadas para ubicaciones

Establece las dimensiones predeterminadas para una ubicación en la página **Tarjeta de ubicación** eligiendo **Dimensiones**. Posteriormente, las dimensiones predeterminadas de la ubicación se asignan a los documentos cuando elige la ubicación en una línea. Si es necesario, puede eliminar o cambiar la dimensión en la línea. En el campo **Registro de valor**, puede solicitar que las personas especifiquen dimensiones para ubicaciones específicas antes de que puedan publicar una entrada. Si desea permitir que las personas elijan solo ciertos valores de dimensión, puede especificarlos en el campo **Filtro valores permitidos**. También puede incluir valores de dimensión de ubicación en la página **Prioridades de dimensión predeterminadas** y en la página **Combinaciones de dimensiones** para combinaciones de reglas de prioridad y dimensión.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Gestionar inventario](inventory-manage-inventory.md)  
[Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md)  
[Crear ubicaciones](warehouse-how-to-create-individual-bins.md)  
[Configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
