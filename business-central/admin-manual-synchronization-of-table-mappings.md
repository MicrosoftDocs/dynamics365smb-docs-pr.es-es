---
title: Sincronización manual de asignaciones de tablas | Documentos de Microsoft
description: La sincronización copia los datos entre tablas de Microsoft Dataverse y Business Central para mantener actualizados ambos sistemas.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="manually-synchronize-table-mappings"></a>Sincronizar manualmente las asignaciones de tablas


Una asignación de tabla de integración asocia una tabla de [!INCLUDE[prod_short](includes/prod_short.md)], como un cliente, con una tabla de [!INCLUDE[prod_short](includes/cds_long_md.md)], como una cuenta. La sincronización de una asignación de tablas de integración le permite sincronizar los datos de todos los registros de la tabla de [!INCLUDE[prod_short](includes/prod_short.md)] y de la tabla de [!INCLUDE[prod_short](includes/cds_long_md.md)] que están emparejadas. Además, dependiendo de la configuración de la asignación de tablas, la sincronización puede crear y emparejar nuevos registros en la solución de destino para los registros desemparejados en el origen.  

La sincronización manual de las asignaciones de tablas de integración puede ser útil durante la configuración inicial de una integración y al diagnosticar errores de sincronización.  

Este artículo describe tres métodos para sincronizar manualmente las asignaciones de tablas de integración. Cada método proporciona un nivel diferente de sincronización.

## <a name="run-a-full-synchronization"></a>Ejecutar una sincronización completa
Una sincronización completa ejecuta todos los trabajos de sincronización de integración predeterminados para sincronizar registros de [!INCLUDE[prod_short](includes/prod_short.md)] y tablas de [!INCLUDE[prod_short](includes/cds_long_md.md)], tal como se define en la página **Asignaciones de tablas de integración**. 

Una sincronización completa realiza las siguientes operaciones para los registros de [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[prod_short](includes/cds_long_md.md)] que son:

* No emparejado, se creará una nueva fila coincidente y se emparejará en la solución opuesta.
Si se crea una fila, y dónde se crea, depende de la dirección de sincronización. Por ejemplo, al sincronizar datos desde los clientes de [!INCLUDE[prod_short](includes/prod_short.md)] con cuentas de [!INCLUDE[prod_short](includes/cds_long_md.md)], si hay un cliente que no está emparejado con una cuenta, se agregará automáticamente una cuenta nueva en [!INCLUDE[prod_short](includes/cds_long_md.md)] que se emparejará con el cliente en [!INCLUDE[prod_short](includes/prod_short.md)]. Lo contrario se aplica cuando la dirección de sincronización es de [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)]. Para cada cuenta que aún no esté emparejada con un cliente, se creará un nuevo cliente coincidente en [!INCLUDE[prod_short](includes/prod_short.md)] y se emparejará con la cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  Para lograr esto, la operación de sincronización completa desactiva temporalmente la opción **Sincronizar solo reg. emparejados** en la asignación de tablas de integración que utiliza el trabajo de sincronización. Al final del proceso de sincronización completa, se le preguntará si desea mantener esta opción desactivada para todos los trabajos.  

* Emparejado, la dirección de sincronización (por ejemplo, de [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[prod_short](includes/cds_long_md.md)] o de [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)]) está predeterminada por las asignaciones de tablas de integración. Para obtener más información, consulte [Asignación de tabla estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Normalmente, solo se utiliza la sincronización completa cuando se configura inicialmente la integración entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)], y solo una de las soluciones contiene datos, que se desea copiar en la otra solución. Una sincronización completa puede ser útil en un entorno de demostración. Debido a que la sincronización completa crea y asocia registros automáticamente entre las soluciones, es más rápido empezar a trabajar con la sincronización de datos entre registros. Por otro lado, solo debe ejecutar una sincronización completa si desea que se incluya una fila de [!INCLUDE[prod_short](includes/prod_short.md)] para cada fila de [!INCLUDE[prod_short](includes/cds_long_md.md)] para las asignaciones de tabla indicadas. De lo contrario, puede tener registros no deseados o duplicados en [!INCLUDE[prod_short](includes/prod_short.md)] o [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Para ejecutar una sincronización completa
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Dataverse** y luego elija el enlace relacionado.

    > [!NOTE]
    > Si desea ejecutar una sincronización completa para tablas a través de Dynamics 365 Sales, use la página **Configuración de la conexión de Microsoft Dynamics 365 Sales** en su lugar.

2.  Seleccione la acción **Ejecutar sincronización completa** y, a continuación, el botón **Sí**.  
3.  Una vez finalizada la sincronización completa, puede especificar si desea permitir que los trabajos de sincronización programados creen nuevos registros.  

    Si desea que todos los trabajos de sincronización creen nuevos registros en el destino para registros desemparejados en el origen, seleccione **Sí**. Esto establece el campo **Sincronizar solo reg. emparejados** en las asignaciones de tablas que utilizan los trabajos de sincronización.  

    Si desea que los trabajos de sincronización se ejecuten como antes de la sincronización completa con respecto a la creación de nuevos registros, seleccione **No**. Esto establece el campo **Sincronizar solo reg. emparejados** a la configuración que tenía antes de la sincronización completa.  

Puede ver los resultados de la sincronización completa en la página **Trabajos de sincronización de integración**. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Sincronización de todos los registros modificados
Puede utilizar la página **Configuración de la conexión de Common Data Service** para sincronizar los cambios en los datos de todas las asignaciones de tablas de integración. Es similar a una sincronización completa. Sincronizará los datos de todos los registros emparejados en las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] definidas en las asignaciones de tablas. De forma predeterminada, solo se sincronizarán los datos que se hayan modificado desde la última sincronización. Los trabajos de sincronización sincronizan las asignaciones de tablas en el siguiente orden para evitar dependencias de emparejamiento entre las tablas:  

1.  DIVISA  
2.  VENDEDORES  
3.  PROVEEDOR  
4.  CLIENTE  
5.  CONTACTOS  

Puede ver los resultados de la sincronización en la página **Trabajos de sincronización de integración**. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Al modificar previamente la asignación de tabla de integración, puede crear filtros para controlar qué datos se sincronizan o configurar asignaciones para crear nuevos datos en la solución de destino para registros o filas desemparejados en el origen. Para obtener más información, consulte [Modificar asignaciones de tablas para la sincronización](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-data-for-all-tables"></a>Para sincronizar los datos para todas las tablas
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Microsoft Dynamics 365 Sales** y luego elija el enlace relacionado.
2.  Elija la acción **Sincronizar registros modificados** y, a continuación, seleccione **Si**.  

## <a name="synchronize-individual-table-mappings"></a>Sincronizar las asignaciones de tablas individuales
Puede utilizar la página **Lista de asignaciones de tablas de integración** para ejecutar un trabajo de sincronización para asignaciones de tabla. Esto sincronizará los datos de todos los registros y filas emparejados en las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] definidas mediante las asignaciones de tablas. De forma predeterminada, solo se sincronizarán los datos que se hayan modificado desde la última sincronización.  

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Para sincronizar los registros de asignación de tabla de integración
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignaciones de tabla de integración** y luego elija el enlace relacionado.
2.  Elija la acción **Sincronizar registros modificados** y, a continuación, seleccione **Si**.  

## <a name="see-also"></a>Consulte también
[Sincronización de Business Central y Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
