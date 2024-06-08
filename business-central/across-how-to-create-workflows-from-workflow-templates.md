---
title: Crear flujos de trabajo a partir de plantillas de flujo de trabajo
description: 'Para ahorrar el tiempo al crear nuevos flujos de trabajo de aprobación, puede crear flujos de trabajo a partir de plantillas de flujo de trabajo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-workflows-from-workflow-templates"></a>Crear flujos de trabajo a partir de plantillas de flujo de trabajo

En la página **Flujo de trabajo** puede crear un flujo de trabajo creando una serie de pasos de flujo de trabajo en las líneas. Cada paso consta de un evento del flujo de trabajo (evento Cuando), moderado por condiciones de evento (Condición On) y una respuesta de flujo de trabajo (Respuesta Entonces), moderada por las opciones de respuesta. Los campos de las líneas de flujo de trabajo proporcionan listas fijas de valores de eventos y respuestas que representan los escenarios que [!INCLUDE [prod_short](includes/prod_short.md)] admite. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).

Para ahorrarle tiempo a la hora de crear flujos de trabajo de aprobación, [!INCLUDE [prod_short](includes/prod_short.md)] proporciona plantillas de flujo de trabajo. Las plantillas están disponibles en la página **Plantillas de flujo de trabajo**. Puede utilizar las plantillas tal como están o personalizarlas para satisfacer sus necesidades. Los códigos para las plantillas de flujo de trabajo de Microsoft llevan el prefijo **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Si cambia una plantilla de flujo de trabajo, pero luego se arrepiente del cambio, use la acción **Restablecer plantillas de Microsoft** para volver a la configuración original del flujo de trabajo.

> [!CAUTION]
> La acción **Restablecer plantillas de Microsoft** restablece todas las plantillas de flujo de trabajo de Microsoft. No puede restablecer una sola plantilla.  

Otra forma de crear rápidamente un flujo de trabajo es importarlo, por ejemplo, si lo exportó desde otra instancia de [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Exportar e importar flujos de trabajo](across-how-to-export-and-import-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Para crear un flujo de trabajo a partir de una plantilla de flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo flujo de trabajo desde plantilla**. Se abre la página **Plantillas de flujo de trabajo**.  
3. Seleccione una plantilla de flujo de trabajo y, a continuación, elija **Aceptar**.  

   La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplía, por ejemplo, con "-01" para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo.  
4. Para personalizar el flujo de trabajo, edite los pasos del flujo de trabajo o agregue nuevos pasos. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Consulte también

[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Importar y exportar flujos de trabajo de aprobación](across-how-to-export-and-import-workflows.md)  
[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminar flujos de trabajo de aprobación](across-how-to-delete-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Flujo de trabajo](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
