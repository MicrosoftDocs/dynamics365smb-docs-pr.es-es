---
title: Crear flujos de trabajo | Documentos de Microsoft
description: Puede crear flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0db0e2e6705a7d2fd1907227996d8c258dcbc554
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754797"
---
# <a name="create-workflows"></a>Crear flujos de trabajo
Puede crear flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo moderado por condiciones de evento y una respuesta de flujo de trabajo con opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

Al crear flujos de trabajo, puede copiar los pasos de flujos de trabajo existentes o de plantillas de flujo de trabajo. Las plantillas de flujo de trabajo representan flujos de trabajo no editables que existen en la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)]. El código de las plantillas de flujo de trabajo agregados por Microsoft se prefija con “MS-“, como “MS-PIW”. Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

Si su escenario empresarial necesita eventos de flujo de trabajo o respuestas que no se admiten, un asociado de Microsoft debe implementarlos personalizando el código de aplicación.  

> [!NOTE]  
>  Todas las notificaciones sobre pasos de flujo de trabajo se envían a través de una cola de proyectos. Asegúrese de que la cola de proyectos en la instalación está configurada para gestionar las notificaciones de flujo de trabajo, así como que la casilla **Iniciar automáticamente desde NAS** esté seleccionada. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Para crear un flujo de trabajo  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Flujos de trabajo** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la página **Flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. Para crear el flujo de trabajo desde una plantilla, en la página **Flujos de trabajo**, seleccione la acción **Crear flujo de trabajo desde plantilla**. Para obtener más información, consulte [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  
5. En el campo **Descripción**, describa el flujo de trabajo.  
6. En el campo **Categoría**, especifique a qué categoría pertenece el flujo de trabajo.  
7. En el campo **Evento Cuando**, especifique el evento que debe producirse para iniciar el paso del flujo de trabajo.  

    Cuando elige el campo, la página **Eventos de flujo de trabajo** se abre, donde puede seleccionar de todos los eventos de flujo de trabajo existentes.  
8. En el campo **Condición**, especifique una o varias condiciones que se deben cumplir para que se produzca el evento en el campo **Evento Cuando**.  

    Cuando elige el campo se abre la página **Condiciones de evento**, donde se elige entre una lista de campos de filtro pertinentes relevantes como condiciones del evento en cuestión. Puede agregar los campos de filtro nuevos que desee utilizar como condiciones del evento. Puede definir filtros de condición de evento igual que define filtros en las páginas de solicitud de informe.  

    Si el evento del flujo de trabajo es el cambio de un campo determinado en un registro, la página **Condiciones del evento** se abre con las opciones para seleccionar el campo y el tipo de cambio.  

    1.  Para especificar un cambio de campo para el evento, en la página **Condiciones del evento**, en el campo **Campo**, seleccione el campo que cambia.  
    2.  En el campo **Operador**, seleccione **Disminuyó**, **Aumentó** o **Cambió**.  
9. Especifique la respuesta que seguirá cuando se produzca el evento del flujo de trabajo en el campo **Respuesta Entonces**.  

     Cuando elija el campo, la página **Respuestas de flujo de trabajo** se abre, donde puede seleccionar de todas las respuestas de flujo de trabajo que existen y fijar opciones de respuesta para la respuesta seleccionada.  
10. En la ficha desplegable **Opciones para la respuesta seleccionada**, especifique las opciones para la respuesta de flujo de trabajo seleccionando los valores en los campos que aparecen, como se indica a continuación:  

    1.  Para especificar las opciones para una respuesta de flujo de trabajo que implica enviar una notificación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Descripción|  
        |----------------------------------|---------------------------------------|  
        |**Notificar remitente**|Especifique si se notifica al solicitante de aprobación en lugar de al destinatario de la solicitud de aprobación. Si selecciona la casilla, el campo **Id. de usuario destinatario** está deshabilitado porque se notificará al solicitante de la aprobación, el remitente. El nombre de la respuesta del flujo de trabajo cambia en consecuencia, a **Crear notificación para &lt;remitente&gt;**. Si la casilla no está seleccionada, el nombre de la respuesta del flujo de trabajo es **Crear notificación para &lt;usuario&gt;**.
        |**Id. de usuario destinatario**|Especifique el usuario al que se debe enviar la notificación. Nota: Esta opción solo está disponible para respuestas de flujo de trabajo con un marcador para un usuario específico. Para las respuestas de flujo de trabajo sin marcadores para usuarios, el usuario de aprobación define normalmente la configuración del destinatario de la notificación.|  
        |**Tipo de movimiento de notificación**|Especifica si la notificación de flujo de trabajo se desencadena por un cambio de registro, una solicitud de aprobación o una fecha de vencimiento pasada.|
        |**Página de destino de vínculo**|Especifique otra página en [!INCLUDE[prod_short](includes/prod_short.md)] que el vínculo de la notificación abrirá en lugar de la página predeterminada.<br /><br />Tenga en cuenta que la página debe tener la misma tabla de origen que el registro involucrado.|  
        |**Personalizar vínculo**|Especifique la dirección URL de un vínculo que se agrega a la notificación además del vínculo a la página en [!INCLUDE[prod_short](includes/prod_short.md)].|  
    2.  Para especificar opciones para una respuesta de flujo de trabajo que implica crear una solicitud de aprobación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo|Description|  
        |----------------------------------|---------------------------------------|  
        |**Fórmula fecha vencimiento**|Especifique la cantidad de días en que se debe completar la solicitud de aprobación desde la fecha en que se ha enviado.|  
        |**Delegar tras**|Especifica si y cuándo se delegará automáticamente una solicitud de aprobación al sustituto correspondiente. Puede seleccionar delegar automáticamente un día, dos o cinco después de la fecha en que se solicitó la aprobación.|  
        |**Tipo de aprobador**|Especifique quién es el aprobador según la configuración de usuarios de aprobación y usuarios de flujo de trabajo.<br /><br /> Las siguientes opciones están disponibles:<br /><br /> -   **Vendedor/Comprador** especifica que el usuario configurado en el campo **Cód. vendedor/comprador** en la página **Config. usuario aprobación** determina quién es el aprobador. Los movimientos de solicitud de aprobación se crean según el valor del campo **Tipo de límite de aprobador**.<br />     Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-workflow-users.md).|  
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
>  Para ver las relaciones entre las tablas que se utilizan en los flujos de trabajo elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") y, a continuación, introduzca **Flujo de trabajo: relaciones de tabla**.  

## <a name="see-also"></a>Consulte también  
[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)   
[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)   
[Eliminar flujos de trabajo](across-how-to-delete-workflows.md)   
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Configuración de flujos de trabajo](across-set-up-workflows.md)   
[Uso de flujos de trabajo](across-use-workflows.md)   
[Flujo de trabajo](across-workflow.md)      


[!INCLUDE[footer-include](includes/footer-banner.md)]