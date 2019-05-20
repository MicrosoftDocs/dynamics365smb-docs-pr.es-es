---
title: Realizar el seguimiento de la actividad de usuario en un registro de cambios | Documentos de Microsoft
description: Puede activar el registro de usuario para tener un historial de los cambios realizados en los datos de las tablas de las que se hace el seguimiento.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240446"
---
# <a name="auditing-changes-in-business-central"></a>Auditar cambios en Business Central

Puede habilitar el registro de cambios en [!INCLUDE[d365fin](includes/d365fin_md.md)] para tener un historial de actividades. El registro se basa en los cambios realizados en los datos en las tablas que se siguen. En la página **Cambiar entradas del registro**, las entradas se ordenan cronológicamente y se muestran los cambios realizados a los campos de las tablas especificadas. El registro de cambios recopila todos los cambios que se han realizado en la tabla.

> [!Important]
> Los cambios de un usuario no son visibles en **Cambiar entradas del registro** hasta que se reinicia la sesión del usuario, lo que ocurre en los siguientes casos:
<br />
> * La sesión ha caducado y se ha actualizado.
> * El usuario seleccionó otra empresa o área de trabajo.
> * El usuario ha salido y ha vuelto a entrar.

## <a name="working-with-the-change-log"></a>Trabajar con el registro de cambios

Un problema habitual en muchos sistemas financieros es localizar el origen de errores y modificaciones en los datos. Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad. El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos. Debe especificar para cada tabla y campo lo que desea que el sistema registre y, a continuación, debe activar el registro de cambios.  

El registro de cambios se activa y desactiva en la página **Config. log cambio**. Si un usuario activa o desactiva el registro de cambios, se registra esta actividad, de modo que siempre puede ver qué usuario ha activado o reactivado el registro de cambios.

En la página **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[d365fin](includes/d365fin_md.md)] también realiza el seguimiento de varias tablas del sistema.

Después de haber configurado el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la página **Movs. registro cambios**. Si desea eliminar movimientos, puede hacerlo en la página **Eliminar movs. reg. de cambios**, donde puede definir filtros basados en fechas y horas.  

## <a name="see-also"></a>Consulte también
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Ordenación](ui-sorting.md)  
[Usar la opción Dígame para encontrar características e información](ui-search.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
