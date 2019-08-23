---
title: Sincronización de Business Central y Dynamics 365 for Sales | Documentos de Microsoft
description: Obtenga información sobre la sincronización de datos entre Business Central y Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/16/2019
ms.author: bholtorf
ms.openlocfilehash: 9290730bb559d4ac03a437a49ed81b09f3c01853
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755223"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Programación de una sincronización entre Business Central y Dynamics 365 for Sales
Puede sincronizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] en intervalos programados configurando proyectos en la cola de proyectos. Los proyectos de sincronización sincronizan los datos de los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de los registros de [!INCLUDE[crm_md](includes/crm_md.md)] que se han emparejado previamente. O, para registros que no se han emparejado, según la dirección y las reglas de sincronización, los proyectos de sincronización pueden crear y emparejar registros nuevos en el sistema de destino. Hay varios trabajos de sincronización que están disponibles de forma inmediata. Puede verlos en la página de **Movimientos de cola de proyectos**. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Proceso de sincronización  
Cada movimiento de cola de proyectos de sincronización utiliza una asignación de tabla de integración concreta que especifica qué tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y entidad de [!INCLUDE[crm_md](includes/crm_md.md)] se deben sincronizar. Las asignaciones de tabla también incluyen configuraciones que controlan qué registros de la tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de la entidad de [!INCLUDE[crm_md](includes/crm_md.md)] se deben sincronizar.  

Para sincronizar datos, los registros de entidad de [!INCLUDE[crm_md](includes/crm_md.md)] deben emparejarse con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, un cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)] debe emparejarse con una cuenta de [!INCLUDE[crm_md](includes/crm_md.md)]. Puede configurar los emparejamientos manualmente, antes de ejecutar los proyectos de sincronización o permitir que los proyectos de sincronización configuren emparejamientos automáticamente. La lista siguiente describe cómo los datos se sincronizan entre [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se utilizan los movimientos de la cola de proyectos de sincronización. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md). 

