---
title: Sincronización de Business Central y Common Data Service | Documentos de Microsoft
description: Obtenga información sobre la sincronización de datos entre Business Central y Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196596"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Programación de una sincronización entre Business Central y Common Data Service
Puede sincronizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[d365fin](includes/cds_long_md.md)] en intervalos programados configurando proyectos en la cola de proyectos. Los proyectos de sincronización sincronizan los datos de los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de los registros de [!INCLUDE[d365fin](includes/cds_long_md.md)] que se han emparejado previamente. O, para registros que no se han emparejado, según la dirección y las reglas de sincronización, los proyectos de sincronización pueden crear y emparejar registros nuevos en el sistema de destino. 

Hay varios trabajos de sincronización que están disponibles de forma inmediata. Los trabajos se ejecutan en el siguiente orden para evitar dependencias de emparejamiento entre entidades. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. Proyecto de sincronización de DIVISA - [!INCLUDE[d365fin](includes/cds_long_md.md)].
2. Proyecto de sincronización de PROVEEDOR - [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
3. Proyecto de sincronización de CONTACTO - [!INCLUDE[d365fin](includes/cds_long_md.md)].
4. Proyecto de sincronización de CLIENTE - [!INCLUDE[d365fin](includes/cds_long_md.md)].
5. Proyecto de sincronización de VENDEDORES - [!INCLUDE[d365fin](includes/cds_long_md.md)].

Puede los proyectos en la página de **Movimientos de cola de proyectos**. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Movimientos de la cola de proyectos de sincronización predeterminados  
La tabla siguiente describe los proyectos de sincronización predeterminados para [!INCLUDE[d365fin](includes/cds_long_md.md)].  

|Mov. cola proyecto|Descripción|Dirección|Asignación de tablas de integración|Frecuencia de sincronización predeterminada (minutos)|Tiempo de reposo de inactividad predeterminado (minutos)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Proyecto de sincronización de CONTACTO - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincroniza los contactos de [!INCLUDE[d365fin](includes/cds_long_md.md)] con los contactos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidireccional|CONTACTO|30|720 <br>(12 horas)| 
|Proyecto de sincronización de DIVISA - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincroniza las divisas de transacciones de [!INCLUDE[d365fin](includes/cds_long_md.md)] con las divisas de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)]|DIVISA|30|720 <br> (12 h)| 
|Proyecto de sincronización de CLIENTE - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincroniza las cuentas de [!INCLUDE[d365fin](includes/cds_long_md.md)] con los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidireccional|CLIENTE|30|720<br> (12 h)|
|Proyecto de sincronización de PROVEEDOR - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincroniza las cuentas de [!INCLUDE[d365fin](includes/cds_long_md.md)] con los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidireccional|PROVEEDOR|30|720<br> (12 h)|
|Proyecto de sincronización de VENDEDORES - [!INCLUDE[d365fin](includes/cds_long_md.md)]|Sincroniza los vendedores de [!INCLUDE[d365fin](includes/d365fin_md.md)] con los usuarios de [!INCLUDE[d365fin](includes/cds_long_md.md)].|De [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]|VENDEDORES|30|1440<br> (24 h)|

## <a name="synchronization-process"></a>Proceso de sincronización  
Cada movimiento de cola de proyectos de sincronización utiliza una asignación de tabla de integración concreta que especifica qué tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] se deben sincronizar. Las asignaciones de tabla también incluyen configuraciones que controlan qué registros de la tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de la entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] se deben sincronizar.  

Para sincronizar datos, los registros de entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] deben emparejarse con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, un cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)] debe emparejarse con una cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Puede configurar los emparejamientos manualmente, antes de ejecutar los proyectos de sincronización o permitir que los proyectos de sincronización configuren emparejamientos automáticamente. La lista siguiente describe cómo los datos se sincronizan entre Common Data Service y [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se utilizan los movimientos de la cola de proyectos de sincronización. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md).

-   La casilla **Sincronizar solo reg. emparejados** controla si se crean nuevos registros cuando sincroniza. De forma predeterminada, la casilla está seleccionada, lo que significa que solo se sincronizarán los registros que estén emparejados. En la asignación de tabla de integración puede cambiar la asignación de tabla entre una entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] y una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)], de manera que los proyectos de sincronización de integración creen los registros nuevos en la base de datos de destino para cada registro de la base de datos de origen que no esté emparejado. Para obtener más información, consulte [Crear registros nuevos](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Ejemplo** Si desactiva la casilla **Sincronizar solo reg. emparejados**, cuando sincroniza los clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)] con cuentas en [!INCLUDE[d365fin](includes/cds_long_md.md)], se crea una nueva cuenta para cada cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)] y se empareja automáticamente. Además, como la sincronización en este caso es bidireccional, se crea un cliente nuevo y se empareja para cada cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)] que aún no está emparejada.  

    > [!NOTE]  
    > Existen reglas y filtros que determinan qué datos se sincronizan. Para obtener más información, vea [Reglas de sincronización](admin-synchronizing-business-central-and-sales.md).

