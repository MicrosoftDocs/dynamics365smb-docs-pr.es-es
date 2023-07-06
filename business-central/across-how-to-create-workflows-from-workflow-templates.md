---
title: Crear flujos de trabajo a partir de plantillas de flujo de trabajo
description: 'Para ahorrar tiempo al crear nuevos flujos de trabajo de aprobación, puede crear flujos de trabajo no editables a partir de plantillas de flujo de trabajo con el prefijo "MS".'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="create-workflows-from-workflow-templates"></a><a name="create-workflows-from-workflow-templates"></a><a name="create-workflows-from-workflow-templates"></a><a name="create-workflows-from-workflow-templates"></a>Crear flujos de trabajo a partir de plantillas de flujo de trabajo

Para ahorrar el tiempo al crear nuevos flujos de trabajo de aprobación, puede usar plantillas de flujo de trabajo.  

Las plantillas de flujo de trabajo son flujos de trabajo no editables que existen en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)]. Los códigos para las plantillas de flujo de trabajo creadas por Microsoft llevan el prefijo "MS-".  

Otra manera de crear rápidamente un flujo de trabajo es importar un flujo de trabajo existente que tenga en un archivo fuera de [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Exportar e importar flujos de trabajo](across-how-to-export-and-import-workflows.md).  

En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a><a name="to-create-a-workflow-from-a-workflow-template"></a><a name="to-create-a-workflow-from-a-workflow-template"></a><a name="to-create-a-workflow-from-a-workflow-template"></a>Para crear un flujo de trabajo a partir de una plantilla de flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo flujo de trabajo desde plantilla**. Se abre la página **Plantillas de flujo de trabajo**.  
3. Seleccione una plantilla de flujo de trabajo y, a continuación, elija **Aceptar**.  

   La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplía, por ejemplo, con "-01" para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo.  
4. Empiece a crear el flujo de trabajo modificando los pasos del flujo de trabajo o agregando nuevos pasos. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-workflows/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Importar y exportar flujos de trabajo de aprobación](across-how-to-export-and-import-workflows.md)  
[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminar flujos de trabajo de aprobación](across-how-to-delete-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Flujo de trabajo](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
