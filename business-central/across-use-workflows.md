---
title: Usar flujos de trabajo de aprobación
description: Puede configurar y utilizar flujos de trabajo que conecten tareas de procesos empresariales como la publicación automática o la solicitud y concesión de aprobación para nuevos registros.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Usar flujos de trabajo de aprobación del producto

Un flujo de trabajo es una secuencia de tareas que se desencadenan por una acción, una condición o una regla. Los flujos de trabajo generalmente se implementan para integrar la lógica empresarial a una organización, como la separación de funciones, unificar procesos o aplicar procedimientos recomendados.

Los flujos de trabajo pueden estar diseñados para crear solicitudes de aprobación de un campo de cambio de registro manteniendo los datos anteriores en caso de que la solicitud no se apruebe. El nuevo valor no se implementará hasta que se apruebe la última solicitud.

La lógica empresarial podría ser la aprobación de:

- Nuevos datos maestros como cuentas de contabilidad general (CG), clientes, proveedores o artículos.
- Cambios en los campos de los registros existentes que contienen información confidencial, como **Cód. cuenta banco proveedor** o **Límite crédito del cliente**.
- Cambios en los campos de los registros existentes que contienen información comercial crítica, como **Precios de venta de artículos**.
- Nuevos usuarios o cambios en los permisos de los usuarios.
- Documentos de compras.
- Documentos de venta.
- Documentos entrantes.
- Diarios financieros antes de registrarlos.

La siguiente ilustración es un ejemplo de un flujo de trabajo con aprobación secuencial desencadenada por un usuario. Al desencadenar el flujo de trabajo, se crea una solicitud de aprobación para el primer aprobador.  

![Ilustración de un flujo de trabajo con aprobación secuencial.](media/Workflows/approval-flow.png)

En la ilustración anterior se ve cómo la solicitud debe ser aprobada por el primer aprobador antes de su envío al siguiente. Si la solicitud no es aprobada por el primer aprobador, la solicitud nunca pasará al siguiente.

La ruta tomada desde el desencadenamiento inicial del flujo de trabajo puede variar según la naturaleza de la aprobación.  

La siguiente ilustración muestra una aprobación paralela que es desencadenada por el usuario. Una aprobación paralela significa que se envía la solicitud de aprobación a todos los aprobadores simultáneamente.  

![Ilustración de un flujo de trabajo con aprobación paralela.](media/Workflows/approval-flow-2.png)

Sin embargo, el flujo de trabajo no se concluye hasta que se hayan aprobado todas las solicitudes, como se muestra en la siguiente ilustración:  

![Ilustración de un flujo de trabajo rechazado con aprobación paralela.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Para un flujo de trabajo con múltiples aprobadores, todos los aprobadores deben aprobar cada paso antes de que el flujo de trabajo pueda avanzar al siguiente evento. La aprobación de un solo aprobador no hará avanzar el flujo de trabajo.

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. También es posible crear el mismo flujo de trabajo más de una vez. Cada flujo de trabajo se puede desencadenar por un evento utilizando diferentes filtros. Esto es útil si una solicitud de aprobación para un departamento debe ser aprobada por un aprobador, mientras que las solicitudes para otros departamentos deben ser aprobadas por un aprobador diferente. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

Antes de empezar a utilizar flujos de trabajo, debe configurar usuarios de flujo de trabajo, crear los flujos de trabajo (potencialmente precedidos por personalización del código) y especificar cómo reciben notificaciones los usuarios. Obtenga más información en [Configurar flujos de trabajo](across-set-up-workflows.md).

> [!NOTE]  
> Los pasos típicos del flujo de trabajo implican que los usuarios soliciten la aprobación de las tareas y que los aprobadores acepten o rechacen las solicitudes de aprobación. Por tanto, muchos temas sobre cómo utilizar los flujos de trabajo hacen referencia a las aprobaciones.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.  

| **Para** | **Vea** |
|--|--|
| Establecer un flujo de trabajo de aprobación para comenzar cuando se produzca el primer evento de punto de entrada. | [Habilitar flujos de trabajo de aprobación](across-how-to-enable-workflows.md) |
| Solicitar aprobación de una tarea como aprobador, aceptar, rechazar o delegar aprobaciones, y enviar o ver notificaciones de aprobación. | [Cómo usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md) |
| Cree pasos de flujo de trabajo que restrinjan el uso de cierto tipo de registros antes de producirse un determinado evento, por ejemplo aprobación del registro. | [Restringir y permitir el uso de un registro](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Ver los casos del paso del flujo de trabajo con estado de **Completado**. | [Ver instancias de paso de flujo de trabajo archivadas](across-how-to-view-archived-workflow-step-instances.md) |
| Eliminar un flujo de trabajo de aprobación que está seguro de que no se utilizará más. | [Eliminar flujos de trabajo de aprobación](across-how-to-delete-workflows.md) |

## Consulte también .

[Configurar flujos de trabajo de aprobación](across-set-up-workflows.md)  
[Flujo de trabajo](across-workflow.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
