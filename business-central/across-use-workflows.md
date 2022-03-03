---
title: Uso de flujos de trabajo
description: Puede configurar y utilizar flujos de trabajo que conecten tareas de procesos empresariales como la publicación automática o la solicitud y concesión de aprobación para nuevos registros.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 2cbf60577e7c0c4f95fcb623fb448f8cb5bd7960
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138705"
---
# <a name="using-workflows"></a>Uso de flujos de trabajo

Un flujo de trabajo es una secuencia de tareas que se desencadenan por una acción, una condición o una regla. Los flujos de trabajo generalmente se implementan para integrar la lógica empresarial a una organización, como la separación de funciones, unificar procesos o aumentar la confianza y las responsabilidades.  

Los flujos de trabajo están diseñados para crear solicitudes de aprobación de un nuevo valor manteniendo el valor anterior en caso de que la solicitud no sea aprobada. El nuevo valor no se implementará hasta que se apruebe la última solicitud.  

La lógica empresarial podría ser la aprobación de:

- Nuevos datos maestros como cuentas de mayor, clientes, proveedores o artículos
- Cambios en los campos de los registros existentes que contienen información confidencial, como **Cód. cuenta banco proveedor** o **Límite crédito del cliente**
- Cambios en los campos de los registros existentes que contienen información comercial crítica, como **Precios de venta de artículos**
- Nuevos usuarios o cambios en los permisos de los usuarios
- Documentos de compras
- Documentos de venta
- Documentos entrantes
- Diarios financieros antes de registrarlos

La siguiente ilustración muestra un ejemplo de un flujo de trabajo con aprobación secuencial desencadenada por un usuario. Al desencadenar el flujo de trabajo, se crea una solicitud de aprobación para el primer aprobador.  

![Ilustración de un flujo de trabajo con aprobación secuencial.](media/Workflows/approval-flow.png)

En este ejemplo, la solicitud debe ser aprobada por el primer aprobador antes de que la solicitud se envíe al siguiente aprobador. Si la solicitud no es aprobada por el primer aprobador, la solicitud nunca pasará al siguiente aprobador.  

La ruta tomada desde el desencadenamiento inicial del flujo de trabajo puede variar según la naturaleza de la aprobación.  

La siguiente ilustración muestra una aprobación paralela que es desencadenada por el usuario. Al activar el flujo de trabajo, se envía una solicitud de aprobación a todos los aprobadores simultáneamente.  

![Ilustración de un flujo de trabajo con aprobación paralela.](media/Workflows/approval-flow-2.png)

Sin embargo, el flujo de trabajo no se aprueba hasta que los aprobadores hayan aprobado todas las solicitudes, como se muestra en la siguiente ilustración:  

![Ilustración de un flujo de trabajo rechazado con aprobación paralela.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> No es posible crear un flujo de trabajo con varios aprobadores y esperar que se apruebe todo el flujo de trabajo después de que se haya aprobado la primera solicitud. Todas las solicitudes deben aprobarse para que se apruebe el flujo de trabajo.

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. También es posible crear el mismo flujo de trabajo más de una vez. Cada flujo de trabajo desencadenado por un evento utilizando diferentes filtros. Esto es útil si una solicitud de aprobación en un departamento debe ser aprobada por un aprobador, mientras que las solicitudes de aprobación en otros departamentos deben ser aprobadas por otro aprobador. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

 Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo, crear los flujos de trabajo, potencialmente precedidos por personalización del código y especificar cómo reciben notificaciones los usuarios. Para obtener más información, consulte [Configurar flujos de trabajo](across-set-up-workflows.md).  

> [!NOTE]  
> Los pasos habituales del flujo de trabajo están relacionados con usuarios que solicitan aprobación de tareas y aprobadores que aceptan o rechazan las solicitudes de aprobación. Por tanto, muchos temas sobre cómo utilizar los flujos de trabajo hacen referencia a las aprobaciones.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Establecer un flujo de trabajo para comenzar cuando se produzca el primer evento de punto de entrada.|[Activar flujos de trabajo](across-how-to-enable-workflows.md)|  
|Solicitar aprobación de una tarea como aprobador, aceptar, rechazar o delegar aprobaciones, y enviar o ver notificaciones de aprobación.|[Usar flujos de trabajo de aprobación del producto](across-how-use-approval-workflows.md)|  
|Cree pasos de flujo de trabajo que restrinjan el uso de cierto tipo de registros antes de producirse un determinado evento, por ejemplo que el registro se apruebe.|[Restringir y permitir el uso de un registro](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Ver los casos del paso del flujo de trabajo con estado de completado.|[Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md)|  
|Eliminar un flujo de trabajo que está seguro que no se utilizará más.|[Eliminar flujos de trabajo](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Consulte también  
[Configuración de flujos de trabajo](across-set-up-workflows.md)   
[Flujo de trabajo](across-workflow.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]