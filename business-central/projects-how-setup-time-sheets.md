---
title: Configurar partes de horas y su aprobación
description: 'Puede configurar hojas de horas para realizar un seguimiento del tiempo empleado en tareas y proyectos, lo que le ayudará en la administración de proyectos, personal y capacidad'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: edupont
---
# Configuración de hojas de horas

Las hojas de horas de [!INCLUDE[prod_short](includes/prod_short.md)] administran el registro de horas en incrementos semanales de siete días. Puede utilizarlas para realizar el seguimiento del tiempo empleado en proyectos y puede usarlas para efectuar el registro de tiempo simple. Antes de poder utilizar las hojas de horas, debe especificar qué usuarios enviarán las hojas de horas y cómo desea configurar las hojas de horas.  

> [!TIP]
> En [!INCLUDE [prod_short](includes/prod_short.md)], los usuarios de las hojas de horas son *recursos*. De esta forma, puede utilizar hojas de horas para realizar un seguimiento del trabajo de los no empleados, por ejemplo. Para realizar un seguimiento del trabajo de sus propios empleados o para utilizar hojas de horas para realizar un seguimiento de la ausencia de empleados, debe asociar *empleados* con *recursos* en la guía de configuración.  

Opcionalmente, especifique si se aprueban las hojas de horas y cómo. En función de las necesidades de su organización, puede designar:

* Uno o varios usuarios como el administrador y el aprobador de todas las hojas de horas.
* Un aprobador de la hoja de horas de cada recurso.

Cuando haya configurado las hojas de horas, puede crear hojas de horas para recursos, y los recursos pueden registrar líneas de hoja de horas. Opcionalmente, asigne hojas de horas a líneas de planificación de trabajos. Para obtener más información, vea [Uso de hojas de horas](projects-how-use-time-sheets.md).  

## Configurar partes de horas con la guía de configuración asistida

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

A partir del lanzamiento de versiones 2 de 2021, puede utilizar una guía de configuración asistida para ayudarle a configurar los partes de horas.  

> [!TIP]
> Debe habilitar la característica **Actualización de datos de característica: nueva experiencia de parte de horas** en la página [Administración de características](https://businesscentral.dynamics.com/?page=2610) para utilizar esta capacidad.
>
> La misma característica también facilita la administración de partes de horas en un dispositivo móvil.

Abra la guía de configuración asistida **Configurar hojas de tiempo** de la página [Configuración asistida](https://businesscentral.dynamics.com/?page=1801).

La guía de configuración asistida le guía a través de los siguientes pasos:

1. Configurar los participantes en los procesos de parte de horas

    La primera página de la guía muestra el número de usuarios en su [!INCLUDE [prod_short](includes/prod_short.md)]. También muestra otra información obligatoria y opcional.  
2. Especificar el primer día de una semana laboral en esta organización

    El primer día de una semana laboral será el primer día predeterminado para todos los partes de horas.
3. Especificar la persona que administra los partes de horas

    Esta persona puede editar y eliminar todos los partes de horas. Opcionalmente, agregue el mismo rol a otras personas en la página **Configuración de usuario**.
4. Configurar los recursos que usarán los partes de horas y las personas que aprobarán los partes de horas

Al final de la guía de configuración, puede optar por permitir que [!INCLUDE [prod_short](includes/prod_short.md)] cree partes de tiempo basados en su configuración. Vea las nuevas hojas de horas en la página **Hojas de horas**, que puede abrir [aquí](https://businesscentral.dynamics.com/?page=951). Alternativamente, ejecute la guía de configuración asistida nuevamente o complete la configuración manualmente.  

## Configurar partes de horas manualmente

Las siguientes secciones describen cómo configurar los partes de horas si no utiliza la guía de configuración asistida **Configurar partes de horas**.  

### Para configurar la información general de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de recursos** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para el campo **Hojas horas por aprob. proyecto**, seleccione una de las opciones siguientes.

| Opción | Descripción |
| --- | --- |
| **Nunca** |El usuario del campo **Id. usuario aprob. hoja horas:** de la ficha de registro aprueba la hoja de horas. |
| **Siempre** |El uso del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. |
| **Solo máquina** |Si la hoja de horas de la máquina está vinculada a un proyecto, el usuario del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. Si la hoja de horas de la máquina está vinculada a un recurso, el usuario del campo **Id. usuario aprob. hoja horas** de la ficha de recurso aprueba la hoja de horas. |

### Para asignar un administrador de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de usuario** y luego elija el enlace relacionado.  
2. Agregue un nuevo usuario, si la lista de usuarios no incluye a la persona que desea que sea el administrador de la hoja de horas. Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).
3. Seleccione el usuario que sea un administrador de hoja de horas y seleccione la casilla **Admin. hoja horas**.  

> [!TIP]  
> Se recomienda que designe a un solo usuario como administrador de hoja de horas para una empresa. En el siguiente procedimiento, configure un propietario y un aprobado de hoja de horas, donde el aprobador se asigne para cada recurso.  

### Para asignar un propietario y un aprobador de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione el recurso para el que desea definir la capacidad para usar hojas de horas y, a continuación, seleccione la casilla **Usar hoja horas**.  
3. En el campo **Id. usuario prop. hoja horas**, escriba el identificador del propietario de la hoja de horas. El propietario puede especificar el uso de tiempo en una hoja de horas y enviarla para su aprobación. Normalmente, cuando el recurso es una persona, esa persona también es el propietario.  
4. En el campo **Id. usuario aprob. hoja horas**, escriba el identificador del aprobador de la hoja de horas. El aprobador puede aprobar, rechazar o volver a abrir una hoja de horas.  

> [!NOTE]  
> No se puede cambiar el identificador de aprobador de la hoja de horas si hay hojas de horas que aún no se han procesado y tienen el estado **Enviado** o **Pendiente**.

## Consultar la [formación de Microsoft](/training/paths/set-up-jobs-resources/) relacionada

## Consulte también .

[Uso de hojas de horas para proyectos](projects-how-use-time-sheets.md)  
[Cómo crear partes de horas](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrar el consumo o uso para proyectos](projects-how-record-job-usage.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
