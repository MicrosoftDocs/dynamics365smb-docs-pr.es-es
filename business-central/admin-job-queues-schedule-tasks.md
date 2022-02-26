---
title: Programar proyectos para que se ejecuten automáticamente
description: Las tareas programadas son administradas por la cola de proyecto. Estos proyectos ejecutan informes y codeunits. Puede configurar proyectos para que se ejecuten una vez o de manera periódica.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 46759304a312e0376e8b309b29d5e0491b34a69f
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012240"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Uso de colas de proyectos para programar tareas

Las colas de proyectos de [!INCLUDE[prod_short](includes/prod_short.md)] permiten a los usuarios programar y ejecutar informes y codeunits específicos. Puede configurar proyectos para que se ejecuten una vez o de manera periódica. Por ejemplo, es posible que desee ejecutar el informe **Vendedor * Estadísticas de ventas** semanalmente, para realizar un seguimiento de las ventas por vendedor cada semana, o puede que desee ejecutar la codeunit **Solicitudes de aprobación de delegados** diariamente, para evitar que los documentos se acumulen o bloqueen el flujo de trabajo.

La página **Entradas de cola de proyectos** enumera todos los proyectos existentes. Si agrega una nueva entrada de cola de proyectos que desee programar, debe especificar información acerca del tipo de objeto que desea ejecutar, por ejemplo, informe o codeunit y nombre y el identificador del objeto que desee ejecutar. También puede agregar parámetros para especificar el comportamiento del movimiento de cola de proyectos. Por ejemplo, puede agregar un parámetro para enviar solo pedidos de venta registrados. Debe disponer de los permisos adecuados para ejecutar el informe o la codeunit en particular; de lo contrario, se devolverá un error al ejecutarse la cola de proyectos.  
> [!IMPORTANT]  
> Si utiliza el conjunto de permisos SUPER que se suministran con [!INCLUDE[prod_short](includes/prod_short.md)], usted y sus usuarios tienen permisos para ejecutar todos los objetos dentro de la licencia. Eso todavía no es suficiente para el administrador delegado o los usuarios con licencia de dispositivo, que no pueden crear entradas para la cola de proyectos.

Una cola de proyectos puede tener muchos movimientos, que son proyectos que la cola controla y ejecuta. La información del movimiento especifica qué codeunit o informe se ejecuta, cuándo y con qué frecuencia se ejecuta el movimiento, en qué categoría se ejecuta el proyecto y cómo se ejecuta.  

Después de configurar y ejecutar las colas de proyectos, el estado puede cambiar de la siguiente manera en cada período recurrente:

* **Esperar**  
* **Preparado**  
* **En proceso**  
* **Error**  
* **Terminada**  

Después de que un proyecto haya finalizado correctamente, se elimina de la lista de movimientos de la cola de proyectos a menos que sea un proyecto periódico. Si es un proyecto periódico, el campo **Hora inicial más próxima** se ajusta para mostrar la próxima vez que se espera que el proyecto se ejecute.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Supervisar el estado o los errores en la cola de proyectos

Los datos que se generan cuando se ejecuta una cola de proyectos se almacenan en la base de datos, para que pueda solucionar los errores de la cola de proyectos.  

Para cada entrada de la cola de proyectos, puede ver y cambiar el estado. Cuando se crea un movimiento de cola de proyectos, su estado se define en **Esperar**. Puede definir el estado a **Preparado** y de nuevo a **Esperar**, por ejemplo. Si no, la información del estado se actualiza automáticamente.

La siguiente tabla describe los valores del campo **Estado**.

| Estado | Descripción |
|--|--|
| Preparado | Indica que el movimiento de la cola de proyectos está listo para ejecutarse. |
| En proceso | Indica que el movimiento de la cola de proyectos está en proceso. Este campo se actualiza mientras la cola de proyectos se está ejecutando. |
| Esperar | Predeterminado. Indica el estado del movimiento de cola de proyectos cuando se crea. Elija la acción **Establecer estado en Preparado** para cambiar el estado a **Preparado**. Elija las acciones **Establecer en espera** o **Suspender** para cambiar el estado de nuevo a **Esperar**. |
| Error | Indica que hay un error. Elija **Mostrar mensaje de error** para ver el mensaje de error. |
| Terminada | Indica que el movimiento de la cola de proyectos se ha terminado. |

