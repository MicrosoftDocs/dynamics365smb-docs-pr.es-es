---
title: Usar partes de horas
description: 'Aprenda a crear, enviar, aprobar y publicar partes de horas para recursos, proyectos y servicios.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 02/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Usar partes de horas

En este artículo se describe cómo utilizar partes de tiempo en Business Central para realizar un seguimiento de las ausencias y para realizar un seguimiento del tiempo y los recursos que se dedican a un proyecto. Seguir el tiempo le permite identificar problemas rápido y evitar retrasos o saturaciones de coste. Con los partes de horas, un recurso puede notificar fácilmente el uso del tiempo de un individuo o una máquina, y los administradores pueden revisar fácilmente el uso y su asignación.

Puede copiar y usar sus líneas de planificación de proyecto en una hoja de horas. De esa forma, solo debe especificar la información en un lugar para que la información de la línea siempre sea correcta. Para más información, consulte [Para copiar líneas de planificación del proyecto en un parte de horas](#copy-project-planning-lines-to-a-time-sheet).

Una vez aprobados los movimientos del parte de horas de un proyecto, puede registrarlos en el diario de proyectos o de recursos correspondiente. Para obtener más información, vaya a [Para publicar líneas del parte de horas en un diario de proyecto](#post-time-sheet-lines-in-a-project-journal) y [Para publicar líneas del parte de horas en un diario de recursos](#post-time-sheet-lines-in-a-resource-journal).

Para poder utilizar las hojas de horas, debe configurar la información general y especificar un administrador y uno o varios aprobadores de hojas de horas. Para obtener más información sobre cómo configurar partes de horas, vaya a [Configurar partes de horas](projects-how-setup-time-sheets.md).  

> [!TIP]
> Puede utilizar partes de horas en un dispositivo móvil. Para hacer eso, es posible que tenga que activar la opción **Usar nueva experiencia de parte de horas** en la página [Configuración de recursos](https://businesscentral.dynamics.com/?page=462).

## <a name="create-time-sheets"></a>Crear partes de horas

Puede usar la página **Crear partes de horas** para configurar hojas de horas de un número determinado de periodos o semanas. Después, el propietario de la hoja de horas puede abrirla y registrar el tiempo dedicado en una tarea. También puede [programar el proyecto por lotes para que se ejecute automáticamente](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Debe disponer de permisos para poder crear los partes de horas. Para obtener más información sobre los permisos, vaya a [Configurar partes de horas](projects-how-setup-time-sheets.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear partes dehoras** y luego elija el enlace relacionado.

    > [!TIP]
    > También puede usar la acción **Crear parte de horas** en la lista de la página **Recursos** y la página **Tarjeta de recurso**.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Antes de crear partes de horas para un recurso, asegúrese de que los campos **Usar parte de horas** y **ID de usuario del propietario del parte de horas** se especifican para ellos en la página **Tarjeta de recursos**.

    Opcionalmente, elija la acción **Programar** para especificar la frecuencia con la que desea que la tarea se ejecute automáticamente. Por ejemplo, para configurar la tarea para que se ejecute semanalmente durante cuatro semanas, en la página **Programar un informe - Crear hojas de tiempo**, configure el campo **Fórmula de fecha de próxima ejecución** a **4W**. Para obtener más información sobre la programación de informes, vaya a [Programación de un informe para ejecutar](ui-work-report.md#ScheduleReport).  

Puede ver las hojas de horas creadas en la página **Partes de horas**. Cada hoja de horas consta de una o más líneas que definen la hora que desea enviar para su aprobación. La siguiente tabla describe los tipos de líneas que puede agregar a la hoja de horas.

| **Campo** | **Descripción** |
|---|---|
| | Utilice para agregar una nota o un marcador en el campo **Descripción** de la línea de la hoja de horas. Por ejemplo, puede utilizar este campo para clasificar movimientos de la hoja de horas. Si deja vacío el campo **Tipo** para una línea de hoja de horas, no podrá escribir valores de tiempo en los campos de día de la semana para esa línea. |
| Ausencia | Utilice para registrar el tiempo en que está ausente durante una semana de trabajo. Para completar la información de la línea, especifique el tipo de ausencia en el campo **Cód. causa ausencia**. |
| Pedido de ensamblado | Se usa para registrar tiempo para pedidos de ensamblado. Una línea de hoja de horas de este tipo se crea durante el registro de líneas de pedido de ensamblado para las que se configura el recurso para utilizar partes de horas. No puede seleccionar manualmente una línea de este tipo. |
| Proyecto | Utilice para registrar el consumo de tiempo para un proyecto. Para completar la información de la línea, especifique el número de proyecto y de tarea del proyecto para los que desea registrar tiempo. Puede registrar tiempo para las líneas que no se han programado.|
| Recurso | Utílicelo para registrar el uso del tiempo para un recurso. Para completar la información de la línea, proporcione una descripción del trabajo. |
| Servicio | Utilice para registrar el uso del tiempo para un pedido de servicio o abono de servicio. |

Por ejemplo, desea enviar un parte de horas de una semana en la que realizó tareas de limpieza y tuvo un día libre para una cita médica. La siguiente tabla muestra cómo agregaría líneas al parte de horas.

| Tipo | Descripción | Cód. tipo trabajo | Código de tipo de ausencia |
|--|--|--|--|
| Recurso | Horas laborables | Limpieza |  |
| Ausencia | Indisponibilidad |  | Sanidad |
|  | Tuve que tomarme el martes libre debido a una cita médica. |  |  |

En este ejemplo hipotético, luego puede registrar las horas de los días relevantes para cada día de la semana.  

> [!TIP]
> En la mayoría de los casos, su empresa tendrá tipos de trabajo predefinidos para los distintos tipos de líneas. En esos casos, simplemente elija el tipo de trabajo relevante de la lista y luego agregue su propia descripción.  
>
> Elija el tipo de trabajo eligiendo el botón :::image type="icon" source="media/assist-edit-icon.png" border="false"::: en el campo **Descripción**, eligiendo la acción **Detalles de la actividad** y luego especificándolo en la página que se abre, o eligiéndolo en el campo **Código de tipo de trabajo** o el campo **Código de tipo de ausencia**, respectivamente. En este caso, puede ignorar la sección [Para definir tipos de trabajo y agregar uno a una hoja de horas](#define-work-types-and-add-one-to-a-time-sheet).  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Para volver a utilizar las líneas del parte de horas en otros partes de horas

Si la información del parte de horas sigue siendo la misma de un período de tiempo a otro, copie las líneas del período anterior para ahorrar tiempo. A continuación, especifique solo el uso del tiempo para el nuevo periodo.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Abra la hoja de horas de un periodo posterior al periodo de una hoja de horas existente con las líneas.  
3. Elija la acción **Copiar líneas desde hoja de horas anterior**.

Las líneas se copiarán, incluidos los detalles como el tipo y la descripción. Por ejemplo, si la línea está relacionada con un proyecto, **Nº proyecto** es el campo que se copia. Todas las líneas copiadas tienen el estado **Abierto**. Ahora puede modificar las líneas según sea necesario.

## <a name="copy-project-planning-lines-to-a-time-sheet"></a>Copiar líneas de planificación del proyecto en una hoja de horas

El procedimiento siguiente describe cómo agregar rápidamente líneas de planificación del proyecto a una hoja de horas.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.  
2. En la página **Hojas de horas**, seleccione un parte de horas para periodo de tiempo correspondiente.  
3. Elija la acción **Crear líneas de planificación de proyecto**. Cualquier línea de planificación de proyecto del periodo de tiempo de la hoja de horas se copia en la hoja de horas de la persona o equipo en el campo **N.º recurso** en la hoja de horas.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Para definir los tipos de trabajo y agregar uno a un parte de horas

Puede definir el tipo de trabajo para todas las líneas de la hoja de horas de pedidos de servicio, pedidos del proyecto y recursos. De esta forma, puede agregar información que necesite para facturar al cliente distintos tipos de trabajo.  

1. En la página **Partes de horas**, seleccione el parte de horas relevante.
2. En la primera de las líneas de la sección **Líneas**, elija el campo **Tipo** y luego elija el tipo relevante, como *Recurso*.  
3. Elija el campo **Descripción** y luego, en la página **Detalle res. línea hoja de horas**, complete los campos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Si hay ningún tipos de trabajo, elija la acción **Nuevo**.
    2. En la página **Tipos de trabajo**, rellene los campos según sea necesario y, a continuación, vuelva a la hoja de horas.
4. Rellene el resto de la hoja de horas. Para obtener más información, consulte la sección [Para completar líneas de la hoja de horas y enviarlas para su aprobación](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Puede seguir pasos similares para definir códigos de ausencia.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Para rellenar una línea de parte de horas y enviarla para su aprobación

El registro de la hoja de horas se hace en horas, la unidad de medida base estándar para los recursos. De forma predeterminada, una hoja de horas muestra los días de trabajo comunes de lunes a viernes.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Seleccione un parte de hojas para el período relevante.
3. Rellene los campos de una línea, que sean necesario. Introduzca el número de horas que ha usado el recurso cada día de la semana.  

    En la mayoría de los casos, para realizar un seguimiento del trabajo, agregue una línea de tipo *Recurso* y luego registre las horas dedicadas cada día. Si desea registrar ausencia, agregue una línea de tipo *Ausencia*.  

    > [!TIP]  
    > Puede revisar la suma de horas de la hoja de horas que ha introducido en el cuadro informativo **Resumen real/presupuestado**.  
4. Repita el paso 3 para otros tipos de trabajo que realice el recurso.  

    A continuación, decida si desea enviar todas las líneas o las seleccionadas en el parte de horas.  

    * Para enviar la hoja de tiempo para una o más líneas, elija la línea relevante y luego elija la accción **Enviar**.

        En la página de envío, elija la opción **Solo líneas seleccionadas**. La línea cambia de estado de **Abierta** a **Enviada**.
    * Para enviar la hoja de horas para todas las líneas abiertas, elija la acción **Enviar** en la parte superior de la página **Hoja de horas**.  

        Se le pedirá que confirme que desea enviar todas las líneas abiertas en el parte de horas actual.  

    > [!NOTE]  
    > Solo puede enviar las líneas de hoja de horas para las que haya especificado tiempo.  
5. Para modificar la información de una línea que se ha definido como **Enviado**, seleccione la línea y, a continuación, elija la acción **Volver a abrir**.

    > [!NOTE]  
    > Un administrador puede rechazar una línea del parte de horas que se ha enviado para su aprobación. Si una línea tiene el estado de **Impagado**, puede realizar los cambios en la línea y seleccionar **Enviar** de nuevo.  
6. Elija el botón **Aceptar**.

## <a name="approve-or-reject-a-time-sheet"></a>Aprobar o rechazar un parte de horas

Una hoja de horas debe haberse enviado para su aprobación para que se pueda usar. Puede aprobar y rechazar las líneas individuales en una hoja de horas o enviarlas de nuevo al emisor. Un parte de horas se puede aprobar de dos maneras:

* Un administrador de la hoja de horas puede aprobar en cualquier momento la hoja.
* La persona que se especifica en el campo **Id. usuario aprob. hoja horas** en una ficha de recurso puede aprobar las hojas de horas de ese recurso. Para obtener más información sobre cómo configurar la aprobación, vaya a [Configurar partes de horas](projects-how-setup-time-sheets.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas del administrador** y luego elija el enlace relacionado.
2. Seleccione una hoja de horas de la lista.  
3. En la página **Parte de horas**: 
    1. Elija la acción **Proceso**, luego elija la acción **Aprobar**.
    2. Elija la acción **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la página **Parte de horas**.
4. Elija el botón **Aceptar**.  
5. También puede elegir la acción **Rechazar** y seguir los pasos del 4 al 5.  

> [!TIP]  
> Utilice los cuadros informativos **Estado de hoja de horas** y **Resumen real/presupuestado** para obtener un resumen de la información de la hoja de horas.

Una vez aprobado o rechazado un parte de horas, no se podrá modificar hasta que no se vuelva a abrir. En el procedimiento siguiente se explica cómo volver a abrir una hoja de horas aprobada o rechazada.

## <a name="reopen-a-time-sheet"></a>Para reabrir un parte de horas

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas del administrador** u **Hojas de horas** y luego elija el enlace relacionado.
2. Abra una hoja de horas de la lista.  

    > [!NOTE]  
    > Puede volver a abrir solo las líneas con el estado **Aprobado**. No puede volver a abrir las líneas con el estado **Rechazado** o que se ha publicado.  
3. En la página **Parte de horas**, elija la acción **Volver a abrir** y, a continuación, **Todas las líneas enviadas** para volver a abrir todas las líneas o la acción **Solo líneas seleccionadas** para volver a abrir únicamente las líneas que están seleccionadas en la página **Parte de horas**.
4. Elija el botón **Aceptar**. El estado de las líneas de la hoja de horas cambia a **Enviado**.  

## <a name="view-and-approve-time-sheets-by-project"></a>Ver y aprobar partes de horas por proyecto

En un proyecto, puede especificar una persona que sea responsable del proyecto. Esa información está vinculada a las líneas del parte de horas. El enlace ofrece a los gerentes de proyecto una lista de los partes de horas para aprobar. Por ejemplo, el director del proyecto del equipo puede ser responsable de determinados proyectos de la empresa. En ese caso, el director debe designarse como **Persona responsable** en la página de la tarjeta de proyecto. En esta vista de información del parte de horas, puede ver las tareas del proyecto asociadas a un proyecto y la cantidad de horas empleadas.

> [!NOTE]
> Para aprobar los partes de horas en la página **Parte de horas del administrador por proyecto**, primero debe seleccionar una opción **Parte de horas por aprobación de proyecto** en la página **Configuración de recursos**. Para obtener más información sobre cómo configurar aprobaciones para recursos, vaya a [Configurar recursos](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-project"></a>Aprobar o rechazar un parte de horas por proyecto

1. En el cuadro **Buscar**, escriba **Hoja de horas del administrador por proyecto** y, a continuación, elija el vínculo relacionado. [!INCLUDE[prod_short](includes/prod_short.md)] muestra una lista de líneas de parte de horas asociadas con los proyectos de los que es responsable.
2. Elija la acción **Aprobar** y, a continuación, elija la acción **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la página **Parte de horas**.

    > [!NOTE]
    > Solo puede aprobar los partes de horas que tengan el estado **Enviado**.

3. Para proporcionar información adicional sobre la aprobación o el rechazo, seleccione la acción **Relacionado** y luego seleccione **Comentarios** y luego **Comentarios de línea**.
4. Elija el botón **Aceptar**.

> [!NOTE]
> Una vez aprobada o rechazada una línea del parte de horas por proyecto, no se podrá volver a abrir ni modificar en la página **Parte de horas**.

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Para registrar las líneas de hoja de horas en un diario de recursos

Una vez aprobados los movimientos de la hoja de horas de un recurso, puede registrarlas en el diario de recursos correspondiente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después escriba **Diarios del recurso**, y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario recursos**, rellene los campos en una línea según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de recursos, donde puede modificar la información según sea necesario.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. recursos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="post-time-sheet-lines-in-a-project-journal"></a>Para registrar las líneas de hoja de horas en un diario de proyectos

Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlas en el diario de proyectos correspondiente.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario proyectos**, rellene los campos en una línea según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de proyectos, donde puede modificar la información según sea necesario.  

    > [!NOTE]  
    > La información acerca del tipo de trabajo y si el trabajo es facturable debe copiarse de la línea del parte de horas. Si es necesario, puede reducir la cantidad de horas cuenta y hacer un registro parcial. Si se reduce la cantidad, la próxima vez que elija la acción **Sugerir líneas de partes de horas**, la línea creada contendrá la cantidad pendiente de horas.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. proyectos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="archive-time-sheets"></a>Archivar partes de horas

Después de registrar los partes de horas, puede archivarlos para referencia futura. Debe publicar todas las líneas en un parte de horas antes de poder archivarlo.

> [!NOTE]  
> Cuando se archiva una hoja de horas, se elimina de las listas de las páginas **Partes de horas** y **Partes de horas del administrador**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.
2. Seleccione la acción **Mover hojas de horas a archivo**.  
3. En la página **Mover hojas de horas a archivo**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.  
4. Para revisar hojas de horas archivadas, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos de hoja de horas** o **Archivos de hoja de horas del administrador** y luego elija el enlace relacionado.

## <a name="see-also"></a>Consulte también .

[Administración de proyectos](projects-manage-projects.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
