---
title: Crear contenido de ubicación
description: Una vez que haya configurado sus contenedores, puede especificar los productos que desea almacenar en ellos y configurar reglas que controlen la frecuencia con la que se rellenan los contenedores.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9135514b6f788aab99b3433a04ad28ec36064e30
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074359"
---
# <a name="create-bin-contents"></a>Crear contenido de ubicación

Después de configurar las ubicaciones, puede configurar el contenido. Es decir, puede configurar los productos que desea almacenar en una ubicación determinada y definir las reglas que rigen la cumplimentación de la ubicación con un producto particular. Puede hacerlo manualmente en la página **Contenidos de ubicación** o automáticamente con la página **Crear hoja de contenido de ubicación**.

## <a name="to-create-bin-content-manually"></a>Para crear el contenido de ubicación manualmente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2. Seleccione la ubicación en la que desee configurar contenidos de ubicación y elija la acción **Ubicaciones**.  
3. Seleccione la ubicación en la que desee configurar contenidos y elija la acción **Contenidos**.  
4. Para cada producto que desee almacenar en la ubicación, rellene una línea en la página **Contenidos ubicación** con la información adecuada. Algunos campos se rellenan con información de la ubicación.  
5. Primero rellene el campo **Nº producto** y, a continuación, si utiliza ubicación y picking directos, rellene otros campos como **Cód. unidad medida**, **Cantidad máx.** y **Cantidad mín.**  

Seleccione el campo **Fijo** si es necesario. Si la ubicación se va a utilizar como la ubicación genérica para el producto, seleccione el campo **Ubicación genérica**.  

Si utiliza ubicación y picking directos y ha introducido la información de dimensiones correcta en la ficha de producto acerca de la unidad de medida de cada producto, la cantidad máxima que haya introducido en la página **Contenidos de ubicación** se contrastará con las capacidades físicas de la ubicación. Se utilizarán las cantidades máxima y mínima al calcular las reposiciones de cada ubicación y se sugerirán ubicaciones.  

Si selecciona el campo **Fijo**, define la ubicación fija del producto, lo que significa que [!INCLUDE[prod_short](includes/prod_short.md)] intentará colocar este producto en la ubicación si tiene espacio para el mismo y mantendrá el registro fijo del producto incluso cuando la cantidad en la ubicación sea 0. Se pueden colocar otros productos en la ubicación, aunque se haya fijado un producto determinado a la ubicación.  

> [!NOTE]  
> Puede configurar varios contenidos de ubicación simultáneamente en la página **Hoja trab. creac. cont. ubic.**  

## <a name="to-create-bin-content-with-a-worksheet"></a>Para crear el contenido de una ubicación con una hoja de trabajo

Cuando haya creado sus ubicaciones, puede crear el contenido de la ubicación que desea para cada ubicación en la hoja de trabajo de creación de contenido de hoja de trabajo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique **Hoja trab. creac. cont. ubic.** y, a continuación, elija el vínculo relacionado.  
2. En la cabecera de la hoja de trabajo, haga clic en el campo **Nombre** y seleccione la hoja de trabajo de la ubicación donde desea crear el contenido de ubicación.  
3. En el campo **Ubicación**, seleccione el código de la ubicación para la que desea definir el contenido.  

    Si utiliza ubicación y picking directos en este almacén, se rellenarán automáticamente los campos relacionados con esa ubicación determinada, como **Tipo ubicación**, **Cód. clase almacén** y **Ranking ubicación**. Es información que necesita tener en cuenta al definir el contenido de la ubicación.  
4. Seleccione el producto que desea asignar a la ubicación y rellene los campos relacionados con el contenido de la ubicación. Si utiliza ubicación y picking directos y desea utilizar el proceso **Calcular reposición ubicación**, rellene los campos **Cantidad máx.** y **Cantidad mín.**  

    Para configurar esta ubicación como preferente para el producto aún cuando la cantidad sea **0** (lo mismo para el resto de los criterios de ubicación), active el campo **Fijo**.  
5. Repita los pasos 3 a 4 para cada producto al que desee asignar una ubicación.  
6. Elija la acción **Imprimir** para ver e imprimir el contenido de la ubicación que ha introducido en la hoja de trabajo. Continúe revisando el contenido de la ubicación hasta que la considere correcta.  
7. Cuando esté preparado, elija la acción **Crear contenido ubicación**.  

En esta hoja puede trabajar con varias líneas de contenido de ubicación para varias ubicaciones y así obtener una buena panorámica de los que coloca en varias ubicaciones de una zona, pasillo o estantería.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/set-up-zones-bins/)

## <a name="see-also"></a>Consulte también .

[Calcular reposición ubicación](warehouse-how-to-calculate-bin-replenishment.md)  
[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Detalles de diseño: Configuración de almacén](design-details-warehouse-setup.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]