---
title: Procedimiento para crear flujos de trabajo a partir de plantillas de flujo de trabajo | Documentos de Microsoft
description: Para ahorrar el tiempo al crear nuevos flujos de trabajo, puede crear flujos de trabajo a partir de plantillas de flujo de trabajo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6376c38e2580881a6d3fbb7ffd7661302a448c1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384529"
---
# <a name="create-workflows-from-workflow-templates"></a>Crear flujos de trabajo a partir de plantillas de flujo de trabajo
Para ahorrar el tiempo al crear nuevos flujos de trabajo, puede crear flujos de trabajo a partir de plantillas de flujo de trabajo.  

 Las plantillas de flujo de trabajo son flujos de trabajo no editables que existen en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)]. Los códigos para las plantillas de flujo de trabajo añadidas por Microsoft llevan el prefijo “MS-“.  

 Otra manera de crear rápidamente un flujo de trabajo es importar un flujo de trabajo existente que tenga en un archivo fuera de [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Exportación e importación de flujos de trabajo](across-how-to-export-and-import-workflows.md).  

En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Para crear un flujo de trabajo a partir de una plantilla de flujo de trabajo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Crear flujo de trabajo desde una plantilla**. Se abre la página **Plantillas de flujo de trabajo**.  
3.  Seleccione una plantilla de flujo de trabajo y haga clic en el botón **Aceptar**.  

     La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplia, por ejemplo, con “-01” para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo.  
4.  Empiece a crear el flujo de trabajo modificando los pasos del flujo de trabajo o agregando nuevos pasos. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Consulte también  
 [Crear flujos de trabajo](across-how-to-create-workflows.md)   
 [Importar y exportar flujos de trabajo](across-how-to-export-and-import-workflows.md)   
 [Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)   
 [Eliminar flujos de trabajo](across-how-to-delete-workflows.md)   
 [Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Configuración de flujos de trabajo](across-set-up-workflows.md)   
 [Uso de flujos de trabajo](across-use-workflows.md)   
 [Flujo de trabajo](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]