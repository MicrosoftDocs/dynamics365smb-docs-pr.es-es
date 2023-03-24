---
title: Programar proyectos para que se ejecuten automáticamente
description: Las tareas programadas son administradas por la cola de proyecto. Estos proyectos ejecutan informes y codeunits. Puede configurar proyectos para que se ejecuten una vez o de manera periódica.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Uso de colas de proyectos para programar tareas

La página Entradas de colas de proyectos permiten a los usuarios programar y ejecutar informes y codeunits específicos. Puede configurar proyectos para que se ejecuten una vez o de manera periódica. Por ejemplo, es posible que desee ejecutar el informe **Vendedor * Estadísticas de ventas** semanalmente para realizar un seguimiento de las ventas por vendedor cada semana o ejecutar la codeunit **Solicitudes de aprobación de delegados** diariamente, para evitar que los documentos se acumulen.

La página **Entradas de cola de proyectos** enumera todos los proyectos existentes. Si agrega una nueva entrada de cola de trabajos que desea programar, debe proporcionar cierta información. Por ejemplo:

* El tipo de objeto que desea ejecutar, como un informe o una codeunit. Debe tener permiso para ejecutar el informe o la codeunit en particular.
* Nombre e id. del objeto. 
* Parámetros para especificar el comportamiento del movimiento de cola de proyectos. Por ejemplo, puede agregar un parámetro para enviar solo pedidos de venta registrados. 
* Cuándo y con qué frecuencia se ejecutará la entrada de la cola de trabajos.

> [!IMPORTANT]  
> Si se le ha asignado el conjunto de permisos SUPER que se suministran con [!INCLUDE[prod_short](includes/prod_short.md)], tiene permisos para ejecutar todos los objetos incluidos en la licencia. Si tiene la función de administrador delegado, puede crear y programar entradas de la cola de trabajos, pero solo los administradores y los usuarios con licencia pueden ejecutarlas. Los usuarios con la licencia de dispositivo no pueden crear ni ejecutar colas de trabajo completas.

Después de configurar y ejecutar las colas de proyectos, el estado puede cambiar de la siguiente manera en cada período recurrente:

* **Esperar**  
* **Preparado**  
* **En proceso**  
* **Error**  
* **Terminada**  

Después de que un proyecto finaliza correctamente, se elimina de la lista de movimientos de la cola de proyectos a menos que sea un proyecto periódico. Para los proyectos periódicos, el campo **Hora inicial más próxima** se ajusta para mostrar la próxima vez que se espera que el proyecto se ejecute.  

## Supervisar el estado o los errores en la cola de proyectos

Los datos que genera la cola de proyectos se almacenan en la base de datos, para que pueda solucionar los errores de la cola de proyectos.  

Para cada entrada de la cola de proyectos, puede ver y cambiar el estado. Cuando se crea un movimiento de cola de proyectos, su estado se define en **Esperar**. Puede definir el estado a **Preparado** y de nuevo a **Esperar**, por ejemplo. Si no, la información del estado se actualiza automáticamente.

La siguiente tabla describe los valores del campo **Estado**.

| Status | Descripción |
|--|--|
| Preparado | La entrada de la cola de proyectos está lista para ejecutarse. |
| En proceso | El movimiento de la cola de proyectos está en proceso. Este campo se actualiza mientras la cola de proyectos se está ejecutando. |
| En espera | Estado predeterminado del movimiento de cola de proyectos cuando se crea. Elija la acción **Establecer estado en Preparado** para cambiar el estado a **Preparado**. Elija la acción **Establecer en espera** para cambiar el estado de nuevo a **Esperar**. |
| Error | Hubo un problema. Elija **Mostrar mensaje de error** para mostrar el mensaje de error. |
| Terminado | El movimiento de la cola de proyectos se ha terminado. |

> [!Tip]  
> Las entradas de la cola de trabajos dejan de ejecutarse cuando hay un error. Por ejemplo, esto puede ser un problema cuando una entrada se conecta a un servicio externo, como una fuente bancaria. Si el servicio no está disponible temporalmente y la entrada de la cola de trabajos no se puede conectar, la entrada mostrará un error y dejará de ejecutarse. Tendrá que reiniciar manualmente la entrada de la cola de proyectos. Sin embargo, los campos **Número máximo de intentos** y **Retardo de repetición (s)** pueden ayudarle a evitar esta situación. El campo **Número máximo de intentos** le permite especificar cuántas veces puede fallar la entrada de la cola de trabajos antes de que deje de intentar ejecutarse. El campo **Retardo de repetición (s)** le permite especificar la cantidad de tiempo, en segundos, entre intentos. La combinación de estos dos campos podría mantener la entrada de la cola de trabajos en ejecución hasta que el servicio externo esté disponible.

