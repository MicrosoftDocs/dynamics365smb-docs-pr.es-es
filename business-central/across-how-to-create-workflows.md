---
title: Crear flujos de trabajo de aprobación para conectar tareas
description: Obtenga información acerca de cómo crear flujos de trabajo que conecten tareas realizadas por distintos usuarios en procesos de negocio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a><a name="create-workflows-to-connect-tasks-in-business-processes"></a><a name="create-workflows-to-connect-tasks-in-business-processes"></a><a name="create-workflows-to-connect-tasks-in-business-processes"></a>Crear flujos de trabajo para conectar tareas en procesos de negocio

Puede crear flujos de trabajo que conecten tareas en procesos de negocio realizadas por distintos usuarios. Puede incluir tareas de sistema, como registros automáticos, como pasos en los flujos de trabajo que van antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

En la página **Flujo de trabajo** puede crear un flujo de trabajo haciendo una lista de los pasos en las líneas. Cada paso consta de un desencadenador y una respuesta:

* Un evento que especifica las condiciones que iniciarán el flujo de trabajo.
* Una respuesta de flujo de trabajo que define lo que hace el flujo de trabajo.

[!INCLUDE[workflow](includes/workflow.md)]

Al crear flujos de trabajo, puede copiar los pasos de flujos de trabajo existentes o de plantillas de flujo de trabajo. Las plantillas de flujo de trabajo son flujos de trabajo no editables que proporciona [!INCLUDE[prod_short](includes/prod_short.md)]. Los identificadores de plantillas de flujo de trabajo se prefijan con "MS-", como "MS-PIW". Obtenga más información en [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Todas las notificaciones sobre pasos de flujo de trabajo se envían a través de una cola de proyectos. Asegúrese de que la cola de trabajos refleje sus necesidades comerciales. Obtenga más información en [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Ilustración de un ejemplo de flujo de trabajo.":::

Un flujo de trabajo se divide en tres secciones:

1. **Evento Cuando**  
   Aquí es donde se selecciona el disparador.  
   Ejemplos de disparador:
   * Se ha cambiado un registro de datos maestros
   * Se ha creado una línea del diario
   * Se ha creado o liberado un documento entrante
   * Se ha solicitado la aprobación de un documento
2. **Condición On**  
   Las **condiciones** están relacionadas con el evento y permiten crear filtros para decidir cómo continúa el flujo de trabajo.
3. **Respuesta Entonces**  
   Las **respuestas** especifican los siguientes pasos en el flujo de trabajo.

Las opciones para eventos y respuestas están definidas por el sistema. Para agregar nuevas opciones, deberá desarrollar una extensión.

## <a name="to-create-a-workflow"></a><a name="to-create-a-workflow"></a><a name="to-create-a-workflow"></a><a name="to-create-a-workflow"></a>Para crear un flujo de trabajo

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la página **Flujo de trabajo**.  
3. En el campo **Código**, introduzca un máximo de 20 caracteres para identificar el flujo de trabajo.  
4. Para crear el flujo de trabajo desde una plantilla, en la página **Flujos de trabajo**, seleccione la acción **Nuevo flujo de trabajo desde plantilla**. Obtenga más información en [Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md).  
5. En el campo **Descripción**, describa el flujo de trabajo.  
6. En el campo **Categoría**, especifique a qué categoría pertenece el flujo de trabajo.  
7. En el campo **Evento Cuando**, especifique el evento que debe producirse para iniciar el paso del flujo de trabajo.  

   Cuando elige el campo, la página **Eventos de flujo de trabajo** muestra todos los eventos de flujo de trabajo disponibles.  
8. En el campo **Condición en**, especifique una o varias condiciones que se deben cumplir para que se produzca el evento en el campo **Evento Cuando**.  

   Cuando elige el campo, la página **Condiciones de evento** enumera los campos de filtro que pueden ser condiciones para el evento. Puede agregar nuevos campos de filtro si lo desea.  

   Si el evento del flujo de trabajo es el cambio de un campo determinado en un registro, utilice la página **Condiciones del evento** para seleccionar el campo y el tipo de cambio.  

   1. Para especificar un cambio de campo para el evento, en la página **Condiciones del evento**, en el campo **Campo**, seleccione el campo que cambia.  
   2. En el campo **Operador**, seleccione **Disminuyó**, **Aumentó** o **Cambió**.  
9. Especifique la respuesta que seguirá cuando se produzca el evento del flujo de trabajo en el campo **Respuesta Entonces**.  

   Cuando elige el campo, la página **Respuestas de flujo de trabajo** muestra todas las respuestas de flujo de trabajo y las opciones de respuesta disponibles.  
10. En la ficha desplegable **Opciones para la respuesta seleccionada**, especifique las opciones para la respuesta de flujo de trabajo seleccionando los valores en los campos que aparecen, como se indica a continuación:  

    1. Para especificar las opciones para una respuesta de flujo de trabajo que implica enviar una notificación, rellene los campos tal como se describe en la tabla siguiente.  

    > [!NOTE]
    > Estos campos varían, según la respuesta que haya elegido.

       |Campo|Descripción|
       |-----|-----------|
       |**Notificar remitente**|Especifique si se notifica al solicitante de aprobación en lugar de al destinatario de la solicitud de aprobación. Si selecciona la casilla, el campo **Id. de usuario destinatario** está deshabilitado porque se notificará al solicitante de la aprobación, el remitente. El nombre de la respuesta del flujo de trabajo cambia en consecuencia, a **Crear notificación para &lt;remitente&gt;**. Si la casilla no está seleccionada, el nombre de la respuesta del flujo de trabajo es **Crear notificación para &lt;usuario&gt;**.|
       |**Id. de usuario destinatario**|Especifique el usuario al que se debe enviar la notificación. **Nota**: Esta opción solo está disponible para respuestas de flujo de trabajo con un marcador para un usuario específico. Para las respuestas de flujo de trabajo sin marcadores para usuarios, el usuario de aprobación define normalmente la **configuración del usuario de aprobación**.|
       |**Tipo de movimiento de notificación**|Especifique un desencadenador para la notificación de flujo de trabajo. El desencadenador puede ser un cambio de registro, una solicitud de aprobación o una fecha de vencimiento pasada.|
       |**Página de destino de vínculo**|Especifique la página que abre el vínculo en la notificación. La página debe tener la misma tabla de origen que el registro involucrado.|
       |**Personalizar vínculo**|Especifique la dirección URL de un vínculo que se incluye en la notificación además del vínculo a la página.|

    2. Para especificar opciones para una respuesta de flujo de trabajo que implica crear una solicitud de aprobación, rellene los campos tal como se describe en la tabla siguiente.  

       |Campo|Descripción|  
       |-----|-----------|  
       |**Fórmula fecha vencimiento**|Especifique el número de días que tiene el aprobador para resolver la solicitud. El plazo comienza cuando se envía la solicitud.|
       |**Delegar tras**|Especifica si y cuándo se delegará automáticamente una solicitud de aprobación al sustituto. Puede seleccionar delegar automáticamente un día, dos o cinco después de la fecha en que se solicitó la aprobación.|
       |**Tipo de aprobador**|Especifique quién es el aprobador según la configuración de usuarios de aprobación y usuarios de flujo de trabajo. Cuando el campo se establece como **Vendedor/Comprador**, el usuario especificado en el campo **Cód. vendedor/comprador** en la página **Config. usuario aprobación** determina quién es el aprobador. Los movimientos de solicitud de aprobación se crean según el valor del campo **Tipo de límite de aprobador**. Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-workflow-users.md).|
       |**Mostrar mensaje de confirmación**|Especifica si se muestra un mensaje de confirmación después de que un usuario solicita una aprobación.|
       |**Tipo de límite de aprobador**|Especifique el efecto de los límites para los aprobadores. El límite de aprobación de un aprobador debe ser superior al valor de la solicitud. Las siguientes opciones están disponibles: <ol><li>**Cadena de aprobadores** especifica que los movimientos de solicitud de aprobación se crean para todos los aprobadores del solicitante hasta el primer aprobador cualificado, incluido este</li><li>**Aprobador directo** especifica que un movimiento de solicitud de aprobación solo se crea para el aprobador inmediato del solicitante, sea cual sea el límite de aprobación del aprobador.</li><li>**Primer aprobador cualificado** especifica que solo se crea un movimiento de solicitud de aprobación para el primer aprobador del solicitante.</li><li>**Aprobador específico** especifica que usted notifique al usuario elegido en el campo **Id. aprobador**.</li></ol>|

    3. Para especificar las opciones para una respuesta de flujo de trabajo que implica crear líneas de diario, rellene los campos tal como se describe en la tabla siguiente.  

       |Campo|Descripción|  
       |-----|-----------|  
       |**Nombre plantilla diario general**|Especifique el nombre de la plantilla de libro de diario general en las que se crearán las líneas de diario especificadas.|  
       |**Nombre sección diario general**|Especifique el nombre del proceso de diario general en las que se crearán las líneas de diario especificadas.|  

11. Seleccione los botones **Aumentar sangría** y **Disminuir sangría** para sangrar el nombre del evento en el campo **Cuando** para definir la posición del paso de flujo de trabajo.  

    1. Aplique sangría al evento bajo el nombre del paso anterior para indicar que es el paso siguiente.  
    2. Indique que el paso es uno de varios pasos alternativos que pueden iniciarse en función de la condición aplicando sangría en el nombre del evento para que coincida con los otros pasos alternativos. Ordene estos pasos opcionales según la prioridad colocando el paso más importante primero.  

    > [!NOTE]  
    >  Puede cambiar solo la sangría de un paso que no tenga un paso subsiguiente.  

12. Repita los pasos del 7 al 11 para añadir más pasos de flujo de trabajo antes o después del paso que ha creado.  
13. Active el control de alternancia **Habilitado** para especificar que el flujo de trabajo empezará cuando se produzca el evento en el primer paso de tipo **Punto de entrada**. Obtenga más información en [Usar flujos de trabajo](across-use-workflows.md).  

> [!NOTE]  
> No habilite un flujo de trabajo hasta que esté seguro de que está listo.  

> [!TIP]  
> Para explorar las relaciones entre las tablas que se utilizan en flujos de trabajo, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") y luego especifique **Flujo de trabajo: relaciones de tabla**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a><a name="example-of-creating-a-new-workflow-using-existing-events"></a><a name="example-of-creating-a-new-workflow-using-existing-events"></a><a name="example-of-creating-a-new-workflow-using-existing-events"></a>Ejemplo de creación de un nuevo flujo de trabajo utilizando eventos existentes

En el siguiente ejemplo, se crea un flujo de trabajo para aprobar un cambio en el nombre de un proveedor:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**. Se abre la página **Flujo de trabajo**.
3. En la sección de flujo de trabajo, rellene los campos tal como se describe en la tabla siguiente.

    |Campo  |Valor  |
    |---------|---------|
    |**Código**|**VENDAPN-01**|
    |**Descripción**|**Aprobación de cambios del nombre de proveedor** |
    |**Categoría**|**COMPRAS**|

4. Para crear el primer paso del flujo de trabajo, haga lo siguiente.

    1. En el campo **Evento Cuando**, especifique *Se modifica un registro de proveedor*.  
    2. En el campo **Condición On**, elija la palabra **Siempre**. A continuación, en la página **Condiciones del evento**, elija el vínculo **Agregar una condición para cuando cambie el valor de un campo** y, a continuación, seleccione el campo **Nombre**. El resultado de este paso es que la condición se lee como *Se cambia el nombre*.  
    3. En el campo **Respuesta entonces**, elija el vínculo **Seleccionar respuesta**. A continuación, en la página **Respuestas de flujo de trabajo**, en el campo **Seleccionar respuesta**, elija la respuesta **Revertir el valor del campo \<Field\> en el registro y guardar el cambio**. Entonces, en la sección **Opciones para la respuesta seleccionada**, especifique el campo **Nombre**.  
    4. Elija el vínculo **Agregar más respuestas** y, a continuación, agregue una entrada para la respuesta **Crear una solicitud de aprobación para el registro utilizando el tipo de aprobador <%1> y <%2>**.  
    5. En la sección **Opciones para la respuesta seleccionada** para la nueva respuesta, cambie el campo **Tipo de aprobador** a **Grupo de usuarios de flujo de trabajo**. Luego, en el campo **Grupo de usuarios de flujo de trabajo**, especifique el grupo de usuarios. Obtenga más información en [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).  
    6. Agregue una tercer respuesta, **Envíe la solicitud de aprobación para el registro y cree una notificación**.  
    7. Agregue una cuarta respuesta, **Mostrar mensaje "%1"**. A continuación, en la sección **Opciones para la respuesta seleccionada**, en el campo **Mensaje**, especifique **Se ha enviado una solicitud de aprobación**.  
    8. Elija **Aceptar** para volver al paso de flujo de trabajo.  

5. En la siguiente línea, agregue un nuevo paso de flujo de trabajo para el evento **Se ha aprobado una solicitud de aprobación**.

    1. En el campo **Evento Cuando**, especifique **Se ha aprobado una solicitud de aprobación**.  
    2. Elija el menú de línea y luego elija **Aumentar sangría**.  
    3. En el campo **Condición On**, elija **Siempre**. Luego, en el campo **Aprobaciones pendientes**, especifique **0**. La condición se lee como **Aprobaciones pendientes:0** para indicar que la solicitud no requiere más aprobadores.  
    4. En el campo **Respuesta entonces**, elija el vínculo **Seleccionar respuesta**. A continuación, en la página **Respuestas de flujo de trabajo**, en el campo **Seleccionar respuesta**, elija la respuesta **Envíe la solicitud de aprobación para el registro y cree una notificación**.  
    5. Elija **Aceptar**.  
6. En la siguiente línea, agregue un segundo paso de flujo de trabajo para el evento **Se ha aprobado una solicitud de aprobación**.  

    1. En el campo **Evento Cuando**, especifique **Se ha aprobado una solicitud de aprobación**.
    2. En el campo **Condición On**, elija **Siempre**. Luego, en el campo **Aprobaciones pendientes**, especifique **>0**. La condición se lee como **Aprobaciones pendientes:>0** para indicar que este no es el último aprobador.  
    3. En el campo **Respuesta entonces**, elija el vínculo **Seleccionar respuesta**. A continuación, en la página **Respuestas de flujo de trabajo**, en el campo **Seleccionar respuesta**, elija la respuesta **Envíe la solicitud de aprobación para el registro y cree una notificación**.  
    4. Elija **Aceptar**.  
7. En la siguiente línea, agregue un paso de flujo de trabajo para el evento **Se ha delegado una solicitud de aprobación**.  

    1. En el campo **Evento Cuando**, especifique **Se ha delegado una solicitud de aprobación**.  
    2. En el campo **Condición On**, deje el valor como **Siempre**.  
    3. En el campo **Respuesta entonces**, elija el vínculo **Seleccionar respuesta**. A continuación, en la página **Respuestas de flujo de trabajo**, en el campo **Seleccionar respuesta**, elija la respuesta **Envíe la solicitud de aprobación para el registro y cree una notificación**.  
    4. Elija **Aceptar**.  
8. En la siguiente línea, agregue un segundo paso de flujo de trabajo para el evento **Se ha rechazado una solicitud de aprobación**.  

    1. En el campo **Evento Cuando**, especifique **Se ha rechazado una solicitud de aprobación**.  
    2. En el campo **Condición On**, deje el valor como **Siempre**.  
    3. En el campo **Respuesta entonces**, elija el vínculo **Seleccionar respuesta**. A continuación, en la página **Respuestas de flujo de trabajo**, en el campo **Seleccionar respuesta**, elija la respuesta **Descartar los nuevos valores**.  
    4. Elija el vínculo **Agregar más respuestas** y luego agregue una entrada para la respuesta **Rechazar la solicitud de aprobación del registro y crear una notificación**.
    5. Elija **Aceptar**.  
9. Para habilitar el flujo de trabajo, active el control de alternancia a **Habilitado**.  

La siguiente ilustración proporciona una descripción general del resultado de este procedimiento.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Ilustración del flujo de trabajo Aprobación del nombre del proveedor.":::

A continuación, pruebe el flujo de trabajo abriendo una tarjeta de proveedor existente y cambiando el nombre. Verifique que se envíe una solicitud de aprobación después de cambiar el nombre del proveedor.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-workflows/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Crear flujos de trabajo a partir de plantillas de flujo de trabajo](across-how-to-create-workflows-from-workflow-templates.md)  
[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar notificaciones de flujo de trabajo de aprobación](across-setting-up-workflow-notifications.md)  
[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)  
[Eliminar flujos de trabajo de aprobación](across-how-to-delete-workflows.md)  
[Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Flujo de trabajo](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
