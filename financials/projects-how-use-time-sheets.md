---
title: Usar hojas de horas para proyectos| Documentos de Microsoft
description: "Describe cómo utilizar las hojas de horas para administrar proyectos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1796436b964f5e1e4220f885e97713848d94bdfb
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-time-sheets-for-jobs"></a>Uso de hojas de horas para proyectos
El proceso **Crear hojas de horas** se usa para configurar hojas de horas de un número determinado de periodos o semanas. Debe disponer de permisos para poder crear las hojas de horas.

Puede copiar y usar sus líneas de planificación de proyecto en una hoja de horas. De esa forma, solo debe especificar la información en un lugar para que la información de la línea siempre sea correcta.

Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlos en el diario de proyectos o de recursos correspondiente.

Para poder utilizar las hojas de horas, debe configurar la información general y especificar un administrador y uno o varios aprobadores de hojas de horas. Para obtener más información, vea [Configuración de hojas de horas](projects-how-setup-time-sheets.md).

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-create-a-time-sheet"></a>Para crear una hoja de horas
Puede usar el proceso **Crear hojas de horas** para configurar hojas de horas de un número determinado de periodos o semanas. Después, el propietario de la hoja de horas puede abrirla y registrar el tiempo dedicado en una tarea.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas** y elija el vínculo relacionado.
2. En la ventana **Lista de hojas de horas**, seleccione la acción **Crear hojas de horas**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Nota**: Los campos **Usar hoja horas** e **Id. usuario prop. hoja horas:** deben completarse en la ficha del recurso de la hoja de horas.

1. Elija el botón **Aceptar**.  

Puede ver las hojas de horas creadas en la ventana **Lista de hojas de horas**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Para copiar líneas de planificación del proyecto en una hoja de horas
El procedimiento siguiente describe cómo agregar rápidamente líneas de planificación del proyecto a una hoja de horas.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas** y elija el vínculo relacionado.  
2. En la ventana **Lista de hojas de horas**, seleccione una hoja de horas del periodo de tiempo correspondiente y, a continuación, elija la acción **Editar hoja de horas**.  
3. Elija la acción **Crear líneas de planificación de proyecto**. Cualquier línea de planificación de proyecto del periodo de tiempo de la hoja de horas se copia en la hoja de horas de la persona o equipo en el campo **N.º recurso** en la hoja de horas.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Para definir los tipos de trabajo y agregar uno a una hoja de horas
Puede definir el tipo de trabajo de todas las líneas de la hoja de horas para los proyectos. De esta forma, puede agregar información que necesite para facturar al cliente distintos tipos de trabajo.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas** y elija el vínculo relacionado.   
2. Abra la hoja de horas relevante.
3. Elija el campo **Descripción**.  
4. En la ventana **Detalle proyecto línea hoja de horas**, elija el campo **Cód. tipo trabajo** y seleccione un tipo de trabajo en la lista, como **Millas**.  
5. Si hay ningún tipos de trabajo, elija la acción **Nuevo**.
6. En la ventana **Tipos de trabajo**, rellene los campos según sea necesario.
7. Repita el paso 4 para asignar el nuevo tipo de trabajo a la hoja de horas.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Para volver a utilizar las líneas de la hoja de horas en otras hojas de horas
Si la información de la hoja de horas no cambia con el tiempo, puede ahorrar tiempo copiando las líneas del periodo anterior. A continuación, solo especifique el uso del tiempo para el nuevo periodo.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas** y elija el vínculo relacionado.  
2. Abra la hoja de horas de un periodo posterior al periodo de una hoja de horas existente con las líneas.  
3. Elija la acción **Copiar líneas desde hoja de horas anterior**.

Las líneas se copiarán, incluidos los detalles como el tipo y la descripción. Por ejemplo, si la línea está relacionada con un proyecto, **Nº proyecto** es el campo que se copia. Todas las líneas copiadas tienen el estado **Abierto**. Ahora puede modificar las líneas según sea necesario.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Para rellenar una línea de hoja de horas y enviarla para su aprobación
El registro de la hoja de horas se hace en horas, la unidad de medida base estándar para los recursos. De forma predeterminada, una hoja de horas muestra los días de trabajo comunes de lunes a viernes.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas** y elija el vínculo relacionado.  
2. Seleccione una hoja de horas del periodo de tiempo correspondiente y, a continuación, elija la acción **Editar hoja de horas**.  
3. Rellene los campos de una línea, que sean necesario. Introduzca el número de horas que ha usado el recurso cada día de la semana.

    **Sugerencia**: Puede revisar la suma de horas de la hoja de horas que ha introducido en el cuadro informativo **Resumen real/presupuestado**.  
4. Repita el paso 3 para otros tipos de trabajo que realice el recurso.
5. Elija la acción **Enviar** y, a continuación, elija la acción **Todas las líneas abiertas** para enviar todas las líneas o la acción **Solo líneas seleccionadas** para enviar únicamente las líneas que están seleccionadas en la ventana **Hoja de horas**.  

    **Nota**: Solo puede enviar las líneas de hoja de horas para las que haya especificado tiempo.  
