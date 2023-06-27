---
title: Sincronización de Business Central y Dataverse
description: Obtenga información sobre la sincronización de datos entre Business Central y Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Programación de una sincronización entre Business Central y Dataverse

Puede sincronizar [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[cds_long_md](includes/cds_long_md.md)] en intervalos programados configurando proyectos en la cola de proyectos. Los trabajos de sincronización sincronizan los datos de los registros de [!INCLUDE[prod_short](includes/prod_short.md)] y de los registros de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] que se han emparejado. Para registros que no se han emparejado, según la dirección y las reglas de sincronización, los trabajos de sincronización pueden crear y emparejar registros nuevos en el sistema de destino.

Hay varios trabajos de sincronización que están disponibles de forma inmediata. Los trabajos se ejecutan en el siguiente orden para evitar dependencias de emparejamiento entre tablas. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

1. Proyecto de sincronización de DIVISA - Common Data Service.
2. Proyecto de sincronización de PROVEEDOR - Common Data Service.
3. Proyecto de sincronización de CONTACTO - Common Data Service.
4. Proyecto de sincronización de CLIENTE - Common Data Service.
5. Proyecto de sincronización de VENDEDORES - Common Data Service.

Puede los proyectos en la página de **Movimientos de cola de proyectos**. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Entradas de cola de proyectos de sincronización predeterminados

La tabla siguiente describe los proyectos de sincronización predeterminados para [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Mov. cola proyecto | Descripción | Dirección | Asignación de tablas de integración | Frecuencia de sincronización predeterminada (minutos) | Tiempo de reposo de inactividad predeterminado (minutos) |
|--|--|--|--|--|--|--|
| Proyecto de sincronización de CONTACTO - Common Data Service | Sincroniza los contactos de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con los contactos de [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidireccional | CONTACTO | 30 | 720 <br>(12 horas) |
| Proyecto de sincronización de DIVISA - Common Data Service | Sincroniza las divisas de transacciones de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con las divisas de [!INCLUDE[prod_short](includes/prod_short.md)]. | De [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | DIVISA | 30 | 720 <br> (12 h) |
| Proyecto de sincronización de CLIENTE - Common Data Service | Sincroniza las cuentas de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con los clientes de [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidireccional | CLIENTE | 30 | 720<br> (12 h) |
| Proyecto de sincronización de PROVEEDOR - Common Data Service | Sincroniza las cuentas de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con los clientes de [!INCLUDE[prod_short](includes/prod_short.md)]. | Bidireccional | PROVEEDOR | 30 | 720<br> (12 h) |
| Proyecto de sincronización de VENDEDORES - Common Data Service | Sincroniza los vendedores de [!INCLUDE[prod_short](includes/prod_short.md)] con los usuarios de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. | De [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)] | VENDEDORES | 30 | 1440<br> (24 h) |

## <a name="synchronization-process"></a>Proceso de sincronización

Cada movimiento de cola de proyectos de sincronización utiliza una asignación de tabla de integración concreta que especifica qué tabla de [!INCLUDE[prod_short](includes/prod_short.md)] y tabla de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] se deben sincronizar. Las asignaciones de tabla también incluyen configuraciones que controlan qué registros de la tabla de [!INCLUDE[prod_short](includes/prod_short.md)] y de la tabla de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] se deben sincronizar.  

Para sincronizar datos, los registros de tabla de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] deben emparejarse con los registros de [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, un cliente de [!INCLUDE[prod_short](includes/prod_short.md)] debe emparejarse con una cuenta de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Puede configurar los emparejamientos manualmente, antes de ejecutar los proyectos de sincronización o permitir que los proyectos de sincronización configuren emparejamientos automáticamente. La lista siguiente describe cómo los datos se sincronizan entre [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] cuando se utilizan los movimientos de la cola de proyectos de sincronización. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

- La casilla **Sincronizar solo reg. emparejados** controla si se crean nuevos registros cuando sincroniza. De forma predeterminada, la casilla está seleccionada, lo que significa que solo se sincronizarán los registros que estén emparejados. En la asignación de tabla de integración puede cambiar la asignación de tabla entre una tabla de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y una tabla de [!INCLUDE[prod_short](includes/prod_short.md)], de manera que los proyectos de sincronización de integración creen los registros nuevos en la base de datos de destino para cada fila de la base de datos de origen que no esté emparejado. Para obtener más información, consulte [Crear registros nuevos](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Ejemplo** Si desactiva la casilla **Sincronizar solo reg. emparejados**, cuando sincroniza los clientes en [!INCLUDE[prod_short](includes/prod_short.md)] con cuentas en [!INCLUDE[cds_long_md](includes/cds_long_md.md)], se crea una nueva cuenta para cada cliente en [!INCLUDE[prod_short](includes/prod_short.md)] y se empareja automáticamente. Además, como la sincronización en este caso es bidireccional, se crea un cliente nuevo y se empareja para cada cuenta de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] que aún no está emparejada.  

    > [!NOTE]  
    > Existen reglas y filtros que determinan qué datos se sincronizan. Para obtener más información, vaya a [Reglas de sincronización](admin-synchronizing-business-central-and-sales.md).

- Cuando se crean nuevos registros en [!INCLUDE[prod_short](includes/prod_short.md)], los registros utilizan la plantilla definida para la asignación de tablas de integración o la plantilla predeterminada que está disponible para el tipo de fila. Los campos se rellenan con datos de [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[cds_long_md](includes/cds_long_md.md)] dependiendo de la dirección de sincronización. Para obtener más información, consulte [Modificar asignaciones de tablas para la sincronización](admin-how-to-modify-table-mappings-for-synchronization.md).  

- En las sincronizaciones posteriores, solo se actualizarán los registros que se hayan modificado o agregado después del último proyecto de sincronización correcto para la tabla.  

     Los nuevos registros de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] se agregan en [!INCLUDE[prod_short](includes/prod_short.md)]. Si los datos de los campos de los registros de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] se han modificado, los datos se copian en el campo correspondiente de [!INCLUDE[prod_short](includes/prod_short.md)].  