### Para ver el estado de un proyecto

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de cola de proyectos** y luego elija el enlace relacionado.
2. En la página **Movs. cola proyectos**, seleccione un movimiento de la cola de proyectos y luego elija la acción **Registrar movs**.  

> [!TIP]
> También puede ver el estado de los movimientos de la cola de proyectos utilizando Application Insights en Microsoft Azure para un análisis más profundo basado en telemetría. Para obtener más información, consulte [Supervisión y análisis de telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) y [Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) en el [!INCLUDE [prod_short](includes/prod_short.md)] contenido de desarrolladores y administración.

## Ver tareas programadas

La página **Tareas programadas** de [!INCLUDE [prod_short](includes/prod_short.md)] muestra qué tareas están listas para ejecutarse en la cola de trabajos. La página también muestra información sobre la empresa para la que está configurada cada tarea. Sin embargo, solo se pueden ejecutar las tareas marcadas como pertenecientes al entorno actual.  

Por ejemplo, todas las tareas programadas se detienen si la empresa actual se encuentra en un entorno que es una copia de otro entorno. Utilice la página **Tareas programadas** para establecer tareas listas para ejecutarse en la cola de trabajos.  

> [!NOTE]
> Los administradores y usuarios con licencia pueden programar tareas para que se ejecuten. Los administradores delegados pueden configurar y programar la ejecución de tareas, pero solo los usuarios con licencia pueden ejecutarlas.

## El apartado de Mi cola proyecto

El apartado **Mi cola proyecto** del Área de trabajo muestra los movimientos de colas de proyectos que se han iniciado, pero que no han finalizado. Por defecto, el apartado no se muestra, pero puede agregarlo en el área de trabajo. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).  

La parte muestra la siguiente información:

* Los documentos con su ID en el campo **Id. usuario asignado** que se están procesando o están en cola, incluidos los documentos qu se registran en segundo plano. 
* Si hubo un error al publicar un documento o en la entrada de la cola de trabajos. 

El apartado Mi cola de proyectos también le permite cancelar un registro de documento.

### Procedimiento para ver un error del apartado Mi la cola de proyectos

1. En un movimiento con el estado **Error**, elija la acción **Mostrar error**.
2. Revise el mensaje de error y corrija el problema.

## Ejemplos de lo que se puede programar usando la cola de proyectos

### Programar informes

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir la acción **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha, la periodicidad.  

Para más información, vea [Programar la ejecución de un informe](ui-work-report.md#ScheduleReport)

### Programación de la sincronización entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)]

Si ha integrado [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], la cola de proyectos le permite programar cuándo sincronizar datos. Según la dirección y las reglas que haya definido, la entrada de la cola de trabajos puede crear registros en una aplicación para que coincidan con los registros en la otra. Un buen ejemplo es cuando registra un contacto en [!INCLUDE[crm_md](includes/crm_md.md)], la entrada de la cola de trabajos puede configurar ese contacto para usted en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Programación de una sincronización entre Business Central y Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Programar la contabilización de pedidos de compra y venta

Puede usar las entradas de la cola de trabajos para programar los procesos comerciales para que se ejecuten en segundo plano. Por ejemplo, las tareas en segundo plano son útiles cuando varios usuarios registran pedidos de venta simultáneamente, pero solo se puede procesar un pedido al mismo tiempo. Para obtener más información, consulte [Para configurar el registro de fondo con colas de proyecto](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Supervisar la cola de proyectos con telemetría

Como administrador, puede utilizar [Application Insights](/azure/azure-monitor/app/app-insights-overview) para recopilar y analizar la telemetría que puede utilizar para identificar problemas. Para obtener más información, consulte [Supervisión y análisis de la telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) en el contenido de desarrolladores y administración.  

## Consulte también

[Administración](admin-setup-and-administration.md)  
[Configuración de Business Central](setup.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]