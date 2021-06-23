---
title: Informes y análisis de proyecto
description: Consulte qué informes y análisis de proyecto están disponibles en la versión estándar de Business Central para que pueda realizar un seguimiento de su negocio.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: ff5294df5cdbeaf0054249f017906bfd60ee4bf7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216400"
---
# <a name="project-reports-and-analytics-in-business-central"></a>Informes y análisis de proyecto en Business Central

Los informes de proyecto en [!INCLUDE [prod_short](includes/prod_short.md)] permite a los profesionales de los proyectos y los negocios obtener información y estadísticas sobre las actividades de proyectos actuales y pasadas.  

## <a name="reports"></a>Informes

La siguiente tabla describe algunos de los informes clave en los informes de proyectos.

|Informe |Id. de objeto|Descripción  |
|---------|---------|---------|
|**Análisis proyecto**|1008|Analiza su proyecto con las opciones que especifique. Por ejemplo, es posible crear un informe que muestre los precios presupuestados, los precios de uso y los precios facturables para luego comparar los tres conjuntos de precios.<br>Puede utilizar una combinación de campos **Importe** disponibles para crear su propio análisis. Para cada campo, seleccione una de los siguientes opciones para los precios, costes o beneficios: Programa, Uso, Contrato o Facturado. <br>Permite seleccionar si la divisa se especifica como Divisa local + o como Divisa extranjera. |
|**Líneas planificación proyecto**|1006|Este informe muestra las diferentes líneas de tareas de trabajo y planificación del proyecto, incluido el tipo de línea, las cantidades, la unidad de medida, los costes totales, etc.|
|**Proyecto real frente a presupuesto**|1009|Compara los importes programados y de consumo de los proyectos seleccionados. Las líneas de dicho proyecto mostrarán la cantidad, el coste total y el importe de la línea. <br>Este informe está pensado para proyectos terminados, si bien puede utilizarlo en cualquier momento del mismo.<br>En EE. UU., Canadá y México, este informe no está disponible. En su lugar, utilice los informes **Proyecto real frente a presupuestado (coste)** (10210) o **Proyecto real frente a presupuestado (precio)** (10211).|
|**Fact. sugerida proyecto**|1011|Muestra una lista de todos los proyectos agrupados por cliente, cuánto se le ha facturado al cliente y cuánto queda por facturar, es decir, la facturación sugerida. <br>En EE. UU., Canadá y México, este informe no está disponible. En su lugar, use informe **Facturación sugerida por coste del proyecto** (10219).|
|**Proyectos por cliente**|1012|Muestra una lista de todos los proyectos, agrupados por cliente. Permite comparar el importe de venta programado, el porcentaje de terminación, el importe de venta facturado y el porcentaje de importes facturados de cada opción **Facturar a nº cliente**.|
|**Productos por proyecto** o **Proyectos por producto**|1013 o 1014|Una descripción general de los elementos usados en un proyecto. Según el informe que desee utilizar para obtener una descripción general de los productos planificados para un proyecto, puede establecer un filtro adicional. El informe muestra los elementos relevantes y un valor acumulado sobre los costes.|
|**Detalle de la transacción del proyecto**|1007|Este informe le ofrece una descripción general de las tareas del proyecto publicadas, como recursos y productos. Incluye información detallada sobre los costes totales y los precios totales además de información sobre los descuentos de línea, etc. El informe muestra datos de los movimientos del proyecto.|
|**WIP a C/G proyecto**|1010|Muestra el valor del trabajo en curso de aquellos proyectos que usted seleccione en comparación con la cantidad que se ha registrado en el módulo de contabilidad.|




## <a name="tasks"></a>Tareas

Los siguientes artículos describen algunas de las tareas clave para analizar el estado de su empresa:

* [Supervisar el progreso y el rendimiento del trabajo](projects-how-monitor-progress-performance.md)  


## <a name="see-also"></a>Consulte también .

[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
