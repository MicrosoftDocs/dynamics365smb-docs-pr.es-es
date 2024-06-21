---
title: Configurar partes de horas y su aprobación
description: Aprenda a usar partes de horas para realizar el seguimiento del tiempo de proyectos y recursos.
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Configurar partes de horas

Las hojas de horas de [!INCLUDE[prod_short](includes/prod_short.md)] administran el registro de horas en incrementos semanales de siete días. Puede utilizarlas para realizar el seguimiento del tiempo empleado en proyectos y puede usarlas para efectuar el registro de tiempo simple. Antes de poder utilizar los partes de horas, debe especificar qué usuarios enviarán los partes de horas y cómo desea configurar los partes de horas.  

> [!TIP]
> La gente que usa partes de horas son *recursos*. Por ejemplo, puede utilizar hojas de horas para realizar un seguimiento del trabajo de los no empleados. Para realizar un seguimiento del trabajo de empleados o para utilizar hojas de horas para realizar un seguimiento de la ausencia de empleados, debe asociar empleados con recursos. Hay una guía de configuración asistida que puede ayudarle a hacerlo. Para más información sobre la guía, vaya a [Configurar partes de horas con la guía de configuración asistida](#set-up-time-sheets-with-the-assisted-setup-guide).  

Opcionalmente, especifique si se aprueban los partes de horas y cómo. En función de las necesidades de su organización, puede designar:

* Uno o varios usuarios como el administrador y el aprobador de todas las hojas de horas.
* Un aprobador de la hoja de horas de cada recurso.

Cuando haya configurado las hojas de horas, puede crear hojas de horas para recursos, y los recursos pueden registrar líneas de hoja de horas. Opcionalmente, asigne hojas de horas a líneas de planificación de proyectos. Para obtener más información, vaya a [Usar partes de horas](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Configurar partes de horas con la guía de configuración asistida

Una guía de configuración asistida puede ayudarle a configurar partes de horas.  

> [!TIP]
> Si tiene una versión anterior al lanzamiento de versiones 1 de 2023 (v22), debe habilitar la característica **Actualización de datos de característica: nueva experiencia de parte de horas** en la página [Administración de características](https://businesscentral.dynamics.com/?page=2610) para utilizar esta capacidad.
>
> Esta configuración también le permite usar partes de horas en dispositivos móviles.

Abra la guía de configuración asistida **Configurar hojas de tiempo** de la página [Configuración asistida](https://businesscentral.dynamics.com/?page=1801).

La guía de configuración asistida le guía a través de los siguientes pasos:

1. Configurar los participantes en los procesos de parte de horas.

    La primera página de la guía muestra el número de usuarios en su [!INCLUDE [prod_short](includes/prod_short.md)]. También muestra otra información obligatoria y opcional.  
2. Especificar el primer día de una semana laboral en esta organización.

    El primer día de una semana laboral es el primer día predeterminado para todos los partes de horas.
3. Especificar la persona que administra los partes de horas.

    Esta persona puede editar y eliminar todos los partes de horas. Opcionalmente, agregue el mismo rol a otras personas en la página **Configuración de usuario**.
4. Configurar los recursos que usarán los partes de horas y las personas que aprobarán los partes de horas.

Al final de la guía de configuración, puede optar por permitir que [!INCLUDE [prod_short](includes/prod_short.md)] cree partes de tiempo basados en su configuración. Vea las nuevas hojas de horas en la página **Hojas de horas**, que puede abrir [aquí](https://businesscentral.dynamics.com/?page=951). Alternativamente, ejecute la guía de configuración asistida nuevamente o complete la configuración manualmente.

> [!IMPORTANT]
> Si está utilizando el primer lanzamiento de versiones de 2023 (v22) o posterior, para asegurarse de poder administrar hojas de horas en dispositivos móviles, debe activar manualmente la opción **Utilice la nueva experiencia de parte de horas** para la configuración del parte de horas, como se describe en el siguiente procedimiento.

## <a name="set-up-time-sheets-manually"></a>Configurar partes de horas manualmente

Las siguientes secciones describen cómo configurar los partes de horas si no utiliza la guía de configuración asistida **Configurar partes de horas**.  

### <a name="set-up-general-information-for-time-sheets-manually"></a>Configurar la información general de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Configuración de recursos** y luego elija el enlace relacionado.  
1. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Si está utilizando el primer lanzamiento de versiones de 2023 (v22) o posterior, para asegurarse de poder administrar partes de horas en dispositivos móviles, active la opción **Utilice la nueva experiencia de parte de horas**.
1. Para el campo **Hojas horas por aprob. proyecto**, seleccione una de las opciones siguientes.

| Opción | Descripción |
| --- | --- |
| **Nunca** |El usuario del campo **Id. usuario aprob. hoja horas:** de la ficha de registro aprueba la hoja de horas. |
| **Siempre** |El uso del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. |
| **Solo máquina** |Si la hoja de horas de la máquina está vinculada a un proyecto, el usuario del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. Si la hoja de horas de la máquina está vinculada a un recurso, el usuario del campo **Id. usuario aprob. hoja horas** de la ficha de recurso aprueba la hoja de horas. |

### <a name="assign-a-time-sheet-administrator-manually"></a>Asignar un administrador de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de usuario** y luego elija el enlace relacionado.  
2. Seleccione el usuario que será el administrador de partes de horas y seleccione la casilla **Admin. partes de horas**.  

> [!TIP]  
> Recomendamos que designe a un solo usuario como administrador de hoja de horas para una empresa. En el siguiente procedimiento, configure un propietario y un aprobado de hoja de horas, donde el aprobador se asigne para cada recurso.  

### <a name="assign-a-time-sheets-owner-and-approver-manually"></a>Asignar un propietario y un aprobador de los partes de horas manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione el recurso para el que desea definir la capacidad para usar hojas de horas y, a continuación, seleccione la casilla **Usar partes de horas**.  
3. En el campo **Id. usuario prop. hoja horas**, escriba el identificador del propietario de la hoja de horas. El propietario puede especificar el uso de tiempo en una hoja de horas y enviarla para su aprobación. Normalmente, cuando el recurso es una persona, esa persona también es el propietario.  
4. En el campo **Id. usuario aprob. hoja horas**, escriba el identificador del aprobador de la hoja de horas. El aprobador puede aprobar, rechazar o volver a abrir una hoja de horas.  

> [!NOTE]  
> No se puede cambiar el identificador de aprobador del parte de horas si hay hojas de horas que aún no se han procesado y tienen el estado **Enviado** o **Pendiente**.

## <a name="see-also"></a>Consulte también .

[Uso de hojas de horas para proyectos](projects-how-use-time-sheets.md)  
[Cómo crear partes de horas](projects-how-use-time-sheets.md#create-time-sheets)  
[Registrar el consumo o uso para proyectos](projects-how-record-job-usage.md)  
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