-   De manera predeterminada, solo se sincronizan los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] que están emparejados con registros de [!INCLUDE[crm_md](includes/crm_md.md)]. Puede cambiar la asignación de tabla entre una entidad de [!INCLUDE[crm_md](includes/crm_md.md)] y una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)], de manera que los proyectos de sincronización de integración creen los registros nuevos en la base de datos de destino para cada registro de la base de datos de origen que no esté emparejado. Los nuevos registros también se emparejan con los registros correspondientes en el origen. Por ejemplo, al sincronizar clientes con cuentas de [!INCLUDE[crm_md](includes/crm_md.md)], se crea un nuevo registro de cuenta para cada cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Las cuentas nuevas se emparejan automáticamente con clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Como la sincronización en este caso es bidireccional, se crea un cliente nuevo y se empareja para cada cuenta de [!INCLUDE[crm_md](includes/crm_md.md)] que aún no está emparejada.  

    > [!NOTE]  
    > Existen reglas y filtros que determinan qué datos se sincronizan. Para obtener más información, vea [Reglas de sincronización](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Cuando se crean nuevos registros en [!INCLUDE[d365fin](includes/d365fin_md.md)], los registros utilizan la plantilla definida para la asignación de tablas de integración o la plantilla predeterminada que está disponible para el tipo de registro. Los campos se rellenan con datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[crm_md](includes/crm_md.md)] dependiendo de la dirección de sincronización. Para obtener más información, consulte [Procedimiento: modificar asignaciones de tablas para la sincronización](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   En las sincronizaciones posteriores, solo se actualizarán los registros que se hayan modificado o agregado después del último proyecto de sincronización correcto para la entidad.  

     Los nuevos registros de [!INCLUDE[crm_md](includes/crm_md.md)] se agregan en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si los datos de los campos de los registros de [!INCLUDE[crm_md](includes/crm_md.md)] se han modificado, los datos se copian en el campo correspondiente de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Con la sincronización bidireccional, el proyecto se sincroniza de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] y, a continuación, de [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Movimientos de la cola de proyectos de sincronización predeterminados  
La tabla siguiente describe los proyectos de sincronización predeterminados.  

|Mov. cola proyecto|Descripción|Dirección|Asignación de tablas de integración|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|Proyecto de sincronización de CONTACTO - Dynamics 365 for Sales|Sincroniza los contactos de [!INCLUDE[crm_md](includes/crm_md.md)] con los contactos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidireccional|CONTACTO|  
|Proyecto de sincronización de DIVISA - Dynamics 365 for Sales|Sincroniza las divisas de transacciones de [!INCLUDE[crm_md](includes/crm_md.md)] con las divisas de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|DIVISA|  
|Proyecto de sincronización de CLIENTE - Dynamics 365 for Sales|Sincroniza las cuentas de [!INCLUDE[crm_md](includes/crm_md.md)] con los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].|Bidireccional|CLIENTE|  
|Proyecto de sincronización de CUSTPRCGRP-PRICE - Dynamics 365 for Sales|Sincroniza las listas de precios de venta de [!INCLUDE[crm_md](includes/crm_md.md)] con los grupos de precios de los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GRUPOS DE PRECIOS DE CLIENTES-LISTAS DE PRECIOS DE VENTA|
|Proyecto de sincronización de ARTÍCULO-PRODUCTO - Dynamics 365 for Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los artículos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|ARTÍCULO-PRODUCTO|
|Proyecto de sincronización de POSTEDSALESINV-INV - Dynamics 365 for Sales|Sincroniza las facturas de [!INCLUDE[crm_md](includes/crm_md.md)] con facturas de ventas registradas de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURAS-FACTURAS DE VENTAS REGISTRADAS|
|Proyecto de sincronización de RECURSO-PRODUCTO - Dynamics 365 for Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los recursos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|RECURSO-PRODUCTO|  
|Proyecto de sincronización de VENDEDORES - Dynamics 365 for Sales|Sincroniza los vendedores de [!INCLUDE[d365fin](includes/d365fin_md.md)] con los usuarios de [!INCLUDE[crm_md](includes/crm_md.md)].|De [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]|VENDEDORES|
|Proyecto de sincronización de SALESPRC-PRODUCTPRICE - Dynamics 365 for Sales|Sincroniza los precios de producto de [!INCLUDE[crm_md](includes/crm_md.md)] con los precios de venta de [!INCLUDE[d365fin](includes/d365fin_md.md)].||PRECIO DEL PRODUCTO-PRECIO DE VENTA|
|Proyecto de sincronización de UNITOFMEASURE - Dynamics 365 for Sales|Sincroniza los grupos de unidad de [!INCLUDE[crm_md](includes/crm_md.md)] con las unidades de medida de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|UNIDAD DE MEDIDA|  
|Estadísticas de clientes: sincronización de Dynamics 365 for Sales|Actualiza las cuentas de [!INCLUDE[crm_md](includes/crm_md.md)] con los últimos datos de los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)]. En [!INCLUDE[crm_md](includes/crm_md.md)], la información se muestra en el formulario de vista rápida **Estadísticas de la cuenta de Business Central** de cuentas que están emparejadas con los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Estos datos también pueden actualizarse manualmente desde cada registro de cliente. Para obtener más información, consulte [Procedimiento: emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Nota:** este movimiento de la cola de proyectos es relevante solo si la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] está instalada en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Acerca de la solución de integración de Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|No aplicable.|No aplicable.|   

## <a name="to-view-the-synchronization-job-log"></a>Para ver el registro de proyectos de sincronización  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Registro de sincronización de integración** y luego elija el enlace relacionado.
2.  Si se generan uno o más errores para un proyecto de sincronización, el número de errores aparece en la columna **Erróneo**. Para ver los errores del proyecto, elija el número.  

    > [!TIP]  
    > Puede ver todos los errores del proyecto de sincronización abriendo el registro de errores del proyecto de sincronización directamente.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Para ver el registro del proyecto de sincronización desde las asignaciones de tabla  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Lista de asignaciones de tablas de integración** y luego elija el enlace relacionado.
2.  En la página **Lista de asignaciones de tablas de integración**, seleccione un movimiento y después seleccione **Registro de trabajo de sinc. de integración**.  

## <a name="to-view-the-synchronization-error-log"></a>Para ver el registro de errores de sincronización  
* Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Errores de sincronización de integración** y luego elija el enlace relacionado.

## <a name="see-also"></a>Consulte también  
[Sincronización de datos en Business Central y Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Sincronizar manualmente las asignaciones de tablas](admin-manual-synchronization-of-table-mappings.md)  
[Programación de una sincronización entre Business Central y Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Acerca de la integración de Dynamics 365 Business Central con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