6. Para modificar la información de una línea que se ha definido como **Enviado**, seleccione la línea y, a continuación, elija la acción **Volver a abrir**.

    **Nota**: Un administrador puede rechazar una línea de hoja de horas que se ha enviado para su aprobación. Si una línea tiene el estado de **Impagado**, puede realizar los cambios en la línea y seleccionar **Enviar** de nuevo.  
7. Elija el botón **Aceptar**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Para aprobar o rechazar una hoja de horas
Una hoja de horas debe haberse enviado para su aprobación para que se pueda usar. Puede aprobar y rechazar las líneas individuales en una hoja de horas o enviarlas de nuevo al emisor para una acción adicional. Una hoja de horas se puede aprobar de dos maneras:

* Un administrador de la hoja de horas puede aprobar en cualquier momento la hoja.
* La persona que se especifica en el campo **Id. usuario aprob. hoja horas** en una ficha de recurso puede aprobar las hojas de horas de ese recurso. Para obtener más información, vea [Configuración de hojas de horas](projects-how-setup-time-sheets.md).

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas del administrador** y elija el vínculo relacionado.
2. Seleccione una hoja de horas de la lista.  
3. En la ventana **Hoja de horas**, elija la acción **Aprobar** y, a continuación, **Todas las líneas enviadas** para aprobar todas las líneas o la acción **Solo líneas seleccionadas** para aprobar únicamente las líneas que están seleccionadas en la ventana **Hoja de horas**.
4. Elija el botón **Aceptar**.  
5. También puede elegir la acción **Rechazar** y seguir los pasos del 4 al 5.  

**Sugerencia**: Utilice los cuadros informativos **Estado de hoja de horas** y **Resumen real/presupuestado** para obtener un resumen de la información de la hoja de horas.

Una vez aprobada o rechazada una hoja de horas, no se podrá modificar hasta que no se vuelva a abrir. En el procedimiento siguiente se explica cómo volver a abrir una hoja de horas aprobada o rechazada.

## <a name="to-reopen-a-time-sheet"></a>Para reabrir una hoja de horas
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Hojas de horas del administrador** u **Hojas de horas** y elija el vínculo relacionado.
2. Abra una hoja de horas de la lista.  

    **Nota**: Puede volver a abrir solo las líneas con el estado **Aprobado**. No puede volver a abrir solo las líneas con el estado **Impagado**. No puede volver a abrir una hoja de horas si ya se ha registrado.  
3. En la ventana **Hoja de horas**, elija la acción **Volver** y, a continuación, **Todas las líneas enviadas** para volver a abrir todas las líneas o la acción **Solo líneas seleccionadas** para volver a abrir únicamente las líneas que están seleccionadas en la ventana **Hoja de horas**.
4. Elija el botón **Aceptar**. El estado de las líneas de la hoja de horas cambia a **Enviado**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Para registrar las líneas de hoja de horas en un diario de recursos
Una vez aprobados los movimientos de la hoja de horas de un recurso, puede registrarlas en el diario de recursos correspondiente.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Diario recurso** y elija el vínculo relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. Rellene los campos según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de recursos, donde puede modificar la información según sea necesario.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la ventana **Movs. recursos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Para registrar las líneas de hoja de horas en un diario de proyectos
Una vez aprobados los movimientos de la hoja de horas de un proyecto, puede registrarlas en el diario de proyecto correspondiente.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Diario proyecto** y elija el vínculo relacionado.  
2. Elija la acción **Sugerir líneas de hojas de horas**.  
3. Rellene los campos según sea necesario.  
4. Elija el botón **Aceptar**. Los movimientos de uso se crean en el diario de proyectos, donde puede modificar la información según sea necesario.  

    **Notas**: La información acerca del tipo de trabajo y si el trabajo es facturable debe copiarse de la línea de la hoja de horas. Si es necesario, puede reducir la cantidad de horas cuenta y hacer un registro parcial. Si se reduce la cantidad, la próxima vez que elija la acción **Sugerir líneas de hojas de horas**, la línea creada contendrá la cantidad pendiente de horas.  
5. Seleccione la acción **Registrar**.  
6. Para comprobar el registro, elija la acción **Movimientos**. Se abre la ventana **Movs. proyectos**, en la que muestra el resultado del registro del diario de recursos.

## <a name="to-archive-time-sheets"></a>Para archivar las hojas de horas
Después de registrar las hojas de horas, puede archivarlas para referencia futura. Para que una hoja de horas se pueda archivar, se deben registrar todas las líneas de hoja de horas.

**Nota**: Cuando se archiva una hoja de horas, se elimina de las listas de las ventanas **Hojas de horas** y **Hojas de horas del administrador**.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Mover hojas de horas a archivo** y elija el vínculo relacionado.  
2. Rellene los campos según sea necesario y, a continuación, haga clic en el botón **Aceptar**.  
3. Para revisar las hojas de horas archivadas, en la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Archivos de hoja de horas** u **Hojas de horas del administrador** y elija el vínculo relacionado.

## <a name="see-also"></a>Consulte también
[Administración de proyectos](projects-manage-projects.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)    
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)     
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

