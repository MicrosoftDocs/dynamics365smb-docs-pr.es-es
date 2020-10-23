---
title: Configurar lugares para utilizar las ubicaciones | Documentos de Microsoft
description: Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos. Cuando haya creado sus ubicaciones, puede definir muy específicamente el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 772463e291403bac66ea08089f993909616f1b76
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920302"
---
# <a name="set-up-locations-to-use-bins"></a>Configurar almacenes para utilizar las ubicaciones
Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos. Cuando haya creado sus ubicaciones, puede definir muy específicamente el contenido que desea que lleve a cada ubicación o la ubicación puede funcionar como una ubicación aleatoria sin contenido específico.  

Para utilizar la funcionalidad de ubicación en un almacén, primero debe activar la funcionalidad en la ficha de **Almacén**. A continuación podrá diseñar el flujo del artículo en la ubicación especificando los códigos de ubicación en los campos de instalación que representan a los distintos flujos.  

> [!NOTE]  
>  Para poder especificar los códigos de ubicación en la ficha de almacén, deben crearse. Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a>Configurar una situación para utilizar las ubicaciones  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Almacenes** y, a continuación, elija el enlace relacionado.  
2.  Seleccione la situación donde desea utilizar las ubicaciones.  
3.  Seleccione la acción **Editar**.  
4.  En la ficha desplegable **Almacén**, elija la casilla **Obligatorio ubicación**.  
5.  Si no utiliza ubicación y picking directos para el almacén, rellene el campo **Selección ubic. por defecto** con el método que el sistema debe utilizar al asignar una ubicación genérica a un producto.  
6.  Abra la tarjeta de ubicación para la que desea configurar las ubicaciones.
7.  En la ficha desplegable **Ubicaciones**, seleccione las ubicaciones que desea utilizar como ubicaciones predeterminadas para las ubicaciones de recepción, envío, entrada, salida y producción de planta abierta.  
8.  Los códigos de ubicación que rellene aparecerán automáticamente en las cabeceras y en las líneas de varios documentos de almacén. Las ubicaciones genéricas definen todos los lugares de inicio y fin de productos del almacén.  
9.  Si utiliza ubicación y picking directos, seleccione una ubicación para los ajustes de almacén. El código de ubicación en el campo de **Cód. ubicación ajuste** define la ubicación virtual en el que registrar las diferencias en el inventario cuando se registran u diferencias observadas registradas en el diario del artículo de almacén, o las calculadas cuando se registra un inventario físico de almacén.  
10. Rellene los campos de la ficha desplegable **Políticas ubic.** si son importantes en el almacén. Los campos más importantes son **Política capacidad ubicación**, **Permite división bulto** y **Cód. plantilla ubicar**.  
11. En la ficha desplegable **Almacén**, rellene los campos **Tiempo manip. alm. salida**, **Tiempo manip. alm. entrada** y **Código calendario base**. Para obtener más información, vea [Configurar calendarios base](across-how-to-assign-base-calendars.md).

## <a name="filling-the-consumption-bin"></a>Rellenando la ubicación del consumo
Este organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la ubicación.

![Diagrama de flujo de ubicación](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Consulte también
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
