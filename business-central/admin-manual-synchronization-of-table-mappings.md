---
title: Sincronización manual de asignaciones de tablas | Documentos de Microsoft
description: La sincronización copia los datos entre las entidades de Common Data Service y Business Central para mantener actualizados ambos sistemas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: ba79088bc386a856f1b3e7727f1f778ebabb7d51
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911335"
---
# <a name="manually-synchronize-table-mappings"></a>Sincronizar manualmente las asignaciones de tablas
Una asignación de tabla de integración asocia una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] (tipo de registro), como un cliente, con una entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)], como una cuenta. La sincronización de una asignación de tablas de integración le permite sincronizar los datos de todos los registros de la tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de la entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] que están emparejadas. Además, dependiendo de la configuración de la asignación de tablas, la sincronización puede crear y emparejar nuevos registros en la solución de destino para los registros desemparejados en el origen.  

La sincronización manual de las asignaciones de tablas de integración puede ser útil durante la configuración inicial de una integración y al diagnosticar errores de sincronización.  

Este artículo describe tres métodos para sincronizar manualmente las asignaciones de tablas de integración. Cada método proporciona un nivel diferente de sincronización.

## <a name="run-a-full-synchronization"></a>Ejecutar una sincronización completa
Una sincronización completa ejecuta todos los trabajos de sincronización de integración predeterminados para sincronizar registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y entidades de [!INCLUDE[d365fin](includes/cds_long_md.md)], tal como se define en la página **Asignaciones de tablas de integración**. 

Una sincronización completa realiza las siguientes operaciones para los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[d365fin](includes/cds_long_md.md)] que son:

* No emparejado, se creará un nuevo registro coincidente y se emparejará en la solución opuesta.
Si se crea un registro, y dónde se crea, depende de la dirección de sincronización. Por ejemplo, al sincronizar datos desde los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] con cuentas de [!INCLUDE[d365fin](includes/cds_long_md.md)], si hay un cliente que no está emparejado con una cuenta, se agregará automáticamente una cuenta nueva en [!INCLUDE[d365fin](includes/cds_long_md.md)] que se emparejará con el cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lo contrario se aplica cuando la dirección de sincronización es de [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para cada cuenta que aún no esté emparejada con un cliente, se creará un nuevo cliente coincidente en [!INCLUDE[d365fin](includes/d365fin_md.md)] y se emparejará con la cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  Para lograr esto, la operación de sincronización completa desactiva temporalmente la opción **Sincronizar solo reg. emparejados** en la asignación de tablas de integración que utiliza el trabajo de sincronización. Al final del proceso de sincronización completa, se le preguntará si desea mantener esta opción desactivada para todos los trabajos.  

* Emparejado, la dirección de sincronización (por ejemplo, de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)] o de [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]) está predeterminada por las asignaciones de tablas de integración. Para obtener más información, consulte [Asignación de entidad estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Normalmente, solo se utiliza la sincronización completa cuando se configura inicialmente la integración entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)], y solo una de las soluciones contiene datos, que se desea copiar en la otra solución. Una sincronización completa puede ser útil en un entorno de demostración. Debido a que la sincronización completa crea y asocia registros automáticamente entre las soluciones, es más rápido empezar a trabajar con la sincronización de datos entre registros. Por otro lado, solo debe ejecutar una sincronización completa si desea que se incluya un registro de [!INCLUDE[d365fin](includes/d365fin_md.md)] para cada registro de [!INCLUDE[d365fin](includes/cds_long_md.md)] para las asignaciones de tabla indicadas. De lo contrario, puede tener registros no deseados o duplicados en [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[d365fin](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Para ejecutar una sincronización completa  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de la conexión de Common Data Service** y luego elija el enlace relacionado.

    > [!NOTE]
    > Si desea ejecutar una sincronización completa para entidades a través de Dynamics 365 Sales, use la página **Configuración de la conexión de Microsoft Dynamics 365 Sales** en su lugar.

2.  Seleccione la acción **Ejecutar sincronización completa** y, a continuación, el botón **Sí**.  
3.  Una vez finalizada la sincronización completa, puede especificar si desea permitir que los trabajos de sincronización programados creen nuevos registros.  

    Si desea que todos los trabajos de sincronización creen nuevos registros en el destino para registros desemparejados en el origen, seleccione **Sí**. Esto establece el campo **Sincronizar solo reg. emparejados** en las asignaciones de tablas que utilizan los trabajos de sincronización.  

    Si desea que los trabajos de sincronización se ejecuten como antes de la sincronización completa con respecto a la creación de nuevos registros, seleccione **No**. Esto establece el campo **Sincronizar solo reg. emparejados** a la configuración que tenía antes de la sincronización completa.  

Puede ver los resultados de la sincronización completa en la página **Trabajos de sincronización de integración**. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Sincronización de todos los registros modificados
Puede utilizar la página **Configuración de la conexión de CDS** para sincronizar los cambios en los datos de todas las asignaciones de tablas de integración. Es similar a una sincronización completa. Sincronizará los datos de todos los registros emparejados en las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y las entidades de [!INCLUDE[d365fin](includes/cds_long_md.md)] definidas en las asignaciones de tablas. De forma predeterminada, solo se sincronizarán los registros que se hayan modificado desde la última vez que se sincronizaron. Los trabajos de sincronización sincronizan las asignaciones de tablas en el siguiente orden para evitar dependencias de emparejamiento entre las entidades:  

1.  DIVISA  
2.  VENDEDORES  
3.  PROVEEDOR  
4.  CLIENTE  
5.  CONTACTOS  

Puede ver los resultados de la sincronización en la página **Trabajos de sincronización de integración**. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Al modificar previamente la asignación de tabla de integración, puede configurar la sincronización con filtros para controlar qué registros se sincronizan o configurarla para crear nuevos registros en la solución de destino para registros desemparejados en el origen. Para obtener más información, consulte [Modificar asignaciones de tablas para la sincronización](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Para sincronizar los registros para todas las tablas  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de la conexión de Microsoft Dynamics 365 Sales** y luego elija el enlace relacionado.
2.  Elija la acción **Sincronizar registros modificados** y, a continuación, seleccione **Si**.  

## <a name="synchronize-individual-table-mappings"></a>Sincronizar las asignaciones de tablas individuales
Puede utilizar la página **Lista de asignaciones de tablas de integración** para ejecutar asignaciones de tabla específicas de un trabajo de sincronización. Esto sincronizará los datos de todos los registros emparejados en la tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y la entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] definidas mediante las asignaciones de tablas. De forma predeterminada, solo se sincronizarán los registros que se hayan modificado desde la última vez que se sincronizaron.  

Al modificar la asignación de tablas de integración por adelantado, puede configurar el trabajo de sincronización para crear nuevos registros en la solución de destino para registros desemparejados en el origen.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Para sincronizar los registros de asignación de tabla de integración  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignaciones de tablas de integración** y luego elija el enlace relacionado.
2.  Elija la acción **Sincronizar registros modificados** y, a continuación, seleccione **Si**.  

## <a name="see-also"></a>Consulte también  
[Sincronización de Business Central y Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   