### <a name="to-view-status-for-any-job"></a>Para ver el estado de un proyecto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de cola de proyectos** y luego elija el enlace relacionado.
2. En la página **Movs. cola proyectos**, seleccione un movimiento de la cola de proyectos y luego elija la acción **Registrar movs**.  

> [!TIP]
> También puede ver el estado de los movimientos de la cola de proyectos utilizando Application Insights en Microsoft Azure para un análisis más profundo basado en telemetría. Para obtener más información, consulte [Supervisión y análisis de telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) y [Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) en el [!INCLUDE [prod_short](includes/prod_short.md)] contenido de desarrolladores y administración.

## <a name="view-scheduled-tasks"></a>Ver tareas programadas

La página **Tareas programadas** de [!INCLUDE [prod_short](includes/prod_short.md)] muestra qué tareas están listas para ejecutarse en la cola de trabajos. La página también muestra información sobre la empresa para la que está configurada cada tarea. Sin embargo, solo se pueden ejecutar las tareas marcadas como pertenecientes al entorno actual.  

Por ejemplo, si la empresa actual se encuentra en un entorno que es una copia de otro entorno, todas las tareas programadas se detienen automáticamente. Utilice la página **Tareas programadas** para establecer tareas listas para ejecutarse en la cola de trabajos.  

> [!NOTE]
> Los administradores y usuarios internos pueden programar tareas para que se ejecuten. Los administradores delegados no pueden.

## <a name="the-my-job-queue-part"></a>El apartado de Mi cola proyecto

El apartado **Mi cola proyecto** del Área de trabajo muestra los movimientos de colas de proyectos que se han iniciado, pero que aún no han finalizado. Por defecto, el apartado no puede verse, por lo que tiene que agregarlo en el área de trabajo. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).  

Este apartado muestra los documentos con su ID en el campo **Id. usuario asignado** que se están procesando o están en cola, incluidos los relacionados con el registro en segundo plano. La parte puede indicar en un vistazo si se produjo error en el registro de un documento o si hay errores en un movimiento de cola de proyectos. El apartado también le permite cancelar un registro de documento si no se está ejecutando.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Procedimiento para ver un error del apartado Mi la cola de proyectos

1. En un movimiento con el estado **Error**, elija la acción **Mostrar error**.
2. Revise el mensaje de error y corrija el problema.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Ejemplos de lo que se puede programar usando la cola de proyectos

### <a name="schedule-reports"></a>Programar informes

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir la acción **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha, la periodicidad.  

Para más información, vea [Programar la ejecución de un informe](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Programación de la sincronización entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)]

Si ha integrado [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], puede utilizar la cola de proyectos para programar cuándo desea sincronizar los datos de los registros que ha emparejado en las dos aplicaciones empresariales. Dependiendo de la dirección y las reglas que haya definido para la integración, los trabajos de sincronización también pueden crear nuevos registros en la aplicación de destino para que coincidan con los del origen. Por ejemplo, si un vendedor crea un nuevo contacto en [!INCLUDE[crm_md](includes/crm_md.md)], el proyecto de sincronización puede crear ese contacto para el vendedor emparejado en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Programación de una sincronización entre Business Central y Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Programar la contabilización de pedidos de compra y venta

Las colas de proyecto son una herramienta eficaz para programar la ejecución de procesos de negocios en segundo plano, como cuando varios usuarios intentan publicar pedidos de ventas, pero solo se puede procesar un pedido a la vez.  

Para obtener más información, consulte [Para configurar el registro de fondo con colas de proyecto](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="monitor-the-job-queue-with-telemetry"></a>Supervisar la cola de proyectos con telemetría

Como administrador, puede utilizar [Application Insights](/azure/azure-monitor/app/app-insights-overview) para recopilar y analizar la telemetría que puede utilizar para identificar problemas. Para obtener más información, consulte [Supervisión y análisis de la telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) en el contenido de desarrolladores y administración.  

## <a name="see-also"></a>Consulte también

[Administración](admin-setup-and-administration.md)  
[Configuración de Business Central](setup.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]