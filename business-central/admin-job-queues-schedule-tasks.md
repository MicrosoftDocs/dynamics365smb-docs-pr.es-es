---
title: Programar proyectos para que se ejecuten automáticamente
description: Aprenda a usar las entradas de la cola de proyectos para ejecutar informes y codeunits.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 09/15/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# Usar colas de proyectos para programar tareas

Use la página **Entradas de colas de proyectos** para programar y ejecutar informes y codeunits específicos. Puede configurar proyectos para que se ejecuten una vez o de manera periódica. Por ejemplo, es posible que desee ejecutar el informe **Vendedor * Estadísticas de ventas** semanalmente para realizar un seguimiento de las ventas por vendedor cada semana o ejecutar la codeunit **Solicitudes de aprobación de delegados** diariamente, para evitar que los documentos se acumulen.

La página Entradas de cola de proyectos enumera todos los proyectos existentes. Si agrega una nueva entrada de cola de proyectos que seguirá una programación, debe proporcionar cierta información. Por ejemplo:

* El tipo de objeto que desea ejecutar, como un informe o una codeunit. Debe tener permiso para ejecutar el informe o la codeunit en particular.
* Nombre e id. del objeto.
* Parámetros para especificar el comportamiento del movimiento de cola de proyectos. Por ejemplo, puede agregar un parámetro para enviar solo pedidos de venta registrados.
* Cuándo y con qué frecuencia se ejecutará la entrada de la cola de trabajos.

> [!IMPORTANT]  
> Si se le ha asignado el conjunto de permisos SUPER que se suministran con [!INCLUDE[prod_short](includes/prod_short.md)], tiene permisos para ejecutar todos los objetos incluidos en la licencia. Si tiene la función de administrador delegado, puede crear y programar entradas de la cola de trabajos, pero solo los administradores y los usuarios con licencia pueden ejecutarlas.

Después de configurar y ejecutar las colas de proyectos, el estado puede cambiar de la siguiente manera en cada período recurrente:

* **En espera**  
* **Preparado**  
* **En proceso**  
* **Error**  
* **Terminada**  
* **En espera debido a la inactividad**

