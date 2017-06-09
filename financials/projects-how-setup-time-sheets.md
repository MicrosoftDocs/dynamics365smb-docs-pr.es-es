---
title: Configurar hojas de horas | Documentos de Microsoft
description: "Describe cómo preparar el sistema para utilizar las hojas de horas para administrar proyectos."
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
ms.openlocfilehash: aa93e7fe867893c52e3b3973a58ea8a43291c1b1
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-time-sheets"></a>Configuración de hojas de horas
Las hojas de horas de [!INCLUDE[d365fin](includes/d365fin_md.md)] administran el registro de horas en incrementos semanales de siete días. Se usan para realizar el seguimiento del tiempo empleado en proyectos y puede usarlas para efectuar el registro de tiempo simple. Antes de poder usar las hojas de horas, debe especificar cómo desea que se configuren.

Después de haber configurado cómo usará su organización las hojas de horas, puede especificar si se aprueban las hojas de horas y cómo se aprueban. En función de las necesidades de su organización, puede designar:

* Uno o varios usuarios como el administrador y el aprobador de todas las hojas de horas.
* Un aprobador de la hoja de horas de cada recurso.

Cuando haya configurado las hojas de horas, puede crear hojas de horas para recursos, asignarlas a líneas de planificación de proyecto y registrar líneas de hoja de horas. Para obtener más información, vea [Uso de hojas de horas](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Para configurar la información general de las hojas de horas
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración de recursos** y elija el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para el campo **Hojas horas por aprob. proyecto**, seleccione una de las opciones siguientes.

| Opción | Descripción |
| --- | --- |
| **Nunca** |El usuario del campo **Id. usuario aprob. hoja horas:** de la ficha de registro aprueba la hoja de horas. |
| **Siempre** |El uso del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. |
| **Solo máquina** |Si la hoja de horas de la máquina está vinculada a un proyecto, el usuario del campo **Cód. responsable** de la ficha de proyecto aprueba la hoja de horas. Si la hoja de horas de la máquina está vinculada a un recurso, el usuario del campo **Id. usuario aprob. hoja horas** de la ficha de recurso aprueba la hoja de horas. |

## <a name="to-assign-a-time-sheet-administrator"></a>Para asignar un administrador de la hoja de horas
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración usuarios** y elija el vínculo relacionado.  
2. Agregue un nuevo usuario, si la lista de usuarios no incluye a la persona que desea que sea el administrador de la hoja de horas. Para obtener más información, vea la sección "Creación de usuarios" en [Preparación para el negocio](ui-get-ready-business.md).  
3. Seleccione el usuario que sea un administrador de hoja de horas y seleccione la casilla **Admin. hoja horas** .  

**Sugerencia**: Se recomienda que designe a un solo usuario como administrador de hoja de horas para una empresa. En el siguiente procedimiento, configure un propietario y un aprobado de hoja de horas, donde el aprobador se asigne para cada recurso.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Para asignar un propietario y un aprobador de la hoja de horas
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Recursos** y elija el vínculo relacionado.
2. Seleccione el recurso para el que desea definir la capacidad para usar hojas de horas y, a continuación, seleccione la casilla **Usar hoja horas**.  
3. En el campo **Id. usuario prop. hoja horas**, escriba el identificador del propietario de la hoja de horas. El propietario puede especificar el uso de tiempo en una hoja de horas y enviarla para su aprobación. Normalmente, cuando el recurso es una persona, esa persona también es el propietario.  
4. En el campo **Id. usuario aprob. hoja horas**, escriba el identificador del aprobador de la hoja de horas. El aprobador puede aprobar, rechazar o volver a abrir una hoja de horas.  

**Nota**: No se puede cambiar el identificador de aprobador de la hoja de horas si hay hojas de horas que aún no se han procesado y tienen el estado **Enviado** o **Pendiente**.

## <a name="see-also"></a>Consulte también
[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)         
[Ventas](sales-manage-sales.md)      
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

