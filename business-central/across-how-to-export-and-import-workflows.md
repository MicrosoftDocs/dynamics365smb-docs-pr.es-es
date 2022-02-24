---
title: Exportar e importar flujos de trabajo | Documentos de Microsoft
description: Para transferir flujos de trabajo a otras bases de datos de Business Central, por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2d309940d177491ce24f49884f388a5c233147fa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188281"
---
# <a name="export-and-import-workflows"></a>Importar y exportar flujos de trabajo
Para transferir flujos de trabajo a otras bases de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.  

 Otra forma de crear rápidamente flujos de trabajo es crearlos a partir de plantillas de flujo de trabajo. Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

 En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación. Para obtener más información, consulte [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Para exportar un flujo de trabajo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2.  Seleccione un flujo de trabajo y, a continuación, la acción **Exportar a archivo**.  
3.  En la página **Exportar archivo**, elija el botón **Guardar**.  
4.  En la página **Exportar**, seleccione una ubicación de archivo y elija el botón **Guardar**.  

## <a name="to-import-a-workflow"></a>Para importar un flujo de trabajo  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2.  Elija la acción **Importar desde archivo**.  
3.  En la página **Importar**, seleccione el archivo XML que contiene el flujo de trabajo y elija el botón **Abrir**.  

> [!CAUTION]  
>  Si el código de flujo de trabajo ya existe en la base de datos, los pasos del flujo de trabajo se sobrescribirán con los pasos del flujo de trabajo importado.  

## <a name="see-also"></a>Consulte también  
 [Crear flujos de trabajo](across-how-to-create-workflows.md)   
 [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)   
 [Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)   
 [Eliminar flujos de trabajo](across-how-to-delete-workflows.md)   
 [Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Configuración de flujos de trabajo](across-set-up-workflows.md)   
 [Uso de flujos de trabajo](across-use-workflows.md)   
 [Flujo de trabajo](across-workflow.md)   