> [!NOTE]
> El estado **En espera debido a la inactividad** se utiliza principalmente para movimientos de cola de proyectos que programan la sincronización entre [!INCLUDE [prod_short](includes/prod_short.md)] y otra aplicación, como [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Para obtener más información acerca de este estado, vaya a [Acerca de los tiempos de espera de inactividad](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts).

Después de que un proyecto finaliza correctamente, se elimina de la lista de movimientos de la cola de proyectos a menos que sea un proyecto periódico. Para los proyectos periódicos, el campo **Hora inicial más próxima** se ajusta para mostrar la próxima vez que el proyecto se ejecute. 

## Importante para la programación de proyectos periódicos

> [!IMPORTANT]  
> Las colas de trabajos periódicos pueden afectar el rendimiento, por lo que no debe ejecutarlas con demasiada frecuencia. Cuando configure la frecuencia con la que ejecutar un trabajo periódico, intente establecer el mayor intervalo de tiempo posible. Por ejemplo, si está a punto de establecer una repetición de cinco minutos, piense si pueden ser 15 minutos o incluso una vez por hora. Al planificar colas de trabajos periódicos, considere a qué áreas de la aplicación afectará el trabajo. ¿Es un área donde trabajan muchos usuarios y se verá afectada por una intensa actividad? Considere la duración de la ejecución de un solo trabajo y las motivaciones comerciales para ejecutar trabajos con una cadencia determinada.

## La primera fecha de inicio

El valor en el campo **Fecha/hora de inicio más temprana** en la página **Tarjeta de entrada de cola de trabajos** se muestra la próxima vez que El trabajo se ejecutará. Hay varios factores que pueden afectar si una entrada de la cola de trabajos realmente se ejecuta en ese momento.

Los factores más comunes son la cantidad de entradas de la cola de trabajos en un entorno y la cantidad total de tareas programadas. Para proteger los niveles de rendimiento, existen límites operativos. Si tiene muchas entradas en la cola y, por ejemplo, una de ellas falla o las entradas simplemente tardan más de lo esperado, es posible que el siguiente trabajo no comience a la hora esperada. Si tiene unidades de código que generan 100 000 o más tareas programadas, debe investigar si realmente necesita todas esas tareas. Puede acceder a la lista de todas las tareas programadas en la página **Tareas programadas**.

Para obtener más información sobre cómo monitorear el estado de las entradas de la cola de trabajos, vaya a [Para ver el estado de cualquier trabajo](#to-view-status-for-any-job). Para obtener más información sobre los límites operativos, vaya a [Límites de tareas asincrónicas](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## Supervisar el estado o los errores en la cola de proyectos

Los datos que genera la cola de proyectos se almacenan, para que pueda solucionar los errores.  

Para cada entrada de la cola de proyectos, puede ver y cambiar el estado. Cuando se crea un movimiento de cola de proyectos, su estado se define en **Esperar**. Puede definir el estado a **Preparado** y de nuevo a **Esperar**, por ejemplo. Si no, la información del estado se actualiza automáticamente.

La siguiente tabla describe los valores del campo **Estado**.

| Status | Descripción |
|--|--|
| Preparado | La entrada de la cola de proyectos está lista para ejecutarse. |
| En proceso | El movimiento de la cola de proyectos está en proceso. Este campo se actualiza mientras la cola de proyectos se está ejecutando. |
| En espera | Estado predeterminado del movimiento de cola de proyectos cuando se crea. Elija la acción **Establecer estado en Preparado** para cambiar el estado a **Preparado**. Elija la acción **Establecer en espera** para cambiar el estado de nuevo a **Esperar**. Para obtener más información, consulte [Acerca de En espera](#about-on-hold).|
| Error | Ha habido un problema. Elija **Mostrar mensaje de error** para mostrar el mensaje de error. |
| Terminado | El movimiento de la cola de proyectos se ha terminado. |

> [!TIP]  
> Las entradas de la cola de trabajos dejan de ejecutarse cuando hay un error. Por ejemplo, esto puede ser un problema cuando una entrada se conecta a un servicio externo, como una fuente bancaria. Si el servicio no está disponible temporalmente y la entrada de la cola de trabajos no se puede conectar, la entrada mostrará un error y dejará de ejecutarse. Tendrá que reiniciar manualmente la entrada de la cola de proyectos. Sin embargo, los campos **Número máximo de intentos** y **Retardo de repetición (s)** pueden ayudarle a evitar esta situación. El campo **Número máximo de intentos** le permite especificar cuántas veces puede fallar la entrada de la cola de trabajos antes de que deje de intentar ejecutarse. El campo **Retardo de repetición (s)** le permite especificar la cantidad de tiempo, en segundos, entre intentos. La combinación de estos dos campos podría mantener la entrada de la cola de trabajos en ejecución hasta que el servicio externo esté disponible.

### Acerca de En espera

Ajustar una entrada de la cola de trabajos a **En espera** no afecta un trabajo que ya se está ejecutando. Una vez que un trabajo se ha iniciado en la cola de trabajos, continúa ejecutándose hasta su finalización, independientemente de cualquier cambio posterior realizado en la entrada de la cola de trabajos, como ponerlo en espera.<br><br>El estado **En espera** se utiliza normalmente para evitar que un trabajo se inicie automáticamente cuando llega a su hora de inicio programada. Le permite pausar temporalmente la ejecución de un trabajo antes de que comience a procesarse. Sin embargo, una vez que un trabajo ya está en marcha, cambiar el estado a "En espera" no interrumpirá ni afectará a la ejecución del trabajo.<br><br>Si necesita detener o cancelar un trabajo en ejecución, puede hacerlo interviniendo manualmente en el proceso, por ejemplo, finalizando la sesión correspondiente o el proceso responsable de ejecutar el trabajo.
### Para ver el estado de un proyecto

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Movimientos de cola de proyectos** y luego elija el enlace relacionado.
2. En la página **Movs. cola proyectos**, seleccione un movimiento de la cola de proyectos y luego elija la acción **Registrar movs**.  

> [!TIP]
> Para un análisis detallado basado en telemetría, puede usar Application Insights en Microsoft Azure para revisar el estado de las entradas de la cola de proyectos. Para obtener más información sobre la telemetría, vaya a [Supervisión y análisis de telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) y [Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## Ver tareas programadas

La página **Tareas programadas** de [!INCLUDE [prod_short](includes/prod_short.md)] muestra qué tareas están listas para ejecutarse en la cola de trabajos. La página también muestra información sobre la empresa para la que está configurada cada tarea. Sin embargo, solo se pueden ejecutar las tareas marcadas como pertenecientes al entorno actual.  

Por ejemplo, todas las tareas programadas se detienen si la empresa actual se encuentra en un entorno que es una copia de otro entorno. Utilice la página **Tareas programadas** para establecer tareas listas para ejecutarse en la cola de trabajos.  

> [!NOTE]
> Los administradores y usuarios con licencia pueden programar tareas para que se ejecuten. Los administradores delegados pueden configurar y programar la ejecución de tareas, pero solo los usuarios con licencia pueden ejecutarlas.

## El apartado de Mi cola de proyectos

El apartado **Mi cola proyecto** del Área de trabajo muestra los movimientos de colas de proyectos que se han iniciado, pero que no han finalizado. Por defecto, el apartado no se muestra, pero puede agregarlo en el área de trabajo. Para obtener más información sobre personalización, vaya a [Personalizar el área de trabajo](ui-personalization-user.md).  

La parte muestra la siguiente información:

* Los documentos con su ID en el campo **Id. usuario asignado** que se están procesando o están en cola, incluidos los documentos qu se registran en segundo plano. 
* Si hubo un error al publicar un documento o en la entrada de la cola de trabajos. 

El apartado Mi cola de proyectos también le permite cancelar un registro de documento.

### Procedimiento para ver un error del apartado Mi la cola de proyectos

1. En un movimiento con el estado **Error**, elija la acción **Mostrar error**.
2. Revise el mensaje de error y corrija el problema.

## Ejemplos de lo que puede programar mediante entradas de la cola de proyectos

### Programar informes

Puede programar un informe o un trabajo por lotes para ejecutarlo en una fecha y hora específicos. Los informes y los trabajos por lotes programados se introducen en la cola de proyectos y se procesan en el momento programado, de manera similar a con otros proyectos. Elija la opción **Programa** después de elegir la acción **Enviar a** y, a continuación, introduzca información como la impresora, la hora y la fecha, la periodicidad.  

Para obtener más información sobre la programación, vaya a [Programación de un informe para ejecutar](ui-work-report.md#ScheduleReport)

### Programación de la sincronización entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)]

Si ha integrado [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], la cola de proyectos le permite programar cuándo sincronizar datos. Según la dirección y las reglas que haya definido, la entrada de la cola de trabajos puede crear registros en una aplicación para que coincidan con los registros en la otra. Un buen ejemplo es cuando registra un contacto en [!INCLUDE[crm_md](includes/crm_md.md)], la entrada de la cola de trabajos puede configurar ese contacto para usted en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información sobre la programación, vaya a [Programación de una sincronización entre Business Central y Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Programar la contabilización de pedidos de compra y venta

Puede usar las entradas de la cola de trabajos para programar los procesos comerciales para que se ejecuten en segundo plano. Por ejemplo, las tareas en segundo plano son útiles cuando varios usuarios registran pedidos de venta simultáneamente, pero solo se puede procesar un pedido al mismo tiempo. Para obtener más información sobre la publicación en segundo plano, vaya a [Configurar la publicación en segundo plano con colas de proyectos](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Gestionar problemas de entrada de la cola de proyectos

Si una entrada de la cola de proyectos muestra un error, su primera opción para resolver el problema es reiniciar la entrada de la cola de proyectos. Puede establecer el estado de la entrada de la cola de trabajos en **En espera** y luego a **Listo**, o simplemente reiniciarlo.

Si un reinicio no ayuda, el problema podría estar en el código. Puede encontrar al propietario (también llamado el *editor*) del código en el seguimiento de la pila AL en el registro de la cola de proyectos. Si el error proviene de una aplicación/extensión, comuníquese con su partner de Microsoft. Si el error proviene de una aplicación de Microsoft, abra una solicitud de soporte con Microsoft.

Si se pone en contacto con su partner de Microsoft o con Microsoft para obtener soporte, proporcione la siguiente información:

* El id. de la entrada de la cola de proyectos donde ocurrió el error
* La marca de tiempo de cuando ocurrió el error
* Su zona horaria

> [!TIP]
> Dependiendo de si su [!INCLUDE [prod_short](includes/prod_short.md)] es anterior o posterior a la versión 22.1, recopile la información de las siguientes maneras:
>
> * Para versiones anteriores, proporcione una captura de pantalla de la página **Entradas de registro de la cola de proyectos**.
> * Para versiones posteriores, use la acción **Copiar detalles** en la página Entradas de registro de cola de proyectos para copiar la información (id. de cola de proyectos, marca de tiempo y su zona horaria).

## Supervisar la cola de proyectos con telemetría

Los administradores pueden usar [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) para reunir y analizar telemetría que les ayude a identificar problemas. Para obtener más información sobre la telemetría, vaya a [Supervisión y análisis de telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) y [Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

La telemetría permite a los administradores configurar alertas sobre problemas en la cola de proyectos que envían un mensaje de texto, un correo electrónico o un mensaje en Teams si algo no está bien. Para obtener más información sobre estas alertas, vaya a [Alerta sobre telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## Consulte también .

[Administración](admin-setup-and-administration.md)  
[Configuración de Business Central](setup.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Análisis de la telemetría de seguimiento del ciclo de vida de la cola de proyectos](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Alerta sobre telemetría](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
