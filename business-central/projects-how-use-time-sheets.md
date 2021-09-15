---
title: Trabajar con hojas de horas para proyectos
description: Describe cómo crear una hoja de horas de un proyecto, copiar líneas de planificación en ella, definir los tipos de trabajo, rellenar la hoja de horas y enviarla para su aprobación.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.date: 08/24/2021
ms.author: edupont
ms.openlocfilehash: 02d9536b27290ef27e5954ad6ea9004094e5cfe2
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440646"
---
# <a name="use-time-sheets-for-jobs"></a>Uso de hojas de horas para proyectos

El proceso **Crear hojas de horas** se usa para configurar hojas de horas de un número determinado de periodos o semanas. Debe disponer de permisos para poder crear las hojas de horas.

Puede copiar y usar sus líneas de planificación de proyecto en una hoja de horas. De esa forma, solo debe especificar la información en un lugar para que la información de la línea siempre sea correcta.

Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlos en el diario de proyectos o de recursos correspondiente.

Para poder utilizar las hojas de horas, debe configurar la información general y especificar un administrador y uno o varios aprobadores de hojas de horas. Para obtener más información, consulte [Configurar hojas de horas](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Para crear una hoja de horas

Puede usar el proceso **Crear hojas de horas** para configurar hojas de horas de un número determinado de periodos o semanas. Después, el propietario de la hoja de horas puede abrirla y registrar el tiempo dedicado en una tarea.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.
2. En la página **Lista de hojas de horas**, seleccione la acción **Crear hojas de horas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Los campos **Usar hoja horas** e **Id. usuario prop. hoja horas** deben completarse en la ficha del recurso de la hoja de horas.
4. Elija el botón **Aceptar**.  

Puede ver las hojas de horas creadas en la página **Lista de hojas de horas**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Para copiar líneas de planificación del proyecto en una hoja de horas
El procedimiento siguiente describe cómo agregar rápidamente líneas de planificación del proyecto a una hoja de horas.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. En la página **Lista de parte de horas**, seleccione un parte de horas para periodo de tiempo correspondiente.  
3. Elija la acción **Línea** y luego elija la acción **Crear líneas a partir de la planificación del trabajo**. Cualquier línea de planificación de proyecto del periodo de tiempo de la hoja de horas se copia en la hoja de horas de la persona o equipo en el campo **N.º recurso** en la hoja de horas.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Para definir los tipos de trabajo y agregar uno a una hoja de horas
Puede definir el tipo de trabajo de todas las líneas de la hoja de horas para los proyectos. De esta forma, puede agregar información que necesite para facturar al cliente distintos tipos de trabajo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.   
2. Abra la hoja de horas relevante.
3. Elija el campo **Descripción**.  
4. En la página **Detalle proyecto línea hoja de horas**, elija el campo **Cód. tipo trabajo** y seleccione un tipo de trabajo en la lista, como **Millas**.  
5. Si hay ningún tipos de trabajo, elija la acción **Nuevo**.
6. En la página **Tipos de trabajo**, rellene los campos según sea necesario.
7. Repita el paso 4 para asignar el nuevo tipo de trabajo a la hoja de horas.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Para volver a utilizar las líneas de la hoja de horas en otras hojas de horas
Si la información de la hoja de horas no cambia con el tiempo, puede ahorrar tiempo copiando las líneas del periodo anterior. A continuación, solo especifique el uso del tiempo para el nuevo periodo.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Abra la hoja de horas de un periodo posterior al periodo de una hoja de horas existente con las líneas.  
3. Elija la acción **Línea** y luego elija la acción **Copiar líneas a partir del parte de horas anterior**.

Las líneas se copiarán, incluidos los detalles como el tipo y la descripción. Por ejemplo, si la línea está relacionada con un trabajo, se copiará **Nº proyecto**. Todas las líneas copiadas tienen el estado **Abierto**. Ahora puede modificar las líneas según sea necesario.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Para rellenar una línea de hoja de horas y enviarla para su aprobación
El registro de la hoja de horas se hace en horas, la unidad de medida base estándar para los recursos. De forma predeterminada, una hoja de horas muestra los días de trabajo comunes de lunes a viernes.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas** y luego elija el enlace relacionado.  
2. Seleccione un parte de hojas para el período relevante.
3. Rellene los campos de una línea, que sean necesario. Introduzca el número de horas que ha usado el recurso cada día de la semana.  

    > [!TIP]  
    >   Puede revisar la suma de horas de la hoja de horas que ha introducido en el cuadro informativo **Resumen real/presupuestado**.  
4. Repita el paso 3 para otros tipos de trabajo que realice el recurso.
5. Elija la acción **Proceso** y, a continuación, elija la acción **Enviar** y, después **Todas las líneas abiertas** para enviar todas las líneas o la acción **Solo líneas seleccionadas** para enviar únicamente las líneas que están seleccionadas en la página **Parte de horas**.  

    > [!NOTE]  
    >   Solo puede enviar las líneas de hoja de horas para las que haya especificado tiempo.  
6. Para modificar la información de una línea que se ha definido como **Enviado**, seleccione la línea y, a continuación, elija la acción **Volver a abrir**.

    > [!NOTE]  
    >   Un administrador puede rechazar una línea de hoja de horas que se ha enviado para su aprobación. Si una línea tiene el estado de **Impagado**, puede realizar los cambios en la línea y seleccionar **Enviar** de nuevo.  
7. Elija el botón **Aceptar**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Para aprobar o rechazar una hoja de horas
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

## <a name="to-reopen-a-time-sheet"></a>Para reabrir una hoja de horas
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de horas del administrador** u **Hojas de horas** y luego elija el enlace relacionado.
2. Abra una hoja de horas de la lista.  

    > [!NOTE]  
    >   Puede volver a abrir sólo las líneas con el estado **Aprobado**. No puede volver a abrir solo las líneas con el estado **Impagado**. No puede volver a abrir una hoja de horas si ya se ha registrado.  
3. En la página **Hoja de horas**, elija la acción **Volver a abrir** y, a continuación, **Todas las líneas enviadas** para volver a abrir todas las líneas o la acción **Solo líneas seleccionadas** para volver a abrir únicamente las líneas que están seleccionadas en la página **Hoja de horas**.
4. Elija el botón **Aceptar**. El estado de las líneas de la hoja de horas cambia a **Enviado**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Para ver y aprobar partes de horas por tarea

En una tarea, puede especificar una persona que sea responsable del proyecto. Dicha información está vinculada a las líneas del parte de horas y puede utilizarse para proporcionar una lista de partes de horas que un director del proyecto deberá revisar y aprobar. Por ejemplo, el director del proyecto del equipo puede ser responsable de determinados trabajos de la empresa. En ese caso, el director debe designarse como **Persona responsable** en la tarjeta de trabajo. En esta vista de información del parte de horas, puede ver las tareas del trabajo asociadas a un trabajo y la cantidad de horas empleadas.

> [!NOTE]
> Para poder aprobar los partes de horas en la ventana **Hoja de horas del administrador por trabajo**, primero debe seleccionar una opción **Parte de horas por aprobación de trabajoo** en la página **Configuración de recursos**. Para obtener más información, consulte [Configurar recursos](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Para aprobar o rechazar un parte de horas por trabajo

1. En el cuadro **Buscar**, escriba **Hoja de horas del administrador por trabajo** y, a continuación, elija el vínculo relacionado. [!INCLUDE[prod_short](includes/prod_short.md)] muestra una lista de líneas de parte de horas asociadas con los trabajos de los que es responsable.
2. Elija la acción **Aprobar** y, a continuación, elija la acción **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la página **Parte de horas**.

    > [!NOTE]
    > Solo puede aprobar los partes de horas que tengan el estado **Enviado**.

3. Para proporcionar información adicional sobre la aprobación o el rechazo, seleccione la acción **Relacionado** y luego seleccione **Comentarios** y luego **Comentarios de línea** y especifique comentarios.
4. Elija el botón **Aceptar**.

> [!NOTE]
> Una vez aprobada o rechazada una línea del parte de horas por trabajo, no se podrá volver a abrir ni modificar en la ventana **Parte de horas**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Para registrar las líneas de hoja de horas en un diario de recursos
Una vez aprobados los movimientos de la hoja de horas de un recurso, puede registrarlas en el diario de recursos correspondiente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después escriba **Diarios del recurso**, y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario recursos**, rellene los campos en una línea según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de recursos, donde puede modificar la información según sea necesario.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. recursos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Para registrar las líneas de hoja de horas en un diario de proyectos
Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlas en el diario de proyecto correspondiente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. En la página **Proponer líneas diario proyectos**, rellene los campos en una línea según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de proyectos, donde puede modificar la información según sea necesario.  

    > [!NOTE]  
    >   La información acerca del tipo de trabajo y si el trabajo es facturable debe copiarse de la línea de la hoja de horas. Si es necesario, puede reducir la cantidad de horas cuenta y hacer un registro parcial. Si se reduce la cantidad, la próxima vez que elija la acción **Sugerir líneas de hojas de horas**, la línea creada contendrá la cantidad pendiente de horas.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la página **Movs. proyectos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="to-archive-time-sheets"></a>Para archivar las hojas de horas
Después de registrar las hojas de horas, puede archivarlas para referencia futura. Para que una hoja de horas se pueda archivar, se deben registrar todas las líneas de hoja de horas.

> [!NOTE]  
>   Cuando se archiva una hoja de horas, se elimina de las listas de las páginas **Hojas de horas** y **Hojas de horas del administrador**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Después, escriba **Parte de horas** y luego elija el enlace relacionado.
2. Seleccione la acción **Mover hojas de horas a archivo**.  
3. En la página **Mover hojas de horas a archivo**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.  
4. Para revisar hojas de horas archivadas, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Archivos de hoja de horas** o **Archivos de hoja de horas del administrador** y luego elija el enlace relacionado.

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]