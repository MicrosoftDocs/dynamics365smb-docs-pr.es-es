---
title: Usar hojas de horas
description: 'Describe cómo crear una hoja de horas, definir los tipos de trabajo, rellenar la hoja de horas y enviarla para su aprobación.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: edupont
---
# Usar hojas de horas

Puede utilizar hojas de tiempo en [!INCLUDE [prod_short](includes/prod_short.md)] para realizar un seguimiento de las ausencias y para realizar un seguimiento del tiempo y los recursos que se gastan en un proyecto. Con la administración de tiempo, puede identificar problemas rápido y evitar retrasos o saturaciones de coste. Con las hojas de horas, un recurso puede notificar fácilmente el uso del tiempo de un individuo o una máquina, y un administrador puede revisar fácilmente el uso y su asignación. Este artículo describe cómo crear una hoja de horas, definir tipos de trabajo, rellenar la hoja de horas y enviarla para su aprobación.  

Puede copiar y usar sus líneas de planificación de proyecto en una hoja de horas. De esa forma, solo debe especificar la información en un lugar para que la información de la línea siempre sea correcta.

Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlos en el diario de proyectos o de recursos correspondiente.

Para poder utilizar las hojas de horas, debe configurar la información general y especificar un administrador y uno o varios aprobadores de hojas de horas. Para obtener más información, consulte [Configurar hojas de horas](projects-how-setup-time-sheets.md).  

