---
title: Exportar e importar flujos de trabajo de aprobación
description: 'Para transferir flujos de trabajo a otras bases de datos de Business Central, por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="export-and-import-approval-workflows"></a><a name="export-and-import-approval-workflows"></a><a name="export-and-import-approval-workflows"></a><a name="export-and-import-approval-workflows"></a>Importar y exportar flujos de trabajo de aprobación

Para transferir flujos de trabajo a otras bases de datos de [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, para ahorrar tiempo al crear nuevos flujos de trabajo, puede exportar e importar flujos de trabajo.  

Otra forma de crear rápidamente flujos de trabajo es usar plantillas de flujo de trabajo. Obtenga más información en [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo usando listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a><a name="export-a-workflow"></a><a name="export-a-workflow"></a><a name="export-a-workflow"></a>Exportar un flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione un flujo de trabajo y, a continuación, la acción **Exportar a archivo**.  

## <a name="import-a-workflow"></a><a name="import-a-workflow"></a><a name="import-a-workflow"></a><a name="import-a-workflow"></a>Importar un flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Elija la acción **Importar desde archivo**.  
3. En la página **Importar**, seleccione **Elegir**, elija el archivo XML que contiene el flujo de trabajo y, a continuación, seleccione **Abrir**.  

> [!CAUTION]  
> Si el código de flujo de trabajo ya existe en la base de datos, los pasos del flujo de trabajo se sobrescribirán con los pasos del flujo de trabajo importado.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)  
[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminar flujos de trabajo de aprobación](across-how-to-delete-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