- Con la sincronización bidireccional, el proyecto se sincroniza de [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[cds_long_md](includes/cds_long_md.md)] y, a continuación, de [!INCLUDE[cds_long_md](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Acerca de los tiempos de espera de inactividad

Algunos movimientos de cola de proyecto, como los que programan la sincronización entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[cds_long_md](includes/cds_long_md.md)], utilizan el campo **Tiempo de inactividad** en la PÁGINA Mov. cola proyecto para evitar que el movimiento de cola de proyecto se ejecute innecesariamente.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Diagrama de flujo para cuando los movimientos de cola de proyecto se ponen en espera debido a la inactividad.":::

Cuando el valor en este campo no es cero y la cola de proyecto no ha encontrado ningún cambio durante la última ejecución, [!INCLUDE[prod_short](includes/prod_short.md)] pone el movimiento de cola de proyecto en espera. Cuando eso sucede, el campo **Estado de la cola de proyecto** mostrará **En espera debido a la inactividad** y [!INCLUDE[prod_short](includes/prod_short.md)] esperará el período de tiempo especificado en el campo **Tiempo de inactividad** antes de que vuelva a ejecutar el movimiento de la cola de proyecto.  

Por ejemplo, de forma predeterminada, el movimiento de cola de trabajo DIVISA, que sincroniza las divisas en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] con los tipos de cambio en [!INCLUDE[prod_short](includes/prod_short.md)], buscará cambios en los tipos de cambio cada 30 minutos. Si no se encuentran cambios, [!INCLUDE[prod_short](includes/prod_short.md)] pone el movimiento de cola de proyecto DIVISA en espera durante 720 minutos (doce horas). Si se cambia un tipo de cambio en [!INCLUDE[prod_short](includes/prod_short.md)] mientras el movimiento de cola de proyecto está en espera, [!INCLUDE[prod_short](includes/prod_short.md)] reactivará automáticamente el movimiento de cola de proyecto y reiniciará la cola de proyecto. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] activará automáticamente los movimientos de cola de proyecto que están en espera solo cuando se producen cambios en [!INCLUDE[prod_short](includes/prod_short.md)]. Los cambios en [!INCLUDE[cds_long_md](includes/cds_long_md.md)] no activarán los movimientos de cola de proyecto.

## <a name="to-view-the-synchronization-job-log"></a>Para ver el registro de proyectos de sincronización

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, introduzca **Registro de sincronización de integración** y luego elija el enlace relacionado.
2. Si se generan uno o más errores para un proyecto de sincronización, el número de errores aparece en la columna **Erróneo**. Para ver los errores del proyecto, elija el número.  

    > [!TIP]  
    > Puede ver todos los errores del proyecto de sincronización abriendo el registro de errores del proyecto de sincronización directamente.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Para ver el registro del proyecto de sincronización desde las asignaciones de tabla

1. Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, introduzca **Asignaciones de tabla de integración** y luego elija el enlace relacionado.
2. En la página **Lista de asignaciones de tablas de integración**, seleccione un movimiento y después seleccione **Registro de trabajo de sinc. de integración**.  

## <a name="to-view-the-synchronization-error-log"></a>Para ver el registro de errores de sincronización

- Elija el icono :::image type="icon" source="media/ui-search/search_small.png" border="false":::, introduzca **Errores de sincronización de integración** y luego elija el enlace relacionado.

## <a name="see-also"></a>Consulte también .

[Sincronización de datos en Business Central y [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Sincronizar manualmente las asignaciones de tablas](admin-manual-synchronization-of-table-mappings.md)  
[Programación de una sincronización entre Business Central y [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Acerca de la integración de Dynamics 365 Business Central con [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
