---
title: Administrar la sincronización de datos maestros
description: Aprenda a administrar la sincronización de datos maestros.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 04/05/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a>Administrar la sincronización de datos maestros

Después de configurar la sincronización de datos maestros y sincronizar por primera vez, los registros de las tablas seleccionadas se acoplan y se crea una entrada de cola de trabajos recurrentes para cada tabla. Las entradas de la cola de trabajos sincronizan automáticamente los datos en las empresas filiales cuando alguien realiza un cambio en la empresa de origen. En otro caso, no necesita hacer nada.

> [!NOTE]
> De forma predeterminada, las entradas de la cola de trabajos se programan para ejecutarse cada minuto y no se puede cambiar la programación.

Sin embargo, a veces las cosas salen mal y puede haber situaciones que deba gestionar o investigar. Por ejemplo, si las personas cambian el mismo registro tanto en la empresa de origen como en una filial, la sincronización fallará para que pueda especificar el cambio correcto. O bien, la empresa de origen podría instalar una extensión que cambie el esquema de una de las tablas que está sincronizando, agregando uno o dos campos. Si desea sincronizar los nuevos campos en las filiales, deberá instalar las mismas extensiones y actualizar los esquemas de tabla en su configuración.

Este artículo describe las herramientas que puede utilizar para que la sincronización funcione sin problemas.

## <a name="overwrite-local-changes"></a>Sobrescribir cambios locales

Puede usar la casilla de verificación **Sobrescribir cambio local** en los campos y tablas que sincroniza para permitir que los datos de la empresa de origen sobrescriban los datos de la empresa subsidiaria.

> [!NOTE]
> No puede habilitar la sincronización de un campo y permitir que la filial escriba valores en él independientemente de la empresa de origen. Debe deshabilitar la sincronización del campo o permitir que la empresa de origen sobrescriba los cambios locales.

## <a name="update-table-schemas"></a>Actualizar esquemas de tablas

Si la empresa de origen cambia una tabla, por ejemplo, al agregar un campo que desea sincronizar, las filiales deben actualizar sus asignaciones de campos. En la página **Campos de sincronización**, use la acción **Actualizar campos**.

## <a name="enable-or-disable-couplings-between-records"></a>Habilitar o deshabilitar los acoplamientos entre registros

Para iniciar o detener el acoplamiento de registros específicos en una tabla, en la página **Campos de sincronización**, elija los campos y luego use las acciones **Habilitar** o **Deshabilitar**.

> [!TIP]
> Una forma rápida de habilitar o deshabilitar varios campos al mismo tiempo es seleccionarlos en la lista y luego usar las acciones **Habilitar** o **Deshabilitar**.

## <a name="run-a-full-synchronization"></a>Ejecutar una sincronización completa

La acción **Ejecutar sincronización completa** programa una sincronización para todos los registros de la tabla en la empresa de origen y resincroniza todos los registros incondicionalmente. Por ejemplo, la resincronización es útil si habilita un campo adicional en una tabla de sincronización o agrega un campo adicional mediante la acción **Actualizar campos**. La acción sincroniza retroactivamente los datos de esos campos.

## <a name="synchronize-modified-records"></a>Sincronizar registros modificados

Si cambia una configuración para una tabla o campo en una filial, debe actualizar la sincronización. Para actualizar la sincronización, use la acción **Sincronizar registros modificados** en la página **Tablas de sincronización**.

La acción **Sincronizar registros modificados** programa una sincronización de los siguientes registros de la tabla:

* Registros que no se pudieron sincronizar en el último intento.
* Los registros que se cambiaron en la empresa de origen después de la última sincronización programada. Puede revisar la última hora de sincronización programada en la página **Tablas de sincronización** en el campo **Sincronizar cambios desde** .

La acción funciona de la misma manera que una sincronización programada y puede usarla como una forma de sincronizar fuera de la programación. Por ejemplo, si selecciona la casilla de verificación **Sobrescribir cambio local** en un campo para permitir que los datos de la empresa de origen sobrescriban los cambios locales, la acción actualiza esos datos. También puede esperar hasta que se produzca la siguiente sincronización programada.

## <a name="investigate-the-status-of-synchronization"></a>Investigar el estado de la sincronización

Hay dos acciones en la página **Tablas de sincronización** que pueden ayudarle a monitorear la sincronización:

* **Trabajos de sincronización de integración**
* **Movs. cola proyecto**

La siguiente tabla describe las acciones.

|Página  |Descripción  |
|---------|---------|
|**Trabajos de sincronización de integración**     | Abra la página **Trabajos de sincronización de integración** para investigar qué sucedió cada vez que se ejecutó una entrada de cola de trabajo. Para profundizar en los detalles sobre los nuevos registros que se agregaron, o explorar por qué un registro no se pudo sincronizar, elija los números en las columnas **Insertado** o **Errores**. También puede usar esta página para limpiar registros más antiguos que quizás no necesite. Para obtener más información sobre la limpieza, vaya a [Limpiar entradas antiguas](#clean-up-old-entries).        |
|**Movs. cola proyecto**     | Acceda a los detalles sobre la entrada de la cola de trabajos que sincronizan los datos de una tabla seleccionada. Por ejemplo, use esta página para administrar el estado de la entrada de la cola de trabajos. Para obtener más información sobre las entradas de la cola de trabajos, vaya a [Usar colas de trabajos para programar tareas](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Si encuentra un error en la página **Trabajos de sincronización de integración** que no puede resolver usted mismo, si se pone en contacto con su socio o Microsoft para obtener asistencia, es útil proporcionar el mensaje de error e información de la pila de llamadas.

## <a name="clean-up-old-entries"></a>Limpiar entradas antiguas

Con el tiempo, la cantidad de entradas del registro de sincronización aumentará, por lo que es posible que desee hacer un poco de limpieza para eliminar las entradas innecesarias. Para facilitar la limpieza de entradas antiguas, la página **Trabajos de sincronización de integración** ofrece las siguientes acciones:

* **Eliminar movs. anteriores a 7 días**
* **Eliminar todos los movs.**

## <a name="adding-extensions"></a>Agregar extensiones

Si la empresa de origen instala una nueva extensión, la filial también debe instalarla si desea sincronizar datos para ella. La filial puede usar la acción **Actualizar campos** en la página **Campos de sincronización** para agregar las tablas de la extensión a la lista.

> [!NOTE]
> Algunas tablas obtienen datos de tablas relacionadas. Si agrega una extensión que no incluye tablas relacionadas, los campos de esas tablas no estarán disponibles. Verifique que haya agregado todas las tablas relacionadas.

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a>Consulte también

[Prepararse para sincronizar datos maestros](admin-set-up-data-sync.md)
