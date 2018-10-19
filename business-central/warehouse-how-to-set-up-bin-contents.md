---
title: "Crear contenidos de ubicación | Documentos de Microsoft"
description: "Después de configurar las ubicaciones, puede configurar el contenido. Es decir, puede configurar los productos que desea almacenar en una ubicación determinada y definir las reglas que rigen la cumplimentación de la ubicación con un producto particular."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b92e6a5227fc2e1c60498ef2aafaae55deaedab8
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-bin-contents"></a>Crear contenido de ubicación
Después de configurar las ubicaciones, puede configurar el contenido. Es decir, puede configurar los productos que desea almacenar en una ubicación determinada y definir las reglas que rigen la cumplimentación de la ubicación con un producto particular. Puede hacerlo manualmente en la ventana **Contenidos de ubicación** o automáticamente con la ventana **Crear hoja de contenido de ubicación**.

## <a name="to-create-bin-content-manually"></a>Para crear el contenido de ubicación manualmente  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Ubicaciones** y luego elija el enlace relacionado.  
2.  Seleccione la ubicación en la que desee configurar contenidos de ubicación y elija la acción **Ubicaciones**.  
3.  Seleccione la ubicación en la que desee configurar contenidos y elija la acción **Contenidos**.  
4.  Para cada producto que desee almacenar en la ubicación, rellene una línea en la ventana **Contenidos ubicación** con la información adecuada. Algunos campos se rellenan con información de la ubicación.  
5.  Primero rellene el campo **Nº producto** y, a continuación, si utiliza ubicación y picking directos, rellene otros campos como **Cód. unidad medida**, **Cantidad máx.** y **Cantidad mín.**  

Seleccione el campo **Fijo** si es necesario. Si la ubicación se va a utilizar como la ubicación genérica para el producto, seleccione el campo **Ubicación genérica**.  

Si utiliza ubicación y picking directos y ha introducido la información de dimensiones correcta en la ficha de producto acerca de la unidad de medida de cada producto, la cantidad máxima que ha introducido en la ventana **Contenidos ubicación** se contrastará con las capacidades físicas de la ubicación. Se utilizarán las cantidades máxima y mínima al calcular las reposiciones de cada ubicación y se sugerirán ubicaciones.  

Si selecciona el campo **Fijo**, define la ubicación fija del producto, lo que significa que [!INCLUDE[d365fin](includes/d365fin_md.md)] intentará colocar este producto en la ubicación si tiene espacio para el mismo y mantendrá el registro fijo del producto incluso cuando la cantidad en la ubicación sea 0. Se pueden colocar otros productos en la ubicación, aunque se haya fijado un producto determinado a la ubicación.  

> [!NOTE]  
>  Puede configurar varios contenidos de ubicación simultáneamente en la **Hoja trab. creac. cont. ubic.**  

## <a name="to-create-bin-content-with-a-worksheet"></a>Para crear el contenido de una ubicación con una hoja de trabajo  
Cuando haya creado sus ubicaciones, puede crear el contenido de la ubicación que desea para cada ubicación en la hoja de trabajo de creación de contenido de hoja de trabajo.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trab. creac. cont. ubic.** y luego elija el enlace relacionado.  
2.  En la cabecera de la hoja de trabajo, haga clic en el campo **Nombre** y seleccione la hoja de trabajo de la ubicación donde desea crear el contenido de ubicación.  
3.  En el campo **Ubicación**, seleccione el código de la ubicación para la que desea definir el contenido.   

    Si utiliza ubicación y picking directos en este almacén, se rellenarán automáticamente los campos relacionados con esa ubicación determinada, como **Tipo ubicación**, **Cód. clase almacén** y **Ranking ubicación**. Es información que necesita tener en cuenta al definir el contenido de la ubicación.  
4.  Seleccione el producto que desea asignar a la ubicación y rellene los campos relacionados con el contenido de la ubicación. Si utiliza ubicación y picking directos y desea utilizar el proceso **Calcular reposición ubicación**, rellene los campos **Cantidad máx.** y **Cantidad mín.**  

    Para configurar esta ubicación como preferente para el producto aún cuando la cantidad sea **0** (lo mismo para el resto de los criterios de ubicación), active el campo **Fijo**.  
5.  Repita los pasos 3 a 4 para cada producto al que desee asignar una ubicación.  
6.  Elija la acción **Imprimir** para ver e imprimir el contenido de la ubicación que ha introducido en la hoja de trabajo. Continúe revisando el contenido de la ubicación hasta que la considere correcta.  
7.  Cuando esté preparado, elija la acción **Crear contenido ubicación**.  

En esta hoja puede trabajar con varias líneas de contenido de ubicación para varias ubicaciones y así obtener una buena panorámica de los que coloca en varias ubicaciones de una zona, pasillo o estantería.  

## <a name="see-also"></a>Consulte también
[Calcular reposición ubicación](warehouse-how-to-calculate-bin-replenishment.md)    
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