> [!TIP]
> A partir del lanzamiento de versiones 2 de 2021, puede administrar los partes de horas asignados en un dispositivo móvil. Sin embargo, puede que el administrador deba habilitar la característica **Actualización de datos de característica: nueva experiencia de parte de horas** en la página [Administración de características](https://businesscentral.dynamics.com/?page=2610) para utilizar esta capacidad. Para obtener más información, consulte [Configurar partes de horas](projects-how-setup-time-sheets.md).

## Para crear partes de horas

Puede usar el proceso **Crear hojas de horas** para configurar hojas de horas de un número determinado de periodos o semanas. Después, el propietario de la hoja de horas puede abrirla y registrar el tiempo dedicado en una tarea. También puede [programar el trabajo por lotes para que se ejecute automáticamente](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Debe disponer de permisos para poder crear las hojas de horas. Para obtener más información, consulte [Configurar partes de horas](projects-how-setup-time-sheets.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.
2. En la página **Hojas de horas**, seleccione la acción **Crear hojas de horas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Los campos **Usar hoja horas** e **Id. usuario prop. hoja horas** deben completarse en la ficha del recurso de la hoja de horas.

    Opcionalmente, elija la acción **Programar** para especificar la frecuencia con la que desea que la tarea se ejecute automáticamente. Por ejemplo, para configurar la tarea para que se ejecute semanalmente durante cuatro semanas, en la página **Programar un informe - Crear hojas de tiempo**, configure el campo **Fórmula de fecha de próxima ejecución** a *4W*. Para más información, vea [Programar la ejecución de un informe](ui-work-report.md#ScheduleReport).  
4. Elija el botón **Aceptar**.  

Puede ver las hojas de horas creadas en la página **Hojas de horas**. Cada hoja de horas consta de una o más líneas que definen la hora que desea enviar para su aprobación. La siguiente tabla describe los tipos de líneas que puede agregar a la hoja de horas.

| **Campo** | **Descripción** |
|---|---|
| | Utilice para agregar una nota o un marcador en el campo **Descripción** de la línea de la hoja de horas. Por ejemplo, puede utilizar este campo para clasificar movimientos de la hoja de horas. Si deja vacío el campo **Tipo** para una línea de hoja de horas, no podrá escribir valores de tiempo en los campos de día de la semana para esa línea. |
| Ausencia | Utilice para registrar el tiempo en que está ausente durante una semana de trabajo. Para completar la información de la línea, especifique el tipo de ausencia en el campo **Cód. causa ausencia**. |
| Pedido de ensamblado | Se usa para registrar tiempo para pedidos de ensamblado. Una línea de hoja de horas de este tipo se crea durante el registro de líneas de pedido de ensamblado para las que se configura el recurso para utilizar hojas de horas. No puede seleccionar manualmente una línea de este tipo. |
| Proyecto | Utilice para registrar el consumo de tiempo para un proyecto. Para completar la información de la línea, especifique el número de proyecto y de tarea del proyecto para los que desea registrar tiempo. Puede registrar tiempo para las líneas que no se han programado.|
| Recurso | Utílicelo para registrar el uso del tiempo para un recurso. Para completar la información de la línea, proporcione una descripción del trabajo. |
| Servicio | Utilice para registrar el uso del tiempo para un pedido de servicio o abono de servicio. |

Por ejemplo, para enviar una hoja de horas para una semana laboral en la que trabajó en tareas de limpieza la mayoría de los días pero tuvo un día libre debido a citas médicas, agregaría líneas como se ilustra en la siguiente tabla.

| Escriba | Descripción | Cód. tipo trabajo | Código de tipo de ausencia |
|--|--|--|--|
| Recurso | Horas laborables | Limpieza |  |
| Ausencia | Indisponibilidad |  | Sanidad |
|  | Tuve que tomarme el martes libre debido a una cita médica. |  |  |

En este ejemplo hipotético, luego registraría las horas relevantes de los días relevantes en los campos para cada día de la semana.  

> [!TIP]
> En la mayoría de los casos, su empresa tendrá tipos de trabajo predefinidos para los distintos tipos de líneas. En esos casos, simplemente elija el tipo de trabajo relevante de la lista y luego agregue su propia descripción.  
>
> Elija el tipo de trabajo eligiendo el botón :::image type="icon" source="media/assist-edit-icon.png" border="false"::: en el campo **Descripción**, eligiendo la acción **Detalles de la actividad** y luego especificándolo en la página que se abre, o eligiéndolo en el campo **Código de tipo de trabajo** o el campo **Código de tipo de ausencia**, respectivamente. En este caso, puede ignorar la sección [Para definir tipos de trabajo y agregar uno a una hoja de horas](#to-define-work-types-and-add-one-to-a-time-sheet).  

## Para volver a utilizar las líneas de la hoja de horas en otras hojas de horas

Si la información de la hoja de horas no cambia con el tiempo, puede ahorrar tiempo copiando las líneas del periodo anterior. A continuación, solo especifique el uso del tiempo para el nuevo periodo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Abra la hoja de horas de un periodo posterior al periodo de una hoja de horas existente con las líneas.  
3. Elija la acción **Copiar líneas desde hoja de horas anterior**.

Las líneas se copiarán, incluidos los detalles como el tipo y la descripción. Por ejemplo, si la línea está relacionada con un trabajo, se copiará **Nº proyecto**. Todas las líneas copiadas tienen el estado **Abierto**. Ahora puede modificar las líneas según sea necesario.

## Para copiar líneas de planificación del proyecto en una hoja de horas
El procedimiento siguiente describe cómo agregar rápidamente líneas de planificación del proyecto a una hoja de horas.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.  
2. En la página **Hojas de horas**, seleccione un parte de horas para periodo de tiempo correspondiente.  
3. Elija la acción **Crear líneas de planificación de proyecto**. Cualquier línea de planificación de proyecto del periodo de tiempo de la hoja de horas se copia en la hoja de horas de la persona o equipo en el campo **N.º recurso** en la hoja de horas.

## Para definir los tipos de trabajo y agregar uno a una hoja de horas

Puede definir el tipo de trabajo para todas las líneas de la hoja de horas de pedidos de servicio, pedidos del proyecto y recursos. De esta forma, puede agregar información que necesite para facturar al cliente distintos tipos de trabajo.  

1. En la página **Hojas de horas**, seleccione la hoja de horas relevante.
2. En la primera de las líneas de la sección **Líneas**, elija el campo **Tipo** y luego elija el tipo relevante, como *Recurso*.  
3. Elija el campo **Descripción** y luego, en la página **Detalle res. línea hoja de horas**, complete los campos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Si hay ningún tipos de trabajo, elija la acción **Nuevo**.
    2. En la página **Tipos de trabajo**, rellene los campos según sea necesario y, a continuación, vuelva a la hoja de horas.
4. Rellene el resto de la hoja de horas. Para obtener más información, consulte la sección [Para completar líneas de la hoja de horas y enviarlas para su aprobación](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Se aplican pasos similares para definir códigos de ausencia.

## Para rellenar una línea de hoja de horas y enviarla para su aprobación

El registro de la hoja de horas se hace en horas, la unidad de medida base estándar para los recursos. De forma predeterminada, una hoja de horas muestra los días de trabajo comunes de lunes a viernes.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Seleccione un parte de hojas para el período relevante.
3. Rellene los campos de una línea, que sean necesario. Introduzca el número de horas que ha usado el recurso cada día de la semana.  

    En la mayoría de los casos, para realizar un seguimiento del trabajo, agregue una línea de tipo *Recurso* y luego registre las horas dedicadas cada día. Si desea registrar ausencia, agregue una línea de tipo *Ausencia*.  

    > [!TIP]  
    > Puede revisar la suma de horas de la hoja de horas que ha introducido en el cuadro informativo **Resumen real/presupuestado**.  
4. Repita el paso 3 para otros tipos de trabajo que realice el recurso.  

    A continuación, debe decidir si desea enviar todas las líneas de la hoja de horas o si desea enviar líneas individuales.  

    * Para enviar la hoja de tiempo para una o más líneas, elija la línea relevante y luego elija la accción **Enviar**.

        En la página de envío, elija la opción **Solo líneas seleccionadas**. La línea cambia de estado de *Abierta* a *Enviada*.
    * Para enviar la hoja de horas para todas las líneas abiertas, elija la acción **Enviar** en la parte superior de la página **Hoja de horas**.  

        Se le pedirá que confirme que desea enviar todas las líneas abiertas en la hoja de horas actual.  

    > [!NOTE]  
    > Solo puede enviar las líneas de hoja de horas para las que haya especificado tiempo.  
5. Para modificar la información de una línea que se ha definido como **Enviado**, seleccione la línea y, a continuación, elija la acción **Volver a abrir**.

    > [!NOTE]  
    >   Un administrador puede rechazar una línea de hoja de horas que se ha enviado para su aprobación. Si una línea tiene el estado de **Impagado**, puede realizar los cambios en la línea y seleccionar **Enviar** de nuevo.  
6. Elija el botón **Aceptar**.

## Para aprobar o rechazar una hoja de horas
Una hoja de horas debe haberse enviado para su aprobación para que se pueda usar. Puede aprobar y rechazar las líneas individuales en una hoja de horas o enviarlas de nuevo al emisor para una acción adicional. Una hoja de horas se puede aprobar de dos maneras:

* Un administrador de la hoja de horas puede aprobar en cualquier momento la hoja.
* La persona que se especifica en el campo **Id. usuario aprob. hoja horas** en una ficha de recurso puede aprobar las hojas de horas de ese recurso. Para obtener más información, consulte [Configurar hojas de horas](projects-how-setup-time-sheets.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas del administrador** y luego elija el enlace relacionado.
2. Seleccione una hoja de horas de la lista.  
3. En la página **Parte de horas**, 
    1. Elija la acción **Proceso**, luego elija la acción **Aprobar**.
    2. Elija la acción **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la página **Parte de horas**.
4. Elija el botón **Aceptar**.  
5. También puede elegir la acción **Rechazar** y seguir los pasos del 4 al 5.  

> [!TIP]  
>   Utilice los cuadros informativos **Estado de hoja de horas** y **Resumen real/presupuestado** para obtener un resumen de la información de la hoja de horas.

Una vez aprobada o rechazada una hoja de horas, no se podrá modificar hasta que no se vuelva a abrir. En el procedimiento siguiente se explica cómo volver a abrir una hoja de horas aprobada o rechazada.

## Para reabrir una hoja de horas
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas del administrador** u **Hojas de horas** y luego elija el enlace relacionado.
2. Abra una hoja de horas de la lista.  

    > [!NOTE]  
    >   Puede volver a abrir sólo las líneas con el estado **Aprobado**. No puede volver a abrir solo las líneas con el estado **Impagado**. No puede volver a abrir una hoja de horas si ya se ha registrado.  
3. En la página **Hoja de horas**, elija la acción **Volver a abrir** y, a continuación, **Todas las líneas enviadas** para volver a abrir todas las líneas o la acción **Solo líneas seleccionadas** para volver a abrir únicamente las líneas que están seleccionadas en la página **Hoja de horas**.
4. Elija el botón **Aceptar**. El estado de las líneas de la hoja de horas cambia a **Enviado**.  

## Para ver y aprobar partes de horas por tarea

En una tarea, puede especificar una persona que sea responsable del proyecto. Dicha información está vinculada a las líneas del parte de horas y puede utilizarse para proporcionar una lista de partes de horas que un director del proyecto deberá revisar y aprobar. Por ejemplo, el director del proyecto del equipo puede ser responsable de determinados trabajos de la empresa. En ese caso, el director debe designarse como **Persona responsable** en la tarjeta de trabajo. En esta vista de información del parte de horas, puede ver las tareas del trabajo asociadas a un trabajo y la cantidad de horas empleadas.

> [!NOTE]
> Para poder aprobar los partes de horas en la ventana **Hoja de horas del administrador por trabajo**, primero debe seleccionar una opción **Parte de horas por aprobación de trabajoo** en la página **Configuración de recursos**. Para obtener más información, consulte [Configurar recursos](projects-how-setup-resources.md).

### Para aprobar o rechazar un parte de horas por trabajo

1. En el cuadro **Buscar**, escriba **Hoja de horas del administrador por trabajo** y, a continuación, elija el vínculo relacionado. [!INCLUDE[prod_short](includes/prod_short.md)] muestra una lista de líneas de parte de horas asociadas con los trabajos de los que es responsable.
2. Elija la acción **Aprobar** y, a continuación, elija la acción **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la página **Parte de horas**.

    > [!NOTE]
    > Solo puede aprobar los partes de horas que tengan el estado **Enviado**.

3. Para proporcionar información adicional sobre la aprobación o el rechazo, seleccione la acción **Relacionado** y luego seleccione **Comentarios** y luego **Comentarios de línea** y especifique comentarios.
4. Elija el botón **Aceptar**.

> [!NOTE]
> Una vez aprobada o rechazada una línea del parte de horas por trabajo, no se podrá volver a abrir ni modificar en la ventana **Parte de horas**.

## Para registrar las líneas de hoja de horas en un diario de recursos
Una vez aprobados los movimientos de la hoja de horas de un recurso, puede registrarlas en el diario de recursos correspondiente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después escriba **Diarios del recurso**, y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario recursos**, rellene los campos en una línea según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de recursos, donde puede modificar la información según sea necesario.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. recursos**, en la que muestra el resultado del registro del diario de recursos.

## Para registrar las líneas de hoja de horas en un diario de proyectos
Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlas en el diario de proyecto correspondiente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario proyectos**, rellene los campos en una línea según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de proyectos, donde puede modificar la información según sea necesario.  

    > [!NOTE]  
    >   La información acerca del tipo de trabajo y si el trabajo es facturable debe copiarse de la línea de la hoja de horas. Si es necesario, puede reducir la cantidad de horas cuenta y hacer un registro parcial. Si se reduce la cantidad, la próxima vez que elija la acción **Sugerir líneas de hojas de horas**, la línea creada contendrá la cantidad pendiente de horas.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. proyectos**, en la que muestra el resultado del registro del diario de recursos.

## Para archivar las hojas de horas
Después de registrar las hojas de horas, puede archivarlas para referencia futura. Para que una hoja de horas se pueda archivar, se deben registrar todas las líneas de hoja de horas.

> [!NOTE]  
>   Cuando se archiva una hoja de horas, se elimina de las listas de las páginas **Hojas de horas** y **Hojas de horas del administrador**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.
2. Seleccione la acción **Mover hojas de horas a archivo**.  
3. En la página **Mover hojas de horas a archivo**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.  
4. Para revisar hojas de horas archivadas, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos de hoja de horas** o **Archivos de hoja de horas del administrador** y luego elija el enlace relacionado.

## Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]