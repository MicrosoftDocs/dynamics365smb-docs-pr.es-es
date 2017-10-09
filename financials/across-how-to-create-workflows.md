---
title: Crear flujos de trabajo | Documentos de Microsoft
description: "Puede crear flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a057da05d6b63ee60e29de70900ffae917d0fee3
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows"></a>Procedimiento: Crear flujos de trabajo
Puede crear flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo moderado por condiciones de evento y una respuesta de flujo de trabajo con opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

Al crear flujos de trabajo, puede copiar los pasos de flujos de trabajo existentes o de plantillas de flujo de trabajo. Las plantillas de flujo de trabajo representan flujos de trabajo no editables que existen en la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)]. El código de las plantillas de flujo de trabajo agregados por Microsoft se prefija con “MS-“, como “MS-PIW”. Para obtener más información, consulte [Procedimiento: crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

Si su escenario empresarial necesita eventos de flujo de trabajo o respuestas que no se admiten, un asociado de Microsoft debe implementarlos personalizando el código de aplicación.  
  
> [!NOTE]  
>  Todas las notificaciones sobre pasos de flujo de trabajo se envían a través de una cola de proyectos. Asegúrese de que la cola de proyectos en la instalación está configurada para gestionar las notificaciones de flujo de trabajo, así como que la casilla **Iniciar automáticamente desde NAS** esté seleccionada. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Para crear un flujo de trabajo  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la ventana **Flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. Para crear el flujo de trabajo desde una plantilla, en la ventana **Flujos de trabajo**, seleccione la acción **Crear flujo de trabajo desde plantilla**. Para obtener más información, consulte [Procedimiento: crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  
5. En el campo **Descripción**, describa el flujo de trabajo.  
6. En el campo **Categoría**, especifique a qué categoría pertenece el flujo de trabajo.  
7. En el campo **Evento Cuando**, especifique el evento que debe producirse para iniciar el paso del flujo de trabajo.  

    Cuando elige el campo, la ventana **Eventos de flujo de trabajo** se abre, donde puede seleccionar de todos los eventos de flujo de trabajo existentes.  
8. En el campo **Condición**, especifique una o varias condiciones que se deben cumplir para que se produzca el evento en el campo **Evento Cuando**.  

    Cuando elige el campo se abre la ventana **Condiciones de evento**, donde se elige entre una lista de campos de filtro pertinentes relevantes como condiciones del evento en cuestión. Puede agregar los campos de filtro nuevos que desee utilizar como condiciones del evento. Puede definir filtros de condición de evento igual que define filtros en las páginas de solicitud de informe.  

    Si el evento del flujo de trabajo es el cambio de un campo determinado en un registro, la ventana **Condiciones del evento** se abre con las opciones para seleccionar el campo y el tipo de cambio.  

    1.  Para especificar un cambio de campo para el evento, en la ventana **Condiciones del evento**, en el campo **Campo**, seleccione el campo que cambia.  
    2.  En el campo **Operador**, seleccione **Disminuyó**, **Aumentó** o **Cambió**.  
9. Especifique la respuesta que seguirá cuando se produzca el evento del flujo de trabajo en el campo **Respuesta Entonces**.  

     Cuando elija el campo, la ventana **Respuestas de flujo de trabajo** se abre, donde puede seleccionar de todas las respuestas de flujo de trabajo que existen y fijar opciones de respuesta para la respuesta seleccionada.  
10. En la ficha desplegable **Opciones para la respuesta seleccionada**, especifique las opciones para la respuesta de flujo de trabajo seleccionando los valores en los campos que aparecen, como se indica a continuación:  

    1.  Para especificar las opciones para una respuesta de flujo de trabajo que implica enviar una notificación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Id. de usuario destinatario**|Especifique el usuario al que se debe enviar la notificación. Nota: Esta opción solo está disponible para respuestas de flujo de trabajo con un marcador para un usuario específico. Para las respuestas de flujo de trabajo sin marcadores para usuarios, el usuario de aprobación define normalmente la configuración del destinatario de la notificación.|  
        |**Página de destino de vínculo**|Especifique otra página en [!INCLUDE[d365fin](includes/d365fin_md.md)] que el vínculo de la notificación abrirá en lugar de la página predeterminada.|  
        |**Personalizar vínculo**|Especifique la dirección URL de un vínculo que se agrega a la notificación además del vínculo a la página en [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Para especificar opciones para una respuesta de flujo de trabajo que implica crear una solicitud de aprobación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Fórmula fecha vencimiento**|Especifique la cantidad de días en que se debe completar la solicitud de aprobación desde la fecha en que se ha enviado.|  
        |**Delegar tras**|Especifica si y cuándo se delegará automáticamente una solicitud de aprobación al sustituto correspondiente. Puede seleccionar delegar automáticamente un día, dos o cinco después de la fecha en que se solicitó la aprobación.|  
        |**Tipo de aprobador**|Especifique quién es el aprobador según la configuración de usuarios de aprobación y usuarios de flujo de trabajo.<br /><br /> Las siguientes opciones están disponibles:<br /><br /> -   **Vendedor/Comprador** especifica que el usuario configurado en el campo **Cód. vendedor/comprador** en la ventana **Config. usuario aprobación** determina quién es el aprobador. Los movimientos de solicitud de aprobación se crean según el valor del campo **Tipo de límite de aprobador**.<br />     Para obtener más información, vea [Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-workflow-users.md).|  
        |**Mostrar mensaje de confirmación**|Especifica si un mensaje de confirmación se muestra los usuarios después de que hayan solicitado una aprobación.|  
        |**Tipo de límite de aprobador**|Especifique cómo afectan los límites de aprobación de los aprobadores cuando se crean movimientos de solicitud de aprobación para ellos. Un aprobador calificado es aquel cuyo límite de aprobación es superior al valor de la solicitud que se está realizando.<br /><br /> Las siguientes opciones están disponibles:<br /><br /> 1.  **Cadena de aprobadores** especifica que los movimientos de solicitud de aprobación se crean para todos los aprobadores del solicitante hasta el primer aprobador cualificado, incluido este.<br />2.  **Aprobador directo** especifica que un movimiento de solicitud de aprobación solo se crea para el aprobador inmediato del solicitante, sea cual sea el límite de aprobación del aprobador.<br />3.  **Primer aprobador cualificado** especifica que solo se crea un movimiento de solicitud de aprobación para el primer aprobador cualificado del solicitante.<br />|  
    3.  Para especificar las opciones para una respuesta de flujo de trabajo que implica crear líneas de diario, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Nombre plantilla diario general**|Especifique el nombre de la plantilla de libro de diario general en las que se crearán las líneas de diario especificadas.|  
        |**Nombre sección diario general**|Especifique el nombre del proceso de diario general en las que se crearán las líneas de diario especificadas.|  

11. Seleccione los botones **Aumentar sangría** y **Disminuir sangría** para sangrar el nombre del evento en el campo **Cuando** para definir la posición del paso de flujo de trabajo.  
    1.  Indique que el paso es el siguiente de la secuencia del flujo de trabajo aplicando sangría en el nombre del evento del evento del paso anterior.  
    2.  Indique que el paso es uno de más pasos alternativos que pueden iniciarse en función de la condición colocando el nombre del evento en el mismo sangrado que los otros pasos alternativos. Ordene estos pasos opcionales según la prioridad colocando el paso más importante primero.  

    > [!NOTE]  
    >  Puede cambiar solo la sangría de un paso que no tenga un paso subsiguiente.  

12. Repita los pasos del 7 al 11 para añadir más pasos de flujo de trabajo antes o después del paso que acaba de crear.  
13. Seleccione la casilla **Habilitado** para especificar que el flujo de trabajo empezará en cuanto se produzca el evento en el primer paso de tipo **Punto de entrada**. Para obtener más información, consulte [Uso de flujos de trabajo](across-use-workflows.md).  

> [!NOTE]  
>  No habilite un flujo de trabajo hasta que esté seguro de que el flujo de trabajo esté completado y que los pasos del flujo de trabajo relacionado puedan comenzar.  

> [!TIP]  
>  Para ver las relaciones entre las tablas que se utilizan en los flujos de trabajo, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe") y, a continuación, introduzca **Flujo de trabajo: relaciones de tabla**.  

## <a name="see-also"></a>Consulte también  
[Procedimiento: crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)   
[Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
[Procedimiento: Ver las instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)   
[Procedimiento: Eliminar flujos de trabajo](across-how-to-delete-workflows.md)   
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Configuración de flujos de trabajo](across-set-up-workflows.md)   
[Uso de flujos de trabajo](across-use-workflows.md)   
[Flujo de trabajo](across-workflow.md)      