-   Cuando se crean nuevos registros en [!INCLUDE[d365fin](includes/d365fin_md.md)], los registros utilizan la plantilla definida para la asignación de tablas de integración o la plantilla predeterminada que está disponible para el tipo de registro. Los campos se rellenan con datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[d365fin](includes/cds_long_md.md)] dependiendo de la dirección de sincronización. Para obtener más información, consulte [Modificar asignaciones de tablas para la sincronización](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   En las sincronizaciones posteriores, solo se actualizarán los registros que se hayan modificado o agregado después del último proyecto de sincronización correcto para la entidad.  

     Los nuevos registros de [!INCLUDE[d365fin](includes/cds_long_md.md)] se agregan en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si los datos de los campos de los registros de [!INCLUDE[d365fin](includes/cds_long_md.md)] se han modificado, los datos se copian en el campo correspondiente de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Con la sincronización bidireccional, el proyecto se sincroniza de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)] y, a continuación, de [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Acerca de los tiempos de espera de inactividad
Algunos movimientos de cola de proyecto, como los que programan la sincronización entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)], utilizan el campo **Tiempo de inactividad** en la ficha Mov. cola proyecto para evitar que el movimiento de cola de proyecto se ejecute innecesariamente.  
<br><br>

> ![Diagrama de flujo para cuando los movimientos de cola de proyecto se ponen en espera debido a la inactividad.](media/on-hold-with-inactivity-timeout.png)

Cuando el valor en este campo no es cero y la cola de proyecto no ha encontrado ningún cambio durante la última ejecución, [!INCLUDE[d365fin](includes/d365fin_md.md)] pone el movimiento de cola de proyecto en espera. Cuando eso sucede, el campo **Estado de la cola de proyecto** mostrará **En espera debido a la inactividad** y [!INCLUDE[d365fin](includes/d365fin_md.md)] esperará el período de tiempo especificado en el campo **Tiempo de inactividad** antes de que vuelva a ejecutar el movimiento de la cola de proyecto. 

Por ejemplo, de forma predeterminada, el movimiento de cola de trabajo DIVISA, que sincroniza las divisas en [!INCLUDE[d365fin](includes/cds_long_md.md)] con los tipos de cambio en [!INCLUDE[d365fin](includes/d365fin_md.md)], buscará cambios en los tipos de cambio cada 30 minutos. Si no se encuentran cambios, [!INCLUDE[d365fin](includes/d365fin_md.md)] pone el movimiento de cola de proyecto DIVISA en espera durante 720 minutos (seis horas). Si se cambia un tipo de cambio en [!INCLUDE[d365fin](includes/d365fin_md.md)] mientras el movimiento de cola de proyecto está en espera, [!INCLUDE[d365fin](includes/d365fin_md.md)] reactivará automáticamente el movimiento de cola de proyecto y reiniciará la cola de proyecto. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] activará automáticamente los movimientos de cola de proyecto que están en espera solo cuando se producen cambios en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Los cambios en [!INCLUDE[d365fin](includes/cds_long_md.md)] no activarán los movimientos de cola de proyecto.

## <a name="to-view-the-synchronization-job-log"></a>Para ver el registro de proyectos de sincronización  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro de sincronización de integración** y luego elija el enlace relacionado.
2.  Si se generan uno o más errores para un proyecto de sincronización, el número de errores aparece en la columna **Erróneo**. Para ver los errores del proyecto, elija el número.  

    > [!TIP]  
    > Puede ver todos los errores del proyecto de sincronización abriendo el registro de errores del proyecto de sincronización directamente.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Para ver el registro del proyecto de sincronización desde las asignaciones de tabla  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignaciones de tablas de integración** y luego elija el enlace relacionado.
2.  En la página **Lista de asignaciones de tablas de integración**, seleccione un movimiento y después seleccione **Registro de trabajo de sinc. de integración**.  

## <a name="to-view-the-synchronization-error-log"></a>Para ver el registro de errores de sincronización  
* Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Errores de sincronización de integración** y luego elija el enlace relacionado.

## <a name="see-also"></a>Consulte también  
[Sincronización de datos en Business Central y [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Sincronizar manualmente las asignaciones de tablas](admin-manual-synchronization-of-table-mappings.md)  
[Programación de una sincronización entre Business Central y [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Acerca de la integración de Dynamics 365 Business Central con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
