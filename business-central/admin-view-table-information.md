---
title: Ver información de tabla
description: Descubra cómo puede ver información sobre las tablas de bases de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776896"
---
# <a name="viewing-table-information"></a>Visualización de información de tabla

La página **8700 Información de tabla** proporciona información sobre todas las tablas de sistema y de negocios en una solución Business Central. En particular, la página muestra información sobre la cantidad de datos que contienen las tablas.

Esta información es útil para solucionar problemas de rendimiento, porque le permite ver la distribución del tamaño de los datos en las tablas.

## <a name="viewing-table-information"></a>Visualización de información de tabla

Para abrir esta página, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Información de tabla** y, a continuación, seleccione el vínculo relacionado.

La siguiente tabla describe la información proporcionada para cada tabla:

|Columna|Descripción|
|------|-----------|
|Nombre de la empresa|El nombre de la empresa, si existe, a la que pertenece la tabla.|
|Nombre tabla|El nombre de la tabla.|
|Nº tabla|El id. de la tabla|
|Nº de registros|El número total de registros almacenados en la tabla.|
|Tamaño del registro|El tamaño de registro promedio en KB/registro. El valor se calcula utilizando la siguiente fórmula: 1024 (Tamaño)/(N.º de registros). |

## <a name="see-also"></a>Consulte también

[Inspección de páginas](across-inspect-page.md)  
[Artículos de rendimiento para desarrolladores](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]