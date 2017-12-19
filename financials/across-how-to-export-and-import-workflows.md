---
title: Exportar e importar flujos de trabajo | Documentos de Microsoft
description: Para transferir flujos de trabajo a otras bases de datos de Dynamics 365, por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a>Procedimiento: exportar e importar flujos de trabajo
Para transferir flujos de trabajo a otras bases de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.  

 Otra forma de crear rápidamente flujos de trabajo es crearlos a partir de plantillas de flujo de trabajo. Para obtener más información, consulte [Procedimiento: crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

 En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación. Para obtener más información, consulte [Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Para exportar un flujo de trabajo  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione un flujo de trabajo y, a continuación, la acción **Exportar a archivo**.  
3.  En la ventana **Exportar archivo**, elija el botón **Guardar**.  
4.  En la ventana **Exportar**, seleccione una ubicación de archivo y elija el botón **Guardar**.  

## <a name="to-import-a-workflow"></a>Para importar un flujo de trabajo  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2.  Elija la acción **Importar desde archivo**.  
3.  En la ventana **Importar**, seleccione el archivo XML que contiene el flujo de trabajo y elija el botón **Abrir** .  

> [!CAUTION]  
>  Si el código de flujo de trabajo ya existe en la base de datos, los pasos del flujo de trabajo se sobrescribirán con los pasos del flujo de trabajo importado.  

## <a name="see-also"></a>Consulte también  
 [Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md)   
 [Procedimiento: crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)   
 [Procedimiento: Ver las instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)   
 [Procedimiento: Eliminar flujos de trabajo](across-how-to-delete-workflows.md)   
 [Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Configuración de flujos de trabajo](across-set-up-workflows.md)   
 [Uso de flujos de trabajo](across-use-workflows.md)   
 [Flujo de trabajo](across-workflow.md)   

