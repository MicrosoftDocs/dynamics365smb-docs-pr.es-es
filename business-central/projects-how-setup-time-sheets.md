---
title: Configurar hojas de horas y su aprobación | Documentos de Microsoft
description: Puede configurar hojas de horas para realizar un seguimiento del tiempo empleado en proyectos y el uso recursos, lo que le ayudará en la administración de proyectos, personal y capacidad
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 057497cfee69ed91c5d37828ea290749585f93d8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805882"
---
# <a name="set-up-time-sheets"></a>Configuración de hojas de horas
Las hojas de horas de [!INCLUDE[d365fin](includes/d365fin_md.md)] administran el registro de horas en incrementos semanales de siete días. Se usan para realizar el seguimiento del tiempo empleado en proyectos y puede usarlas para efectuar el registro de tiempo simple. Antes de poder usar las hojas de horas, debe especificar cómo desea que se configuren.

Después de haber configurado cómo usará su organización las hojas de horas, puede especificar si se aprueban las hojas de horas y cómo se aprueban. En función de las necesidades de su organización, puede designar:

* Uno o varios usuarios como el administrador y el aprobador de todas las hojas de horas.
* Un aprobador de la hoja de horas de cada recurso.

Cuando haya configurado las hojas de horas, puede crear hojas de horas para recursos, asignarlas a líneas de planificación de proyecto y registrar líneas de hoja de horas. Para obtener más información, vea [Uso de hojas de horas](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Para configurar la información general de las hojas de horas
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de recursos** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para el campo **Hojas horas por aprob. proyecto**, seleccione una de las opciones siguientes.

| Opción | Descripción |
| --- | --- |
| **Nunca** |El usuario del campo **Id. usuario aprob. hoja horas:** de la ficha de registro aprueba la hoja de horas. |
| **Siempre** |El uso del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. |
| **Solo máquina** |Si la hoja de horas de la máquina está vinculada a un proyecto, el usuario del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. Si la hoja de horas de la máquina está vinculada a un recurso, el usuario del campo **Id. usuario aprob. hoja horas** de la ficha de recurso aprueba la hoja de horas. |

## <a name="to-assign-a-time-sheet-administrator"></a>Para asignar un administrador de la hoja de horas
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración del usuario** y luego elija el enlace relacionado.  
2. Agregue un nuevo usuario, si la lista de usuarios no incluye a la persona que desea que sea el administrador de la hoja de horas. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).
3. Seleccione el usuario que sea un administrador de hoja de horas y seleccione la casilla **Admin. hoja horas**.  

> [!TIP]  
>   Se recomienda que designe a un solo usuario como administrador de hoja de horas para una empresa. En el siguiente procedimiento, configure un propietario y un aprobado de hoja de horas, donde el aprobador se asigne para cada recurso.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Para asignar un propietario y un aprobador de la hoja de horas
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione el recurso para el que desea definir la capacidad para usar hojas de horas y, a continuación, seleccione la casilla **Usar hoja horas**.  
3. En el campo **Id. usuario prop. hoja horas**, escriba el identificador del propietario de la hoja de horas. El propietario puede especificar el uso de tiempo en una hoja de horas y enviarla para su aprobación. Normalmente, cuando el recurso es una persona, esa persona también es el propietario.  
4. En el campo **Id. usuario aprob. hoja horas**, escriba el identificador del aprobador de la hoja de horas. El aprobador puede aprobar, rechazar o volver a abrir una hoja de horas.  

> [!NOTE]  
>   No se puede cambiar el identificador de aprobador de la hoja de horas si hay hojas de horas que aún no se han procesado y tienen el estado **Enviado** o **Pendiente**.

## <a name="see-also"></a>Consulte también
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
